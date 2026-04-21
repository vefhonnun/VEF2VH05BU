# CSS transition og transform

CSS **transition** er einfaldasta leiðin til að búa til hreyfingu í CSS. Hún sér um að brúa bilið á milli tveggja gilda þegar eiginleika staks er breytt, þannig að breytingin gerist **mjúklega** yfir ákveðinn tíma í stað þess að gerast samstundis.

Hér er það sem þú þarft að vita:

---

### 1. Hvernig virkar það?
Transition virkar eins og „sjálfvirk millifylling“. Ef þú breytir t.d. lit á hnappi úr bláum í rauðan, þá reiknar vafrinn út alla millilitina þannig að breytingin verði eins og rennsli.

Til þess að transition virki þarf yfirleitt **kveikju** (trigger), eins og:
* Notandi setur músina yfir hlut (`:hover`).
* Notandi smellir á hlut (`:active`).
* Breyting á klasa (*class*) í gegnum JavaScript.

### 2. Helstu eiginleikar
Þegar þú skilgreinir transition notarðu fjórar undirstöður:
1. **`transition-property`**: Hvað á að hreyfast? (t.d. `background-color`, `width`, eða `all`).
2. **`transition-duration`**: Hversu lengi á það að taka? (t.d. `0.5s`).
3. **`transition-timing-function`**: Hvernig er hraðinn? (t.d. `ease` byrjar rólega, `linear` er jafn hraði).
4. **`transition-delay`**: Á að bíða í smá stund áður en hreyfingin byrjar?

---

### 3. Einfalt dæmi
Hér er dæmi þar sem kassi verður hringlaga þegar músin fer yfir hann:

```css
.kassi {
  width: 100px;
  height: 100px;
  background: blue;
  border-radius: 0%;
  
  /* Segjum vafranum að fylgjast með border-radius breytingum */
  transition: border-radius 0.4s ease;
}

.kassi:hover {
  border-radius: 50%; /* Verður hringur */
}
```

### Munurinn á Transition og Animation
* **Transition:** Þarf kveikju (t.d. hover), fer bara frá punkti A til B, og er mjög einfalt í uppsetningu.
* **Animation:** Keyrir sjálfkrafa, getur haft marga punkta (A -> B -> C -> D) og getur verið í endalausri lykkju.

Viltu vita hvernig maður stjórnar því að mismunandi hlutir hreyfist á mismunandi hraða í einni transition?

CSS **transform** eiginleikinn er notaður til að breyta útliti og staðsetningu staka í tvívíðu (2D) eða þrívíðu (3D) rými án þess að hafa áhrif á skipulag annarra hluta á síðunni. Þegar við tölum um **kvikun** (animation), þýðir það að við látum þessar breytingar gerast smám saman yfir ákveðinn tíma.

Hér eru helstu leiðirnar til að nota transform:

---

### Helstu tegundir transform
* **`rotate()`**: Snýr stakinu um miðju sína (t.d. `rotate(45deg)`).
* **`scale()`**: Stækkar eða minnkar stakið (t.d. `scale(1.5)` gerir hlutinn 50% stærri).
* **`translate()`**: Færir stakið til hliðar eða upp og niður (t.d. `translateX(50px)`).
* **`skew()`**: Skekkir stakið (lætur það hallast).



---

### Hvernig verður þetta að kvikun?
Til þess að breytingin sé ekki hvellstök (e. eins og smellt sé á rofa), notum við yfirleitt annað af tvennu:

1.  **`transition`**: Notast þegar hlutur breytist við ákveðinn atburð, t.d. þegar músin fer yfir hnapp (*hover*).
    * *Dæmi:* Hnappur stækkar mjúklega þegar þú bendir á hann.
2.  **`@keyframes`**: Notað fyrir flóknari hreyfingar sem eiga að ganga sjálfkrafa eða í lykkju.
    * *Dæmi:* Merki (logo) sem snýst stöðugt í hringi.

### Af hverju að nota transform?
Stærsti kosturinn við transform er **afköst** (performance). Vafrinn vinnur úr transform-breytingum á grafíkörgjörvanum (GPU) í stað aðalörgjörvans. Það þýðir að hreyfingarnar verða „mjúkar“ og valda síður hCalculation-lagi eða harki í vafranum miðað við að breyta gildum eins og `top`, `left` eða `width`.

