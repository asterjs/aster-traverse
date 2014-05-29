# aster-traverse
[![NPM version][npm-image]][npm-url]
[![Build Status][travis-image]][travis-url]

> Traverse with aster.

## Usage

First, install `aster-traverse` as a development dependency:

```shell
npm install --save-dev aster-traverse
```

Then, add it to your build script:

```javascript
var aster = require('aster');
var traverse = require('aster-traverse');

aster.src('src/**/*.js')
.map(traverse({
  stringOption: 'value'
}))
.map(aster.dest('dist'))
.concatAll()
.subscribe(
  function (file) { console.log('%s processed successfully.', file.loc.source) },
  function (err) { console.error('Error: %s', err) }
);
```

## API

### traverse(options)

#### options.stringOption
Type: `String`

Some string option.

## License

[MIT License](http://en.wikipedia.org/wiki/MIT_License)

[npm-url]: https://npmjs.org/package/aster-traverse
[npm-image]: https://badge.fury.io/js/aster-traverse.png

[travis-url]: http://travis-ci.org/asterjs/aster-traverse
[travis-image]: https://secure.travis-ci.org/asterjs/aster-traverse.png?branch=master
