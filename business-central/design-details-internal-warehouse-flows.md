---
title: 'Upplýsingar um hönnun - Flæði fyrir framleiðslu, samsetningu og verk'
description: 'Fræðast um flæðið milli hólfa fyrir tínslu íhluta og frágang lokavara fyrir samsetningar-, framleiðslu- eða verkpantanir.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 02/05/2024
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs"></a>Flæði fyrir framleiðslu, samsetningu og verk

Innra flæði, svo sem tínsluíhlutir og frágangur lokavara fyrir samsetningar-, verk- og framleiðslupantanir, er svipað og flæði á inn- eða útleið. Margar ferlanna kunnuglega. Í þessari grein eru upplýsingar um hvernig á að vinna með vöruhúsaflæði innanhúss með mismunandi flóknari stigum.

## <a name="overview-of-different-configuration-options"></a>Yfirlit yfir mismunandi skilgreiningarvalkosti

Hægt er að grunnstilla vöruhúsaaðgerðir á ýmsa vegu. Mikilvægt er að valkostirnir sem notandi velur endurbæti ferla án þess að valda sameiginlegum kostnaði. Eftirfarandi töflur lýsa dæmigerðum grunnstillingum til að vinna með efnislegar vörur fyrir framleiðslu, verk og samsetningarpantanir.

### <a name="inbound-flow-put-away"></a>Flæði á innleið (frágangur)

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Innleiðarflæði framleiðslupöntunar|Samsetningarflæði á innleið|Verkflæði á innleið|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjálst. Hólfakótanum er stýrt **áskilin** .|Framleiðslubók -> Frálagsbók</br><br/> **ATHUGIÐ**: Hægt er að bóka frálag með **Framleiðslubók**.|Samsetningarpöntun|Frágangur á ekki við um verk|  
|Grunnatriði|Pöntun fyrir hverja pöntun.|Krefjast frágangs. </br><br/> **ATHUGIÐ**: Þó að stillingin sé kölluð **Krefjast frágangs** er samt hægt að bóka frálag úr upprunaskjölum í birgðageymslum þar sem þessi gátreitur er valinn. |Valfrjálst. Hólfakótanum er stýrt **áskilin** .|Framleiðslupöntun -> Birgðafrágangur|Samsetningarpöntun|Frágangur á ekki við um verk|
|Ítarlegt|Sameinaðar frágangsaðgerðir fyrir mörg upprunaskjöl.|Krefjast móttöku + Krefjast frágangs|Valfrjálst. Hólfakótanum er stýrt **áskilin** .|Framleiðslupantanir -> Frálagsbók|Samsetningarpantanir -> innri hreyfingar | Frágangur á ekki við um verk|
|Ítarlegt|Sama og að ofan + Beinar tínslu-/frágangsaðgerðir|Bein tínsla og frágangur (ósjálfstæð vígblöð verða gerð virk sjálfvirkt)|Áskilið|Sama og hér að ofan|Sama og hér að ofan| Frágangur á ekki við um verk|

