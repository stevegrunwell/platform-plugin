### The Plugin Class

```php
/**
 * Bootstrap the entire plugin.
 *
 * 1. Define any necessary constants
 * 2. Load all integrations
 * 3. Load WP-CLI commands
 */
public function bootstrap() {
    $this->defineConstants();
    $this->loadIntegrations();
    $this->loadCommands();
}
```

Note:

The `Plugin` class is the main plugin class, and its sole purpose is to set everything else in motion.

It has one public method, `bootstrap()`, which is responsible for loading all of the integrations, including running their `shouldLoadIntegration()` methods. It also defines constants and registers the WP-CLI commands.

We'll see this in action in just a second.
