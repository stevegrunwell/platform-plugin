### Class constructors

<pre class="fragment-replacement hljs lang-php"><code class="fragment fade-out" data-fragment-index="0">class SomeClass {

    /**
     * @var WP_Post
     */
    protected $post;

    public function __construct( WP_Post $post ) {
        $this->post = $post;

        $this->register_hooks();
    }
}</code><code class="fragment fade-in" data-fragment-index="0">class SomeClass {

    /**
     * @var WP_Post
     */
    protected $post;

    public function __construct( WP_Post $post ) {
        $this->post = $post;
    }
}</code></pre>

<pre class="fragment-replacement hljs lang-php"><code class="fragment fade-out" data-fragment-index="0">$instance = new SomeClass( $post );</code><code class="fragment fade-in" data-fragment-index="0">$instance = new SomeClass( $post );
$instance->register_hooks();</code></pre>

Note:

Really common pattern in WP plugins that will cause pain: treating class constructors like default methods.

In this example, any time an instance of SomeClass gets instantiated, it registers hooks. Multiple instances = multiple callbacks, which can lead to all sorts of issues.

Remember: in object-oriented programming, the constructor is meant to provide the instance with any dependencies, not as the default method call.

Much better: instantiate the class, then call the method. In our plugin class, that's the bootstrap method. In our integrations, it's the `setup()` method. Also makes the object compatible with DI container, since we're only bootstrapping the object when we mean to.
