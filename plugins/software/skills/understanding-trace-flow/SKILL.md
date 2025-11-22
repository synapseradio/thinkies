---
name: trace-flow
description: Follow data and control flow through execution paths, state changes, and transformations to understand runtime behavior
---

# Trace Flow

Track how data moves, transforms, and controls execution as it flows through the system from input to output.

## Instructions

When I need to understand how data actually moves through code, I trace its journey step by step, watching how it transforms and what decisions it drives.

1. **Identify the starting point** - I locate where the data enters the system, whether that's a function parameter, API request, user input, or database query result, and note its initial shape and type so I know what I'm following.

2. **Track transformations** - I follow each operation that modifies the data, noting what changes at each step: mapping objects to different shapes, filtering arrays, parsing strings to numbers, or combining multiple sources into one structure.

3. **Observe control decisions** - I identify where the data determines program flow through conditionals, loops, or pattern matching, recognizing that data values decide which code paths execute and understanding the conditions that trigger each branch.

4. **Follow state changes** - I watch how data gets stored, updated, or deleted in variables, objects, databases, or caches, tracking not just the values but also when and why state mutates, as timing matters for correctness.

5. **Note side effects** - I mark every point where data causes effects beyond its transformation: logging, API calls, file writes, UI updates, or event emissions, since these effects are often the actual purpose of the flow.

6. **Trace error paths** - I follow what happens when data is invalid, missing, or unexpected, identifying where validation occurs, how errors propagate, and whether the system fails safely or leaves inconsistent state behind.

7. **Map the complete journey** - I verify I can explain the entire path from input to output without gaps, ensuring I understand every transformation and decision point, because missing one step means missing potential bugs or unexpected behavior.

## Examples

### Tracing user authentication flow

I'm debugging why some users can't log in. I start with the login request payload `{ email, password }` hitting the API endpoint. The email gets lowercased and trimmed in the route handler before passing to `AuthService.login()`. Inside the service, the email queries the database which returns a user object with `{ id, email, passwordHash, isActive }`. The password gets hashed using bcrypt with the stored salt, then compared to `passwordHash`. If they match AND `isActive` is true, the code generates a JWT with `{ userId: user.id, email: user.email }` as payload. The JWT gets stored in Redis with a 24-hour TTL and returned to the client as `{ token }`. The client stores it in localStorage and includes it in the Authorization header for subsequent requests. I discover the bug: inactive users get a valid token before the `isActive` check happens, because the check occurs after token generation instead of before.

### Tracing data transformation pipeline

I'm investigating why some product prices are displaying incorrectly. Starting with raw product data from the API `{ price_cents: 1299, currency: 'USD', tax_rate: 0.08 }`, I follow it into `normalizeProduct()` which converts `price_cents` to `price: 12.99` by dividing by 100. Then `calculateTax()` computes `taxAmount: 1.04` by multiplying price by tax_rate and rounding to 2 decimals. The `enrichProduct()` function adds `totalPrice: 14.03` by summing price and taxAmount. This object flows into React state where `formatPrice()` applies currency formatting to create `"$14.03"` for display. I trace a problematic case: when `price_cents` is 1000, dividing by 100 gives 10.00, but JavaScript floating point arithmetic in tax calculation yields `10 * 0.08 = 0.7999999999999999`, which rounds to 0.80 correctly. The bug is elsewhere: some products have null `tax_rate` causing NaN propagation, which I wouldn't have found without tracing the complete data flow including edge cases.

### Tracing event propagation

I need to understand why clicking a button sometimes triggers duplicate actions. The click event on `<Button onClick={handleSubmit}>` fires, calling `handleSubmit()` which dispatches `{ type: 'FORM_SUBMIT', payload: formData }` to Redux. The reducer updates state from `{ status: 'idle' }` to `{ status: 'submitting', data: formData }`. A Redux middleware intercepts this action and makes an API call. The API response triggers another dispatch `{ type: 'FORM_SUCCESS', payload: result }` updating state to `{ status: 'success', result }`. A `useEffect` watching the status field fires when status changes to 'success', which calls `onSuccess(result)` from props. I trace the duplicate: the parent component passes `onSuccess={() => navigate('/dashboard')}` but doesn't memoize it, so it creates a new function each render. The useEffect has `onSuccess` in its dependency array, causing it to rerun even when status hasn't changed. The real flow shows two separate mechanisms: Redux state change AND effect dependency change, both triggering navigation.

## When to use this skill

Use this skill when I need to ground my understanding in actual execution rather than assumptions:

- **When I'm making claims about runtime behavior** - If I'm about to explain "what this code does" based on reading alone, I should trace it to verify my mental model matches reality, especially with complex conditionals, state mutations, or async operations.

- **When the gap between static and dynamic matters** - Code that looks simple when reading may have non-obvious runtime behavior due to side effects, closure captures, event timing, or framework magic. If execution order or data mutations could surprise me, I need to trace.

- **When I'm reasoning about specific inputs** - General understanding of code structure differs from knowing what happens with particular data. If someone asks "what happens when X is null" or "why does Y fail with this input", I should trace that specific case rather than speculate.

- **When my assumptions could mislead** - Before claiming "this validates the data" or "this handles errors correctly" or "this is where the bug must be", I should verify by following the actual execution path. Intellectual honesty requires distinguishing what I've verified from what I've inferred.

- **When multiple paths or transformations create complexity** - If data flows through several functions, gets transformed multiple times, or branches based on conditions, my mental simulation is likely incomplete. Tracing reveals the details I'd miss by reasoning alone.

- **When I need to verify rather than explain** - Reading code tells me what could happen. Tracing tells me what does happen. Use this skill when the difference matters for correctness, security, or giving accurate advice.

## Related Skills

- `codebase-cartography` - Build the high-level map first, then use trace-flow to explore specific paths in detail
- `dependency-graph` - Understand what depends on what after tracing shows you the runtime relationships
- `failure-modes` - Use trace-flow to identify where things can go wrong in the data journey
- `edge-finder` - Trace edge cases and boundary conditions to find where data flow breaks down
