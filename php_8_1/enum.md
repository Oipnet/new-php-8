# Enum

Enum a été introduit en PHP 8.1

Il permet de représenter une collection de constante

```php
enum Status
{
    case DRAFT;
    case PUBLISHED;
    case ARCHIVED;
}
```

L'avantage principal de cette collection est qu'il peut etre typé

```php
class BlogPost {
    public function __construct(
        public Status $status
    ){}
}

$post = new BlogPost(Status::DRAFT)
```

Il est possible d'ajouter des méthodes à un Enum

```php
enum Status
{
    case DRAFT;
    case PUBLISHED;
    case ARCHIVED;
    
    public function color(): string
    {
        return match($this) 
        {
            Status::DRAFT => 'grey',   
            Status::PUBLISHED => 'green',   
            Status::ARCHIVED => 'red',   
        };
    }
}

$status = Status::ARCHIVED;

$status->color(); // 'red'
```

Un Enum peut également implementer une interface

```php
interface HasColor
{
    public function color(): string;
}

enum Status implements HasColor
{
    case DRAFT;
    case PUBLISHED;
    case ARCHIVED;
    
    public function color(): string { /* … */ }
}
```

Les valeurs d'un enum sont représenté par un objet 
interne. Il est possible de leur assigné des valeurs. Très
utile pour sérialiser en BDD

```php
enum Status: string
{
    case DRAFT = 'draft';
    case PUBLISHED = 'published';
    case ARCHIVED = 'archived';
}

$value = Status::PUBLISHED->value;
$status = Status::from('draft')

$status = Status::from('unknown'); // ValueError
$status = Status::tryFrom('unknown'); // null
```

Il est possible de lister les valeurs possible d'un Enum

```php
Status::cases();
/* [
    Status::DRAFT,
    Status::PUBLISHED,
    STATUS::ARCHIVED
 ] */
```

Les Enums etant des objets ils ne peuvent pas etre utilisé en tant que clés d'un tableau.

```php
$list = [
    Status::DRAFT => 'draft' // Erreur php
];
```

Une RFC a été proposée pour ce problème, mais n'est pas encore approuvée
