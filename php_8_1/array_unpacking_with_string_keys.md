# Array unpacking with string keys

Il est dorénavant possible d'utiliser ... sur les array dont les clés sont des chaines de charactère

```php
$array1 = ["a" => 1];

$array2 = ["b" => 2];

$array = ["a" => 0, ...$array1, ...$array2];

var_dump($array); // ["a" => 1, "b" => 2]
```
