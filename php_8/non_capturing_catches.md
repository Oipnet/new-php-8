# Non-capturing catches

Si l'exception n'est pas utilisée dans le bloc catch il est possible de ne pas la préciser.

Il n'est toutefois pas possible d'avoir un cath vide, on utilise Throwable pour catcher tous les types

## Avant PHP 8
```php
try {
    // Something goes wrong
} catch (MySpecialException $exception) {
    Log::error("Something went wrong");
}
```

## En PHP 8
```php
try {
    // Something goes wrong
} catch (MySpecialException) {
    Log::error("Something went wrong");
}
```
