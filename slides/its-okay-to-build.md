### It's okay to have a build step

Separate <u>source</u> control from build artifacts

Note:

First, in front of all of WordCamp, I want to tell you that it's absolutely fine to have a build step.

A lot of WordPress developers seem to have this idea in their heads that the plugin as it exists in GitHub must be built and ready to go at any time. They commit third-party dependencies and compiled CSS + JS, which just makes reviews a pain and invites merge conflicts.

This is probably conflated by the plugin SVN repos, which are meant for distribution, **not** development.

Let me tell you: it's absolutely okay to have a build process for your plugin. We have one. WooCommerce has one. Jetpack has one. Heck, even WordPress core has been modernizing their build process...
