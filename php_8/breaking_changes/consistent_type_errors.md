# Consistent type errors

Les méthodes internes de php ne levait pas d'exception en cas d'erreur de type lors de leur appel.

C'est desormais le cas

## Avant PHP 8
```php
$result = explode([], 'test');

var_dump($result);
```
```text
Warning: explode() expects parameter 1 to be string, array given in /home/user/scripts/code.php on line 3
NULL
```

## Après PHP 8
```php
$result = explode([], 'test');

var_dump($result);
```
```text
Fatal error: Uncaught TypeError: explode(): Argument #1 ($separator) must be of type string, array given in /home/user/scripts/code.php:3
Stack trace:
#0 /home/user/scripts/code.php(3): explode(Array, 'test')
#1 {main}
  thrown in /home/user/scripts/code.php on line 3
```
