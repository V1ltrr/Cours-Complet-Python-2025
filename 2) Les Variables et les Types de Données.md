# <u>Les Variables :</u>
Une variable est un conteneur qui permet de stocker des données. En Python, on crée une variable en lui attribuant une valeur avec le symbole **=**.

### Règles de nommage
1. Le nom d'une variable doit commencer par une lettre ou un underscore (`_`).
2. Il ne peut pas commencer par un chiffre.
3. Il peut contenir des lettres, chiffres et underscores.
4. Les mots-clés réservés du langage Python ne peuvent pas être utilisés comme noms de variables (par exemple, **if**, **for**, **print**, etc.).
```py
# Déclaration de variables

nom = "Alice"            # Chaîne de caractères
age = 25                 # Nombre entier
pi = 3.14                # Nombre décimal (float)
est_majeur = True        # Booléen (True ou False)

print(nom)               # Alice
print(age)               # 25
print(pi)                # 3.14
print(est_majeur)        # True
```
# <u>Les Types de Données :</u>
Python propose plusieurs types de données courants :

- **int** : Nombres entiers (e.g., **1**, **42**, **-7**).
- **float** : Nombres décimaux (e.g., **3.14**, **-2.71**).
- **str** : Chaînes de caractères (e.g., **"Bonjour"**, **Python**).
- **bool** : Booléens (**True** ou **False**).
- **list** : Liste d'éléments (e.g., **[1, 2, 3]**).
- **tuple** : Liste immuable (e.g., **(1, 2, 3)**).
- **dict** : Dictionnaire clé-valeur (e.g., **{"nom": "Alice", "age": 25}**).  
### Exemple :
```py
# Différents types de données

entier = 10               # int
decimal = 4.5             # float
texte = "Hello"           # str
booleen = False           # bool
liste = [1, 2, 3]         # list
tuple_immutable = (1, 2)  # tuple
dictionnaire = {"clé": "valeur"}  # dict

print(type(entier))       # <class 'int'>
print(type(decimal))      # <class 'float'>
print(type(texte))        # <class 'str'>
print(type(booleen))      # <class 'bool'>
print(type(liste))        # <class 'list'>
print(type(tuple_immutable))  # <class 'tuple'>
print(type(dictionnaire))     # <class 'dict'>
```
# <u>Les Conversions de Types :</u>
Il est possible de convertir un type de données en un autre grâce à des fonctions intégrées :

- **int()** : Convertir en entier.
- **float()** : Convertir en nombre décimal.
- **str()** : Convertir en chaîne de caractères.
- **bool()** : Convertir en booléen.
### Exemple :
```py
# Conversion entre types

x = "42"                # str
y = int(x)              # Convertir str en int
z = float(y)            # Convertir int en float

print(type(x), x)       # <class 'str'> 42
print(type(y), y)       # <class 'int'> 42
print(type(z), z)       # <class 'float'> 42.0

```
