---
title: "Hvernig skal safnvista sölu- og innkaupaskjölum | Microsoft Docs"
description: "Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6b1b23c062fdb1c4558a292c7aa454ae24ff3c71
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="archive-documents"></a>Safnvista skjöl
Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá.

## <a name="to-set-up-automatic-document-archiving"></a>Setja upp sjálfvirka safnvistun  
Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.

Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum. Skrefin eru svipuð fyrir innkaupaskjöl.
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sölu & útistandandi** og veldu síðan tengda tengilinn.
2. Í glugganum **Uppsetning sölu & útistandandi** er fyllt út í reitina á eftirfarandi hátt.

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

Sölupöntunin er safnvistuð. Hægt er að skoða hana í glugganum **Safnvistaðar sölupantanir**. Héðan er einnig hægt að endurgera sölupöntunina frá staðnum sem hún var safnvistuð frá.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Endurgera sölupöntun frá skjalasafninu
Eftirfarandi ferli sýnir hvernig skal endurgera sölupöntun. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Safnvistaðar sölupantanir** og veldu síðan tengda tengilinn.
2.  Valin er safnvistuð sölupöntun sem á að endurgera og velja síðan aðgerðina **Endurstilla**.  

Sölupöntunin er stofnuð og bætt við gluggann **Sölupantanir**.

## <a name="to-delete-archived-sales-orders"></a>Eyða safnvistuðum sölupöntunum
Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum. Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða safnvistaðar útgáfur sölupantana** og veldu síðan tengda tengilinn.  
2.  Í glugganum **Eyða útgáfum sölupantana í skjalasafni** skal velja viðeigandi síur.  
3.  Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Rekja skjalalínur](across-how-to-track-document-lines.md)  
[Sala](sales-manage-sales.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

