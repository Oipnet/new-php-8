# Create DateTime objects from interface

Afin de créer un DateTime depuis un DateTimeImmutable il était possible de faire
```php
DateTime::createFromImmutable($immutableDateTime)
```

Il a été ajouté la methode createFromInterface aux classes DateTime et DateTimeImmutable
```php
DateTime::createFromInterface(DateTimeInterface $other);

DateTimeImmutable::createFromInterface(DateTimeInterface $other);
```
