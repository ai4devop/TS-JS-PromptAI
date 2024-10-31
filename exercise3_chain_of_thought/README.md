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
Create a prompt for the model to write documentation for TypeScript code.
```

What was the response?

```markdown
## Client Management API
### Introduction
This API service allows managing client information via two endpoints: one to get information on a specific client and one to update a client's information.

### Endpoints
#### 1. GET /clients/:clientId
- **Description**: Retrieves information about a client based on their ID.
- **Parameter**: `clientId` (string) – the client's identifier.
- **Example response**: John Doe

#### 2. POST /clients
- **Description**: Updates a client's information.
- **Example response**: Client updated!

### Usage
To use this API service, send HTTP requests to the specified endpoints using the base URL.
**Example usage with curl:**
# Retrieve client information
curl http://localhost:5000/clients/123
# Update a client
curl -X POST http://localhost:5000/clients -d "Client updated!"
```

## 2️⃣ Use Case 2: Create a Prompt for the Model to Document the Same API Using a Specific Methodology

Possible example:

```typescript
Write documentation for this API service using the OpenAPI methodology.
```

Now it's your turn to integrate your prompt below: 👀

```typescript
Create a prompt for the model to document the same API using a specific methodology.
```

What was the response?

```typescript
openapi: 3.0.0
info:
  title: Client Management API
  description: API to retrieve and update client information.
  version: 1.0.0
paths:
/clients/{clientId}:
  get:
    summary: Retrieve client information
    parameters:
      - in: path
        name: clientId
        required: true
        schema:
          type: string
        description: The client's ID to retrieve.
    responses:
      '200':
        description: Success
        content:
          application/json:
            schema:
              type: string
            example: John Doe
/clients:
  post:
    summary: Update a client
    requestBody:
      required: true
      content:
        application/json:
          schema:
            type: string
    responses:
      '200':
        description: Success
        content:
          application/json:
            schema:
              type: string
            example: Client updated!
```

## 3️⃣ Use Case 3: Compare Your Two Responses and Test Other Methodologies or Custom Plans
Feel free to explore other documentation methodologies or customize plans to test how the model adapts to different structures and requirements.