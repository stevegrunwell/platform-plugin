### The bootstrap file

```php
namespace Nexcess\MAPPS;

try {
    require_once __DIR__ . '/nexcess-mapps/autoload.php';

    $plugin = ( new Container() )->get( Plugin::class );
    $plugin->bootstrap();
} catch ( \Exception $e ) {
    trigger_error( $e->getMessage(), E_USER_WARNING );
}
```


Note:

Because MU plugins don't get "activated" in the same way as regular plugins, we need to define a single entry point: wp-content/mu-plugins/nexcess-mapps.php.

Abbreviated version of the bootstrap file, with a few key things to note

First, we're wrapping the whole thing in a try/catch block, so if anything goes wrong we're not going to white-screen a site.

Next, we create our single instance of the container, and use it to resolve our Plugin class. What are its dependencies? It doesn't matter, the container has taken care of it!

Finally, we call the bootstrap method from earlier on the Plugin class, which kicks everything off.

Fully bootstrapped in like 3 lines!
