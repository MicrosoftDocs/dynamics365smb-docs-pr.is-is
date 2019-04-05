---
title: Hvernig skal safnvista sölu- og innkaupaskjölum | Microsoft Docs
description: Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/14/2018
ms.author: sgroespe
ms.openlocfilehash: 2f05313d30aede255e4ef49065f0189d649ce93c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800622"
---
# <a name="archive-documents"></a>Safnvista skjöl
Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum, t.d. vegna þess að þú vilt vista afrit af skjali til að nota aftur seinna. Þú getur safnvistað sölu- eða innkaupaskjali nokkrum sinnum og vistað aðra safnvistaða útgáfu í hvert skipti.

Fyrir safnvistuð skjöl þar sem upprunalega skjalið er ennþá til og er ekki bókað, getur þú notað virknina **Endurheimta** til að skrifa yfir upprunalega skjalið með safnvistuðu útgáfu skjalsins. Þetta er hagnýtt ef þú þarft að endurheimta eldri stöðu á innihaldi skjals.

Fyrir safnvistuð skjöl þar sem upprunalega skjalinu er eytt geturðu aðeins notað efnið aftur með því að afrita gögnin, til dæmis með virkninni **Afrita skjal**.   

## <a name="to-set-up-automatic-document-archiving"></a>Setja upp sjálfvirka safnvistun  
Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.

Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum. Skrefin eru svipuð fyrir innkaupaskjöl.
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sölu & útistandandi** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning sölu & útistandandi** er fyllt út í reitina á eftirfarandi hátt.

|Svæði|Description|
|-----|-----------|
|**Safnvista sölutilboð**|**Aldrei** til að aldrei safnvista sölutilboðum þegar þeim er eytt. **Spurning** til að biðja notandann um að velja hvort safnvista eigi sölutilboðum þegar þeim er eytt. **Alltaf** til að safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.|
|**Safnvista standandi sölupöntunum**|Veldu að safnvista standandi sölupöntunum sjálfkrafa í hvert skipti sem þeim er eytt.|
|**Safnvista pöntunum og vöruskilapöntunum**|Veldu til að safnvista sölupöntunum sjálfkrafa í hvert skipti sem þeim eru eytt.|

## <a name="to-archive-a-sales-order"></a>Til að safnvista sölupöntun
Eftirfarandi ferli sýnir hvernig skal safnvista sölupöntun. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2.  Opnuð er sölupöntun sem þú vilt kaupa safnvista.  
3.  Valin er aðgerðin **Safnvista skjal**.

Sölupöntunin er safnvistuð. Hægt er að skoða hana á síðunni **Safnvistaðar sölupantanir**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Að endurheimta óbókaða sölupöntun úr skjalasafninu
Eftirfarandi ferli sýnir hvernig skal ná innihaldi safnvistaðrar sölupöntunar aftur í upprunalega sölupöntun. Þetta er aðeins mögulegt þegar upprunalega skjalið hefur ekki verið bókað. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Safnvistaðar sölupantanir** og veldu síðan tengda tengilinn.
2. Valin er safnvistuð sölupöntun, eða útgáfa af henni, sem á að endurheimta og velja síðan aðgerðina **Endurheimta**.  

Innihald upphaflegu sölupöntunar er skipt út fyrir innihald völdu safnvistuðu útgáfunnar.

## <a name="to-delete-archived-sales-orders"></a>Eyða safnvistuðum sölupöntunum
Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum. Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða safnvistaðar útgáfur sölupantana** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Eyða útgáfum sölupantana í skjalasafni** skal velja viðeigandi síur.  
3.  Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Rekja skjalalínur](across-how-to-track-document-lines.md)  
[Sala](sales-manage-sales.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
