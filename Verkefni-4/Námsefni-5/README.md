# HTML & CSS3 Kvikun

```HTML
<div class="kvikun"></div>
```
### CSS

```CSS
.kvikun {
  width: 100px;
  height: 100px;
  background-color: red;
  position: relative;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
}

@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}
```

| Value  |  Description |
| ---- | ---- |
| animation-name: | Specifies the name of the keyframe you want to bind to  the selector   |
| animation-duration  | Specifies how many seconds or milliseconds an animation takes to complete  |
| animation-timing-function	| Specifies the speed curve of the animation  |
| animation-delay  | Specifies a delay before the animation will start  |
| animation-iteration-count	| Specifies how many times an animation should be played  |
| animation-direction  | Specifies whether or not the animation should play in reverse on alternate cycles  |
| animation-fill-mode  | Specifies what values are applied by the animation outside the time it is executing  |
| animation-play-state  | Specifies whether the animation is running or paused  |

**Animation** is actually a shorthand for eight subproperties:

` animation: duration timing delay iteration direction fill play name; `

```CSS
  /* @keyframes duration | easing-function | delay |
  iteration-count | direction | fill-mode | play-state | name */
  animation: 3s ease-in 1s 2 reverse both paused slide-in;
  
  /* @keyframes duration | easing-function | delay | name */
  animation: 3s linear 1s slide-in;
  
  /* two animations */
  animation:
    3s linear slide-in,
    3s ease-out 5s slide-out;
```

Note: for the shorthand to work properly, make sure you list the values in the same order as listed above.
As you're using the shorthand, there's no need to list the subproperties – you just need to define the values you need. You don't need to use all of the subproperties, but animation-name and animation-duration are necessary for the CSS animation property to work as intended.


heimild: [W3School Animation](https://www.w3schools.com/cssref/css3_pr_animation.asp)

---

### Sýnidæmi

1. [Code pen](https://codepen.io/rokobuljan/pen/XXzqKQ)
1.  [Code pen](https://codepen.io/maheshambure21/pen/qZZrxy)
1.  [Code pen](https://codepen.io/paulnoble/pen/ZYOzLG)
1.  [Code pen](https://codepen.io/jaskiranchhokar/pen/wmGXav)

#### Kvikun - Animation

* [W3Schools CSS Animation](https://www.w3schools.com/css/css3_animations.asp)
* [CSS transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
* [Animate Style](https://animate.style/)
* [Slideshow w3.org](https://www.w3.org/Style/Examples/007/slideshow.en.html#top)
* [Slideshow CSS](https://css-tricks.com/css-only-carousel/)
* [CSS Scrolling text](https://blog.hubspot.com/website/scrolling-text-css)
* [CSS &#9776; - X icon](https://www.w3schools.com/howto/howto_css_menu_icon.asp)
* [Cubic Bezier](https://cubic-bezier.com/)
* Safnsíður
  * [CSS Text Animations](https://freefrontend.com/css-text-animations/)
  * [CSS3 slideshow dæmi](https://codeshack.io/pure-css3-image-slideshow-example/)
  * [28 Slideshow dæmi](https://freefrontend.com/css-slideshows/)
  * [skjá-skvettur (Splash-screens)](https://speckyboy.com/splash-screen-design/)

#### SVG kvikun (_Animation_)

* [Góð byrjun í SVG kvikun](https://artificial.design/archives/2018/05/23/svg-animation.html)
* [CSS Tricks - SVG kvikun](https://css-tricks.com/animating-svg-css/)
* [SVG Icons](https://webdesign.tutsplus.com/tutorials/how-to-animate-festive-svg-icons-with-css--webdesign-17658)

