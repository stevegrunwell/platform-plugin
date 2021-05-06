### Autoloading

<pre class="fragment-replacement hljs lang-php"><code class="fragment fade-out" data-fragment-index="0"># The old way
require_once __DIR__ . '/src/SomeClass.php';
require_once __DIR__ . '/src/SomeOtherClass.php';
require_once __DIR__ . '/src/SomeThirdClass.php';

new SomeClass();
new SomeOtherClass();
new SomeThirdClass();</code><code class="fragment fade-in" data-fragment-index="0"># Modern autoloading
require_once __DIR__ . '/vendor/autoload.php';

new SomeClass();      # src/SomeClass.php
new SomeOtherClass(); # src/SomeOtherClass.php
new SomeThirdClass(); # src/SomeThirdClass.php</code></pre>

Note:

With our Composer-generated autoloader, we can replace all of those require_once statements with a single call to the autoloader, and PHP will handle everything else from there!
