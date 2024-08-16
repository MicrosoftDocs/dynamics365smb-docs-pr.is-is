---
title: 'Upplýsingar um hönnun - flæði fyrir framleiðslu, samsetningu og verkefni'
description: 'Fræðast um flæðið milli hólfa fyrir tínslu íhluta og frágang lokavara fyrir samsetningar-, framleiðslu- eða verkefnispantanir.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/12/2024
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-projects"></a>Flæði fyrir framleiðslu, samsetningu og verkefni

Innra flæði, svo sem tínsluíhlutir og frágangur lokavara fyrir samsetningar-, verk- og framleiðslupantanir, er svipað og flæði á inn- eða útleið. Margar vinnslurnar kunna að þekkja. Í þessari grein eru upplýsingar um hvernig á að vinna með vöruhúsaflæði innanhúss með mismunandi flóknari stigum.

## <a name="overview-of-different-configuration-options"></a>Yfirlit yfir mismunandi skilgreiningarvalkosti

Hægt er að grunnstilla vöruhúsaaðgerðir á ýmsa vegu. Mikilvægt er að valkostirnir sem notandi velur endurbæti ferla án þess að valda sameiginlegum kostnaði. Eftirfarandi töflur lýsa dæmigerðum grunnstillingum fyrir stjórnun efnislegra vara fyrir framleiðslu, verkefni og samsetningarpantanir.

### <a name="inbound-flow-put-away"></a>Flæði á innleið (frágangur)

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Innleiðarflæði framleiðslupöntunar|Samsetningarflæði á innleið|Innleiðarflæði verka|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjáls. Hólfakótanum er stýrt **áskilin** .|Framleiðslubók -> Frálagsbók</br><br/> **ATHUGIÐ**: Hægt er að bóka frálag með **Framleiðslubók**.|Samsetningarpöntun|Frágangur á ekki við um verkefni|  
|Grunnatriði|Pöntun fyrir hverja pöntun.|Meðhöndlun framleiðslufrálags vöruhúss: Birgðafrágangur. </br><br/> **ATH**: Samt er hægt að bóka frálag beint úr upprunaskjölunum í birgðageymslum þar sem þessar stillingar var virkjuð. |Valfrjáls. Hólfakótanum er stýrt **áskilin** .|Framleiðslupöntun -> Birgðafrágangur|Samsetningarpöntun|Frágangur á ekki við um verkefni|
|Ítarlegt|Sameinaðar frágangsaðgerðir fyrir mörg upprunaskjöl.|Engar sérstaktar stillingar|Valfrjáls. Hólfakótanum er stýrt **áskilin** .|Framleiðslupantanir -> Frálagsbók|Samsetningarpantanir -> innri hreyfingar | Frágangur á ekki við um verkefni|
|Ítarlegt|Sama og að ofan plús beinar tínslu-/frágangsaðgerðir|Bein tínsla og frágangur (ósjálfstæð vígblöð eru gerð virk sjálfvirkt)|Áskilið|Sama og hér að ofan|Sama og hér að ofan| Frágangur á ekki við um verkefni|

Sumar grunnstillingar leyfa ekki notkun sérsniðinna vöruhúsaskjala til að skrá frágang. Ef hins vegar hólf eru notuð í birgðageymslunni er hægt að nota almenn hreyfingaskjöl til að færa framleiddar eða samsettar vörur í vöruhús. Nánari upplýsingar um flutning á [vörum](warehouse-move-items.md).

### <a name="outbound-flow-pick"></a>Flæði á útleið (tínsla)

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Útleiðarflæði framleiðslupöntunar|Samsetningarflæði á útleið|Verkflæði á útleið|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjáls. Hólfakótanum er stýrt **áskilin** .|Framleiðslubók -> notkunarbók </br><br/> **ATHUGIÐ**: Hægt er að bóka notkun með **framleiðslubók**.|Samsetningarpöntun|Verk - > verkbók|  
|Grunnatriði|Pöntun fyrir hverja pöntun.|Framleiðsla, Samsetning, Verkefni: Birgðatínsla, Birgðahreyfing </br><br/> **ATH**: Enn er hægt að bóka notkun beint úr upprunaskjölum í birgðageymslum þar sem þessar stillingar var virkjuð.|Valfrjáls. Hólfakótanum er stýrt **áskilin** .|Framleiðslupöntun -> Birgðatínsla|Samsetningarpöntun -> Birgðahreyfing</br><br/> **Aðeins er hægt að nota Birgðahreyfinguna** með hólfum.|Verk - > Birgðatínsla|
|Ítarlegt|Sameinaðar tínsluaðgerðir fyrir mörg upprunaskjöl.|Framleiðsla, Samsetning, Verkefni: Vöruhúsatínsla|Valfrjáls. Hólfakótanum er stýrt áskilin vífæra|Framleiðslupantanir -> vöruhúsatínslu - > Notkunarbók |Samsetningarpantanir -> vöruhúsatínslu| Verkefni -> vöruhúsatínsla - > Verkbók |
|Ítarlegt|Sama og að ofan + Beinar tínslu-/frágangsaðgerðir|Bein tínsla og frágangur (ósjálfstæð vígblöð eru gerð virk sjálfvirkt)|Áskilið|Sama og hér að ofan|Sama og hér að ofan| Bein tínsla og frágangur er ekki studdur fyrir verkefni|

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Vöruhús án sérsniðinnar vöruhúsaaðgerðar

