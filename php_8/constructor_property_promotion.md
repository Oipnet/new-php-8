# Constructor Property Promotion

Cela permet de simplifier l'ecriture d'une classe et de ses attributs

## Avant PHP 8

```php
class Money 
{
    public Currency $currency;
 
    public int $amount;
 
    public function __construct(
        Currency $currency,
        int $amount,
    ) {
        $this->currency = $currency;
        $this->amount = $amount;
    }
}
```

## Après PHP 8

```php
class Money 
{
    public function __construct(
        public Currency $currency,
        public int $amount,
    ) {}
}
```
