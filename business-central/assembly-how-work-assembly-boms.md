---
title: Vinna með Samsetningaruppskriftir
description: Stofnuð er samsetningaruppskrift til að tilgreina þá íhluti sem þarf til að setja saman vöru sem UPPSKRIFTIN táknar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: assembly bom, bills of material,
ms.search.form: 36, 5870, 5872, 5874
ms.date: 09/26/2022
ms.author: edupont
ms.openlocfilehash: 87379ca23e914cf29ebff0d4cfc13639ce6d0d54
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608489"
---
# <a name="work-with-assembly-boms"></a>Vinna með Samsetningaruppskriftir

Samsetningaruppskriftir (uppskriftir) eru notaðar við uppbyggingu yfiratriða sem verður að setja saman úr íhlutum með litlu sem engri tilfanganotkun. Hægt er að nota söfnunaruppskrift til dæmis til að selja yfirvöru sem Raðhús sem samanstendur af íhlutavörum.

Samsetningarpantanir eru notaðar til að gera lokaafurð úr íhlutum með einföldu ferli sem hægt er að vinna með einu eða fleiri tilföngum, sem ekki eru vélar eða vinnustöðvar, eða án nokkurra tilfanga. Til dæmis gæti samsetningarferli falið í sér að velja tvær vínflöskur og einn kaffipoka og pakka þeim sem gjafavöru.  

Samsetningaruppskrift er aðalgögn sem skilgreina hvaða íhlutavörur fara í samsetta endanlega vöru og hvaða forðar er notaðir til að setja saman samsetningarvöruna. Þegar samsetningarvara og magn eru færð inn í haus nýrrar samsetningarpöntunar eru samsetningarpöntunarlínurnar sjálfkrafa fylltar út samkvæmt samsetningaruppskriftinni með eina samsetningarpöntunarlínu fyrir hvern íhlut eða tilfang. Frekari upplýsingar hjá [Samsetningarstjórn](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] styður einnig framl. uppskriftir. Framleiðsluuppskriftir eru frábrugðnar samsetningaruppskriftum með því að tengjast flóknari ferlum, þar á meðal forðanotkun, framleiðsluleið og vinnu-eða vélastöðvum. Fáðu frekari upplýsingar um muninn í [vinnunni með uppskriftum](inventory-how-work-BOMs.md) og [Búðu til framl. uppskriftir](production-how-to-create-production-boms.md).

## <a name="to-create-an-assembly-bom"></a>Til að stofna samsetningaruppskrift

Til að tilgreina yfireiningu sem samanstendur af öðrum atriðum, og hugsanlega úr tilföngum sem þarf til að setja yfireininguna saman, verður þú að búa til samsetningaruppskrift.  

Samsetningaruppskriftir innihalda yfirleitt vörur en geta einnig innihaldið einn eða fleiri forða sem eru nauðsynlegir til að setja samsetningaríhlutinn saman.

Samsetningaruppskriftir geta haft mörg stig, sem þýðir að íhlutur í samsetningaruppskrift getur verið samsetningarvara sömuleiðis. Í því tilviki inniheldur **samsetningaruppskrift** reiturinn á samsetningaruppskriftinni **Já**.

Sérstakar kröfur gilda um vörur í samsetningaruppskriftum varðandi framboð. [Frekari upplýsingar er að finna í til að sjá ráðstöfunarmagn vöru með notkun hennar í Samsetningaruppskriftum](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Að búa til samsetningaruppskrift er gert í tveimur hltuum:

- Uppsetning nýrra vöru
- Skilgreining á gerð uppskriftar samsetningaríhlutar.

1. Setja upp nýtt atriði. Lærðu meira á að [skrá nýjar vörur](inventory-how-register-new-items.md).

   Haltu áfram að slá inn íhluti eða tilföng á samsetningaruppskrift.  
2. **Á síðunni birgðaspjald** fyrir samsetningar vöru skal velja **samsetningaraðgerðina** og velja **síðan aðgerðina samsetningaruppskrift**.
3. Á síðunni **Samsetningaruppskrift** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Samsetningarvörur geta haft mismunandi afbrigði stillt á [!INCLUDE[prod_short](includes/prod_short.md)] rétt eins og önnur atriði, sem hjálpa til við að halda listanum yfir tiltækar afurðir styttri. Frekari upplýsingar um aðgerðina í [Umsjón afurðarafbrigða](inventory-item-variants.md).

## <a name="to-edit-assembly-boms"></a>Samsetningaruppskrift breytt

Hægt er að breyta línum samsetningaruppskriftar hvenær sem er. En Hafðu í huga að UPPSKRIFTIN kann að vera í notkun í yfirstandandi sölu eða samsetningum yfireiningar sem breytingin kann að hafa áhrif á. Veljið aðgerðina **Notkunarstaðir** til að sjá í hvaða vöru er verið að nota hana og þá hvort það hafi áhrif á sölu- eða samsetningarpantanir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **atriði** og veljið síðan tengda tengilinn.
2. Veljið gildið **Já** í dálkinum **Samsetningaruppskrift**.
3. **Á SAMSETNINGARUPPSKRIFTARSÍÐUNNI** skal velja **aðgerðina Breytingaskrá**, og breyta svo svæði eftir þörfum.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Til að skoða íhluti og aðföng sem ætluð eru samkvæmt uppskriftaruppbyggingunni

Af síðunni **Samsetningaruppskrift** er hægt að opna annan gluaa sem sýnir íhluti og önnur tilföng samkvæmt uppskriftarstöðu undir samsetningaríhlutnum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **atriði** og veljið síðan tengda tengilinn.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn á síðunni **Vörur** inniheldur **Já**.)
3. **Á síðunni birgðaspjald** skal velja **samsetningaraðgerðina** og velja **síðan aðgerðina samsetningaruppskrift**.
4. Á síðunni **Samsetningaruppskrift** velurðu aðgerðina **Sýna uppskrift**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Skipta samsetningaríhlutnum út fyrir hluta hans á skjalalínum.

