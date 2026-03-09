# CSS Variables and Additional Styling Techniques

### Goal:
Students should gain an understanding of how variables and other advanced features can be used in a CSS stylesheet.

### CSS Variables

Custom Properties 3%
Here is an example of how properties can be styled in a way that resembles variables in programming.

```CSS

/* :root is a global location; the --properties defined there can be used in all style rules. */

:root {
  --body: rgb(34, 34, 34);
  --a: rgb(19, 104, 112);
  --visited: rgb(33, 140, 150);
  --hover: rgb(33, 140, 150); 
  --footerbg: linear-gradient(rgb(183, 232, 236),rgb(125, 221, 230));
}


body {
  color: var(--body);
}
a {
  color: var(--a); 
}
a:visited {
  color: var(--visited); 
}
a:hover,
a:active {
  color: var(--hover);
  text-decoration: none;
}
.footerbg {
  background-image: var(--footerbg);
}

```

Many companies choose a color and typography combination to stand out from competitors, so it is useful to define the color scheme at the beginning of a stylesheet. Where the same color appears across different surfaces and text, the same variable can be reused. The styles can then be transferred to another company by only changing the colors in the variables.
See more here: https://developer.mozilla.org/en-US/docs/Web/CSS/

