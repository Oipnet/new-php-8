# Fibers

Fibers sont un mécanisme de bas niveau afin de gérer le parallelisme

Peut de chance qu'il soit utilisé dans les projets, mais très utilisé 
par des frameworks tel que Amphp ou ReactPHP

## Exemple
```php
$fiber = new Fiber(function (): void {
    $valueAfterResuming = Fiber::suspend('after suspending');
    
    // … 
});
 
$valueAfterSuspending = $fiber->start();
 
$fiber->resume('after resuming');
```
