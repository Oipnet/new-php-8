# Throw expression

PHP 8 offre la possibilit√© d'utiliser throw dans plusieurs nouveaux contextes

```php
$triggerError = fn () => throw new MyError();

$foo = $bar['offset'] ?? throw new OffsetDoesNotExist('offset');
```
