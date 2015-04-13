#Slim PHP

>[Slim](http://www.slimframework.com/) en un microframework PHP que le ayuda  a escribir con rapidez aplicaciones web simples.

##Instalacion

Para instalar slim via composer creamos el archivo **composer.json** con la siguiente dependencia en **require**.

```
{
    "require": {
        "slim/slim": "2.*"
    }
}
```

##Usando Slim

Para usar Slim cargamos el archivo **require 'vendor/autoload.php'** que genera composer y creamos una instancia **$app = new \Slim\Slim()**.
Podemos definir una ruta HTTP GET **$app->get('ruta',funcion_asociada())**. Entonces corremos la aplicacion **$app->run**.
 
```
	<?php 	require 'vendor/autoload.php';
		$app = new \Slim\Slim();
		$app->get('/hello/:name', function ($name) { echo "Hello, $name"; });
		$app->run();
```
