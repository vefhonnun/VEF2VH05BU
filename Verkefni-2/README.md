# Flókin stílbrögð 

### Markmið:
Nemendur öðlast skilning á að beita flóknari stílaðferðum í CSS til að hanna betri vefsíður. 

### Fellilisti í efnisyfirliti (_Drop down menu_)

Nú á að búa til efnisyfirlit á vefsíðuna, gerið ráð fyrir að það séu nokkrir tenglar (links) séu í efnisyfirlitinu.  
 
- Í skjáum stærri en 48em á efnisyfirlitið að vera lárétt efst á síðunni með fastri (_„fixed“_) staðsetningu
- Í minni skjástærðum 20em – 48em, á efnisyfirlitið að vera í fellilista (_drop down menu_) og [≡] hnappur er efst á síðunni
- Þegar smellt er á [≡] hnappinn þá birtist efnisyfirlitið og fer tilbaka þegar smellt er aftur á takkann. 
- ![fellilisti - drop down menu](images/fellilisti.jpg)
- Dæmi: [https://tolvubraut.is](https://tolvubraut.is/)

### Sprettigluggi (_Modal_)

- Í efnisyfirlitinu (_nav_) á að vera tengill sem ber heitið **Innskráning**
- Þegar smellt er á tengilinn þá birtist sprettigluggi (_Modal_). 
- Í glugganum á að vera form með innsláttarreitum fyrir nafn og lykilorð
- ![pop up modal](images/modal.jpg)
- Sjá nánar: [Pop up Modal](https://picocss.com/docs/modal)
- Það á ekki að vera hægt að senda formið án þess að fylla út innsláttarreitina
- þegar smellt er á **innskráning** þá förum við á nýja vefsíðu
- ` <form action="admin.html" method="get"> ` (_í VEFÞ2VF05CU verður formið notað með réttum hætti_)
- ![control panel](images/controlpanel.jpg)

### Stjórnborð

- Á "admin.html" á að útlitshanna viðmót á umsjónarkerfi vefs
- Upplýsingar um hvern flokk á að setja í tagið `details` 
- Upplýsingar um Notendur eru í `summary` taginu í `table`
- ![notendatafla](images/controlpanelOpen.jpg)
- Taflan á að vera sveigjanleg 
- ![notendatafla 2](images/controlpanelSmall.jpg)

### Námsmat 5%

- Fellilisti í efnisyfirliti (_drop down menu_)
    -	[≡] Tákn sem birtir fellilista (Drop down menu)
    -	Allir tenglar sýnilegir í einni línu efst í vefsíðu í 60rem + skjástærð
- Details list (_Accordion list_)
- Sprettigluggi (_Modal_)
- Admin html síða


#### Verkefnaskil

-  Inna/VEFÞ2VH05BU/Verkefni-2  í **.zip** skrá.

#### Einkunn verður birt í Innu

_Gangi þér vel_

---

#### Námsefni

* [Pico CSS](https://picocss.com/)
* [Complex Selectors](Námsefni-2/README.md)
* [Transition og transform](Námsefni-2/Transition-Transform.md)
* [Hulduklasar (_Pseudo classes_)](Námsefni-2/pseudo-classes.md)
* [11 New CSS Features Every Browser Supports in 2025](https://www.youtube.com/watch?v=55uUK-iJeNM)

#### Flóknir stílar - _Complex Selectors_

* [Shayhowe, Flóknar stílsetningar (_Complex Selectors_)](https://learn.shayhowe.com/advanced-html-css/complex-selectors/)
* [Sprettigluggi (_Modal_)](https://picocss.com/docs/modal)
* [Harmonikkulisti **Details & Summary**](https://picocss.com/docs/accordion)
