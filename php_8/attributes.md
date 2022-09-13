# Attributes

Appelé annotation dans la pluspart des langages ils permettent d'ajouter des meta data à une class.

Ce concept n'est pas nouveau, nous utilisons depuis longtemp le bloc de phpdoc pour passer des meta data.

Les attributs PHP apporte 
 - un gain de performance
 - L'attribut etant mappé a une class est non une chaine de charactère cela reduit
une grosse source de bug
 - Les IDE comprennent mieux cette syntaxe

## Utilisation

```php
use Attributes\TestAttribute;

class Foo {
    #[TestAttribute('buzz')]
    public function bar() {}
}
```

```php
namespace Attributes;

class TestAttribute {
    public function __construct(
        public string $title
    ){}
}
```

```php
use Foo;
use Attributes\TestAttribute;

$reflexion = new ReflectionClass(Foo::class);
$barMethod = $reflexion->getMethod('bar');

$attributes = $barMethod->getAttributes(TestAttribute::class);
var_dump($attributes);
```
## Les différents types d'attributs

Les attributs peuvent être attachés à différents niveaux :
 - La class ou une class Anonyme
```php
#[ClassAttribute]
class MyClass { /* … */ }

$object = new #[ObjectAttribute] class () { /* … */ };
```
 - Une propriété ou constante
```php
#[PropertyAttribute]
public int $foo;

#[ConstAttribute]
public const BAR = 1;
```
 - Une methode
```php
#[MethodAttribute]
public function doSomething(): void { /* … */ }

#[FunctionAttribute]
function foo() { /* … */ }
```
 - Une closure
```php
$closure = #[ClosureAttribute] fn() => /* … */;
```
 - Une paramètre de fonction
```php
function foo(#[ArgumentAttribute] $bar) { /* … */ }
```

## Configuration des attributs

Par défaut l'attribut peut ajouté à n'importe quel place.

Nous pouvons spécifier le type d'attribut lors de la configuration de la classe

```php
#[Attribute(Attribute::TARGET_CLASS)]
class ClassAttribute
{
}
```

Les différents flags disponible
```php
Attribute::TARGET_CLASS
Attribute::TARGET_FUNCTION
Attribute::TARGET_METHOD
Attribute::TARGET_PROPERTY
Attribute::TARGET_CLASS_CONSTANT
Attribute::TARGET_PARAMETER
Attribute::TARGET_ALL
```

Les flags peuvent être combiné 
```php
#[Attribute(Attribute::TARGET_METHOD|Attribute::TARGET_FUNCTION)]
class ClassAttribute
{
}
```
