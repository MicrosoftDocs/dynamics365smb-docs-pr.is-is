---
title: "Rekja aðgerðir notanda í breytingaskrá| Microsoft Docs"
Description: "Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="logging-changes-in-dynamics-365-for-financials"></a>Skráning breytinga í Dynamics 365 for Financials
Hægt er að kveikja á breytingaskrá í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fá verkþáttarferil. Breytingaskráin skráir breytingar sem gerðar eru á gögnum í töflunum sem eru raktar. Í breytingarskránni, er færslum raðað í tímaröð og sýndar eru breytingar sem gerðar eru á reitum á tilgreindri töflu. Breytingaskráin safnar saman öllum breytingum sem gerðar eru á töflunni.  

## <a name="working-with-the-change-log"></a>Vinna með breytingaskrá
Það er alþekkt vandamál í stýrðum tölvukerfum að finna uppruna villna og breytinga á gögnum. Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag. Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum. Tilgreina verður hverja töflu og reit sem kerfið á að skrá og síðan þarf að virkja breytingaskrána.  

Glugginn **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka. Þegar kveikt eða slökkt er á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni. Ekki er hægt að gera þá skráningu óvirka.  

Í glugganum **Uppsetning breytingaskrár** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[d365fin](includes/d365fin_md.md)] rekur einnig margar kerfistöflur.

Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar í glugganum **Breytingaskrárfærslur**. Ef á að eyða færslum er hægt að gera í glugganum **Eyða Breytingaskrárfærslum** þar sem hægt er að stilla afmarkanir eftir dagsetningar og tíma.  

## <a name="see-also"></a>Sjá einnig
[Breyta grunnstillingum](ui-change-basic-settings.md)  
[Röðun](ui-sorting.md)  
[Notkun Leit að síðu eða skýrslu](ui-search.md)  
[Hvernig á að: Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
