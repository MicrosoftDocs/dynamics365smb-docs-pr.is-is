---
title: Setja upp bókhaldslykil (inniheldur Video)
description: Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn. Hægt er að breyta sjálfgefnum lyklum í bókahaldslyklum og hægt er að bæta við nýjum lyklum.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: f2ef4432d91d9f647a4bea58febbdfd5513a4350
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520283"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Setja upp eða breyta bókhaldslykli

Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.
Hins vegar er hægt að breyta sjálfgefnum lyklum og hægt er að bæta við nýjum lyklum.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Bæta við eða breyta lyklum

Fyrir hvern bókhaldslykil er hægt að opna hvern einstakan fjárhagslykil og bæta við eða breyta stillingum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Ef þörf krefur er hægt að nota fleiri en eina línu fyrir heiti á fjárhagsreikningi. Á síðunni **Fjárhagsspjald**, í hópnum **Lykill**, skal velja **Lengdir textar** og síðan fylla út eina eða fleiri línu með sem textanum sem á að afrita og heiti lykilsins.  

Fylla þarf út reitinn **Samantekt** fyrir reikninga af reikningsgerðinni **Samtals**. Þessi reitur fyllist sjálfkrafa út með inndráttaraðgerðinni fyrir reikninga af gerðinni **Lokasamtala**. Þegar allir lyklar hafa verið settir upp skal velja **Vinna úr** og síðan velja **Inndráttur bókhaldslykla**.  

> [!IMPORTANT]
> Ef skilgreiningar hafa verið færðar í **Samtals**-reitina fyrir **Til-tölu**-reikningana áður en inndráttaraðgerðin er framkvæmd þarf að færa þær inn aftur því að aðgerðin skrifar yfir gildin í öllum **Til-tölu**-reitum.

## <a name="delete-accounts"></a>Eyða lyklum

Hægt er að eyða fjárhagsreikningur. Áðu en honum er eytt þarf hins vegar eftirfarandi að vera rétt:  

* Staða reikningsins verður að vera núll.  
* Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur á síðunni **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.  
* Ef reiturinn **Athuga notkun fjárhagsr.** á síðunni **Uppsetning fjárhags** er valinn má ekki nota lykilinn í neinum bókunarflokkum eða bókunargrunnum.  

[!INCLUDE[prod_short](includes/prod_short.md)] kemur í veg fyrir að fjárhagsreikningi sé eytt sem geymir gögn sem þarf í bókhaldslyklinum.  

## <a name="block-deletion-of-gl-accounts"></a>Útiloka eyðingu fjárhagsreikninga

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

2022 losun bylgjupappa 2 kynnir viðbótarvörn gegn eyðingu á fjárhagsreikningum, jafnvel í atburðarás þar sem skilyrði eru uppfyllt.  

Nýtt svæði, **bálki við eyðingu fjárhagsreikninga**, er bætt **á síðuuppsetningarsíðu** fjárhags. Svæðið vinnur sem viðbótarvilluleit þegar notandi reynir að eyða lykli þar sem færslur eru eftir dagsetninguna sem er tilgreind í **reitnum kanna eyðingu** Fjárhagsreikn.

**Þegar bálki reitanna eyðing fjárhagsreikninga** er stilltur á *Já* er ekki hægt að eyða fjárhagsreikningum sem eru með færslur eftir dagsetninguna í **reitnum kanna g/h-Reikn.** Til þess að eyða slíkum reikningi þarf notandi með aðgang að **á uppsetningarsíðu** fjárhags fyrst að stilla þetta svæði á *Nr*. Þá er hægt að eyða reikningnum.  

Mælt er **með því að setja blokkun í reitinn Fjárhagsreikningur** á *Já*. Við mælum einnig með að þú hafir alltaf dagsetningar sem er sett í **reitinn ávísun Fjárhagsreikn., eftir** svæði, til dæmis þann tíma sem þú verður að þurfa til að geyma fjármálagögnin þín.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Vinna með víddir](finance-dimensions.md)  
[Flytja inn gögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Vinna með fjárhagsskemu](bi-how-work-account-schedule.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Loka lyklum rekstrarreiknings í franskri útgáfu](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Prenta rekstrarreikninga í ástralskri útgáfu](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Prenta rekstrarreikninga í nýsjálenskri útgáfu](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Setja upp og loka stöðum rekstrarreiknings í spænskri útgáfu](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Inndráttur og staðfesting á bókhaldslyklinum í spænskri útgáfu](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]