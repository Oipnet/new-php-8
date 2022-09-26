# Autovivification on false

L'initialisation d'un tableau avec false permettait de construire un tableau vide.

En PHP 8 cela provoquera une notice de déprécation

```php
$array = false;

$array[] = 2;

// Automatic conversion of false to array is deprecated
```
