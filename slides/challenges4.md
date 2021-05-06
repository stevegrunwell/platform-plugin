## Challenges

1. Every site is different
2. Not every customer gets every feature
3. We're pushing changes to <u>a lot</u> of sites 😬
4. We never want to be the bottleneck

Note:

Looking back, we're handling differences between sites and toggling features based on the customer. We're using autoloading and the DI container to keep a small footprint, and we have a consistent way of building, _exhaustively_ testing, and deploying across all customer sites.

We've hit all of these at this point, but there's more we can do, especially around #1...
