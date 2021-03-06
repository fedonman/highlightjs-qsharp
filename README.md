# Q# syntax support for [highlight.js](https://highlightjs.org/)

[![NPM](https://nodei.co/npm/highlightjs-qsharp.png)](https://npmjs.org/package/highlightjs-qsharp)

This repository provides syntax highlighting for Microsoft's Q# language using highlight.js

## Usage

Simply include the Highlight.js library in your webpage or Node app, then load this module.

### Static website or simple usage

Simply load the module after loading highlight.js. You'll use the minified version found in the `dist` directory. This module is just a CDN build of the language, so it will register itself as the Javascript is loaded.

```html
<script type="text/javascript" src="/path/to/highlight.min.js"></script>
<script type="text/javascript" src="/path/to/highlightjs-qsharp/dist/qsharp.min.js"></script>
<script type="text/javascript"> hljs.initHighlightingOnLoad(); </script>
```

This will find and highlight code inside of `<pre><code>` tags; it tries to detect the language automatically. If automatic detection doesn’t work for you, you can specify the language in the `class` attribute:

```html
<pre>
    <code class="qsharp">
    ...
    </code>
</pre>
```

### Using directly from the UNPKG CDN

```html
<script type="text/javascript" src="https://unpkg.com/highlightjs-qsharp/dist/qsharp.min.js"></script>
```

- More info: <https://unpkg.com>

### With Node or another build system

If you're using Node / Webpack / Rollup / Browserify, etc, simply require the language module, then register it with Highlight.js.

```javascript
var hljs = require('highlightjs');
var hljsQsharp = require('highlightjs-qsharp');

hljs.registerLanguage("qsharp", hljsQsharp);
hljs.initHighlightingOnLoad();
```

## License

hightlightjs-qsharp is released under the MIT License. See [LICENSE][1] file for details.

## Author

Vyron Vasileiadis <hi@fedonman.com>

## Links

- The official site for the Highlight.js library is <https://highlightjs.org/>.
- The Highlight.js GitHub project: <https://github.com/highlightjs/highlight.js>
- Learn more about Q#: <https://docs.microsoft.com/en-us/azure/quantum/user-guide/>

[1]: https://github.com/fedonman/highlightjs-qsharp/blob/master/LICENSE
