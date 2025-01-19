En Python, une **exception** est un événement qui interrompt le flux normal d'un programme. Les exceptions surviennent généralement lorsqu'une erreur est détectée, comme une division par zéro ou l'accès à une variable inexistante.

La gestion des exceptions permet de gérer ces erreurs sans interrompre brusquement l'exécution du programme.
# <u>Lever une exception</u>
### Exemple
```py
# Division par zéro (provoque une exception ZeroDivisionError)
print(10 / 0)  
```
### Résultat
```py
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```
# <u>Gérer une exception</u>
### Syntaxe
```py
try:
    # Code qui peut provoquer une exception
    opération_risquée()
except TypeErreur as e:
    # Code exécuté en cas d'erreur
    gestion_erreur(e)
```
### Exemple
```py
try:
    a = int(input("Entrez un nombre : "))
    print(10 / a)
except ZeroDivisionError:
    print("Erreur : Division par zéro interdite.")
except ValueError:
    print("Erreur : Veuillez entrer un nombre valide.")
```
# <u>Utiliser **else** et **finally**</u>

- **else** : Code exécuté si aucune exception n’est levée dans le bloc **try**.
- **finally** : Code exécuté dans tous les cas (qu'il y ait une exception ou non).
### Exemple
```py
try:
    fichier = open("exemple.txt", "r")
    contenu = fichier.read()
except FileNotFoundError:
    print("Erreur : Le fichier n'existe pas.")
else:
    print("Contenu du fichier :", contenu)
finally:
    print("Opération terminée.")
```
# <u>Lever une exception manuellement</u>
Vous pouvez utiliser le mot-clé **raise** pour lever une exception manuellement.
### Exemple
```py
def verifier_age(age):
    if age < 0:
        raise ValueError("L'âge ne peut pas être négatif.")
    print(f"Âge valide : {age}")

try:
    verifier_age(-5)
except ValueError as e:
    print("Erreur :", e)
```
# <u>Créer des exceptions personnalisées</u>
Vous pouvez définir vos propres exceptions en créant une classe qui hérite de la classe intégrée **Exception**.
### Exemple
```py
class ErreurPersonnalisee(Exception):
    pass

def verifier_score(score):
    if score > 100:
        raise ErreurPersonnalisee("Le score ne peut pas dépasser 100.")
    print(f"Score valide : {score}")

try:
    verifier_score(150)
except ErreurPersonnalisee as e:
    print("Erreur :", e)
```
# <u>Les exceptions intégrées en python</u>
Voici quelques-unes des exceptions les plus courantes :

| Exception             | Description                               |
| --------------------- | ----------------------------------------- |
| **ZeroDivisionError** | Division par zéro.                        |
| **ValueError**        | Type de valeur incorrect.                 |
| **TypeError**         | Opération effectuée avec un mauvais type. |
| **FileNotFoundError** | Fichier introuvable.                      |
| **KeyError**          | Clé inexistante dans un dictionnaire.     |
| **IndexError**        | Indice inexistant dans une liste.         |
| **AttributeError**    | Attribut inexistant pour un objet.        |
# <u>Les bonnes pratiques</u>
**Soyez spécifique** : Gérer uniquement les exceptions que vous attendez.
```py
try:
    résultat = 10 / 0
except ZeroDivisionError:
    print("Erreur de division par zéro.")
```
**Ne pas masquer les erreurs** : Évitez d’utiliser un bloc **except** trop générique.
```py
# À éviter
try:
    operation()
except Exception:
    pass  # Masque potentiellement des erreurs importantes
```
