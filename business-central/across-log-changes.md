---
title: "Rekja aðgerðir notanda í breytingaskrá| Microsoft Docs"
description: "Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fe5bac9b47ccaca4cb3c1bdac7cda6b8d5ebbfd4
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="logging-changes-in-business-central"></a>Skráir breytingar í Business Central
Hægt er að kveikja á breytingaskrá í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fá verkþáttarferil. Skráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Í breytingarskránni, er færslum raðað í tímaröð og sýndar eru breytingar sem gerðar eru á reitum á tilgreindri töflu. Breytingaskráin safnar saman öllum breytingum sem gerðar eru á töflunni.  

## <a name="working-with-the-change-log"></a>Vinna með breytingaskrá
Það er alþekkt vandamál í stýrðum tölvukerfum að finna uppruna villna og breytinga á gögnum. Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag. Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum. Tilgreina verður hverja töflu og reit sem kerfið á að skrá og síðan þarf að virkja breytingaskrána.  

Glugginn **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka. Þegar kveikt eða slökkt er á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni. Ekki er hægt að gera þá skráningu óvirka.  

Í glugganum **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[d365fin](includes/d365fin_md.md)] rekur einnig númer kerfistaflna.

Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar í glugganum **Breytingaskrárfærslur**. Ef á að eyða færslum er hægt að gera í glugganum **Eyða Breytingaskrárfærslum** þar sem hægt er að stilla afmarkanir eftir dagsetningar og tíma.  

## <a name="see-also"></a>Sjá einnig
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Röðun](ui-sorting.md)  
[Notkun Leit að síðu eða skýrslu](ui-search.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
