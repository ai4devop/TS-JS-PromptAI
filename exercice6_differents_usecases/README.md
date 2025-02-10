# 📝 Exercise6 - Different usecases ~ 20 minutes
The fichier contient plusieurs exercices qui mettent en avant plusieurs use cases de développeur. Ces exercices vous permettent de tester plusieurs scénario, permettant de mieux comprendre comment utiliser l'IA dans votre quotidien.

## Use Case 1: Fix code
Exemple possible:
```typescript
// Vérifiez pourquoi ce code ne fonctionne pas (sans IA)
// Demandez à l'IA de réparer ce code
function divide(a: int, b: str) {
    // Division
    let result = a / b;
    result = 0
    return result;
}
```

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```typescript
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```typescript
Ecrivez la réponse de l'IA ici
```

## Use Case 2: Optimize code
Exemple possible:
```typescript
// Demandez à l'IA d'ajouter de l'optimisation comme une protection du denominateur différent de 0
function divide(a, b) {
    let result = a / b;
    return result;
}

```

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```typescript
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```typescript
Ecrivez la réponse de l'IA ici
```

## Use Case 3: Reverse engineering
Exemple possible:
```typescript
// Essayez de trouver ce que fait ce code sans IA
// Demande à l'IA ce que fait ce code
// Avez-vous réussi a comprendre en moins de temps que l'IA ?
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

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```typescript
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```typescript
Ecrivez la réponse de l'IA ici
```

## Use Case 4: REGEX
Exemple possible:
```typescript
// Essayez de comprendre cette regex sans utiliser l'IA
// Demandez à l'IA ce que fait ce code et comparer avec votre temps de réflexion
// Modifiez cette regex pour fonctionner pour votre entreprise

^[\w\.=-]+@[\w\.-]+\.[\w]{2,3}$
```

À vous de jouer en intégrant votre prompt ci-dessous : 👀
```typescript
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```typescript
Ecrivez la réponse de l'IA ici
```
