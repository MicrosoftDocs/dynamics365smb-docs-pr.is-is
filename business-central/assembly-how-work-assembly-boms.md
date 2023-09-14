---
title: Vinna með samsetningaruppskriftum
description: Þú stofnar samsetningaruppskrift til að tilgreina íhlutina sem þarf til að setja saman vöruna sem uppskriftin segir til um.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 09/26/2022
ms.author: bholtorf
---
# Vinna með samsetningaruppskriftum

Þú notar samsetningaruppskriftir til að skipuleggja yfirvörur sem þarf að setja saman úr íhlutum með lítilli eða engri notkun á tilföngum. Hægt er að nota samsetningaruppskrift t.d. til að selja yfirvöru sem sett sem samanstendur af íhlutavörum.

Samsetningarpantanir eru notaðar til að gera lokaafurð úr íhlutum með einföldu ferli sem hægt er að vinna með einu eða fleiri tilföngum, sem ekki eru vélar eða vinnustöðvar, eða án nokkurra tilfanga. Til dæmis gæti samsetningarferli falið í sér að velja tvær vínflöskur og einn kaffipoka og pakka þeim sem gjafavöru.  

Samsetningaruppskrift er aðalgögn sem skilgreina hvaða íhlutavörur fara í samsetta endanlega vöru og hvaða forðar er notaðir til að setja saman samsetningarvöruna. Þegar samsetningarvara og magn eru færð inn í haus nýrrar samsetningarpöntunar eru samsetningarpöntunarlínurnar sjálfkrafa fylltar út samkvæmt samsetningaruppskriftinni með eina samsetningarpöntunarlínu fyrir hvern íhlut eða tilfang. Frekari upplýsingar má finna á [Samsetningarstjórnun](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] styður einnig framleiðsluuppskriftir. Framleiðsluuppskriftir eru öðruvísi en samsetningaruppskriftir því þær fela í sér flóknari ferla, þ.m.t. tilfanganotkun, framleiðsluleiðir og vinnu- eða vélastöðvar. Frekari upplýsingar um muninn er að finna í [Vinna með uppskriftir](inventory-how-work-BOMs.md) og [Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md).

## Til að stofna samsetningaruppskrift

Til að tilgreina yfireiningu sem samanstendur af öðrum atriðum, og hugsanlega úr tilföngum sem þarf til að setja yfireininguna saman, verður þú að búa til samsetningaruppskrift.  

Samsetningaruppskriftir innihalda yfirleitt vörur en geta einnig innihaldið einn eða fleiri forða sem eru nauðsynlegir til að setja samsetningaríhlutinn saman.

Samsetningaruppskriftir geta haft mörg stig, sem þýðir að íhlutur í samsetningaruppskrift getur verið samsetningarvara sömuleiðis. Í því tilviki inniheldur **samsetningaruppskrift** reiturinn á samsetningaruppskriftinni **Já**.

Sérstakar kröfur eiga við um vörur í samsetningaruppskriftum hvað varðar framboð. Frekari upplýsingar má finna á [Til að sjá framboð vöru út frá notkun hennar í samsetningaruppskrift](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Að búa til samsetningaruppskrift er gert í tveimur hltuum:

- Uppsetning nýrra vöru
- Skilgreining á gerð uppskriftar samsetningaríhlutar.

1. Setja upp nýtt atriði. Frekari upplýsingar eru á [Skrá nýjar vörur](inventory-how-register-new-items.md).

   Haltu áfram að slá inn íhluti eða tilföng á samsetningaruppskrift.  
2. Á síðunni **Birgðaspjald** fyrir samsetningaríhluti, veldu **Samsetning** og svo **Samsetningaruppskrift**.
3. Á síðunni **Samsetningaruppskrift** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Samsetningaríhlutir geta verið með mismunandi afbrigði stillt í [!INCLUDE[prod_short](includes/prod_short.md)] rétt eins og aðrar vörur, sem hjálpar þér að halda listanum yfir tiltækar afurðir styttri. Frekari upplýsingar um eiginleikann er að finna í [Stjórna afurðarafbrigðum](inventory-item-variants.md).

## Samsetningaruppskrift breytt

Hægt er að breyta línum samsetningaruppskriftar hvenær sem er. En Hafðu í huga að UPPSKRIFTIN kann að vera í notkun í yfirstandandi sölu eða samsetningum yfireiningar sem breytingin kann að hafa áhrif á. Veljið aðgerðina **Notkunarstaðir** til að sjá í hvaða vöru er verið að nota hana og þá hvort það hafi áhrif á sölu- eða samsetningarpantanir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Veljið gildið **Já** í dálkinum **Samsetningaruppskrift**.
3. Á síðunni **Samsetningaruppskrift** skal velja aðgerðina **Breyta lista** og breyta svo hvaða reit sem er eftir þörfum.

## Til að skoða íhluti og aðföng sem ætluð eru samkvæmt uppskriftaruppbyggingunni

Af síðunni **Samsetningaruppskrift** er hægt að opna annan gluaa sem sýnir íhluti og önnur tilföng samkvæmt uppskriftarstöðu undir samsetningaríhlutnum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn á síðunni **Vörur** inniheldur **Já**.)
3. Á síðunni **Birgðaspjald** skal velja aðgerðina **Samsetning** og svo aðgerðina **Samsetningaruppskrift**.
4. Á síðunni **Samsetningaruppskrift** velurðu aðgerðina **Sýna uppskrift**.

