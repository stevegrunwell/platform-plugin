### Welcome to CI/CD!

* <!-- .element: class="fragment" --> Automatically build the plugin, run tests on push
* <!-- .element: class="fragment" --> Multiple versions of PHP, WordPress
* <!-- .element: class="fragment" --> Additional tests, production build for releases

Note:

Continuous Integration and Delivery, or CI/CD, is a process that automatically runs all of these tests every time we push to GitHub.
* if computers are good at one thing, it's taking a set of instructions and following them over and over again.

Every time we push, our pipeline builds the plugin and runs all of our tests. As a result, we get consistent builds and know that our tests will always be run under the same conditions, in the same order, with no "whoops, I forgot to test". It's testing across multiple combinations of PHP and WordPress, and I don't have to lift a finger.

When we're preparing a release, the pipeline also calls that build script to generate the optimized, production-ready zip file, but *only* after checking that dependencies are up-to-date and other pre-flight checks.

It runs the same way every time and — if we encounter an issue — we make sure a check is added so that issue doesn't happen again.
