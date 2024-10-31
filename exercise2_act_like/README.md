# 📝 Exercise2 - Act Like ~ 10 minutes

"Act like" involves asking the model to behave as a specific person or role. In this case, we use it to get advice on developing features in TypeScript.

## 1️⃣ Use Case 1: Create a Prompt for the Model to Provide Steps for Developing a TypeScript Project and Highlight Key Points

Possible example:
```typescript
Act like an experienced TypeScript developer. What should not be forgotten when developing a secure API in TypeScript?
```

Now it's your turn to integrate your prompt below: 👀

```typescript
Create a prompt for the model to provide steps for developing a TypeScript project and highlight key points.
```

What was the response?
```typescript
As an experienced TypeScript developer, here’s what should not be forgotten when developing a secure API:
1. **Input Validation**: Use libraries like `zod` or `Joi` to validate incoming data and prevent SQL injection or other input-based attacks.
2. **Error Handling**: Implement consistent error handling so the API returns appropriate error messages without exposing sensitive information.
3. **Authentication and Authorization**: Implement authentication via JWT and ensure users have appropriate permissions to access routes.
4. **Encryption of Sensitive Data**: Use libraries like `crypto` to secure sensitive data, especially passwords, before storage.
5. **Security Testing**: Write unit and integration tests with tools like `Jest` to ensure your API is secure and functions as expected.
```

## 2️⃣ Use Case 2: Create a Prompt for the Model to Assist by Acting as a Specialized Expert

Possible example:
```typescript
Act like a web application security expert. What needs to be integrated into a TypeScript API to ensure compliance with OWASP standards?
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Create a prompt for the model to assist by acting as a specialized expert.
```

What was the response?
```typescript
As a web application security expert, here’s what should be integrated into a TypeScript API for OWASP compliance:
1. **Injection Prevention**: Use ORMs like TypeORM to interact with your database and prevent SQL injection.
2. **Session Management Security**: Ensure JWT tokens are well-signed and have limited lifespan to prevent exploitation.
3. **Encryption of Sensitive Data**: All sensitive data such as passwords or personal information must be encrypted before storage.
4. **Error Management Without Information Leakage**: Never return full errors to end users. Use an error-handling middleware to return generic messages.
5. **Protect Against CSRF and XSS Attacks**: Use CSRF tokens and validate user input to prevent XSS attacks.

By following these recommendations, you’ll ensure compliance with OWASP’s best security practices.
```

## 3️⃣ Use Case 3: Compare Your Two Responses and Test Other Response Structures

Possible example:
```typescript
Act like a Lead Dev TypeScript in a development team. What are the design principles to never forget when creating a new service in TypeScript?
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Compare your two responses and test other response structures.
```

What was the response?
```typescript
As a Lead Dev TypeScript, here are the design principles to never forget:
1. **SOLID Principles**: Ensure each module and function follows SOLID principles for maintainable and scalable code.
2. **Strict Types and Advanced Typing**: Use TypeScript's advanced typing features such as generics and union types to ensure code robustness.
3. **Testability**: Focus on writing modular and testable code. Each service should have unit and integration tests.
4. **Design Patterns**: Use suitable design patterns like the "Repository" pattern for database communication management.
5. **Clear Documentation**: Document each function and class to facilitate other developers’ work and ensure team consistency.
```

