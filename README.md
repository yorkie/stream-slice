
slice-stream [![Build Status](https://travis-ci.org/yorkie/slice-stream.svg?branch=master)](https://travis-ci.org/yorkie/koa-range)
==========================
slice stream like buffer/string

### Installation

```sh
$ npm install slice-stream --save
```

### Usage

```js
var fs = require('fs');
var slice = require('slice-stream').slice;
fs.createReadStream('your path')
  .pipe(slice(10, 100))
  .on('data', function() {
    // here we only get the buffer from 10th to 100th.
  });
```

### License

MIT