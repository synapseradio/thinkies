---
name: anticipating-failure-modes
description: Systematically enumerate how code can fail to prevent claiming safety without evidence
---

# Anticipating Failure Modes

Enumerate specific ways code can fail rather than assuming it works.

## Instructions

When I review or write code, I systematically identify failure scenarios before claiming the code is safe or robust.

1. **Examine inputs** - I question what happens with null, undefined, empty strings, negative numbers, arrays with zero or millions of items, objects missing expected properties, or values outside expected ranges, because inputs rarely arrive in the perfect form I imagine.

2. **Consider environment** - I identify dependencies on networks, filesystems, databases, external APIs, or third-party services that could be unreachable, slow, or returning unexpected responses, because the world outside the process boundary is unreliable.

3. **Analyze state** - I look for race conditions between async operations, concurrent access to shared resources, stale cached data, or assumptions that state hasn't changed since it was last checked, because time and concurrency introduce failure modes that don't exist in synchronous code.

4. **Check resources** - I consider whether memory allocations could fail, disk space could be exhausted, connection pools could be depleted, or operations could timeout, because finite resources eventually run out under load or long execution times.

5. **Question logic** - I examine boundary conditions like off-by-one errors, division by zero, assumptions about sort order or uniqueness, and whether the code handles the first item, last item, and empty collection correctly, because logic that works for typical cases often breaks at boundaries.

6. **Trace errors** - I follow how exceptions propagate through the call stack, whether errors are caught and handled or silently swallowed, and if failures in one operation leave the system in an inconsistent state, because error paths are often untested and unhandled.

7. **Validate recovery** - I verify whether the code includes retries, fallbacks, circuit breakers, or graceful degradation when failures occur, and whether it logs enough information to diagnose production failures, because systems that fail loudly and recoverably are easier to operate than those that fail silently.

## Examples

### Reviewing an API endpoint

I'm reviewing a POST endpoint that creates user accounts. The happy path looks clean: it extracts email and password from the request body, hashes the password, inserts into the database, and returns the new user. But I systematically enumerate failure modes. For inputs, what if email is null, an empty string, or missing the @ symbol? What if password is undefined or an empty string? The code assumes both exist. For environment, what if the database connection fails during insert, or another user with that email is created between the uniqueness check and insert? There's a race condition. For logic, what if the email is 10,000 characters and breaks the database column width? For errors, if hashing throws an exception, does it return a 500 or a useful error? I find the code has no input validation, no handling for duplicate key violations, no maximum length checks, and errors would expose stack traces to clients.

### Analyzing async payment processing

I'm examining code that processes payments by calling a third-party API and updating order status. It awaits the API call, then updates the database. Systematically checking failures: For environment, what if the API is unreachable, times out after 30 seconds, returns a 500 error, or returns success but the payment actually failed? What if the network drops after the payment succeeds but before we receive the response? For state, what if another process already processed this payment? There's no idempotency check. For resources, if this runs for thousands of concurrent payments, could we exhaust API rate limits or database connections? For errors, if the database update fails after the payment succeeds, the customer is charged but the order stays pending - there's no transaction across the boundary. For recovery, there's no retry logic, no webhook to handle delayed confirmations, and no way to reconcile payments with order status later. The code works perfectly in ideal conditions but has catastrophic failure modes in production.

### Evaluating data transformation

I'm reviewing a function that transforms API response data into domain objects. It maps over an array of items, extracting nested properties and parsing dates. Checking systematically: For inputs, what if the array is empty, null, or undefined? The map would throw. What if an item is missing the nested property path? Optional chaining isn't used, so it throws. What if the date string is invalid or in an unexpected format? Date parsing silently returns Invalid Date. For logic, what if the array has a million items - does mapping them all into memory cause issues? What if some items are valid and others aren't - does one bad item fail the entire batch? For errors, exceptions bubble up uncaught, so the caller can't distinguish between "no data" and "malformed data". The code needs input validation before mapping, error handling within the map to skip or collect invalid items, and consideration of whether to process large arrays in chunks.

## When to use this skill

- I catch myself describing code as "safe" or "robust" without having enumerated specific failure scenarios
- I'm reviewing code and only noting what it does in the happy path without considering what goes wrong
- I'm about to approve changes without asking "how could this fail in production"
- I find myself assuming inputs are valid, services are available, and operations succeed without evidence
- I'm writing code and thinking "this should work" rather than "I've verified how this fails"
- I notice I'm testing only successful cases without exercising error paths
- I'm recommending patterns or approaches without considering their failure modes under load or adverse conditions

## Related Skills

- `edge-finder` - Identify boundary conditions and edge cases that reveal failure modes
- `trace-flow` - Follow execution paths through error handling and exception propagation
- `blast-radius` - Assess impact when anticipated failures actually occur in production
