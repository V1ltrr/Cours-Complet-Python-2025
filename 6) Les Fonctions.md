Une fonction est un bloc de code réutilisable qui exécute une tâche précise. En Python, les fonctions permettent de structurer le code, d'améliorer sa lisibilité et de réduire la répétition.

# <u>Définir une fonction</u>
Une fonction se définit avec le mot-clé **def**, suivi du nom de la fonction et d’éventuels paramètres entre parenthèses.

### Syntaxe
```py
def nom_de_la_fonction(parametre1, parametre2):
    # Instructions de la fonction
    return resultat  # Optionnel : retourne une valeur
```
### Exemple
```py
# Définir une fonction simple
def saluer(nom):
    print(f"Bonjour, {nom} !")

# Appeler la fonction
saluer("Alice")  # Bonjour, Alice !
```
# <u>Les paramètres et arguments</u>
- **Paramètres** : Variables définies dans les parenthèses lors de la déclaration d’une fonction.
- **Arguments** : Valeurs passées à la fonction lors de son appel.

### Exemple
```py
def addition(a, b):
    return a + b

resultat = addition(3, 7)  # Appel de la fonction avec 3 et 7 comme arguments
print(resultat)  # 10
```
# <u>Les paramètres avec valeurs par défaut</u>
Vous pouvez définir des valeurs par défaut pour certains paramètres, qui seront utilisées si aucun argument n'est fourni.

### Exemple
```py
def saluer(nom="inconnu"):
    print(f"Bonjour, {nom} !")

saluer()              # Bonjour, inconnu !
saluer("Marie")       # Bonjour, Marie !
```
# <u>Les fonctions avec retour de valeur</u>
La fonction peut renvoyer un résultat avec le mot-clé **return**, ce qui permet de l’utiliser ailleurs dans le programme.

### Exemple
```py
def multiplier(a, b):
    return a * b

produit = multiplier(4, 5)
print(produit)  # 20
```
# <u>Les fonctions lambda</u>
Les fonctions lambda (ou anonymes) sont des fonctions compactes qui s’écrivent sur une seule ligne. Elles sont utiles pour des tâches simples.

### Syntaxe
```py
lambda param1, param2: expression
```
### Exemple
```py
# Fonction lambda pour additionner deux nombres
addition = lambda x, y: x + y
print(addition(3, 4))  # 7

# Utilisation dans une fonction standard
def appliquer_fonction(fonction, a, b):
    return fonction(a, b)

resultat = appliquer_fonction(lambda x, y: x * y, 5, 6)
print(resultat)  # 30
```
# <u>Les fonctions imbriquées</u>
Une fonction peut être définie à l'intérieur d'une autre.

### Exemple
```py
def exterieur(x):
    def interieur(y):
        return y * y
    return interieur(x) + 1

print(exterieur(3))  # 10
```
# <u>Les portées des variables</u>
- **Globale** : Variable accessible partout dans le programme.
- **Locale** : Variable définie à l’intérieur d’une fonction et accessible uniquement dans cette fonction.

### Exemple
```py
x = 10  # Variable globale

def fonction():
    x = 5  # Variable locale
    print(x)

fonction()  # 5
print(x)    # 10
```
