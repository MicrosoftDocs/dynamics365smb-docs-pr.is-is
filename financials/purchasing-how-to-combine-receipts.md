---
title: "Hvernig skal sameina móttökur | Microsoft Docs"
description: "Ef reikningsfæra á fleiri en eina innkaupamóttöku í einu er hægt að nota aðgerðina sameinaðar móttökur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9b3599a3f1a2cfc53d682a153eda8395e892305b
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-receipts-on-a-single-invoice"></a>Hvernig á að: sameina móttökur í einn reikning
Ef reikningsfæra á fleiri en eina innkaupamóttöku í einu er hægt að nota aðgerðina **sameinaðar móttökur**.  

Áður en hægt er að búa til sameinaða innkaupamóttöku, þarf að vera búið að bóka fleiri en eina móttöku frá sama lánardrottininn í sama gjaldmiðlinum. Það er að segja, það þarf að vera búið að fylla út tvær eða fleiri innkaupapantanir og bóka þær sem mótteknar en ekki reikningsfærðar.  

Þegar innkaupareikningar eru sameinaðir og bókaðir á reikningi, er bókaður innkaupareikningur stofnaður fyrir reikningslínu(r). Reiturinn **Reikningsfært magn** á upprunalegri innkaupapöntun eða standandi innkaupapöntun er uppfærður á grundvelli reikningsfærða magnsins. Hins vegar er upprunalega innkaupaskjalinu ekki eytt jafnvel þó það hafi verið móttekið og reikningsfært að fullu og því verður að eyða innkaupaskjalinu.  

## <a name="to-combine-receipts"></a>Sameining móttakna:  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð. Nánari upplýsingar eru í [Hvernig á að: Skrá innkaup](purchasing-how-record-purchases.md).  
3. Á flýtiflipanum **Línur** skal velja **Sækja móttökulínur** aðgerðina.  
4. Nokkrar móttökulínur eru valdar sem eiga að vera á reikningnum:  

    Ef röng móttökulína var valin eða byrja á upp á nýtt er einfaldlega hægt að eyða línunum í innkaupareikningum og nota aftur aðgerðina **Sækja móttökulínur**.  
5. Til að bóka reikningur er valið aðgerðin **bóka**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Til að fjarlægja opnar innkaupapantanir eftir bókun sameinaðrar móttöku  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Eyða reikningsfærðum innkaupapantanir** og velja svo viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Velja hnappinn **Í lagi**.  

Að öðrum kosti skal eyða einstökum pöntunum handvirkt.

Skref 1 til 3 eru endurtekin fyrir öll skjöl sem urðu fyrir áhrifum, eins og auðar innikaupapantanir.

## <a name="see-also"></a>Sjá einnig  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

