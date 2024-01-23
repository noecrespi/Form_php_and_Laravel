Pasos para crear el proyecto

Crear el proyecto. 
```bash
composer create-project --prefer-dist laravel/laravel nombreProyecto
```

Poara empezar el crud. Hay que crear un controlador.
```bash
php artisan make:controller nombreController
```

Crar el modelo y mamigracion para poder establecer con el sistema de persistencia. Se genera las dos cosas a la vez. 
```bash
php artisan make:model nombre --migration
```

Establecer conecxion con la base de datos. Entrare en el `.env`
```.env
DB_CONNECTION=pgsql
DB_HOST="randion.es"
DB_PORT=5432
DB_DATABASE="nombreBaseDatos"
DB_USERNAME="Ususario"
DB_PASSWORD="Contraseña"
```

parte de persistencia
- database/migrations/2020_05_12_000000_create_users_table.php
```php 
Schema::create('publicacions', function (Blueprint $table) {
            $table->id();
            $table->string('title');        // añadido
            $table->string('description'); // añadido
            $table->timestamps();
        });
```

- app/Models/Publicacion.php
```php 
use HasFactory;

    protected $fillable = [ // añadido
        "title",            // añadido
        "description",      // añadido
    ];
```

ejecutar la migracion de todos los elemntos 
```bash
php artisan migrate
```

