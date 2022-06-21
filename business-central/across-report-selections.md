---
title: Skýrsluval í Business Central
description: Kynntu þér hvernig á að setja upp skýrslurnar sem þú notar til að prenta ýmsar tegundir skjala í Business Central.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 03/11/2022
ms.author: edupont
ms.openlocfilehash: 9106b1ac3f6b179e26c8dfb01212b88e92b694fe
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950200"
---
# <a name="report-selection-in-business-central"></a>Skýrsluval í Business Central

Hægt er að setja upp sjálfgefnar skýrslur til að nota við prentun skjala fyrir sölu og innkaup, svo sem pantanir, tilboð og reikninga. Ef til dæmis um er að ræða tiltekið útlit fyrir sölureikninga er hægt að tilgreina þá skýrslu á síðunni **Skýrsluval - Sala** þannig að hún verði notuð til að senda eða prenta sölureikninga.  

Síðurnar **Skýrsluval** tilgreina hvaða skýrsla verður prentuð við mismunandi aðstæður. [!INCLUDE [prod_short](includes/prod_short.md)] gefur sjálfgefin afbrigði en hægt er að breyta þeim ef þörf krefur. Einnig er hægt að bæta skýrslum við síðurnar **Skýrsluval** ef á að prenta fleiri en eina skýrslu fyrir hverja skjalagerð sem dæmi.  

## <a name="available-report-selections"></a>Skýrsluval í boði

[!INCLUDE [prod_short](includes/prod_short.md)] inniheldur mismunandi síður **Skýrsluvals** fyrir mismunandi svæði. Eftirfarandi tafla lýsir því hvar hægt er að finna upplýsingar um hinar ólíku síður.  

|Svæði eða verkefni  |Frekari upplýsingar|
|--------------|----------|
|Dæmi um hvernig skýrsluval virkar (sala)|[Skýrsluval fyrir söluskjöl](#example-report-selection-for-sales-documents)|
|Sjálfgefið útlit fyrir tölvupósta með sölu- og innkaupaskjölum  |[Setja upp Endurnýtanlegan Senditexta og útlit fyrir sölu-og innkaupaskjöl](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Skilgreina útlit ávísana     |[Velja útlit ávísunar](finance-how-define-check-layouts.md) |
|Skilgreina skýrslur fyrir VSK-skýrslugerð (Þýskaland)|[Setja upp skýrslur fyrir VSK og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Sem dæmi getur [!INCLUDE [prod_short](includes/prod_short.md)] innihaldið fleiri síður **Skýrsluvals**, en það fer eftir staðsetningu þinni og atvinnugrein. Það er alltaf hægt að athuga uppsetninguna með því að velja ![Ljósapera sem opnar eiginleika viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið og fara í **Skýrsluval** og velja síðan viðkomandi tengil.

Sjálfgefna útgáfan af [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur eftirfarandi síður **Skýrsluhluta**:

* **Skýrsluval - Sala**  
* **Skýrsluval - innkaup**  
* **Skýrsluval - Birgðir**  
* **Skýrsluval - Sjóðstreymi**  
* **Skýrsluval – vöruhús**  
* **Skýrsluval - Bankareikningur**  
* **Innheimtubréf/vaxtareikningur skýrsluvals**  
* **Skýrsluval-starf**  

## <a name="example-report-selection-for-sales-documents"></a>Dæmi: Skýrsluval fyrir söluskjöl

Síðan **Skýrsluval - Sala** skilgreinir sjálfgefnar skýrslur til að nota í mismunandi aðstæðum fyrir hverja skjalagerð sem á við. Veljið gerð skjals í reitnum **Notkun** og bætið síðan við eða yfirfarið skýrsluvalið. Hægt er að setja upp fleiri en eina skýrslu og röðina sem á að senda eða prenta skýrslurnar eftir.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Sumar gerðir skjala er hægt að senda sem viðhengi í tölvupósti, og aðrir geta það ekki. Ef hægt er að senda tegund skjals í tölvupósti **mun Skýrsluvalssían** innihalda aukareiti.  

Til dæmis á síðunum **Skýrsluval - Sala** og **Skýrsluval - innkaup** hjálpa eftirfarandi reitir þér við að setja upp tölvupóst:

|Heiti reits |Lýsing  |
|-----------|-------------|
|**Nota fyrir meginmál tölvupósts**| Setja inn samanteknar upplýsingar, svo sem reikningsnúmer, gjalddaga og greiðsluþjónustutengil, í tölvupósti.        |
|**Nota fyrir tölvupóstsviðhengi**| Tengja tengda skjalið við netfangið.|
|**Lýsing á útliti meginmáls tölvupósts**|Tilgreinið líkamsútlit tölvupósts sem nota á. Algengast er að útlitið sé sérsniðið skýrslusnið. |

## <a name="see-also"></a>Sjá einnig .

[Setja upp Endurnýtanlegan Senditexta og skipulag](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Velja útlit ávísunar](finance-how-define-check-layouts.md)  
[Setja upp skýrslur fyrir VSK og Intrastat (Þýskaland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md)  
[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Ársskýrslur og Greinaskil á Viðskiptaaðalfundi](finance-reports.md)  
[Viðskiptaskýrslur og greinaskil í viðskiptabönkum miðlæg](receivables-reports.md) 
[viðskiptaskýrsla og greinaskil í viðskiptamiðinu](payables-reports.md)  
[Eignaskýrslur og Greinaskil í Viðskiptamiðinu](fa-reports.md)  
[Verkefnaskýrslur og Greinaskil í Viðskiptamiðinu](project-reports.md)  
[Söluskýrslur og Greinaskil í Viðskiptamiðinu](sales-reports.md)  
[Innkaupaskýrslur og Greinaskil í Viðskiptamiðinu](purchase-reports.md)  
[Birgðir og Vöruhúsatínslur og Analytics í viðskiptum miðlægt](inventory-WMS-reports.md)  
[Samsetningarskýrslur og Greinaskil í Viðskiptamiðinu](assembly-reports.md)  
[Framleiðsluskýrslur og Greinaskil í Viðskiptamiðinu](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]