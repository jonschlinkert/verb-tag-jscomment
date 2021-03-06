# verb-tag-jscomments [![NPM version](https://badge.fury.io/js/verb-tag-jscomments.png)](http://badge.fury.io/js/verb-tag-jscomments)

> Tag for Verb. Uses js-comments to parse JavaScript code comments and generate API documentation.

Visit the [js-comments](https://github.com/jonschlinkert/js-comments) repo for documentation.

## Install
Install with [npm](npmjs.org):

```bash
npm i verb-tag-jscomments --save-dev
```

## Usage

If you're using [verb-cli][verb-cli], you will need to define `['verb-tag-jscomments']` in the `tags` property in the front matter of your project's `.verbrc.md` (or `docs/README.tmpl.md`). This registers the tag with [verb][verb]:

Example:

```yaml
---
tags: ['verb-tag-jscomments']
---
```

In your templates, you can now use the tag like this:

```js
{%= jscomments("index.js") %}
```

_(Also note that front-matter is just one way to register verb tags, filters, and plugins. See the [verb documentation][docs] for more info.)_


## Filtering

The easiest way to filter the output is to use Coffee front matter.

```coffee
---coffee
tags: ['verb-tag-jscomments']

# extend the function onto the context
fn:
  filter = (comment) -> console.log(comment)
---

{%= jscomments("index.js", {fn: filter}) %}
```

## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2014 Jon Schlinkert, contributors.  
Released under the MIT license

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on August 25, 2014._

[verb]: https://github.com/assemble/verb
[docs]: https://github.com/assemble/verb/blob/master/DOCS.md#tags
[verb-cli]: https://github.com/assemble/verb-cli