[@zokugun/lang.color](https://github.com/ZokugunKS/lang.color)
==============================================================

[![kaoscript](https://img.shields.io/badge/language-kaoscript-orange.svg)](https://github.com/kaoscript/kaoscript)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![NPM Version](https://img.shields.io/npm/v/@zokugun/lang.color.svg?colorB=green)](https://www.npmjs.com/package/@zokugun/lang.color)
[![Dependency Status](https://badges.depfu.com/badges/000941dbceefbec0cdabd2e6215fc4aa/overview.svg)](https://depfu.com/github/zokugun/lang.color)
[![Build Status](https://travis-ci.org/ZokugunKS/lang.color.svg?branch=master)](https://travis-ci.org/ZokugunKS/lang.color)
[![CircleCI](https://circleci.com/gh/ZokugunKS/lang.color/tree/master.svg?style=shield)](https://circleci.com/gh/ZokugunKS/lang.color/tree/master)
[![Coverage Status](https://img.shields.io/coveralls/ZokugunKS/lang.color/master.svg)](https://coveralls.io/github/ZokugunKS/lang.color)

Provides a color class with the support of the RGB space with support of extensible spaces.

Getting Started
---------------

With [node](http://nodejs.org) previously installed:

	npm install @zokugun/lang.color

Use it with `JavaScript`:

```javascript
require('kaoscript/register');

const { Color, Space } = require('@zokugun/lang.color')();

const c = new Color('#ff0');
```

Use it with `kaoscript`:
```kaoscript
import '@zokugun/lang.color'

const c = new Color('#ff0')
```

Methods
-------

### Properties

A color is defined in a color space. If you try to access it into another space, the color will be automatically converted into the new space.

* `alpha()`: *Number*
* `alpha(Number)`: *Color*

#### srgb/rgb

* `red()`: *Number*
* `red(Number)`: *Color*
* `green()`: *Number*
* `green(Number)`: *Color*
* `blue()`: *Number*
* `blue(Number)`: *Color*

### Transformers

* `blend(Color, Number:percentage, String:space, Boolean:alpha)`: *Color*
* `clearer(Number)`: *Color*
* `opaquer(Number)`: *Color*
* `shade(Number)`: *Color*
* `tint(Number)`: *Color*
* `tone(Number)`: *Color*
* `greyscale(String:model)`: *Color*
* `negative()`: *Color*
* `scheme(Array<Function>)`: *Array&lt;Color>*
* `gradient(Color, Number)`: *Array&lt;Color>*

### Data

* `contrast()`
* `distance(Color)`: *Number*
* `luminance()`: *Number*
* `readable(Color)`: *Boolean*

### Formatters

* `format(String)`: *String*
* `hex()`: *String*

### Extends

* `Color.registerFormatter(String:format, Function)`
* `Color.registerParser(String:format, Function)`

### Macros

* `Color.registerSpace!(Object:space)`

ICC Profiles
------------

There no support for ICC profiles, yet.
So the rgb is the standard RGB of the web: sRGB.

Spaces
------

Spaces 										| Package
------ 										| -------
hsl, hsb/hsv, hsi, hwb						| [@zokugun/lang.color.alvy](https://github.com/ZokugunKS/lang.color.alvy)
CIELAB, CIELUV, CIELCh, CIEXYZ, CIEYxy		| [@zokugun/lang.color.cie](https://github.com/ZokugunKS/lang.color.cie)

Inspired by
-----------

* http://www.xarg.org/project/jquery-color-plugin-xcolor/
* https://github.com/brehaut/color-js
* https://github.com/LeaVerou/contrast-ratio

License
-------

[MIT](http://www.opensource.org/licenses/mit-license.php) &copy; Baptiste Augrain
