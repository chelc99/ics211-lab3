# ICS211 Web Applications - Lab 3 SOP App

## Purpose:

This project is used for lab 3.

### Folders in this Project:

* `/src` - the source files for the web application.

* `/web` - contains the Dockerfile for building the App Web Server.

### Files in this Project:

* `docker-compose.yml` - instructions for docker-compose to bring up the app. **Don't change anything in this file.**  

* `README.md` - what you're reading right now!

## Directions:

To bring up the environment, do the following:

1. If you are using *Docker for Windows*, **you need to share the drive that has this Project Folder**. In the System Tray, right-click on the Docker icon, select Settings then Shared Drives. Place a check mark next to the drive letter that contains this Project Folder. Hit Apply at the bottom. When it asks you for Credentials, enter in your Windows login credentials.  

2. In a Git Bash Shell, in the same directory as the docker compose file, type:

    `docker-compose up -d`

    This will build a web server image and create a container for the web server. It will also link the project's `/src` folder with `/var/www/html` in the web container.

3. Your application will be at http://localhost:8080

    * If it isn't working, verify that the containers are running: `docker-compose ps`  

    * If you want to look at logs (might help with debugging): `docker-compose logs`

    * If you want an interactive shell with the web server (using Git Bash): `winpty docker exec -it php-apache bash`  

4. When you're done:

    * Stop and remove the container: `docker-compose down`
