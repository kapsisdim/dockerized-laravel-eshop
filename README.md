# dockerized-laravel-eshop

# Installation guide

RUN `docker-compose up -d --build`

RUN `docker-compose exec app composer install`

RUN `docker-compose exec app cp .env.example .env`

RUN `docker-compose exec app cp .env.example .env.testing`

RUN `docker-compose exec app php artisan key:generate`

RUN `docker-compose exec app php artisan storage:link`

# DB setup guide

RUN `docker exec -it mysql-container bash`

RUN `mysql -u root -p`

RUN `root`

RUN `create database my_shop_db;`

RUN `exit;`

RUN `exit;`

RUN `docker-compose exec app php artisan migrate:refresh --seed`
