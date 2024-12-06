# CSS breytur og fleiri stílbrögð 

### Markmið:
Nemendur eiga að öðlast skilning á hvernig hægt er að nota breytur og aðrar flóknar aðgerðir í CSS stílsíðu.

### CSS breytur (_Variables_)

Custom Properties 3%  
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
Sjá nánar hér: https://developer.mozilla.org/en-US/docs/Web/CSS/

