## Client LCOV file parser

Simple LCOV file parser.

This project is fork from 'lcov-parser' and remove the fs dependency.

## Installation

    npm install lcov-parse


## Usage

    var parse = require('lcov-parse');

    parse('./path/to/file.info', function(err, data) {
        //process the data here
    });

or

    parse(lcovString, function(err, data) {
        //process the data here
    });

## Formatting

Using this as a guide: http://ltp.sourceforge.net/coverage/lcov/geninfo.1.php

It will return JSON like this:

```
 {
    "title": "Test #1",
    "file": "anim-base/anim-base-coverage.js",
    "functions": {
      "hit": 23,
      "found": 29,
      "details": [
        {
          "name": "(anonymous 1)",
          "line": 7,
          "hit": 6
        },
        {
          "name": "(anonymous 2)",
          "line": 620,
          "hit": 225
        },
        {
          "name": "_end",
          "line": 516,
          "hit": 228
        }
      ]
    }
    "lines": {
      "found": 181,
      "hit": 143,
      "details": [
        {
          "line": 7,
          "hit": 6
        },
        {
          "line": 29,
          "hit": 6
        }
      ]
    }
}
```

## Tests

    npm install && npm test

