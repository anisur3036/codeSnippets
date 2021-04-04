# SCSS Things

### **calc()** function use like this

```scss
$a = 4rem;

div {
    height: calc(#{a} - 12px);
    background: tomato;
}
```
### Custom Properties in SCSS

```scss
:root {
    --primary-color: blue;
    --gap: 1.75rem;
}
.wrapper {
    background-color: var(--primary-color);
}

h1 {
    color: var(--primary-color);
    margin-bottom: calc(var(--gap)  * 5px)
}
```

### Font Size Scaling
```scss
:root {
    --base-size: 1em;
    --type-scale: 1.125;
    --small: calc(var(--base-size) / var(--type-scale));
    --h5: calc(var(--base-size) * var(--type-scale));
    --h4: calc(var(--h5) * var(--type-scale));
    --h3: calc(var(--h4) * var(--type-scale));
    --h2: calc(var(--h3) * var(--type-scale));
    --h1: calc(var(--h2) * var(--type-scale));
}

html {font-size: 100%;} /*16px*/

body {
  background: white;
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
  line-height: 1.75;
  color: #000000;
}

p {margin-bottom: 1rem;}

h1, h2, h3, h4, h5 {
  margin: 3rem 0 1.38rem;
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
  line-height: 1.3;
}

h1 {
  margin-top: 0;
  font-size: var(--h1);;
}

h2 {font-size: var(--h2);}

h3 {font-size: var(--h3);}

h4 {font-size: var(--h4);}

h5 {font-size: var(--h5);}

small, .text_small {font-size: var(--small)}

@media (min-width: 480px) {
  :root {
    --type-scale: 1.25;
  }
}

@media (min-width: 780px) {
  :root {
    --type-scale: 1.3;
  }
}
```

[back to css](./readme.md)
