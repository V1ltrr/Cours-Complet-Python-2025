Les boucles permettent d'exécuter un bloc de code plusieurs fois, soit pour un nombre défini d'itérations (**for**), soit tant qu'une condition est vraie (**while**).
# <u>La boucle "**for**" </u>
La boucle **for** est utilisée pour parcourir une séquence (liste, chaîne de caractères, plage de nombres, etc.).

### Syntaxe
```py
for variable in sequence:
    # Code à exécuter pour chaque élément de la séquence
```
### Exemple
```py
# Parcourir une liste
fruits = ["pomme", "banane", "cerise"]
for fruit in fruits:
    print(fruit)

# Parcourir une plage de nombres
for i in range(5):  # De 0 à 4
    print(i)

# Parcourir une chaîne de caractères
for lettre in "Python":
    print(lettre)
```
# <u>La fonction "**range( )**"</u>
La fonction **range()** est souvent utilisée avec les boucles **for** pour générer une plage de nombres.

- **range(stop)** : Génère les nombres de **0** à **stop - 1**.
- **range(start, stop)** : Génère les nombres de **start** à **stop - 1**.
- **range(start, stop, step)** : Génère les nombres de **start** à **stop - 1** avec un intervalle de **step**.

### Exemple
```py
for i in range(1, 10, 2):  # De 1 à 9, avec un pas de 2
    print(i)
```
# <u>La boucle **while**</u>
La boucle **while** exécute un bloc de code tant qu'une condition est vraie.

### Syntaxe
```py
while condition:
    # Code exécuté tant que la condition est vraie
```
### Exemple
```py
# Compter jusqu'à 5
compteur = 1
while compteur <= 5:
    print(compteur)
    compteur += 1  # Incrémentation
```
# Boucles infinies
Si la condition d'une boucle **while** reste toujours vraie, cela crée une boucle infinie.  
Pour éviter cela, assurez-vous que la condition devient fausse à un moment donné.

### Exemple
```py
while True:
    commande = input("Tapez 'exit' pour quitter : ")
    if commande == "exit":
        break  # Interrompt la boucle
```
# <u>Instruction utiles avec les boucles</u>
- **break** : Interrompt la boucle immédiatement.
- **continue** : Passe directement à l'itération suivante de la boucle.
- **else** : Code exécuté lorsque la boucle se termine sans interruption (**break**).

### Exemple
```py
# Utilisation de break
for nombre in range(10):
    if nombre == 5:
        break  # Interrompt la boucle quand nombre == 5
    print(nombre)

# Utilisation de continue
for nombre in range(10):
    if nombre % 2 == 0:
        continue  # Ignore les nombres pairs
    print(nombre)

# Clause else dans une boucle
for nombre in range(3):
    print(nombre)
else:
    print("La boucle est terminée")
```
