# CSS

## Pseudo Selectors

### :first-child
First child only works if the node you are targeting really is 
the first child, it is not getting the first child of that type.

Example, we want to target the first ul and give it a red background.
One might be tempted to go with `ul:first-child`.
```html
  <div class="container">
    <div class="links">
      <ul>
        <li>A</li>
        <li>B</li>
        <li>C</li>
      </ul>
    </div>
    <div class="links">
      <ul>
        <li>D</li>
        <li>E</li>
        <li>F</li>
      </ul>
    </div>
  </div>
```
```css
/* 
  does not work, both ul will get red background 
*/
.container ul:first-child {
  background: red;
}

/* 
  works, only the first ul will get it, since we are targeting
  1. container
    2. the first .links
      3. ul
*/
.container > .links:first-child > ul {
  background: red;
}
```

## Text

### Truncating text inside a flex child
https://codepen.io/chriscoyier/pen/zqedEr
