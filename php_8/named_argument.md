# Named Argument

Afin de ne pas prendre en considération l'ordre des arguments il est possible de spécifié leur nom. 
Les paramètres optionnels peuvent etre omis

## Exemple

```
   function foo(string $a, string $b, ?string $c = null, ?string $d = null) {}
   
   foo(
    b: 'Valeur B'
    a: 'Valeur A'
    d: 'Valeur D'
   ); 
```
