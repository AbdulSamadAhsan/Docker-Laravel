# Laravel Docker Development Environment

Containerized Laravel development environment with PHP, Nginx, MySQL, and phpMyAdmin.

## Overview

- Docker Compose services for application and database
- Nginx configuration
- phpMyAdmin for local database administration

## Run locally

Requires Docker with Docker Compose.

```bash
git clone https://github.com/AbdulSamadAhsan/Docker-Laravel.git
cd Docker-Laravel/laravelseven
docker compose up -d --build
docker compose exec app composer install
```

Copy `src/.env.example` to `src/.env`. Configure the database host as `mysql`, port `3306`, and use the local development database values defined in `docker-compose.yml`.

```bash
docker compose exec app php artisan key:generate
docker compose exec app php artisan migrate
```

- Application: `http://localhost:8001`
- phpMyAdmin: `http://localhost:8082`
- MySQL host port: `3308`

## Scope

This is a local development scaffold. Review the image versions and replace example credentials before using it outside a local environment. Application source lives in `laravelseven/src/`.

## Author

[Syed Abdul Samad Ahsan](https://github.com/AbdulSamadAhsan)
