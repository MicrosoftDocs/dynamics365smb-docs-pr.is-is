---
title: Skýrsluval í Business Central
description: Kynntu þér hvernig á að setja upp skýrslurnar sem þú notar til að prenta ýmsar tegundir skjala í Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 06/09/2022
ms.author: bholtorf
ms.openlocfilehash: fc5bfe8b22d06455379dabd20723fb0ccfe4032b
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607500"
---
# <a name="report-selection-for-documents-in-business-central"></a>Skýrsluval fyrir skjöl í Viðskiptamiðinu

Hægt er að setja upp sjálfgefnar skýrslur til að nota til að prenta sölu, innkaup og þjónustuskjöl, svo sem pantanir, tilboð og reikninga. Ef til dæmis um er að ræða tiltekið útlit fyrir sölureikninga er hægt að tilgreina þá skýrslu á síðunni **Skýrsluval - Sala** þannig að hún verði notuð til að senda eða prenta sölureikninga.  

## <a name="available-report-selections"></a>Skýrsluval í boði

Síðurnar **Skýrsluval** tilgreina hvaða skýrsla verður prentuð við mismunandi aðstæður. [!INCLUDE [prod_short](includes/prod_short.md)] gefur sjálfgefin afbrigði en hægt er að breyta þeim ef þörf krefur. Einnig er hægt að bæta skýrslum við síðurnar **Skýrsluval** ef á að prenta fleiri en eina skýrslu fyrir hverja skjalagerð sem dæmi. 

Eftirfarandi tafla lýsir því hvar hægt er að finna upplýsingar um hinar ólíku síður.  

|Svæði eða verkefni  |Frekari upplýsingar|
|--------------|----------|
|Dæmi um hvernig Skýrsluval virkar (sala)|[Skýrsluval fyrir söluskjöl](#example-report-selection-for-sales-documents) fundin hér fyrir neðan|
|Sjálfgefið útlit fyrir tölvupósta með sölu- og innkaupaskjölum  |[Setja upp Endurnýtanlegan Senditexta og útlit fyrir sölu-og innkaupaskjöl](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Skilgreina útlit ávísana     |[Velja útlit ávísunar](finance-how-define-check-layouts.md) |
|Skilgreina skýrslur fyrir virðisaukandi skatt (VSK)-skýrslugerð (Þýskaland)|[Setja upp skýrslur fyrir VSK og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Sem dæmi getur [!INCLUDE [prod_short](includes/prod_short.md)] innihaldið fleiri síður **Skýrsluvals**, en það fer eftir staðsetningu þinni og atvinnugrein. Til að kanna uppsetninguna skaltu velja þá ![ljósaperu sem opnar aðgerðina segja mér upp.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **Skýrsluval**, veldu síðan viðeigandi tengil.

Sjálfgefin útgáfa [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur eftirfarandi **skýrsluvalsíður**:

* **Skýrsluval - Sala**  
* **Skýrsluval - innkaup**  
* **Skýrsluval - Birgðir**  
* **Skýrsluval - Sjóðstreymi**  
* **Skýrsluval – vöruhús**  
* **Skýrsluval - Bankareikningur**  
* **Skýrsluval-starf**  
* **Skýrsluval-þjónusta**

## <a name="example-report-selection-for-sales-documents"></a>Dæmi: Skýrsluval fyrir söluskjöl

**Skýrsluval-sölusíða** býður upp á sjálfgefnar skýrslur til að nota í mismunandi aðstæðum fyrir tengda skjalagerð. Velja skal skjalagerð fyrir **notkunarreitinn**, bæta við eða fara yfir Skýrsluval. Hægt er að setja upp fleiri en eina skýrslu og tilgreina röðina sem skýrslurnar verða að vera sendar eða prentaðar í.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Ekki er hægt að senda allar skjalagerðir sem viðhengi í tölvupósti. Fyrir þá sem að því **koma er Skýrsluvalssíð** innihalda aukareiti.  

Til dæmis um **Skýrsluval-sölu** -og **Skýrsluval-innkaupasíður** hafa eftirtalin svæði hjálpað til við að setja upp email:

|Heiti reits |Lýsing  |
|-----------|-------------|
|**Nota fyrir meginmál tölvupósts**| Settu inn samandregnar upplýsingar eins og reikningsnúmer, gjalddaga eða tengil á greiðsluþjónustu í tölvupósti.        |
|**Nota fyrir tölvupóstsviðhengi**| Tengja tengda skjalið við netfangið.|
|**Lýsing á útliti meginmáls tölvupósts**|Tilgreinið líkamsútlit tölvupósts sem nota á. Yfirleitt er þetta útlit á sérsniðnu skýrslusniði. |

## <a name="see-also"></a>Sjá einnig .

[Setja upp Endurnýtanlegan Senditexta og skipulag](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Velja útlit ávísunar](finance-how-define-check-layouts.md)  
[Setja upp skýrslur fyrir VSK og Intrastat (Þýskaland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md)  
[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Ársskýrslur og Greinaskil á Viðskiptaaðalfundi](finance-reports.md)  
[Viðskiptaskýrslur og Greinaskil í Viðskiptamiðinu](receivables-reports.md)  
[Skýrslur og Greinaskil í Viðskiptabönkum seðlabanka](payables-reports.md)  
[Eignaskýrslur og Greinaskil í Viðskiptamiðinu](fa-reports.md)  
[Verkefnaskýrslur og Greinaskil í Viðskiptamiðinu](project-reports.md)  
[Söluskýrslur og Greinaskil í Viðskiptamiðinu](sales-reports.md)  
[Innkaupaskýrslur og Greinaskil í Viðskiptamiðinu](purchase-reports.md)  
[Birgðir og Vöruhúsatínslur og Analytics í viðskiptum miðlægt](inventory-WMS-reports.md)  
[Samsetningarskýrslur og Greinaskil í Viðskiptamiðinu](assembly-reports.md)  
[Framleiðsluskýrslur og Greinaskil í Viðskiptamiðinu](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
