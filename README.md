# Manipulation de données 💽
## Insertion, mise à jour et suppression de données

Pour interagir avec vos données, il est crucial de savoir comment ajouter, modifier et supprimer des enregistrements. Ces opérations sont réalisées avec les commandes INSERT, UPDATE, et DELETE.

Exemple :

### Ajouter un nouveau client :

```sql

INSERT INTO Clients (Nom, Email) VALUES ('Dupont', 'dupont@email.com');
```
### Mettre à jour l'email d'un client :

```sql

UPDATE Clients SET Email = 'new.email@email.com' WHERE Nom = 'Dupont';
```
### Supprimer un client :

```sql

DELETE FROM Clients WHERE Nom = 'Dupont';
```
## Comprendre les transactions

Une transaction est une séquence d'une ou plusieurs instructions SQL qui sont exécutées en tant qu'unité de travail. Les transactions peuvent être validées (COMMIT) ou annulées (ROLLBACK).

Exemple :
Lors de l'ajout d'une nouvelle commande, il peut être nécessaire d'ajouter un nouveau client et de mettre à jour le stock. Ces opérations doivent être effectuées ensemble.

```sql

BEGIN TRANSACTION;

INSERT INTO Clients (Nom, Email) VALUES ('Durand', 'durand@email.com');
INSERT INTO Commandes (Produit, Quantité) VALUES ('Chaise', 3);
UPDATE Stock SET Quantité = Quantité - 3 WHERE Produit = 'Chaise';

-- Si tout est bon
COMMIT;

-- Sinon
ROLLBACK;
```
