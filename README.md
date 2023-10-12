# Création et gestion de bases de données 🛠️
## Création et modification de tables

Créer des bases de données et des tables est la première étape pour structurer vos données. Ceci est réalisé grâce aux commandes CREATE DATABASE et CREATE TABLE.

Exemple :

  Création d'une base de données :

```sql

CREATE DATABASE MaBaseDeDonnées;
```
Création d'une table Clients :

```sql

    CREATE TABLE Clients (
        ID_Client INT PRIMARY KEY,
        Nom VARCHAR(50),
        Email VARCHAR(100)
    );
```
## Introduction aux contraintes

Les contraintes garantissent l'intégrité des données en définissant des règles sur les données. Les plus courantes sont PRIMARY KEY, FOREIGN KEY, UNIQUE, et NOT NULL.

Exemple :
Définir l'ID_Client comme clé primaire et l'email comme unique :

```sql

CREATE TABLE Clients (
    ID_Client INT PRIMARY KEY,
    Nom VARCHAR(50),
    Email VARCHAR(100) UNIQUE NOT NULL
);
```
## ALTER TABLE : ajout/suppression de colonnes, changement de type de données

Modifiez la structure de vos tables pour répondre à des besoins changeants en utilisant la commande ALTER TABLE.

Exemple :

 Ajout d'une colonne téléphone :

```sql

ALTER TABLE Clients ADD Téléphone VARCHAR(15);
```
Changement du type de données d'une colonne :

```sql

ALTER TABLE Clients ALTER COLUMN Téléphone INT;
```
## Suppression de bases de données et tables

Pour supprimer des bases de données et des tables, utilisez les commandes DROP DATABASE et DROP TABLE.

Exemple :

  Suppression d'une table :

```sql

DROP TABLE Clients;
```
Suppression d'une base de données :

```sql

DROP DATABASE MaBaseDeDonnées;
```
