---
title: "Hvernig á að úthluta vörum sjálfgefnum hólfum | Microsoft Docs"
description: "Ef hólf eru notuð í birgðageymslu verður öll móttaka, afhending og hreyfing á vörum mun auðveldari ef sjálfgefin hólf eru notuð. Þegar sjálfgefið hólf er tengt vöru leggur kerfið það til í hvert sinn sem færsla fer í gang fyrir vöruna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 826e1392143b166566619c5aef8c28ac2b09bc22
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="assign-default-bins-to-items"></a>Sjálfgefin hólf tengd vörum
Ef hólf eru notuð í birgðageymslu verður öll móttaka, afhending og hreyfing á vörum mun auðveldari ef sjálfgefin hólf eru notuð. Þegar sjálfgefið hólf er tengt vöru leggur kerfið það til í hvert sinn sem færsla fer í gang fyrir vöruna. Sjálfgefin hólf eru skilgreind í glugganum **Innihald hólfs**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Að úthluta vöru sjálfgefnu hólfi
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vinnublað f. stofnun hólfainnihalds** og velja svo viðeigandi tengil.  
2.  Tilgreindur er hólfkóti og vöruupplýsingar fyrir hvert hólf sem á að verða sjálfgefið og vöru. Gæta skal þess að velja reitinn **Sjálfgefið**.  
3.  Valið er **Stofna innihald hólfa** aðgerð. Sjálfgefin hólf hafa nú verið tengd vörunum.  

> [!NOTE]  
>  Þegar gengið er frá vöru og hún er ekki með sjálfgefið hólf gerir kerfið hólfið sem hún er sett í sjálfgefið.  

## <a name="to-change-the-default-bin-for-an-item"></a>Skipt um sjálfgefið hólf vöru  
Stundum getur þurft að skipta um sjálfgefið hólf vöru eða gefa nýrri vöru sjálfgefið hólf.    
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hólfainnihald** og velja svo viðeigandi tengil.  
2.  Í reitnum **Birgðageymsluafmörkun** er valinn réttur birgðageymslukóti.  
3.  Gildandi sjálfgefið hólfafærsla vörunnar er fundið og gátreitur **Sjálfgefið hólf** er hreinsaður.  
4.  Hólfinnihaldslína hólfsins sem á að verða sjálfgefið er fundin. Veljið gátreitinn **Sjálfgefið hólf**.  

> [!NOTE]  
>  Þegar gengið er frá vöru í fyrsta skipti og hún er ekki með sjálfgefið hólf gerir kerfið hólfið sem hún er sett í sjálfgefið.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

