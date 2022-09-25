# Readonly properties

Les variables peuvent etre déclarées en lecture seule. Elle ne peuvent plus 
etre modifié après avoir été initialisé.

```php
class PostData {
    public function __construct(
        public readonly string $title,
        public readonly DateTimeImmutable $date,
    ) {}
}
```
