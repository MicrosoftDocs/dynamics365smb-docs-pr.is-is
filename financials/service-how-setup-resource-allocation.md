---
title: "Setja upp forðaúthlutun | Microsoft Docs"
description: "Lærðu hvernig kerfið getur hjálpað til við að tryggja að þú úthlutir þjónustu til einhvers sem hefur nauðsynlega eiginleika til veita hana."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b16ba9366aefc108f39667678fe8ab70ce421b83
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-resource-allocation"></a>Setja upp forðaúthlutun
Til að tryggja að þjónustuverkhluti sé framkvæmdur svo vel sé, er mikilvægt að finna tilfang sem er hæft til starfans. Þú getur sett upp [!INCLUDE[d365fin](includes/d365fin_md.md)] svo það sé auðvelt að úthluta verkinu til einhvers sem er hæfur til þess. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er þetta nefnt _Forðaúthlutun_. Hægt er að úthluta til tilfanga út frá hæfni þeirra, tiltækileika, eða hvort þau eru á sama þjónustusvæði og viðskiptamaðurinn. 

Til að  nota forðaúthlutun skal setja upp:  
  
* Nauðsynlega hæfni til að gera við og viðhalda þjónustuvörum. Þú úthlutar þessum til þjónustuvara og tilfanga.  
* Landfræðileg svæði, kölluð svæði, sem þú getur skilgreint fyrir þinn markað. Til dæmis austur, vestur, miðsvæðis og svo framvegis. Þú úthlutar þessum til viðskiptamanna og tilfanga.  
* Hvort á að birta tilföng hæfni og svæði, og hvort á að birta viðvörun er einhver velur óhæft tilfang, eða tilfang sem er ekki á þjónustusvæði viðskiptamanns.  

## <a name="to-set-up-skills"></a>Uppsetning á hæfni
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hæfni** og velja svo viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Úthluta hæfni til þjónustuvöru og tilfanga
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuvörur** eða **Tilföng** og velja svo viðeigandi tengil.  
2. Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:  
  
    * Fyrir þjónustuvöru, velja **Tilföng hæfni**.  
    * Fyrir tilföng, velja **Hæfni**.  

## <a name="to-set-up-zones"></a>Setja upp svæði
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Svæði** og velja svo viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Úthluta svæðum til viðskiptamanna og tilfanga 
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Viðskiptamenn** eða **Tilföng** og velja svo viðeigandi tengil.  
2. Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:  
  
    * Fyrir viðskiptamenn, velja svæði í **Þjónustusvæðiskóði** reitnum.  
    * Fyrir tilföng, velja **Þjónustusvæði** aðgerðina.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Tilgreina hvað á að sýna þegar tilfang er valið
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning þjónustu** og velja svo viðeigandi tengil. 
2. Í reitnum **Valkostir Tilföng hæfni** skal velja einn af valkostunum sem lýst er í eftirfarandi töflu.  
  
    |**Valkostur**|**Lýsing**|  
    |------------|-------------|  
    |Sýndur kóti | Birtir eingöngu kóða.|  
    |Sýnd viðvörun | Sýnir upplýsingarnar og birtir viðvörun ef þú velur tilfang sem ekki er hæft.|  
    |Ekki notað | Sýnir ekki þessar upplýsingar.|  

## <a name="to-update-resource-capacity"></a>Uppfæra Forðageta  
Ef til vill þarf að breyta forðagetu.  
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Forðageta** og velja svo viðeigandi tengil.  
2. Veljið tilfang og velja svo aðgerðina **Stilla afkastageta**.  
3. Gera breytingar og velja svo **Uppfæra afkastagetu**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Uppfæra hæfni fyrir vörur, þjónustuvörur, eða þjónustuvöruflokka
Ef þú vilt breyta hæfniskóðum sem vörum hefur verið úthlutað, til dæmis úr **PC** í **PCS**, geturðu gert það annað hvort fyrir vörur eða fyrir allar vörur í þjónustuvöruflokknum.  
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** eða **Þjónustuvara**, eða **Þjónustuvöruflokkur** og velja svo viðeigandi tengil.  
2. Veljið tilfang og velja svo aðgerðina **Forðahæfni**.  
3. Í línunni með kótanum sem á að breyta, í reitnum **Hæfniskóti** skal velja viðeigandi hæfniskóta.  
4.  Ef þjónustuvörur tengjast vörunni opnast gluggi með eftirfarandi tveimur valkostum:  
  
    * Breyta sérþekkingarkótunum í valið gildi: þessi kostur er valinn ef skipta skal á gamla og nýja kótanum í öllum tengdum þjónustuvörum.  
    * Eyða sérþekkingarkótunum eða uppfæra tengsl þeirra: Þessi kostur er valinn ef aðeins á að breyta sérþekkingarkótanum í þessari vöru. Sérþekkingarkótanum í tengdum þjónustuvörum verður endurúthlutað, það er, reiturinn **Úthlutað frá** verður uppfærður.  
  
## <a name="see-also"></a>Sjá einnig
[Úthluta forða](service-how-to-allocate-resources.md)  
[Setja upp vinnustundir og þjónustustundir](service-how-setup-work-service-hours.md)  
[Setja upp bilanatilkynningar](service-how-setup-fault-reporting.md)  
[Setja upp Kóta fyrir Staðlaða þjónustu](service-how-setup-service-coding.md)  
 


