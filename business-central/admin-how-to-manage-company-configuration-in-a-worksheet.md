---
title: "Hvernig á að vinna með grunnstillingu fyrirtækis í vinnublaði | Microsoft Docs"
description: "Skilgreiningarvinnublaðið er aðalstaðsetningin þar sem hægt er að áætla, rekja og framkvæma skilgreiningarvinnu. Hægt er að stofna vinnublað fyrir hvert fyrirtæki sem unnið er með eða stofna staðlað skilgreiningarvinnublað sem hægt er að nota þegar mörg eins fyrirtæki eru skilgreind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cc2c7d5ecbff5d7cd0109c56e3c76ca137564d30
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="manage-company-configuration-in-a-worksheet"></a>Vinna með grunnstillingu fyrirtækis í vinnublaði
Skilgreiningarvinnublaðið er aðalstaðsetningin þar sem hægt er að áætla, rekja og framkvæma skilgreiningarvinnu. Hægt er að stofna vinnublað fyrir hvert fyrirtæki sem unnið er með eða stofna staðlað skilgreiningarvinnublað sem hægt er að nota þegar mörg eins fyrirtæki eru skilgreind.  

Fyrsta skrefið í að undirbúa grunnstillingarpakka er að velja fyrirtæki sem þegar hefur verið uppsett og breytt, svo það falli að flestum af þörfum þínum eftir lausnum. Þetta fyrirtæki er grunnlína fyrir grunnstillingarvinnu í nýjum fyrirtækjum. Á vinnublaðinu, eru töflurnar tilgreindar sem óskað er eftir að stillingar stjórni og meðhöndli. Þar sem flestar töflur í [!INCLUDE[d365fin](includes/d365fin_md.md)] eru tengdar og háðar öðrum töflum, ætti einnig að hafa þessar tengdu töflur með eins og nauðsyn krefur. Saman eru þessar töflur síðan grindin sem nýtt fyrirtæki er byggt á. Næstu skref hjálpa til við að virkja og síðan gangsetja stillingu þína.  

Til að aðstoða við eftirlit og yfirlestur á vinnu þinni skaltu nota **Skilgreiningarpakkatöflu** upplýsingareitinn til að sjá upplýsingar um færslur. Notið **Skilgreiningatengdar töflur** upplýsingareitinn til að fylgjast með töflutengslum.  

Eftirfarandi ferli sýna hvernig eigi að bæta við og sérstilla töfluupplýsingar fyrir viðkomandi grunnstillingu.  

## <a name="to-open-the-configuration-worksheet"></a>Til að opna skilgreiningarvinnublað  
1.  Í [!INCLUDE[d365fin](includes/d365fin_md.md)], opnið fyrirtækið sem er grunnlína fyrir grunnstillingu og opnið síðan Mitt hlutverk RapidStart Services innleiðara.  
2.  Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.  

## <a name="to-add-a-table-to-the-worksheet"></a>Til að bæta töflu við vinnublað  
1.  Í glugganum **Grunnstillingarvinnublað** skal velja aðgerðina **Breyta lista**.  
2.  Í fyrstu línunni, í reitnum **Tegund línu** skal velja **Tafla**.  
4.  Í reitnum **Töflukenni** veljið töflu sem á að bæta við grunnstillingu.  
5.  Í reitnum **Síðukenni** skal færa inn síðukennið sem tengt er við töfluna. Fyrir staðlaðar  töflur er þetta gildi fyllt út sjálfkrafa. Fyrir sérsniðnar töflur þarf að gefa upp kennið.
6.  Í reitnum **Tilvísun** skal færa inn vefslóð skjalasíðu, t.d. í hjálpinni, sem veitir bestu upplýsingar um framkvæmd eða leiðbeiningar um hvernig eigi að setja upp töflu.  
7.  Til að bæta við tengdum töflum skal velja aðgerðina **Sækja tengdar töflur**.  

    > [!NOTE]  
    > Tengdum töflu verður ekki bætt við **Sækja tengdar töflur** ef annaðhvort af eftirfarandi er satt:
    > - Tengslin eru skilyrt.  
    > Dæmi: Ef tengdar töflur fást fyrir töfluna **Viðskiptamaður** verður töflunni **Staðsetning** ekki bætt við því hún er aðeins tengd töflunni **Viðskiptamaður** með vissum skilyrðum, þ.e. ef reiturinn **Staðsetningarkóði** í töflunni **Viðskiptamaður** er útfylltur.  
    > - Tengda taflan ef með afmörkunum.  
    > Dæmi: Reitur í tengdu töflunni er með HVAR klausu. Ástæðan er að upplýsingar um þau tengsl sem í hlut eiga eru vistaðar í kerfistöflunni **Reitur**, sem er ekki algerlega aðgengileg forritinu.  
    > Slíkum töflum þarf að bæta við handvirkt með því að fylgja skrefi 4 í þessum verklagsreglum.  

