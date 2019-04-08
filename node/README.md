# Server security

## Prep

```
sh setup.sh
```

## MySQL Setup

#### windows:

```
https://dev.mysql.com/downloads/installer/
```

#### Debian:

```
wget http://repo.mysql.com/mysql-apt-config_0.8.9-1_all.deb
sudo dpkg -i mysql-apt-config_0.8.9-1_all.deb
sudo apt update
sudo apt install mysql-server
sudo systemctl restart mysql
sudo mysql_secure_installation
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

## MySQL

### Password has expired

```
mysql -u root -p
ALTER USER `root`@`localhost` IDENTIFIED BY 'password';
flush privileges;
```

### reset password

```
ALTER USER `root`@`localhost` IDENTIFIED BY '';
flush privileges;
```

### ER_NOT_SUPPORTED_AUTH_MODE

```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
flush privileges;
```
