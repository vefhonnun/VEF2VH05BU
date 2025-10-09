# Upplýsingasíða og dæmi, Pico CSS

* Á vefsíðu Pico CSS er hægt að less um alla þætti, íhluti og grunnstíla (leturfræði, form, töflur o.s.frv.) bæði í **ljósum og dökkum ham** sem er beitt á stöðluðum merkingarfræðilegum HTML einingum. Dæmi er hægt að skoða sem notar lágmarks eða enga klasa, sem leggur áherslu á „rithátt HTML“ (_Semandtic HTML_).
* **Grunnsniðmát**: [Dæmi sem sýna flesta íhluti](https://picocss.com/examples/preview/)
* **Grunnsniðmát án klasa:**  [picocss.com/examples/classless/](https://picocss.com/examples/classless/)
* **Tengill á Pico CSS GitHub:** [https://github.com/picocss/pico](https://github.com/picocss/pico)


### CSS breytur (_Variables_)

Hér er dæmi um hvernig hægt er að stíla eigindi þannig að líkja má við breytur í forritun.   

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

Mörg fyrirtæki velja sér lita- og letursamsetningu til að aðgreina sig frá keppinautum þannig að það er gott að geta skilgreint litasamsetningu í upphafi stílsíðu og þar sem sami liturinn birtist á mismunandi flötum og letri þá er alltaf kallað á sama litinn.  Síðan er hægt að yfirfæra stílana yfir á annað fyrirtæki og skipta þá aðeins um litina í breytunum.
Sjá nánar hér: [Using CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)


#### CSS breytur

* [CSS breytur W3Schools](https://www.w3schools.com/css/css3_variables.asp)
* [Moz:lla, CSS eigindi - CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
* [Breytilegt litaþema](https://web.dev/articles/prefers-color-scheme)
* [CSS calc('litaskali)](https://blog.jim-nielsen.com/2021/css-relative-colors/)

#### Lesefni

* [CSS í stærri verkefnum](https://bok.vefforritun.is/22.css-verkefni) (_Bókin um vefforritun, ÓSK_)

#### Annað efni

* [Portal - Minimal CSS](https://github.com/dohliam/dropin-minimal-css)
* [Moz:lla - CSS Grid template](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template)
* [W3Schools - CSS Grid template](https://www.w3schools.com/cssref/pr_grid-template.asp)
* [CSS grid dæmi](https://gridbyexample.com/)
* [CSS tricks, GRID guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
