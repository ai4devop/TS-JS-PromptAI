# 📝 Exercise4 - Self-Evaluation ~ 10 minutes

Self-evaluation involves asking the model to assess itself using specific criteria. In this exercise, we apply this method to TypeScript scenarios.

## 1️⃣ Use Case 1: Create a Prompt for the Model to List Comprehensive Items to Test a TypeScript Component

Possible example:

```typescript
// Ask your AI to give you a list to test this method
// Function that validates an email address
function validateEmail(email: string): boolean {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return emailRegex.test(email);
}
```

Now it's your turn to integrate your prompt below: 👀

```typescript
write a list of string that test this function.
```

What was the response?

```typescript
Here is a list of example strings to test the validateEmail function:
1. "test@example.com" (Valid)
2. "user@domain.co.uk" (Valid)
3. "invalid-email" (Invalid)
4. "test@.com" (Invalid)
5. "name@domain@domain.com" (Invalid)
6. "user@domain.c" (Valid but borderline)
7. "user@sub.domain.com" (Valid)
8. "" (Empty string, invalid)
9. "plainaddress" (Invalid)
10. "user@domain..com" (Invalid)
It is important to cover these cases to check the boundaries and effectiveness of the validateEmail function.
```

## 2️⃣ Use Case 2: Ask the Model if It Can Provide More Possibilities

Possible example:

```typescript
Ask the model if it can provide more possibilities.
```

Now it's your turn to integrate your prompt below:  👀

```typescript
Can you provide other examples of strings to test the validateEmail function?

```

What was the response?

```typescript
Certainly! Here are some additional examples to broaden test coverage:
11. "email@123.123.123.123" (Valid, IP address)
12. "user@[IPv6:2001:db8::1]" (Valid, IPv6)
13. ".user@domain.com" (Invalid, leading dot)
14. "user@domain.web" (Valid, custom domain)
15. "user@domain" (Invalid, incomplete domain)
16. "user@.domain.com" (Invalid, dot after @)
17. "user@domain..com" (Invalid, double dot)
These additional examples allow testing of less common but potentially problematic cases for email validation.
```

## 3️⃣ Use Case 3: Ask the Model to Self-Evaluate and Improve Its Response

Possible example:

```typescript
Ask the model to self-evaluate and improve its response.
```

Now it's your turn to integrate your prompt below: 👀

```typescript
Is the list of strings sufficient to fully test the validateEmail function? If not, how can it be improved?
```

What was the response?

```typescript
The list provided covers many common cases, but it can be improved by adding cases specific to current email standards and considering some rarer configurations. Here are potential improvements:
1. **International Character Cases**: Add emails with Unicode characters to test if the function can handle usernames or domains in other alphabets.
   - Example: "名@例.com" (Valid)
2. **More than 64 Characters Before the @ Symbol**: Email addresses can have up to 64 characters before the @.
   - Example: "longemailaddresslongemailaddresslongemailaddresslongemailaddress@domain.com" (Valid)
3. **Domain Without Extension Case**: Test domains that do not have traditional domain extensions.
   - Example: "user@localhost" (Potentially valid in some environments)

By considering these additional cases, you will achieve more comprehensive validation of the validateEmail function.
```
