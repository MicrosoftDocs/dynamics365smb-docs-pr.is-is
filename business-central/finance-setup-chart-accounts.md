---
title: Setja upp eða breyta bókhaldslyklum (inniheldur myndskeið)
description: Lærðu um að setja upp reikningsyfirlit þitt (COA) til að sýna fjárhagsreikninga sem geyma fjárhagsgögnin þín.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 12/19/2023
ms.custom: bap-template
---
# Setja upp eða breyta bókhaldslyklum

Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki. Hins vegar er hægt að breyta sjálfgefnum lyklum og hægt er að bæta við nýjum lyklum.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## Bæta við eða breyta reikningum

Úr bókhaldslyklinum geturðu opnað hvern fjárhagsreikning og bætt við eða breytt stillingum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Ef þörf krefur er hægt að nota fleiri en eina línu fyrir heiti á fjárhagsreikningi. Á síðunni **Fjárhagsreikningsspjald**, í hópnum **Lykill**, skal velja **Lengdir textar** og síðan fylla út eina eða fleiri línur með heiti lykilsins og afritaðan texta.  

Fylla þarf út reitinn **Samantekt** fyrir reikninga af reikningsgerðinni **Samtals**. Þessi reitur fyllist sjálfkrafa út með inndráttaraðgerðinni fyrir reikninga af gerðinni **Lokasamtala**. Þegar allir lyklar hafa verið settir upp skal velja aðgerðina **Vinna úr** og síðan velja **Inndráttur bókhaldslykla**.  

> [!IMPORTANT]
> Ef skilgreiningar hafa verið færðar í **Samtals**-reitina fyrir **Til-tölu**-reikningana áður en inndráttaraðgerðin er framkvæmd þarf að færa þær inn aftur því að aðgerðin skrifar yfir gildin í öllum **Til-tölu**-reitum.

## Eyða reikningum

Hægt er að eyða fjárhagsreikningur. Áðu en honum er eytt þarf hins vegar eftirfarandi að vera rétt:  

* Staða reikningsins verður að vera núll.  
* Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur á síðunni **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.  
* Ef reiturinn **Athugaðu notkun bókhaldsreiknings**  á síðunni **General Ledger Setup** er valinn, má reikningurinn ekki hægt að nota í hvaða pósthópum sem er eða póstuppsetningu.  

[!INCLUDE[prod_short](includes/prod_short.md)] kemur í veg fyrir að fjárhagsreikningi sé eytt sem geymir gögn sem þarf í bókhaldslyklinum.  

Þú getur líka tilgreint hvenær á að leyfa fólki að eyða reikningum. Á síðunni **General Ledger Setup** vinnur **Loka á eyðingu stórreikninga** víxlans ásamt dagsetningunni í the **Athugaðu G/L Acc. Eyði eftir** reitnum til að virka sem auka staðfesting. Ef þú kveikir á **Loka á eyðingu aðalreikninga** rofa geturðu ekki eytt aðalbókarreikningum með höfuðbókarfærslum eftir dagsetninguna í **Athugaðu bókhaldsreikning. Eyðing Eftir** reit. Til að eyða slíkum reikningi verður einhver með aðgang að  **General Ledger Setup** síðunni að slökkva á  **Loka á eyðingu stórreikninga** skipta.  

Að kveikja á reitnum **Loka á eyðingu bókhaldsreikninga** er oft ákjósanlegt, sem og að stilla dagsetninguna í **Athugaðu bókhald . Eyðing Eftir** reitnum, til dæmis til dagsins þar sem reglur krefjast þess að þú geymir fjárhagsgögn.  

### Vídeó leiðsögn

Þetta myndband sýnir hvernig á að tilgreina hvort og hvenær fólk geti eytt heimilisreikningum.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## Sjá einnig

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
