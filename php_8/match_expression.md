# Match expression

Très similaire au switch

Comme le switch le match compare un sujet avec plusieur alternative

Contrairement au switch

- Le break; n'est pas necessaire
- La comparaison est une égalité strict
- Les alternatives sont evalué comme cela est fait dans une expression ternaire

## Exemple

```php

$result = match($input) {
    0 => 'Zéro',
    1, 2, 3 => 'Un, Deux ou Trois',
    default => 'Plus de trois'
}
```
```php
$age = 21;

$result = match(true) {
    $age < 18 => 'Mineur',
    $age >= 18 => 'Majeur'
}
```
