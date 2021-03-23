---
title: Vinna með uppskriftir til að stjórna íhlutum
description: Þú stofnar samsetningar- eða framleiðsluuppskrift til að tilgreina íhlutina eða tilföngin sem þarf til að setja saman vöruna sem samsetningaruppskriftin segir til um.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 01/05/2021
ms.author: edupont
ms.openlocfilehash: 2ada3cea6a7c7e5fddc122b9405a6e608f35a804
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377599"
---
# <a name="work-with-bills-of-material"></a>Vinna með uppskriftir
Nota skal uppskriftir til að byggja upp yfirvöru sem verður að vera sett saman eða framleidd af tilföngum eða vélstöðvum úr íhlutum. Samsetningaruppskrift getur líka verið notuð til að selja yfirvöru sem sett, gert úr íhlutum hennar.

## <a name="assembly-boms-or-production-boms"></a>Samsetningaruppskriftir eða framleiðsluuppskriftir
Samsetningarpantanir eru notaðar til að gera lokaafurð úr íhlutum með einföldu ferli sem hægt er að vinna með einu eða fleiri tilföngum, sem ekki eru vélar eða vinnustöðvar, eða án nokkurra tilfanga. Til dæmis gæti samsetningarferli falið í sér að velja tvær vínflöskur og einn kaffipoka og pakka þeim sem gjafavöru.  

Samsetningaruppskrift er aðalgögn sem skilgreina hvaða íhlutavörur fara í samsetta endanlega vöru og hvaða forðar er notaðir til að setja saman samsetningarvöruna. Þegar samsetningarvara og magn eru færð inn í haus nýrrar samsetningarpöntunar eru samsetningarpöntunarlínurnar sjálfkrafa fylltar út samkvæmt samsetningaruppskriftinni með eina samsetningarpöntunarlínu fyrir hvern íhlut eða tilfang. Nánari upplýsingar, sjá [Samsetningarstjórnun](assembly-assemble-items.md).

Í þessu efnisatriði er samsetningaruppskriftum lýst.

Framleiðslupantanir er notaðar til að búa til lokavörur úr íhlutum í flóknu ferli sem krefst framleiðsluleiða og vinnu- eða vélastöðva, sem endurspegla framleiðslugetu. Til dæmis getur verið að framleiðsluferli falið í sér að skera stálplötur í einni aðgerð, sjóða þær í þeirri næsta aðgerð og mála endanlegur vöruna í síðustu aðgerðinni. Frekari upplýsingar eru í [Framleiða](production-manage-manufacturing.md).  

Framleiðsluuppskrift er aðalgögn sem skilgreinir framleiðsluvöru og íhlutina sem notaðir eru í hana. fyrir samsetningarvöru verður framleiðsluuppskrift að vera vottuð og henni úthlutað til framleiðsluvörunnar áður en hægt er að nota hana í framleiðslupöntun. Þegar framleiðsluvaran er færð inn í framleiðslupöntunarlínu, annað hvort handvirkt eða með því að endurnýjun pöntunina, verður framleiðsluuppskriftin framleiðslupöntunaríhlutirnir. Frekari upplýsingar eru í [Stofna framleiðsluuppskriftir](production-how-to-create-production-boms.md).  

Hugtakið forði í framleiðslu er mun flóknara en í samsetningarstjórnun. Vinnustöðvar og vélastöðvar virka sem forði og framleiðsluskref eru sýnd með aðgerðum sem skráðar eru á forða í framleiðslu í framleiðsluleiðum. Nánari upplýsingar eru í [Stofna leiðir](production-how-to-create-routings.md).

Hægt er að tengja bæði samsetningarpantanir og framleiðslupantanir beint við sölupantanir. Hins vegar er aðeins hægt að nota samsetningarpantanir til að sérsníða endanlegu vöruna beint samkvæmt beiðni viðskiptamanns með sölupöntun.

## <a name="to-create-an-assembly-bom"></a>Til að stofna samsetningaruppskrift
Til að tilgreina yfireiningu sem samanstendur af öðrum atriðum, og hugsanlega úr tilföngum sem þarf til að setja yfireininguna saman, verður þú að búa til samsetningaruppskrift.  

Samsetningaruppskriftir innihalda yfirleitt vörur en geta einnig innihaldið einn eða fleiri forða sem eru nauðsynlegir til að setja samsetningaríhlutinn saman.

Samsetningaruppskriftir geta haft mörg stig, sem þýðir að íhlutur í samsetningaruppskrift getur verið samsetningarvara sömuleiðis. Í því tilviki inniheldur **samsetningaruppskrift** reiturinn á samsetningaruppskriftinni **Já**.

