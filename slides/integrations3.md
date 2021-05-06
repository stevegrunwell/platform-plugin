### Integrations

```php
/**
 * Perform any necessary setup for the integration.
 *
 * This method is the entry-point for all integrations.
 */
public function setup() {
    // Add hooks
    // Load bundled dependencies
}
```

Note:

Assuming `shouldLoadIntegration()` returns true, the next step is the integrations' `setup()` method, which is how we actually hook in the integration.

This is usually registering actions and filters, but some integrations also need to load plugins that we bundle with the MU plugin or otherwise start up different service classes.
