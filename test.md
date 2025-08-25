# <u>Les Variables :</u>
Une variable est un espace mémoire qui permet de stocker des données.  
En **C**, on crée une variable en **indiquant d’abord son type**, puis son nom, et éventuellement une valeur initiale avec le symbole `=`.

### Règles de nommage
1. Le nom d'une variable doit commencer par une lettre ou un underscore (`_`).
2. Il ne peut pas commencer par un chiffre.
3. Il peut contenir des lettres, chiffres et underscores.
4. Les mots-clés réservés du langage C ne peuvent pas être utilisés comme noms de variables (par exemple, **int**, **for**, **return**, etc.).

```c
#include <stdio.h>

int main() {
    // Déclaration de variables

    char nom[] = "Alice";     // Chaîne de caractères (tableau de char)
    int age = 25;             // Nombre entier
    float pi = 3.14;          // Nombre décimal
    int est_majeur = 1;       // Booléen (0 = faux, 1 = vrai)

    printf("%s\n", nom);      // Alice
    printf("%d\n", age);      // 25
    printf("%.2f\n", pi);     // 3.14
    printf("%d\n", est_majeur); // 1

    return 0;
}
```

---

# <u>Les Types de Données :</u>
Le langage C propose plusieurs types de données de base :  

- **int** : Nombres entiers (ex. **1**, **42**, **-7**)  
- **float** : Nombres décimaux (précision simple, ex. **3.14**)  
- **double** : Nombres décimaux à double précision (ex. **2.718281828**)  
- **char** : Caractère unique (ex. `'A'`, `'z'`)  
- **_Bool** (ou `int`) : Booléen (`0` pour faux, `1` pour vrai, disponible via `<stdbool.h>`)  

⚠️ Contrairement à Python, C n’a pas de listes ou dictionnaires intégrés. On utilise plutôt des **tableaux** et des **structures** pour représenter des collections de données.

### Exemple :
```c
#include <stdio.h>
#include <stdbool.h>

int main() {
    int entier = 10;         // int
    float decimal = 4.5;     // float
    double grandDecimal = 2.718281828; // double
    char lettre = 'H';       // char
    bool booleen = false;    // bool (nécessite <stdbool.h>)

    printf("int : %d\n", entier);
    printf("float : %.2f\n", decimal);
    printf("double : %.9f\n", grandDecimal);
    printf("char : %c\n", lettre);
    printf("bool : %d\n", booleen); // Affiche 0 (faux) ou 1 (vrai)

    return 0;
}
```

---

# <u>Les Conversions de Types :</u>
En C, on peut convertir un type en un autre grâce au **casting** (conversion explicite) ou parfois automatiquement (conversion implicite).

- **(int)** : Convertir en entier.  
- **(float)** : Convertir en flottant.  
- **(double)** : Convertir en double précision.  
- **(char)** : Convertir en caractère ASCII.  

### Exemple :
```c
#include <stdio.h>

int main() {
    float x = 42.7;      
    int y = (int)x;      // Conversion float -> int (tronque la partie décimale)
    char z = (char)y;    // Conversion int -> char (valeur ASCII)

    printf("x = %.2f (float)\n", x);  // 42.70
    printf("y = %d (int)\n", y);      // 42
    printf("z = %c (char)\n", z);     // * (selon le code ASCII de 42)

    return 0;
}
```
