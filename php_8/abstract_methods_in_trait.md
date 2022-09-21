# Abstract methods in traits improvements

Lors de l'utilisation du mot clef abstract dans un trait la signature de la 
methode dans la class utilisant ce trait n'était pas vérifiée.

Le code suivant était valide.
```php
trait Test {
    abstract public function test(int $input): int;
}

class UsesTrait
{
    use Test;

    public function test($input)
    {
        return $input;
    }
}
```

Il faut dorénavant que la signature soit valide
```php
class UsesTrait
{
    use Test;

    public function test(int $input): int
    {
        return $input;
    }
}
```
