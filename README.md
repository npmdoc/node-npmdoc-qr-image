# api documentation for  [qr-image (v3.2.0)](https://github.com/alexeyten/qr-image)  [![npm package](https://img.shields.io/npm/v/npmdoc-qr-image.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-qr-image) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-qr-image.svg)](https://travis-ci.org/npmdoc/node-npmdoc-qr-image)
#### QR Code generator (png, svg, pdf, eps)

[![NPM](https://nodei.co/npm/qr-image.png?downloads=true)](https://www.npmjs.com/package/qr-image)

[![apidoc](https://npmdoc.github.io/node-npmdoc-qr-image/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-qr-image_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-qr-image/build..beta..travis-ci.org/apidoc.html)

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
            "name": "alexeyten",
            "email": "alexeyten@gmail.com"
        }
    ],
    "name": "qr-image",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
1.  object <span class="apidocSignatureSpan">qr-image.</span>png
1.  object <span class="apidocSignatureSpan">qr-image.</span>qr_base
1.  object <span class="apidocSignatureSpan">qr-image.</span>vector

#### [module qr-image.matrix](#apidoc.module.qr-image.matrix)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>calculatePenalty (matrix)](#apidoc.element.qr-image.matrix.calculatePenalty)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillAlignAndTiming (matrix)](#apidoc.element.qr-image.matrix.fillAlignAndTiming)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillData (matrix, data, mask)](#apidoc.element.qr-image.matrix.fillData)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillFinders (matrix)](#apidoc.element.qr-image.matrix.fillFinders)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillReserved (matrix, ec_level, mask)](#apidoc.element.qr-image.matrix.fillReserved)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillStub (matrix)](#apidoc.element.qr-image.matrix.fillStub)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>getMatrix (data)](#apidoc.element.qr-image.matrix.getMatrix)
1.  [function <span class="apidocSignatureSpan">qr-image.matrix.</span>init (version)](#apidoc.element.qr-image.matrix.init)

#### [module qr-image.png](#apidoc.module.qr-image.png)
1.  [function <span class="apidocSignatureSpan">qr-image.</span>png (bitmap, stream)](#apidoc.element.qr-image.png.png)
1.  [function <span class="apidocSignatureSpan">qr-image.png.</span>bitmap (matrix, size, margin)](#apidoc.element.qr-image.png.bitmap)

#### [module qr-image.qr_base](#apidoc.module.qr-image.qr_base)
1.  [function <span class="apidocSignatureSpan">qr-image.qr_base.</span>QR (text, ec_level, parse_url)](#apidoc.element.qr-image.qr_base.QR)
1.  [function <span class="apidocSignatureSpan">qr-image.qr_base.</span>fillTemplate (message, template)](#apidoc.element.qr-image.qr_base.fillTemplate)
1.  [function <span class="apidocSignatureSpan">qr-image.qr_base.</span>getTemplate (message, ec_level)](#apidoc.element.qr-image.qr_base.getTemplate)

#### [module qr-image.vector](#apidoc.module.qr-image.vector)
1.  [function <span class="apidocSignatureSpan">qr-image.vector.</span>eps (matrix, stream, margin)](#apidoc.element.qr-image.vector.eps)
1.  [function <span class="apidocSignatureSpan">qr-image.vector.</span>pdf (matrix, stream, margin)](#apidoc.element.qr-image.vector.pdf)
1.  [function <span class="apidocSignatureSpan">qr-image.vector.</span>svg (matrix, stream, margin, size)](#apidoc.element.qr-image.vector.svg)
1.  [function <span class="apidocSignatureSpan">qr-image.vector.</span>svg_object (matrix, margin)](#apidoc.element.qr-image.vector.svg_object)



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



# <a name="apidoc.module.qr-image.matrix"></a>[module qr-image.matrix](#apidoc.module.qr-image.matrix)

#### <a name="apidoc.element.qr-image.matrix.calculatePenalty"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>calculatePenalty (matrix)](#apidoc.element.qr-image.matrix.calculatePenalty)
- description and source-code
```javascript
function calculatePenalty(matrix) {
    var N = matrix.length;
    var penalty = 0;
    // Rule 1
    for (var i = 0; i < N; i++) {
        var pixel = matrix[i][0] & 1;
        var len = 1;
        for (var j = 1; j < N; j++) {
            var p = matrix[i][j] & 1;
            if (p == pixel) {
                len++;
                continue;
            }
            if (len >= 5) {
                penalty += len - 2;
            }
            pixel = p;
            len = 1;
        }
        if (len >= 5) {
            penalty += len - 2;
        }
    }
    for (var j = 0; j < N; j++) {
        var pixel = matrix[0][j] & 1;
        var len = 1;
        for (var i = 1; i < N; i++) {
            var p = matrix[i][j] & 1;
            if (p == pixel) {
                len++;
                continue;
            }
            if (len >= 5) {
                penalty += len - 2;
            }
            pixel = p;
            len = 1;
        }
        if (len >= 5) {
            penalty += len - 2;
        }
    }

    // Rule 2
    for (var i = 0; i < N - 1; i++) {
        for (var j = 0; j < N - 1; j++) {
            var s = matrix[i][j] + matrix[i][j + 1] + matrix[i + 1][j] + matrix[i + 1][j + 1] & 7;
            if (s == 0 || s == 4) {
                penalty += 3;
            }
        }
    }

    // Rule 3
    function I(k) { return matrix[i][j + k] & 1 };
    function J(k) { return matrix[i + k][j] & 1 };
    for (var i = 0; i < N; i++) {
        for (var j = 0; j < N; j++) {
            if (j < N - 6 && I(0) && !I(1) && I(2) && I(3) && I(4) && !I(5) && I(6)) {
                if (j >= 4 && !(I(-4) || I(-3) || I(-2) || I(-1))) {
                    penalty += 40;
                }
                if (j < N - 10 && !(I(7) || I(8) || I(9) || I(10))) {
                    penalty += 40;
                }
            }

            if (i < N - 6 && J(0) && !J(1) && J(2) && J(3) && J(4) && !J(5) && J(6)) {
                if (i >= 4 && !(J(-4) || J(-3) || J(-2) || J(-1))) {
                    penalty += 40;
                }
                if (i < N - 10 && !(J(7) || J(8) || J(9) || J(10))) {
                    penalty += 40;
                }
            }
        }
    }

    // Rule 4
    var numDark = 0;
    for (var i = 0; i < N; i++) {
        for (var j = 0; j < N; j++) {
            if (matrix[i][j] & 1) numDark++;
        }
    }
    penalty += 10 * Math.floor(Math.abs(10 - 20 * numDark/(N * N)));

    return penalty;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.matrix.fillAlignAndTiming"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillAlignAndTiming (matrix)](#apidoc.element.qr-image.matrix.fillAlignAndTiming)
- description and source-code
```javascript
function fillAlignAndTiming(matrix) {
    var N = matrix.length;
    if (N > 21) {
        var len = N - 13;
        var delta = Math.round(len / Math.ceil(len / 28));
        if (delta % 2) delta++;
        var res = [];
        for (var p = len + 6; p > 10; p -= delta) {
            res.unshift(p);
        }
        res.unshift(6);
        for (var i = 0; i < res.length; i++) {
            for (var j = 0; j < res.length; j++) {
                var x = res[i], y = res[j];
                if (matrix[x][y]) continue;
                for (var r = -2; r <=2 ; r++) {
                    for (var c = -2; c <=2 ; c++) {
                        var max = Math.max(r, c);
                        var min = Math.min(r, c);
                        var pixel = (max == 1 && min >= -1) || (min == -1 && max <= 1) ? 0x80 : 0x81;
                        matrix[x + r][y + c] = pixel;
                    }
                }
            }
        }
    }
    for (var i = 8; i < N - 8; i++) {
        matrix[6][i] = matrix[i][6] = i % 2 ? 0x80 : 0x81;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.matrix.fillData"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillData (matrix, data, mask)](#apidoc.element.qr-image.matrix.fillData)
- description and source-code
```javascript
function fillData(matrix, data, mask) {
    var N = matrix.length;
    var row, col, dir = -1;
    row = col = N - 1;
    var mask_fn = MASK_FUNCTIONS[mask];
    var len = data.blocks[data.blocks.length - 1].length;

    for (var i = 0; i < len; i++) {
        for (var b = 0; b < data.blocks.length; b++) {
            if (data.blocks[b].length <= i) continue;
            put(data.blocks[b][i]);
        }
    }

    len = data.ec_len;
    for (var i = 0; i < len; i++) {
        for (var b = 0; b < data.ec.length; b++) {
            put(data.ec[b][i]);
        }
    }

    if (col > -1) {
        do {
            matrix[row][col] = mask_fn(row, col) ? 1 : 0;
        } while (next());
    }

    function put(byte) {
        for (var mask = 0x80; mask; mask = mask >> 1) {
            var pixel = !!(mask & byte);
            if (mask_fn(row, col)) pixel = !pixel;
            matrix[row][col] = pixel ? 1 : 0;
            next();
        }
    }

    function next() {
        do {
            if ((col % 2) ^ (col < 6)) {
                if (dir < 0 && row == 0 || dir > 0 && row == N - 1) {
                    col--;
                    dir = -dir;
                } else {
                    col++;
                    row += dir;
                }
            } else {
                col--;
            }
            if (col == 6) {
                col--;
            }
            if (col < 0) {
                return false;
            }
        } while (matrix[row][col] & 0xf0);
        return true;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.matrix.fillFinders"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillFinders (matrix)](#apidoc.element.qr-image.matrix.fillFinders)
- description and source-code
```javascript
function fillFinders(matrix) {
    var N = matrix.length;
    for (var i = -3; i <= 3; i++) {
        for (var j = -3; j <= 3; j++) {
            var max = Math.max(i, j);
            var min = Math.min(i, j);
            var pixel = (max == 2 && min >= -2) || (min == -2 && max <= 2) ? 0x80 : 0x81;
            matrix[3 + i][3 + j] = pixel;
            matrix[3 + i][N - 4 + j] = pixel;
            matrix[N - 4 + i][3 + j] = pixel;
        }
    }
    for (var i = 0; i < 8; i++) {
        matrix[7][i] = matrix[i][7] =
        matrix[7][N - i - 1] = matrix[i][N - 8] =
        matrix[N - 8][i] = matrix[N - 1 - i][7] = 0x80;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.matrix.fillReserved"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillReserved (matrix, ec_level, mask)](#apidoc.element.qr-image.matrix.fillReserved)
- description and source-code
```javascript
function fillReserved(matrix, ec_level, mask) {
    var N = matrix.length;
    var format = FORMATS[EC_LEVELS[ec_level] << 3 | mask];
    function F(k) { return format >> k & 1 ? 0x81 : 0x80 };
    for (var i = 0; i < 8; i++) {
        matrix[8][N - 1 - i] = F(i);
        if (i < 6) matrix[i][8] = F(i);
    }
    for (var i = 8; i < 15; i++) {
        matrix[N - 15 + i][8] = F(i);
        if (i > 8) matrix[8][14 - i] = F(i);
    }
    matrix[7][8] = F(6);
    matrix[8][8] = F(7);
    matrix[8][7] = F(8);

    var version = VERSIONS[(N - 17)/4];
    if (!version) return;
    function V(k) { return version >> k & 1 ? 0x81 : 0x80 };
    for (var i = 0; i < 6; i++) {
        for (var j = 0; j < 3; j++) {
            matrix[N - 11 + j][i] = matrix[i][N - 11 + j] = V(i * 3 + j);
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.matrix.fillStub"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>fillStub (matrix)](#apidoc.element.qr-image.matrix.fillStub)
- description and source-code
```javascript
function fillStub(matrix) {
    var N = matrix.length;
    for (var i = 0; i < 8; i++) {
        if (i != 6) {
            matrix[8][i] = matrix[i][8] = 0x80;
        }
        matrix[8][N - 1 - i] = 0x80;
        matrix[N - 1 - i][8] = 0x80;
    }
    matrix[8][8] = 0x80;
    matrix[N - 8][8] = 0x81;

    if (N < 45) return;

    for (var i = N - 11; i < N - 8; i++) {
        for (var j = 0; j < 6; j++) {
            matrix[i][j] = matrix[j][i] = 0x80;
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.matrix.getMatrix"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>getMatrix (data)](#apidoc.element.qr-image.matrix.getMatrix)
- description and source-code
```javascript
function getMatrix(data) {
    var matrix = init(data.version);
    fillFinders(matrix);
    fillAlignAndTiming(matrix);
    fillStub(matrix);

    var penalty = Infinity;
    var bestMask = 0;
    for (var mask = 0; mask < 8; mask++) {
        fillData(matrix, data, mask);
        fillReserved(matrix, data.ec_level, mask);
        var p = calculatePenalty(matrix);
        if (p < penalty) {
            penalty = p;
            bestMask = mask;
        }
    }

    fillData(matrix, data, bestMask);
    fillReserved(matrix, data.ec_level, bestMask);

    return matrix.map(function(row) {
        return row.map(function(cell) {
            return cell & 1;
        });
    });
}
```
- example usage
```shell
...
}

// {{{1 All-in-one
function QR(text, ec_level, parse_url) {
ec_level = EC_LEVELS.indexOf(ec_level) > -1 ? ec_level : 'M';
var message = encode(text, parse_url);
var data = fillTemplate(message, getTemplate(message, ec_level));
return matrix.getMatrix(data);
}

// {{{1 export functions
module.exports = {
QR: QR,
getTemplate: getTemplate,
fillTemplate: fillTemplate,
...
```

#### <a name="apidoc.element.qr-image.matrix.init"></a>[function <span class="apidocSignatureSpan">qr-image.matrix.</span>init (version)](#apidoc.element.qr-image.matrix.init)
- description and source-code
```javascript
function init(version) {
    var N = version * 4 + 17;
    var matrix = [];
    var zeros = new Buffer(N);
    zeros.fill(0);
    zeros = [].slice.call(zeros);
    for (var i = 0; i < N; i++) {
        matrix[i] = zeros.slice();
    }
    return matrix;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.qr-image.png"></a>[module qr-image.png](#apidoc.module.qr-image.png)

#### <a name="apidoc.element.qr-image.png.png"></a>[function <span class="apidocSignatureSpan">qr-image.</span>png (bitmap, stream)](#apidoc.element.qr-image.png.png)
- description and source-code
```javascript
function png(bitmap, stream) {
    stream.push(PNG_HEAD);

    var IHDR = Buffer.concat([PNG_IHDR]);
    IHDR.writeUInt32BE(bitmap.size, 8);
    IHDR.writeUInt32BE(bitmap.size, 12);
    IHDR.writeUInt32BE(crc32(IHDR.slice(4, -4)), 21);
    stream.push(IHDR);

    var IDAT = Buffer.concat([
        PNG_IDAT,
        zlib.deflateSync(bitmap.data, { level: 9 }),
        new Buffer(4)
    ]);
    IDAT.writeUInt32BE(IDAT.length - 12, 0);
    IDAT.writeUInt32BE(crc32(IDAT.slice(4, -4)), IDAT.length - 4);
    stream.push(IDAT);

    stream.push(PNG_IEND);
    stream.push(null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.png.bitmap"></a>[function <span class="apidocSignatureSpan">qr-image.png.</span>bitmap (matrix, size, margin)](#apidoc.element.qr-image.png.bitmap)
- description and source-code
```javascript
function bitmap(matrix, size, margin) {
    var N = matrix.length;
    var X = (N + 2 * margin) * size;
    var data = new Buffer((X + 1) * X);
    data.fill(255);
    for (var i = 0; i < X; i++) {
        data[i * (X + 1)] = 0;
    }

    for (var i = 0; i < N; i++) {
        for (var j = 0; j < N; j++) {
            if (matrix[i][j]) {
                var offset = ((margin + i) * (X + 1) + (margin + j)) * size + 1;
                data.fill(0, offset, offset + size);
                for (var c = 1; c < size; c++) {
                    data.copy(data, offset + c * (X + 1), offset, offset + size);
                }
            }
        }
    }

    return {
        data: data,
        size: X
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.qr-image.qr_base"></a>[module qr-image.qr_base](#apidoc.module.qr-image.qr_base)

#### <a name="apidoc.element.qr-image.qr_base.QR"></a>[function <span class="apidocSignatureSpan">qr-image.qr_base.</span>QR (text, ec_level, parse_url)](#apidoc.element.qr-image.qr_base.QR)
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
n/a
```

#### <a name="apidoc.element.qr-image.qr_base.fillTemplate"></a>[function <span class="apidocSignatureSpan">qr-image.qr_base.</span>fillTemplate (message, template)](#apidoc.element.qr-image.qr_base.fillTemplate)
- description and source-code
```javascript
function fillTemplate(message, template) {
    var blocks = new Buffer(template.data_len);
    blocks.fill(0);

    if (template.version < 10) {
        message = message.data1;
    } else if (template.version < 27) {
        message = message.data10;
    } else {
        message = message.data27;
    }

    var len = message.length;

    for (var i = 0; i < len; i += 8) {
        var b = 0;
        for (var j = 0; j < 8; j++) {
            b = (b << 1) | (message[i + j] ? 1 : 0);
        }
        blocks[i / 8] = b;
    }

    var pad = 236;
    for (var i = Math.ceil((len + 4) / 8); i < blocks.length; i++) {
        blocks[i] = pad;
        pad = (pad == 236) ? 17 : 236;
    }

    var offset = 0;
    template.blocks = template.blocks.map(function(n) {
        var b = blocks.slice(offset, offset + n);
        offset += n;
        template.ec.push(calculateEC(b, template.ec_len));
        return b;
    });

    return template;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.qr_base.getTemplate"></a>[function <span class="apidocSignatureSpan">qr-image.qr_base.</span>getTemplate (message, ec_level)](#apidoc.element.qr-image.qr_base.getTemplate)
- description and source-code
```javascript
function getTemplate(message, ec_level) {
    var i = 1;
    var len;

    if (message.data1) {
        len = Math.ceil(message.data1.length / 8);
    } else {
        i = 10;
    }
    for (/* i */; i < 10; i++) {
        var version = versions[i][ec_level];
        if (version.data_len >= len) {
            return _deepCopy(version);
        }
    }

    if (message.data10) {
        len = Math.ceil(message.data10.length / 8);
    } else {
        i = 27;
    }
    for (/* i */; i < 27; i++) {
        var version = versions[i][ec_level];
        if (version.data_len >= len) {
            return _deepCopy(version);
        }
    }

    len = Math.ceil(message.data27.length / 8);
    for (/* i */; i < 41; i++) {
        var version = versions[i][ec_level];
        if (version.data_len >= len) {
            return _deepCopy(version);
        }
    }
    throw new Error("Too much data");
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.qr-image.vector"></a>[module qr-image.vector](#apidoc.module.qr-image.vector)

#### <a name="apidoc.element.qr-image.vector.eps"></a>[function <span class="apidocSignatureSpan">qr-image.vector.</span>eps (matrix, stream, margin)](#apidoc.element.qr-image.vector.eps)
- description and source-code
```javascript
function EPS(matrix, stream, margin) {
    var N = matrix.length;
    var scale = 9;
    var X = (N + 2 * margin) * scale;
    stream.push([
        '%!PS-Adobe-3.0 EPSF-3.0',
        '%%BoundingBox: 0 0 ' + X + ' ' + X,
        '/h { 0 rlineto } bind def',
        '/v { 0 exch neg rlineto } bind def',
        '/M { neg ' + (N + margin) + ' add moveto } bind def',
        '/z { closepath } bind def',
        scale + ' ' + scale + ' scale',
        ''
    ].join('\n'));

    matrix2path(matrix).forEach(function(subpath) {
        var res = '';
        for (var k = 0; k < subpath.length; k++) {
            var item = subpath[k];
            switch (item[0]) {
            case 'M':
                res += (item[1] + margin) + ' ' + item[2] + ' M ';
                break;
            default:
                res += item[1] + ' ' + item[0] + ' ';
            }
        }
        res += 'z\n';
        stream.push(res);
    });

    stream.push('fill\n%%EOF\n');
    stream.push(null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.vector.pdf"></a>[function <span class="apidocSignatureSpan">qr-image.vector.</span>pdf (matrix, stream, margin)](#apidoc.element.qr-image.vector.pdf)
- description and source-code
```javascript
function PDF(matrix, stream, margin) {
    // TODO deflate
    var N = matrix.length;
    var scale = 9;
    var X = (N + 2 * margin) * scale;
    var data = [
        '%PDF-1.0\n\n',
        '1 0 obj << /Type /Catalog /Pages 2 0 R >> endobj\n',
        '2 0 obj << /Type /Pages /Count 1 /Kids [ 3 0 R ] >> endobj\n',
    ];
    data.push('3 0 obj << /Type /Page /Parent 2 0 R /Resources <<>> ' +
        '/Contents 4 0 R /MediaBox [ 0 0 ' + X + ' ' + X + ' ] >> endobj\n');

    var path = scale + ' 0 0 ' + scale + ' 0 0 cm\n';
    path += matrix2path(matrix).map(function(subpath) {
        var res = '';
        var x, y;
        for (var k = 0; k < subpath.length; k++) {
            var item = subpath[k];
            switch (item[0]) {
            case 'M':
                x = item[1] + margin;
                y = N - item[2] + margin;
                res += x + ' ' + y + ' m ';
                break;
            case 'h':
                x += item[1];
                res += x + ' ' + y + ' l ';
                break;
            case 'v':
                y -= item[1];
                res += x + ' ' + y + ' l ';
                break;
            }
        }
        res += 'h';
        return res;
    }).join('\n');
    path += '\nf\n';
    data.push('4 0 obj << /Length ' + path.length + ' >> stream\n' +
        path + 'endstream\nendobj\n');

    var xref = 'xref\n0 5\n0000000000 65535 f \n';
    for (var i = 1, l = data[0].length; i < 5; i++) {
        xref += ('0000000000' + l).substr(-10) + ' 00000 n \n';
        l += data[i].length;
    }
    data.push(
        xref,
        'trailer << /Root 1 0 R /Size 5 >>\n',
        'startxref\n' + l + '\n%%EOF\n'
    );
    stream.push(data.join(''));
    stream.push(null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.vector.svg"></a>[function <span class="apidocSignatureSpan">qr-image.vector.</span>svg (matrix, stream, margin, size)](#apidoc.element.qr-image.vector.svg)
- description and source-code
```javascript
function SVG(matrix, stream, margin, size) {
    var X = matrix.length + 2 * margin;
    stream.push('<svg xmlns="http://www.w3.org/2000/svg" ');
    if (size > 0) {
        var XY = X * size;
        stream.push('width="' + XY + '" height="' + XY + '" ');
    }
    stream.push('viewBox="0 0 ' + X + ' ' + X + '">');
    stream.push('<path d="');
    pushSVGPath(matrix, stream, margin);
    stream.push('"/></svg>');
    stream.push(null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.qr-image.vector.svg_object"></a>[function <span class="apidocSignatureSpan">qr-image.vector.</span>svg_object (matrix, margin)](#apidoc.element.qr-image.vector.svg_object)
- description and source-code
```javascript
function SVG_object(matrix, margin) {
    var stream = [];
    pushSVGPath(matrix, stream, margin);

    var result = {
        size: matrix.length + 2 * margin,
        path: stream.filter(Boolean).join('')
    }

    return result;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
