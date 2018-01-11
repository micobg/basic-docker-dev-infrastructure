# basic-docker-dev-infrastructure
A simple Docker development infrastructure of LAMP backend server and nginx for the frontend.

Just run **docker-compose** command to start.
```
docker-compose up -d --build
```

It contains of four containers:

## Frontend
Latest version of nginx server is used for frontend container. It is bound to *localhost* on port *80*. The code is placed in *frontend* directory.

## Backend
Apache + PHP (last version) runs at the backend. You can find it on *localhost:5000*.

## MySQL
The password for *root* user in mysql is placed in *config/secrets.env* file. Fell free to change it to something more secure.

## phpMyAdmin
phpMyAdmin panel can be found on *localhost:8080*.

Enjoy web development!
