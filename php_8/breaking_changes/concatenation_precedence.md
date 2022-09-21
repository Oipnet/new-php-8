# Concatenation precedence

L'ordre des priorités de concaténation a changé en PHP 8

Si vous faites ceci 

```php
echo "sum: " . $a + $b;
```

PHP 7 interprete 
```php
echo ("sum: " . $a) + $b;
```

PHP 8 interprete
```php
echo "sum: " . ($a + $b);
```
