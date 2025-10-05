# CSS grunnsíða - _CSS boilerplate_
 
### Markmið:
Nemendur öðlast skilning á skipulagningu stílsíðukerfis og á hönnun CSS-grunnsíðu (Boilerplate) til að hanna betri vefsíður.

Þegar komið er að því að hanna vef með skipulögðum hætti er gott að geta stuðst við grunnkerfi þar sem búið er að hanna alla grunnþætti sem nota þarf í vef. Þar má nefna grindakerfi, sveigjanlega hönnun, litaval og leturnotkun.

Meðfylgjandi verkefni er HTML og CSS grunnsíða sem þú getur notað til að búa til þitt eigið grunnsíðukerfi. Vefurinn á að sýna skipulag og útlit vefsins.

* [New CSS - Boilerplate](Námsefni-1/new-css-boilerplate/)
  * [Vefsíða New.css](https://github.com/xz/new.css)
* [Verkefni 1 vinnugögn (.zip skrá)](Námsefni-1/verkefni-1-nemendur.zip)

### Tvískipt litaþema

Hér er dæmi um vefsíðu þar sem vafrinn velur litaþema eftir því hvort notandi er með ljóst eða dökkt litaþema valið í honum. 

![Mynd 1](synidaemi/verk-1L.jpg)
![Mynd 2](synidaemi/verk-1D.jpg)

Litir í mynd eru settir í CSS litaþemað og gulur litur búinn til og settur í það.

### Grid dálkakerfi

![Mynd 3](synidaemi/verk-12L.jpg)
![Mynd 3](synidaemi/verk-13L.jpg)

![Mynd 4](synidaemi/verk-12D.jpg)
![Mynd 4](synidaemi/verk-13D.jpg)

### Svegjanleg hönnun

Farsímar (_Mobile_). Ein dálkabreidd á öllum grid klösum (1fr).

![mynd 5](synidaemi/mobile.JPG) 

Spjaldtölvur (_laptops_). 6 dálkar skiptast rétt.

![mynd 6](synidaemi/ipads.jpg)

Fatölvur. Græni bakgrunnurinn teygist yfir skjáinn (_sérsnið - custom css_).

![mynd 7](synidaemi/laptops.jpg)

# Tafla  &lt;Table> 

Búðu til töflu í vefsíðu, innhald töflunnar getur verið dagskrá af einhverju tagi. Til að byrja með má notast við _dummy_ texta. Vefsíðan á að vera sú sama og þú gerðir í 1. verkefni.

Taflan á að birtast í öllum skjástærðum án þess að fara út fyrir skjáinn.  

#### Viðmið 0 – 48rem (0 – 768px) Það á ekki að þurfa að hliðra til skjánum þegar taflan er skoðuð í farsímum.

![Mynd 1.](synidaemi/tafla-mobileD.jpg) ![Mynd 2.](synidaemi/tafla-mobileL.jpg)

Taflan á að vera í tvískiptu litaþema

#### Viðmið 48rem + (768px).

![Mynd 3.](synidaemi/tafla-ipad.jpg)

#### Viðmið 80rem + (1280px).

![Mynd 4.](synidaemi/tafla-laptop.jpg)

Tabular Data &lt;td> er eina tagið sem er hannað til að sækja gögn af miðlara í hvert sinn sem vefsíða er opnuð, jafnvel þegar flett er á milli síðna. Það er mjög gagnlegt þegar um er að ræða upplýsingar sem þurfa að uppfærast daglega eða oftar.

Töflur henta illa í útlithönnun ss til að birta texta og myndir sem breytast ekki. Vafrinn getur geymt slíkar upplýsingar í vinnsluminni sínu og þarf ekki að sækja þessi gögn í sífellu. "Table" tagið er erfitt að eiga við þegar kemur að sveigjanleika vefsíðu og best að nota það ekki nema þegar um gagnvirkar færslur er að ræða.  

---

## Skráningarform 

Setjið skráningarform inn á vefinn ykkar, hafið samræmi í útliti formsins og töflunnar og í rökréttu samhengi við heildarútlit vefsins.  Formið á að vera sýnilegt í öllum helstu skjástærðum. 
  
![Mynd 5.](synidaemi/form-mobileD.jpg) ![Mynd 6.](synidaemi/form-mobileL.jpg)

Formið á að vera í tvískiptu litaþema

#### Viðmið 48rem + (768px).

![Mynd 7.](synidaemi/form-ipad.jpg)

#### Viðmið 80rem + (1280px).

![Mynd 7.](synidaemi/form-laptop.jpg)

#### Réttritun (_validation_)
Þegar smellt er á hnappinn (_input type:submit_) í skráningarforminu þá athugar (_validate_) vafrinn hvort texti sé rétt skráður í innsláttarreiti (_input_). Ef textinn uppfyllir ekki þau skilyrði sem eiga við þá á ekki að vera hægt að senda upplýsingar frá vefsíðunni (en ef allt er í lagi þá sendum við innsláttinn út í bláinn). 

` <input type=“x“ name=“x“ value=“X“ required placeholder=“fyllið út þennan reit“> `

* Ekki er hægt að skilja nafnareit auðan 		
* Símanúmer verður að vera tölur (numbers)
* Tölvupóstfang verður að vera með @	      	
* Notið „input date“
* Notið „select option, checkbox og radio“. 	
* Notið aðra leturgerð og stærð í „textarea“

#### Tafla 

* Taflan inniheldur upplýsingar sem eru skiljanlegar og skilmerkilega settar upp.
* Notaðu thead, tbody og tfooter tögin í töflukóðanum. Í stílsíðu er hægt að nota gerviklasa (Pseudo class - nth-child) til að fá litskiptingu í bakgrunn töflunnar. 
* Taflan er svegjanleg (responsive) og skiptist þannig að hún er öll sýnileg
á litlum skjáum.

#### Form 
* input -text, -email, -radio, -checkbox, select og textarea er í pöntunarformi 
* Ekki á að vera hægt að senda (submit) form fyrr en skilyrðum (request)  eru uppfyllt í „text“, „email“, „date“ og „telephone“.

### Námsmat: 15%

* Skipulag – Layout				
  * 2% Dálkaskipulag - Grid 
  *	1% Myndir aðlagast skjástærðum
* Útlit					
  * 2% CSS breytur - Litasamsetning
  * 1% Leturval - leturnotkun	
* Tafla	5%
  * aðlagast skjástærðum
* Form	5%				
  * aðlagast skjástærðum
  * innsláttarreitir eru skilyrtir (_required_)	

Vefsíðu og stílsíðu er skilað í _Innu/VEFÞ1VG/Verkefni-2_ í **.zip** skrá. 

#### Einkunn verður birt í Innu

_Gangi þér vel_

---

Vefsíðu og stílsíðu er skilað í _Innu/VEFÞ1VG/Verkefni-1_ í þjappaðri skrá, **Æfingar.zip**. 

#### Einkunn verður birt í Innu

---

### Bjargir

* [Pico _CSS mini framework_](https://picocss.com/docs)


#### CSS breytur (_CSS Variables_)

* [CSS breytur W3Schools](https://www.w3schools.com/css/css3_variables.asp)
* [Moz:lla, CSS eigindi - CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
* [Breytilegt litaþema](https://dev.to/fabiogiolito/create-a-color-theme-with-these-upcoming-css-features-4o83)
* [Create better themes with css variables](https://blog.logrocket.com/create-better-themes-with-css-variables/)

#### Töflur 	

* [Skipulagning gagna](http://learn.shayhowe.com/html-css/organizing-data-with-tables/)
* [Scope eigindið](https://www.w3schools.com/tags/att_scope.asp)
* [RWD tafla, Smitty](http://allthingssmitty.com/2016/10/03/responsive-table-layout/)
* [RWD tafla, CSS-tricks](https://css-tricks.com/responsive-data-tables/)

#### Form

*   [Building Forms](http://learn.shayhowe.com/html-css/building-forms/)
*   [Form moz:lla](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)

#### Form validation

* [HTML &lt;input> pattern Attribute](https://www.w3schools.com/tags/att_input_pattern.asp)
* [W3Schools Form attributes](http://www.w3schools.com/html/html_form_attributes.asp)
* [Form Data Validation](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/Data_form_validation)
* [input date, time fix](https://stackoverflow.com/questions/14946091/are-there-any-style-options-for-the-html5-date-picker?newreg=23b233a466f14c6e851d6e948e96d7ee)

#### Annað
* [11 New CSS Features Every Browser Supports in 2025](https://www.youtube.com/watch?v=55uUK-iJeNM)


