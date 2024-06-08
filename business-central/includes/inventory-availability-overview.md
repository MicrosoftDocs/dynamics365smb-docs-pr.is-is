---
author: brentholtorf
ms.topic: include
ms.date: 04/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Auka skilvirkni í vöruhúsinu með nákvæmum og nákvæmum upplýsingum um þætti sem geta haft áhrif á tiltækt magn. Dæmi: 

* Birgðastig
* Staðsetningar
* Vinnsluþrep
* Biðgeymsluvörur
* Bókanir

Hægt er að nálgast upplýsingar um vörur til ráðstöfunar úr eftirfarandi upprunaskjölum:

* Sölupantanir
* Framleiðslupantanir
* Samsetningarpantanir
* Verk

Upplýsingarnar varða einnig aðra þætti sem hafa áhrif á ráðstöfunarmagn. Til dæmis sérstakt hólf, læst hólf og vörur sem ekki eru tiltækar til tínslu. Til dæmis er hægt að taka vörur frá eða bíða frágangs- eða afhendingaraðgerða. Síðan **Tínsluyfirlit** gerir kleift að fara yfir vörurnar sem [!INCLUDE [prod_short](prod_short.md)] ekki voru með í tínsluskjölum og framkvæma nauðsynlegar aðgerðir.

> [!NOTE]
> Þessi möguleiki krefst þess að kveikt sé á **vífærinu Beinn frágangur og tínsla** fyrir birgðageymslurnar sem notaðar eru í tínsluferlinu.

### <a name="set-up-previews"></a>Setja upp forskoðun

Til að fá upplýsingar um hvað er verið að tína og hvað ekki skal kveikja á **Sýna samantekt (beinn frágangur og tínsla)** víxla á beiðnisíðunum **Vöruhús - Stofna fylgiskjal** eða **Vöruhúsaafhendingu - Stofna tínslubeiðnisíður** .

### <a name="determine-the-quantity-you-can-pick"></a>Ákveða magnið sem hægt er að tína

Í línum á síðunni **Stofna yfirlit vöruhúsatínslu sýnir reiturinn** Magn til afgreiðslu (stofn) **hvaða og hversu margar vörur** reyndu að tína. [!INCLUDE [prod_short](prod_short.md)]  Upplýsingakassinn **samantektar** veitir nánari upplýsingar.

Til einfaldrar rannsóknar ræðst **Tiltekið magn** nægilegar upplýsingar gefnar. Í reitnum sést hversu margar vörur eru til ráðstöfunar. Ef tínslumagnið er lægra en búist var við er hólfainnihaldið skoðað.

Reiturinn **Tínt magn** er hámarksmagnið sem [!INCLUDE [prod_short](prod_short.md)] tekið er tillit til til tínslu. Þetta magn samanstendur af vörum í tínsluhólfum. Magnið undanskilur magnið sem er í lokað eða sérstakt hólf eða vörur sem verið er að tína í vöruhúsatínsluskjölum. Ef varan sem á að tína krefst vörurakningar eru lokuð lotu- eða raðnúmer sem geymd eru í tínsluhólfum undanskilin frá tínslumagninu.

Ef tínslumagnið er frábrugðið magninu í tínsluhólfum gæti komið upp vandamál. Skoða innihald hólfs til að finna lokuð hólf eða magn í virkum fylgiskjölum.

Reiturinn **Magn í vöruhúsi** sýnir heildarmagnið sem er að finna í vöruhúsinu ef talning raunbirgða er talin. Hægt er að kafa niður í vöruhúsafærslurnar úr þessum reit. Ef reiturinn sýnir minna magn en magnið í magninu **í tínsluhólfum** er misræmi milli vöruhúss og birgðamagns. Í því tilviki skal nota aðgerðina **Reikna vöruhúsaleiðréttingu** á síðunni **Birgðabók** og stofna síðan vöruhúsatínsluna aftur.

Eftirfarandi mynd sýnir hámarksmagn sem tekið er til tínslu.

:::image type="content" source="../media/pickable-qty.png" alt-text="Hámarksmagn sem tekið er til tínslu.":::

**Þjóðsaga**

