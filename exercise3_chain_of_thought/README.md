# 📝 Exercise3 - Chain of Thought ~ 10 minutes

The "chain of thought" technique involves guiding the model through a reasoning process to explain each step of the thought process. Here, we use this method to generate TypeScript documentation.

## 1️⃣ Use Case 1: Create a Prompt for the Model to Write Documentation for TypeScript Code

Possible example:

```typescript
Here is my code:
import express, { Request, Response } from 'express';
const app = express();
const port: number = 5000;
app.get('/clients/:clientId', (req: Request, res: Response): void => {
  res.send('John Doe');
});
app.post('/clients', (req: Request, res: Response): void => {
  res.send('Client updated!');
});
app.listen(port, (): void => {
  console.log(`App listening on port ${port}`);
});
Write documentation for this API service.
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Write your prompt here
```

What was the response?
```typescript
Write AI response here
```

## 2️⃣ Use Case 2: Create a Prompt for the Model to Document the Same API Using a Specific Methodology

Possible example:

```typescript
Create a prompt for the model to document the same API using a specific methodology like OpenAPI.
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Write your prompt here
```

What was the response?
```typescript
Write AI response here
```

## 3️⃣ Use Case 3: Compare Your Two Responses and Test Other Methodologies or Custom Plans
Feel free to explore other documentation methodologies or customize plans to test how the model adapts to different structures and requirements.