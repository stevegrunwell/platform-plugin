<!-- .element: class="seamless" -->![High-level architecture of the Nexcess MAPPS MU plugin](resources/architecture.svg)

Note:

We'll talk through each of these, but at a high level this shows how they all connect. The green nexcess-mapps.php file is our bootstrap that lives in wp-content/mu-plugins and kicks everything off.

We're using an autoloader, so the bootstrap file loads that, then initializes our Dependency Injection container and uses it to resolve the main Plugin class, which sets up everything else — our integrations, WP-CLI commands, and things like our Settings class...
