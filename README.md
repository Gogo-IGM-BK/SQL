# Fonctions SQL 🔧
## Fonctions de chaînes

Les fonctions de chaînes vous permettent de manipuler des données textuelles pour des opérations comme la concaténation, la conversion en majuscules/minuscules, etc.

Exemple :

  Concaténation de deux chaînes :

```sql

SELECT CONCAT('Hello', ' World');
```
Convertir en majuscules :

```sql

SELECT UPPER('hello');
```
## Fonctions numériques

Manipulez et transformez vos données numériques grâce à diverses fonctions telles que l'arrondissement, le calcul de la racine carrée, etc.

Exemple :

Arrondir un nombre :

```sql

SELECT ROUND(123.4567, 2);
```
Calculer la racine carrée :

```sql

SELECT SQRT(16);
```
## Fonctions de date

Les fonctions de date sont essentielles pour manipuler et formater les données temporelles en SQL.

Exemple :

  Obtenir la date actuelle :

```sql

SELECT CURRENT_DATE;
```
Extraire l'année d'une date :

```sql

SELECT EXTRACT(YEAR FROM '2023-10-12');
```
