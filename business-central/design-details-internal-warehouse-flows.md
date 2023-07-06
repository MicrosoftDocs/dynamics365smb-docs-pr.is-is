---
title: 'Upplýsingar um hönnun-flæði fyrir framleiðslu, samsetningu og vinnslur'
description: 'Upplýsingar um flæðið milli hólfa fyrir tiltektaríhluti og frágang lokaatriða fyrir samsetningar, framleiðslu eða vinnslurfyrirmæli.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs"></a><a name="flows-for-production-assembly-and-jobs"></a><a name="flows-for-production-assembly-and-jobs"></a>Flæði fyrir framleiðslu, samsetningu og vinnslur

Innra flæði, eins og tiltektaríhlutir og lokavörur til samsetningar, vinnslu og framleiðslupantana eru líkar inn-eða útstreymis. Svo gætu margir á ferlinum séð kunnuglega. Í þessari grein er að finna upplýsingar um hvernig unnið er með innra vöruhúsaflæði með ýmsum stigum flókið.

## <a name="overview-of-different-configuration-options"></a><a name="overview-of-different-configuration-options"></a><a name="overview-of-different-configuration-options"></a>Yfirlit yfir mismunandi skilgreiningarvalkosti

Hægt er að skilgreina vöruhúsaaðgerðir á ýmsa vegu. Það skiptir miklu máli að Valkostirnir sem þú velur bæta ferla þína án þess að valda rekstrarkostnaði. Eftirfarandi töflur lýsa dæmigerðum afbrigðum fyrir að eiga við efnislegar vörur fyrir framleiðslu, vinnslur og samsetningarpantanir.

### <a name="inbound-flow-put-away"></a><a name="inbound-flow-put-away"></a><a name="inbound-flow-put-away"></a>Heimstreymi (frágangur)

|Flækjustig|Description|Stillingar|Hólfkóti|Innflæði framleiðslupöntunar|Innflæðis Samsetningarpöntun|Flæði um störf á innleið|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjálst. Hólfakóta er skylda  **að**  skipta út.|Framleiðslubók-> Úttaksbók</br><br/> **Til athugunar** : Hægt er að bóka úttak með  **framleiðslubók**.|Samsetningarpöntun|Frágangur á ekki við um störf|  
|Grunnatriði|Pöntun-eftir pöntun.|Krafist frágangs. </br><br/> **Til athugunar** : þótt stillingin sé kölluð  **Krefjast frágangs** er enn hægt að bóka úttak úr upprunaskjölum á birgðageymslur þar sem gátreiturinn er valinn. |Valfrjálst. Hólfakóta er skylda  **að**  skipta út.|Framleiðslupöntun-> frágang birgða|Samsetningarpöntun|Frágangur á ekki við um störf|
|Ítarlegt|Verkþættir samsteypufrágangs fyrir mörg upprunaskjöl.|Krefjast innhreyfinga + Krefjast frágangs|Valfrjálst. Hólfakóta er skylda  **að**  skipta út.|Framl. pantanir-> Úttaksbók|Samsetningarskipanir-> innri hreyfingar | Frágangur á ekki við um störf|
|Ítarlegt|Sama og fyrir ofan + beinar frágangs/frágang frágangsverkþátta|Beinar Tínslugerð og frágangingar (háðir víxlar verða virkjaðir sjálfkrafa)|Áskilið|Sama og fyrir ofan.|Sama og fyrir ofan.| Frágangur á ekki við um störf|

