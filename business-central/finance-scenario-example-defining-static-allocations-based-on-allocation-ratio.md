---
title: Skilgreining fastrar úthlutunar á grundvelli úthlutunarhlutfalls | Microsoft Docs
description: Föst úthlutunaraðferð er byggð á tilteknu gildi, s.s. fermetrum í notkun eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: d35fd5de7a0583c3864268d0749384322bf947ed
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800737"
---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Dæmi: Skilgreining fastrar úthlutunar á grundvelli úthlutunarhlutfalls
Föst úthlutunaraðferð er byggð á tilteknu gildi, s.s. fermetrum í notkun eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4.  

Í þessu efnisatriði er lýst hvernig á að skilgreina þrjá nýja kostnaðarhluti úthlutunarmarks fyrir kostnaðarstað úthlutunarupprunans FRAML með fyrirliggjandi úthlutunarhlutfallinu 5:2:4. Kostnaðarhlutirnir þrír eru ACCESSO, PAINT og FITTINGS.  

> [!NOTE]  
>  Í dæminu er notast við sýnigögnin í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Til að skilgreina PROD kostnaðarstað úthlutunarveitu á flýtiflipanum Almennt  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Kostnaðarúthlutun** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Kostnaðarúthlutun** skal velja aðgerðina **Nýtt**.  
3.  Í reitnum **Kenni** smellið á færslulykilinn eða sláið inn auðkenni.  
4.  Í reitinn **Stig**, sláið inn **1**.  
5.  Í reitnum **Gildir frá** og **Gildir til** eru viðeigandi dagsetningar færðar inn.  
6.  Í reitinn **Kóði kostnaðarstaðar** er slegið inn **SALA**.  
7.  Í **Kreditfært í kostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Til að skilgreina kostnaðarhluti úthlutunarmarks á flýtiflipanum Línur  

1.  Í fyrstu línunni í reitnum **Markkostnaðartegund** sláið inn **9903**.  
2.  Í fyrstu línunni í reitnum **Markkostnaðarhlutur** veljið **ACCESSO**.  
3.  Í fyrstu línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
4.  Í fyrstu línunni í reitnum **Grunnur** veljið **Fast** til að nota fasta úthlutunaraðferð.  
5.  Í fyrstu línuna í reitnum **Deila** setjið inn úthlutunarhlutfallið **5**.  
6.  Í aðra línuna í reitnum **Markkostnaðartegund** sláið inn **9903**.  
7.  Í annarri línunni, í reitnum **Markkostnaðarhlutur** er valið **MÁLNING**.  
8.  Í annarri línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
9. Í annarri línunni, í reitnum **Grunnur**, er valið **Föst** til að nota fasta úthlutunaraðferð.  
10. Í annarri línunni, í reitnum **Deila**, er sett inn úthlutunarhlutfallið **2**.  
11. Í þriðju línuna í reitnum **Markkostnaðartegund** sláið inn **9903**.  
12. Í þriðju línunni í reitnum **Markkostnaðarhlutur**, er slegið inn **TENGIHLUTIR**.  
13. Í þriðju línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
14. Í þriðju línunni í reitnum **Grunnur**, er valið **Föst** til að nota fasta úthlutunaraðferð.  
15. Í þriðju línunni, í reitnum **Deila**, er sett inn úthlutunarhlutfallið **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] reiknar sjálfkrafa reitinn **Prósenta** með því að nota prósentuhlutfall sem er háð öllum þremur úthlutunarhlutföllum sem færð eru inn í reitinn **Deila** í öllum þremur línunum.  

## <a name="see-also"></a>Sjá einnig  
[Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md)   
