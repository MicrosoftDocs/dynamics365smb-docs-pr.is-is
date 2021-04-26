---
title: Umsjón fjárhagsáætlana fyrir eignir| Microsoft Docs
description: Til að hjálpa til við undirbúning fjárhagsáætlana og forspáa, eru settar upp upplýsingar um fjárfestingar, afskráningar og afskriftir eigna í framtíðinni.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3b435d1e9edae7a13514786f2de51e32237aaf94
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783560"
---
# <a name="manage-budgets-for-fixed-assets"></a>Umsjón fjárhagsáætlana fyrir eignir
Hægt er að setja upp áætlaðar eignir. Til dæmis leyfir þetta þér að taka með áætluð kaup og sölu í skýrslum.  

Við gerð áætlaðs rekstrarreiknings, efnahagsreiknings og sjóðstreymis þarf upplýsingar um fjárfestingar, afskráningar og afskriftir eigna í framtíðinni. Hægt er að fá þessar upplýsingar í skýrslunni **Eignir - Áætlað virði**. Áður en skýrslan er prentuð þarf að taka saman fjárhagsáætlunina.  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>Setja kaupverð eignar í fjárhagsáætlun
Til undirbúnings fjárhagsáætlunar verður að stofna eignaspjöld fyrir þær eignir sem ætlunin er að kaupa í framtíðinni. Eignir á fjárhagsáætlun eru settar upp eins og venjulegar eignir, en það verður að setja þær upp þannig að þær bókist ekki í fjárhag.

Þegar kaupverð er bókað er færður inn fjöldi áætlaðra eigna í reitnum **Áætlað eignanr.**. Þetta veldur því að forritið bókar stofnkostnað með gagnstæðu formerki á áætluðu eigninni. Heildarstofnkostnaður áætluðu eignarinnar er þá mismunurinn milli áætlaðs og raunverulegs stofnkostnaðar.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.
2. Veldu aðgerðina **Nýtt** til að stofna nýtt eignaspjald fyrir áætluðu eignina.
3. Velja reitnum **Áætluð Eign** gátreitinn til að hindra bókun í fjárhag.
4. Hinir reitirnir eru fylltir út, úthluta afskriftabók og bóka síðan fyrsta kaupverð með áætluðu eigninni sem er færð inn í reitinn **Áætlað Eignanr.** á færslubókarlínunni. Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>Setja afskráningu eignar í fjárhagsáætlun
Eigi að selja eignir á áætlunartímabilinu er hægt að færa inn upplýsingar um söluverð og söludagsetningu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.
2. Valin er eignin sem á að afskrá, og velja síðan **Afskriftabækur** aðgerð.
3. Á síðunni **Eignaafskriftabækur** er fært inn í reitina **Áætluð afskráningardags.** og **Áætlaður afrakstur undir reitnum Afskráning**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Skoðun á áætluðu virði afskráninga:
Keyra má skýrsluna **Eignir - Áætlað virði** til að skoða áætlað afskráningarvirði og reikna hagnað/tap.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlað virði eigna** og veldu síðan tengda tengilinn.
2. Fyllið inn í svæðin eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="to-budget-depreciation"></a>Áætlun afskrifta:
Þú getur notað **Eignir – Áætlað virði** skýrsluna til að reikna afskrift í framtíðinni. Í skýrslunni er hægt að skoða bókfært virði og uppsafnaðar afskriftir við upphaf valins tímabils, breytingar sem á tímabilinu og bókfært virði og uppsafnaðar afskriftir i lok tímabilsins.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlað virði eigna** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum.
3. Til að skoða heildarvirði allra eigna skal hreinsa gátreitinn **Prenta á Eign**.
4. Flýtiflipinn **Eignir** er hafður auður ef taka á allar eignir með. Ritaðu **Nei** í reitinn **Áætluð eign** til að undanskilja áætlaðar eignir eða **Já** til að skoða einungis áætlaðar eignir.
5. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="see-also"></a>Sjá einnig
[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]