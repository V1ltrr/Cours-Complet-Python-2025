Les modules et bibliothèques permettent de réutiliser du code existant ou d’accéder à des fonctionnalités avancées sans avoir à tout coder soi-même.

- **Un module** est un fichier Python contenant du code réutilisable (fonctions, classes, variables).
- **Une bibliothèque** est un ensemble de modules regroupés pour offrir une solution à un domaine spécifique (comme la manipulation de données ou le calcul scientifique).
# <u>Importer un module</u>
### Syntaxe 
```py
import nom_du_module
```
### Exemple
```py
import math  # Import du module mathématique
print(math.sqrt(16))  # Racine carrée de 16 : 4.0
```
# <u>Importer une partie d'un module</u>
Pour importer une fonction ou une variable spécifique d’un module :
### Syntaxe
```py
from nom_du_module import element
```
### Exemple
```py
from math import sqrt
print(sqrt(25))  # 5.0
```
# <u>Renommer un module ou un élément</u>
Vous pouvez utiliser le mot-clé **as** pour attribuer un alias à un module ou un élément, afin de simplifier son utilisation.
### Exemple
```py
import math as m
print(m.pi)  # 3.141592653589793

from math import factorial as fact
print(fact(5))  # 120
```
# <u>Les modules intégrés</u>
Python propose de nombreux modules prêts à l’emploi. Voici quelques-uns des plus courants :

| Module       | Utilisation principale                                      |
| ------------ | ----------------------------------------------------------- |
| **math**     | Fonctions mathématiques avancées.                           |
| **random**   | Génération de nombres aléatoires.                           |
| **datetime** | Manipulation des dates et heures.                           |
| **os**       | Interaction avec le système d’exploitation.                 |
| **sys**      | Gestion des paramètres et des fonctionnalités du programme. |
### Exemple
```py
import random

# Générer un nombre aléatoire entre 1 et 10
nombre_aleatoire = random.randint(1, 10)
print(nombre_aleatoire)
```
# <u>Les modules externes</u>
Certains modules ne sont pas intégrés à Python et doivent être installés avec **pip**, le gestionnaire de paquets de Python.
### Syntaxe pour installer un module
```py
pip install nom_du_module
```
### Exemple
```py
pip install numpy
```
### Exemple d'utilisation
```py
import numpy as np

# Créer un tableau NumPy
tableau = np.array([1, 2, 3, 4])
print(tableau)
```
# <u>Créer un module personnel</u>
Vous pouvez créer vos propres modules en enregistrant du code Python dans un fichier **.py**.
### Exemple :
##### <u>Etape 1 :</u> créer un fichier **mon_module.py**
```py
# Contenu de mon_module.py
def saluer(nom):
    return f"Bonjour, {nom} !"
```
##### <u>Etape 2 :</u> importer le module dans un autre script
```py
import mon_module

message = mon_module.saluer("Alice")
print(message)  # Bonjour, Alice !
```
