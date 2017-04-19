# npmdoc-listr

#### api documentation for  [listr (v0.11.0)](https://github.com/samverschueren/listr#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-listr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-listr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-listr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-listr)

#### Terminal task list

[![NPM](https://nodei.co/npm/listr.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/listr)

- [https://npmdoc.github.io/node-npmdoc-listr/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-listr/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-listr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-listr/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-listr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-listr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sam Verschueren",
        "url": "github.com/SamVerschueren"
    },
    "bugs": {
        "url": "https://github.com/samverschueren/listr/issues"
    },
    "dependencies": {
        "chalk": "^1.1.3",
        "cli-truncate": "^0.2.1",
        "figures": "^1.7.0",
        "indent-string": "^2.1.0",
        "is-promise": "^2.1.0",
        "is-stream": "^1.1.0",
        "listr-silent-renderer": "^1.1.1",
        "listr-update-renderer": "^0.2.0",
        "listr-verbose-renderer": "^0.4.0",
        "log-symbols": "^1.0.2",
        "log-update": "^1.0.2",
        "ora": "^0.2.3",
        "rxjs": "^5.0.0-beta.11",
        "stream-to-observable": "^0.1.0",
        "strip-ansi": "^3.0.1"
    },
    "description": "Terminal task list",
    "devDependencies": {
        "ava": "*",
        "clinton": "*",
        "coveralls": "^2.11.14",
        "delay": "^1.3.1",
        "hook-std": "^0.2.0",
        "nyc": "^8.3.2",
        "xo": "*",
        "zen-observable": "^0.3.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5e778bc23806ac3ab984ed75564458151f39b03e",
        "tarball": "https://registry.npmjs.org/listr/-/listr-0.11.0.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "files": [
        "index.js",
        "lib"
    ],
    "gitHead": "7b334b155a06100d1614b78eaba9220e063bdec0",
    "homepage": "https://github.com/samverschueren/listr#readme",
    "keywords": [
        "cli",
        "task",
        "list",
        "tasklist",
        "terminal",
        "term",
        "console",
        "ascii",
        "unicode",
        "loading",
        "indicator",
        "progress",
        "busy",
        "wait",
        "idle"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "samverschueren"
        }
    ],
    "name": "listr",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/samverschueren/listr.git"
    },
    "scripts": {
        "coveralls": "nyc report --reporter=text-lcov | coveralls",
        "test": "clinton && xo && nyc ava"
    },
    "version": "0.11.0",
    "xo": {
        "esnext": true
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
