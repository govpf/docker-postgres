# Docker PostgreSQL

Procédure de génération de container PostgreSQL.

## Variables d'environnement

Attribute        | Description | Type | Default
-----------------|-------------|------|--------
POSTGRES_DB | postgress database | string | postgres
POSTGRES_USER | postgres user | string | postgres
POSTGRES_PASSWORD | postgres password | string | postgres
PGDATA | postgres data path | string | /var/lib/postgresql/data

## Utilisation

Build

```
docker build -t dsipf/postgres:latest 11
```

--------------

Exécution

```
docker run --name my-postgres -d -p 5432:5432 dsipf/postgres
```

```
docker run --name my-postgres -d -p 5432:5432 -v postgres_sample:/var/lib/postgresql dispf/postgres
```

```
docker run --name my-postgres -d [-p 5432:5432] [-e POSTGRES_DB=my_database] [-e POSTGRES_USER=my_user] [-e POSTGRES_PASSWORD=my_password] dsipf/postgres
```

> Configuration par défaut: 
>  - username: postgres
>  - password: postgres
>  - database: postgres


## Développement

### Pré-requis

* Docker ([https://docs.docker.com/engine/installation/](https://docs.docker.com/engine/installation/))

#### Initialisation

```
git clone https://gitlab.gov.pf/docker/postgres.git docker-postgres
cd docker-postgres
```
