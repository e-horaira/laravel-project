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

## How to run Laravel Project from GitHub
1. 
```
composer install
```
or,

```
composer update
```

2. .env.example to .env and update database part
3. create database from Xampp or other server
4. Run
```
php artisan migrate
```
5. 
```
php artisan key:generate
```

6. 

```
 php artisan storage:link
```
7. 
```
php artisan serve
```


## Query Builder
Add this line routes/web.php

`use Illuminate\Support\Facades\DB;`

### Create Operations

```
$user = DB::table('users')
                ->insert([
                    "name"      => "Admin Four",
                    "email"     => "hashem.home18@yahoo.com",
                    "password"  => "MyPassword1",
                ]);
dd($user);
```

### Read Operations

```
$users = DB::table('users')
                ->get();
dd($users);
```
or

```
$user = DB::table('users')
                ->where('id',1)
                ->get();
dd($user);
```

### Update Operations

```
$user = DB::table('users')
                ->where('id', 3)
                ->update([
                    'email' => "admin@example.com",
                ]);
```

### Delete Operations

```
$user = DB::table('users')
                ->where('id',3)
                ->delete();
```

## ORM object-relational mapper

Add this line routes/web.php

``use App\Models\User;``

### Create a new user

```
$user = User::create([
        "name"      => "Aesha Seri",
        "email"     => "aesha.hasina@yahoo.com",
        "password"  => "amihasina420",
    ]);
dd($user);
```

### Read a data

```
$user = User::where('id',1)->get();
dd($user);
```
or, 
```
$users = User::get(); // to get all users
```
or, 
```
$users = User::all(); // to get all users
```



### Update an existing user

```
$user = User::where('id', 6)->first();
```
or

```
$user = User::find(6);
```

```
$user->update([
        "email" => "hashem.home18@gmail.com",
    ]); 
dd($user);
```

### Delete an existing user

Step 1: 
```
$user = User::where('id', 6)->first();
```
or

```
$user = User::find(6);
```

Step 2: 
```
$user->delete();
```

