# api documentation for  [qr-image (v3.2.0)](https://github.com/alexeyten/qr-image)  [![npm package](https://img.shields.io/npm/v/npmdoc-qr-image.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-qr-image) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-qr-image.svg)](https://travis-ci.org/npmdoc/node-npmdoc-qr-image)
#### QR Code generator (png, svg, pdf, eps)

[![NPM](https://nodei.co/npm/qr-image.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/qr-image)

[![apidoc](https://npmdoc.github.io/node-npmdoc-qr-image/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-qr-image/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-qr-image/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-qr-image/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Alexey Ten",
        "url": "http://git.io/alexeyten"
    },
    "bugs": {
        "url": "https://github.com/alexeyten/qr-image/issues"
    },
    "dependencies": {},
    "description": "QR Code generator (png, svg, pdf, eps)",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "9fa8295beae50c4a149cf9f909a1db464a8672e8",
        "tarball": "https://registry.npmjs.org/qr-image/-/qr-image-3.2.0.tgz"
    },
    "files": [
        "lib",
        "LICENSE"
    ],
    "gitHead": "e184a78ee49cae71f88461bf90f4e23193857742",
    "homepage": "https://github.com/alexeyten/qr-image",
    "keywords": [
        "qrcode",
        "qr code",
        "qr",
        "png",
        "svg",
        "image"
    ],
    "license": "MIT",
    "main": "./lib/qr.js",
    "maintainers": [
        {
            "name": "alexeyten"
        }
    ],
    "name": "qr-image",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/alexeyten/qr-image.git"
    },
    "scripts": {
        "test": "./tests/test.js"
    },
    "version": "3.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module qr-image](#apidoc.module.qr-image)
1.  [function <span class="apidocSignatureSpan">qr-image.</span>image (text, options)](#apidoc.element.qr-image.image)
1.  [function <span class="apidocSignatureSpan">qr-image.</span>imageSync (text, options)](#apidoc.element.qr-image.imageSync)
1.  [function <span class="apidocSignatureSpan">qr-image.</span>matrix (text, ec_level, parse_url)](#apidoc.element.qr-image.matrix)
1.  [function <span class="apidocSignatureSpan">qr-image.</span>svgObject (text, options)](#apidoc.element.qr-image.svgObject)



# <a name="apidoc.module.qr-image"></a>[module qr-image](#apidoc.module.qr-image)

#### <a name="apidoc.element.qr-image.image"></a>[function <span class="apidocSignatureSpan">qr-image.</span>image (text, options)](#apidoc.element.qr-image.image)
- description and source-code
```javascript
function qr_image(text, options) {
    options = get_options(options);

    var matrix = QR(text, options.ec_level, options.parse_url);
    var stream = new Readable();
    stream._read = fn_noop;

    switch (options.type) {
    case 'svg':
    case 'pdf':
    case 'eps':
        process.nextTick(function() {
            vector[options.type](matrix, stream, options.margin, options.size);
        });
        break;
    case 'svgpath':
        // deprecated, use svg_object method
        process.nextTick(function() {
            var obj = vector.svg_object(matrix, options.margin, options.size);
            stream.push(obj.path);
            stream.push(null);
        });
        break;
    case 'png':
    default:
        process.nextTick(function() {
            var bitmap = png.bitmap(matrix, options.size, options.margin);
            if (options.customize) {
                options.customize(bitmap);
            }
            png.png(bitmap, stream);
        });
    }

    return stream;
}
```
- example usage
```shell
...
Usage
-----

Example:
'''javascript
var qr = require('qr-image');

var qr_svg = qr.image('I love QR!', { type: 'svg' });
qr_svg.pipe(require('fs').createWriteStream('i_love_qr.svg'));

var svg_string = qr.imageSync('I love QR!', { type: 'svg' });
'''

[More examples](./examples)
...
```

#### <a name="apidoc.element.qr-image.imageSync"></a>[function <span class="apidocSignatureSpan">qr-image.</span>imageSync (text, options)](#apidoc.element.qr-image.imageSync)
- description and source-code
```javascript
function qr_image_sync(text, options) {
    options = get_options(options);

    var matrix = QR(text, options.ec_level, options.parse_url);
    var stream = [];
    var result;

    switch (options.type) {
    case 'svg':
    case 'pdf':
    case 'eps':
        vector[options.type](matrix, stream, options.margin, options.size);
        result = stream.filter(Boolean).join('');
        break;
    case 'png':
    default:
        var bitmap = png.bitmap(matrix, options.size, options.margin);
        if (options.customize) {
            options.customize(bitmap);
        }
        png.png(bitmap, stream);
        result = Buffer.concat(stream.filter(Boolean));
    }

    return result;
}
```
- example usage
```shell
...
Example:
'''javascript
var qr = require('qr-image');

var qr_svg = qr.image('I love QR!', { type: 'svg' });
qr_svg.pipe(require('fs').createWriteStream('i_love_qr.svg'));

var svg_string = qr.imageSync('I love QR!', { type: 'svg' });
'''

[More examples](./examples)

'qr = require('qr-image')'

### Methods
...
```

#### <a name="apidoc.element.qr-image.matrix"></a>[function <span class="apidocSignatureSpan">qr-image.</span>matrix (text, ec_level, parse_url)](#apidoc.element.qr-image.matrix)
- description and source-code
```javascript
function QR(text, ec_level, parse_url) {
    ec_level = EC_LEVELS.indexOf(ec_level) > -1 ? ec_level : 'M';
    var message = encode(text, parse_url);
    var data = fillTemplate(message, getTemplate(message, ec_level));
    return matrix.getMatrix(data);
}
```
- example usage
```shell
...
'qr = require('qr-image')'

### Methods

* 'qr.image(text, [ec_level | options])' — Readable stream with image data;
* 'qr.imageSync(text, [ec_level | options])' — string with image data. (Buffer for 'png');
* 'qr.svgObject(text, [ec_level | options])' — object with SVG path and size;
* 'qr.matrix(text, [ec_level])' — 2D array.


### Options

* 'text' — text to encode;
* 'ec_level' — error correction level. One of 'L', 'M', 'Q', 'H'. Default 'M'.
* 'options' — image options object:
...
```

#### <a name="apidoc.element.qr-image.svgObject"></a>[function <span class="apidocSignatureSpan">qr-image.</span>svgObject (text, options)](#apidoc.element.qr-image.svgObject)
- description and source-code
```javascript
function svg_object(text, options) {
    options = get_options(options, 'svg');

    var matrix = QR(text, options.ec_level);
    return vector.svg_object(matrix, options.margin);
}
```
- example usage
```shell
...

'qr = require('qr-image')'

### Methods

* 'qr.image(text, [ec_level | options])' — Readable stream with image data;
* 'qr.imageSync(text, [ec_level | options])' — string with image data. (Buffer for 'png');
* 'qr.svgObject(text, [ec_level | options])' — object with SVG path and size;
* 'qr.matrix(text, [ec_level])' — 2D array.


### Options

* 'text' — text to encode;
* 'ec_level' — error correction level. One of 'L', 'M', 'Q', 'H'. Default 'M'.
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
