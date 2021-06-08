# docker-lamp

Creates a MySQL Server.
Stored (persisted) in a folder called ‘database’ where your compose file is.

The ‘command’ switches new MySQL back to the old auth type, supported by most PHP apps.
Creates a phpMyAdmin access point.
Web GUI accessible on port 8082.

Creates an SMTP Mail Catcher.
Configure your apps to send emails to host mail on port 1025, with no authentication.
Web GUI accessible on port 8081.

Finally, creates a PHP (Apache) frontend.
HTTP accessible on port 8080.

Uses content found in folder ‘www’ relative to where your compose file is.
Loads last, after DB and Mail have been setup by Docker.

Run with docker-compose up and congratulations – You have a development LAMP stack running via Docker!


More command info
docker-compose (up/stop/down)

Docker compose is the magical command that translates your yml configuration file into docker commands.

up runs the containers detailed in the config file (will create them, or start up stopped containers).
stop pauses the containers, like clicking shutdown on your PC.
down stops and deletes your containers, ready to start fresh. Data in volumes are not deleted.
