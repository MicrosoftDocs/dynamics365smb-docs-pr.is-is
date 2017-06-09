---
title: "Hvernig á að: Vinna með uppskriftir | Microsoft Docs"
description: "Samsetningaruppskriftir tilgreina hvaða íhlutir eða forðar þurfa að vera til staðar til að setja saman vöruna sem samsetningaruppskriftin stendur fyrir. Samsetningaruppskriftir innihalda yfirleitt vörur en geta einnig innihaldið einn eða fleiri forða sem sinna samsetningarvinnunni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: ce75a9d292e12c58efc51c4db2fbc5a37b7553c7
ms.openlocfilehash: f55dcf4b391ae42ab46a22b729597a96645d9b71
ms.contentlocale: is-is
ms.lasthandoff: 05/05/2017


---
# <a name="how-to-work-with-bills-of-materials"></a>Hvernig á að: Vinna með uppskriftir
**Athugaðu**: Núverandi útgáfa [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur aðeins fyrsta hluta þingstýringarinnar. Eins og er getur þú aðeins búið til samsetningaruppskrift og síðan séð um tengda yfireiningar sem venjulega birgðavöru. Í framtíðar uppfærslu getur þú stjórnað raunverulegu samsetningu hluta úr hlutum, annaðhvort í samanburði til birgðir eða samsetningar til þess að flytja og þú getur selt hluti sem pökkum.

Þú notar uppskrift til að byggja upp yfireiningu sem þú selur sem undireiningar sem samanstanda af yfiríhlutnum eða sem þú setja saman í pöntun eða í birgðir.

Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er uppskrift vísað til sem samsetningaruppskrift. Samsetningaruppskriftir tilgreina hvaða íhlutir eru í yfireiningu. Í þessum gögnum er átt við foreldrahluta sem "samsetningarhlutur".

Samsetningaruppskriftir innihalda yfirleitt vörur en geta einnig innihaldið einn eða fleiri forða sem eru nauðsynlegir til að setja samsetningaríhlutinn saman.

Samsetningaruppskriftir geta haft mörg stig, sem þýðir að íhlutur í samsetningaruppskrift getur verið samsetningarvara sömuleiðis. Í því tilviki inniheldur **samsetningaruppskrift** reiturinn á samsetningaruppskriftinni **Já**.

Sérstakar kröfur eiga við um hluti í samsetningaruppskrift að því er varðar framboð. Nánari upplýsingar er að finna í "Til að sjá framboð á vöru með því að nota það í samsetningaruppskrift“ hlutann í [Hvernig á að: Fá yfirlit yfir framboð](inventory-how-availability-overview.md).

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar er að finna í [aðlaga fjárhagsupplifun þína](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>Til að stofna samsetningaruppskrift
Til að tilgreina yfireiningu sem samanstendur af öðrum atriðum, og hugsanlega úr tilföngum sem þarf til að setja yfireininguna saman, verður þú að búa til samsetningaruppskrift.  

Að búa til samsetningaruppskrift er gert í tveimur hltuum:
- Uppsetning nýrra vöru
- Skilgreining á gerð uppskriftar samsetningaríhlutar.

1. Setja upp nýtt atriði. Nánari upplýsingar eru í [Hvernig á að: Skrá nýjar vörur](inventory-how-register-new-items.md).

    Haltu áfram að slá inn íhluti eða tilföng á samsetningaruppskrift.  
2. Í glugganum **Birgðaspjald** fyrir samsetningaríhluti, veldu **Samsetning** og svo **Samsetningaruppskrift**.
3. Í glugganum **Samsetningaruppskrift** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Til að skoða íhluti samsetningaríhlutar sem ætlaður er samkvæmt uppskriftaruppbyggingunni
Úr **Samsetningaruppskrift** glugganum er hægt að opna annan gluaa sem sýnir íhluti og önnur tilföng samkvæmt uppskriftarstöðu undir samsetningaríhlutnum.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Vörur**, og velja síðan viðeigandi tengil.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn í **Vara** glugganum inniheldur **Já**.)
3. Í glugganum **Birgðaspjald** fyrir veldu **Samsetning** og svo **Samsetningaruppskrift**.
4. Í glugganum **Samsetningaruppskrift** velurðu aðgerðina **Sýna uppskrift**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Til að kaupa, selja eða flytja samsetningaríhluti
Vegna þess að núverandi útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur eingöngu getuna til að skilgreina og úthluta samsettum uppskriftum, geturðu séð um samsetningarhluti á skjalalínum eins og venjulega hluti eingöngu.

**Athugið**: Birgðamagn uppskriftaríhluta verður ekki aðlagað fyrir þig.

## <a name="see-also"></a>Sjá einnig
[Hvernig á að Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Hvernig á að: Sækja yfirlit yfir aðgengi](inventory-how-availability-overview.md)     
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

