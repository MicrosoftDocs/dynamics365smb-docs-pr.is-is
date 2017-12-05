---
title: "Dæmi – Skilgreining kvikrar úthlutunar á grundvelli seldra vara | Microsoft Docs"
description: "Þetta efnisatriði sýnir dæmi um hvernig á að skilgreina úthlutanir með því að nota kvika úthlutunaraðferð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d87e01cb987a019c6e71b50dcdeae55dc0375146
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Dæmi: Skilgreining kvikrar úthlutunar á grundvelli seldra vara
Þetta efnisatriði sýnir dæmi um hvernig á að skilgreina úthlutanir með því að nota kvika úthlutunaraðferð. Í dæminu er kvika úthlutun af kostnaði fyrir kostnaðarstað breytt til að styðja nýjan kostnaðarhlut IT EQUIPMENT. IT EQUIPMENT pakkar hafa vörunúmer frá 8904-W til 8924-W. Sölutölur fyrra árs eru notaðar til að reikna út hlutdeild. Úthlutunin er bókuð í aukakostnaðartegund 9903.  

> [!NOTE]  
>  Í dæminu er notast við sýnigögnin í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Til að skilgreina kvikar úthlutanir sem byggja á vörum sem seldar voru á síðasta ári  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Kostnaðarúthlutanir** og velja svo viðeigandi tengil.  
2.  Í glugganum **Kostnaðarúthlutun** skal velja aðgerðina **Nýtt**.  
3.  Í reitnum **Kenni** smellið á færslulykilinn eða sláið inn auðkenni.  
4.  Í reitinn **Stig**, sláið inn **1**.  
5.  Í reitnum **Gildir frá** og **Gildir til** eru viðeigandi dagsetningar færðar inn.  
6.  Í reitinn **Kóði kostnaðarstaðar** er slegið inn **SALA**.  
7.  Í **Kreditfært í kostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.  
8.  Í **Markkostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.  
9. Í reitnum **Markkostnaðarhlutur** veljið **Nýtt** til að stofna nýja kostnaðarhlutinn IT EQUIPMENT og fyllt er í reitina eftir þörfum. Veljið **IT EQUIPMENT**. Reiturinn **Markkostnaðarstaður** er hafður auður.  
10. Í reitnum **Gerð úthlutunarmarka**, veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
11. Í reitnum **Grunnur** veljið úthlutunarstofninn **Seldar vörur (upphæð)**.  
12. Í retinn **Númersafmörkun** er fært inn **8904-W..8924-W**.  
13. Í reitinn **Kóði gagnaafmörkunar** er fært inn **Síðasta ár**.  
14. Veljið **Reikna úthlutunarlykil** aðgerðina til að reikna út hlutinn.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] notar sölutölur fyrri ára til að reikna hlut 1596.50 SGM með 100 prósentum fyrir pakka IT EQUIPMENT. Þetta merkir að öllum seldum vörum síðasta árs verður úthlutað á kostnaðarhlutinn IT EQUIPMENT.  

## <a name="see-also"></a>Sjá einnig  
 [Uppsetning afmarkanir fyrir Kvik úthlutunargrunnar.](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Hvernig á að setja upp uppruna og markhópa úthlutanna](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md)   
 [Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md)   
 [Um kostnaðarbókhald](finance-about-cost-accounting.md)

