# Les fonctions en Python

Une fonction regroupe des instructions que tu peux exécuter plusieurs fois en l'appelant par son nom.

## Définir et appeler une fonction

```python
def prix_total(prix_unitaire, quantite):
    return prix_unitaire * quantite

total = prix_total(8, 3)
print(total)  # 24
```

- `def` définit la fonction. Le corps commence après les deux-points et s'écrit avec quatre espaces d'indentation.
- `prix_unitaire` et `quantite` sont les **paramètres**. Ils désignent les valeurs attendues dans la définition.
- `8` et `3` sont les **arguments**. Ce sont les valeurs données au moment de l'appel.
- `return` termine l'appel et renvoie une valeur. Ici, on la stocke dans `total`.

## Afficher ou renvoyer une valeur

```python
def dire_bonjour(prenom):
    print(f"Bonjour {prenom} !")

dire_bonjour("Ayham")  # Affiche Bonjour Ayham !
```

`print()` affiche une information dans la console. Une fonction qui se termine sans exécuter de `return` renvoie automatiquement `None`. Pour réutiliser un résultat dans un calcul ou une condition, renvoie-le avec `return`.

## Utiliser une fonction dans une autre

```python
def peut_acheter(solde, prix_unitaire, quantite):
    cout = prix_total(prix_unitaire, quantite)
    return solde >= cout

print(peut_acheter(24, 8, 3))  # True
print(peut_acheter(23, 8, 3))  # False
```

`cout` est une variable locale à la fonction. Pour tester une condition, essaie aussi la valeur à la limite, ici un solde exactement égal au coût.

## À toi de jouer

Écris `prix_reduit(prix, reduction)` qui renvoie le prix après une réduction exprimée en euros. Vérifie que `prix_reduit(25, 5)` renvoie `20`, puis stocke le résultat dans une variable et utilise-le pour calculer le prix de trois articles.
