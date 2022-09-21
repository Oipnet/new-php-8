# Mixed Type

Ce type permet de résoudre un problème, 
Certaines méthodes n'ont pas un retour déterminé. Il n'était pas possible alors de les typer simplement

Mixed regroupe les types suivants :
 - array
 - bool
 - callable
 - int
 - float
 - null
 - object
 - resource
 - string

Mixed peut être également utilisé pour typer un paramètre ou une propriété

Mixed incluant le type null il ne peut pas etre nullable
```php
function bar(): ?mixed {}
```
