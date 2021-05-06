### WP-CLI commands

* <!-- .element: class="fragment" -->A series of custom WP-CLI commands
* <!-- .element: class="fragment" -->Application-level setup work, support tools

Note:

The plugin also includes a number of custom WP-CLI commands, which are available to everyone but tend to be more for internal use.

Example: when a new site is provisioned, the last step is calling our setup command to pre-configure sites — default permalink structures, pre-install bundled premium plugins, enable caching, etc.

Also includes commands to help our support team — flushing all caches, clean up after migrations from other hosts, or even create self-destructing, temporary support users.
