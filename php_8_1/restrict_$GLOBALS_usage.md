# Restrict $GLOBALS usage

Il n'est plus possible d'effectuer les opérations suivantes sur la variable $GLOBALS

```php
$GLOBALS = [];
$GLOBALS += [];
$GLOBALS =& $x;
$x =& $GLOBALS;
unset($GLOBALS);

by_ref($GLOBALS); // Run-time error
```
Ce changement a été fait pour des raisons de performance.

Après analyse des 2000 packages les plus utilisés sur Packagist seulement 23 sont impacté par ce changement.
On peut en conclure que très peu de projets sont impactés.
