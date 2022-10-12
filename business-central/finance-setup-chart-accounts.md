---
title: Setja upp eða breyta bókhaldslykli (inniheldur Video)
description: Bókhaldslykillinn (COA) sýnir fjárhagslyklunum sem geyma fjárhagsgögnin þín. Hægt er að breyta sjálfgefnum lyklum í bókahaldslyklum og hægt er að bæta við nýjum lyklum.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: 15eca1f6bc4a75ca6758e5be351d4a459226ac5b
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606695"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Setja upp eða breyta bókhaldslykli

Bókhaldslykillinn (COA) sýnir fjárhagslyklunum sem geyma fjárhagsgögnin þín. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlað GREIÐSLUKERFI sem er tilbúið til að styðja við viðskipti þín. Hins vegar er hægt að breyta sjálfgefnum lyklum og bæta við nýjum lyklum.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Bæta við eða breyta lyklum

Í GREIÐSLUKERFI er hægt að opna hvern almennan fjárhag (fjárhagsreikning) og bæta við eða breyta stillingum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Ef þörf krefur er hægt að nota fleiri en eina línu fyrir heiti á fjárhagsreikningi. **Á síðunni Fjárhagsreikningur korta**, í **lykilflokknum**, skal velja **lengda texta** og síðan fylla út eina eða fleiri línur með reikningsheiti og afrituðum texta.  

Fylla þarf út reitinn **Samantekt** fyrir reikninga af reikningsgerðinni **Samtals**. Þessi reitur fyllist sjálfkrafa út með inndráttaraðgerðinni fyrir reikninga af gerðinni **Lokasamtala**. Eftir að allir lyklar hafa verið settir upp skal velja **vinnsluaðgerðina** og velja **síðan inndrátt bókhaldslykil**.  

> [!IMPORTANT]
> Ef skilgreiningar hafa verið færðar í **Samtals**-reitina fyrir **Til-tölu**-reikningana áður en inndráttaraðgerðin er framkvæmd þarf að færa þær inn aftur því að aðgerðin skrifar yfir gildin í öllum **Til-tölu**-reitum.

## <a name="delete-accounts"></a>Eyða lyklum

Hægt er að eyða fjárhagsreikningur. Áðu en honum er eytt þarf hins vegar eftirfarandi að vera rétt:  

* Staða reikningsins verður að vera núll.  
* Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur á síðunni **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.  
* Ef reiturinn **Athuga notkun fjárhagsr.** á síðunni **Uppsetning fjárhags** er valinn má ekki nota lykilinn í neinum bókunarflokkum eða bókunargrunnum.  

[!INCLUDE[prod_short](includes/prod_short.md)] hindrar að þú eyðir almennum fjárhagslykli sem geymir gögn sem þarf í bókhaldslykilinn.  

## <a name="block-deletion-of-gl-accounts"></a>Útiloka eyðingu fjárhagsreikninga

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

2022 losun bylgjupappa 2 kynnir viðbótarvörn gegn eyðingu á fjárhagsreikningum, jafnvel í atburðarás þar sem skilyrði eru uppfyllt.  

Nýjum reit, **bálki fyrir fjárhagsreikninga**, hefur verið bætt **við á uppsetningarsíðu** fjárhags. Þegar stillt er á *Já*, virkar svæðið sem auka villuleit, sem þýðir að ekki er hægt að eyða fjárhagsreikningum með færslum eftir dagsetninguna í **reitnum kanna g/h Reikn.** Til að eyða slíkum lykli þarf notandi með aðgang að **á uppsetningarsíðu** fjárhags fyrst að stilla þetta svæði á *Nr*.  

**Ef lokað hefur verið fyrir lokun reitanna fjárhagsreikningar** á *Já* má telja þá bestu framkvæmd eins og er að setja dagsetninguna í **reitinn kanna fjárhagsupplýsingar eftir** til dæmis til að geyma gögnin sem notandi hefur krafist til að vista gögn um fjármál.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Vinna með víddir](finance-dimensions.md)  
[Flytja inn gögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Vinna með ársskýrslur](bi-how-work-account-schedule.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Loka lyklum rekstrarreiknings í franskri útgáfu](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Prenta rekstrarreikninga í ástralskri útgáfu](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Prenta rekstrarreikninga í nýsjálenskri útgáfu](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Setja upp og loka stöðum rekstrarreiknings í spænskri útgáfu](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Inndráttur og staðfesting á bókhaldslyklinum í spænskri útgáfu](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
