---
title: 'Hönnunarupplýsingar - Flæði fyrir framleiðslu, samsetningu og störf'
description: 'Kynntu þér flæðið á milli hólfa til að tína íhluti og setja frá sér lokahluti fyrir samsetningu, framleiðslu eða verkpantanir.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs"></a>Flæði fyrir framleiðslu, samsetningu og störf

Innra flæði, eins og að tína íhluti og setja frá sér lokahluti fyrir samsetningu, verk og framleiðslupantanir, eru svipað og inn- eða útstreymi. Þannig að mörg ferlanna gæti verið kunnugleg. Þessi grein veitir upplýsingar um hvernig á að vinna með innra vöruhúsaflæði með ýmsum flækjustigum.

## <a name="overview-of-different-configuration-options"></a>Yfirlit yfir mismunandi stillingarvalkosti

Þú getur stillt vöruhúseiginleika á ýmsa vegu. Það er mikilvægt að valkostirnir sem þú velur bæti ferla þína án þess að valda kostnaði. Eftirfarandi töflur lýsa dæmigerðum stillingum til að takast á við efnislegar vörur fyrir framleiðslu, verk og samsetningarpantanir.

### <a name="inbound-flow-put-away"></a>Innstreymi (sett í burtu)

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Innleiðandi flæði framleiðslupöntunar|Innleiðandi flæði samsetningarpöntunar|Innleiðandi störf|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og dagbókum.||Valfrjálst. Stjórnað af **Bin Code er skylda** rofi.|Framleiðslublað -> Output Journal</br><br/> **ATHUGIÐ**: Þú getur sent úttak með því að nota **Production Journal**.|Samsetningarpöntun|Frágangur á ekki við um störf|  
|Grunnatriði|Röð eftir pöntun.|Krefjast frágangs. </br><br/> **ATHUGIÐ**: Þó að stillingin sé kölluð **Require Set-away** geturðu samt sent úttak úr upprunaskjölunum á stöðum þar sem þú velur þennan gátreit. |Valfrjálst. Stjórnað af **Bin Code er skylda** rofi.|Framleiðslupöntun -> Birgðasetning|Samsetningarpöntun|Frágangur á ekki við um störf|
|Ítarlegt|Samþætt frágangur fyrir mörg frumskjöl.|Krefjast kvittunar + Krefjast frágangs|Valfrjálst. Stjórnað af **Bin Code er skylda** rofi.|Framleiðslupantanir -> Output Journal|Samsetningarpantanir -> innri hreyfingar | Frágangur á ekki við um störf|
|Ítarlegt|Sama og hér að ofan + Stýrð tínsla/frágangur|Stýrt val og frágang (háðir rofar verða sjálfkrafa virkjaðir)|Áskilið|Sama og fyrir ofan.|Sama og fyrir ofan.| Frágangur á ekki við um störf|

