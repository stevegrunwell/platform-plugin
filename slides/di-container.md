### Dependency Injection

<pre class="fragment-replacement hljs lang-php"><code class="fragment fade-out" data-fragment-index="0">use Nexcess\MAPPS\Container;
use Nexcess\MAPPS\Integrations\SomeIntegration;
use Nexcess\MAPPS\Services\SomeOtherService;
use Nexcess\MAPPS\Services\SomeService;
use Nexcess\MAPPS\Settings.php;

$settings = new Settings();
$service1 = new SomeOtherService();
$service2 = new SomeService( $service, $service1 );
$instance = new SomeIntegration( $settings, $service2 );</code><code class="fragment fade-in" data-fragment-index="0">use Nexcess\MAPPS\Container;
use Nexcess\MAPPS\Integrations\SomeIntegration;

$container = new Container();
$instance  = $container->get( SomeIntegration::class );</code></pre>

<!-- .element: class="fragment" -->Does <u>not</u> use auto-wiring!

Note:

The DI container lets us define the dependencies for each integration, service, etc. and let the container recursively resolve them. This saves unnecessary instantiation of objects, which saves memory.

For example, instead of manually instantiating all of these objects, when we tell the container to get `SomeIntegration`, it will resolve any of that class' dependencies and give us a concrete instance of that class.

Note that we don't use any sort of auto-wiring, as that can impact performance; instead, we explicitly define everything in the container definition, which looks like this:
