# 📝 Exercice3 - Chain of thought ~ 10 minutes

La technique "chain of thought" consiste à guider le modèle dans un processus de raisonnement pour expliquer chaque étape du processus de réflexion. Ici, nous utilisons cette méthode pour générer de la documentation en TypeScript.

## 1️⃣ Cas d'usage 1 : Créez un prompt qui demande au modèle d'écrire de la documentation pour un code TypeScript.

Exemple possible:

```typescript
Créez un prompt qui demande au modèle d'écrire de la documentation pour un code TypeScript.
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
```

A vous de jouer en intégrant votre prompt ci-dessous: 👀

```typescript
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```typescript
Ecrivez la réponse de l'IA ici
```

## 2️⃣ Cas d'usage 2 : Créez un prompt qui demande au modèle la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique.

Exemple possible:

```typescript
Créez un prompt qui demande au modèle la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique, par exemple la méthode OpenAPI
```

A vous de jouer en intégrant votre prompt ci-dessous: 👀

```typescript
Ecrivez votre prompt ici
```

Quelle a été la réponse ?
```typescript
Ecrivez la réponse de l'IA ici
```

## 3️⃣ Cas d'usage 3 : Comparer vos deux réponses et tester d’autres méthodologies ou plans personnalisés.
