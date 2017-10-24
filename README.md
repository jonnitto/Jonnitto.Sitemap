Jonnitto.Sitemap
================

[![Latest Stable Version](https://poser.pugx.org/jonnitto/sitemap/v/stable)](https://packagist.org/packages/jonnitto/sitemap)
[![Total Downloads](https://poser.pugx.org/jonnitto/sitemap/downloads)](https://packagist.org/packages/jonnitto/sitemap)
[![License](https://poser.pugx.org/jonnitto/sitemap/license)](https://packagist.org/packages/jonnitto/sitemap)

XML-Sitemap for [Neos CMS](https://www.neos.io) with some improvements:

* The property `metaRobotsNoindex` get observed.
* Template-Less approach: Everything is done in Fusion
* With the NodeType Mixin `Jonnitto.Sitemap:RemoveFromSitemap` you can easily set which document node should not show up in the `sitemap.xml`. `Neos.Neos:Shortcut` is already done like that.
* Add `robots.txt` with automatic sitemap entries. Works also great in multi-site environments

**Important**  
To activate the automatic `robots.txt` you have to delete the `robots.txt` inside the `/Web` folder. You also have to edit the `.htaccess`: Change the line `RewriteRule ^(_Resources/Packages/|robots\.txt|favicon\.ico) - [L]` to `RewriteRule ^(_Resources/Packages/|favicon\.ico) - [L]`

If you only want to render a subset of the available language dimensions (e.g. if the filling is not yet ready) you can set this in the Settings.yaml:

```
Jonnitto:
  Sitemap:
    robotsTxt:
      # Activate only english and german
      dimensionsPresets: ['en','de']
```

Installation
------------
Most of the time you have to make small adjustments to a package (e.g. configuration in Settings.yaml). Because of that, it is important to add the corresponding package to the composer from your theme package. Mostly this is the site packages located under Packages/Sites/. To install it correctly go to your theme package (e.g.Packages/Sites/Foo.Bar) and run following command:

```
composer require jonnitto/sitemap --no-update
```

The --no-update command prevent the automatic update of the dependencies. After the package was added to your theme composer.json, go back to the root of the Neos installation and run composer update. Et voilà! Your desired package is now installed correctly.


License
-------

Licensed under MIT, see [LICENSE](LICENSE)
