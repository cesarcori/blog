## Solution

I use the next command to get what I wanted. 

Into psql and connected to the database:

    \copy (SELECT id, field FROM) to '~/file-output.csv' with DELIMITER '|' csv HEADER

## Execute command psql in shell

    psql -U postgres -d database-name -c "select * from table"

Con eso incluso se puede exportar la salida.


https://stackoverflow.com/questions/18223665/postgresql-query-from-bash-script-as-database-user-postgres

## Ingresar a psql

Por defecto tratará de ingresar a una base de datos de nombre: postgres
sin no existe, saldrá error. 

    psql -U postgres
    sudo -u postgres psql

Directamente a una base de datos: 

    psql -d database-name -U postgres

En caso de no tener configurado nada: 

    sudo -i -u postgres

https://phoenixnap.com/kb/how-to-connect-postgresql-database-command-line

## En caso de un script con password

https://dba.stackexchange.com/questions/14740/how-to-use-psql-with-no-password-prompt

## Ejecutar un archivo sql en psql

    psql -d database-name -U postgres -f /path/file.sql

https://www.warp.dev/terminus/psql-run-sql-file

## Source: 
[fuente](https://hevodata.com/learn/postgres-export-to-csv/)