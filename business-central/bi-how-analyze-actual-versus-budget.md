---
title: Greina raunverulegar og áætlaðar upphæðir| Microsoft Docs
description: Lýsir því hvernig greina skal raunverulegar upphæðir annars vegar og áætlaðar upphæðir hins vegar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9c601dc3507b0777f3aeecb063e6cebe8866768c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781123"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Greina raunverulegar og áætlaðar upphæðir
Hluti af því að safna saman, greina og deila upplýsingum fyrirtækis, er að skoða raunverulegar upphæðir í samanburði við áætlaðar upphæðir fyrir alla reikninga og nokkur tímabil.

Til að greina áætlaðar upphæðir, verður fyrst að búa til fjárhagsáætlun. Frekari upplýsingar eru í [Stofna fjárhagsáætlun](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Til að skoða fjárhagsáætlun
Í áætlun með víddum er hægt að setja afmarkanir á færslurnar og sjá tilteknar áætlanir.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsáætlanir** og veldu síðan tengda tengilinn.
2. Á síðunni **Fjárhagsáætlanir** skal velja þá áætlun sem á að skoða.  
3. Efst á síðunni skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Ef valið var **Tímabil** annað hvort í reitnum **Sýna sem línur** eða **Sýna sem dálka** þarf að fylla út reitinn **Skoða eftir**. Ef ekki hefur verið valið **Tímabil**, hvorki í reitnum **Sýna sem línur** né **Sýna sem dálka**, skal slá inn viðeigandi tímabil í reitnum **Dags.afmörkun**.  

> [!NOTE]  
>   Aðeins færslur úr fjárhagsáætlun með afmörkunarkótum sem færðir eru inn á flýtiflipanum **Afmarkanir** eru teknar með í útreikninginn. Áætlunarfærslur með aðra afmörkunarkóta eða án nokkurra afmörkunarkóta teljast ekki með. Á meðan afmörkunin er stillt á síðunni sýnir áætlunin aðeins áætlunarfærslur með þessum afmörkunarkóðum.  

> [!TIP]  
>   Ef þörf er á að breyta áætlun, er hægt að breyta áætlunarfærslunum. Velja upphæð til að skoða undirliggjandi fjárhagsáætlunarfærslur.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Að skoða raunverulegar og áætlaðar upphæðir fyrir alla reikninga  
Hægt er að skoða fjárhagsáætlanir og bera þær saman við raunverulegar upphæðir í mörgum svæðum í [!INCLUDE[prod_short](includes/prod_short.md)].

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókhaldslykill** og veldu síðan tengda tengilinn.  
2. Á síðunni **Bókhaldslykill**, skal velja aðgerðina **Fjárhagur staða/áætlun**.
3. Efst á síðunni skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.  
4. Til að sjá tilgreininguna sem birt upphæð samanstendur af skal velja reitinn.  

> [!NOTE]  
>   Afmarkanir sem settar eru a síðuhausinn verða notaðar í fjárhagsfærslum og áætlunarfærslum.

Bókhaldslykillinn er í dálkunum til vinstri. Af dálkunum fimm lengst til hægri sýna fjórir þeir fyrstu raunverulegar og áætlaðar debet- og kreditfærslur á hverjum reikningi. Fimmti dálkurinn sýnir hlutfallsleg tengsl raunverulegra og áætlaðra upphæða á fjárhagsreikningnum.  

> [!TIP]  
>   Reiturinn **Skoða eftir** á síðunni **Fjárhagur - Staða/áætlun** er notaður til að velja lengd tímabils. Smellt er á reitinn  **Skoða sem** til að velja hvernig upphæðir eru reiknaðar (**Hreyfing** eða **Staða til dags**). Veljið aðgerðina **Fyrra tímabil** eða **Næsta tímabil** til að breyta tímabilinu.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Að skoða raunverulegar og áætlaðar upphæðir fyrir nokkur tímabil  
Í stað þess að skoða raunverulegar og áætlaðar upphæðir á öllum reikningum innan ákveðins tímabils er hægt að skoða fjölda tímabila á stökum reikningi.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókhaldslykill** og veldu síðan tengda tengilinn.  
2. Á síðunni **Bókhaldslykill** veljið viðeigandi fjárhagsreikning, og veljið síðan aðgerðina **Fjárhagsreikningur staða/áætlun**.  
3. Efst á síðunni skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.   
4. Til að sjá tilgreiningu á birtri upphæð skal velja reitinn.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Vinna með fjárhagsskemu](bi-how-work-account-schedule.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]