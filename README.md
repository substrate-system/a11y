# a11y
![tests](https://github.com/substrate-system/a11y/actions/workflows/nodejs.yml/badge.svg)
[![semantic versioning](https://img.shields.io/badge/semver-2.0.0-blue?logo=semver&style=flat-square)](https://semver.org/)
[![Common Changelog](https://nichoth.github.io/badge/common-changelog.svg)](./CHANGELOG.md)
[![dependencies](https://img.shields.io/badge/dependencies-zero-brightgreen.svg?style=flat-square)](package.json)
[![install size](https://flat.badgen.net/packagephobia/install/@substrate-system/a11y?cache-control=no-cache)](https://packagephobia.com/result?p=@substrate-system/a11y)
[![license](https://img.shields.io/badge/license-Polyform_Non_Commercial-26bc71?style=flat-square)](LICENSE)


Factoring out some common CSS utilities, so there is less duplication
across projects.

* [Accessible Icon Buttons](https://www.sarasoueidan.com/blog/accessible-icon-buttons/).
* [Inclusively Hidden](https://www.scottohara.me/blog/2017/04/14/inclusively-hidden.html)

**_featuring_**

The [`visually-hidden` class](#visually-hidden).

<details><summary><h2>Contents</h2></summary>

<!-- toc -->

- [install](#install)
- [Use](#use)
  * [example](#example)
  * [Import CSS](#import-css)
  * [Link](#link)
- [API](#api)
  * [`visually-hidden`](#visually-hidden)
- [see also](#see-also)

<!-- tocstop -->

</details>


## install

```sh
npm i -S @substrate-system/a11y
```

## Use
This package exposes CSS only.

### example
Put the relevant classes in your HTML.

```html
<button>
  <svg><!--  icon here  --></svg>
  <span class="visually-hidden">My Cool Button text</span>
</button>
```

### Import CSS
If using a bundler, import the package as normal.

```js
import '@substrate-system/a11y'
```

#### Import specific things

```js
import '@substrate-system/a11y/visually-hidden'
```

Or minified:
```js
import '@substrate-system/a11y/min'
```

### Link
If you don't want to use a bundler, this package exposes minified CSS files too.
You can copy them to a location that is accessible to your web server, then link
to them directly in HTML.

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

## API
This package exposes CSS that will look for the following classes.

### `visually-hidden`
Use this to create accessible buttons with no visible text.

See [this article](https://www.sarasoueidan.com/blog/accessible-icon-buttons/).

```html
<button class="${classes}">
    <svg><!--  icon here  --></svg>
    <span class="visually-hidden">Button text</span>
</button>
```

## see also

* [Accessible Icon Buttons ](https://www.sarasoueidan.com/blog/accessible-icon-buttons/)
* [Inclusively Hidden](https://www.scottohara.me/blog/2017/04/14/inclusively-hidden.html)
