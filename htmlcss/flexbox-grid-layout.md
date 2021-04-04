# Grid Layout with Flexbox

This is example <code>index.html</code> file
```html
<div class="page-wrapper">
    <section>some conent</section>
    <section>some conent</section>
    <section>some conent</section>
    <section>some conent</section>
</div>
```
css look like this

```css
/* Mobile device */ 
.page-wrapper {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between; 
    --columns: 12;
}
section {
    --width: 12;
    --initial-flex-basis: calc(var(--width, 0) / var(--columns) * 100%);
    --gap: calc((var(--columns, 12) - var(--width)) * 0.4%);
    flex-basis: calc(var(--initial-flex-basis) - var(--gap));
}

/* tablet device and up */
@media (min-width: 740px) {
    section {
        --width: 3;
    }
}
```

[back to css](./readme.md)