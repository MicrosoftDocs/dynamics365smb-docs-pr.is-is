---
title: "Vinna með uppskriftir til að stjórna íhlutum| Microsoft Docs"
description: "Þú stofnar samsetningaruppskrift til að tilgreina íhlutina eða tilföngin sem þarf til að setja saman vöruna sem samsetningaruppskriftin segir til um, og þú getur skoða íhluti samsetningarvöru."
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
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-bills-of-material"></a>Hvernig á að: Vinna með uppskriftir
> [!NOTE]  
>   Núverandi útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur aðeins fyrsta hluta samsetningarstjórnunarbúnaðarins. Eins og er getur þú aðeins búið til samsetningaruppskrift og síðan séð um tengda yfireiningar sem venjulega birgðavöru. Í framtíðar uppfærslu getur þú stjórnað raunverulegu samsetningu hluta úr hlutum, annaðhvort í samanburði til birgðir eða samsetningar til þess að flytja og þú getur selt hluti sem pökkum.

Þú notar uppskrift til að byggja upp yfireiningu sem þú selur sem undireiningar sem samanstanda af yfiríhlutnum eða sem þú setja saman í pöntun eða í birgðir.

Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er uppskrift vísað til sem samsetningaruppskrift. Samsetningaruppskriftir tilgreina hvaða íhlutir eru í yfireiningu. Í þessum gögnum er átt við foreldrahluta sem "samsetningarhlutur".

Samsetningaruppskriftir innihalda yfirleitt vörur en geta einnig innihaldið einn eða fleiri forða sem eru nauðsynlegir til að setja samsetningaríhlutinn saman.

Samsetningaruppskriftir geta haft mörg stig, sem þýðir að íhlutur í samsetningaruppskrift getur verið samsetningarvara sömuleiðis. Í því tilviki inniheldur **samsetningaruppskrift** reiturinn á samsetningaruppskriftinni **Já**.

Sérstakar kröfur eiga við um hluti í samsetningaruppskrift að því er varðar framboð. Nánari upplýsingar er að finna í "Til að sjá framboð vöru með notkun þess í samsetningaruppskrift“ hlutann í [Hvernig á að: Fá yfirlit yfir framboð](inventory-how-availability-overview.md).

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**. Nánari upplýsingar er að finna í [aðlaga fjárhagsupplifun þína](ui-experiences.md).

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

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn í **Vara** glugganum inniheldur **Já**.)
3. Í glugganum **Birgðaspjald** fyrir veldu **Samsetning** og svo **Samsetningaruppskrift**.
4. Í glugganum **Samsetningaruppskrift** velurðu aðgerðina **Sýna uppskrift**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Til að kaupa, selja eða flytja samsetningaríhluti
Vegna þess að núverandi útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur eingöngu getuna til að skilgreina og úthluta samsettum uppskriftum, geturðu séð um samsetningarhluti á skjalalínum eins og venjulega hluti eingöngu.

**Athugið**: Birgðamagn uppskriftaríhluta verður ekki aðlagað fyrir þig.

## <a name="see-also"></a>Sjá einnig
[Hvernig á að Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Hvernig skal: Skoða tiltækileika vöru](inventory-how-availability-overview.md)     
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

