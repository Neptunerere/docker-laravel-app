<h1 align="left">Welcome to the starting guide</h1>

<h3>Here is a Docker file I created to run a Laravel project, based on PHP 8.1. Please note that there may be areas that need improvement. 😳</h3>

## Requirements
for building and running the application you need:

- <a href="https://www.docker.com">Docker</a>

## Installation
```bash
$ docker-compose up -d --build
$ docker-compose exec app composer create-project laravel/laravel --prefer-dist application
```

## Guide
If you are checking the APP_KEY in the .env file, please refer to the code below, which retrieves the APP_KEY from the parent folder's .env file if it exists, and generates it if it doesn't.
```
$ cd application
$ cat .env | grep ^APP_KEY
$ php artisan key:generate
```