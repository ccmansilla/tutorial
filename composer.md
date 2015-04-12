#Composer

>En el mundo de PHP existen soluciones disponibles (librerias de codigo abierto) para las tareas mas comunes de una aplicacion. Composer es una herramienta de gestion de dependencias de librerias en PHP. Esta se ejecuta desde una terminal y permite instalar las librerias declaradas como requeridas en un archivo (composer.json). Estas librerias estan disponibles generalmente en su repositorio principal "Packagist". 

##Instalacion
Para instalar composer basta con ejecutar en la terminal:

```
    #curl -sS https://getcomposer.org/installer | php
    #sudo mv composer.phar /usr/local/bin/composer
```

##Usando Composer

Para comenzar a usar composer en tu proyecto, necesitas crear en el directorio del mismo un archivo llamado **composer.json**. Este archivo describe las dependencias de tu proyecto y debe contener tambien otros metadatos.

```
{
    "require": {
        "monolog/monolog": "1.0.*"
    }
}
```

Luego instalamos las dependencias al ejecutar:

```
	#composer install
```

Para utilizar las librerias instaladas simplemente incluya un archivo ***vendor/autoload.php** que composer genera para hacerlo mas facil.

```
	require 'vendor/autoload.php';
	$log = new Monolog\Logger('name');
	$log->pushHandler(new Monolog\Handler\StreamHandler('app.log', Monolog\Logger::WARNING));

	$log->addWarning('Foo');
```  
