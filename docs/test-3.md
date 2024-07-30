Markdown:  
`[Button](https://google.com ":class=button")`  
[Button](https://google.com ":class=button")

HTML:  
`<a href="https://google.com " class="button">Button</a>`  
<a href="https://google.com " class="button">Button</a>

Markdown (unsupported):  
`[Primary Button](https://google.com ":class=button primary")`  
[Primary Button](https://google.com ":class=button primary")

HTML:  
`<a href="https://google.com " class="button primary">Primary Button</a>`  
<a href="https://google.com " class="button primary">Primary Button</a>

Markdown:  
`[Primary Button](https://google.com '{class: button primary"}`  
[Primary Button](https://google.com '{class: button primary"}

HTML:  
`<a href="https://google.com " class="button primary">Primary Button</a>`  
<a href="https://google.com " class="button primary">Primary Button</a>

Markdown:  
`[Text](page.md '{foo: true, target: "_blank" class: "bar baz"}  This is the title')`
`[Text](page.md '{{foo: true, target: "_blank" class: "bar baz"}}  This is the title')`

HTML:  
<a href="page.md" foo="true" target="_blank" class="bar baz" title="This is the title">Text</a>

OTHER TESTS

`[Text](page.md ':target=_blank :class=foo bar')`  
[Text](page.md ':target=_blank :class=foo bar')

`[Text](page.md ':class=foo bar :target=_blank ')`  
[Text](page.md ':class=foo bar :target=_blank ')

