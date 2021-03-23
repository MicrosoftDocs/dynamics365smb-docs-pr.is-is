---
title: Setja upp og gefa út KPI-vefþjónustu fyrir fjárhagsskemu | Microsoft Docs
description: Í þessu efnisatriði er því lýst hvernig skuli sýna KPI-gögn fjárhagsskema byggt á tilteknum fjárhagsskemum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a5125b1989c5e8d6acd82ba88457f7c846deb83b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382555"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum
Á síðunni **Uppsetning Fjárhagsskema KPI netþjónustu** getur þú ákveðið hvernig skal sýna KPI gögn fjárhagsskema og á hvaða einstaka fjárhagsskemum skuli byggja afkastavísa. Þegar þú velur **Birta netþjónustu** hnappinn bætast KPI gögn fjárhagsskema á lista yfir vefþjónustu sem birt hefur verið á síðunni **Vefþjónusta**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Til að setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning vefþjónustu fyrir KPI fyrir fjárhagsskema** og veldu síðan tengda tengilinn.  
2.  Á flýtiflipanum **Almennt** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Forspárgildi hefjast**|Tilgreinið á hvaða tímapunkti áætluðu gildin eru sýnd á mynd KPI fyrir fjárhagsskema.<br /><br /> Spárgildin eru sótt í fjárhagsáætlun sem þú velur reitnum **Heiti fjárhagsáætlunar**. **Athugið:**  Til að fá afkastavísana sem sýna spárgildin eftir tiltekna dagsetningu og raungildin fyrir dagsetninguna, geturðu breytt reitnum **Leyfa bókun frá** á síðunni **Uppsetning Fjárhags**. Frekari upplýsingar, sjá Leyfa bókun frá|  
    |**Heiti fjárhagsáætl.**|Tilgreinið heiti fjárhagsáætlunarinnar sem veitir áætluð gildi fyrir KPI-vefþjónustu fjárhagsskemans.|  
    |**Tímabil**|Tilgreinið tímabilið sem KPI-vefþjónusta fjárhagsskemans er byggð á.|  
    |**Skoða eftir**|Tilgreinið hvaða tímabil á að nota til að sýna KPI fyrir fjárhagsskema.|  
    |**Heiti vefþjónustu**|Tilgreinið heiti KPI-vefþjónustu fyrir fjárhagsskema.<br /><br /> Þetta heiti mun birtast í **Heiti þjónustu** reitnum á síðunni **Netþjónusta**.|  

    Tilgreinið eitt eða fleiri fjárhagsskemu sem á að birta sem KPI-vefþjónustu samkvæmt uppsetningunni sem var búin til í fyrri töflu.  

3.  Í flýtiflipanum **Fjárhagsskemu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Heiti fjárh.skema**|Tilgreinið fjárhagsskemað sem KPI-vefþjónustan byggir á.|  
    |**Lýsing á fjárhagsskema**|Tilgreinið lýsingu fjárhagsskemans sem KPI-vefþjónustan byggir á.|  

4.  Liður 3 er endurtekinn fyrir öll fjárhagsskemu sem þú vilt nota í KPI-fjárhagsskemavefþjónustunni.  
5.  Til að skoða eða breyta völdu fjárhagsskema er **Fjárhagsskema** valið á flýtiflipanum **Breyta fjárhagsskema**.  
6.  Til að skoða KPI gögn fyrir afkastavísisvefþjónustu fyrir fjárhagsskema sem þú hefur sett upp, skal velja **Vefþjónusta KPI fyrir fjárhagsskema** aðgerðinni.  
7.  Til að birta afkastavísisvefþjónustu fyrir fjárhagsskema skal velja **Birta vefþjónustu** aðgerðina. Netþjónustunni er bætt á lista yfir vefþjónustu sem birt hefur verið á síðunni **Vefþjónusta**.  

> [!NOTE]  
>  Þú getur líka birt KPI netþjónustuna með því að benda á síðuhlutinn **Uppsetning fjárhagsskema KPI netþjónustu** af síðunni **Netþjónusta**. Frekari upplýsingar er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).  

## <a name="see-also"></a>Sjá einnig  
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]