Frá hverju sölu- og framleiðsluskjali sem innheldur samsetningaríhlut, geturðu notað sérstaka aðgerð til að skipta línunni út fyrir samsetningaríhlutinn með nýjum línum fyrir hluta hans. Þessi aðgerð er til að mynda nytsamleg ef þú vilt selja hlutana sem sett sem stendur fyrir samsetningaríhlutinn.

**Aðgerðin NIÐURBROT uppskriftar** er einnig tiltæk á **síðunni samsetningaruppskrift** sem leið til að skoða undirsamsetningarvörur í samsetningaruppskrift.

> [!CAUTION]  
> Varúð: Þegar búið er að nota aðgerðina **Opna uppskrift** er ekki auðvelt að taka hana til baka. Eyða verður sölupöntunarlínunni sem táknar íhlutina og færa svo aftur inn sölupöntunarlínu fyrir samsetningarvöruna.

Eftirfarandi ferli byggist á sölureikningi. Sömu skrefin eiga við um önnur söluskjöl og öll innkaupaskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **sölureikninga** og velja síðan tengda tengilinn.
2. Opna sölureikning sem inniheldur línu fyrir samsetningaríhlut.
3. Velja skal línuna fyrir samsetningaratriði og brjóta síðan **niður AÐGERÐ uppskriftarlínu**.

Allir reitir í sölureikningslínunni fyrir samsetningaríhlutinn eru hreinsaðir nema reitirnir **Vara** og **Lýsing**. Sölureikningslínur sem eru útfylltar eru settar inn fyrir íhlutina og hugsanlegt tilföng sem hafa að geyma samsetningaríhlutinn.

> [!NOTE]
> Skýrslunni **Tínslulisti eftir pöntun** er einnig breytt til að sýna aðeins þættina. Þetta þýðir að starfsmaður vöruhúss sem tínir yfirvöruna, samsetningaríhlutinn, mun ekki sjá hana á tínslulistanum. [Frekari upplýsingar er að prenta í tiltektarlistanum](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Reikna staðalkostnað samsetningaríhluta

Kostnaðarverð tiltektarvöru er reiknað með því að taka saman kostnaðarverð hvers íhlutar og forða í samsetningaruppskrift vörunnar.

Einnig er hægt að reikna og uppfæra staðlaðan kostnað fyrir einn eða fleiri vörur á síðunni **Staðlaður kostnaður vinnublað**. Frekari upplýsingar við [uppfærslu staðalkostnaðar](finance-how-to-update-standard-costs.md).  

Einingaverð samsetningaruppskriftar er alltaf jafnt heildareiningakostnaði íhluta hennar, þar með talið aðrar samsetningaruppskriftir og tilföng.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **atriði** og veljið síðan tengda tengilinn.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn á síðunni **Vörur** inniheldur **Já**.)
3. **Á síðunni birgðaspjald** skal velja **samsetningaraðgerðina** og velja **síðan aðgerðina samsetningaruppskrift**.
4. Á síðunni **Samsetningaruppskrift** velurðu aðgerðina **Reikna staðlaðan kostnað**.
5. Veldu einn af eftirfarandi valkostum, Veldu **síðan OK** hnappinn.

|Valkostur |Lýsing |
|-------|------------|
|**Efsta stig**|Reiknar staðlaðan kostnað samsetningarvörunnar sem heildarkostnað af öllum aðkeyptum eða samsettum vörum á þeirri samsetningaruppskrift, óháð undirliggjandi samsetningaruppskriftum.|
|**Öll stig**|Reiknar staðlaður kostnaður samsetningaríhluta sem summu: 1) Útreiknaður kostaður allra undirliggjandi samsetningaruppskrifta á samsetningaruppskriftinni. 2) Kostnaður allra aðkeyptra vara á samsetningaruppskriftinni.|

Kostnaðarverð þeirra vara sem mynda samsetningaruppskriftina er afritað úr birgðaspjöldum íhlutarins. Kostnaðurinn við hverja vöru er margfaldaður með magninu og heildarkostnaðurinn sést í reitnum **Kostnaðarverð** á birgðarspjaldinu.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/set-up-assembly-items-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Skoða tiltækileika vöru](inventory-how-availability-overview.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
