# New Stringable interface

L'interface Stringable peut etre utilisé pour typer tout objet qui implémente la methode __toString()

Dès qu'un objet implemente la methode __toString() il implémente automatique l'interface

```php
class Foo
{
    public function __toString(): string
    {
        return 'foo';
    }
}

function bar(string|Stringable $stringable) { /* … */ }

bar(new Foo());
bar('abc');
```
