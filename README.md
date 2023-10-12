# Index et performances 🚀


Un index est une structure de données utilisée pour améliorer la rapidité des opérations de récupération de données. Pensez-y comme à la table des matières d'un livre qui permet de trouver rapidement une information spécifique sans parcourir chaque page.

Exemple :

  Recherche sans index :

```sql

SELECT * FROM Livres WHERE Titre = 'L'Art de la Guerre';
```
  Cela pourrait parcourir chaque ligne de la table pour trouver le bon enregistrement.

## Création, modification et suppression d'index

Gérer les index est crucial pour maintenir des performances optimales dans votre base de données.

Exemple :

  Création d'un index sur le titre des livres :

```sql

CREATE INDEX idx_Titre ON Livres (Titre);
```
Suppression d'un index :

```sql

    DROP INDEX idx_Titre ON Livres;
```
## Plan d'exécution et optimisation de requêtes

Le plan d'exécution montre comment le système de gestion de base de données prévoit d'exécuter une requête. Comprendre ces plans peut vous aider à optimiser vos requêtes pour de meilleures performances.

Exemple :

  Pour voir le plan d'exécution dans certains SGBD :

``` sql

EXPLAIN SELECT * FROM Livres WHERE Titre = 'L'Art de la Guerre';
```
Cela affichera le plan d'exécution et vous aidera à identifier les éventuels goulets d'étranglement ou les domaines d'amélioration.```