Sumar stillingar leyfa þér ekki að nota sérstök vöruhúsaskjöl til að skrá frágang. Hins vegar, ef staðsetning þín notar bakka geturðu notað almenn flutningsskjöl til að flytja framleidda eða samsetta hluti í vöruhús. Lærðu meira á [Færa hluti innbyrðis í grunnstillingum vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick"></a>Útstreymi (velja)

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Útstreymi framleiðslupöntunar|Útstreymi samsetningarpöntunar|Útstreymi starfa|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og dagbókum.||Valfrjálst. Stjórnað af **Bin Code er skylda** rofi.|Framleiðslublað -> Neyslublað </br><br/> **ATHUGIÐ**: Þú getur birt neyslu með því að nota **Production Journal**.|Samsetningarpöntun|Starf -> Atvinnublað|  
|Grunnatriði|Röð eftir pöntun.|Krefjast Pick. </br><br/> **ATHUGIÐ**: Þó að stillingin sé kölluð **Require Pick** geturðu samt sent úttak úr upprunaskjölunum á stöðum þar sem þú velur þennan gátreit. <!-- ToDo Test prod output-->|Valfrjálst. Stjórnað af **Bin Code er skylda** rofi.|Framleiðslupöntun -> Birgðaval|Samsetningarpöntun -> Birgðahreyfing</br><br/>Aðeins er hægt að nota **Birgðahreyfinguna**  með ruslum.|Starf -> Birgðaval|
|Ítarlegt|Samþætt valvirkni fyrir mörg upprunaskjöl.|Krefjast sendingar + Krefjast tínslu|Valfrjálst. Stjórnað af Bin Code er skyldubundinn rofi|Framleiðslupantanir -> Vöruhúsval -> Neyslublað |Samsetningarpantanir -> Vöruhúsaval| Störf -> Vöruhúsval -> Atvinnublað |
|Ítarlegt|Sama og hér að ofan + Stýrð tínsla/frágangur|Stýrt val og frágang (háðir rofar verða sjálfkrafa virkjaðir)|Áskilið|Sama og fyrir ofan.|Sama og fyrir ofan.| Stýrt val og frágang er ekki stutt fyrir störf|

Svipað og innstreymi, leyfa sumar stillingar þér ekki að nota sérstök vöruhúsaskjöl til að skrá frágang. Ef staðsetning þín notar bakka geturðu notað almenn flutningsskjöl til að flytja framleidda eða samsetta hluti. Lærðu meira á [Að flytja hluti](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Vöruhús án sérstakra vöruhúsastarfsemi

Jafnvel þótt þú sért ekki með sérstaka vöruhúsastarfsemi, muntu líklega enn vilja halda utan um hluti eins og neyslu og framleiðsluframleiðslu. Eftirfarandi greinar veita upplýsingar um hvernig á að vinna með kvittanir fyrir upprunaskjöl.

* [Skráðu neyslu og afköst fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md)
* [Sameina vörur](assembly-how-to-assemble-items.md)
* [Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Grunnuppsetning vöruhúss

Inn- og útstreymi í grunnstillingu vöruhúss felur í sér eftirfarandi stillingar á  **Staðsetningarkorti** síðunni fyrir staðsetninguna:

* Fyrir innstreymi (frálát) skaltu kveikja á **Krefjast frágang** rofa, en slökkva á **Krefjast kvittunar** skipta.
* Fyrir útstreymi (velja) skaltu kveikja á **Krefjast tínslu** rofa, en slökkva á **Krefjast sendingu** víxlinum.

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Flæði til og frá framleiðslu í grunnstillingu vöruhúss

Notaðu **Birgðaval** skjöl til að velja framleiðsluíhluti í flæði til framleiðslu. Til að leggja frá þér vörurnar sem þú framleiðir skaltu nota **Inventory Put-away** skjöl.

Fyrir staðsetningar sem nota bakkar eru birgðaflutningsskjöl sérstaklega gagnleg fyrir íhlutaskolun. Til að fræðast meira um hvernig íhlutanotkun er skoluð úr tunnunum fyrir framleiðslu eða opna búðarhæð, farðu í [Skolun framleiðsluíhluta í vöruhúsinu](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Birgðahreyfingar eru mikilvæg skjöl ef þú notar **Pick + Forward** eða **Pick + Backward** skoðaaðferðir. Lærðu meira á [Róunaraðferðir](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* The **Kóði fyrir framleiðsluhólf**, **Kóði frá framleiðslukörfu**, og **Opnaðu ruslakóða verslunarhæðar**  reitir á staðsetningu eða vél/vinnustöð skilgreina sjálfgefið flæði til og frá framleiðslusvæðum.
* Stjórna hreyfingu framleiddra hluta á **Innri hreyfing**  síðu án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Flæði til og frá samsetningu í grunnstillingu vöruhúss

Bókaðu framleiðsla og notkun samsetningar beint úr samsetningarpöntun.

> [!NOTE]
> **Birgðaval**  og **Birgðasetning**  skjöl eru ekki studd fyrir samsetningarpantanir.

Fyrir staði sem nota ruslakörfur:

* Notaðu **Birgðahreyfing**  skjöl til að færa samsetningaríhluti á samsetningarsvæðið.
* Reitirnir **Til-samsetningu hólfskóði**, **Frá samsetningu hólfkóða**  á staðsetningarspjaldinu skilgreina sjálfgefið flæði til og frá samkomusvæðum.
* Stjórnaðu flutningi samsettra hluta á síðunni **Innri hreyfing**, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningu á lager og samsetningu eftir pöntun. Lærðu meira á [Skilning á að setja saman til að panta og setja saman á lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). Í tengslum við vöruhúsastjórnun er samsetning í lager hluti af innra vöruhúsaflæði og samsetning eftir pöntun er í útleið vöruhúsaflæði. Frekari upplýsingar er að finna á [Meðhöndlun samsettra vara til pöntunar með birgðavali](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flæði fyrir verkefnastjórnun í grunnstillingu vöruhúss

Notaðu **Birgðaval** skjöl til að velja verkþætti í flæðinu til verkefnastjórnunar.

Fyrir staðsetningu sem notar hólf, skilgreinir **To-Job Bin Code** reiturinn á staðsetningunni sjálfgefið flæði til verkefnastjórnunar.

## <a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi

Inn- og útstreymi í háþróaðri vöruhúsastillingu felur í sér eftirfarandi stillingar á  **Staðsetningarspjald** síðunni fyrir staðsetninguna:

* Fyrir innstreymið (frálát), kveiktu á **Krefjast kvittunar** og **Krefjast frágangs** kveikjum.
* Fyrir útstreymi (velja), kveiktu á **Krefjast sendingar** og **Krefjast kvittunar** rofa.

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flæði til og frá framleiðslu í háþróaðri vöruhúsastillingum

Notaðu **Vöruhústínslu** skjölin og **Vínduvinnublaðið** til að velja íhluti til framleiðslu.

Fyrir staði sem nota ruslakörfur:

* **Vöruhúsahreyfingar** skjöl og **hreyfingarvinnublaðið** síðan eru sérstaklega gagnleg til að skola íhlutum. Frekari upplýsingar á [Skolun framleiðsluíhluta í vöruhúsinu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
*  **Til-framleiðslu hólfskóðinn**, **Frá-framleiðsluhólfskóðinn** og **Open Kóði búðarhæðar** reitir á staðsetningu eða vél/vinnustöð skilgreina sjálfgefið flæði til og frá framleiðslusvæðum. 
* Stjórna flutningi framleiddra hluta á **Hreyfingarblaðinu** eða **Whse. Innri frágangs** síður, án tengsla við framleiðslupöntun.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Flæði til og frá samsetningu í háþróaðri vöruhúsastillingum

Notaðu **Warehouse Pick** skjöl og  **Veldu vinnublaðið** síðuna til að velja íhluti fyrir samsetningu.

Fyrir staði sem nota ruslakörfur:

* Reitirnir **To-Assembly Bin Code** og **From-Assembly Bin Code** á staðsetningunni skilgreina sjálfgefið flæði til og frá samkomusvæðum.
* Stjórna flutningi samsetningarhluta á **Hreyfingarblaðinu** eða **Whse. Innri frágangs** síður, án tengsla við samsetningarpöntun.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningu á lager og samsetningu eftir pöntun. Lærðu meira á [Skilning á að setja saman til að panta og setja saman á lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Samsetning í lager er hluti af innra vöruhúsaflæði og samsetning eftir pöntun er í útleið vöruhúsaflæði. Frekari upplýsingar er að finna á [Meðhöndlun samsettra vara í vöruhúsasendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Flæði til verkefnastjórnunar í háþróuðum vöruhúsastillingum

Notaðu **Warehouse Pick** skjöl og  **Veldu vinnublaðið** síðuna til að velja íhluti í flæðið til verkefnastjórnunar.

Fyrir staðsetningar sem nota hólf, skilgreinir **To-Jobs hólfkóði** reitinn á staðsetningunni sjálfgefið flæði til verksvæðisins.

## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
