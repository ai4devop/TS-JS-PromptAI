# 📝 Exercise9 - System / Policy Instructions ~ 10 minutes
System instructions or policy instructions set overarching rules the model should follow. You might specify style guides, corporate policy, or constraints that must be respected in any final output.

## 1️⃣ Use Case 1: Setting a Strict Coding Style Policy
Possible example:

```typescript
// System instruction (conceptually): "Always use camelCase for variables, and do not use 'var'—only 'let' or 'const' in TypeScript code."
// Then your actual user prompt might be: "Write a function that logs user login attempts."
```

1.System/Policy Prompt (written as if it’s a hidden “system” message):
```plaintext
"You must always use camelCase, never use 'var', and prefer 'const' over 'let' where possible."
```

User Prompt:
```typescript
// Write a function "logLoginAttempt" that takes a username (string) and a timestamp (Date).
// It should console.log: "<username> attempted login at <timestamp>".
```
Your turn:

Imagine you have a “system message” that imposes a coding style.
Provide the user-level prompt.
See if the model follows the style instructions.

System/Policy Prompt:

```plaintext
Write your system-level constraints here
```

User Prompt:

```typescript
Write your user prompt here
```

Model’s Response:

```typescript
Write AI response here
```

## 2️⃣ Use Case 2: Enforce a Documentation Standard

- Policy says: “All functions must have JSDoc comments.”
- See if the model includes them in the final answer.
