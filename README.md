# npmdoc-documentation

#### basic api documentation for  [documentation (v3.0.4)](https://github.com/documentationjs/documentation#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-documentation.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-documentation) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-documentation.svg)](https://travis-ci.org/npmdoc/node-npmdoc-documentation)

#### a documentation generator

[![NPM](https://nodei.co/npm/documentation.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/documentation)

- [https://npmdoc.github.io/node-npmdoc-documentation/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-documentation/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-documentation/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-documentation/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-documentation/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-documentation/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tom MacWright"
    },
    "bin": {
        "documentation": "./bin/documentation.js"
    },
    "browser": {
        "vinyl-fs": false
    },
    "browserify": {
        "transform": [
            "brfs"
        ]
    },
    "bugs": {
        "url": "https://github.com/documentationjs/documentation/issues"
    },
    "dependencies": {
        "ast-types": "^0.8.12",
        "babel-core": "^5.0.0",
        "babelify": "^6.3.0",
        "brfs": "^1.4.0",
        "concat-stream": "^1.5.0",
        "doctrine": "^0.7.0",
        "documentation-theme-default": "^1.0.0",
        "extend": "^3.0.0",
        "get-comments": "^1.0.1",
        "github-url-from-git": "^1.4.0",
        "globals-docs": "^2.1.0",
        "handlebars": "^3.0.0",
        "highlight.js": "^8.4.0",
        "js-yaml": "^3.3.1",
        "jsdoc-inline-lex": "^1.0.1",
        "mdast": "^2.0.0",
        "mdast-html": "^1.2.1",
        "mdast-toc": "^1.1.0",
        "micromatch": "^2.1.6",
        "module-deps": "^3.7.3",
        "parse-filepath": "^0.6.3",
        "remote-origin-url": "^0.4.0",
        "resolve": "^1.1.6",
        "slugg": "^0.1.2",
        "stream-array": "^1.1.0",
        "strip-json-comments": "^1.0.2",
        "traverse": "^0.6.6",
        "unist-builder": "^1.0.0",
        "vfile": "^1.1.2",
        "vfile-reporter": "^1.4.1",
        "vfile-sort": "^1.0.0",
        "vinyl": "^0.5.0",
        "vinyl-fs": "^1.0.0",
        "yargs": "^3.5.4"
    },
    "description": "a documentation generator",
    "devDependencies": {
        "chdir": "0.0.0",
        "eslint": "^1.5.1",
        "glob": "^5.0.2",
        "lodash": "^3.10.1",
        "mock-fs": "^3.2.0",
        "tap": "^2.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "c3c714745cec1b498380d8b6754f83e061ac076c",
        "tarball": "https://registry.npmjs.org/documentation/-/documentation-3.0.4.tgz"
    },
    "gitHead": "ab318125d4333f38b657e9b8418e1180670aa6c1",
    "homepage": "https://github.com/documentationjs/documentation#readme",
    "keywords": [
        "documentation",
        "formatter",
        "jsdoc",
        "jsdoc3",
        "parser",
        "website"
    ],
    "license": "ISC",
    "main": "index.js",
    "maintainers": [
        {
            "name": "tmcw"
        },
        {
            "name": "mourner"
        },
        {
            "name": "jfirebaugh"
        }
    ],
    "name": "documentation",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/documentationjs/documentation.git"
    },
    "scripts": {
        "doc": "documentation index.js -f md > docs/NODE_API.md",
        "lint": "eslint bin lib index.js test",
        "test": "npm run lint && tap -t 120 --coverage test/*.js test/lib test/misc test/streams"
    },
    "version": "3.0.4"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