## Skipta samsetningaríhlutnum út fyrir hluta hans á skjalalínum.

Frá hverju sölu- og framleiðsluskjali sem innheldur samsetningaríhlut, geturðu notað sérstaka aðgerð til að skipta línunni út fyrir samsetningaríhlutinn með nýjum línum fyrir hluta hans. Þessi aðgerð er til að mynda nytsamleg ef þú vilt selja hlutana sem sett sem stendur fyrir samsetningaríhlutinn.

Aðgerðin **Opna uppskrift** er líka í boði á síðunni **Samsetningaruppskrift** sem leið til að skoða vörur undirsamsetningar í samsetningaruppskrift.

> [!CAUTION]  
> Varúð: Þegar búið er að nota aðgerðina **Opna uppskrift** er ekki auðvelt að taka hana til baka. Eyða verður sölupöntunarlínunni sem táknar íhlutina og færa svo aftur inn sölupöntunarlínu fyrir samsetningarvöruna.

Eftirfarandi ferli byggist á sölureikningi. Sömu skref eiga við um önnur söluskjöl og öll innkaupaskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.
2. Opna sölureikning sem inniheldur línu fyrir samsetningaríhlut.
3. Veldu línuna fyrir samsetningaríhlut og svo línuaðgerðina **Opna uppskrift**.

Allir reitir í sölureikningslínunni fyrir samsetningaríhlutinn eru hreinsaðir nema reitirnir **Vara** og **Lýsing**. Sölureikningslínur sem eru útfylltar eru settar inn fyrir íhlutina og hugsanlegt tilföng sem hafa að geyma samsetningaríhlutinn.

> [!NOTE]
> Skýrslunni **Tínslulisti eftir pöntun** er einnig breytt til að sýna aðeins þættina. Þetta þýðir að starfsmaður vöruhúss sem tínir yfirvöruna, samsetningaríhlutinn, mun ekki sjá hana á tínslulistanum. Frekari upplýsingar er að finna á [Prenta tiltektarlistann](sales-how-print-picking-list.md).

## Reikna staðalkostnað samsetningaríhluta

Kostnaðarverð tiltektarvöru er reiknað með því að taka saman kostnaðarverð hvers íhlutar og forða í samsetningaruppskrift vörunnar.

Einnig er hægt að reikna og uppfæra staðlaðan kostnað fyrir einn eða fleiri vörur á síðunni **Staðlaður kostnaður vinnublað**. Frekari upplýsingar má finna á [Uppfæra staðlaðan kostnað](finance-how-to-update-standard-costs.md).  

Einingaverð samsetningaruppskriftar er alltaf jafnt heildareiningakostnaði íhluta hennar, þar með talið aðrar samsetningaruppskriftir og tilföng.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn á síðunni **Vörur** inniheldur **Já**.)
3. Á síðunni **Birgðaspjald** skal velja aðgerðina **Samsetning** og svo aðgerðina **Samsetningaruppskrift**.
4. Á síðunni **Samsetningaruppskrift** velurðu aðgerðina **Reikna staðlaðan kostnað**.
5. Veldu einn af eftirfarandi valkostum, veldu síðan hnappinn **Í lagi**.

|Valkostur |Lýsing |
|-------|------------|
|**Efsta stig**|Reiknar staðlaðan kostnað samsetningarvörunnar sem heildarkostnað af öllum aðkeyptum eða samsettum vörum á þeirri samsetningaruppskrift, óháð undirliggjandi samsetningaruppskriftum.|
|**Öll stig**|Reiknar staðlaður kostnaður samsetningaríhluta sem summu: 1) Útreiknaður kostaður allra undirliggjandi samsetningaruppskrifta á samsetningaruppskriftinni. 2) Kostnaður allra aðkeyptra vara á samsetningaruppskriftinni.|

Kostnaðarverð þeirra vara sem mynda samsetningaruppskriftina er afritað úr birgðaspjöldum íhlutarins. Kostnaðurinn við hverja vöru er margfaldaður með magninu og heildarkostnaðurinn sést í reitnum **Kostnaðarverð** á birgðarspjaldinu.

## Sjá tengda [Microsoft þjálfun](/training/modules/set-up-assembly-items-dynamics-365-business-central/).

## Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Skoða tiltækileika vöru](inventory-how-availability-overview.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
