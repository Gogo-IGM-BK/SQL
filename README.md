# Vues, procédures stockées et déclencheurs 🔍
## Création et utilisation de vues

Les vues sont des représentations virtuelles des résultats d'une instruction SELECT. Elles permettent de simplifier des requêtes complexes en les résumant en une seule "table virtuelle".

Exemple :

  Création d'une vue qui affiche tous les clients actifs :

```sql

CREATE VIEW ClientsActifs AS
SELECT Nom, Email FROM Clients WHERE Statut = 'Actif';
```
Utilisation de la vue :

```sql

SELECT * FROM ClientsActifs;
```
# Introduction aux procédures stockées

Les procédures stockées permettent d'emballer des séquences d'instructions SQL pour exécuter des tâches complexes et les réutiliser facilement.

Exemple :

  Création d'une procédure stockée pour ajouter un client :

```sql

CREATE PROCEDURE AjouterClient (@Nom NVARCHAR(50), @Email NVARCHAR(100))
AS
BEGIN
    INSERT INTO Clients (Nom, Email) VALUES (@Nom, @Email);
END;
```
Exécution de la procédure stockée :

```sql

EXEC AjouterClient 'John Doe', 'john.doe@example.com';
```
## Déclencheurs (Triggers) et leurs utilisations

Les déclencheurs sont des procédures automatiques qui s'exécutent en réponse à des événements spécifiques sur une table ou une vue, tels que les insertions, mises à jour ou suppressions.

Exemple :

   Création d'un déclencheur qui inscrit la date de création pour chaque nouveau client :

```sql

CREATE TRIGGER tr_InsertDateClient
AFTER INSERT ON Clients
FOR EACH ROW 
BEGIN
    UPDATE Clients SET DateCreation = CURRENT_DATE WHERE ID_Client = NEW.ID_Client;
END;
```
