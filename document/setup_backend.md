## 1: Setup laravel

-   Before setup laravel, you need to have **xampp**, **composer**
-   Install **laravel**

```bash
composer global require laravel/installer
```

-   create new project

```bash
laravel new laravel-react-full-stack
```

-   In this project we use **sqlite** as database, not use **mysql**, so you can change this in **.env**

```php
DB_CONNECTION=sqlite

DB_DATABASE=database\database.sqlite
DB_FOREIGN_KEYS=true
```

-   use need create **database.sqlite** in **database** folder
-   must sure that in **php.init** remove **;** in **extension=pdo_sqlite**
-   Then run `php artisan migrate` to create database. Remember, when use **sqlite**, you need to comment DB_HOST, DB_PORT,DB_USERNAME, DB_PASSWORD
-   [config sqlite](https://laravel.com/docs/8.x/database#sqlite-configuration)
-   Then run `php artisan serve` to start server
