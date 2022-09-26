# New fsync function

La fonction fsync permet de s'assurer que le fichier a bien été faite sur le filesystem

```php
$file = fopen("sample.txt", "w");

fwrite($file, "Some content");

if (fsync($file)) {
    echo "File has been successfully persisted to disk.";
}

fclose($file);
```
