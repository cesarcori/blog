## Comandos

    cat dump-db-202311031843 | sudo docker exec -i postgres-name-container pg_restore -U <name_username> -d <name_database>

## Detalles

Problema de Native client is not specified for connection. Es porque no tengo postgres instalado nativamente, lo utilizo por docker.

## Fuente

https://stackoverflow.com/questions/24718706/backup-restore-a-dockerized-postgresql-database

https://simkimsia.com/how-to-restore-database-dumps-for-postgres-in-docker-container/

https://www.youtube.com/watch?v=q_Zy0eGPmvk