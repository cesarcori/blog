Trying restore database "pg_restore", It raise the error: input file
appears to be a text format dump. Please use psql. 

As a prompt says --please use psql-- it's necessary use psql.

    psql -U username -d name-database < database-backup.sql

That command is necessary when I use the command pg_dump: 

    pg_dump -U username -d name-database > database-backup.sql

Before I was using the common way with DBeaver, Tools > backup. That was the difference.