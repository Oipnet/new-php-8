# Pure intersection types

Similaire à l'union type l'interserction type permet de verifier qu'un objet 
implémente les 2 interfaces.

```php
function generateSlug(HasTitle&HasId $post) {
    return strtolower($post->getTitle()) . $post->getId();
}
```
