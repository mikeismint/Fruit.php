# Fruit.php

My first attempt at a simple PHP router.
Influenced by [AltoRouter](https://github.com/dannyvankooten/AltoRouter)

## Usage

```php

$router = new Fruit();

// map single route
$router->addRoute('GET', '/', 'Controller#Method');

// map post details page
$router->addRoute('GET', '/^posts\/id\/(?P<id>\d+)$/', 'Controller#Method');

// map multiple routes
$router->addRoutes(array(
    array('GET', '/', 'Controller#Method'),
    array('GET', '/^posts\/id\/(?P<id>\d+)$/', 'Controller#Method'),
));

```

## Other features

  * Accepts multiple HTTP methods separated by `|`
  * Uses regex to match URL pattern
  * Accepts optional fourth parameter to name routes
