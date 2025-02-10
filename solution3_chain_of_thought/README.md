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
Voici mon code :
[code]
Écris une documentation pour ce service API.
```

Quelle a été la réponse ?

```markdown
## API de gestion des clients

### Introduction
Ce service API permet de gérer les informations des clients via deux endpoints : un pour obtenir des informations sur un client spécifique et un pour mettre à jour les informations d’un client.

### Endpoints

#### 1. GET /clients/:clientId
- **Description** : Récupère les informations d'un client en fonction de son ID.
- **Paramètre** : `clientId` (string) – l’identifiant du client.
- **Exemple de réponse** : John Doe


#### 2. POST /clients
- **Description** : Met à jour les informations d'un client.
- **Exemple de réponse** : Client updated!
### Utilisation
Pour utiliser ce service API, envoyez des requêtes HTTP aux endpoints spécifiés en utilisant l’URL de base.
**Exemple d’utilisation avec curl :**
# Récupérer les informations d’un client
curl http://localhost:5000/clients/123

# Mettre à jour un client
curl -X POST http://localhost:5000/clients -d "Client updated!"
```

## 2️⃣ Cas d'usage 2 : Créez un prompt qui demande au modèle la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique.

Exemple possible:

```typescript
Créez un prompt qui demande au modèle la documentation pour la même API, mais cette fois-ci en utilisant une méthodologie spécifique, par exemple la méthode OpenAPI
```

A vous de jouer en intégrant votre prompt ci-dessous: 👀

```typescript
Écris une documentation pour ce service API en utilisant la méthodologie OpenAPI.
```

Quelle a été la réponse ?

```typescript
openapi: 3.0.0
info:
  title: API de gestion des clients
  description: API pour récupérer et mettre à jour des informations de clients.
  version: 1.0.0

paths:
  /clients/{clientId}:
    get:
      summary: Récupérer les informations d'un client
      parameters:
        - in: path
          name: clientId
          required: true
          schema:
            type: string
          description: L'identifiant du client à récupérer.
      responses:
        '200':
          description: Succès
          content:
            application/json:
              schema:
                type: string
              example: John Doe

  /clients:
    post:
      summary: Mettre à jour un client
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: string
      responses:
        '200':
          description: Succès
          content:
            application/json:
              schema:
                type: string
              example: Client updated!
```

## 3️⃣ Cas d'usage 3 : Comparer vos deux réponses et tester d’autres méthodologies ou plans personnalisés.
