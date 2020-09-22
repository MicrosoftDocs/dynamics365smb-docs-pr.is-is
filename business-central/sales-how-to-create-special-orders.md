---
title: Hvernig á að stofna sérpöntun | Microsoft Docs
description: Hægt er að stofna sérpöntun til að tiltekið vörulistaatriði sé sent tilteknum viðskiptamanni. Birgir sendir vöruna í vöruhús og þá má senda hana áfram til viðskiptamanns, annaðhvort sérstaklega eða með annarri pöntun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 41e0c3e93a2a778745ad70d2a1711c76f28ec091
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788926"
---
# <a name="create-special-orders"></a>Sérstakar pantanir stofnaðar
Hægt er að stofna sérpöntun til að tiltekið vörulistaatriði sé sent tilteknum viðskiptamanni. Birgir sendir vöruna í vöruhús og þá má senda hana áfram til viðskiptamanns, annaðhvort sérstaklega eða með annarri pöntun.  

Sérpantanir gefa til kynna að innkaupa- og sölupöntun séu tengdar til að tryggja að sértækt vörulistaatriði sé tínt og afhent viðskiptamanni.  

Þessa aðgerð er ekki hægt að nota nema búið sé að setja upp spjald fyrir viðskiptamann, lánardrottin og vöru svo hægt sé að vinna pöntunina.  

## <a name="to-create-a-special-order"></a>Stofnuð sérpöntun:  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**. Búin er til ný  sölupöntun fyrir vöruna. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3.  Á flýtiflipanum **Línur** er fyllt út í sölulínuna. Í reitnum **Innkaupakóti** veljið innkaupakóta sem er með reitinn **Sérpöntun** valinn.

    Nú þarf að stofna innkaupapöntun út frá innkaupatillögu.  
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupatillaga** og veldu síðan tengda tengilinn.  
5. Veljið aðgerðina **Sérpöntun** og veljið síðan aðgerðina **sækja sölupöntun**.  
6.  Á síðunni **Sækja sölupantanir** sýna niðurstöður þar sem **Númer fylgiskjals** er sölupöntunarnúmeri. Velja hnappinn **Í lagi**. Kerfið stofnar innkaupatillögulínu vegna vörunnar.  
7.  Í innkaupatillögulínunni skal velja **Nýtt** í reitnum **Aðgerðarboð**.  
8.  Á síðunni **Innkaupatillaga** veljið aðgerðina **Framkvæma aðgerðaboð**. Síðan **Framkv. aðgerðaboð - Beiðni** opnast. Velja hnappinn **Í lagi**.  

    Þá birtast boð þess efnis að innkaupapantanir hafi verið stofnaðar. Velja hnappinn **Í lagi**.  

Tekið er tillit til stofnaðrar innkaupapöntunar fyrir sérpöntun af kerfinu þar sem hún jafnar framboð og eftirspurn. Það er, innkaupapöntun (framboð) helst tengd við sölupöntun (eftirspurn) jafnvel þó innkaupapöntunin gæti lagt til fyrri eftirspurnar. Nánari upplýsingar eru í [Upplýsingar um hönnun: Endurpöntunarstefnur](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Ekki er hægt að nota sérpöntunarkostinn ef varan er þegar frátekin. Þess vegna, fyrir vörur sem eru seldar með sérpöntunum, gakktu úr skugga um að **Frátekning** reiturinn á birgðaspjaldinu sé ekki stilltur á **Alltaf**.  

## <a name="see-also"></a>Sjá einnig  
[Vinna með vörulista](inventory-how-work-nonstock-items.md)  
[Sala](sales-manage-sales.md)  
[Beinar sendingar](sales-how-drop-shipment.md)   
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reservation-order-tracking-and-action-messaging.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
