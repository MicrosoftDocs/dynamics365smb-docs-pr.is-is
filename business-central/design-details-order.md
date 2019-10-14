---
title: Hönnunarupplýsingar - Pantanir | Microsoft Docs
description: Þetta efnisatriði veitir upplýsingar um pöntun til pöntunar hlekki í framleiða eftir pöntun umhverfi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 09ef0ab320b2f7c19c0484f05efe7b3ae1fa41f7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303113"
---
# <a name="design-details-order"></a>Hönnunarupplýsingar: pantanir
Í framleiða eftir pöntun umhverfi, er vara keypt eða framleidd til eingöngu ná ákveðna eftirspurn. Venjulega tekur hún til A-vara og ástæða fyrir að velja Endurpöntunarstefnu pöntunar getur verið að eftirspurn er hverfandi, sem afhendingartími er óveruleg, eða nauðsynlegar eigindir mismunandi.  

Forritið stofnar pöntun-við-pöntun tengsl sem virka sem undirbúningstengsl milli framboðsins, birgðapöntunar eða birgða og eftirspurnarinnar sem henni er ætlað að mæta.  

Burtséð frá notkun pöntunarstefnu er hægt að nota tengil á milli pantana í áætlun með eftirfarandi hætti:  

* Þegar reglan framleiðsla eftir pöntun er notuð til að stofna margþrepa framleiðslupöntun eða framleiðslupöntun af gerðinni verk (nauðsynlegir íhlutir framleiddir samkv. sömu framleiðslupöntun).  
* Þegar búnaðurinn Sölupantanaáætlun er notaður til að stofna framleiðslupöntun úr sölupöntun.  

Jafnvel þótt framleiðslufyrirtæki álíti sig framleiða eftir pöntun geur verið best að nota endurpöntunarstefnuna lota fyrir lotu ef vörurnar eru staðlaðar án afbrigða í eigindum. Niðurstaðan er að kerfið mun nota óáætlaðar birgðir og safna aðeins sölupöntunum með sömu afhendingardagsetningu eða innan tilgreinds tímaramma.  

## <a name="order-to-order-links-and-past-due-dates"></a>Tenglar á milli pantana og liðnir skiladagar  
Ólíkt flestum framboð-eftirspurn settum eru tengdar pantanir með skiladag á undan upphafsdagsetningu áætlunar áætlaðar að fullu af kerfinu. Viðskiptaástæðan fyrir þessa undanþágu er að tiltekin pör eftirspurnar og framboðs þurfa að vera samstillt fram að framkvæmdinni. Nánari upplýsingar um frosna svæðið sem eiga við um flestar gerðir framboðs og eftirspurnar eru í [Hönnunarupplýsingar: Takast á við pantanir fyrir upphafsdagsetningu áætlunar](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
