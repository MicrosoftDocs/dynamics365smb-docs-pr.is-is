---
title: Safnvista sölu- og innkaupaskjöl
description: Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum svo þú getur notað safnvistaða skjalið til að endurgera skjalið sem það var safnvistað frá.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: a12d8d7a11e581a6cfe93b6a1f4588cd87efc98f
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543273"
---
# <a name="archive-documents"></a>Safnvista skjöl
Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum, t.d. vegna þess að þú vilt vista afrit af skjali til að nota aftur seinna. Þú getur safnvistað sölu- eða innkaupaskjali nokkrum sinnum og vistað aðra safnvistaða útgáfu í hvert skipti.

Fyrir safnvistuð söluskjöl þar sem upprunalega skjalið er ennþá til og er ekki bókað, getur þú notað virknina **Endurheimta** til að skrifa yfir upprunalega skjalið með safnvistuðu útgáfu skjalsins. Þetta er hagnýtt ef þú þarft að endurheimta eldri stöðu á innihaldi skjals.

Fyrir safnvistuð skjöl þar sem upprunalega skjalinu er eytt geturðu aðeins notað efnið aftur með því að afrita gögnin, til dæmis með virkninni **Afrita úr skjali**.  

## <a name="to-set-up-automatic-document-archiving"></a>Setja upp sjálfvirka safnvistun

Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.

Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum. Skrefin eru svipuð fyrir innkaupaskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.
2. Á síðunni **Uppsetning sölu & útistandandi** er fyllt út í reitina. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Sérstaklega fyrir reitinn **Safnvista tilboðum** sýnir eftirfarandi tafla muninn á milli valmöguleika.

|Valkostur|Description|
|------|-----------|
|**Aldrei**| Aldrei safnvista sölutilboðum þegar þeim er eytt.|
|**Spurning**|Veldu að biðja notandann um að velja hvort safnvista eigi sölutilboðum þegar þeim er eytt.|
|**Alltaf**|Veldu að safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.|

## <a name="to-archive-a-sales-order"></a>Til að safnvista sölupöntun

Eftirfarandi ferli sýnir hvernig skal safnvista sölupöntun. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Opnuð er sölupöntun sem þú vilt kaupa safnvista.  
3. Valin er aðgerðin **Safnvista skjal**.

Sölupöntunin er safnvistuð. Hægt er að skoða hana á síðunni **Safnvistaðar sölupantanir**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Að endurheimta óbókaða sölupöntun úr skjalasafninu

Eftirfarandi ferli sýnir hvernig skal ná innihaldi safnvistaðrar sölupöntunar aftur í upprunalega sölupöntun. Þetta er aðeins mögulegt þegar upprunalega skjalið hefur ekki verið bókað. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Safnvistaðar sölupantanir** og velja síðan viðkomandi tengil.
2. Valin er safnvistuð sölupöntun, eða útgáfa af henni, sem á að endurheimta og velja síðan aðgerðina **Endurheimta**.  

Innihald upphaflegu sölupöntunar er skipt út fyrir innihald völdu safnvistuðu útgáfunnar.

## <a name="to-delete-archived-sales-orders"></a>Eyða safnvistuðum sölupöntunum

Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum. Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Safnvistaðar sölupantanir** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Eyða útgáfum sölupantana í skjalasafni** og síðan á síðunni **Eyða útgáfum sölupantana í skjalasafni** skaltu velja viðeigandi síur.  
3. Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig

[Rekja skjalalínur](across-how-to-track-document-lines.md)  
[Sala](sales-manage-sales.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
