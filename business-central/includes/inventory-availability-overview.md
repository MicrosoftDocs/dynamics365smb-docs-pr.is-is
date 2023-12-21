---
author: brentholtorf
ms.topic: include
ms.date: 09/11/2023
ms.author: bholtorf
---

Auktu skilvirkni í vöruhúsi þínu með nákvæmum rauntímaupplýsingum um þætti sem geta haft áhrif á tiltækt magn. Dæmi: 

* Birgðastig
* Staðsetningar
* Vinnslustig
* Hlutir í sóttkví
* Bókanir

Þú getur nálgast upplýsingar um framboð á hlutum úr eftirfarandi upprunaskjölum:

* Sölupantanir
* Framleiðslupantanir
* Samkomulög
* Verk

Upplýsingarnar virða einnig aðra þætti sem hafa áhrif á framboð. Til dæmis sérstakar bakkar, læstar bakkar og hlutir sem ekki er hægt að tína. Til dæmis gætu hlutir verið fráteknir eða beðið eftir flutningi eða sendingu. Síðan **Velja samantekt**  gerir þér kleift að fara yfir atriðin sem [!INCLUDE [prod_short](prod_short.md)] ekki voru með í valsskjölum og grípa til nauðsynlegra aðgerða.

> [!NOTE]
> Þessi möguleiki krefst þess að þú kveikir á **Bein frágangi og Velja** rofi fyrir staðsetningarnar sem þú notar í tínsluferlinu þínu.

### <a name="set-up-previews"></a>Settu upp forsýningar

Til að fá upplýsingar um hvað er verið að velja og hvað ekki skaltu kveikja á **Sýna samantekt (bein frágangi og vali)** kveikja á **Whse.-Source - Búa til skjal** eða **Whse.-Shipment - Búa til Pick** beiðnisíður.

### <a name="determine-the-quantity-you-can-pick"></a>Ákveðið magnið sem þú getur valið

Á línum á  **Create Warehouse Pick Summary** síðunni er **Magn. to Handle (Base)** reiturinn sýnir hvaða og hversu mörg atriði [!INCLUDE [prod_short](prod_short.md)] reyndu að velja.  **Samantekt** Staðreyndakassinn veitir frekari upplýsingar.

Fyrir einfaldar rannsóknir gæti **valanlegt magn.**  gefið þér nægar upplýsingar. Reiturinn sýnir hversu margir hlutir eru tiltækir. Ef magn sem hægt er að velja er minna en búist var við, skoðaðu innihald tunnunnar.

 **Tilvalanlegt magn.** er hámarksmagnið sem [!INCLUDE [prod_short](prod_short.md)] getur tekið til greina við tínslu. Þetta magn samanstendur af hlutum í valinn tunnur. Magnið útilokar magn sem er í læstum eða sérstökum hólfum, eða vörur sem verið er að tína í vöruhústínsluskjölum. Ef hluturinn sem þú vilt velja krefst vörurakningar, eru læst lotu- eða raðnúmer sem eru geymd í valinn hólfum útilokuð frá valanlegu magni.

Ef tínanlegt magn er frábrugðið magninu í tínslutunnunum gæti verið vandamál. Skoðaðu hólfainnihaldið til að finna læst tunnur eða magn í virkum skjölum.

Reiturinn **Magn í vöruhúsi**  sýnir heildarmagnið sem þú finnur í vöruhúsinu þínu ef þú gerir líkamlega talningu. Hægt er að grafa niður í vöruhúsabókarfærslur úr þessum reit. Ef reiturinn sýnir magn sem er minna en magnið í **Magni í valanlegum hólfum**, er misskipting milli vöruhúss og birgðamagns. Í því tilviki skaltu nota **Reikna vöruhúsaleiðréttingu** aðgerðina á  **Vörubók** síðunni og búa síðan til vöruhúsatínsluna aftur.

Eftirfarandi mynd sýnir hámarksmagn sem tekið er til greina við tínslu.

:::image type="content" source="../media/pickable-qty.png" alt-text="Hámarksmagn sem kemur til greina við tínslu.":::

**Goðsögn**

|Stafur  |Heimildasamstæða  |
|---------|---------|
|T     |Bakkar með innihaldi af gerðinni Pick         |
|D     |Bakkar með innihaldi af gerðinni Velja merktar sem sérstakar bakkar        |
|A     |Bakkar með efni af gerðinni Velja í virku skjölunum (eins og annað val)       |
|T     |Bakkar með innihaldi af gerðinni Velja með hlutum með læstri rakningu         |
|Á     |Bakkar með innihaldi af gerðinni Velja með læstri útleið         |
|O     |Aðrar ruslar         |

### <a name="reservations"></a>Bókanir

Ef fyrirvarar eru fyrir vöruna sem verið er að velja heldur útreikningurinn áfram. Hugmyndin er sú að frátekin eftirspurn hafi meiri forgang en ekki frátekin, sem þýðir að tínsla fyrir óátekna eftirspurn ætti ekki að koma í veg fyrir tínslu fyrir frátekna eftirspurn síðar.

Til að ganga úr skugga um að magnið þitt geti staðið undir eftirspurn skaltu bera saman **valanlegt magn.** gildi í **yfirliti** staðreyndakassi gildi í **Magni. að meðhöndla (Base)** reit á línunum.

Þú getur fundið pantanir í **Heildar fráteknu magni. á vöruhúsi** reitnum. Frátekið magn sem þegar er tínt og tilbúið til sendingar, notkunar eða neyslu hefur ekki áhrif á framboð.  **Frátekið magn. í Pick/Ship Bins** reitnum sýnir þetta magn.

The **Gegn. Magn. Að undanskildum sendingarhólfi** reiturinn sýnir magnið sem er tiltækt, að undanskildum magni þar sem eftirfarandi á við:

* Þeir eru þegar valdir til sendingar.
* Þau eru í lokuðum hlutum eða raðnúmerum.
* Þeir eru í lokuðum tunnum.

Þetta magn gæti verið tiltækt, en þú gætir ekki valið þau ennþá. Þeir gætu samt verið á móttöku-, geymslu- eða gæðatryggingarsvæðum. Hægt er að færa þau á tínslusvæðið með því að vinna frágangs- eða hreyfiblaði.

Munurinn á **Avail. Magn. Að frátöldum sendingarhólfi** og fráteknu magni í vöruhúsi er það magn sem er tiltækt til tínslu án þess að hafa áhrif á frátekið lager.

### <a name="other-details"></a>Aðrar upplýsingar

Ef vörur krefjast vörurakningar geturðu einnig fundið magnið í læstum hlutum eða raðnúmerum, sem veldur eftirfarandi lækkunum:

* Magnið sem hægt er að velja
* Tiltækt magn, fyrir utan sendingartunnuna
* Frátekið magn í vöruhúsi 

Ef þú velur sama hlutinn fyrir mörg upprunaskjöl eða línur, sem er einnig raunin þegar þú velur raðnúmer, birtast upplýsingar um tiltektir fyrir aðrar línur einnig vegna þess að það dregur úr magni sem hægt er að velja.
