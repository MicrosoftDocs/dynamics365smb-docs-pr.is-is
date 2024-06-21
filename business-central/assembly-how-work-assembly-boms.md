---
title: Vinna með samsetningaruppskriftir
description: Þú stofnar samsetningaruppskrift til að tilgreina íhlutina sem þarf til að setja saman vöruna sem uppskriftin segir til um.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Vinna með samsetningaruppskriftir

Þú notar samsetningaruppskriftir til að skipuleggja yfirvörur sem þarf að setja saman úr íhlutum með lítilli eða engri notkun á tilföngum. Hægt er að nota samsetningaruppskrift t.d. til að selja yfirvöru sem sett sem samanstendur af íhlutavörum.

Nota samsetningarpantanir til að búa til fullunnar vörur úr íhlutum í vinnslu sem einn eða fleiri grunnforði getur framkvæmt, sem eru ekki véla- eða vinnustöðvar eða án forða. Samsetningarferli gæti til dæmis verið að velja tvær vínflöskur og eina kaffipoka og pakka þeim sem gjafavöru.  

Samsetningaruppskrift er aðalgögn sem skilgreina hvaða íhlutavörur fara í samsetta endanlega vöru og hvaða forðar er notaðir til að setja saman samsetningarvöruna. Þegar samsetningarvara og magn eru færð inn í samsetningarpöntun eru samsetningarpöntunarlínurnar fylltar út samkvæmt samsetningaruppskriftinni. Pöntunin er með eina samsetningarpöntunarlínu á hvern íhlut eða forða. Frekari upplýsingar má finna á [Samsetningarstjórnun](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] styður einnig framleiðsluuppskriftir. Framleiðsluuppskriftir eru frábrugðnar samsetningaruppskriftum því þær fela í sér flóknari ferli, svo sem forðanotkun, framleiðsluleiðir og vinnu- eða vélastöðvar. Frekari upplýsingar um muninn er að finna í [Vinna með uppskriftir](inventory-how-work-BOMs.md) og [Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md).

## Til að stofna samsetningaruppskrift

Til að skilgreina vöru sem samanstendur af öðrum vörum og forðanum sem settur er saman verður að búa til samsetningaruppskrift.  

Samsetningaruppskriftir geta haft mörg stig, sem þýðir að íhlutur í samsetningaruppskrift getur verið samsetningarvara sömuleiðis. Í því tilviki inniheldur **samsetningaruppskrift** reiturinn á samsetningaruppskriftinni **Já**.

Sérstakar kröfur eiga við um vörur í samsetningaruppskriftum hvað varðar framboð. Frekari upplýsingar má finna á [Til að sjá framboð vöru út frá notkun hennar í samsetningaruppskrift](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Að búa til samsetningaruppskrift er gert í tveimur hltuum:

- Uppsetning nýrra vöru.
- Skilgreining á gerð uppskriftar samsetningaríhlutar.

1. Setja upp nýtt atriði. Frekari upplýsingar eru á [Skrá nýjar vörur](inventory-how-register-new-items.md).

   Haltu áfram að slá inn íhluti eða tilföng á samsetningaruppskrift.  
2. Á síðunni **Birgðaspjald** fyrir samsetningaríhluti, veldu **Samsetning** og svo **Samsetningaruppskrift**.
3. Á síðunni **Samsetningaruppskrift** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Samsetningarvörur geta haft afbrigði, eins og hver önnur vara, sem hjálpar til við að halda vörulistanum styttri. Frekari upplýsingar um eiginleikann er að finna í [Stjórna afurðarafbrigðum](inventory-item-variants.md).

## Samsetningaruppskrift breytt

Hægt er að breyta línum samsetningaruppskriftar hvenær sem er. Hins vegar getur uppskriftin verið í notkun með yfirsölu eða samsetningum yfirvörunnar. Ef uppskriftinni er breytt gæti það haft áhrif á þær aðgerðir. Velja aðgerðina **Notkunarstaður** til að skoða vörurnar sem nota hana og hvort það gæti haft áhrif á sölu- eða samsetningarpantanir.

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

Úr hvaða sölu- og innkaupaskjali sem er með samsetningarvöru er hægt að nota sérstaka aðgerð til að koma í stað línunnar fyrir samsetningarvöruna með nýjum línum fyrir íhluti hennar. Þessi aðgerð er til dæmis gagnleg ef selja á íhlutina sem sett sem táknar samsetningarvöruna.

Aðgerðin **Opna uppskrift** er líka í boði á síðunni **Samsetningaruppskrift** sem leið til að skoða vörur undirsamsetningar í samsetningaruppskrift.

> [!CAUTION]  
> Þegar aðgerðin **Opna uppskrift** hefur verið notuð er ekki auðvelt að afturkalla hana. Eyða verður sölupöntunarlínum fyrir íhlutina og færa síðan aftur inn sölupöntunarlínu fyrir samsetningarvöruna.

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
3. Á síðunni **Birgðaspjald** er aðgerðin **Samsetningaruppskrift** valin.
4. Á síðunni **Samsetningaruppskrift** velurðu aðgerðina **Reikna staðlaðan kostnað**.
5. Veldu einn af eftirfarandi valkostum, veldu síðan hnappinn **Í lagi**.

|Valkostur |Lýsing |
|-------|------------|
|**Efsta stig**|Reiknar staðlaðan kostnað samsetningarvörunnar sem heildarkostnað af öllum aðkeyptum eða samsettum vörum á þeirri samsetningaruppskrift, óháð undirliggjandi samsetningaruppskriftum.|
|**Öll stig**|Reiknar staðlað kostnaðarverð vörunnar sem summu af:</br></br>* Reiknaður kostnaður allra undirliggjandi samsetningaruppskrifta í samsetningaruppskriftinni.</br>* Kostnaður allra keyptra vara á samsetningaruppskriftinni.|

Kostnaðarverð þeirra vara sem mynda samsetningaruppskriftina er afritað úr birgðaspjöldum íhlutarins. Kostnaðurinn við hverja vöru er margfaldaður með magninu og heildarkostnaðurinn sést í reitnum **Kostnaðarverð** á birgðarspjaldinu.

## Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Skoða tiltækileika vöru](inventory-how-availability-overview.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
