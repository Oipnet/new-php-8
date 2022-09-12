# Union types
Depuis php7 le typage a été ajouté.

L'une des faiblesse de ce dernier était de ne pas proposer la possibilité d'avoir différents type pour une variable.

Il est dorénavant possible de le faire
```
public function foo(Foo|Bar $input): int|float;
```

## Restrictions

1. void ne peux pas faire partie d'un "union type"
2. nullable union peut être écrit en utilisant |null ou la notition existante en php 7 ?
```
public function foo(Foo|null $foo): void;

public function bar(?Bar $bar): void;
```