Jonnitto.Sitemap
================

XML-Sitemap for [Neos CMS](https://www.neos.io) with some improvements:

* You can set which types of pages are included to get hashed links. In that way you can provide a sitemap who links also to a particular part of a page.  
* The property `metaRobotsNoindex` is also observed.  
* You can also set which kind of pages (like Shortcuts) get ignored.  

**Make sure to include the commented route in `Jonnitto.Sitemap/Configuration/Routes.yaml` before the TYPO3.Neos subroutes in your global ``/Configuration/Routes.yaml`.**


License
-------
The MIT License (MIT)

Copyright (c) 2016 Jon Uhlmann

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
