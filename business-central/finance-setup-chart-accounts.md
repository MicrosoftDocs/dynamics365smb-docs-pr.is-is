---
title: Setja upp eða breyta bókhaldslyklum (inniheldur myndskeið)
description: Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn. Hægt er að breyta sjálfgefnum lyklum í bókahaldslyklum og hægt er að bæta við nýjum lyklum.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 01/21/2022
ms.author: edupont
---
# <a name="set-up-or-change-the-chart-of-accounts"></a><a name="set-up-or-change-the-chart-of-accounts"></a><a name="set-up-or-change-the-chart-of-accounts"></a>Setja upp eða breyta bókhaldslyklum

Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki. Hins vegar er hægt að breyta sjálfgefnum lyklum og hægt er að bæta við nýjum lyklum.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a><a name="add-or-change-accounts"></a><a name="add-or-change-accounts"></a>Bæta við eða breyta reikningum

Úr bókhaldslyklinum geturðu opnað hvern fjárhagsreikning og bætt við eða breytt stillingum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Ef þörf krefur er hægt að nota fleiri en eina línu fyrir heiti á fjárhagsreikningi. Á síðunni **Fjárhagsreikningsspjald**, í hópnum **Lykill**, skal velja **Lengdir textar** og síðan fylla út eina eða fleiri línur með heiti lykilsins og afritaðan texta.  

Fylla þarf út reitinn **Samantekt** fyrir reikninga af reikningsgerðinni **Samtals**. Þessi reitur fyllist sjálfkrafa út með inndráttaraðgerðinni fyrir reikninga af gerðinni **Lokasamtala**. Þegar allir lyklar hafa verið settir upp skal velja aðgerðina **Vinna úr** og síðan velja **Inndráttur bókhaldslykla**.  

> [!IMPORTANT]
> Ef skilgreiningar hafa verið færðar í **Samtals**-reitina fyrir **Til-tölu**-reikningana áður en inndráttaraðgerðin er framkvæmd þarf að færa þær inn aftur því að aðgerðin skrifar yfir gildin í öllum **Til-tölu**-reitum.

## <a name="delete-accounts"></a><a name="delete-accounts"></a><a name="delete-accounts"></a>Eyða reikningum

Hægt er að eyða fjárhagsreikningur. Áðu en honum er eytt þarf hins vegar eftirfarandi að vera rétt:  

* Staða reikningsins verður að vera núll.  
* Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur á síðunni **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.  
* Ef reiturinn **Athuga notkun fjárhagsr.** á síðunni **Uppsetning fjárhags** er valinn má ekki nota lykilinn í neinum bókunarflokkum eða bókunargrunnum.  

[!INCLUDE[prod_short](includes/prod_short.md)] kemur í veg fyrir að fjárhagsreikningi sé eytt sem geymir gögn sem þarf í bókhaldslyklinum.  

## <a name="block-deletion-of-gl-accounts"></a><a name="block-deletion-of-gl-accounts"></a><a name="block-deletion-of-gl-accounts"></a>Útiloka eyðingu fjárhagsreikninga

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

2022 útgáfutímabil 2 kynnir aukavörn gegn eyðingu fjárhagsreikninga fyrir slysni jafnvel í sviðsmyndun þar sem skilyrði eru uppfyllt.  

Nýjum reit, **Loka fyrir eyðingu fjárhagsreikninga**, hefur verið bætt við síðuna **Fjárhagsgrunnur**. Þegar stillt er á *Já* virkar reiturinn sem auka staðfesting sem þýðir að þú getur ekki eytt fjárhagsreikningum með fjárhagsfærslum eftir dagsetninguna í reitnum **Athuga eyðingu fjárhagsr. eftir**. Til að eyða slíkum reikningi þarf notandi með aðgang að síðunni **Fjárhagsgrunnur** fyrst að stilla þennan reit á *Nei*.  

Að stilla reitinn **Loka fyrir eyðinga á fjárhagsreikningum** á *Já* er hægt að líta á sem bestu venju, sem og að stilla dagsetninguna í reitnum **Athuga eyðingu fjárhagsr. eftir**, t.d. á dagsetninguna sem þú þarft að vista fjárhagsgögnin þín.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Vinna með víddir](finance-dimensions.md)  
[Flytja inn gögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Vinna með fjárhagsskýrslur](bi-how-work-account-schedule.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Loka lyklum rekstrarreiknings í franskri útgáfu](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Prenta rekstrarreikninga í ástralskri útgáfu](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Prenta rekstrarreikninga í nýsjálenskri útgáfu](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Setja upp og loka stöðum rekstrarreiknings í spænskri útgáfu](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Inndráttur og staðfesting á bókhaldslyklinum í spænskri útgáfu](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