Sumar grunnstillingar leyfa ekki notkun sérsniðinna vöruhúsaskjala til að skrá frágang. Ef hins vegar hólf eru notuð í birgðageymslunni er hægt að nota almenn hreyfingaskjöl til að færa framleiddar eða samsettar vörur í vöruhús. Fá nánari upplýsingar um [hvernig á að færa vörur innri vinnslu í einfaldri vöruhúsagrunnstillingu](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick"></a>Flæði á útleið (tínsla)

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Útleiðarflæði framleiðslupöntunar|Samsetningarflæði á útleið|Verkflæði á útleið|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjálst. Hólfakótanum er stýrt **áskilin** .|Framleiðslubók -> notkunarbók </br><br/> **ATHUGIÐ**: Hægt er að bóka notkun með **framleiðslubók**.|Samsetningarpöntun|Verk - > verkbók|  
|Grunnatriði|Pöntun fyrir hverja pöntun.|Krefjast tínslu. </br><br/> **ATHUGIÐ**: Þó að stillingin sé kölluð **Krefjast tínslu** er samt hægt að bóka frálag úr upprunaskjölum í birgðageymslum þar sem þessi gátreitur er valinn. <!-- ToDo Test prod output-->|Valfrjálst. Hólfakótanum er stýrt **áskilin** .|Framleiðslupöntun -> Birgðatínsla|Samsetningarpöntun -> Birgðahreyfing</br><br/> **Aðeins er hægt að nota Birgðahreyfinguna** með hólfum.|Verk - > Birgðatínsla|
|Ítarlegt|Sameinaðar tínsluaðgerðir fyrir mörg upprunaskjöl.|Krefjast afhendingar + Krefjast tínslu|Valfrjálst. Hólfakótanum er stýrt áskilin vífæra|Framleiðslupantanir -> vöruhúsatínslu - > Notkunarbók |Samsetningarpantanir -> vöruhúsatínslu| Verk - > vöruhúsatínsla - > verkbók |
|Ítarlegt|Sama og að ofan + Beinar tínslu-/frágangsaðgerðir|Bein tínsla og frágangur (ósjálfstæð vígblöð verða gerð virk sjálfvirkt)|Áskilið|Sama og hér að ofan|Sama og hér að ofan| Bein tínsla og frágangur er ekki studdur fyrir verk|

Svipað og í innleiðarflæðinu leyfa sumar grunnstillingar ekki að nota sérstök vöruhúsaskjöl til að skrá frágang. Ef hólf eru notuð í birgðageymslunni er hægt að nota almenn hreyfingaskjöl til að færa framleiddar eða samsettar vörur. Nánari upplýsingar um flutning á [vörum](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Vöruhús án sérsniðinnar vöruhúsaaðgerðar

Jafnvel þó ekki séu til sérstakt vöruhúsaaðgerðir er líklegast ráðlegt að fylgjast með hlutum eins og notkun og framleiðslufrálagi. Eftirfarandi greinar veita upplýsingar um hvernig á að vinna móttökur fyrir upprunaskjöl.

* [Skrá notkun og frálag fyrir eina línu útgefinnar framleiðslupöntunar](production-how-to-register-consumption-and-output.md)
* [Sameina vörur](assembly-how-to-assemble-items.md)
* [Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Grunnskilgreining vöruhúss

Inn- og útleiðarflæðið í einfaldri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir flæði á innleið (frágang) er kveikt á vífærinu **Krefjast frágangs** en slökkt er á vífærinu **Krefjast móttöku** .
* Fyrir útleiðarflæðið (tínslu) skal kveikja á vífærinu **Krefjast tínslu** en slökkva á vífærinu **Krefjast afhendingar** .

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Flæðir til og frá framleiðslu í einfaldri vöruhúsaskilgreiningu

Nota **birgðatínsluskjöl** til að tína framleiðsluíhluti í flæðinu til framleiðslu. Til að ganga frá vörum sem eru framleiddar skal nota **Birgðafrágangsskjöl** .

Í birgðageymslum þar sem hólf eru notuð eru birgðahreyfingaskjöl sérstaklega gagnleg fyrir birgðaskráningu íhluta. Nánari upplýsingar um hvernig íhlutanotkun er birgðaskráð úr Verkefnaframleiðslu eða Opnum vinnusalarhólfum er farið [í Birgðaskráning framleiðsluíhluta í vöruhúsinu](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Birgðahreyfingar eru mikilvæg skjöl ef tínsla + Framvirk **eða** Tínsla + Afturvirk **birgðaskráningaraðferðir eru notaðar** . Fræðast meira um [birgðaskráningaraðferðir](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Reitirnir **Hólfkóti** verkstæðisframleiðslu, **Hólfakóti** frá-framleiðslu og **Opna hólfakóta** vinnusalar á birgðageymslunni eða véla-/vinnustöðin skilgreina sjálfgefið flæði til og frá framleiðslusvæðum.
* Vinna með hreyfingu framleiddra vara á síðunni **Innri hreyfing** án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Flæðir til og frá samsetningu í einfaldri vöruhúsaskilgreiningu

Bóka samsetningarafköst og notkun beint úr samsetningarpöntun.

> [!NOTE]
> **Birgðatínsla** og **Birgðafrágangsskjöl** eru ekki studd samsetningarpöntunum.

Í birgðageymslum sem nota hólf:

* Nota **skjöl birgðahreyfingar** til að færa samsetningaríhluti í samsetningarsvæðið.
* Reitirnir **Kóti** samsetningarhólfs, **Kóti** frá-samsetningarhólfs á birgðageymsluspjaldinu skilgreina sjálfgefin flæði til og frá samsetningarsvæðum.
* Vinna með hreyfingu samsettra vara á síðunni **Innri hreyfing**, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningarflæði til lagerbirgða og samsetningarflæði til pöntunar saman. Nánari upplýsingar um [hvernig á að skilja samsetningu pöntunar og setja saman á lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). Í tengslum við vöruhúsakerfi er samsetning til birgða hluti af innra vöruhúsaflæðinu og samsetning til pöntunar er í vöruhúsaflæði út. Fræðast meira um [samsetningarvörur í pöntun með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flæði fyrir verkefnastjórnun í einfaldri vöruhúsaskilgreiningu

Nota **birgðatínsluskjöl** til að tína verkíhluti í flæðinu til verkefnastjórnunar.

Í birgðageymslu sem notar hólf tilgreinir reiturinn **Hólfkóti** verkefnis í birgðageymslunni sjálfgefið flæði til verkefnastjórnunar.

## <a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi

Inn- og útleiðarflæði í ítarlegri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir flæði á innleið (frágang) er kveikt á **krefjast móttöku** og **Krefjast frágangsvígslna** .
* Fyrir útleiðarflæðið (tínsluna) er kveikt á vífærslnunum **Krefjast afhendingar** og **Krefjast móttöku** .

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flæðir til og frá framleiðslu í ítarlegri vöruhúsaskilgreiningu

Nota skal skjöl vöruhúsatínslu **og** síðuna **Tínsluvinnublað** til að tína íhluti fyrir framleiðslu.

Í birgðageymslum sem nota hólf:

* **Vöruhúsahreyfingaskjöl** og **síðan Vinnublað** hreyfinga eru sérstaklega gagnleg fyrir birgðaskráningu íhluta. Fræðast meira um [birgðaskráningu framleiðsluíhluta í vöruhúsinu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
*  **Kóti** verkefnahólfs, **Kóti** frá-framleiðsluhólfs og **Kóti opins hólfs** vinnusalar á birgðageymslunni eða véla-/vinnustöðinni skilgreina sjálfgefnu flæðin til og frá framleiðslusvæðum. 
* Vinna með hreyfingar á framleiddum vörum á **hreyfingavinnublaðinu eða** Vöruhúsamóttökunni **. Innanhússfrágangssíður**, án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Flæðir til og frá samsetningu í ítarlegum vöruhúsaskilgreiningum

Nota **vöruhúsatínsluskjöl** og síðuna **Tínsluvinnublað** til að tína íhluti fyrir samsetningu.

Í birgðageymslum sem nota hólf:

* Reitirnir **Kóti** samsetningarhólfs og **Kóti frá-samsetningarhólfs** í birgðageymslunni skilgreina sjálfgefið flæði til og frá samsetningarsvæðum.
* Vinna með hreyfingu samsetningarvara á **hreyfingavinnublaðinu** eða **Vöruhúsalínunni. Innanhússfrágangssíður**, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningarflæði til lagerbirgða og samsetningarflæði til pöntunar saman. Nánari upplýsingar um [hvernig á að skilja samsetningu pöntunar og setja saman á lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Samsetning til lager er hluti af innra vöruhúsaflæðinu og samsetning-til-pöntun er í vöruhúsaflæði út. Fræðast meira um [vöru með samsetningu á pöntun í vöruhúsaafhendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Flæðir í verkefnastjórnun í ítarlegri vöruhúsaskilgreiningu

Nota **vöruhúsatínsluskjöl** og síðuna **Tínsluvinnublað** til að tína íhluti í flæðinu til verkefnastjórnunar.

Í birgðageymslum sem nota hólf tilgreinir reiturinn **Hólfakóti** verka í birgðageymslunni sjálfgefið flæði til verksvæðisins.

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
