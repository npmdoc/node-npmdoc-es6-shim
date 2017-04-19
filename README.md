# npmdoc-es6-shim

#### api documentation for  [es6-shim (v0.35.3)](https://github.com/paulmillr/es6-shim/)  [![npm package](https://img.shields.io/npm/v/npmdoc-es6-shim.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-es6-shim) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-es6-shim.svg)](https://travis-ci.org/npmdoc/node-npmdoc-es6-shim)

#### ECMAScript 6 (Harmony) compatibility shims for legacy JavaScript engines

[![NPM](https://nodei.co/npm/es6-shim.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/es6-shim)

- [https://npmdoc.github.io/node-npmdoc-es6-shim/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-es6-shim/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-es6-shim/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-es6-shim/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-es6-shim/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-es6-shim/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Paul Miller",
        "url": "http://paulmillr.com"
    },
    "bugs": {
        "url": "https://github.com/paulmillr/es6-shim/issues"
    },
    "dependencies": {},
    "description": "ECMAScript 6 (Harmony) compatibility shims for legacy JavaScript engines",
    "devDependencies": {
        "@ljharb/eslint-config": "^10.0.0",
        "chai": "^3.5.0",
        "es5-shim": "^4.5.9",
        "eslint": "^3.14.0",
        "evalmd": "^0.0.17",
        "grunt": "^0.4.5",
        "grunt-contrib-connect": "^1.0.2",
        "grunt-contrib-watch": "^1.0.0",
        "grunt-saucelabs": "^8.6.3",
        "jscs": "^3.0.7",
        "jshint": "^2.9.4",
        "mocha": "^3.2.0",
        "promises-aplus-tests": "^2.1.2",
        "promises-es6-tests": "^0.5.0",
        "uglify-js": "2.7.3"
    },
    "directories": {},
    "dist": {
        "shasum": "9bfb7363feffff87a6cdb6cd93e405ec3c4b6f26",
        "tarball": "https://registry.npmjs.org/es6-shim/-/es6-shim-0.35.3.tgz"
    },
    "gitHead": "129819173958a0da2b487e219425baf0ca6d1a99",
    "homepage": "https://github.com/paulmillr/es6-shim/",
    "keywords": [
        "ecmascript",
        "harmony",
        "es6",
        "shim",
        "promise",
        "promises",
        "setPrototypeOf",
        "map",
        "set",
        "__proto__"
    ],
    "license": "MIT",
    "main": "es6-shim",
    "maintainers": [
        {
            "name": "paulmillr"
        },
        {
            "name": "ljharb"
        }
    ],
    "name": "es6-shim",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/paulmillr/es6-shim.git"
    },
    "scripts": {
        "eslint": "npm run --silent eslint:shim && npm run --silent eslint:sham",
        "eslint:sham": "eslint es6-sham.js test-sham/*.js",
        "eslint:shim": "eslint es6-shim.js test/*.js test/*/*.js",
        "jscs": "npm run --silent jscs:shim && npm run --silent jscs:sham",
        "jscs:sham": "jscs es6-sham.js test-sham/*.js",
        "jscs:shim": "jscs es6-shim.js test/*.js test/*/*.js",
        "jshint": "npm run --silent jshint:shim && npm run --silent jshint:sham",
        "jshint:sham": "jshint es6-sham.js test-sham/*.js",
        "jshint:shim": "jshint es6-shim.js test/*.js test/*/*.js",
        "lint": "npm run --silent lint:shim && npm run --silent lint:sham",
        "lint:sham": "npm run --silent jshint:sham && npm run --silent jscs:sham && npm run --silent eslint:sham",
        "lint:shim": "npm run --silent jshint:shim && npm run --silent jscs:shim && npm run --silent eslint:shim",
        "minify": "npm run --silent minify:shim && npm run --silent minify:sham",
        "minify:sham": "uglifyjs es6-sham.js --keep-fnames --comments --source-map=es6-sham.map -m -b ascii_only=true,beautify=false > es6-sham.min.js",
        "minify:shim": "uglifyjs es6-shim.js --keep-fnames --comments --source-map=es6-shim.map -m -b ascii_only=true,beautify=false > es6-shim.min.js",
        "pretest": "npm run --silent lint && evalmd *.md",
        "sauce": "npm run --silent sauce-connect && grunt sauce",
        "sauce-connect": "curl -L https://gist.githubusercontent.com/henrikhodne/9322897/raw/sauce-connect.sh | bash && export TRAVIS_SAUCE_CONNECT=true",
        "test": "npm run --silent tests-only",
        "test:native": "NO_ES6_SHIM=1 npm run --silent tests-only",
        "test:sham": "mocha test-sham/*.js",
        "test:shim": "mocha test/*.js test/*/*.js",
        "tests-only": "npm run --silent test:shim && npm run --silent test:sham"
    },
    "testling": {
        "html": "testling.html",
        "browsers": [
            "iexplore/6.0..latest",
            "firefox/3.0..6.0",
            "firefox/10.0",
            "firefox/15.0..latest",
            "firefox/nightly",
            "chrome/4.0..10.0",
            "chrome/20.0..latest",
            "chrome/canary",
            "opera/10.0..latest",
            "opera/next",
            "safari/4.0..latest",
            "ipad/6.0..latest",
            "iphone/6.0..latest",
            "android-browser/4.2..latest"
        ]
    },
    "version": "0.35.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
