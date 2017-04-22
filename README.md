# npmtest-mocha-webpack

#### basic test coverage for  mocha-webpack (v0.7.0)  [![npm package](https://img.shields.io/npm/v/npmtest-mocha-webpack.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-mocha-webpack) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-mocha-webpack.svg)](https://travis-ci.org/npmtest/node-npmtest-mocha-webpack)

#### mocha cli with webpack support

[![NPM](https://nodei.co/npm/mocha-webpack.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mocha-webpack)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-mocha-webpack/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-mocha-webpack/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-mocha-webpack/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-mocha-webpack/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-mocha-webpack/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-mocha-webpack/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-mocha-webpack/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-mocha-webpack/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-mocha-webpack/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-mocha-webpack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-mocha-webpack/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-mocha-webpack/build/test-report.html](https://npmtest.github.io/node-npmtest-mocha-webpack/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-mocha-webpack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-mocha-webpack/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-mocha-webpack/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mocha-webpack/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mocha-webpack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mocha-webpack/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-mocha-webpack/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-mocha-webpack/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "mocha-webpack",
    "version": "0.7.0",
    "description": "mocha cli with webpack support",
    "bin": {
        "mocha-webpack": "./bin/mocha-webpack"
    },
    "files": [
        "*.md",
        "bin",
        "src",
        "lib"
    ],
    "scripts": {
        "clean-lib": "del-cli \"lib/**\" \"!lib\" \"!lib/reporters\" \"!lib/utils.js\" \"!lib/reporters/base.js\"",
        "clean-tmp": "del-cli \".tmp/**\"",
        "build": "npm run clean-lib && babel ./src -d lib",
        "lint": "node-version-gte-4 && eslint src test bin || echo Node version too old to run linting",
        "test": "npm run clean-tmp && npm run build && mocha --timeout 10000 --recursive --require test/setup.js \"test/**/*.test.js\"",
        "posttest": "npm run lint",
        "prepublish": "npm run build",
        "release": "np"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/zinserjan/mocha-webpack"
    },
    "bugs": {
        "url": "https://github.com/zinserjan/mocha-webpack/issues"
    },
    "keywords": [
        "webpack",
        "mocha"
    ],
    "author": "Jan-André Zinser",
    "license": "MIT",
    "peerDependencies": {
        "mocha": "^2.4.5 || ^3.0.0",
        "webpack": "^1.12.13 || ^2.1.0-beta.15"
    },
    "devDependencies": {
        "babel-cli": "^6.5.1",
        "babel-eslint": "^6.1.2",
        "babel-plugin-transform-class-properties": "^6.5.2",
        "babel-preset-es2015": "^6.5.0",
        "babel-register": "^6.5.2",
        "chai": "^3.5.0",
        "coffee-script": "^1.11.1",
        "del": "^2.2.0",
        "del-cli": "^0.2.0",
        "eslint": "^3.1.0",
        "eslint-config-airbnb-base": "^4.0.2",
        "eslint-plugin-import": "^1.11.0",
        "mocha": "^3.0.0",
        "node-version-check": "^2.1.1",
        "np": "^2.9.0",
        "sinon": "^1.17.3",
        "webpack": "^1.12.13"
    },
    "dependencies": {
        "anymatch": "^1.3.0",
        "fs-extra": "^0.30.0",
        "glob-parent": "^2.0.0",
        "interpret": "^1.0.1",
        "invariant": "^2.2.0",
        "is-glob": "^2.0.1",
        "loader-utils": "^0.2.13",
        "lodash": "^4.3.0",
        "normalize-path": "^2.0.1",
        "object-hash": "^1.1.2",
        "webpack-info-plugin": "^0.1.0",
        "webpack-sources": "^0.1.1",
        "yargs": "^4.8.0"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
