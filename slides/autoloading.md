### Autoloading

```php
# The old way
require_once __DIR__ . '/src/SomeClass.php';
require_once __DIR__ . '/src/SomeOtherClass.php';
require_once __DIR__ . '/src/SomeThirdClass.php';

new SomeClass();
new SomeOtherClass();
new SomeThirdClass();
```

Note:

If you noticed a severe lack of `require_once` statements, that wasn't for the sake of bevity. Instead of loading every plugin file into memory on every request, we can take advantage of autoloading.

Autoloader = tell PHP how to resolve class names to files, and when a request is made to an unrecognized class it will automatically load the file.

If you're using Composer, it can generate the autoloader for you automatically:
