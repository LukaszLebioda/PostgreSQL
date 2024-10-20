# Postgres.app

- Postgress.app (https://postgresapp.com/downloads.html); this will install PostgreSQL 17 (or other version);
- launch Postgress.app; a little elephant icon appears on the top bar; click that icon and press "start" next to PostgreSQL17 => this will start the db-server, which gives us acces to our databases;

# DBeaver

- create => connection => PostgreSQL;
- host => localhost; port => 5432;

# CLI:

## general

- terminal => vi .zshrc => export PATH=$PATH:/Applications/Postgres.app/Contents/Versions/17/bin
- terminal => source .zshrc
- now we have access to psql command;
- terminal => psql --help (some help);
- psql => help => to see short list of hints;
- psql => e.g. \q (quit), \? (more help);

## connect to a database + commands:

- psql -h localhost -p 5432 -U llebioda mypostgres (to connect to a database);
- or: \c mypostgres
- psql => \l => list all databases
- psql => \d => list all tables
- psql => \d tablename => displays particular table

# SQL

## Databases

each command must end with " ; ", otherwise it won't be recognized

CREATE DATABASE mypostgres;
DROP DATABASE mypostgres;

CREATE TABLE mytable (
id BIGSERIAL NOT NULL PRIMARY KEY,
name VARCHAR(50) NOT NULL,
age INT NOT NULL,
date DATE,
email VARCHAR(150)
);
DROP TABLE mytable;

# to-do

- Postgress.app => PostgreSQL 17 => start server,
- terminal => psql,
- psql => \c databasename,
