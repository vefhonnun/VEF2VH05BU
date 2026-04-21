# CSS Cubic-Bezier Kúrfur: Hraði og Hreyfing

Cubic-bezier kúrfur í CSS eru notaðar til að stjórna **hraða** hreyfinga (transitions eða animations) yfir tímann. Í stað þess að hlutur hreyfist með jöfnum hraða, gerir þetta okkur kleift að búa til náttúrulegri hreyfingar, eins og hluti sem byrja rólega og flýta svo á sér.

---

### Hvernig virkar hún?

Kúrvan byggir á fjórum punktum á hnitakerfi sem skilgreina lögun línunnar. Formúlan lítur svona út:

`cubic-bezier(x1, y1, x2, y2)`

* **P0 (0,0):** Upphafspunkturinn (fastur, neðst til vinstri).
* **P1 (x1, y1):** Fyrri "stýripunkturinn" sem togar í kúrvuna.
* **P2 (x2, y2):** Seinni "stýripunkturinn" sem togar í kúrvuna.
* **P3 (1,1):** Endapunkturinn (fastur, efst til hægri).



**X-ásinn** táknar tímann (frá 0% til 100%), og **Y-ásinn** táknar framvindu hreyfingarinnar. Með því að færa punktana $P1$ og $P2$ geturðu búið til hreyfingar sem skoppa, þjóta af stað eða hægja mjúklega á sér.

---

### Einfalt dæmi

Hér er dæmi um hvernig þú myndir nota þetta í CSS. Við ætlum að búa til hreyfingu sem byrjar mjög hratt en "skýst" aðeins fram úr lokamarkmiðinu áður en hún lendir (svokallað *back-out* effect).

```css
.box {
  width: 100px;
  height: 100px;
  background-color: skyblue;
  transition: transform 0.6s cubic-bezier(0.17, 0.67, 0.83, 1.67);
}

.box:hover {
  transform: translateX(300px);
}
```

### Algengar tilbúnar kúrfur
CSS býður upp á flýtileiðir fyrir algengustu týpurnar, sem eru í raun bara fyrirfram skilgreindir cubic-bezier punktar:

* **`ease`**: Svarar til `cubic-bezier(0.25, 0.1, 0.25, 1.0)`
* **`linear`**: Svarar til `cubic-bezier(0.0, 0.0, 1.0, 1.0)` (jafn hraði)
* **`ease-in-out`**: Svarar til `cubic-bezier(0.42, 0, 0.58, 1.0)`

> **Ráð:** Það er nánast ómögulegt að skrifa þessar tölur úr höfðinu. Flestir hönnuðir nota tól eins og [**cubic-bezier.com**](https://cubic-bezier.com/#.17,.67,.83,.67) eða Inspect Element í vafranum til að draga punktana til og sjá hreyfinguna í rauntíma.

---

Hér er dæmi um hvernig hægt er að nota `cubic-bezier` í CSS `animation` til að búa til náttúrulega og dýnamíska skopp-hreyfingu (bounce animation).

Lykillinn að því að láta þetta líta raunverulega út er að nota tvær mismunandi kúrfur: eina þegar hluturinn fellur (hraðari) og aðra þegar hann skoppar upp aftur (rólegri í byrjun, hægir á sér undir lokin).

### CSS Kóðinn

```css
/* Geymirinn sem boltinn er í */
.stage {
  width: 100%;
  height: 300px;
  position: relative;
  background: #f0f0f0;
  border-bottom: 5px solid #333; /* Gólfið */
  overflow: hidden;
}

/* Boltinn */
.ball {
  width: 50px;
  height: 50px;
  background-color: #ff4757;
  border-radius: 50%;
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  
  /* Hér gerist töfrarnir */
  animation: bounce 1.5s infinite;
}

/* Skilgreining á hreyfingunni */
@keyframes bounce {
  /* Upphafsstaða: Boltinn er efst */
  0% {
    top: 0;
    /* Flýtir á sér þegar hann fellur */
    animation-timing-function: cubic-bezier(0.42, 0, 1.0, 0.7);
  }
  
  /* Boltinn lendir á botninum */
  40% {
    top: 250px; /* (Hæð sviðs - hæð bolta) */
    transform: translateX(-50%) scaleY(1); /* Engin skekkja ennþá */
  }
  
  /* "Kreistist" þegar hann lendir */
  50% {
    top: 260px; /* Fer örlítið neðar vegna kreistingar */
    transform: translateX(-50%) scaleY(0.7) scaleX(1.3); /* Kreistur saman */
    /* Byrjar rólega að skoppa upp */
    animation-timing-function: cubic-bezier(0, 0.3, 0.5, 1.0);
  }
  
  /* Helmingur skoppsins upp */
  70% {
    top: 150px;
    transform: translateX(-50%) scaleY(1); /* Endurheimtir lögun */
    animation-timing-function: cubic-bezier(0, 0.3, 0.5, 1.0);
  }

  /* Boltinn er næstum kominn aftur upp */
  100% {
    top: 0;
    transform: translateX(-50%) scaleY(1);
  }
}
```

### Útskýring á því hvernig þetta virkar

Í þessu dæmi notum við `@keyframes` til að skilgreina hvernig boltinn hegðar sér á mismunandi tímapunktum hreyfingarinnar. cubic-bezier gildin spila lykilhlutverk í að stjórna hraðanum:

1.  **Fall (0% - 40%):**
    * Við notum `animation-timing-function: cubic-bezier(0.42, 0, 1.0, 0.7)`. Þessi kúrva lætur boltann byrja tiltölulega hægt en flýta sérsvakalega á sér þegar hann nálgast jörðina, sem hermir eftir þyngdaraflinu.

2.  **Lending og Kreisting (40% - 50%):**
    * Hér notum við `scaleY` og `scaleX` til að láta boltann "kreistast" örlítið þegar hann lendir, sem gefur honum dýnamískari og mýkri tilfinningu.

3.  **Skopp Upp (50% - 100%):**
    * Eftir kreistinguna notum við `animation-timing-function: cubic-bezier(0, 0.3, 0.5, 1.0)`. Þessi kúrva lætur boltann *skjótast* upp frá jörðinni en hægja svo mjúklega á sér þegar hann nær hámarkshæð.

Með því að skipta hreyfingunni niður í þessi skref og nota mismunandi kúrfur fyrir upp- og niðurleið, búum við til mun líflegra og dýnamískara skopp en ef við myndum bara nota einfalt `ease`.