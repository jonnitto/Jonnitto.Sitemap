Jonnitto.Sitemap
================

[![Latest Stable Version](https://poser.pugx.org/jonnitto/sitemap/v/stable)](https://packagist.org/packages/jonnitto/sitemap)
[![Total Downloads](https://poser.pugx.org/jonnitto/sitemap/downloads)](https://packagist.org/packages/jonnitto/sitemap)
[![License](https://poser.pugx.org/jonnitto/sitemap/license)](https://packagist.org/packages/jonnitto/sitemap)

XML-Sitemap for [Neos CMS](https://www.neos.io) with some improvements:

* The property `metaRobotsNoindex` get observed.
* Template-Less approach: Everything is done in Fusion
* With the NodeType Mixin `Jonnitto.Sitemap:RemoveFromSitemap` you can easily set which document node should not show up in the `sitemap.xml`. `Neos.Neos:Shortcut` is already done like that.

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
