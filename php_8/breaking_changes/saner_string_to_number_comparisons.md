# Saner string to number comparisons

Certaine comparaison étrange ont été corrigé

## Exemple
```php
var_dump(0 == "foo");
```

En PHP 7
```text
bool(true)
```

En PHP 8
```text
bool(false)
```
