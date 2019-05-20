---
title: Rekja aðgerðir notanda í breytingaskrá| Microsoft Docs
description: Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc14d11bf75ea39553c1ed04986273903874a0e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240442"
---
# <a name="auditing-changes-in-business-central"></a>Endurskoðunarbreytingar í Business Central

Hægt er að kveikja á breytingaskrá í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fá verkþáttarferil. Skráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Á síðunni **Breytingaskrárfærslur** er færslum raðað í tímaröð og sýndar eru breytingar sem gerðar eru á reitum á tilgreindum töflum. Breytingaskráin safnar saman öllum breytingum sem gerðar eru á töflunni.

> [!Important]
> Breytingar notanda eru ekki sýnilegar í **Breytingaskrárfærslum** fyrr en lota notanda er endurræst á ný, sem gerist í eftirfarandi tilvikum:
<br />
> * Lotan rann út og var endurnýjuð.
> * Notandinn valdi annað fyrirtæki eða hlutverkamiðstöð.
> * Notandinn skráði sig út og aftur inn.

## <a name="working-with-the-change-log"></a>Vinna með breytingaskrá

Það er alþekkt vandamál í stýrðum tölvukerfum að finna uppruna villna og breytinga á gögnum. Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag. Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum. Tilgreina verður hverja töflu og reit sem kerfið á að skrá og síðan þarf að virkja breytingaskrána.  

Síðan **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka. Þegar notandi kveikir eða slekkur á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni.

Á síðunni **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[d365fin](includes/d365fin_md.md)] rekur einnig númer kerfistaflna.

Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar á síðunni **Breytingaskrárfærslur**. Ef á að eyða færslum er hægt að gera það á síðunni **Eyða breytingaskrárfærslum** þar sem hægt er að stilla afmarkanir eftir dagsetningu og tíma.  

## <a name="see-also"></a>Sjá einnig
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Röðun](ui-sorting.md)  
[Nota Viðmótsleit til að finna eiginleika og upplýsingar](ui-search.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
