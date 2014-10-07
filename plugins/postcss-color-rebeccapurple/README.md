# postcss-color-rebeccapurple [![Build Status](https://travis-ci.org/postcss/postcss-color-rebeccapurple.png)](https://travis-ci.org/postcss/postcss-color-rebeccapurple)

> [PostCSS](https://github.com/postcss/postcss) plugin to transform [W3C CSS `rebeccapurple` color](http://dev.w3.org/csswg/css-color/#valuedef-color-rebeccapurple) to more compatible CSS (rgb()).

_[Why this plugin ?](http://meyerweb.com/eric/thoughts/2014/06/19/rebeccapurple/)_

## Installation

```bash
$ npm install postcss-color-rebeccapurple
```

## Usage

```js
// dependencies
var fs = require("fs")
var postcss = require("postcss")
var colorRebeccapurple = require("postcss-color-rebeccapurple")

// css to be processed
var css = fs.readFileSync("input.css", "utf8")

// process css
var output = postcss()
  .use(colorRebeccapurple())
  .process(css)
  .css
```

Using this `input.css`:

```css
body {
  color: rebeccapurple
}

```

you will get:

```css
body {
  color: rgb(102, 51, 153);
}
```

Checkout [tests](test) for more examples.

---

## Contributing

Work on a branch, install dev-dependencies, respect coding style & run tests before submitting a bug fix or a feature.

    $ git clone https://github.com/postcss/postcss-color-rebeccapurple.git
    $ git checkout -b patch-1
    $ npm install
    $ npm test

## [Changelog](CHANGELOG.md)

## [License](LICENSE)