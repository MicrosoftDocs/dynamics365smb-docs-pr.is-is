---
title: Hönnunarupplýsingar - Birgðavirði | Microsoft-skjöl
description: Birgðaverðmat er ákvörðun kostnaðar af birgðavöru.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Hönnunarupplýsingar: Birgðavirðismat
Birgðaverðmat er ákvörðun kostnaðar sem er úthlutað til birgðavara, eins og lýst með eftirfarandi jöfnu.  

Lokabirgðir = uppahafsbirgðir + nettóinnkaup – kostnaður seldra vara  

Útreikning á lagerverðmat notar reitinn **Kostnaðarupphæð (raunverul.)** í verðmæti færslum fyrir vöru. Færslurnar eru flokkaðar eftir gerð sem samsvarar kostnaðarþætti, beinum kostnaði, óbeinum kostnaði, dreifni, endurmat og námundun. Nánari upplýsingar eru í [Upplýsingar um hönnun: kostnaðarhlutar](design-details-cost-components.md).  

Færslur eru jafnaðar hver við aðra, annaðhvort með fastri jöfnun eða samkvæmt almennri kostnaðarflæðisáætlun sem skilgreind er af kostnaðaraðferðinni. Ein færsla birgðaminnkunar getur verið jöfnuð við meira en eina aukningarfærslu með öðrum bókunardagsetningum og mögulega öðru kaupverði. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md). Því byggir útreikningur á birgðavirði fyrir tiltekna dagsetningu á samantekt jákvæðra og neikvæðra virðisfærslna.  

## Skýrsla um verðmætamat birgða  
Til að reikna út birgðavirði í **Birgðavirðisskýrslu** hefst skýrslan með því að reikna verðmæti birgðabreytinga atriðisins á tilteknu upphafsdag. Taflan bætir svo virði birgðaaukningar við og dregur frá virði birgðaminnkunar, upp að uppgefinni lokadagsetningu. Lokaniðurstaðan er birgðavirði á lokadag. Skýrslan reiknar þessi gildi út með því að reikna út samtölu gildanna í reitnum **Kostnaðarupphæð (raunverul)** í gildafærslunum, með því að nota bókunardagsetningar til að afmarka.  

Prentaða skýrslan sýnir alltaf raunupphæðir, þ.e. verðgildi færslna sem hafa verið bókaðar sem reikningsfærðar. Einnig prentar skýrslan væntanlegan kostnað færslna sem bókaðar eru sem mótteknar eða afhentar ef reiturinn Taka væntanlegan kostnað með í flýtiflipanum Valkostir er valinn.  

> [!IMPORTANT]  
>  Gildi í **Birgðavirði** skýrslu er afstemmt við Birgðareikninginn í fjárhag, sem þýðir að virðisfærslur sem um ræðir hafa verið bókaðar í fjárhag.  

> [!IMPORTANT]  
>  Fjárhæðir í dálkunum **Virði** í skýrslunni eru byggðar á bókunardagsetningu færslna fyrir vöru.  

## Verðmætamat birgða - VÍV-skýrsla  
Framleiðslufyrirtæki þarf að velja gildi fyrir þrenns konar birgðir:  

* Hráefnisbirgðir  
* VÍV-birgðir  
* Fullunnar vörur í birgðum  

Gildi VÍV-birgða er ákvarðar samkvæmt eftirfarandi jöfnu.  

* Lokabirgðir VÍV = Upphafsbirgðir VÍV + framleiðslukostnaður – kostnaður framleiddra vara  

Eins og fyrir keyptar birgðir eru virðisfærslur grunnur birgðamats. Útreikningur er gerður því að nota gildin í reitnum **Kostnaðarupphæð (raunverul.)** fyrir vöruna og afkastagildisfærslurnar sem tengjast framleiðslupöntun.  

Tilgangur verðmætamats VÍV-birgða er að ákvarða virði þeirra vara sem framleiðslunni hefur ekki enn verið lokið á tilteknum degi. Því byggist VÍV-birgðavirðið á virðisfærslum tengdum notkun og færslum í afkastahöfuðbók. Reikningsfæra verður notkunarbókarfærslur á matsdegi. Því sýnir **Verðmæti birgða VÍV** skýrslan kostnaðinn sem endurspeglar VÍV-birgðavirðið í tveimur flokkum: notkun og afkastageta.  

## Sjá einnig .  
[Hönnunarupplýsingar: afstemming í fjárhagur](design-details-reconciliation-with-the-general-ledger.md)   
[Hönnunarupplýsingar: Endurmat](design-details-revaluation.md)   
[Hönnunarupplýsingar: staða framleiðslupöntunar](design-details-production-order-posting.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)    
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]