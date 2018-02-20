---
title: "Hvernig á að: Setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum | Microsoft Docs"
description: "Í **Uppsetning Fjárhagsskema KPI netþjónustu** glugganum getur þú ákveðið hvernig skal sýna KPI gögn fjárhagsskema og á hvaða einstaka fjárhagsskemum skuli byggja afkastavísa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57f36592105faf0801864e034c3b930ae196ee62
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum
Í **Uppsetning Fjárhagsskema KPI netþjónustu** glugganum getur þú ákveðið hvernig skal sýna KPI gögn fjárhagsskema og á hvaða einstaka fjárhagsskemum skuli byggja afkastavísa. Þegar þú velur **Birta netþjónustu** hnappinn bætast KPI gögn fjárhagsskema á lista yfir vefþjónustu sem birt hefur verið í glugganum **Vefþjónusta**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Til að setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") táknið slá inn **Uppsetning vefþjónustu fyrir KPI fyrir fjárhagsskema** og velja svo tengdan tengil.  
2.  Á flýtiflipanum **Almennt** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Forspárgildi hefjast**|Tilgreinið á hvaða tímapunkti áætluðu gildin eru sýnd á mynd KPI fyrir fjárhagsskema.<br /><br /> Spárgildin eru sótt í fjárhagsáætlun sem þú velur reitnum **Heiti fjárhagsáætlunar**. **Athugið:**  Til að fá afkastavísana sem sýna spárgildin eftir tiltekna dagsetningu og raungildin fyrir dagsetninguna, geturðu breytt reitnum **Leyfa bókun frá** í glugganum **Uppsetning Fjárhags**. Frekari upplýsingar, sjá Leyfa bókun frá|  
    |**Heiti fjárhagsáætl.**|Tilgreinið heiti fjárhagsáætlunarinnar sem veitir áætluð gildi fyrir KPI-vefþjónustu fjárhagsskemans.|  
    |**Tímabil**|Tilgreinið tímabilið sem KPI-vefþjónusta fjárhagsskemans er byggð á.|  
    |**Skoða eftir**|Tilgreinið hvaða tímabil á að nota til að sýna KPI fyrir fjárhagsskema.|  
    |**Heiti vefþjónustu**|Tilgreinið heiti KPI-vefþjónustu fyrir fjárhagsskema.<br /><br /> Þetta heiti mun birtast í **Heiti þjónustu** reitnum í **Netþjónusta** glugganum.|  

    Nú skal tilgreina eitt eða fleiri fjárhagsskemu sem á að birta sem KPI-vefþjónustu samkvæmt uppsetningunni í fyrri töflu.  

3.  Í flýtiflipanum **Fjárhagsskemu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Heiti fjárh.skema**|Tilgreinið fjárhagsskemað sem KPI-vefþjónustan byggir á.|  
    |**Lýsing á fjárhagsskema**|Tilgreinið lýsingu fjárhagsskemans sem KPI-vefþjónustan byggir á.|  

4.  Liður 3 er endurtekinn fyrir öll fjárhagsskemu sem þú vilt nota í KPI-fjárhagsskemavefþjónustunni.  
5.  Til að skoða eða breyta völdu fjárhagsskema er **Fjárhagsskema** valið á flýtiflipanum **Breyta fjárhagsskema**.  
6.  Til að skoða KPI gögn fyrir afkastavísisvefþjónustu fyrir fjárhagsskema sem þú hefur sett upp, skal velja **Vefþjónusta KPI fyrir fjárhagsskema** aðgerðinni.  
7.  Til að birta afkastavísisvefþjónustu fyrir fjárhagsskema skal velja **Birta vefþjónustu** aðgerðina. Netþjónustunni er bætt á lista yfir vefþjónustu sem birt hefur verið í glugganum **Vefþjónusta**.  

> [!NOTE]  
>  Þú getur líka birt KPI netþjónustuna með því að benda á síðuhlutinn **Uppsetning fjárhagsskema KPI netþjónustu** frá **Netþjónusta** glugganum. Frekari upplýsingar er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).  

## <a name="see-also"></a>Sjá einnig  
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

