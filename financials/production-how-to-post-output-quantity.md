---
title: "Hvernig á að fjöldabóka framleiðslufrálag og keyrslutíma | Microsoft Docs"
description: "Afkastsmagnið sýnir vinnuframvinduna í formi afgreidds magns."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e885149e28c2e09dc244bc5c0a431e7b2fe047a5
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-output-and-run-times"></a>Fjöldabóka frálag og keyrslutíma
Afkastsmagnið sýnir vinnuframvinduna í formi afgreidds magns.  

> [!NOTE]
> Aðeins þegar afkastsmagn er bókað í síðustu aðgerðinni eru birgðir sjálfkrafa uppfærðar.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Bóka frálagsmagn fyrir eina eða fleiri framleiðslupantanalínur
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **frálagsbók** og velja svo viðeigandi tengil.  
2. Reitirnir eru fylltir út með framleiðslupöntunargögnunum og frálagsgögnunum. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Ef aðgerðinni er lokið skal velja reitinn **Lokið**.  

    Ef vöruhúsið þar sem ganga á frá vörunum notar hólf en krefst ekki frágangsvinnslu skal  tengja kóta hólfs við bókarlínuna til að tilgreina hvar skuli setja vörurnar í vöruhúsinu. Frekari upplýsingar eru í [Ganga frá framleiðslu eða samsetningarúttaki](warehouse-how-to-put-away-production-output.md).  

4. Veljið **Bókun** til að bóka aðgerðirnar. Afkastsmagnið verður bókað. Varan er nú tilbúin til afhendingar.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Bóka keyrslutími fyrir eina eða fleiri framleiðslupantanalínur
Keyrslutíminn sýnir vinnuframvinduna í formi nauðsynlegs vinnutíma.    

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **frálagsbók** og velja svo viðeigandi tengil.  
2. Reitirnir eru fylltir út með framleiðslupöntunargögnunum og frálagsgögnunum.  
3.  Ef aðgerðinni er lokið skal velja reitinn **Lokið**.  
4. Velja **bóka** aðgerðina til að bóka tíma eytt á aðgerð. Afkastagetufærslur eru uppfærðar fyrir notaðar vinnu- eða vélastöðvar.

## <a name="see-also"></a>Sjá einnig  
[Framleiðsla](production-manage-manufacturing.md)    
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)      
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

