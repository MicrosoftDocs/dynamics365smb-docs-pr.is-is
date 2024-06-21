---
title: Setja upp eða breyta bókhaldslykli
description: Fræðast um uppsetningu bókhaldslykils (COA) með fjárhagsreikningum sem geyma fjárhagsgögnin.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Setja upp eða breyta bókhaldslykli

Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki. Hins vegar er hægt að breyta sjálfgefnum lyklum og hægt er að bæta við nýjum lyklum.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## Bæta við eða breyta reikningum

Úr bókhaldslyklinum geturðu opnað hvern fjárhagsreikning og bætt við eða breytt stillingum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Ef þörf krefur er hægt að nota fleiri en eina línu fyrir heiti á fjárhagsreikningi. Á síðunni **Fjárhagsreikningsspjald**, í hópnum **Lykill**, skal velja **Lengdir textar** og síðan fylla út eina eða fleiri línur með heiti lykilsins og afritaðan texta.  

Fylla þarf út reitinn **Samantekt** fyrir reikninga af reikningsgerðinni **Samtals**. Þessi reitur fyllist sjálfkrafa út með inndráttaraðgerðinni fyrir reikninga af gerðinni **Lokasamtala**. Þegar reikningarnir hafa verið settir upp skal velja aðgerðina **Vinna** og velja **síðan Þrefalda bókhaldslykil**.  

> [!IMPORTANT]
> Ef skilgreiningar hafa verið færðar í **Samtals**-reitina fyrir **Til-tölu**-reikningana áður en inndráttaraðgerðin er framkvæmd þarf að færa þær inn aftur því að aðgerðin skrifar yfir gildin í öllum **Til-tölu**-reitum.

## Eyða reikningum

Hægt er að eyða fjárhagsreikningur. Áður en henni er eytt verða hins vegar eftirfarandi skilyrði að vera rétt:  

* Staða reikningsins verður að vera núll.  
* Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur á síðunni **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.  
* Ef reiturinn **Kanna notkun fjárhagsreiknings** á síðunni **Fjárhagsgrunnur** er valinn má ekki nota reikninginn í neinum bókunarflokkum eða bókunargrunni.  

[!INCLUDE[prod_short](includes/prod_short.md)] kemur í veg fyrir að fjárhagsreikningi sé eytt sem geymir gögn sem þarf í bókhaldslyklinum.  

Einnig er hægt að tilgreina hvenær leyfa eigi fólki að eyða reikningum. Á síðunni **Fjárhagsgrunnur** **virkar lokað á eyðingu fjárhagsreikninga** ásamt dagsetningunni í reitnum **Eyðing fjárhagsreikn. eftir** að hafa unnið sem aukaprófun. Ef kveikt er á **vísbendingu um eyðingu fjárhagsreikninga** er ekki hægt að eyða fjárhagsreikningum með fjárhagsfærslum eftir dagsetninguna í reitnum Eyðing fjárhagsreikninga eftir **dagsetninguna í reitnum** Eyðing fjárhagsreikninga. Til að eyða slíkum reikningi verður einhver með aðgang að síðunni **Fjárhagsgrunnur** að slökkva á **vísbið um eyðingu fjárhagsreikninga** .  

Best er að kveikja á reitnum **Loka eyðingu fjárhagsreikninga**, eins og að stilla dagsetninguna í reitnum **Eyðing fjárhagsreikn. eftir**, til dæmis til dagsetningarinnar þar sem reglugerðir krefjast þess að geyma fjárhagsgögn.  

### Vídeóleiðbeiningar

Þetta myndband sýnir hvernig á að tilgreina hvort og hvenær, fólk getur eytt fjárhagsreikningum.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## Námsleið: Setja upp bókhaldslykil í Dynamics 365 Business Central

Viltu læra hvernig bókhaldslykillinn [!INCLUDE [prod_short](includes/prod_short.md)] er settur upp? Byrja síðan á eftirfarandi námsleið [Setja upp bókhaldslykil í Dynamics 365 Business Central](/training/modules/chart-accounts-dynamics-365-business-central).

## Sjá einnig .

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
