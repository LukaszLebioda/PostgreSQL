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
- psql => e.g. \q (quit), \l (list databases), \? (more help);

## connect to a database:

- psql -h localhost -p 5432 -U llebioda mypostgres (to connect to a database);
- psql => \l; psql => \c mypostgres;

# SQL

## Databases

- CREATE DATABASE mypostgres;
- DROP DATABASE mypostgres;
