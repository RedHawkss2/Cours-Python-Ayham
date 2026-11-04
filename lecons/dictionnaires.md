# Les dictionnaires Python

Un dictionnaire associe des **clés** à des **valeurs**. Par exemple, la clé `"niveau"` donne le niveau du personnage.

## Créer, lire et modifier

```python
joueur = {"nom": "Luna", "niveau": 1, "points": 20}

print(joueur["nom"])      # Luna
joueur["niveau"] = 2     # Modifier une valeur
joueur["vie"] = 100      # Ajouter une clé et sa valeur
del joueur["points"]    # Supprimer une entrée
```

## Vérifier si une clé existe

`joueur["arme"]` provoque une erreur si la clé est absente. Avec `get`, tu peux choisir une valeur par défaut.

```python
print(joueur.get("arme", "Aucune"))  # Aucune

if "vie" in joueur:
    print(joueur["vie"])  # 100
```

## Parcourir les entrées

```python
for cle, valeur in joueur.items():
    print(f"{cle} : {valeur}")
```

## Exercices à faire dans PyCharm

### 1. Fiche de personnage

Crée un dictionnaire avec les clés `"nom"`, `"niveau"` et `"vie"`. Choisis les valeurs de départ, affiche le nom, augmente le niveau de 1 et ajoute une clé `"classe"`. Affiche ensuite le dictionnaire complet.

### 2. Inventaire

Pars de `inventaire = {"potion": 3, "fleche": 10}`. Utilise une potion en diminuant son stock de 1, puis ajoute deux boucliers sous la clé `"bouclier"`. Affiche le stock de potions. Tu dois obtenir `2`.

### 3. Prix en boutique

Pars de `prix = {"potion": 5, "epee": 20, "bouclier": 12}`. Demande un objet avec `input()`. Affiche son prix s’il est dans le dictionnaire, sinon affiche `Objet inconnu`. Teste avec `potion` et `casque`.

### Bonus. Total des points

Pars de `scores = {"Luna": 15, "Noah": 20, "Maya": 12}`. Avec une boucle, affiche chaque nom et son score, puis calcule le total. Tu dois obtenir `47`.
