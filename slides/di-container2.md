### DI Configuration

```php
# Nexcess\MAPPS\Container
public function getConfiguration() {
    return [
        Integrations\SomeIntegration::class => function ( $app ) {
            return new Integrations\SomeIntegration(
                $app->get( Settings::class ),
                $app->get( Services\SomeService::class )
            );
        },

        // ...
    ];
}
```

Note:

This is inside the Container class — we have a `getConfiguration()` method that returns a big array of classes mapped to closures that return instances.

Here, we're saying that in order to build `SomeIntegration`, we need the `Settings` instance as well as some service class.

The container then caches results, so we're only instantiating each of these objects once by default. Kind of like a Singleton, but way easier to work with and to test.