Jafnvel þó ekki séu notaðar sértækar vöruhúsaaðgerðir gæti verið gott að rekja hluti eins og notkun og framleiðslufrálag. Eftirfarandi greinar veita upplýsingar um hvernig á að vinna móttökur fyrir upprunaskjöl.

* [Skrá notkun og frálag fyrir eina línu útgefinnar framleiðslupöntunar](production-how-to-register-consumption-and-output.md)
* [Sameina vörur](assembly-how-to-assemble-items.md)
* [Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Grunnskilgreining vöruhúss

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Flæðir til og frá framleiðslu í einfaldri vöruhúsaskilgreiningu

Inn- og útleiðarflæðið í einfaldri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir flæði á innleið (frágangi) í reitnum **Vöruh. frálagsreitur – Vöruh. Meðhöndlunarreitur** er birgðafrágangur **valinn**.
* Fyrir útleiðarflæðið (tínsluna) í reitnum **Vörunotkunarh. Meðhöndlun** er birgðatínsla/hreyfing **valin**.

Nota **birgðatínsluskjöl** til að tína framleiðsluíhluti í flæðinu til framleiðslu. Til að ganga frá vörum sem eru framleiddar skal nota **Birgðafrágangsskjöl** .

Í birgðageymslum þar sem hólf eru notuð eru birgðahreyfingaskjöl sérstaklega gagnleg fyrir birgðaskráningu íhluta. Nánari upplýsingar um hvernig íhlutanotkun er birgðaskráð úr Verkefnaframleiðslu eða Opnum vinnusalarhólfum er farið [í Birgðaskráning framleiðsluíhluta í vöruhúsinu](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Birgðahreyfingar eru mikilvæg skjöl ef tínsla + Framvirk **eða** Tínsla + Afturvirk **birgðaskráningaraðferðir eru notaðar** . Fræðast meira um [birgðaskráningaraðferðir](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Reitirnir **Hólfkóti** verkstæðisframleiðslu, **Hólfakóti** frá-framleiðslu og **Opna hólfakóta** vinnusalar á birgðageymslunni eða véla-/vinnustöðin skilgreina sjálfgefið flæði til og frá framleiðslusvæðum.
* Vinna með hreyfingu framleiddra vara á síðunni **Innri hreyfing** án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Flæðir til og frá samsetningu í einfaldri vöruhúsaskilgreiningu

Útleiðarflæðið í einfaldri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir útleiðarflæðið (tínsluna) í reitnum **Asm. Vöruh. notkunar vöruhúss Meðhöndlunarreitur** er Birgðahreyfing **valin**.

Nota **skjöl birgðahreyfingar** til að tína samsetningaríhluti í flæði til samsetningar. Bóka samsetningarafköst og notkun beint úr samsetningarpöntun.

> [!NOTE]
> **Birgðatínsla** og **Birgðafrágangsskjöl** eru ekki studd samsetningarpöntunum.

Í birgðageymslum sem nota hólf:

* Nota **skjöl birgðahreyfingar** til að færa samsetningaríhluti í samsetningarsvæðið.
* Reitirnir **Kóti** samsetningarhólfs, **Kóti** frá-samsetningarhólfs á birgðageymsluspjaldinu skilgreina sjálfgefin flæði til og frá samsetningarsvæðum.
* Vinna með hreyfingu samsettra vara á síðunni **Innri hreyfing**, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningarflæði til lagerbirgða og samsetningarflæði til pöntunar saman. Nánari upplýsingar um [hvernig á að skilja samsetningu pöntunar og setja saman á lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). Í tengslum við vöruhúsakerfi er samsetning til birgða hluti af innra vöruhúsaflæðinu og samsetning til pöntunar er í vöruhúsaflæði út. Fræðast meira um [samsetningarvörur í pöntun með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flæði fyrir verkefnastjórnun í einfaldri vöruhúsaskilgreiningu

Útleiðarflæðið í einfaldri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir útleiðarflæðið (tínslu) í reitnum **Notkunarflæði verks Meðhöndlunarreitur** er Birgðatínsla **valin**.

Nota birgðatínsluskjöl **til** að tína verkíhluti í flæðinu til verkefnastjórnunar.

Í birgðageymslu sem notar hólf skilgreinir reiturinn **Hólfakóti** verkefnis í birgðageymslunni sjálfgefið flæði til verkefnastjórnunar.

## <a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flæðir til og frá framleiðslu í ítarlegri vöruhúsaskilgreiningu

Flæði á útleið í ítarlegri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir útleiðarflæðið (tínsluna) í reitnum **Vörunotkunarh. Meðhöndlun** er vöruhúsatínsla **(valfrjálst)** eða **Vöruhúsatínsla (áskilin)**.

Nota skal skjöl vöruhúsatínslu **og** síðuna **Tínsluvinnublað** til að tína íhluti fyrir framleiðslu.

> [!NOTE]
> **Vöruhúsafrágangsskjöl** eru ekki studd fyrir frálag framleiðslu.

Í birgðageymslum sem nota hólf:

* **Vöruhúsahreyfingaskjöl** og **síðan Vinnublað** hreyfinga eru sérstaklega gagnleg fyrir birgðaskráningu íhluta. Fræðast meira um [birgðaskráningu framleiðsluíhluta í vöruhúsinu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
*  **Kóti** verkefnahólfs, **Kóti** frá-framleiðsluhólfs og **Kóti opins hólfs** vinnusalar á birgðageymslunni eða véla-/vinnustöðinni skilgreina sjálfgefnu flæðin til og frá framleiðslusvæðum. 
* Vinna með hreyfingar á framleiddum vörum á **hreyfingavinnublaðinu eða** Vöruhúsamóttökunni **. Innanhússfrágangssíður**, án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Flæðir til og frá samsetningu í ítarlegum vöruhúsaskilgreiningum

Flæði á útleið í ítarlegri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir útleiðarflæðið (tínsluna) í reitnum **Asm. Vöruh. notkunar vöruhúss Meðhöndlun** er vöruhúsatínsla **(valfrjálst)** eða **Vöruhúsatínsla (áskilin)**. 

Nota **vöruhúsatínsluskjöl** og síðuna **Tínsluvinnublað** til að tína íhluti fyrir samsetningu.

> [!NOTE]
> **Vöruhúsafrágangsskjalið** er ekki stutt fyrir samsetningarpantanir.

Í birgðageymslum sem nota hólf:

* Reitirnir **Kóti** samsetningarhólfs og **Kóti frá-samsetningarhólfs** í birgðageymslunni skilgreina sjálfgefið flæði til og frá samsetningarsvæðum.
* Vinna með hreyfingu samsetningarvara á **hreyfingavinnublaðinu** eða **Vöruhúsalínunni. Innanhússfrágangssíður**, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningarflæði til lagerbirgða og samsetningarflæði til pöntunar saman. Nánari upplýsingar um [hvernig á að skilja samsetningu pöntunar og setja saman á lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Samsetning til lager er hluti af innra vöruhúsaflæðinu og samsetning-til-pöntun er í vöruhúsaflæði út. Fræðast meira um [vöru með samsetningu á pöntun í vöruhúsaafhendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Flæðir í verkefnastjórnun í ítarlegri vöruhúsaskilgreiningu

Flæði á útleið í ítarlegri vöruhúsagrunnstillingu felur í sér eftirfarandi stillingar á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna:

* Fyrir útleiðarflæðið (tínslu) í reitnum **Notkunarflæði verks Meðhöndlun** er vöruhúsatínsla **(valfrjálst)** eða **Vöruhúsatínsla (áskilin)**.

Nota **vöruhúsatínsluskjöl** og síðuna **Tínsluvinnublað** til að tína íhluti í flæðinu til verkefnastjórnunar.

Í birgðageymslum sem nota hólf tilgreinir reiturinn **Hólfakóti** verkefnis í birgðageymslunni sjálfgefið flæði yfir á verksvæðið.

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
