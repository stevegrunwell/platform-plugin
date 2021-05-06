### Progressive enhancement

Build for the masses, enhance where you can

Note:

First, it's important to embrace the idea of progressive enhancement.

The general idea is to build a solid baseline, something that will work in as many places as you find reasonable; then, as their configuration or environment allows, start adding or improving features. That's the whole point of `shouldLoadIntegration()` in integrations — remove it if we have any reason not to load it.

Instead of backporting features to old versions of WordPress, check to see if they support the feature and, if so, *then* load it, e.g. if some feature wasn't available until WordPress 5.4 and the customer's still running 5.2, they just don't get that feature.
