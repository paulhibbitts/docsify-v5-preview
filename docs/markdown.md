# Markdown configuration

**docsify** uses [marked v13+](https://github.com/markedjs/marked) as its Markdown parser. You can customize how it renders your Markdown content to HTML by customizing `renderer`:

```js
window.$docsify = {
  markdown: {
    smartypants: true,
    renderer: {
      link() {
        // ...
      },
    },
  },
};
```

?> Configuration Options Reference: [marked documentation](https://marked.js.org/#/USING_ADVANCED.md)

You can completely customize the parsing rules.

```js
window.$docsify = {
  markdown(marked, renderer) {
    // ...

    return marked;
  },
};
```

## Limited Support of mermaid

!> Currently, docsify only supports mermaid version `v9.3.0` (as the async render in mermaid `v10.x` is not yet supported in docsify)

```js

// <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.css">
// <script src="https://cdn.jsdelivr.net/npm/mermaid@9.3.0/dist/mermaid.min.js"></script>

let num = 0;
mermaid.initialize({ startOnLoad: false });

window.$docsify = {
  markdown: {
    renderer: {
      code({ text, lang }) {
        if (lang === 'mermaid') {
          return /* html */ `
            <div class="mermaid">${mermaid.render(
              'mermaid-svg-' + num++,
              text,
            )}</div>
          `;
        }
        return this.origin.code.apply(this, arguments);
      },
    },
  },
};
```
