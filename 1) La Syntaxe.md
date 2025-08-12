# <u>Structure de base</u>
Dans VS code, on peut créer un nouveau fichier qui pourra ensuite exécuter notre code en python. 
Notre script va ensuite s'effectuer dans la console.

Dans python, nous pouvons par exemple faire un programme qui affiche certaines informations dans la console, pour ça, voyons déjà quelles sont les différents types de données.

| <u>Type de donnée</u>           | <u>Description</u>                                | <u>Comment les définir</u>                             |
| ------------------------------- | ------------------------------------------------- | ------------------------------------------------------ |
| Les entiers (int)               | Nombres entiers                                   | *nombre = 5*                                           |
| Lef Flottants (float)           | Nombres décimaux                                  | *nombre = 3.21*                                        |
| Les chaînes de caractères (str) | Texte (qui peut contenir des mots et des nombres) | *information = "L'avion va décoller dans 10 minutes."* |
| Booléens (bool)                 | Définit une variable comme vrai ou fausse         | *ouvert = false*                                       |

## <u>Variables :</u>
### <u>Définir des variables</u>
Une variable est un espace en mémoire où l’on stocke une donnée. Elle est définie en utilisant le signe =** .
```py
age = 25
nom = "Alice"
```
### <u>Règles pour nommer des variables</u>
- Utilisez des lettres (a-z, A-Z), des chiffres (0-9) et des underscores (**_**).
- Ne commencez jamais par un chiffre.
- Évitez d'utiliser les mots-clés réservés de Python, comme **for**, **if**, **while**, etc.

### <u>Changer la valeur d’une variable</u>
Vous pouvez réassigner une nouvelle valeur à une variable existante :
```py
age = 30
nom = "Alice"
age = 40
```
### <u>Type de données et conversion</u>
Pour convertir une donnée en un autre type, utilisez les fonctions de conversion :
```py
nombre_entier = int("5") # Convertit une chaîne en entier
nombre_float = float(5) # Convertit un entier en flottant
texte = str(5) # Convertit un entier en chaîne
```
