# Hosting

The Ignite CMS can be hosted on any platform, including popular Drupal hosts like Acquia, Pantheon and Platform.sh.

### Pantheon.io configuration

To utilize Pantheon's integrated Composer for Drupal 10 you will need to add a few items from their managed Composer repository

### Steps

1. Clone [https://github.com/pantheon-upstreams/drupal-composer-managed](https://github.com/pantheon-upstreams/drupal-composer-managed) to your local machine.
2. Add 'pantheon' ignore rules from .gitignore to your project's .gitignore file.
3. Copy pantheon.upstream.yml to your root directory.
4. Add the '"upstream-configuration" repository to your composer.json
5. Require the "pantheon-upstreams/upstream-configuration" and "pantheon-systems/drupal-integrations" packages.
6. Add any lines with "upstream" or "pantheon" into your local composer.json.
7. Copy the "upstream-configuration" folder to your root directory.
8. Run composer update, resolve any conflicts.
9. Add a remote to the git repository URL provided in your Pantheon.io site dashboard.
10. Commit your changes and attempt to push to Pantheon with --force to override Pantheon's git history with your own git history (eg Github, Bitbucket, etc.).
11. If you do not receive any errors on the command line you can visit your Dashboard to see if it has pulled in your changes.
12. Run a manual installation or use terminus to install your Iginite profile.
