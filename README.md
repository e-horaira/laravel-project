# laravel-project

1. example-app projectname
```
composer create-project laravel/laravel example-app
```
2. change to project directory and run server
```
cd example-app
php artisan serve
```
3. Explore some directory, Go to ``resources/views``

``routes/web.php``
   
``composer.json`` packages for this project which will you get on **vendor** directory
   
``phpunit.xml`` for testing purposes

4. full authentication with laravel breeze
```
composer require laravel/breeze --dev

php artisan breeze:install
```
5. Run Xampp Server and then run:
```
php artisan migrate
```
*Note:* If you don't know anything, type help command
>
> php artisan migrate --help
>
> or
>
> php artisan migrate -h

> To Know more about [Migrations](https://laravel.com/docs/10.x/migrations#main-content) or search migrations on laravel documentations
> 
> [migration-video](https://www.youtube.com/watch?v=e5QcI5mDUBI)
