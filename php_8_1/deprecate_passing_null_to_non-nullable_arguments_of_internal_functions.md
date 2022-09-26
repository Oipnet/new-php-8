# Deprecate passing null to non-nullable arguments of internal functions

Le fait de passer un null pour un argument non nullable d'une fonction interne de php déclanchera une notice de deprecation.

```php
str_contains("string", null);
```

En PHP 9 les deprecations seront converties en erreurs
