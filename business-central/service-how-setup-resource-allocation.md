---
title: Setja upp forðaúthlutun | Microsoft Docs
description: Lærðu hvernig kerfið getur hjálpað til við að tryggja að þú úthlutir þjónustu til einhvers sem hefur nauðsynlega eiginleika til veita hana.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6799f3c92bb41404b4510b03a26601419e2dbb4c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772380"
---
# <a name="set-up-resource-allocation"></a>Setja upp forðaúthlutun
Til að tryggja að þjónustuverkhluti sé framkvæmdur svo vel sé, er mikilvægt að finna tilfang sem er hæft til starfans. Þú getur sett upp [!INCLUDE[prod_short](includes/prod_short.md)] svo það sé auðvelt að úthluta verkinu til einhvers sem er hæfur til þess. Í [!INCLUDE[prod_short](includes/prod_short.md)] er þetta nefnt _Forðaúthlutun_. Hægt er að úthluta til tilfanga út frá hæfni þeirra, tiltækileika, eða hvort þau eru á sama þjónustusvæði og viðskiptamaðurinn. 

Til að  nota forðaúthlutun skal setja upp:  
  
* Nauðsynlega hæfni til að gera við og viðhalda þjónustuvörum. Þú úthlutar þessum til þjónustuvara og tilfanga.  
* Landfræðileg svæði, kölluð svæði, sem þú getur skilgreint fyrir þinn markað. Til dæmis austur, vestur, miðsvæðis og svo framvegis. Þú úthlutar þessum til viðskiptamanna og tilfanga.  
* Hvort á að birta tilföng hæfni og svæði, og hvort á að birta viðvörun er einhver velur óhæft tilfang, eða tilfang sem er ekki á þjónustusvæði viðskiptamanns.  

## <a name="to-set-up-skills"></a>Uppsetning á hæfni
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hæfni** og veldu síðan tengda tengilinn.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Úthluta hæfni til þjónustuvöru og tilfanga
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustuvörur** eða **Tilföng** og veldu síðan tengda tengilinn.  
2. Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:  
  
    * Fyrir þjónustuvöru, velja **Tilföng hæfni**.  
    * Fyrir tilföng, velja **Hæfni**.  

## <a name="to-set-up-zones"></a>Setja upp svæði
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Svæði** og veldu síðan tengda tengilinn.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Úthluta svæðum til viðskiptamanna og tilfanga 
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** eða **Tilföng** og veldu síðan tengda tengilinn.  
2. Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:  
  
    * Fyrir viðskiptamenn, velja svæði í **Þjónustusvæðiskóði** reitnum.  
    * Fyrir tilföng, velja **Þjónustusvæði** aðgerðina.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Tilgreina hvað á að sýna þegar tilfang er valið
1. Veldu táknið ![Ljósapera sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), sláðu inn **Þjónustukerfisgrunnur** og veldu síðan tengda tengilinn. 
2. Í reitnum **Valkostir Tilföng hæfni** skal velja einn af valkostunum sem lýst er í eftirfarandi töflu.  
  
    |**Valkostur**|**Lýsing**|  
    |------------|-------------|  
    |Sýndur kóti | Birtir eingöngu kóða.|  
    |Sýnd viðvörun | Sýnir upplýsingarnar og birtir viðvörun ef þú velur tilfang sem ekki er hæft.|  
    |Ekki notað | Sýnir ekki þessar upplýsingar.|  

## <a name="to-update-resource-capacity"></a>Uppfæra Forðageta  
Ef til vill þarf að breyta forðagetu.  
  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forðageta** og veldu síðan tengda tengilinn.  
2. Veljið tilfang og velja svo aðgerðina **Stilla afkastageta**.  
3. Gera breytingar og velja svo **Uppfæra afkastagetu**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Uppfæra hæfni fyrir vörur, þjónustuvörur, eða þjónustuvöruflokka
Ef þú vilt breyta hæfniskóðum sem vörum hefur verið úthlutað, til dæmis úr **PC** í **PCS**, geturðu gert það annað hvort fyrir vörur eða fyrir allar vörur í þjónustuvöruflokknum.  
  
1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** eða **Þjónustuvörur** eða **Þjónustuvöruflokkar** og veldu síðan tengda hlekkinn.  
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
 



[!INCLUDE[footer-include](includes/footer-banner.md)]