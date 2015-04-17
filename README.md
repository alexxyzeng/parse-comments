# parse-comments [![NPM version](https://badge.fury.io/js/parse-comments.svg)](http://badge.fury.io/js/parse-comments)  [![Build Status](https://travis-ci.org/jonschlinkert/parse-comments.svg)](https://travis-ci.org/jonschlinkert/parse-comments) 

> Parse code comments from JavaScript or any language that uses the same format.

## Install with [npm](npmjs.org)

```bash
npm i parse-comments --save
```

## Usage

```js
var comments = require('parse-comments');
comments(str);
```

Parses a comment like this:

```js
/**
 * Read in source files from file paths or glob patterns. 
 *
 * ```js
 * verb.src('src/*.hbs', {layout: 'default'});
 * ```
 *
 * **Example usage**
 *
 * ```js
 * verb.task('site', function() {
 *   verb.src('src/*.hbs', {layout: 'default'})
 *     verb.dest('dist');
 * });
 * ```
 *
 * @param {String|Array} `glob` Glob patterns or file paths to source files.
 * @param {Object} `options` Options or locals to merge into the context and/or pass to `src` plugins
 * @api public
 */
```

Into an array of comment objects, like this:

```js
[ { subheads: [ 'Example usage' ],
    description: '\n\n```js\nverb.src(\'src/*.hbs\', {layout: \'default\'});\n```\n\n**Example usage**\n\n```js\nverb.task(\'site\', function() {\n  verb.src(\'src/*.hbs\', {layout: \'default\'})\n    verb.dest(\'dist\');\n});\n```',
    param: 
     [ '{String|Array} `glob` Glob patterns or file paths to source files.',
       '{Object} `options` Options or locals to merge into the context and/or pass to `src` plugins' ],
    api: 'public',
    params: 
     [ { type: 'String|Array',
         name: 'glob',
         description: 'Glob patterns or file paths to source files.' },
       { type: 'Object',
         name: 'options',
         description: 'Options or locals to merge into the context and/or pass to `src` plugins' } ],
    comment: 
     { begin: 2,
       end: 21,
       code: 'Verb.prototype.src = function(glob, opts) {',
       content: 'Read in source files from file paths or glob patterns.\n\n```js\nverb.src(\'src/*.hbs\', {layout: \'default\'});\n```\n\n**Example usage**\n\n```js\nverb.task(\'site\', function() {\n  verb.src(\'src/*.hbs\', {layout: \'default\'})\n    verb.dest(\'dist\');\n});\n```\n\n@param {String|Array} `glob` Glob patterns or file paths to source files.\n@param {Object} `options` Options or locals to merge into the context and/or pass to `src` plugins\n@api public\n',
       codeStart: 23 },
    context: 
     { begin: 23,
       type: 'prototype method',
       class: 'Verb',
       name: 'src',
       params: [ 'glob', 'opts' ],
       string: 'Verb.prototype.src()',
       original: 'Verb.prototype.src = function(glob, opts) {' },
    heading: { level: 2, text: 'src', prefix: '.' },
    lead: 'Read in source files from file paths or glob patterns.',
    name: 'src',
    examples: 
     [ { lang: 'js',
         code: 'verb.src(\'src/*.hbs\', {layout: \'default\'});',
         block: '```js\nverb.src(\'src/*.hbs\', {layout: \'default\'});\n```' },
       { lang: 'js',
         code: 'verb.task(\'site\', function() {\n  verb.src(\'src/*.hbs\', {layout: \'default\'})\n    verb.dest(\'dist\');\n});',
         block: '```js\nverb.task(\'site\', function() {\n  verb.src(\'src/*.hbs\', {layout: \'default\'})\n    verb.dest(\'dist\');\n});\n```' } ] } ]
```

## Related projects
 * [js-comments](https://github.com/jonschlinkert/js-comments): Parse JavaScript code comments and generate API documentation.
 * [parse-code-context](https://github.com/jonschlinkert/parse-code-context): Parse code context in a single line of javascript, for functions, variable declarations, methods, prototype properties, prototype methods etc.
 * [code-context](https://github.com/jonschlinkert/code-context): Parse a string of javascript to determine the context for functions, variables and comments based on the code that follows.
 * [gfm-code-blocks](https://github.com/jonschlinkert/gfm-code-blocks): Extract gfm (GitHub Flavored Markdown) fenced code blocks from a string.
 * [extract-comments](https://github.com/jonschlinkert/extract-comments): Extract code comments from string or from a glob of files.
 * [esprima-extract-comments](https://github.com/jonschlinkert/esprima-extract-comments): Extract code comments from string or from a glob of files using esprima.  

## Running tests
Install dev dependencies:

```bash
npm i -d && npm test
```

## Contributing
Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/parse-comments/issues)

## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2015 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on April 17, 2015._

<!-- deps:mocha -->
