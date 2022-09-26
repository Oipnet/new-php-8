# Other small changes

 - MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH no longer has an effect
 - MYSQLI_STORE_RESULT_COPY_DATA no longer has an effect
 - PDO::ATTR_STRINGIFY_FETCHES now also works with booleans
 - Integers and floats in PDO MySQL and Sqlite result sets will be returned using native PHP types instead of strings when using emulated prepared statements
 - Functions like htmlspecialchars and htmlentities now also escape ' by default to &#039;; malformed UTF-8 will also be replaced with a unicode character, instead of resulting in an empty string
 - The hash, hash_file and hash_init have an extra argument added to them called $options, it has a default value of [] so it won't affect your code
 - New support for MurmurHash3 and xxHash
