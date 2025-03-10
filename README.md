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

