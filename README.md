[![Latest Stable Version](https://poser.pugx.org/jonnitto/sitemap/v/stable)](https://packagist.org/packages/jonnitto/sitemap)
[![Total Downloads](https://poser.pugx.org/jonnitto/sitemap/downloads)](https://packagist.org/packages/jonnitto/sitemap)
[![License](https://poser.pugx.org/jonnitto/sitemap/license)](LICENSE)
[![GitHub forks](https://img.shields.io/github/forks/jonnitto/Jonnitto.Sitemap.svg?style=social&label=Fork)](https://github.com/jonnitto/Jonnitto.Sitemap/fork)
[![GitHub stars](https://img.shields.io/github/stars/jonnitto/Jonnitto.Sitemap.svg?style=social&label=Stars)](https://github.com/jonnitto/Jonnitto.Sitemap/stargazers)
[![GitHub watchers](https://img.shields.io/github/watchers/jonnitto/Jonnitto.Sitemap.svg?style=social&label=Watch)](https://github.com/jonnitto/Jonnitto.Sitemap/subscription)
[![GitHub followers](https://img.shields.io/github/followers/jonnitto.svg?style=social&label=Follow)](https://github.com/jonnitto/followers)
[![Follow Jon on Twitter](https://img.shields.io/twitter/follow/jonnitto.svg?style=social&label=Follow)](https://twitter.com/jonnitto)

# Jonnitto.Sitemap

XML-Sitemap for [Neos CMS](https://www.neos.io) with some improvements:

* The property `metaRobotsNoindex` get observed.
* Template-Less approach: Everything is done in Fusion
* With the NodeType Mixin `Jonnitto.Sitemap:RemoveFromSitemap` you can easily set which document node should not show up in the `sitemap.xml`. `Neos.Neos:Shortcut` is already done like that.
* Add `robots.txt` with automatic sitemap entries. Works also great in multi-site environments

**Important**  
To activate the automatic `robots.txt` you have to delete the `robots.txt` inside the `/Web` folder. You also have to edit the `.htaccess`: Change the line `RewriteRule ^(_Resources/Packages/|robots\.txt|favicon\.ico) - [L]` to `RewriteRule ^(_Resources/Packages/|favicon\.ico) - [L]`.  
**If don't want to delete `robots.txt` after every update, you should add following lines to your `.htaccess`:**

```apache
# Use Neos robots.txt
RewriteCond %{REQUEST_URI} ^/robots\.txt
RewriteRule (.*) index.php [L]
```

If you only want to render a subset of the available language dimensions (e.g., if the content is not yet ready) you can configure this in the `Settings.yaml`:

```yaml
Jonnitto:
  Sitemap:
    robotsTxt:
      # Activate only English and German
      dimensionsPresets: ['en','de']
```

## Installation

Most of the time you have to make small adjustments to a package (e.g., a configuration in `Settings.yaml`). Because of that, it is important to add the corresponding package to the composer from your theme package. Mostly this is the site package located under Packages/Sites/. To install it correctly go to your theme package (e.g.Packages/Sites/Foo.Bar) and run following command:

```bash
composer require jonnitto/sitemap --no-update
```

The --no-update command prevent the automatic update of the dependencies. After the package was added to your theme `composer.json`, go back to the root of the Neos installation and run composer update. Et voilà! Your desired package is now installed correctly.

## License

Licensed under MIT, see [LICENSE](LICENSE)
