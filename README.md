# Considerations & Concerns for Platform Plugin Development

One of the major strengths of WordPress is the ability to develop small plugins to solve particular needs. Whether you want to re-arrange menus or add a new dashboard widget, WordPress gives you the tools to make small, focused plugins to customize nearly anything.

This paradigm changes when your code is running across tens of thousands of customer sites, however. Suddenly, you have to coordinate which features are active based on the site. Is this a WooCommerce site? Does this feature exist in this version of WordPress? Has the site owner already installed another plugin to handle this piece of functionality?

In this session, we'll be taking a deep dive into the architecture, development decisions, and release process behind the "Must-Use" (MU) plugin that runs on every WordPress site across [the Nexcess Managed Applications platform](https://www.nexcess.net/wordpress). Attendees will learn about the practice and challenges of building a WordPress plugin at-scale, as well as how to better handle conflicts in their own plugins of any size.

:sparkles: **[View slides](http://stevegrunwell.github.io/platform-plugin)** :sparkles:


## Resources

The following resources expand upon some of the topics we could barely touch upon in this talk.


### PHP Namespaces and Autoloading

* [A Crash-course in PHP Namespaces for WordPress Developers](https://stevegrunwell.com/blog/php-namespaces-wordpress/) — alternately, you may prefer [the slides for the talk of the same name](https://stevegrunwell.com/slides/php-namespaces)
* Some autoloading reference


### Dependency Injection

* [Dependency Injection in PHP](https://codeinphp.github.io/post/dependency-injection-in-php/) — A great introduction to dependency injection in PHP by @sarfraznawaz2005
* [PSR-11: Container Interface](https://www.php-fig.org/psr/psr-11/) — Official specification for PSR-11
* [Dependency Injection v Service Location](https://www.php-fig.org/psr/psr-11/meta/#4-recommended-usage-container-psr-and-the-service-locator) — Explains the differences between actual Dependency Injection and the Service Locater pattern


### Testing and Software Quality

* [Confidently Testing WordPress](https://stevegrunwell.com/slides/testing-wordpress)
* [Build and Release Confidently with Continuous Integration and Delivery](https://stevegrunwell.com/slides/intro-to-ci-cd)
* [Code Review: For Me & You](https://stevegrunwell.com/slides/code-review)
* [Performance Optimisation: How do I go about it?](https://www.youtube.com/watch?v=hOajLLej68Y) — Excellent introduction to performance optimization by @katzien ([slides](https://github.com/katzien/talks/blob/master/performance-optimisation/laraconeu-2019-08-30/slides.pdf))


#### Referenced libraries

* PHP CodeSniffer
* PHP Compatibility
* PHP Coding Standards Fixer
* PHPStan (WordPress-specific)
* [Symfony's PHPUnit Bridge component](https://symfony.com/doc/current/components/phpunit_bridge.html)


### Misc

* [Writing WP-CLI Commands That Work!](https://stevegrunwell.com/slides/wp-cli)


## Presentation History

* [WordCamp Northeast Ohio Region (NEO) 2021](https://neo.wordcamp.org/2021/)
