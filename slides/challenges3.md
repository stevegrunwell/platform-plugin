## Challenges

1. Every site is different
2. Not every customer gets every feature
3. We're pushing changes to <u>a lot</u> of sites 😬
4. We never want to be the bottleneck

Note:

Remember these?

The architecture of the plugin helps address some of these:

* We're using namespaces to prevent us from conflicting with other code (#1, #3)
* We can selectively activate integrations based on the environment, and destroy those we don't need (#2, #4)
* Autoloading and Dependency Injection make sure we're not loading a ton of unnecessary code (#4)
