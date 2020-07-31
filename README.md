# Laravel Docker Demo
A pretty simplified Docker setup of containers for local Laravel development. You can view the full repository and article that inspired this repo under:
- https://github.com/aschmelyun/docker-compose-laravel
- https://www.digitalocean.com/community/tutorials/how-to-containerize-a-laravel-application-for-development-with-docker-compose-on-ubuntu-18-04

## Requirements
To get started, make sure you have [Docker installed](https://docs.docker.com/docker-for-windows/install/) on your system.

## Installation
1. Then clone this repository.
2. Next, navigate in your terminal to the directory you cloned this repository.
3. Build or pull image and spin up the containers for the web server by running `docker-compose up -d`.
4. After that...
   a) provide your Laravel project files in to the `www` directory and run...
     - `docker-compose exec app composer install`
     - `docker-compose exec app php artisan key:generate`
   b) or create a new Laravel project with command `docker-compose exec app composer create-project laravel/laravel .`.
5. Now go to your browser and access your server's domain name or IP address on port 8000 (http://server_domain_or_IP:8000)