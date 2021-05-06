### Integrations

<pre class="fragment-replacement hljs lang-php"><code class="fragment fade-out" data-fragment-index="0">/**
 * Determine whether or not this integration should be loaded.
 *
 * @return bool
 */
public function shouldLoadIntegration() {
    return true;
}</code><span class="fragment fade-out" data-fragment-index="1"><code class="fragment fade-in php" data-fragment-index="0">/**
 * Determine whether or not this integration should be loaded.
 *
 * @return bool
 */
public function shouldLoadIntegration() {
    return $this->settings->is_staging_site;
}</code></span><span class="fragment fade-out php" data-fragment-index="2"><code class="fragment fade-in" data-fragment-index="1">/**
 * Determine whether or not this integration should be loaded.
 *
 * @return bool
 */
public function shouldLoadIntegration() {
    return $this->isPluginActive( 'jetpack/jetpack.php' )
        || $this->isPluginBeingActivated( 'jetpack/jetpack.php' );
}</code></span><code class="fragment fade-in" data-fragment-index="2">/**
 * Determine whether or not this integration should be loaded.
 *
 * @return bool
 */
public function shouldLoadIntegration() {
    return false; // Destroy this instance.
}</code></pre>

Note:

Every integration includes a `shouldLoadIntegration()` method, which is meant to decide "based on what I know, should this integration be loaded?"

Should this only be loaded on a staging site? Maybe the integration is only needed if Jetpack is active?

If this method returns false, we destroy the instance of the integration and don't do anything further.
