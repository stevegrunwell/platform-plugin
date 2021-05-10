# Considerations & Concerns for Platform Plugin Development

One of the major strengths of WordPress is the ability to develop small plugins to solve particular needs. Whether you want to re-arrange menus or add a new dashboard widget, WordPress gives you the tools to make small, focused plugins to customize nearly anything.

This paradigm changes when your code is running across tens of thousands of customer sites, however. Suddenly, you have to coordinate which features are active based on the site. Is this a WooCommerce site? Does this feature exist in this version of WordPress? Has the site owner already installed another plugin to handle this piece of functionality?

In this session, we'll be taking a deep dive into the architecture, development decisions, and release process behind the "Must-Use" (MU) plugin that runs on every WordPress site across [the Nexcess Managed Applications platform](https://www.nexcess.net/wordpress). Attendees will learn about the practice and challenges of building a WordPress plugin at-scale, as well as how to better handle conflicts in their own plugins of any size.

:sparkles: **[View slides](http://stevegrunwell.github.io/platform-plugin)** :sparkles:


## Presentation History

* [WordCamp Northeast Ohio Region (NEO) 2021](https://neo.wordcamp.org/2021/)


## Resources

The following resources expand upon some of the topics we could barely touch upon in this talk.


### PHP Namespaces and Autoloading

* [A Crash-course in PHP Namespaces for WordPress Developers](https://stevegrunwell.com/blog/php-namespaces-wordpress/)
    * Alternatively, you may prefer [the slides for the talk of the same name](https://stevegrunwell.com/slides/php-namespaces)
* [PHP Manual entry on Autoloading](https://www.php.net/manual/en/language.oop5.autoload.php)
* [PSR-4: Autoloader](https://www.php-fig.org/psr/psr-4/) — Official specification for PSR-4
* [Composer autoloader reference](https://getcomposer.org/doc/04-schema.md#autoload)


### Dependency Injection

* [Dependency Injection in PHP](https://codeinphp.github.io/post/dependency-injection-in-php/) — A great introduction to dependency injection in PHP by @sarfraznawaz2005
* [PSR-11: Container Interface](https://www.php-fig.org/psr/psr-11/) — Official specification for PSR-11
* [Dependency Injection v Service Location](https://www.php-fig.org/psr/psr-11/meta/#4-recommended-usage-container-psr-and-the-service-locator) — Explains the differences between actual Dependency Injection and the Service Locater pattern


### Testing and Software Quality

* [Writing WP-CLI Commands That Work!](https://stevegrunwell.com/slides/wp-cli)
* [Confidently Testing WordPress](https://stevegrunwell.com/slides/testing-wordpress)
* [Build and Release Confidently with Continuous Integration and Delivery](https://stevegrunwell.com/slides/intro-to-ci-cd)
* [Code Review: For Me & You](https://stevegrunwell.com/slides/code-review)
* [Performance Optimisation: How do I go about it?](https://www.youtube.com/watch?v=hOajLLej68Y) — Excellent introduction to performance optimization by @katzien ([slides](https://github.com/katzien/talks/blob/master/performance-optimisation/laraconeu-2019-08-30/slides.pdf))


#### Referenced tools and libraries

* [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) — Coding standards
* [PHP Compatibility](https://github.com/PHPCompatibility/PHPCompatibility) — PHP_CodeSniffer ruleset for checking compatibility across PHP versions
* [cweagans/composer-patches](https://github.com/cweagans/composer-patches) — Composer plugin for patching Composer dependencies
* [PHP Coding Standards Fixer](https://github.com/FriendsOfPhp/PHP-CS-Fixer) — Alternative coding standards checker for PHP
* [PHPStan](https://phpstan.org/) — Static code analysis
* [WordPress extensions for PHPStan](https://github.com/szepeviktor/phpstan-wordpress) by @szepeviktor
* [Symfony's PHPUnit Bridge component](https://symfony.com/doc/current/components/phpunit_bridge.html) — Run your test suite across multiple versions of PHPUnit
    * [Details on how we get the WordPress Core Test Suite working with PHPUnit 8+](https://gist.github.com/stevegrunwell/1876f7a35a2be88e80faea297cc29f94)


### Misc

* [Interworx](https://www.interworx.com/) — Hosting software used to expose environment details to the MU plugin
* [Currently supported versions of PHP](https://www.php.net/supported-versions.php)
* [What Is Garbage Collection in PHP And How Do You Make The Most Of It?](https://tideways.com/profiler/blog/what-is-garbage-collection-in-php-and-how-do-you-make-the-most-of-it)
