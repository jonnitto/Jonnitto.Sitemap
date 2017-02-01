Jonnitto.Sitemap
================

[![Latest Stable Version](https://poser.pugx.org/jonnitto/sitemap/v/stable)](https://packagist.org/packages/jonnitto/sitemap)
[![Total Downloads](https://poser.pugx.org/jonnitto/sitemap/downloads)](https://packagist.org/packages/jonnitto/sitemap)
[![License](https://poser.pugx.org/jonnitto/sitemap/license)](https://packagist.org/packages/jonnitto/sitemap)

XML-Sitemap for [Neos CMS](https://www.neos.io) with some improvements:

* The property `metaRobotsNoindex` get observed.
* Template-Less approach: All is done in TypoScript
* With the NodeType Mixin `Jonnitto.Sitemap:RemoveFromSitemap` you can easily set which document node should not show up in the `sitemap.xml`. `Neos.Neos:Shortcut` is already done like that.


License
-------
The MIT License (MIT)

Copyright (c) 2017 Jon Uhlmann

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
