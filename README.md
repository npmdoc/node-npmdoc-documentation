# api documentation for  [documentation (v3.0.4)](https://github.com/documentationjs/documentation#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-documentation.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-documentation) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-documentation.svg)](https://travis-ci.org/npmdoc/node-npmdoc-documentation)
#### a documentation generator

[![NPM](https://nodei.co/npm/documentation.png?downloads=true)](https://www.npmjs.com/package/documentation)

[![apidoc](https://npmdoc.github.io/node-npmdoc-documentation/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-documentation_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-documentation/build/apidoc.html)

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
            "name": "tmcw",
            "email": "tom@macwright.org"
        },
        {
            "name": "mourner",
            "email": "agafonkin@gmail.com"
        },
        {
            "name": "jfirebaugh",
            "email": "john.firebaugh@gmail.com"
        }
    ],
    "name": "documentation",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module documentation](#apidoc.module.documentation)
1.  object <span class="apidocSignatureSpan">documentation.</span>formats
1.  object <span class="apidocSignatureSpan">documentation.</span>lint
1.  object <span class="apidocSignatureSpan">documentation.</span>module_filters

#### [module documentation.formats](#apidoc.module.documentation.formats)
1.  [function <span class="apidocSignatureSpan">documentation.formats.</span>html (comments, options, callback)](#apidoc.element.documentation.formats.html)
1.  [function <span class="apidocSignatureSpan">documentation.formats.</span>json (comments, opts, callback)](#apidoc.element.documentation.formats.json)
1.  [function <span class="apidocSignatureSpan">documentation.formats.</span>md (comments, opts, callback)](#apidoc.element.documentation.formats.md)

#### [module documentation.lint](#apidoc.module.documentation.lint)
1.  [function <span class="apidocSignatureSpan">documentation.</span>lint (comment)](#apidoc.element.documentation.lint.lint)
1.  [function <span class="apidocSignatureSpan">documentation.lint.</span>format (comments)](#apidoc.element.documentation.lint.format)

#### [module documentation.module_filters](#apidoc.module.documentation.module_filters)
1.  [function <span class="apidocSignatureSpan">documentation.module_filters.</span>externals (indexes, options)](#apidoc.element.documentation.module_filters.externals)
1.  [function <span class="apidocSignatureSpan">documentation.module_filters.</span>internalOnly ()](#apidoc.element.documentation.module_filters.internalOnly)



# <a name="apidoc.module.documentation"></a>[module documentation](#apidoc.module.documentation)



# <a name="apidoc.module.documentation.formats"></a>[module documentation.formats](#apidoc.module.documentation.formats)

#### <a name="apidoc.element.documentation.formats.html"></a>[function <span class="apidocSignatureSpan">documentation.formats.</span>html (comments, options, callback)](#apidoc.element.documentation.formats.html)
- description and source-code
```javascript
function makeHTML(comments, options, callback) {
  comments = walk(comments, highlight);

  options = options || {};

  var themeModule = resolveTheme(options.theme);
  var pageTemplate = getTemplate(Handlebars, themeModule, 'index.hbs');

  Handlebars.registerPartial('section',
    getTemplate(Handlebars, themeModule, 'section.hbs'));

  var paths = comments.map(function (comment) {
    return comment.path.join('.');
  }).filter(function (path) {
    return path;
  });

  helpers(Handlebars, paths);

  // push assets into the pipeline as well.
  vfs.src([themeModule + '/assets/**'], { base: themeModule })
    .pipe(concat(function (files) {
      callback(null, files.concat(new File({
        path: 'index.html',
        contents: new Buffer(pageTemplate({
          docs: comments,
          options: options
        }), 'utf8')
      })));
    }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.documentation.formats.json"></a>[function <span class="apidocSignatureSpan">documentation.formats.</span>json (comments, opts, callback)](#apidoc.element.documentation.formats.json)
- description and source-code
```javascript
json = function (comments, opts, callback) {

  walk(comments, function (comment) {
    delete comment.errors;
  });

  return callback(null, JSON.stringify(comments, null, 2));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.documentation.formats.md"></a>[function <span class="apidocSignatureSpan">documentation.formats.</span>md (comments, opts, callback)](#apidoc.element.documentation.formats.md)
- description and source-code
```javascript
md = function (comments, opts, callback) {
  var processor = mdast().use(toc);
  markdownAST(comments, opts, function (err, ast) {
    var processedAST = processor.run(ast);
    return callback(null, processor.stringify(processedAST));
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.documentation.lint"></a>[module documentation.lint](#apidoc.module.documentation.lint)

#### <a name="apidoc.element.documentation.lint.lint"></a>[function <span class="apidocSignatureSpan">documentation.</span>lint (comment)](#apidoc.element.documentation.lint.lint)
- description and source-code
```javascript
function lint(comment) {
  comment.tags.forEach(function (tag) {
    function nameInvariant(name) {
      if (CANONICAL[name]) {
        comment.errors.push({
          message: 'type ' + name + ' found, ' + CANONICAL[name] + ' is standard',
          commentLineNumber: tag.lineNumber
        });
      }
    }

    function checkCanonical(type) {
      if (type.type === 'NameExpression') {
        nameInvariant(type.name);
      } else if (type.type === 'UnionType') {
        type.elements.forEach(checkCanonical);
      } else if (type.type === 'OptionalType') {
        checkCanonical(type.expression);
      } else if (type.type === 'TypeApplication') {
        checkCanonical(type.expression);
        type.applications.map(checkCanonical);
      }
    }

    if (tag.title === 'param' && tag.type) {
      checkCanonical(tag.type);
    }
  });
  return comment;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.documentation.lint.format"></a>[function <span class="apidocSignatureSpan">documentation.lint.</span>format (comments)](#apidoc.element.documentation.lint.format)
- description and source-code
```javascript
function format(comments) {
  var vFiles = {};
  walk(comments, function (comment) {
    comment.errors.forEach(function (error) {
      var p = comment.context.file;
      var parts = parseFilepath(p);
      vFiles[p] = vFiles[p] || new VFile({
        directory: parts.dirname,
        filename: parts.basename
      });
      vFiles[p].warn(error.message, {
        line: comment.loc.start.line + error.commentLineNumber || 0
      });
    });
  });
  return reporter(Object.keys(vFiles).map(function (p) {
    return vfileSort(vFiles[p]);
  }));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.documentation.module_filters"></a>[module documentation.module_filters](#apidoc.module.documentation.module_filters)

#### <a name="apidoc.element.documentation.module_filters.externals"></a>[function <span class="apidocSignatureSpan">documentation.module_filters.</span>externals (indexes, options)](#apidoc.element.documentation.module_filters.externals)
- description and source-code
```javascript
function externalModuleFilter(indexes, options) {
  var externalFilters = false;
  if (options.external) {
    var test = micromatch.matcher(options.external);
    externalFilters = indexes.map(function (index) {
      // grab the path of the top-level node_modules directory.
      var topNodeModules = path.join(path.dirname(index), 'node_modules');
      return function matchGlob(file, pkg) {
        // if a module is not found, don't include it.
        if (!file || !pkg) {
          return false;
        }
        // if package.json specifies a 'main' script, strip that path off
        // the file to get the module's directory.
        // otherwise, just use the dirname of the file.
        if (pkg.main) {
          file = file.slice(0, -path.normalize(pkg.main).length);
        } else {
          file = path.dirname(file);
        }
        // test the path relative to the top node_modules dir.
        var p = path.relative(topNodeModules, file);
        return test(p);
      };
    });
  }

  return function (id, file, pkg) {
    var internal = internalModuleRegexp.test(id);
    return internal || (externalFilters &&
      externalFilters
      .some(function (f) {
        return f(file, pkg);
      }));
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.documentation.module_filters.internalOnly"></a>[function <span class="apidocSignatureSpan">documentation.module_filters.</span>internalOnly ()](#apidoc.element.documentation.module_filters.internalOnly)
- description and source-code
```javascript
internalOnly = function () { [native code] }
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
