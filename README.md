## Base Docker Setup for PHP 7.4 + FPM & NGINX & MariaDB

## Instructions

### Add Laravel
- cd .
- git clone https://github.com/laravel/laravel.git laravel

Or you can bring over an existing laravel application

### Update Dockerfile

- set your project root appropriately
- Volumes are your persistent data, you will not lose them on shutdowns, only if you prune the volume
- Mount your local code to the volume so that you can make changes from your local machine

### Docker-compose.yml

- This file defines the build process. If your setup requires a custom image, create a seperate Dockerfile so that you can include your neccessary build steps there.
- The image, if built from a Dockerfile will need to one you create, use your own username/new-image-name as a general naming convention
- Be sure to update the php74 image name


## Helpful Commands

- docker-compose up ( brings up the containers and shows output in the terminal )
- docker-compose up --build ( rebuilds any changes made to the Dockerfile )
- docker-compose up -d ( brings up the containers in detached mode, so you can use your terminal for other things )
- docker-compose down ( brings them down )

- docker ps ( lists all your active containers and get their id's )
- docker exec -it {containerId} /bin/bash ( ssh into your container )