## Create New Project
- $ cd /var/www/php-projects
- $ composer create-project --prefer-dist laravel/laravel project-name
- $ cd project-name 
- $ php artisan serve

---
## Generate basic scaffolding...
- $ composer require laravel/ui
- $ php artisan ui bootstrap
- $ npm install && npm run dev //to install all debedcice in pakage.json and compile it


## Authintecation Scaffold
- $ composer require laravel/ui
- $ php artisan ui bootstrap --auth
- $ npm install && npm run dev

---

## create DB and congig .env file 

## Database
<this is comment>
- $ php artisan migrate

## Generate Controller 
* $ php artisan make:controller ControllerName

* If you would like to generate a Resource Controller "CRUD":
    - $ php artisan make:controller ControllerName --resource
* Specifying The Resource Model - If you are using route model binding and would 
     like   the resource controller's methods to type-hint a model instance:
     
    - $ php artisan make:controller ControllerName --resource --model=ModelName

## Generate Model
* $ php artisan make:model model-name

* If you would like to generate a database migration with creation of model: 
    - $ php artisan make:model ModelName -m


## Generating Migrations
- $ php artisan make:migration create_users_table --create|table=users 
- Run Migration to DB
    - $ php artisan migrate
- Rolling Back Migrations
    - $ php artisan migrate:rollback
    - $ php artisan migrate
- or 
    <!-- Roll Back & Migrate Using A Single Command -->
    - $ php artisan migrate:refresh

----
## MySQL Commands
- show tables;
- describe tb-name;



## Show Routes List
- $ php artisan route:list

## Composer
- $ composer update


------------------------------

## Command from jeffrey
* for any help in php artisan 
    - $ php artisan help [command]
                        make:model / make:migration
* generate multifiles in single command
    - $ php artisan make:model <ModelName> [options]
    EX: php artisan make:model Project -mc => generrate model with its controller and  its migraton
* tinker
    - $ php artisan tinker
    >>> App\User::find(7)->articles
    >>> App\User::find(7)->articles->count()
    - reversie 
    >>> App\article::find(1)->author
    >>> App\article::find(1)->author->name

* database factory
    - $ php artisan make:factory articleFactory --model=article
    - calling in tinker => factory(App\article::class)->create()
    -                   => factory(App\article::class, 5)->create() // 5 is number of instances
    -                   => factory(App\article::class, 2)->create([
                                                    'user_id' => 1,
                                                    'title' => 'override title'
                                                ]) // atrr overriding

* create a new email class
    - $ php artisan make:mail  // HTML mail
    - $ php artisan make:mail --markdown //markdown templates
    (EX: php artisan make:mail Contact --markdown=emails.contact)

    - Customizing The Components
        - $ php artisan vendor:publish --tag=laravel-mail 
                //Publish any publishable assets from vendor packages


* Create a new notification class
    - $ php artisan make:notification //HTML
    - $ php artisan make:notification --markdown=[PATH] //HTML







