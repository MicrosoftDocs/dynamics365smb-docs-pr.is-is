---
title: Skýrsluval í Business Central
description: Kynntu þér hvernig á að setja upp skýrslurnar sem þú notar til að prenta ýmsar tegundir skjala í Business Central.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 16ad3480c10da544c7fdd3a6a299dc6d86cfce46
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134057"
---
# <a name="report-selection-in-business-central"></a>Skýrsluval í Business Central

Hægt er að setja upp sjálfgefnar skýrslur sem verða notaðar til að prenta hin ýmsu skjöl fyrir sölu og innkaup, svo sem pantanir, tilboð, reikninga og kreditreikninga. Ef til dæmis um er að ræða tiltekið útlit fyrir sölureikninga er hægt að tilgreina þá skýrslu á síðunni **Skýrsluval - Sala** þannig að hún verði notuð til að senda eða prenta sölureikninga.  

Síðurnar **Skýrsluval** tilgreina hvaða skýrsla verður prentuð við mismunandi aðstæður. [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur sjálfgefnar skilgreiningar, en hægt er að breyta þeim. Einnig er hægt að bæta skýrslum við síðurnar **Skýrsluval** ef á að prenta fleiri en eina skýrslu fyrir hverja skjalagerð sem dæmi.  

## <a name="available-report-selections"></a>Skýrsluval í boði

[!INCLUDE [prod_short](includes/prod_short.md)] inniheldur mismunandi síður **Skýrsluvals** fyrir mismunandi svæði. Eftirfarandi töflur útskýra hvar hægt er að finna upplýsingar um mismunandi síður.  

|Svæði eða verkefni  |Frekari upplýsingar|
|--------------|----------|
|Dæmi um hvernig skýrsluval virkar (sala)|[Skýrsluval fyrir söluskjöl](#example-report-selection-for-sales-documents)|
|Sjálfgefið útlit fyrir tölvupósta með sölu- og innkaupaskjölum  |[Setja upp endurnýtanlega texta og útlit tölvupósts fyrir sölu- og innkaupaskjöl](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
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

## <a name="example-report-selection-for-sales-documents"></a>Dæmi: Skýrsluval fyrir söluskjöl

Síðan **Skýrsluval - Sala** skilgreinir sjálfgefnar skýrslur til að nota í mismunandi aðstæðum fyrir hverja skjalagerð sem á við. Veljið gerð skjals í reitnum **Notkun** og bætið síðan við eða yfirfarið skýrsluvalið. Hægt er að setja upp fleiri en eina skýrslu og röðina sem á að senda eða prenta skýrslurnar eftir.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Sumar skjalagerðir er hægt að senda sem tölvupóstviðhengi en aðrar ekki. Hver síða **Skýrsluvals** sýnir viðbótarreiti ef gerðin styður tölvupóst.  

Til dæmis á síðunum **Skýrsluval - Sala** og **Skýrsluval - innkaup** hjálpa eftirfarandi reitir þér við að setja upp tölvupóst:

|Heiti reits |Description  |
|-----------|-------------|
|**Nota fyrir meginmál tölvupósts**| Tilgreinir samanteknar upplýsingar, eins og númer reiknings, gjalddaga og tengil greiðsluþjónustu, sem verða settar inn í meginmál tölvupóstsins sem á að senda.        |
|**Nota fyrir tölvupóstsviðhengi**| Tilgreinir að tengt fylgiskjal verði hengt við tölvupóstinn.|
|**Lýsing á útliti meginmáls tölvupósts**|Tilgreinir útlit á meginmáli tölvupósts sem er notað, yfirleitt sérsniðið skýrsluútlit. |

## <a name="see-also"></a>Sjá einnig .

[Setja upp endurnýtanlega texta og útlit tölvupósts fyrir sölu- og innkaupaskjöl](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Velja útlit ávísunar](finance-how-define-check-layouts.md)  
[Setja upp skýrslur fyrir VSK og Intrastat (Þýskaland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md)  
[Setja upp prentara](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]