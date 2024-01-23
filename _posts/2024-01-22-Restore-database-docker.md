Restore the database could be an easy task, but I find with the
problem when I was working on Docker, and it's because it has
to be over command interface. 

The command that helps me was the next: 

    cat <name-database-to-restore> | sudo docker exec -i <name-container> pg_restore -U <name-user> -d <name-database>

That's it. See you the next post.