Sérstakar kröfur eiga við um hluti í samsetningaruppskrift að því er varðar framboð. Nánari upplýsingar er að finna í [Til að sjá framboð vöru út frá notkun hennar í samsetningaruppskrift](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Að búa til samsetningaruppskrift er gert í tveimur hltuum:
- Uppsetning nýrra vöru
- Skilgreining á gerð uppskriftar samsetningaríhlutar.

1. Setja upp nýtt atriði. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

    Haltu áfram að slá inn íhluti eða tilföng á samsetningaruppskrift.  
2. Á síðunni **Birgðaspjald** fyrir samsetningaríhluti, veldu **Samsetning** og svo **Samsetningaruppskrift**.
3. Á síðunni **Samsetningaruppskrift** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-edit-assembly-boms"></a>Samsetningaruppskrift breytt
Hægt er að breyta línum samsetningaruppskriftar hvenær sem er. En Hafðu í huga að UPPSKRIFTIN kann að vera í notkun í yfirstandandi sölu eða samsetningum yfireiningar sem breytingin kann að hafa áhrif á. Veljið aðgerðina **Notkunarstaðir** til að sjá í hvaða vöru er verið að nota hana og þá hvort það hafi áhrif á sölu- eða samsetningarpantanir.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Veljið gildið **Já** í dálkinum **Samsetningaruppskrift**.
3. Á síðunni **Samsetningaruppskrift** skal velja aðgerðina **Breyta lista** og fylla svo út reitina eins og þörf krefur.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Til að skoða íhluti og aðföng sem ætluð eru samkvæmt uppskriftaruppbyggingunni
Af síðunni **Samsetningaruppskrift** er hægt að opna annan gluaa sem sýnir íhluti og önnur tilföng samkvæmt uppskriftarstöðu undir samsetningaríhlutnum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn á síðunni **Vörur** inniheldur **Já**.)
3. Á síðunni **Birgðaspjald** fyrir veldu **Samsetning** og svo **Samsetningaruppskrift**.
4. Á síðunni **Samsetningaruppskrift** velurðu aðgerðina **Sýna uppskrift**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Skipta samsetningaríhlutnum út fyrir hluta hans á skjalalínum.
Frá hverju sölu- og framleiðsluskjali sem innheldur samsetningaríhlut, geturðu notað sérstaka aðgerð til að skipta línunni út fyrir samsetningaríhlutinn með nýjum línum fyrir hluta hans. Þessi aðgerð er til að mynda nytsamleg ef þú vilt selja hlutana sem sett sem stendur fyrir samsetningaríhlutinn.

Opna uppskrift aðgerðin er líka tiltæk á síðunni **Samsetningaruppskrift** sem aðferð til að skoða undirvörur undirsamstæða á samsetningaruppskrift.

> [!CAUTION]  
>  Varúð: Þegar búið er að nota aðgerðina **Opna uppskrift** er ekki auðvelt að taka hana til baka. Eyða verður sölupöntunarlínunni sem táknar íhlutina og færa svo aftur inn sölupöntunarlínu fyrir samsetningarvöruna.

Eftirfarandi ferli byggist á sölureikningi. Sömu skref eiga við um önnur söluskjöl og öll innkaupaskjöl.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.
2. Opna sölureikning sem inniheldur línu fyrir samsetningaríhlut.
3. Veljið línuna fyrir samsetningaríhlut og svo línuaðgerðina **Opna uppskrift**.

Allir reitir í sölureikningslínunni fyrir samsetningaríhlutinn eru hreinsaðir nema reitirnir **Vara** og **Lýsing**. Sölureikningslínur sem eru útfylltar eru settar inn fyrir íhlutina og hugsanlegt tilföng sem hafa að geyma samsetningaríhlutinn.

> [!NOTE]
> Skýrslunni **Tínslulisti eftir pöntun** er einnig breytt til að sýna aðeins þættina. Þetta þýðir að starfsmaður vöruhúss sem tínir yfirvöruna, samsetningaríhlutinn, mun ekki sjá hana á tínslulistanum. Frekari upplýsingar er að finna í [Prenta tiltektarlistann](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Reikna staðalkostnað samsetningaríhluta

Kostnaðarverð tiltektarvöru er reiknað með því að taka saman kostnaðarverð hvers íhlutar og forða í samsetningaruppskrift vörunnar.

Einnig er hægt að reikna og uppfæra staðlaðan kostnað fyrir einn eða fleiri vörur á síðunni **Staðlaður kostnaður vinnublað**. Frekari upplýsingar eru í [Uppfæra staðlað kostnaðarverð](finance-how-to-update-standard-costs.md).  

Einingaverð samsetningaruppskriftar er alltaf jafnt heildareiningakostnaði íhluta hennar, þar með talið aðrar samsetningaruppskriftir og tilföng.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Í efra hægra horni skal velja táknið **Leita að síðu eða skýrslu** slá inn **Vörur**, og velja síðan viðeigandi tengil.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn á síðunni **Vörur** inniheldur **Já**.)
3. Á síðunni **Birgðaspjald** fyrir veldu **Samsetning** og svo **Samsetningaruppskrift**.
4. Á síðunni **Samsetningaruppskrift** velurðu aðgerðina **Reikna staðlaðan kostnað**.
5. Veldu einn eftirfarandi valkosta og svo hnappinn **Í lagi**.

|Valkostur |Description |
|-------|------------|
|**Efsta stig**|Reiknar staðlaðan kostnað samsetningarvörunnar sem heildarkostnað af öllum aðkeyptum eða samsettum vörum á þeirri samsetningaruppskrift, óháð undirliggjandi samsetningaruppskriftum.|
|**Öll stig**|Reiknar staðlaður kostnaður samsetningaríhluta sem summu: 1) Útreiknaður kostaður allra undirliggjandi samsetningaruppskrifta á samsetningaruppskriftinni. 2) Kostnaður allra aðkeyptra vara á samsetningaruppskriftinni.|



Kostnaðarverð þeirra vara sem mynda samsetningaruppskriftina er afritað úr birgðaspjöldum íhlutarins. Kostnaðurinn við hverja vöru er margfaldaður með magninu og heildarkostnaðurinn sést í reitnum **Kostnaðarverð** á birgðarspjaldinu.

## <a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Skoða tiltækileika vöru](inventory-how-availability-overview.md)     
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]