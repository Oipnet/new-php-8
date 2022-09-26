# New never type

Le type never permet d'indiquer qu'un methode va arreter le 
flow du programme avec par exemple un exit

```php
function dd(mixed $input): never
{
    // dump
    
    exit;
}
```
