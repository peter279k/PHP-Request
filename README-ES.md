# PHP Request library

[![Latest Stable Version](https://poser.pugx.org/josantonius/request/v/stable)](https://packagist.org/packages/josantonius/request) [![Total Downloads](https://poser.pugx.org/josantonius/request/downloads)](https://packagist.org/packages/josantonius/request) [![Latest Unstable Version](https://poser.pugx.org/josantonius/request/v/unstable)](https://packagist.org/packages/josantonius/request) [![License](https://poser.pugx.org/josantonius/request/license)](https://packagist.org/packages/josantonius/request)

[Spanish version](README-ES.md)

Librería PHP para manejo de peticiones.

---

- [Instalación](#instalación)
- [Requisitos](#requisitos)
- [Cómo empezar y ejemplos](#cómo-empezar-y-ejemplos)
- [Métodos disponibles](#métodos-disponibles)
- [Uso](#uso)
- [Tests](#tests)
- [Manejador de excepciones](#manejador-de-excepciones)
- [Contribuir](#contribuir)
- [Repositorio](#repositorio)
- [Autor](#autor)
- [Licencia](#licencia)

---

### Instalación 

La mejor forma de instalar esta extensión es a través de [composer](http://getcomposer.org/download/).

Para instalar PHP Request library, simplemente escribe:

    $ composer require Josantonius/Request

### Requisitos

Esta ĺibrería es soportada por versiones de PHP 7.0 o superiores y es compatible con versiones de HHVM 3.0 o superiores.

Para utilizar esta librería en HHVM (HipHop Virtual Machine) tendrás que activar los tipos escalares. Añade la siguiente ĺínea "hhvm.php7.scalar_types = true" en tu "/etc/hhvm/php.ini".

### Cómo empezar y ejemplos

Para utilizar esta librería, simplemente:

```php
require __DIR__ . '/vendor/autoload.php';

use Josantonius\Request\Request;
```
### Métodos disponibles

Métodos disponibles en esta librería:

```php
Request::get();
Request::post();
Request::files();
Request::put();
Request::del();
Request::isGet();
Request::isPost();
Request::isPut();
Request::isDelete();
Request::isAjax();
```
### Uso

Ejemplo de uso para esta librería:

```php
<?php
require __DIR__ . '/vendor/autoload.php';

use Josantonius\Request\Request;

if (Request::isPost()) {

    $name = Request::post('name');
}
```

### Tests 

Para utilizar la clase de [pruebas](tests), simplemente:

```php
<?php
$loader = require __DIR__ . '/vendor/autoload.php';

$loader->addPsr4('Josantonius\\Request\\Tests\\', __DIR__ . '/vendor/josantonius/request/tests');

use Josantonius\Request\Tests\RequestTest;
```
Métodos de prueba disponibles en esta librería:

```php
RequestTest::testGet();
RequestTest::testGetSpecificKey();
RequestTest::testPost();
RequestTest::testPostSpecificKey();
RequestTest::testFiles();
RequestTest::testFilesSpecificKey();
RequestTest::testPut();
RequestTest::testPutSpecificKey();
RequestTest::testDel();
RequestTest::testDelSpecificKey();
RequestTest::testIsGet();
RequestTest::testIsPost();
RequestTest::testIsPut();
RequestTest::testIsDelete();
RequestTest::testIsAjax();
```

### Manejador de excepciones

Esta librería utiliza [control de excepciones](src/Exception) que puedes personalizar a tu gusto.
### Contribuir
1. Comprobar si hay incidencias abiertas o abrir una nueva para iniciar una discusión en torno a un fallo o función.
1. Bifurca la rama del repositorio en GitHub para iniciar la operación de ajuste.
1. Escribe una o más pruebas para la nueva característica o expón el error.
1. Haz cambios en el código para implementar la característica o reparar el fallo.
1. Envía pull request para fusionar los cambios y que sean publicados.

Esto está pensado para proyectos grandes y de larga duración.

### Repositorio

Los archivos de este repositorio se crearon y subieron automáticamente con [Reposgit Creator](https://github.com/Josantonius/BASH-Reposgit).

### Autor

Mantenido por [Josantonius](https://github.com/Josantonius/).

### Licencia

Este proyecto está licenciado bajo la **licencia MIT**. Consulta el archivo [LICENSE](LICENSE) para más información.