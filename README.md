docker run --name postgres_container \
  -e POSTGRES_USER=dataiku \
  -e POSTGRES_PASSWORD=dataiku \
  -e POSTGRES_DB=sql_database \
  -p 5432:5432 \
  -itd postgres:latest


  -- Création de la base de données
CREATE DATABASE test_database;

-- Connexion à la base de données
\c test_database;

-- Création de la table 'customers'
CREATE TABLE IF NOT EXISTS customers (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    city VARCHAR(100)
);

-- Insertion des données dans la table 'customers'
INSERT INTO customers (name, age, city) VALUES
('Alice', 35, 'New York'),
('Bob', 28, 'San Francisco'),
('Charlie', 40, 'Los Angeles'),
('Diana', 25, 'Boston');



psql -U ton_utilisateur -h ton_hote -d postgres

\i create_customers_database_pgsql.sql





Diapositive 1 : Titre
Découvrez la fonctionnalité "Generate SQL AI" dans Dataiku
•	Présenté par : [Ton Nom]
•	Date : [Date]
________________________________________
Diapositive 2 : Introduction à Dataiku
•	Dataiku : Plateforme d'analytics et de data science permettant de créer et déployer des modèles de machine learning.
•	Objectif : Simplifier l'analyse de données grâce à des outils automatisés et intelligents.
________________________________________
Diapositive 3 : Qu'est-ce que "Generate SQL AI" ?
•	Une fonctionnalité qui permet à l'IA de générer des requêtes SQL automatiquement.
•	Convertir des requêtes en langage naturel ou des besoins analytiques en requêtes SQL.
•	Pas besoin de connaître le SQL pour générer des requêtes complexes.
________________________________________
Diapositive 4 : Avantages de "Generate SQL AI"
•	Simplicité : Pas de besoin de connaissance SQL.
•	Gain de temps : Générez des requêtes SQL rapidement.
•	Précision : Requêtes optimisées par l'IA.
•	Adaptabilité : Utilisation sur différents types de bases de données et scénarios complexes.
________________________________________
Diapositive 5 : Comment utiliser "Generate SQL AI" ?
1.	Accéder à l'outil :
o	Ouvrir un projet Dataiku.
o	Aller dans le volet "SQL" ou "Notebooks".
2.	Entrer une requête en langage naturel :
o	Exemple : "Je veux savoir le total des ventes par région pour l'année 2023".
________________________________________
Diapositive 6 : Exemple de génération de SQL
•	Requête entrée :
o	"Je veux savoir le total des ventes par région pour l'année 2023".
•	SQL généré automatiquement :
sql
Copy
SELECT region, SUM(sales) as total_sales 
FROM sales_data 
WHERE year = 2023 
GROUP BY region;
________________________________________
Diapositive 7 : Vérification et exécution de la requête
•	Vérification : L'utilisateur peut examiner et modifier la requête générée.
•	Exécution : Une fois vérifiée, la requête est exécutée directement dans Dataiku pour obtenir les résultats.
________________________________________
Diapositive 8 : Exemple d'usage pratique
•	Cas d'utilisation :
o	Question : "Quels produits ont généré les meilleures ventes en 2023 ?"
•	Requête SQL générée :
sql
Copy
SELECT product_name, SUM(sales) as total_sales 
FROM sales_data 
WHERE year = 2023 
GROUP BY product_name 
ORDER BY total_sales DESC;
•	Cette requête est prête à être exécutée dans Dataiku.
________________________________________
Diapositive 9 : Conclusion
•	"Generate SQL AI" : Facilite la création de requêtes SQL dans Dataiku, idéal pour les utilisateurs sans expérience SQL.
•	Bénéfice : Gain de temps et efficacité dans l'analyse des données.
________________________________________
Diapositive 10 : Questions et Réponses
•	Questions : Ouvre la session pour des questions et réponses.
________________________________________
Conseils pour les captures d'écran :
•	Pour chaque étape où tu expliques un processus (accès à l'outil, entrée de la requête, génération de SQL, exécution), prends une capture d'écran de l'interface Dataiku pour illustrer visuellement chaque étape.


