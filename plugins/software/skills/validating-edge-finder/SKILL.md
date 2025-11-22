---
name: edge-finder
description: Systematically discover edge cases through boundary analysis and input space exploration
---

# Edge Finder

Uncover edge cases by mapping input boundaries and exploring what happens at the limits of expected behavior.

## Instructions

When I need to verify correctness or test assumptions, I systematically explore the boundary conditions and extreme cases that reveal where code breaks down.

1. **Map the input space** - I identify every input the code accepts, noting their types, valid ranges, and documented constraints, because edge cases live at the boundaries of what's explicitly handled versus what's merely assumed.

2. **Find natural boundaries** - I locate the limits in each input domain such as zero, negative numbers, empty collections, null values, maximum sizes, and special sentinel values, as these boundaries are where assumptions often fail.

3. **Test boundary conditions** - I trace through the code with values at, just before, and just beyond each boundary, observing whether the code handles these cases explicitly or relies on implicit assumptions that might not hold.

4. **Identify implicit assumptions** - I look for what the code assumes but doesn't validate, like assuming arrays are non-empty, numbers are positive, strings contain valid data, or operations complete in order, since unvalidated assumptions are where bugs hide.

5. **Explore parameter interactions** - I examine how combinations of parameters behave, especially when multiple inputs are at their boundaries simultaneously, because code might handle each edge case individually but fail when they combine.

6. **Consider temporal boundaries** - I think about timing-related edges like race conditions, operation ordering, timeout boundaries, retry limits, and state transitions, as these temporal edges are often overlooked in spatial boundary analysis.

7. **Validate coverage** - I check whether I've explored the complete boundary surface by asking what happens at every limit, transition, and extreme, ensuring no assumption remains untested and no boundary unexplored.

## Examples

### Finding edges in pagination logic

I'm reviewing a function that fetches paginated results with `getItems(page, pageSize)`. Mapping the input space, I see two numeric parameters. The natural boundaries are page=0, page=1, negative pages, pageSize=0, pageSize=1, very large pageSizes, and negative pageSizes. Tracing with page=0, I discover the code calculates offset as `(page - 1) * pageSize`, which gives -1 for page 0, likely causing an error or returning wrong data. Testing pageSize=0 reveals a division by zero when calculating total pages. Checking the interaction of page=1000000 with pageSize=1000000 shows the offset calculation could overflow. I also notice no upper bound on pageSize, meaning someone could request pageSize=999999999 and exhaust memory. The temporal edge appears when considering concurrent requests with changing data between pages. These edges reveal the code assumes page >= 1, pageSize > 0, and reasonable memory constraints, but validates none of these.

### Finding edges in email validation

I'm examining an email validator that uses a regex pattern and checks for an @ symbol. The input space is strings of arbitrary length and content. Natural boundaries include empty string, null, undefined, single character, very long strings, and strings with special characters. Testing the empty string, I find it passes validation because the code checks `email.includes('@')` but doesn't ensure anything comes before or after the @. With '@', it validates successfully despite being invalid. Testing 'a@' and '@b' both pass. Looking at length boundaries, I try a 10000 character email and discover the regex causes catastrophic backtracking, hanging the validator. Testing unicode reveals 'user@domain.com\u200B' (with zero-width space) passes but won't work as an email. Checking null and undefined, I find the code crashes with "Cannot read property 'includes' of null" because it assumes a string. The interaction between multiple @ symbols like 'a@@b' passes the includes check. These edges show the code assumes non-empty strings with exactly one @ and ASCII characters, but only validates that @ exists somewhere.

### Finding edges in cache invalidation

I'm reviewing a caching system where `updateUser(userId, data)` updates the database and invalidates `cache.delete(userId)`. The input space includes userId values and the cache state. Natural boundaries are null userId, empty string userId, non-existent users, and cache states (empty, full, mid-update). Tracing with userId=null shows the cache delete succeeds but database update fails, leaving the cache in a stale state. Testing rapid sequential updates reveals a race condition: if two updates for the same user happen simultaneously, both invalidate the cache, both write to database, but the order is non-deterministic, so the final cached value might be from the earlier update. Examining the cache-full edge case, I discover that if cache deletion fails due to memory pressure, the update proceeds anyway, leaving stale data cached. Testing the boundary between update and read, I find a window where the cache is invalidated but new data isn't fetched yet, causing a stampede of database queries if multiple requests arrive during that window. The temporal edge of network partition means the cache and database could diverge. These edges reveal assumptions that operations are atomic, sequential, and always succeed, none of which are validated or handled.

## When to use this skill

- I catch myself claiming code is correct or handles all cases without having explored what happens at boundaries
- I'm about to validate a solution or approve an implementation based on happy path testing alone
- I notice I'm reasoning about typical inputs while ignoring atypical but valid ones
- I find myself assuming inputs will be well-formed, positive, non-empty, or within reasonable ranges without verification
- I'm confident about behavior without having tested zero, null, empty, maximum, minimum, or negative values
- I realize I haven't considered what happens when multiple edge conditions occur simultaneously
- I'm about to ship code or make claims about correctness without having mapped the boundary surface

## Related Skills

- `failure-modes` - Explore how systems fail after identifying edge cases that might trigger failures
- `trace-flow` - Follow execution paths at boundary conditions to understand exact behavior
- `blast-radius` - Assess impact after discovering edge cases that might affect multiple components