8.  Til að breyta töflulistanum sem þá kemur skal velja töflu sem á að fjarlægja og síðan skal velja aðgerðina **Eyða**.  
9. Endurtaka skal skrefið fyrir hverja töflu sem á að bæta við grunnstillinguna.  
10. Til að fjarlægja tvíteknar töfluupplýsingar, sem geta komið vegna aðgerðarinnar **Sækja tengdar töflur** skal velja aðgerðina **Eyða tvíteknum línum**. Þetta mun eyða tvíteknum töflum sem eru með sama pakkakóða.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Til að bæta mörgum töflum við grunnstillingarvinnublaðið.  
1. Nota skal aðgerðina **Sækja töflur**. Glugginn **Sækja skilgreiningartöflur** runuvinnsla opnast.  
2. Á flýtiflipanum **Valkostir** skal tilgreina gerðir taflnanna sem á að bæta við grunnstillinguna eins og lýst er eftirfarandi töflu.

    |Valkostur|Description|  
    |----------------------------------|---------------------------------------|  
    |**Hafa aðeins með gögnum**|Veljið gátreitinn til að taka aðeins með töflur sem innihalda gögn. Til dæmis gæti verið gott að taka með töflu sem skilgreinir nú þegar dæmigerða greiðsluskilmála sem lausn notanda styður.|  
    |**Hafa tengdar töflur með**|Veljið gátreitinn til að hafa allar tengdar töflur með. Til að bæta inn undirsafni tengdra tafla skal skoða skref 3 í þessu ferli.|  
    |**Hafa víddartöflur með**|Veljið gátreitinn til að hafa víddatöflur með.|  
    |**Hafa aðeins leyfðar töflur með**|Veljið gátreitinn til að hafa aðeins þær töflur sem leyfið sem notað er til að búa vinnublaðið til gefur aðgang að.|

3. Á flýtiflipanum **Hlutur** skal stilla afmarkanir til að tilgreina tegundir taflnanna á að taka með eða útiloka.  
4. Velja hnappinn **Í lagi**. [!INCLUDE[d365fin](includes/d365fin_md.md)] töflum eru bætt við vinnublaðið. Hver færsla í listanum er með línugerðina **Tafla**.  
5. Til að fjarlægja tvíteknar töfluupplýsingar, sem geta komið vegna aðgerðarinnar **Sækja töflur** skal velja aðgerðina **Eyða tvíteknum línum**. Þetta mun eyða tvíteknum töflum sem eru með sama pakkakóða.  
6. Hægt er að bæta töflum við vinnublaðið sem tengist töflu sem valin var. Fara skal yfir upplýsingarnar í upplýsingakassanum **Tengdar töflur** til að athuga hvort töflur vanti. Til að bæta við tengdum töflum fyrir ákveðna töflu skal velja töflu af listanum og síðan velja aðgerðina **Sækja tengdar töflur**.  

    > [!NOTE]  
    > Tengdum töflu verður ekki bætt við **Sækja tengdar töflur** ef annaðhvort af eftirfarandi er satt:
    > - Tengslin eru skilyrt.  
    > Dæmi: Ef tengdar töflur fást fyrir töfluna **Viðskiptamaður** verður töflunni **Staðsetning** ekki bætt við því hún er aðeins tengd töflunni **Viðskiptamaður** með vissum skilyrðum, þ.e. ef reiturinn **Staðsetningarkóði** í töflunni **Viðskiptamaður** er útfylltur.  
    > - Tengda taflan ef með afmörkunum.  
    > Dæmi: Reitur í tengdu töflunni er með HVAR klausu. Ástæðan er að upplýsingar um þau tengsl sem í hlut eiga eru vistaðar í sýndartöflunni **Reitur** og eru ekki tiltækar í gluggum eins og grunnstillingarvinnublaðinu vegna afkastagetu.  
    > Tengdum töflum með svo flóknu sambandi þarf að bæta við handvirkt með því að fylgja skrefi 4 í kaflanum „Að bæta við töflu á vinnublaðið".

