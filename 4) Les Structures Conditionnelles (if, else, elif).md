# <u>La syntaxe de base</u>
```py
if condition:
    # Code exécuté si la condition est vraie
elif autre_condition:
    # Code exécuté si la première condition est fausse
    # et cette condition est vraie
else:
    # Code exécuté si toutes les conditions sont fausses
```
### Exemple
```py
age = 20

if age < 18:
    print("Mineur")
elif age == 18:
    print("Tout juste majeur")
else:
    print("Majeur")
```
# <u>Les opérateurs utilisés dans les conditions</u>
- **Égalité** : `==`
- **Différence** : `!=`
- **Plus grand** : `>`
- **Plus petit** : `<`
- **Plus grand ou égal** : `>=`
- **Plus petit ou égal** : `<=`

Les conditions peuvent également combiner plusieurs expressions grâce aux opérateurs logiques :
- **ET** : `and`
- **OUI** : `or`
- **NON** : `not`

### Exemple
```py
note = 15

if note >= 10 and note < 20:
    print("Admis")
elif note == 20:
    print("Admis avec distinction")
else:
    print("Non admis")
```
# <u>L'instruction ternaire</u>
En Python, il est possible d’écrire une condition simple sur une seule ligne avec une instruction ternaire :
```py
variable = valeur_si_vrai if condition else valeur_si_faux
```
### Exemple
```py
age = 17
statut = "Majeur" if age >= 18 else "Mineur"
print(statut)  # Mineur
```
# <u>Les conditions imbriquées</u>
Les structures conditionnelles peuvent être imbriquées pour traiter des cas plus complexes.  
Cependant, il est conseillé d'éviter trop d'imbrications pour garder le code lisible.

### Exemple

```py
age = 16
parent_present = True

if age < 18:
    if parent_present:
        print("Accès autorisé avec un parent")
    else:
        print("Accès interdit")
else:
    print("Accès autorisé")
```
# <u>Les conditions avec booléens</u>
Les booléens **`True`** et **`False`** peuvent être utilisés directement comme conditions.

### Exemple
```py
autorisation = False

if autorisation:
    print("Action autorisée")
else:
    print("Action non autorisée")
```
