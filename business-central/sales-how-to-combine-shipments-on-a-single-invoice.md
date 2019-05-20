---
title: Hvernig á að sameina afhendingar í einn reikning | Microsoft Docs
description: Eigi að reikningsfæra fleiri en eina afhendingu saman er hægt að nota eiginleikann sameina afhendingar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3d4aa37a90a700ffb634867c0c96299cec941e35
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252551"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Sameina afhendingar einn reikning
Eigi að reikningsfæra fleiri en eina afhendingu saman er hægt að nota eiginleikann sameina afhendingar.  

 Áður en hægt er að búa til sameinaða afhendingu þarf að vera búið að bóka fleiri en eina söluafhendingu fyrir sama viðskiptamanninn í sama gjaldmiðlinum. Það er að segja, það þarf að vera búið að fylla út tvær eða fleiri sölupantanir og bóka þær sem afhentar en ekki reikningsfærðar. Til að sameina afhendingar þarf að velja gátreitinn **Sameina afhendingar** á flýtiflipanum **Afhending** í spjaldinu **viðskiptamaður**.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Að sameina afhendingar handvirkt í einn reikning  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).
3. Í reitnum **Selt til Viðskm.nr.**. reitnum er viðskiptamaðurinn sem fær reikninginn fyrir afhentar vörur tilgreindur.  
4. Á flýtiflipanum **Línur** skal velja **Sækja afhendingarlínur** aðgerðina.  
5. Afhendingarlínan sem á að vera á reikningnum er valin:  

    - Til að setja allar línur inn eru allar línur valda og svo smellt á **Í lagi**.  
    - Til að setja sérstakar línur inn eru línurnar valdar og svo smellt á **Í lagi**. Hægt er að nota Ctrl-takkanum til að velja margar línur sem ekki eru samliggjandi.  

    Ef röng afhendingarlína var valin eða byrja á aftur er línunum einfaldlega eytt í reikningnum aðgerðin **Sækja afhendingarlínur** keyrð aftur.  
7. Til að bóka reikningur er valið aðgerðin **bóka**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Til að sameina afhendingar sjálfkrafa á einn reikning  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sameina afhendingar** og veldu síðan tengda tengilinn. Síðan fyrir keyrslubeiðniglugga opnast.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja skal gátreitinn **Bóka reikninga**.  
4.  Velja hnappinn **Í lagi**.  

> [!NOTE]  
>  Bóka þarf reikninga handvirkt ef gátreiturinn **Bóka reikninga** var ekki valinn í keyrslunni.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Til að fjarlægja opnar sölupantanir eftir sameinaða afhending bókun 
Þegar afhendingar eru sameinaðar í reikningi og bókaðar er bókaður sölureikningur stofnaður fyrir reikningsfærðu línurnar. Reiturinn **Reikningsfært magn** í upphaflegu standandi sölupöntuninni eða sölupöntuninni er uppfærður samkvæmt reikningsfærða magninu.  

Þegar afhendingar eru reikningsfærðar á þennan hátt eru pantanir sem afhendingar voru bókaðar úr enn til staðar, jafnvel þótt þær hafi verið afhentar og reikningsfærðar að fullu.   

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða reikningsfærðum sölupöntunum** og veldu síðan tengda tengilinn.  
2. Tilgreinið í **Nr.**. afmörkunarreitnum hvaða sölupantanir á að eyða.  
3. Velja hnappinn **Í lagi**.  

Að öðrum kosti skal eyða einstökum sölupöntunum handvirkt.  

Skref 1 til 3 eru endurtekin fyrir öll skjöl sem urðu fyrir áhrifum, eins og auðar sölupantanir.

## <a name="see-also"></a>Sjá einnig  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