7. Til að eyða töflum úr listanum sem þá kemur skal velja töflu sem á að fjarlægja og síðan velja aðgerðina **Eyða**.  

Nota skal næsta ferli til að tilgreina hvaða töflureiti skal hafa með. Eftir að þessi tilgreining er gerð, er hægt að flytja út töfluna í Excel og nota töfluuppbygginguna sem sniðmát fyrir söfnun gagna um viðskiptamenn. Frekari upplýsingar eru í [Undirbúa flutning á gögnum viðskiptamanns](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Til að tilgreina safn reita og færsla fyrir skilgreiningartöflu  
1. Veljið töflu á lista yfir grunnstillingartöflur og því næst aðgerðina **Breyta lista**.  
2. Veljið töflu þar sem á að tilgreina reitaupplýsingar og veljið því næst aðgerðina **Reitir**.  
3. Til að velja aðeins þá reiti sem hafa á með er valin aðgerðin **Hreinsa það sem haft er með**. Til að bæta öllum reitum við skal velja aðgerðina **Safn haft með**.  
4. Til að tilgreina að svæðisgögn ætti ekki að villuleita skal hreinsa gátreitinn **Villuleita reit** fyrir reitinn.  
5. Velja hnappinn **Í lagi**.  
6. Til að sía ákveðinn hóp af færslum sem á að vera með í skilgreiningarvinnublaðinu er valin aðgerðin **Síur** og síðan viðeigandi síugildi tilgreind.

Hægt er að stofna svið aðgerða og töfluflokka í vinnublaðinu til að setja svipaða virkni saman. Til dæmis í uppsetningu bókhaldslykilsins fyrir grunnstillingarnar, gæti notandi ákveðið að stofna flokk bókunartaflna. Yfirleitt eru svæði notuð til að hópa saman töflusöfn sem samsvara virku svæði. Hvert svæði getur innihaldið flokka. Flokk er hægt að nota til að raða saman töflum sem hafa sameiginlega merkingu.  

Eftirfarandi ferli lýsir því hvernig eigi að bæta við merkingum svæða og flokka, eftir að upphaflegur töflulisti hefur verið stofnaður. Eftir að hafa bætt við þessa flokka er hægt að halda áfram að bæta við og breyta lista yfir töflur.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Til að skipta niður og flokka aðgerðir í vinnublaðinu  
1. Í upphafi svæðis skal setja inn nýja línu á vinnublaðið.  
2. Í reitnum **Tegund línu** veljið **Svæði**. Í svæðinu **Heiti** er fært inn heiti fyrir svæðið.  
3. Í upphafi flokkunar á töflum skal setja inn nýja línu á vinnublaðið.  
4. Í reitnum **Tegund línu** veljið **Flokkur**. Í svæðinu **Heiti** er fært inn heiti fyrir svæðið. Heiti flokksins er sjálfkrafa inndregið.  
5. Til að færa töflur í viðeigandi flokk skal velja töflu til að flytja og síðan velja aðgerðina **Flytja upp** eða **Flytja niður**. Einnig er hægt að eyða vinnublaðslínu og færa inn töflu aftur á áskilinn stað.  

Sumar [!INCLUDE[d365fin](includes/d365fin_md.md)] töflur eru staðlaðar og gögn þeirra eru ekki líkleg til að breytast á milli innleiðinga. Þar af leiðandi, til að hjálpa viðskiptamanni notanda að einbeita sér, skal fjarlægja þessar töflur úr vinnublaðinu eftir að hafa tekið þær með í grunnstillingarpakkanum. Þegar þeim er bætt við haldast töflurnar áfram sem hluti af grunnstillingarpakkanum.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Til að fjarlægja staðlaða töflu í vinnublaðinu  
Eftir að notandi hefur bætt öllum nauðsynlegum töflum við grunnstillingarpakkann, skal ákvarða hvaða töflur krefjast ekki athygli viðskiptamanns.  
1.  Veljið töflurnar og eyðið þeim svo með því að velja aðgerðina **Eyða**.  

    > [!NOTE]  
    >  Töflurnar eru áfram í pakkanum jafnvel þótt þeim hafi verið eytt úr vinnublaðinu.  

## <a name="see-also"></a>Sjá einnig  
[Uppsetning grunnstillingu fyrirtækis](admin-set-up-company-configuration.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)

