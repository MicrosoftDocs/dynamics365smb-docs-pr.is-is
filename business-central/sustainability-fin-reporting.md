---
title: Sjálfbærni fjárhagsskýrslugerð
description: Lýsir því hvernig eigi að nota fjárhagsskýrslur til að búa til ýmis yfirlit og skýrslur til að greina gögn um afköst sjálfbærni.
author: altotovi
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: '104, 108, 490'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Greining sjálfbærnifærslna með fjárhagsskýrslum 

Eiginleikinn *Ársskýrslur* veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum fjárhagur (fjárhags)og bera saman fjárhagur færslur við áætlunarfærslur. En einnig er hægt að greina tölfræðileg og sjálfbærnigögn með sama eiginleika og jafnvel sameina allar þrjár gerðir gagna.  

## Skilyrði fyrir fjárhagsskýrslugerð  

Uppsetning fjárhagsskýrslna krefst skilnings á skipulagi gagna sem á að greina. Það eru lykilhugtök sem líklega þarf að vekja athygli á áður en fjárhagsskýrslurnar eru hannaðar: 

1. Bókhaldslykillinn tengist: 
   1. Varpa fjárhagsbókunarreikningum í fjárhagsreikningsflokka. 
   2. Hanna hvernig víddir eru notaðar.
   3. Setja upp fjárhagsáætlanir.  
2. Sjálfbærni tengt:   
   1. Setja upp sjálfbærnireikninga. 
   2. Setja upp kolefnisgjald og CO2e í **útblástursgjöldin**.
   3. Hanna hvernig víddir eru notaðar.  
3. Tengt upplýsingareikningum: 
   1. Setja upp tölfræðilega reikninga. 
   2. Hanna hvernig víddir eru notaðar.  

> [!NOTE]
> Fjárhagsskýrslur vinna ekki beint með CO2, CH4 eða N2O losun. Í stað þess að það notar co2 jafngilda líkanið og það þýðir að fyrst þarf að grunnstilla **CO2e**  (kolefnisjafngildi) á síðunni **Losunargjöld** .  

> [!NOTE]
> Hér má finna fleiri óskir um notkun Fjárhagsskýrslna með fjárhagsgögnum og bókhaldslykli hér [Byggja upp fjárhagsskýrslur með því að nota fjárhagsgögn og reikningsflokka](bi-how-work-account-schedule.md).   

## Stofna nýja fjárhagsskýrslu  

Til að búa til eigin fjárhagsskýrslur á fljótlegan hátt skal byrja á því að afrita eldri skýrslur, eins og lýst er í skrefi 3 hér á eftir. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.  
2. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti fjárhagsskýrslu.  
3. Stutt heiti skýrslunnar er fært inn í **reitinn Heiti**  (ekki er hægt að breyta heitinu síðar) og færa inn **Lýsing**.  
4. Velja skal línuskilgreining og dálkskilgreining.   
5.  **Veljið Breyta skýrsluskilgreining**  aðgerð til að fá aðgang að fleiri eiginleikum fjárhagsskýrslunnar.  
6. Á flýtiflipanum **Valkostir** er hægt að breyta skýrslulýsingunni, breyta línu- og dálkaskilgreiningum og skilgreina hvernig eigi að sýna dagsetningar. Dagsetningar geta verið dag- og viku-/mánaðar-/ársfjórðungsstigveldi eða notað reikningstímabil. Nánari upplýsingar eru notaðar í Samanburður á reikningstímabilum með því að [nota reiknireglur tímabila](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas). 
7. Á flýtiflipanum **Víddir** er hægt að skilgreina víddarafmarkanir fyrir skýrsluna.  
8. Hægt er að forútgáfa skýrsluna á svæðinu fyrir neðan **flýtiflipann Víddir** .   

Ef greina á sjálfbærni- eða tölfræðigögn er hægt að ná því með því að setja upp **línuskilgreining**.  

Til að stofna eða breyta línuskilgreining skal fylgja skrefunum:

1. Á síðunni **Fjárhagsskýrslur** skal velja viðeigandi fjárhagsskýrslu og velja **síðan Breyta línuskilgreining**  aðgerð. 
2. Setja upp línur eins og í eftirfarandi skrefum.  

> [!NOTE]
> **Línan nr.** reiturinn sýnir fyrstu 10 stafina í kennimerki, eins og reikningsnúmer. Ef einingum með kennum sem byrja á sömu 10 stöfum er bætt við eru tvítekningar í reitnum **Línunr.** . Ef þörf er á er hægt að breyta kennimerkjum handvirkt eftir að þú hefur sett inn einingarnar. Öll kennimerkin eru birt í reitnum **Samantekt**.

> [!NOTE]
> Hægt er að sameina allar **tegundir** samtölu, þ.e. Bókunarreikningar, Súsanna. Reikningar, Upplýsingareikningur.

> [!NOTE]
> Línuskilgreiningar eru ekki útgáfaðar. Þegar línuskilgreining er breytt er gömlu útgáfunni skipt út og breytingarnar verða vistaðar í gagnagrunninum. 

### Greining sjálfbærnigagna  

1. Reiturinn Línunr. er **færður inn.** Til að auðkenna hráa og bæta við **lýsingu** sem texta sem birtist í fjárhagsskýrslulínunni. 
2. Í dálknum Tegund samantektar skal velja Viðskm **. Valkosturinn Reikningar** .   
3. Í reitnum Samantekt skal velja einn eða fleiri sjálfbærnireikninga með öllum viðeigandi afmörkunum. 
4. Í reitnum **Tegund upphæðar** er valinn einn af kostunum:   
   1. **CO2e** ef tilkynna á CO2 jafngildi úr reitnum **CO2e Losun** í **sjálfbærnibókarfærslunum**. 
   2. **Kolefnisgjald** ef gefa á skýrslu um fjárhagslegt jafngildi (kolefnisgjald) úr reitnum **Kolefnisgjald** í **sjálfbærnifærslunum**. 
5. Ef Reikniregla **er valin** sem **Tegund** samantektar er hægt að nota stærðfræðilegar reiknireglur í dálknum **Samantekt** .  

### Greining tölfræðilegra gagna

1. Reiturinn Línunr. er **færður inn.** Til að auðkenna línuna og bæta við **lýsingu** sem texta sem birtist í fjárhagsskýrslulínunni. 
2. Í dálknum **Tegund** samantektar er valkosturinn **Upplýsingareikningar** valinn.   
3. Í reitnum **Samantekt** skal velja einn eða fleiri sjálfbærnireikninga með öllum viðeigandi afmörkunum. 
4. Ef Reikniregla **er valin** sem **Tegund** samantektar er hægt að nota stærðfræðilegar reiknireglur í dálknum **Samantekt** .  

## Sjá einnig .

[Yfirlit yfir sjálfbærnistjórnun](finance-manage-sustainability.md)    
[Sjálfbærniskýrslur og greiningar í Business Central](sustainability-reports.md)   
[API sjálfbærni](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Undirbúa fjárhagsskýrslugerð](bi-how-work-account-schedule.md)    
[línuskilgreining í fjárhagsskýrslugerð](bi-row-definitions.md)    
[dálkskilgreining í fjárhagsskýrslugerð](bi-column-definitions.md)    
[Fjármál](finance.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
