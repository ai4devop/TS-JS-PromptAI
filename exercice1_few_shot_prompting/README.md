# 📝 Exercice1 - Few-Shot Prompting ~ 10 minutes
Le few-shot prompting consiste à fournir au modèle quelques exemples d'entrées et de sorties pour lui indiquer le type de tâche à effectuer. C'est une méthode simple et intuitive qui peut être utilisée pour diverses tâches de génération de code ou de vérification de fonctionnalités.

## 1️⃣ Cas d'usage 1 : Créez un prompt qui demande au modèle de générer une fonction TypeScript
Exemple possible:
```typescript
// Créez une fonction qui vérifie si un nombre est pair ou impair.
// la fonction isEvenOrOdd appelé avec le paramètre 3, comme ceci isEvenOrOdd(3), doit me retourner "odd"
// la fonction isEvenOrOdd appelé avec le paramètre 4, comme ceci isEvenOrOdd(4), doit me retourner "even"
```

A vous de jouer en intégrant votre prompt ci-dessous: 👀
```typescript
Créez un prompt qui demande au modèle de générer une fonction TypeScript
```

Quelle a été la réponse ?
```typescript
function isEvenOrOdd(number: number): string {
  if (number % 2 === 0) {
    return 'Even';
  }
  return 'Odd';
}
```

## 2️⃣ Cas d'usage 2 : Créez un nouveau prompt qui demande au modèle de générer une fonction TypeScript avec une structure de réponse spécifique
Exemple possible:
```typescript
// Peux-tu créer une fonction TypeScript qui vérifie si un mot est un palindrome ?
// Input: isPalindrome("radar") > Ouput: true
// Input: isPalindrome("Bonjour") > Ouput: false
```

A vous de jouer en intégrant votre prompt ci-dessous: 👀
```typescript
Créez un nouveau prompt qui demande au modèle de générer une fonction TypeScript avec une structure de réponse spécifique
```

Quelle a été la réponse ?
```typescript
function isPalindrome(word: string): boolean {
  const reversed = word.split('').reverse().join('');
  return word === reversed;
}
```

## 3️⃣ Cas d'usage 3 : Comparez vos deux réponses et testez d'autres structures de réponses

