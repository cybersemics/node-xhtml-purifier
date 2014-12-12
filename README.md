Javascript XHTML Purifier
=========================

Forked from the wonderful [javascript-xhtml-purifier](https://github.com/biilmann/javascript-xhtml-purifier)

This script provides a method to cleanup dirty html. It will take a string of dirty and badly formatted html, and return a pretty printed valid XHTML string.

Usage
-----

```javascript
require('xhtml-purifier').purify(html_string);
```

About the Implementation
------------------------

The purifying is based on section 8.2 in the [HTML5 specification](http://www.whatwg.org/specs/web-apps/current-work/#parsing), and implements a subset of the algorithm described there.

Only a limited set of the permitted HTML5 elements and attributes are permitted, and all other tags/attributes will simply be gone in the resulting XHTML.

Allowed elements
----------------

* strong (b and all headers will currently be transformed to strong)
* em
* blockquote
* ol
* ul
* li
* p
* pre
* a
* img
* br
* table
* caption
* col
* colgroup
* tbody
* td
* tfoot
* th
* thead
* tr

All other elements will be stripped from the resulting XHTML, although the inner text will be left intact.

The script was originally created for use with a Rich Text Editor for a CMS, and purposefully puts very firm limits on what can be included in the resulting XHTML. Since it is based on the HTML5 parsing specification it is very robust when it comes to cleaning up tag soup. 

License
-------

Copyright © 2014 [Charlie Stigler](http://charliestigler.com) with [Zaption](http://www.zaption.com) and released under the MIT license.

Based on javascript-html-purifier, which is copyright © 2008 [Mathias Biilmann Christensen](http://mathias-biilmann.net) / [Domestika INTERNET S.L.](http://domestika.com), released under the MIT license (see MIT-LICENSE)

Includes John Resig's and Erik Arvidsson's HTML Parser, which is used as a tokenizer.

HTML Parser By John Resig (ejohn.org)
Original code by Erik Arvidsson, Mozilla Public License
http://erik.eae.net/simplehtmlparser/simplehtmlparser.js
