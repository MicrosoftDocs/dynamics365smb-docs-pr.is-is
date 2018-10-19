---
title: "Vinna með uppskriftir til að stjórna íhlutum| Microsoft Docs"
description: "Þú stofnar samsetningar- eða framleiðsluuppskrift til að tilgreina íhlutina eða tilföngin sem þarf til að setja saman vöruna sem samsetningaruppskriftin segir til um."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 44648f9d9cfd9ad2e1ea3589031b6560f4a4dcfb
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

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

Sérstakar kröfur eiga við um hluti í samsetningaruppskrift að því er varðar framboð. Nánari upplýsingar er að finna í „Til að sjá framboð vöru með notkun þess í samsetningaruppskrift“ hlutann í [Fá yfirlit yfir framboð](inventory-how-availability-overview.md).

Að búa til samsetningaruppskrift er gert í tveimur hltuum:
- Uppsetning nýrra vöru
- Skilgreining á gerð uppskriftar samsetningaríhlutar.

1. Setja upp nýtt atriði. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

    Haltu áfram að slá inn íhluti eða tilföng á samsetningaruppskrift.  
2. Í glugganum **Birgðaspjald** fyrir samsetningaríhluti, veldu **Samsetning** og svo **Samsetningaruppskrift**.
3. Í glugganum **Samsetningaruppskrift** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Til að skoða íhluti samsetningaríhlutar sem ætlaður er samkvæmt uppskriftaruppbyggingunni
Úr **Samsetningaruppskrift** glugganum er hægt að opna annan gluaa sem sýnir íhluti og önnur tilföng samkvæmt uppskriftarstöðu undir samsetningaríhlutnum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn í **Vara** glugganum inniheldur **Já**.)
3. Í glugganum **Birgðaspjald** fyrir veldu **Samsetning** og svo **Samsetningaruppskrift**.
4. Í glugganum **Samsetningaruppskrift** velurðu aðgerðina **Sýna uppskrift**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Skipta samsetningaríhlutnum út fyrir hluta hans á skjalalínum.
Frá hverju sölu- og framleiðsluskjali sem innheldur samsetningaríhlut, geturðu notað sérstaka aðgerð til að skipta línunni út fyrir samsetningaríhlutinn með nýjum línum fyrir hluta hans. Þessi aðgerð er til að mynda nytsamleg ef þú vilt selja hlutana sem sett sem stendur fyrir samsetningaríhlutinn.

**Varúð**: Þegar búið er að nota aðgerðina **Opna uppskrift** er ekki auðvelt að taka hana til baka. Eyða verður sölupöntunarlínunni sem táknar íhlutina og færa svo aftur inn sölupöntunarlínu fyrir samsetningarvöruna.

Eftirfarandi ferli byggist á sölureikningi. Sömu skref eiga við um önnur söluskjöl og öll innkaupaskjöl.

1. Í efra hægra horni skal velja táknið **Leita að síðu eða skýrslu**, slá inn **söluferli**, og velja síðan viðeigandi tengil.
2. Opna sölureikning sem inniheldur línu fyrir samsetningaríhlut.
3. Veljið línuna fyrir samsetningaríhlut og svo línuaðgerðina **Opna uppskrift**.

Allir reitir í sölureikningslínunni fyrir samsetningaríhlutinn eru hreinsaðir nema reitirnir **Vara** og **Lýsing**. Sölureikningslínur sem eru útfylltar eru settar inn fyrir íhlutina og hugsanlegt tilföng sem hafa að geyma samsetningaríhlutinn.

**Athugið**: Opna uppskrift aðgerðin er líka tiltæk í **Samsetningaruppskrift** glugganum.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Reikna staðalkostnað samsetningaríhluta
Kostnaðarverð tiltektarvöru er reiknað með því að taka saman kostnaðarverð hvers íhlutar og forða í samsetningaruppskrift vörunnar.

Einnig er hægt að reikna og uppfæra staðlaðan kostnað fyrir einn eða fleiri vörur í **Staðlaður kostnaður vinnublað** glugganum. Frekari upplýsingar eru í [Uppfæra staðlað kostnaðarverð](finance-how-to-update-standard-costs.md).  

Einingaverð samsetningaruppskriftar er alltaf jafnt heildareiningakostnaði íhluta hennar, þar með talið aðrar samsetningaruppskriftir og tilföng.

1. Í efra hægra horni skal velja táknið **Leita að síðu eða skýrslu** slá inn **Vörur**, og velja síðan viðeigandi tengil.
2. Opnaðu kortið fyrir samsetningarhlut. (**Samsetningaruppskrift** reiturinn í **Vara** glugganum inniheldur **Já**.)
3. Í glugganum **Birgðaspjald** fyrir veldu **Samsetning** og svo **Samsetningaruppskrift**.
4. Í glugganum **Samsetningaruppskrift** velurðu aðgerðina **Reikna staðlaðan kostnað**.
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
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

