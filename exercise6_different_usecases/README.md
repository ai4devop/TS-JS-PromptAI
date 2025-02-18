# 📝 Exercise6 - Different usecases ~ 20 minutes
This file contains several exercises that highlight various use cases for a developer. These exercises will allow you to test multiple scenarios, providing a comprehensive understanding of different situations you may encounter in development.

## Use Case 1: Fix code
Possible example:
```typescript
// Check why this code is not working whithout IA
// Ask AI to fix it
function divide(a: int, b: str) {
    // Division
    let result = a / b;
    result = 0
    return result;
}
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Write your prompt here
```

What was the response?
```typescript
Write AI response here
```

This code will correctly divide a by b and return the result.

## Use Case 2: Optimize code
Possible example:

```typescript
//ask AI to add some optimization like protecting the denominator from 0
function bulkDivide(numbers: number[], b: number): number[] {
    let results: number[] = [];
    for (let i = 0; i < numbers.length; i++) {
        results.push(numbers[i] / b);
    }
    return results;
}
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Write your prompt here
```

What was the response?
```typescript
Write AI response here
```

## Use Case 3: Reverse engineering
Possible example:
```typescript
// Try to found out what this code do without AI
// Ask AI what is the purpose of this code
// Did you manage to found out before AI ?
function calcul(limit) {
    let primes = [];
    let is_prime = new Array(limit + 1).fill(true);
    let p = 2;

    while (p * p <= limit) {
        if (is_prime[p]) {
            for (let i = p * p; i <= limit; i += p) {
                is_prime[i] = false;
            }
        }
        p += 1;
    }

    for (let p = 2; p <= limit; p++) {
        if (is_prime[p]) {
            primes.push(p);
        }
    }

    return primes;
}

```

Now it's your turn to integrate your prompt below: 👀
```typescript
Write your prompt here
```

What was the response?
```typescript
Write AI response here
```

## Use Case 4: REGEX
Possible example:
```typescript
// Try to understand what this regex does without AI
// Ask AI what the regex does and compare
// Modify the regex to match your company

^[\w\.=-]+@[\w\.-]+\.[\w]{2,3}$
```

Now it's your turn to integrate your prompt below: 👀
```typescript
Write your prompt here
```

What was the response?
```typescript
Write AI response here
```
