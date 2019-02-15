# Server security

## Prep

```
sh setup.sh
```

## Postgresql Setup

#### windows:

```
https://www.postgresql.org/download/windows/
```

#### Debian:

```
emacs /etc/apt/sources.list.d/pgdg.list
- ADD:
deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main

wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
apt-get install postgresql-10 postgresql-client-10 libpq-dev postgresql-server-dev-10 pgadmin4

sudo -u postgres createuser --superuser $USER
sudo -u postgres createdb YOUR_DATABASE_NAME
sudo touch .psql_history
psql
```

## Navicat Setup

```
https://www.navicat.com/en/download/navicat-premium
https://www.jianshu.com/p/5f693b4c9468
```
