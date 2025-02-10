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
Génère une fonction en javascript qui accepte un nombre et retourne "pair" si c'est pair et "impair" si c'est impair
```

Quelle a été la réponse ?
```typescript
function verifierParite(nombre) {
    if (nombre % 2 === 0) {
        return "pair";
    } else {
        return "impair";
    }
}

// Exemple d'utilisation
console.log(verifierParite(4)); // "pair"
console.log(verifierParite(7)); // "impair"
```

## 2️⃣ Cas d'usage 2 : Créez un nouveau prompt qui demande au modèle de générer une fonction TypeScript avec une structure de réponse spécifique
Exemple possible:
```typescript
// créez une méthode Javascript qui vérifie si un mot est un palindrome en décrivant avec vos propres mot ce qu'est un palindrome sans écrire le mot palindrome
// Input: isPalindrome("radar") > Ouput: true
// Input: isPalindrome("Bonjour") > Ouput: false
```

A vous de jouer en intégrant votre prompt ci-dessous: 👀
```typescript
Génère une méthode en java qui va prendre une chaine de caractères et vérifier s'il peut se lire dans les deux sens comme radar ou kayak
```

Quelle a été la réponse ?
```typescript
public class PalindromeChecker {

    public static boolean isPalindrome(String str) {
        if (str == null) {
            return false;
        }
        int left = 0;
        int right = str.length() - 1;
        
        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) {
                return false;
            }
            left++;
            right--;
        }
        return true;
    }

    public static void main(String[] args) {
        String test1 = "radar";
        String test2 = "kayak";
        String test3 = "hello";
        
        System.out.println(test1 + " is palindrome? " + isPalindrome(test1));
        System.out.println(test2 + " is palindrome? " + isPalindrome(test2));
        System.out.println(test3 + " is palindrome? " + isPalindrome(test3));
    }
}
```

## 3️⃣ Cas d'usage 3 : Comparez vos deux réponses et testez d'autres structures de réponses

