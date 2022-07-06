# reamrk-mdi

Transforms 
```md
Hello :mdi-robot:!
```

to

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

or when processed to html, it will result as

```html
<p>
    Hello <span class="mdi-ronot mdi"></span>!
</p>
```

## installation

```
yarn add remark-mdi @mdi/font
```

and make sure to import the stylesheet of mdi: 

```scss
import "@mdi/font/css/materialdesignicons.min.css"
```
