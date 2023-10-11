# Les bases de SQL 📝
## Structure d'une base de données

Une base de données est essentiellement organisée en tables, qui sont composées de lignes (ou enregistrements) et de colonnes (ou champs). Chaque table stocke un type particulier de données. Par exemple, une base de données d'un magasin pourrait avoir une table Clients, une table Produits, et une table Commandes.

  Exemple :
        Table Clients : ID_Client, Nom, Prénom, Email.
        Table Produits : ID_Produit, Nom_Produit, Prix.

## Types de données courants

SQL prend en charge différents types de données pour répondre aux divers besoins de stockage, tels que INT pour les nombres entiers, VARCHAR pour les chaînes de caractères de longueur variable, ou DATE pour les dates.

    Exemple :
        Age : INT
        Nom : VARCHAR(100)
        DateDeNaissance : DATE

## Requêtes élémentaires

Le cœur de SQL réside dans la possibilité d'interroger une base de données. Les commandes fondamentales pour cela incluent SELECT (pour choisir les colonnes), FROM (pour spécifier la table) et WHERE (pour ajouter des conditions).

Exemple : Pour sélectionner tous les noms des clients :
```sql
    SELECT Nom FROM Clients;
```
## Tri des résultats

La clause ORDER BY vous permet d'organiser vos résultats selon un ou plusieurs champs, soit en ordre croissant (ASC par défaut) ou décroissant (DESC).

Exemple : Pour lister les produits par ordre décroissant de prix :
```sql
    SELECT Nom_Produit FROM Produits ORDER BY Prix DESC;
```
## Filtrage avec WHERE

La clause WHERE est puissante pour filtrer les résultats en fonction de conditions spécifiques.

Exemple : Pour trouver les clients nés après 1990 :


```sql
    SELECT Nom, DateDeNaissance FROM Clients WHERE DateDeNaissance > '1990-01-01';
```