|Stafur  |Heimildasamstæða  |
|---------|---------|
|T     |Hólf með innihald tegundarinnar Tína         |
|D     |Hólf með innihald tegundarinnar Tína merkt sem Sérstök hólf        |
|A     |Hólf með innihald tegundarinnar Tína í virku skjölunum (líkt og önnur tínsla)       |
|T     |Hólf með innihald tegundarinnar Tína með vörum með rakningu sem er lokuð         |
|Á     |Hólf með innihald tegundarinnar Tína með lokaðri hreyfingu á útleið         |
|O     |Önnur hólf         |

### <a name="reservations"></a>Bókanir

Ef tekið er frá fyrir vöruna sem verið er að tína heldur útreikningurinn áfram. Hugmyndin er sú að frátekin eftirspurn hafi meiri forgang en ekki var tekin frá, sem þýðir að tínsla fyrir ófrátekna eftirspurn ætti ekki að koma í veg fyrir að tínt sé fyrir frátekna eftirspurn síðar.

Til að staðfesta að magnið nái yfir eftirspurn er reiturinn **Tínt magn bera saman.**  **í samantektaruppl** . með gildinu í reitnum **Magn til afgreiðslu (stofn)** í línunum.

Finna má frátekningar í reitnum **Heildarmagn frátekið í vöruhúsi** . Frátekið magn sem þegar hefur verið tínt og er tilbúið til afhendingar, notkunar eða notkunar, hefur ekki áhrif á tiltækileika. Reiturinn **Frátekið magn í tínslu-/afhendingarhólfum** sýnir þetta magn.

Reiturinn **Til ráðst. magn án afhendingarhólfs** sýnir tiltækt magn, að frádregnu magni sem eftirfarandi á við:

* Þeir eru þegar tíndir fyrir sendingar.
* Þau eru í lokuðum vörulotum eða raðnúmerum.
* Þau eru í lokuðum hólfum.
* Þau eru í hollum hólfum.

Þetta magn getur verið tiltækt en hugsanlega er ekki hægt að tína það ennþá. Þau geta enn verið á móttöku-, geymslu- eða gæðaeftirlitssvæðum. Hægt er að færa þær á tínslusvæðið með því að vinna vinnublað frágangs eða hreyfingar.

Mismunurinn á magni **til ráðst. án afhendingarhólfs** og frátekins magns í vöruhúsi er magnið sem er tiltækt til tínslu án þess að hafa áhrif á fráteknar birgðir.

Eftirfarandi sökkli sýnir úthlutun á hæfilegu magni fyrir frátekna sýkingu.

:::image type="content" source="../media/Warehouse_Reservation_Pick.png" alt-text="Hámarksmagn sem tekið er tillit til tiltektar þegar um er að ræða frátekningu.":::

**Þjóðsaga**

|Stafur  |Heimildasamstæða  |
|---------|---------|
|T     |Magn sem á að tína         |
|TR    |Samtals frátekið magn í vöruhúsi.         |
|RS    |Frátekið magn sem þegar hefur verið tínt og er tilbúið til afhendingar, notkunar eða notkunar       |
|A     |Tilt. magn fyrir utan afhendingarhólf         |
|Á     |Magn í sérstökum eða lokuðum hólfum, lokuðum vörulotum eða raðnúmerum         |

Þó að nægt tiltækt magn sé í vöruhúsi til að fullnægja tínslunni að fullu leiðir það til þess að fráteknu heildarmagni er úthlutað á móti magninu í sérstökum eða lokuðum hólfum, sem hindrar tínslu á þessari eftirspurn. Þar sem frátekin eftirspurn hefur meiri forgang minnkar [!INCLUDE [prod_short](prod_short.md)]  magnið sem á að tína til að koma í veg fyrir neikvæð áhrif, svo sem vanhæfni til tínslu, á frátekna eftirspurn.

### <a name="other-details"></a>Aðrar upplýsingar

Ef vörur krefjast vörurakningar er einnig hægt að finna magnið í lokuðum lotum eða raðnúmerum sem veldur eftirfarandi lækkun:

* Tiltekið magn
* Tiltækt magn, að afhendingarhólfi undanskildum
* Frátekið magn í vöruhúsi 

Ef sama varan er tínd fyrir mörg upprunaskjöl eða línur, sem er einnig raunin þegar raðnúmer eru tínd, birtast upplýsingar um tínslur fyrir aðrar línur einnig þar sem það minnkar tínslumagnið.
