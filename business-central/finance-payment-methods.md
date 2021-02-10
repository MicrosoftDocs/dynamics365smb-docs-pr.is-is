---
title: Setja upp greiðsluhætti
description: Greiðsluhættir eru notaðir, til dæmis ávísun, bankamillifærsla, reiðufé eða PayPal, til að tilgreina hvernig sölu- og innkaupareikningar verða greiddir.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 01/21/2021
ms.author: bholtorf
ms.openlocfilehash: 78e754998c7adc871b57347ff0bed714db8cc83f
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035357"
---
# <a name="set-up-payment-methods"></a>Setja upp greiðsluhætti

Greiðsluhættir skilgreina hvernig þú vilt að viðskiptavinir greiði þér og hvernig þú vilt greiða lánardrottnum þínum. Greiðslumátinn getur verið breytilegur fyrir hvern viðskiptavin eða lánardrottin. Dæmi um dæmigerða greiðsluhætti eru **banki**, **reiðufé**, **ávísun** eða **reikningur**.

Þú getur úthlutað greiðslumáta til viðskiptavina og lánardrottna þannig að sama aðferðin sé alltaf notuð á sölu- og innkaupskjölunum sem þú býrð til fyrir þá. Hægt er að breyta greiðslumátanum í sölu- og innkaupaskjalinu ef þörf krefur. Til dæmis, ef þú vilt greiða ákveðinn innkaupareikning í reiðufé frekar en með ávísun. Þetta breytir ekki sjálfgefna greiðslumátanum sem lánardrottninum er úthlutað.

Sömu greiðsluaðferðir eru notaðar fyrir sölu- og innkaupaskjöl. Til dæmis er greiðslumátinn _reiðufé_ notaður bæði þegar þú greiðir og þegar þú færð greitt. [!INCLUDE[prod_short](includes/prod_short.md)] veit að þegar þú ert að búa til sölureikning þá býstu við að fá greiðslur og hið gagnstæða fyrir innkaupareikninga.

Kreditreikningar vegna skila eru þó undantekningar vegna þess að peningar flæða í gagnstæða átt, frá þér til viðskiptavina og frá lánardrottni til þín. Þess vegna er sjálfgefnum greiðslumáta ekki úthlutað á kreditreikninga. Það er hins vegar til hjáleið ef þú hefur tilgreint greiðsluskilmála fyrir viðskiptavin eða lánardrottin. Þótt reiturinn **Reikna greiðsluafsl. af kreditreikn.** er ekki ætlaður fyrir þetta, ef þú velur gátreitinn á síðunni **Greiðsluskilmálar**, verður sjálfgefnum greiðslumáta bætt við þegar þú stofnar kreditreikning. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Greiðsluaðferðir settar upp

[!INCLUDE[prod_short](includes/prod_short.md)] veitir nokkrar greiðsluaðferðir sem fyrirtæki nota oft. Þó er hægt að bæta við eins mörgum og þörf krefur.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslumáti** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Þú getur einnig bætt við greiðsluskilmálum við greiðslumátann þinn. Nánari upplýsingar um það eru í [Setja upp greiðsluskilmála](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Viðskiptavinum eða lánardrottnum úthlutaður greiðslumáti

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamaður** eða **Lánardrottinn** og veldu síðan tengda tengilinn.
2. Í reitnum **Kóði greiðslumáta** skal velja greiðslumátann sem á að nota að sjálfgefnu viðskiptavin eða lánardrottin.

## <a name="see-also"></a>Sjá einnig

[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Setja upp greiðsluskilmála](finance-payment-terms.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
