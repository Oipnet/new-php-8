# new in initializers

Il est possible d'utiliser le mot clés new dans la définition d'une fonction pour une valeur par defaut

```php
class MyController {
    public function __construct(
        private Logger $logger = new NullLogger(),
    ) {}
}
```
