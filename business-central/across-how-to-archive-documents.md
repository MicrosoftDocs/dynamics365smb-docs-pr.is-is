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
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Safnvista skjöl
Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá.

## <a name="to-set-up-automatic-document-archiving"></a>Setja upp sjálfvirka safnvistun  
Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.

Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum. Skrefin eru svipuð fyrir innkaupaskjöl.
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning Sala & útistandandi** og velja svo viðeigandi tengil.
2. Í glugganum **Uppsetning sölu & útistandandi** er fyllt út í reitina á eftirfarandi hátt.

|Svæði|Description|
|-----|-----------|
|**Safnvista sölutilboð**|**Aldrei** til að aldrei safnvista sölutilboðum þegar þeim er eytt. **Spurning** til að biðja notandann um að velja hvort safnvista eigi sölutilboðum þegar þeim er eytt. **Alltaf** til að safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.|
|**Safnvista standandi sölupöntunum**|Veldu að safnvista standandi sölupöntunum sjálfkrafa í hvert skipti sem þeim er eytt.|
|**Safnvista pöntunum og vöruskilapöntunum**|Veldu til að safnvista sölupöntunum sjálfkrafa í hvert skipti sem þeim eru eytt.|

## <a name="to-archive-a-sales-order"></a>Til að safnvista sölupöntun
Eftirfarandi ferli sýnir hvernig skal safnvista sölupöntun. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.  
2.  Opnuð er sölupöntun sem þú vilt kaupa safnvista.  
3.  Valin er aðgerðin **Safnvista skjal**.

Sölupöntunin er safnvistuð. Hægt er að skoða hana í glugganum **Safnvistaðar sölupantanir**. Héðan er einnig hægt að endurgera sölupöntunina frá staðnum sem hún var safnvistuð frá.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Endurgera sölupöntun frá skjalasafninu
Eftirfarandi ferli sýnir hvernig skal endurgera sölupöntun. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1.  Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Safnvistaðar sölupantanir** og velja svo viðeigandi tengil.
2.  Valin er safnvistuð sölupöntun sem á að endurgera og velja síðan aðgerðina **Endurstilla**.  

Sölupöntunin er stofnuð og bætt við gluggann **Sölupantanir**.

## <a name="to-delete-archived-sales-orders"></a>Eyða safnvistuðum sölupöntunum
Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum. Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.

1.  Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), fara í **Eyða útgáfum sölupantana í skjalasafni** og velja svo viðeigandi tengil.  
2.  Í glugganum **Eyða útgáfum sölupantana í skjalasafni** skal velja viðeigandi síur.  
3.  Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Rekja skjalalínur](across-how-to-track-document-lines.md)  
[Sala](sales-manage-sales.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

