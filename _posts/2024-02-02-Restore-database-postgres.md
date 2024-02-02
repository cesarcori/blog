Trying restore database I find in error, because I backup with dump,
and when you use pg_dump for make backups, it's necessary use psql.

    psql -U username -d name-database < database-backup.sql

Another command to do this: 

    pg_restore -U username -d 'name-database' 'database-backup'

This problem raise because I use the command pg_dump: 

    pd_dump -U username -d name-database > database-backup.sql

Before I was using the common way with DBeaver. That was the difference.