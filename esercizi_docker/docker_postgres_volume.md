# Esercitazione su container postgres

Ho creato un volume _volume_db_, da montare poi nel container nel percorso _/var/lib/postgresql_. Dunque ho creato il container con il comando
- _docker run -e POSTGRES_PASSWORD=password -d -v volume_db:/var/lib/postgresql postgres_

Dopo essere entrato nella bash del container, ho cambiato utente da _root_ al superuser _postgres_ digitando
- _su - postgres_

Dunque ho digitato _psql_ e sono entrato nel client dove ho creato un database e ho inserito alcuni dati in una tabella.

Dopo aver eliminato il container e averlo ricreato come prima, il database era ancora lì.