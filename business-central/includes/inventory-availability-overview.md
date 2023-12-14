---
author: brentholtorf
ms.topic: include
ms.date: 09/11/2023
ms.author: bholtorf
---

Auka skilvirkni í vöruhúsinu með nákvæmum, rauntíma upplýsingum um þætti sem geta haft áhrif á tiltækt magn. Dæmi: 

* Birgðastig
* Staðsetningar
* Vinnslustigum
* Atriði í sóttkví
* Bókanir

Hægt er að nálgast upplýsingar um vöruframboð úr eftirtöldum upprunaskjölum:

* Sölupantanir
* Framleiðslupantanir
* Samsetningar pantanir
* Verk

Upplýsingarnar virða einnig aðra þætti sem hafa áhrif á framboð. Til dæmis, hollur hólmur, læst hólf og vörur sem ekki eru tiltækar fyrir tiltekt. Til dæmis gætu vörur verið teknar frá eða verið í bið eða frágangsaðgerðir eða afhendingar.  **Síðan Tínslusamantekt**  gerir kleift að fara yfir atriðin sem  [!INCLUDE [prod_short](prod_short.md)]  ekki hafa verið í tínsluskjölum og grípa til nauðsynlegra aðgerða.

> [!NOTE]
> Þessi hæfileiki krefst þess að kveikt sé á  **beini-frágangs-og tínsluvíxlun**  fyrir birgðageymslur sem notaðar eru í tiltektarferlinu.

### Setja upp forsýn

Til að fá upplýsingar um hvað er verið að taka til og hvað er ekki, er kveikt  **á yfirlitssýningu (beinn frágangur og tínsla)**  Víxlböð  **·**  **-Stofna tínslu-og afhendingarsíður-stofnað tínslubeiðandi.** 

### Ákvarða magnið sem hægt er að tína

Í línum á  **yfirlitssíðu**  vöruhúsatínslu er reiturinn Magn til afgreiðslu (stofn)  **, og hversu margar,**  sem reynt var að taka  [!INCLUDE [prod_short](prod_short.md)]  til. Í upplýsingakassa samantektar  **er að**  finna nánari upplýsingar.

Til einföldunar er  **rannsakað magn pickable-magns.** gæti gefið þér nægar upplýsingar. Í reitnum sést hversu mörg atriði eru tiltæk. Ef magn pickable er minna en búist var við skal kanna innihald hólfsins.

 **Pickable-magn** er hámarksmagn sem  [!INCLUDE [prod_short](prod_short.md)]  telja má til tínslu. Þetta magn samanstendur af vörum í pickable-hólfum. Magnið í útilokuðu magni sem er í læstum eða tilefnum hólfum eða vörum sem eru tíndar inn í vöruhúsatínsluskjölum. Ef varan sem sækja á krefst vörurakningu eru lokuð lotu-eða raðnúmer sem geymd eru í pickable-hólfum undanskilin pickable-magninu.

Ef pickable-magnið er frábrugðið magninu í pickable-hólfum gæti það verið vandamál. Skoða hólfainnihald til að finna læst hólf eða magn í virkum skjölum.

 **Magnið í reitnum vöruhús**  sýnir heildarmagn sem þú finnur í vöruhúsinu ef þú gerir efnislega talningu. Hægt er að kafa niður í vöruhúsafærslurnar úr þessum reit. Ef reiturinn sýnir magn sem er minna en magnið í  **Pickable-hólfum** er misröðun milli vöruhúss og birgðamagns. Í því tilviki skal nota  **aðgerðina reikna Leiðréttingarvöruhluta**  á  **síðunni birgðabókar**  og stofna síðan vöruhúsakínslu aftur.

Eftirfarandi mynd sýnir hámarksmagn sem tekið er með í tiltekt.

:::image type="content" source="../media/pickable-qty.png" alt-text="Hámarksmagn sem talið er tiltekt á.":::

**Þjóðsaga**

|Stafur  |Heimildasamstæða  |
|---------|---------|
|T     |Hólf með efni af gerðinni Pick         |
|D     |Hólf með efni af gerðinni tiltekt merkt sem hollur hólmur        |
|A     |Hólf með efni af gerðinni tínsla í virku skjölunum (eins og önnur tínsla)       |
|T     |Hólf með efni af gerðinni tínsla með vörum með læstum rakningu         |
|Á     |Hólf með efni af gerðinni velja með lokaða hreyfingu á útleið         |
|O     |Önnur hólf         |

### Bókanir

Ef til er Frátekning á vörunni sem verið er að taka til er útreikningur heldur áfram. Hugmyndin er að frátekt eftirspurn hafi hærri forgang en það sem er ekki frátekið, sem þýðir að tiltekt fyrir eftirspurn án frátekna ætti ekki að koma í veg fyrir tiltekt vegna frátekna eftirspurnar síðar.

Til að sannreyna að magnið geti náð yfir eftirspurn er hægt að bera saman  **pickable-magn.** gildi á  **upplýsingakassa samantektar**  með gildinu í  **reitnum Magn til afgreiðslu (stofn)**  í línunum.

Hægt er að finna frátekningar í  **reitnum Samtals frátekið magn í vöruhúsi** . Frátekið magn sem þegar er valið og er tilbúið til afhendingar, notkunar eða notkunar, hefur ekki áhrif á framboð.  **Svæðið frátekið magn í reitnum velja/sendist hólf**  sýnir þetta magn.

 **Reiturinn Magn án afhendingar í hólfi**  fyrir utan afhendingu sýnir magnið sem er tiltækt, að undanskildum magni sem eftirfarandi gildir:

* Þau eru þegar tekin til afhendingar.
* Þeir eru í læstum vörulotum eða raðnúmerum.
* Þeir eru í læstum hólfum.

Þetta magn gæti verið tiltækt en ekki væri hægt að tína þau enn. Þeir gætu enn fremur verið á móttöku-, geymslu-eða gæðatryggingarsvæðum. Hægt er að flytja þau á tiltektarsvæðið með því að vinna úr vinnublaði frágangs eða hreyfinga.

Mismunurinn  **á. magn, fyrir utan afhendingarhólf**  og frátekið magn í vöruhúsi, er það magn sem er tiltækt til tiltektar án þess að það hafi áhrif á frátekta birgðir.

### Aðrar upplýsingar

Ef vörur þurfa vörurakningu er einnig hægt að finna magnið í læstum lotum eða raðnúmerum, sem veldur eftirfarandi lækkun:

* Pickable-magnið
* Tiltækt magn, að undanskildum sendingarhólfinu
* Frátekið magn í vöruhúsi 

Ef sama atriðið er valið fyrir mörg upprunaskjöl eða línur sem einnig eru raunin þegar raðnúmer eru sótt birtast upplýsingar um tínslur í öðrum línum þar sem það dregur úr pickable-magninu.