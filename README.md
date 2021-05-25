<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# todo-laravel

> A Laravel project

The project is the Server for the [Vue client](https://github.com/MikiWojak/todo-vue)

## General setup

- Clone the repository
- Copy __.env.example__ file to __.env__
- Edit the database credentials in the __.env__ file
- Open Terminal and execute the commands:

```bash
# Install libraries, packages, etc.
composer install

# Generate application key
php artisan key:generate

# Create tables in the database
php artisan migrate

# Install Laravel Passport and generate the clients
php artisan passport:install
# 'Client ID' and 'Client secret' of the 'Password grant client' will be used further
# The credentials are also in the database in the table 'oauth_clients'
```

- Open again the __.env__ file and edit consts:
    - `PASSPORT_LOGIN_ENDPOINT` - the endpoint in charge of authentication, for instance: "http://todo-laravel.com/oauth/token"
    - `PASSPORT_CLIENT_ID` - 'Client ID' of the 'Password grant client'
    - `PASSPORT_CLIENT_SECRET` - Client secret' of the 'Password grant client'
