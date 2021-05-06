### Integrations

* <!-- .element: class="fragment" --> A way to logically group related functionality
    - `ObjectCache`, `Cron`, `StagingSites`, etc.
* <!-- .element: class="fragment" --> Traits that can be applied as needed
    - `HasHooks`, `HasCronEvents`, etc.

Note:

The settings object is often injected into our integrations, which are the basic building block of the plugin — can think of them like Jetpack's extensions, but they're turned on and off based on the environment, the customer's plan, active plugins, etc.

We also have a number of PHP traits that we can apply to particular integrations if they require certain functionality.
