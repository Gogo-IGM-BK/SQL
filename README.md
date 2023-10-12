
# Requêtes avancées 🔍
## Jointures

Les jointures permettent de combiner des données de deux tables ou plus en fonction d'une colonne commune. Les types de jointures courantes comprennent INNER JOIN, LEFT/RIGHT JOIN, et FULL JOIN.

Exemple :
Relier les tables Clients et Commandes sur l'ID_Client :
```sql

SELECT Clients.Nom, Commandes.Produit 
FROM Clients 
INNER JOIN Commandes 
ON Clients.ID_Client = Commandes.ID_Client;
```
## Agrégation

Les fonctions d'agrégation fournissent un moyen de résumer un ensemble de données. Parmi elles, on trouve COUNT, SUM, AVG, MIN, et MAX.

Exemple :
Obtenir le coût total de toutes les commandes :
```sql

SELECT SUM(Prix) AS TotalPrix FROM Commandes;
```
## GROUP BY et HAVING

GROUP BY est utilisé pour regrouper les lignes ayant des valeurs communes. HAVING est utilisé pour filtrer les résultats agrégés.

Exemple :
Nombre de commandes par client avec un total supérieur à 100 :
```sql

SELECT ID_Client, COUNT(ID_Commande) 
FROM Commandes 
GROUP BY ID_Client 
HAVING SUM(Prix) > 100;
```
## Sous-requêtes et requêtes imbriquées

Ces requêtes permettent d'effectuer une requête à l'intérieur d'une autre requête pour filtrer ou transformer davantage les données.

Exemple :
Trouver les clients qui n'ont pas passé de commandes :

```sql

SELECT Nom FROM Clients 
WHERE ID_Client NOT IN 
(SELECT ID_Client FROM Commandes);

```