Hér er einfalt dæmi þar sem við búum til hnapp sem **stækkar** og **snýst** smávegis þegar músin er sett yfir hann (*hover*).

Til að gera þetta mjúkt notum við `transition` ásamt `transform`.

---

### HTML
Fyrst búum við til einfaldan hnapp:
```html
<button class="minn-hnappur">Sjáðu mig!</button>
```

### CSS
Hér gerist galdurinn. Við skilgreinum hvernig hnappurinn á að líta út í grunninn og hvernig hann á að „transformast“:

```css
.minn-hnappur {
  padding: 15px 30px;
  background-color: #3498db;
  color: white;
  border: none;
  cursor: pointer;
  
  /* Hér segjum við vafranum að allar breytingar eigi að taka 0.3 sekúndur */
  transition: transform 0.3s ease;
}

/* Hvað gerist þegar músin fer yfir? */
.minn-hnappur:hover {
  /* Hér stækkum við hnappinn um 10% og snúum honum um 5 gráður */
  transform: scale(1.1) rotate(5deg);
}
```

---

### Hvað er að gerast í kóðanum?

* **`scale(1.1)`**: Stækkar hnappinn úr 100% í 110%.
* **`rotate(5deg)`**: Hallar hnappnum örlítið til hægri.
* **`transition`**: Þetta er mikilvægasta skrefið fyrir kvikunina sjálfa. Án þess myndi hnappurinn „skoppa“ samstundis í nýja lögun. Með því að gefa honum tímann **0.3s** rennur hann mjúklega í nýju stöðuna.

---

Til þess að búa til hreyfingu sem keyrir sjálfkrafa og stöðugt notum við **`@keyframes`**. Í stað þess að bíða eftir að notandinn geri eitthvað (eins og að setja músina yfir), þá skilgreinum við ákveðna „lykilramma“ sem vafrinn fylgir í lykkju.

Hér er dæmi um einfaldan hring sem svífur upp og niður og breytir um lit.

---

### HTML
```html
<div class="bolti"></div>
```

### CSS
Hér skilgreinum við hreyfimynstrið með `@keyframes` og tengjum það svo við boltann:

```css
/* 1. Við búum til hreyfinguna og skírum hana "svif" */
@keyframes svif {
  0% {
    transform: translateY(0px); /* Upphafsstaða */
  }
  50% {
    transform: translateY(-50px) scale(1.1); /* Miðja: fer upp og stækkar */
  }
  100% {
    transform: translateY(0px); /* Endar aftur í sömu stöðu */
  }
}

/* 2. Við búum til boltann og ræsum hreyfinguna */
.bolti {
  width: 100px;
  height: 100px;
  background-color: #e74c3c;
  border-radius: 50%; /* Gerir hlutinn hringlaga */
  margin: 100px auto;

  /* Hér tengjum við hreyfinguna: */
  animation-name: svif;        /* Nafnið á @keyframes */
  animation-duration: 2s;      /* Hversu lengi hver hringur tekur */
  animation-iteration-count: infinite; /* Keyra endalaust */
  animation-timing-function: ease-in-out; /* Gera hreyfinguna mýkri */
}
```

---

### Útskýring á helstu skipunum:

* **`@keyframes`**: Þetta er handritið. Við segjum hvað á að gerast við $0\%$, $50\%$ og $100\%$ af tímanum.
* **`animation-iteration-count: infinite`**: Þetta er mikilvægasta skipunin fyrir „stöðuga“ hreyfingu. Án hennar myndi hreyfingin bara gerast einu sinni og stoppa svo.
* **`translateY(-50px)`**: Færir boltann upp um 50 pixla á Y-ásnum.

### Af hverju er þetta betra en að færa hlutinn með `top` eða `margin`?
Eins og áður sagði þá notar **`transform`** grafíkhraðalinn þinn. Ef þú ert með marga hluti sem hreyfast stöðugt (eins og snjókorn eða stjörnur í bakgrunni), þá mun síðan ennþá keyra mjúklega á meðan aðrar aðferðir gætu látið vafrann „hökta“.

Viltu prófa að búa til eitthvað flóknara, eins og snúning í þrívídd (3D)?