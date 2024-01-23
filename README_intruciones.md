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
