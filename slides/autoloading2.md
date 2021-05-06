### Autoloading

```js
// composer.json
{
    // ...

    "autoload": {
        "psr-4": {
            "MyCompany\\MyPlugin\\": "src/"
        }
    }
}
```

Namespaces <u>must</u> mirror the directory structure!

Note:

The standard autoloading pattern these days is PSR-4, where the filenames match the class names and namespace structure, so "MyCompany\MyPlugin\SomeClass" maps to "src/SomeClass.php", because we've told it to look in the src directory for the MyCompany\MyPlugin namespace.
