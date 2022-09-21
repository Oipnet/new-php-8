# New str_contains() function

Il n'est plus nécessaire de passer par strpos() pour savoir si une chaine contient une autre chaine

## Avant PHP 8
```php
if (strpos('string with lots of words', 'words') !== false) { /* … */ }
```

## Après PHP 8
```php
if (str_contains('string with lots of words', 'words')) { /* … */ }
```
