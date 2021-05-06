### The Settings Class

* <!-- .element: class="fragment" --> Central point for conditional logic
* <!-- .element: class="fragment" --> Interpolate environment details

```php
if ( $settings->is_mwch_site ) {
    // Do something for Managed WooCommerce customers.
} elseif ( $settings->is_mapps_site ) {
    // Do something for non-WooCommerce MAPPS customers.
}
```
<!-- .element: class="fragment" -->


Note:

Acts as the brain of the plugin, and can be injected anywhere it might be necessary. This gives us a centralized location for things like production v staging site, the plan code, account ID, etc.

We're able to read raw environmental details from Interworx (part of our platform's infrastructure), then do some light processing to get these useful insights.
