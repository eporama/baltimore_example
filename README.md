# baltimore_example
A temporary repo for DrupalCon Baltimore

This branch "lightning" has a composer.json and composer.lock file that were from a vanilla install of [the Acquia lightning-project](https://github.com/acquia/lightning-project)

It also contains a .gitignore file that ignores everything in docroot and vendor, so that if you build locally, you do not commit these files to your github repo.

The docroot directory does include `sites/default/settings.php` and `sites/default/services.yml` files which are only present to allow the addition of the "Acquia require line"

```
require("/var/www/site-php/".$_ENV['AH_SITE_GROUP']."/".$_ENV['AH_SITE_GROUP']."-settings.inc");
```

This is a simplified settings file that will allow the site to be deployed on Acquia hosting.
