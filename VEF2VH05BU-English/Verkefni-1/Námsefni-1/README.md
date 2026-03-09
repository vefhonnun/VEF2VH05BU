# Information Page and Examples, Pico CSS

* On the Pico CSS website, you can read about all elements, components, and base styles (typography, forms, tables, etc.) in both **light and dark mode**, applied to standard semantic HTML elements. You can also view examples that use minimal or no classes, emphasizing "semantic HTML writing style" (_Semantic HTML_).
* **Base template**: [Examples showing most components](https://picocss.com/examples/preview/)
* **Classless base template:**  [picocss.com/examples/classless/](https://picocss.com/examples/classless/)
* **Link to Pico CSS GitHub:** [https://github.com/picocss/pico](https://github.com/picocss/pico)


### CSS Variables

Here is an example of how properties can be styled in a way that resembles variables in programming.

```CSS

/* :root er „global“ staðsetning, --eigindin sem eru þar er hægt að nota í öllum stílsetningum. */

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

Many companies choose a color and typography combination to stand out from competitors, so it is useful to define the color scheme at the start of a stylesheet. Wherever the same color appears across different surfaces and text, the same variable can be reused. The styles can then be transferred to another brand by only changing the colors in the variables.
See more here: [Using CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)


#### CSS Variables

* [CSS variables W3Schools](https://www.w3schools.com/css/css3_variables.asp)
* [Mozilla, CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
* [Adaptive color theme](https://web.dev/articles/prefers-color-scheme)
* [CSS calc (color scale)](https://blog.jim-nielsen.com/2021/css-relative-colors/)

#### Reading Material

* [CSS in larger projects](https://bok.vefforritun.is/22.css-verkefni) (_The Web Programming Book, OSK_)

#### Other Material

* [Portal - Minimal CSS](https://github.com/dohliam/dropin-minimal-css)
* [Moz:lla - CSS Grid template](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template)
* [W3Schools - CSS Grid template](https://www.w3schools.com/cssref/pr_grid-template.asp)
* [CSS grid examples](https://gridbyexample.com/)
* [CSS tricks, GRID guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
