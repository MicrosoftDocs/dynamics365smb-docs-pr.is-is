---
title: "Hönnunarupplýsingar - Birgðavirði | Microsoft Docs"
description: "Birgðaverðmat er ákvörðun kostnaðar sem er úthlutað til birgðavara, eins og lýst með eftirfarandi jöfnu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8276d7362fb940c70573f14ac10b8f02d3e145e4
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inventory-valuation"></a>Hönnunarupplýsingar: Birgðavirði
Birgðaverðmat er ákvörðun kostnaðar sem er úthlutað til birgðavara, eins og lýst með eftirfarandi jöfnu.  

Lokabirgðir = uppahafsbirgðir + nettóinnkaup – kostnaður seldra vara  

Útreikning á lagerverðmat notar reitinn **Kostnaðarupphæð (raunverul.)** í verðmæti færslum fyrir vöru. Færslurnar eru flokkaðar eftir gerð sem samsvarar kostnaðarþætti, beinum kostnaði, óbeinum kostnaði, dreifni, endurmati og námundun. Nánari upplýsingar eru í [Upplýsingar um hönnun: kostnaðarhlutar](design-details-cost-components.md).  

Færslur eru jafnaðar hver við aðra, annaðhvort með fastri jöfnun XE „Jöfnun; Föst“ eða samkvæmt almennri kostnaðarflæðisáætlun sem skilgreind er af kostnaðaraðferðinni XE „Aðferð; Kostnaður“  XE „Kostnaðaraðferð“. Ein færsla birgðaminnkunar getur verið jöfnuð við meira en eina aukningarfærslu með öðrum bókunardagsetningum og mögulega öðru kaupverði. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md). Því byggir útreikningur á birgðavirði fyrir tiltekna dagsetningu á samantekt jákvæðra og neikvæðra virðisfærslna.  

## <a name="inventory-valuation-report"></a>Birgðavirðisskýrsla  
Til að reikna út birgðavirði í **Birgðavirðisskýrslu** hefst skýrslan með því að reikna verðmæti birgðabreytinga atriðisins á tilteknu upphafsdag. Taflan bætir svo virði birgðaaukningar við og dregur frá virði birgðaminnkunar, upp að uppgefinni lokadagsetningu. Lokaniðurstaðan er birgðavirði á lokadag. Skýrslan reiknar þessi gildi út með því að reikna út samtölu gildanna í reitnum **Kostnaðarupphæð (raunverul)** í gildafærslunum, með því að nota bókunardagsetningar til að afmarka.  

Prentaða skýrslan sýnir alltaf raunupphæðir, þ.e. verðgildi færslna sem hafa verið bókaðar sem reikningsfærðar. Í skýrslunni er einnig prentaður væntanlegur kostnaður fyrir færslur sem bókaðar eru sem mótteknar eða afhentar ef gátmerki er valið í reitnum Taka með væntanl. kostn. á flýtiflipanum Valkostir.  

> [!IMPORTANT]  
>  Gildi í **Birgðavirði** skýrslu er afstemmt við Birgðareikninginn í fjárhag, sem þýðir að virðisfærslur sem um ræðir hafa verið bókaðar í fjárhag.  

> [!IMPORTANT]  
>  Fjárhæðir í dálkunum **Virði** í skýrslunni eru byggðar á bókunardagsetningu færslna fyrir vöru.  

## <a name="inventory-valuation---wip-report"></a>Birgðavirði - VÍV-skýrsla  
Framleiðslufyrirtæki þarf að velja gildi fyrir þrenns konar birgðir:  

* Hráefnisbirgðir  
* VÍV-birgðir  
* Fullunnar vörur í birgðum  

Gildi VÍV-birgða er ákvarðar samkvæmt eftirfarandi jöfnu.  

* Lokabirgðir VÍV = Upphafsbirgðir VÍV + framleiðslukostnaður – kostnaður framleiddra vara  

Eins og fyrir keyptar birgðir eru virðisfærslur grunnur birgðamats. Útreikningur er gerður því að nota gildin í reitnum **Kostnaðarupphæð (raunverul.)** fyrir vöruna og afkastagildisfærslurnar sem tengjast framleiðslupöntun.  

Tilgangurinn með VÍV-verðmati á birgðum er að ákvarða virði þeirra vara sem ekki eru enn fullunnar á tiltekinni dagsetningu. Því byggist VÍV-birgðavirðið á virðisfærslum tengdum notkun og færslum í afkastahöfuðbók. Fjárhagsfærslur um notkun verða að vera að fullu reikningsfærðar á dagsetningu fullgildingar. Því sýnir **Verðmæti birgða VÍV** skýrslan kostnaðinn sem endurspeglar VÍV-birgðavirðið í tveimur flokkum: notkun og afkastageta.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: afstemming í fjárhag](design-details-reconciliation-with-the-general-ledger.md)   
[Hönnunarupplýsingar: Endurmat](design-details-revaluation.md)   
[Hönnunarupplýsingar: Bókun framleiðslupöntunar](design-details-production-order-posting.md)
[Stjórna birgðakostnaði](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

