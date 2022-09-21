# New get_resource_id() function

Une ressource est une variable spéciale qui permet de référencer une ressource externe (Ex : une connection MYSQL)

Par le passé le seul moyen de récupérer cet id était de fait un cast sur la ressource.
```php
$resourceId = (int) $resource;
```

PHP 8 introduit une nouvelle fonction get_resource_id()
```php
$resourceId = get_resource_id($resource);
```
