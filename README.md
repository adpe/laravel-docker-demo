# Laravel Docker Demo
A pretty simplified Docker setup of containers for local Laravel development. You can view the full repository and article that inspired this repo under:
- https://github.com/aschmelyun/docker-compose-laravel
- https://www.digitalocean.com/community/tutorials/how-to-containerize-a-laravel-application-for-development-with-docker-compose-on-ubuntu-18-04

## Requirements
To get started, make sure you have [Docker installed](https://docs.docker.com/docker-for-windows/install/) on your system.

## Installation
1. Clone this repository `git clone https://github.com/adpe/laravel-docker-demo.git`
2. Navigate to the directory you cloned this repository.
3. Build or pull image `docker pull adpe/laravel-demo:mssql` and spin up the containers for the web server by running `docker-compose up -d`.
4. Cleanup and prepare `www` directory, run `docker-compose exec app rm .gitkeep`.
5. After that create a new Laravel project with `docker-compose exec app composer create-project laravel/laravel .` or provide your existing Laravel project files in the `www` directory, run if your provide a existing project and neccesary these commands:
   - `docker-compose exec app composer install`
   - `docker-compose exec app php artisan key:generate`
6. Now go to your browser and access your server's domain name or IP address on port 8000 (http://server_domain_or_IP:8000)