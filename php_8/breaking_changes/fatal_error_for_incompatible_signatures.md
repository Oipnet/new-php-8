# Fatal error for incompatible method signatures

Le code suivant en PHP 7 une Fatal Error
```php
interface I {
    public function method(array $a);
}
class C implements I {
    public function method(int $a) {}
}
```

alors que le suivant se contente d'un warning
```php
class C1 {
    public function method(array $a) {}
}
class C2 extends C1 {
    public function method(int $a) {}
}
```
Le comportement a été uniformisé en PHP 8.
