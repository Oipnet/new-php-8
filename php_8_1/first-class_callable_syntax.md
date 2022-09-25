# First-class callable syntax

Il est possible de créer une closure à partir d'un callable et lui passant ... 
en paramètre.


```php
function foo(int $a, int $b) { /* … */ }

$foo = foo(...);

$foo(a: 1, b: 2);
```
