# lowly

[![Travis](https://img.shields.io/travis/thiamsantos/lowly.svg)](https://travis-ci.org/thiamsantos/lowly)
[![Coveralls](https://img.shields.io/coveralls/thiamsantos/lowly.svg)](https://coveralls.io/github/thiamsantos/lowly?branch=master)
[![npm (scoped)](https://img.shields.io/npm/v/lowly.svg)](https://www.npmjs.com/package/lowly)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)

> Build low quality images.

## Table of Contents
- [Install](#install)
- [Usage](#usage)
  - [CLI](#cli)
- [API](#api)
- [License](#license)

## Install
This project uses [node](http://nodejs.org) and [npm](https://npmjs.com). Go check them out if you don't have them locally installed.

```sh
$ npm install lowly
```

## Usage

```javascript
const fs = require('fs')
const lowly = require('lowly')

const image = fs.readFileSync('image.jpg')

lowly(image)
  .then(buff => {
    fs.writeFileSync('image-lowly.jpg', buff)
  })
```

### CLI

```
$ lowly --help

  Usage
      $ lowly <input>

  Examples
    $ lowly image.jpg
    $ lowly images/**/* image.jpg
```

## License
[MIT License](LICENSE.md) &copy; [Thiago Santos](https://thiamsantos.github.io/)
