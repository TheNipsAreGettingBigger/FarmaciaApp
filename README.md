# ENTORNOS PARA LA BASE DE DATOS

## ENTORNO DE DESARROLLO

```sql
select user from mysql.user;
CREATE USER 'admin_farmacia'@'127.0.0.1' IDENTIFIED BY 'secret';

CREATE DATABASE IF NOT EXISTS farmacia_db;
GRANT ALL PRIVILEGES ON farmacia_db.* TO 'admin_farmacia'@'127.0.0.1';
FLUSH PRIVILEGES; 
```

## ENTORNO DE TESTING

```SQL
select user from mysql.user;
CREATE USER 'admin_farmacia_test'@'127.0.0.1' IDENTIFIED BY 'secret';

CREATE DATABASE IF NOT EXISTS farmacia_db_test;
GRANT ALL PRIVILEGES ON farmacia_db_test.* TO 'admin_farmacia_test'@'127.0.0.1';
FLUSH PRIVILEGES;
```

```sh
  npm run m:gen --  src/migrations/initDB
  npm run m:run
```

```sh
 # railway
 CREATE USER 'admin_farmacia'@'127.0.0.1' IDENTIFIED BY 'secret';
  GRANT ALL PRIVILEGES ON railway.* TO 'admin_farmacia'@'127.0.0.1';
  FLUSH PRIVILEGES; 

 npm run m:gen --  src/migrations/initDB
npm run m:run
```
