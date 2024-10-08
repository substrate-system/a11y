# a11y
![tests](https://github.com/substrate-system/a11y/actions/workflows/nodejs.yml/badge.svg)
[![semantic versioning](https://img.shields.io/badge/semver-2.0.0-blue?logo=semver&style=flat-square)](https://semver.org/)
[![Common Changelog](https://nichoth.github.io/badge/common-changelog.svg)](./CHANGELOG.md)
[![dependencies](https://img.shields.io/badge/dependencies-zero-brightgreen.svg?style=flat-square)](package.json)
[![install size](https://packagephobia.com/badge?p=@substrate-system/a11y)](https://packagephobia.com/result?p=@substrate-system/a11y)
[![license](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)

Factoring out some common CSS utilities, so there is less duplication across projects.

<!-- toc -->

- [install](#install)
- [API](#api)
  * [`visually-hidden`](#visually-hidden)
- [Use](#use)
  * [Import CSS](#import-css)
  * [Minified CSS](#minified-css)

<!-- tocstop -->

## install

```sh
npm i -S @substrate-system/a11y
```

## API
This package looks for these classes:

### `visually-hidden`

Use this to create accessible buttons with no visible text.

See [this article](https://www.sarasoueidan.com/blog/accessible-icon-buttons/).

```html
<button class="${classes}">
    <svg><!--  icon here  --></svg>
    <span class="visually-hidden">Button text</span>
</button>
```

## Use

### Import CSS

```js
import '@substrate-system/a11y'
```

Or minified:
```js
import '@substrate-system/a11y/min'
```

### Minified CSS
This package exposes minified CSS files. You can copy them to a location that is
accessible to your web server, then link to them directly in HTML.

#### copy
```sh
cp ./node_modules/@substrate-system/a11y/dist/index.min.css ./public/a11y.css
```

#### HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="stylesheet" href="./a11y.css">
</head>
</html>
```
