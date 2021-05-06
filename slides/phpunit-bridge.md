### PHPUnit Bridge

Run a test suite across multiple versions of PHPUnit

Note:

One pain point we ran into early on was testing across multiple versions of PHP

* Didn't want to abandon customers who are still running dead versions of PHP (since we haven't forced them to upgrade yet)
* Didn't want to live forever in dead versions of PHPUnit, either

PHPUnit Bridge lets us run the latest version of PHPUnit based on PHP version.

Hacked the core test suite a bit to get it running on PHP 8.x, so now we're running the test suite on PHP 5.6, all versions of 7.x, and PHP 8
