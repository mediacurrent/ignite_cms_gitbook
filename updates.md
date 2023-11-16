# Updates

### November 16, 2023

#### Rain Gin replaces by Ignite Gin

If you are using the rain\_gin package you can replace with the ignite\_gin package which includes CSS to clean up the Gin LB integration with Ignite.

#### Steps to migrate from rain\_gin to ignite\_gin

1. Remove rain\_gin from composer.json.
2. Require ignite\_gin in your project composer.
3. Remove "gin" component from your custom Ignite theme.
4. Enable the ignite\_gin module.
5. Clear caches.

