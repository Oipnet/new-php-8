# Interal method return types

Lorsque l'on étend des classes standard (Ex: Datetime) sans préciser le type de retour des fonctions surchargé
une notice de deprecation a été rajouté.

Il suffit de rajouter le type de retour afin de ne plus avoir cette notice.

```php
class MyDateTime extends DateTime
{
    public function modify(string $modifier): DateTime|false 
    { 
        return false; 
    }
}
```

Il est aussi possible d'ajouter l'attribut ReturnTypeWillChange qui corrige le problème jusqu'à PHP 9
```php
class MyDateTime extends DateTime
{
    /**
     * @return DateTime|false
     */
    #[ReturnTypeWillChange]
    public function modify(string $modifier) 
    { 
        return false; 
    }
}
```
