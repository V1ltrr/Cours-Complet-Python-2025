Une liste est une structure de données qui permet de stocker plusieurs éléments dans un ordre donné.  
Les listes en Python sont **modifiables** (on peut ajouter, supprimer ou modifier des éléments).

# <u>Créer une liste</u>
### Syntaxe
```py
ma_liste = [element1, element2, element3]
```
### Exemple
```py
# Liste de nombres
nombres = [1, 2, 3, 4, 5]

# Liste de chaînes de caractères
jours = ["lundi", "mardi", "mercredi"]

# Liste mixte
mixte = [10, "Python", True, 3.14]

print(nombres)  # [1, 2, 3, 4, 5]
print(jours)    # ['lundi', 'mardi', 'mercredi']
print(mixte)    # [10, 'Python', True, 3.14]
```
# <u>Accéder aux éléments d'une liste</u>
Les éléments d'une liste sont accessibles grâce à leur **index** (position), qui commence à **0**.
### Exemple
```py
fruits = ["pomme", "banane", "cerise"]

print(fruits[0])  # pomme (premier élément)
print(fruits[1])  # banane (deuxième élément)
print(fruits[-1]) # cerise (dernier élément)
```
# <u>Modifier une liste</u>
Ajouter un élément :
- `append()` : Ajoute un élément à la fin de la liste.
- `insert(index, element)` : Insère un élément à une position donnée.

### Exemple
```py
fruits = ["pomme", "banane"]
fruits.append("cerise")  # Ajoute à la fin
fruits.insert(1, "orange")  # Ajoute "orange" à l'index 1
print(fruits)  # ['pomme', 'orange', 'banane', 'cerise']
```
### Modifier un élément
```py
fruits[0] = "kiwi"  # Remplace "pomme" par "kiwi"
print(fruits)  # ['kiwi', 'orange', 'banane', 'cerise']
```
# <u>Supprimer un élément</u>
- `remove(element)` : Supprime le premier élément correspondant.
- `pop(index)` : Supprime l'élément à l'index donné (ou le dernier si aucun index n'est fourni).
- `del liste[index]` : Supprime un élément à un index donné.
- `clear()` : Vide entièrement la liste.

### Exemple
```py
fruits = ["pomme", "banane", "cerise", "banane"]

fruits.remove("banane")  # Supprime la première "banane"
print(fruits)  # ['pomme', 'cerise', 'banane']

fruits.pop(1)  # Supprime "cerise" (index 1)
print(fruits)  # ['pomme', 'banane']

del fruits[0]  # Supprime "pomme"
print(fruits)  # ['banane']

fruits.clear()  # Vide la liste
print(fruits)  # []
```
# Parcourir une liste
### Exemple
```py
fruits = ["pomme", "banane", "cerise"]

# Parcourir avec une boucle for
for fruit in fruits:
    print(fruit)

# Parcourir avec les index
for i in range(len(fruits)):
    print(f"L'élément à l'index {i} est {fruits[i]}")
```
# <u>Opérations sur les listes</u>
**Concaténation** : Combine deux listes.
### Exemple
```py
liste1 = [1, 2]
liste2 = [3, 4]
resultat = liste1 + liste2
print(resultat)  # [1, 2, 3, 4]
```

**Répétition** : Répète les éléments de la liste.
```py
liste = [1, 2]
print(liste * 3)  # [1, 2, 1, 2, 1, 2]
```

**Tester la présence d’un élément** :
```py
fruits = ["pomme", "banane", "cerise"]
print("pomme" in fruits)  # True
print("kiwi" not in fruits)  # True
```
# <u>Les méthodes utiles pour les listes</u>
| Méthode          | Description                                       |
| ---------------- | ------------------------------------------------- |
| *len(liste)*     | Renvoie le nombre d'éléments.                     |
| *list.sort()*    | Trie la liste en place.                           |
| *list.reverse()* | Inverse l'ordre des éléments.                     |
| *list.count(x)*  | Compte le nombre d’occurrences de `x`.            |
| *list.index(x)*  | Renvoie l’index de la première occurrence de `x`. |
### Exemple
```py
nombres = [3, 1, 4, 1, 5, 9]

print(len(nombres))       # 6
nombres.sort()
print(nombres)            # [1, 1, 3, 4, 5, 9]
nombres.reverse()
print(nombres)            # [9, 5, 4, 3, 1, 1]
print(nombres.count(1))   # 2
print(nombres.index(5))   # 1
```
