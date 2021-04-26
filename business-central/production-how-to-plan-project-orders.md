---
title: Hvernig á að áætla verkefnispantanir | Microsoft Docs
description: Þessi áætlanagerð byrjar í sölupöntun og nýtir síðuna **Áætlun sölupöntunar**. Þegar framleiðslupöntun verkefnis er stofnuð er hægt að skipuleggja hana frekar með því að nota síðuna **Pantanaáætlun**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 28568cd8ab7751e15bf24acd3c727828bba9f76c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787953"
---
# <a name="plan-project-orders"></a>Áætla verkefnispantanir
Þessi áætlanagerð byrjar í sölupöntun og nýtir síðuna **Áætlun sölupöntunar**. Þegar framleiðslupöntun verkefnis er stofnuð er hægt að skipuleggja hana frekar með því að nota síðuna **Pantanaáætlun**.  

## <a name="to-create-a-project-production-order"></a>Framleiðslupöntun verkefnis stofnuð  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2.  Veljið sölupöntunina sem sýnir framleiðsluverkefnið, og veljið síðan aðgerðina **Áætla**.  
4.  Á síðunni **Áætlun sölupöntunar** er smellt á aðgerðina **Stofna framl.pöntun**.  
5.  Á síðunni **Stofna pöntun úr sölu** í reitnum **Tegund pöntunar** er **Verkefnispöntun** valin.  
6.  Velja hnappinn **Já**.  
7.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Framleiðslupantanir** og veldu síðan tengda tengilinn.
8. Opna skal nýstofnaða framleiðslupöntun.  

    Athugið að reiturinn **Tegund uppruna** í framleiðslupöntuninni inniheldur **Söluhaus** og hún hefur margar línur, eina fyrir hverja vöru sölulínu sem þarf að framleiða.  
9. Veldu aðgerðina **Áætlun**.
10. Á síðunni **Pantanaáætlun** er smellt á **Uppfæra** aðgerðina til reikna nýja eftirspurn.  

Pöntunarhausslínan fyrir verkefnispöntunina birtist með allar óuppfylltar eftirspurnarlínur stækkaðar neðan hennar. Þótt framleiðslupöntunin innihaldi línur fyrir nokkrar framleiddar vörur er heildareftirspurnin fyrir allar framleiðslupöntunarlínur skráð undir einni pöntunarhausslínu á síðunni **Pantanaáætlun**, auk þess sem nafn upprunalega viðskiptamannsins er birt. Nú er hægt að fara áætla eftirspurn eins og lýst er í [Gera áætlanir um nýja eftirspurn pöntun fyrir pöntun](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Eftirspurnarlínur í framleiðslupöntun verkefnisins sem hafa **Framl.pöntun** í reitnum **Áfyllingarkerfi** tákna undirliggjandi framleiðslupantanir. Eftir að hafa myndað þessar framleiðslupantanir, þarf að reikna aftur út áætlun á síðunni **Pantanaáætlun** til að auðkenna alla óuppfyllta eftirspurn eftir íhlutum fyrir þær. Í því tilviki er birtist eftirspurnin í eftirspurnarlínum undir línu í haus venjulegrar framleiðslupöntunar sem þýðir að verkefnistengslin sjást ekki lengur á síðunni. Ef á hinn bóginn notast er við eiginleikann Rekja pöntun er hægt að fara fram og aftur í allar framboðspantanir undir upphaflegu sölupöntuninni.  

## <a name="see-also"></a>Sjá einnig
[Áætlun](production-planning.md)   
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]