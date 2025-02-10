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
Pourquoi mon code ne fonctionne pas
function divide(a: int, b: str) {
    // Division
    let result = a / b;
    result = 0
    return result;
}
```

Quelle a été la réponse ?
```typescript
Votre code ne fonctionne pas pour plusieurs raisons :

Le type de l'argument b est incorrect. Il devrait être un nombre (number) et non une chaîne de caractères (str).
La division par zéro n'est pas gérée.
La variable result est réinitialisée à 0 avant d'être retournée, ce qui rend la division inutile.
Voici une version corrigée de votre code :

function divide(a: number, b: number): number {
    if (b === 0) {
        throw new Error("Division by zero is not allowed.");
    }
    let result = a / b;
    return result;
}

Cette version corrige les types des arguments, gère la division par zéro et retourne le résultat correct.
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
Peux-tu ajouter une sécurité pour éviter le dénominateur à 0 ?
function divide(a, b) {
    let result = a / b;
    return result;
}
```

Quelle a été la réponse ?
```typescript
Voici comment vous pouvez ajouter une vérification pour éviter la division par zéro :
function divide(a, b) {
    if (b === 0) {
        throw new Error("Division by zero is not allowed.");
    }
    let result = a / b;
    return result;
}
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
Que fait ce code ?
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

Quelle a été la réponse ?
```typescript
Ce code implémente l'algorithme du crible d'Ératosthène pour trouver tous les nombres premiers jusqu'à une limite donnée. Voici une explication détaillée :

La fonction calcul prend un argument limit qui représente la limite supérieure jusqu'à laquelle on veut trouver les nombres premiers.
Elle initialise un tableau primes pour stocker les nombres premiers trouvés.
Elle crée un tableau is_prime de taille limit + 1 et le remplit avec la valeur true, indiquant que tous les nombres sont initialement considérés comme premiers.
Elle initialise la variable p à 2, le premier nombre premier.
Elle utilise une boucle while pour marquer les multiples de chaque nombre premier comme non premiers (false) dans le tableau is_prime. Cette boucle continue tant que p * p est inférieur ou égal à limit.
Une fois que tous les multiples des nombres premiers jusqu'à sqrt(limit) ont été marqués, elle utilise une boucle for pour ajouter tous les nombres restants marqués comme premiers dans le tableau primes.
Enfin, elle retourne le tableau primes contenant tous les nombres premiers jusqu'à limit.
En résumé, ce code trouve et retourne tous les nombres premiers jusqu'à une limite donnée en utilisant l'algorithme du crible d'Ératosthène.
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
Modifie cette regex ^[\w.=-]+@[\w.-]+.[\w]{2,3} pour que cela accepts seulement les chaines qui finissent par "@gmail.com"
```

Quelle a été la réponse ?
```typescript
^[\w\.=-]+@gmail\.com$
```
