# Subresource Integrity (SRI)

[Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity)

Verify that resources are delivered without manipulation.

## Example

### JS

```html
<script
    src="https://cdn.jsdelivr.net/npm/vue@2.6.12/dist/vue.min.js"
    integrity="sha256-KSlsysqp7TXtFo/FHjb1T9b425x3hrvzjMWaJyKbpcI="
    crossorigin="anonymous"
></script>
```

### CSS

```html
<link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/tailwindcss@1.8.10/dist/tailwind.min.css"
    integrity="sha256-iDkm+6+g02b+JwSCy00as47Ywhx+tP+NvegUVP+Wsa8="
    crossorigin="anonymous"
>
```
