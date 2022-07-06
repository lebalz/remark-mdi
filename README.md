# remark-mdi
## Syntax

```md
Hello :mdi-robot:!
```
## AST (see [mdast](https://github.com/syntax-tree/mdast/blob/master/readme.md) specification)

For example, the following markdown:

`:mdi-robot:`

Yields:

```js
{
    type: 'mdi',
    mdi: 'robot',
    data: {
        hName: 'span',
        icon: 'robot',
        hProperties: {
            className: ['mdi-robot', 'mdi']
        }
    }
}
```

## Rehype

This plugin is compatible with [rehype][https://github.com/rehypejs/rehype]. `mdi` mdast nodes (e.g. `:mdi-robot:`) will become `<span class="mdi-robot mdi"></span>`.

## Installation

```bash
yarn add remark-mdi @mdi/font
```

and make sure to import the stylesheet of mdi: 

```scss
import "@mdi/font/css/materialdesignicons.min.css"
```


## Usage

Dependencies:

```javascript
const unified = require('unified')
const remarkParse = require('remark-parse')
const stringify = require('rehype-stringify')
const remark2rehype = require('remark-rehype')

const remarkMdi = require('remark-mdi')
```

Usage:

```javascript
unified()
  .use(remarkParse)
  .use(remarkMdi)
  .use(remark2rehype)
  .use(stringify)
```
