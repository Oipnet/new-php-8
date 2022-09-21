# Allowing ::class on objects

Il est maintenant possible d'utiliser ::class directement sur un objet au lieu de passer par la méthode get_class()

Cela fonctionne de la meme manière que get_class()

```php
$foo = new Foo();

var_dump($foo::class);
```