Sum afbrigði leyfa ekki að nota sérhæfð vöruhúsaskjöl til að skrá frágang. Ef hólf eru notuð er hins vegar hægt að nota almenn hreyfsluskjöl til að flytja framleiddar eða settar vörur í vöruhús.  [Frekari upplýsingar eru í Flytjendavörum í Grunnvöruafbrigðum](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick"></a><a name="outbound-flow-pick"></a><a name="outbound-flow-pick"></a>Flæði á útleið (taka til)

|Flækjustig|Description|Stillingar|Hólfkóti|Flæði framleiðslupöntunar|Flæði Samsetningarpöntunar|Flæði um vinnslur|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjálst. Hólfakóta er skylda  **að**  skipta út.|Framleiðslubók-> notkunarbók </br><br/> **Til** athugunar  **: Hægt er að bóka notkun með framleiðslubók**.|Samsetningarpöntun|Starf-> verkbók|  
|Grunnatriði|Pöntun-eftir pöntun.|Krefjast tínslu. </br><br/> **Til athugunar** : þó að stillingin sé kölluð  **krefjast tínslu** er enn hægt að bóka úttak úr upprunaskjölum í birgðageymslum þar sem gátreiturinn er valinn. <!-- ToDo Test prod output-->|Valfrjálst. Hólfakóta er skylda  **að**  skipta út.|Framleiðslupöntun-> Birgðatínsla|Samsetningarpöntun-> birgðahreyfingar</br><br/> **Aðeins er hægt að nota Birgðahreyfinguna**  með hólfum.|Vinnsla-> Birgðatínsla|
|Ítarlegt|Sameinaðar tínsluaðgerðir fyrir mörg upprunaskjöl.|Krefjast sendingar + krefjast tínslu|Valfrjálst. Hólfakóta sem stjórnað er er skylda að skipta|Framleiðslupantanir-> Vöruhúsatínsla-> notkunarbók |Samsetningarpantanir-> Vöruhúsatiltekt| Vinnslur-> Vöruhúsatínsla-> verkbók |
|Ítarlegt|Sama og fyrir ofan + beinar frágangs/frágang frágangsverkþátta|Beinar Tínslugerð og frágangingar (háðir víxlar verða virkjaðir sjálfkrafa)|Áskilið|Sama og fyrir ofan.|Sama og fyrir ofan.| Beinn tínsla og frágangur er ekki studdur fyrir störf|

Líkt og á innleið er ekki leyfilegt að nota sérhæfð vöruhúsaskjöl til að skrá frágang. Ef hólf eru notuð er hægt að nota almenn hreyfhreyfiskjöl til að flytja framleiddar eða settar vörur saman. Frekari upplýsingar hjá  [hreyfanlegum vörum](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity"></a><a name="warehouses-without-dedicated-warehouse-activity"></a><a name="warehouses-without-dedicated-warehouse-activity"></a>Vöruhús án sérstæð vöruhúsastarfsemi

Jafnvel þótt þú sért ekki með sérlega vöruhúsastarfsemi, munt þú líklega enn vilja fylgjast með hlutunum eins og notkun og framleiðsla framleiðsla. Eftirtaldar greinar veita upplýsingar um hvernig á að vinna innhreyfingar fyrir upprunaskjöl.

* [Skrá notkun og úttak fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md)
* [Sameina vörur](assembly-how-to-assemble-items.md)
* [Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a><a name="basic-warehouse-configuration"></a><a name="basic-warehouse-configuration"></a>Skilgreining grunnvöruhúss

Á inn-og útstreymis í grunnvöruvöruhúsi felast eftirfarandi stillingar á  **síðunni Birgðageymsluspjald**  fyrir birgðageymsluna:

* Fyrir innflæði (frágangur), skal kveikja á  **kröfu um frágang**, en  **slökkva á kröfu um viðtökuvíxla** .
* Ef um útflæði (tínslu) er að ræða er kveikt á  **krefjast tínslu**  en slökkt er  **á víxlun á krefjast afhendingu** .

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a><a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a><a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Streymi til og frá framleiðslu í grunnstillingu vöruhúss

Nota  **birgðatínsluskjöl**  til að velja framleiðsluíhluti í flæði til framleiðslu. Nota  **birgðafrágangsskjöl**  til að ganga frá afurðanna sem verið er að framleiða.

Fyrir staðsetningar sem nota hólf eru birgðahreyfðarskjöl sérstaklega gagnleg fyrir hlutabirgðaflutning. Til að fræðast nánar um hvernig íhlutalotkun er varpað úr framleiðslu eða opnum vinnusalarhólfum er farið í  [Flushing framleiðsluíhluti í vöruhúsinu](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Birgðahreyfingar eru mikilvæg skjöl ef þú notar  **tína + Forward**  eða  **tína + afturábak**  birgðaskráningaraðferðir. Frekari upplýsingar um  [flúorskolun](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

*  **Kóti til-framleiðslu hólfs**,  **Kóti frá-framleiðsla hólfs** og  **opinn kóti vinnukóta**  hólfs á staðnum eða í vélinni/vinnustöðinni skilgreinir sjálfgefin flæði til og frá framleiðslusvæðum.
* Hafa umsjón með flutningi framleiddra vara á  **síðu hreyfingarinnar**  innanhúss án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a><a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a><a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Streymi til og frá samsetningu í grunnstillingu vöruhúss

Bóka samsetningarúttak og notkun beint úr samsetningarpöntun.

> [!NOTE]
> **Birgðatínsla**  og  **frágangsskjöl**  sem eru ekki studd fyrir tillögur.

Fyrir staðsetningar sem nota hólf:

* Nota  **birgðahreyfingagátt**  til að færa samsetningaríhluti við samsetningarsvæðið.
*  **Hólfakótinn** **Kóti frá-samsetningarhólfkóti**  á birgðageymsluspjaldinu skilgreinir sjálfgefin streymi til og frá samsetningarsvæði.
* Hafa umsjón með hreyfingum samsettra vara á  **síðunni innanhúss**, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styðjum saman til Hlutabréfakaup og setji saman til að setja á laggirnar samkirkjulegar línur. Lærðu meira á  [að skilja saman til að panta og setja saman við birgðir](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). Í tengslum við vöruhúsastjórnun er sett saman við lager hluti af innra vöruhúsamóttafflæði og samsetja-pöntun er í vöruhúsi á útleið. Frekari upplýsingar á  [afgreiðslunum setja saman við vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a><a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a><a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flæði fyrir verkefnastjórnun í grunnstillingu vöruhúss

Nota  **birgðatínsluskjöl**  til að velja vinnsluíhluti í flæði til verkefnastjórnunar.

Fyrir birgðageymslu sem notar hólf er  **reiturinn til-kóti**  vinnslu í birgðageymslunni skilgreinir sjálfgefin flæði í Verkstjórnun.

## <a name="advanced-warehouse-configurations"></a><a name="advanced-warehouse-configurations"></a><a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi

Inn-og útstreymis í ítarlegri samskipan vöruhúss felur í sér Eftirtaldar stillingar á  **síðunni Birgðageymsluspjald**  fyrir birgðageymsluna:

* Fyrir innflæði (frágangur) skal kveikja á  **krefjast kvittunar**  og  **krefjast frágangsmáta** .
* Fyrir útstreymissútflæði (Pick) er kveikt á  **krefjast skips og**  krafist **Skiptilinnhreyfingar** .

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a><a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a><a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flæði til og frá framleiðslu í ítarlegum vöruhúsafbrigðum

 **Notið Vöruhúsatínsluskjölin**  og  **síðuna tínsluvinnublað**  til að velja íhluti fyrir framleiðslu.

Fyrir staðsetningar sem nota hólf:

* **Vöruhúsahreyfingin**  skjöl og  **vinnublaðið**  Hreyfill hreyfinga henta sérstaklega vel fyrir hlutaflúrin.  [Frekari upplýsingar um Flushing framleiðsluíhluti í vöruhúsinu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-a-advanced-warehouse-configuration).
*  **Kóti til-framleiðslu hólfs**,  **Kóti frá-framleiðsla hólfs** og  **opinn kóti vinnukóta**  hólfs á birgðageymslunni eða véla-/vinnustöðin skilgreina sjálfgefin flæði til og frá framleiðslusvæðum. 
* Stjórna hreyfingum framleiddra vara á  **vinnublaði**  eða  **vöruhúsaskjölum. Innri frágangssíður**, án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a><a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a><a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Streymi til og frá samsetningu í ítarlegum vöruhúsafbrigðum

Notið  **vöruhúsatínsluskjöl**  og  **síðuna tínsluvinnublað**  til að velja íhluti fyrir samsetningu.

Fyrir staðsetningar sem nota hólf:

*  **Reitirnir Kóti hólfs**  og  **frá-samsetningarkóti**  á birgðageymslunni skilgreina sjálfgefna streyta til og frá-samsetningarsvæðum.
* Stjórna hreyfingum samsetningaratriða á  **Hreyfingarblaði**  eða  **vöruhúsavöruhúss. Innanhússfrágangssíður**, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styðjum saman til Hlutabréfakaup og setji saman til að setja á laggirnar samkirkjulegar línur. Lærðu meira á  [að skilja saman til að panta og setja saman við birgðir](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Samsetja-birgðir eru hluti af innra vöruhúsamóttafflæði, og setja saman við pöntun er í flæði vöruhúss á útleið. Frekari upplýsingar á  [afgreiðslu setja saman vörur í Vöruhúsasendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a><a name="flows-to-project-management-in-advanced-warehouse-configurations"></a><a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Streymir til verkefnastjórnunar í ítarlegum vöruhúsafbrigðum

Nota  **vöruhúsatínsluskjöl**  og  **síðuna tínsluvinnublað**  til að velja íhluti í flæði til verkefnastjórnunar.

Fyrir staðsetningar sem nota hólf er  **reiturinn að-vinnsla hólfakóta**  á birgðageymslunni skilgreinir sjálfgefnu flæðin í Verksvæðið.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
