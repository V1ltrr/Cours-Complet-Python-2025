Python permet de lire, écrire et manipuler des fichiers (texte, binaire, etc.) facilement. Ce chapitre couvre les bases pour interagir avec des fichiers dans vos programmes.
# <u>Ouvrir et fermer un fichier</u>
Pour travailler avec un fichier, il faut d’abord l’ouvrir avec la fonction **open()**, puis le fermer une fois l’opération terminée.
### Syntaxe
```py
fichier = open("nom_du_fichier", mode)
# ... opérations sur le fichier ...
fichier.close()
```
**Modes courants** :
- "**r**" : Lecture seule (par défaut).
- "**w**" : Écriture, remplace le contenu existant.
- "**a**" : Écriture, ajoute au contenu existant.
- "**x**" : Crée un nouveau fichier, erreur s’il existe déjà.
### Exemple
```py
fichier = open("exemple.txt", "w")  # Ouvre en mode écriture
fichier.write("Bonjour, monde !")
fichier.close()
```
# <u>Lire un fichier</u>
### Lire tout le contenu
```py
fichier = open("exemple.txt", "r")
contenu = fichier.read()
print(contenu)
fichier.close()
```
### Lire ligne par ligne
```py
fichier = open("exemple.txt", "r")
for ligne in fichier:
    print(ligne.strip())  # Supprime les espaces en fin de ligne
fichier.close()
```
### Utiliser **readlines()**
```py
fichier = open("exemple.txt", "r")
lignes = fichier.readlines()  # Retourne une liste de lignes
print(lignes)
fichier.close()
```
# <u>Ecrire dans un fichier</u>
### Exemple
```py
fichier = open("exemple.txt", "w")
fichier.write("Première ligne.\n")
fichier.write("Deuxième ligne.")
fichier.close()
```
### Mode **a** (ajout)
```py
fichier = open("exemple.txt", "a")
fichier.write("\nNouvelle ligne ajoutée.")
fichier.close()
```
# <u>Gestion Automatique avec **with**</u>
Le mot-clé **with** permet de s’assurer que le fichier sera fermé automatiquement, même en cas d’erreur.
### Exemple
```py
with open("exemple.txt", "r") as fichier:
    contenu = fichier.read()
    print(contenu)
# Le fichier est automatiquement fermé ici
```
# <u>Vérifier l'existence d'un fichier</u>
Pour éviter les erreurs, vous pouvez vérifier si un fichier existe avant de l’ouvrir.
### Exemple
```py
import os

if os.path.exists("exemple.txt"):
    with open("exemple.txt", "r") as fichier:
        print(fichier.read())
else:
    print("Le fichier n'existe pas.")
```
# <u>Supprimer un fichier</u>
Pour éviter les erreurs, vous pouvez vérifier si un fichier existe avant de l’ouvrir.
### Exemple
```py
import os

if os.path.exists("exemple.txt"):
    os.remove("exemple.txt")
    print("Fichier supprimé.")
else:
    print("Le fichier n'existe pas.")
```
# <u>Lire et écrire des fichiers binaires</u>
Les fichiers binaires (images, vidéos, etc.) nécessitent des modes **rb** (lecture) et **wb** (écriture).
### Exemple
```py
# Copier un fichier binaire
with open("image_source.jpg", "rb") as source:
    contenu = source.read()

with open("image_copie.jpg", "wb") as destination:
    destination.write(contenu)
```
# <u>Les méthodes utiles pour les fichiers</u>

| Méthode          | Description                                   |
| ---------------- | --------------------------------------------- |
| **read(size)**   | Lit un nombre d’octets donné (tout si omis).  |
| **readline()**   | Lit une seule ligne du fichier.               |
| **write(data)**  | Écrit une chaîne dans le fichier.             |
| **seek(offset)** | Déplace le curseur à une position spécifique. |
| **tell()**       | Retourne la position actuelle du curseur.     |
### Exemple
```py
with open("exemple.txt", "r") as fichier:
    fichier.seek(5)  # Déplace le curseur après le 5e caractère
    print(fichier.read())  # Lit depuis cette position
```
