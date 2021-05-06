### Test suite

* <!-- .element: class="fragment" --> Unit & integration tests
* <!-- .element: class="fragment" --> Coding standards
* <!-- .element: class="fragment" --> Compatibility checks
* <!-- .element: class="fragment" --> Static code analysis
* <!-- .element: class="fragment" --> Dependencies
* <!-- .element: class="fragment" --> Code review, Manual testing

Note:

So what kinds of tests do we run?

If you know me, you know I'm big on automated testing — at this point, we're hovering around 1k unit and integration tests using the WP core testing framework.

If you're new to testing, I highly recommend checking out my talk "Confidently Testing WordPress", which I've linked to in the README

* Coding standards — PHP_CodeSniffer and PHP Coding Standards Fixer
* Compatibility — everything we write needs to be compatible, but so does everything we bundle — actually have a method of patching vendor code if necessary
* Static code analysis (analyzing code without executing it)
* Dependencies: check that all bundled dependencies are up to date
* Code review: every change to the plugin gets reviewed by at least one other person
* Manual testing: roll up the sleeves and make sure the tests don't lie
