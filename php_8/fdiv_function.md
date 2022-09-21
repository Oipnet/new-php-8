# New fdiv() function

Comme les function fmod() et intdiv() cette methode permet les divisions pas 0 et retourne INF, -INF ou NAN en fonction du cas.

```php
fdiv(1.0, 0.0); // INF
fdiv(-1.0, 0.0); // -INF
fdiv(0.0, 0.0); // NAN
```
