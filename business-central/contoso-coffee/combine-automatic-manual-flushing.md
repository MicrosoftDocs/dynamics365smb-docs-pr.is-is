---
title: Sameina sjálfvirka og handvirka Flushing
description: Walkthrough fyrir framleiðslustjóran á contoso Coffee, sem vill sameina sjálfvirka og handvirka andlitsgerð.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 6b128f79cb8e629147bdd5ae77f2545ad0f7025c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524202"
---
# <a name="walkthrough-combine-automatic-and-manual-flushing"></a>Walkthrough: sameina sjálfvirka og handvirka Andlitsroða

Í þessari grein tekur þú á móti skrefunum til að nota contoso Coffee sýnigögnin í andlitsroða.  

## <a name="scenario"></a>Aðstæður

Þú ert framleiðslustjósinn í contoso Coffee. Stofna verður nýja framleiðslupöntun fyrir tíu eininga vöru SP-SCM1004, AutoDrip. Sumir þættir og aðgerðir verða áfram rof, aðrir afturábak roðnum út frá mismunandi aðstæðum.

## <a name="steps"></a>Skref

1. Stofna fastáætlaða framleiðslupöntun fyrir fimm einingar af vöru **SP-SCM1004, AutoDrip**. Fyrir ráðgjöf, sjá [Walkthrough: stofna fastáætlaða framleiðslupöntun og breyta henni](create-firm-planned-production-order-change.md).  

2. Sleppið framleiðslupöntuninni.

    1. **Velja stöðuaðgerðina** Breyta.  

    2. Í síðunni sem birtist er nýi Stöðureiturinn **settur** *út* og síðan er **Já** -hnappnum valinn.  

        Skilaboð sem hafa stöðulínum birtist og vísar til sjálfvirkrar notkunar. Þessu er fylgt eftir með staðfestingarskilaboðum um að pöntuninni sé breytt til að fá stöðuna *Útgefin*.  

    3. Velja skal **OK** hnappinn til að loka staðfestingarboðunum.

3. Fara yfir vöru-og Getubókarfærslur fyrir framleiðslupöntunina.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  

    2. Framleiðslupöntunin er opnuð með 5 eininga sjálfvirkri kaffivél í sjálfvirka Borvél.  

    3. Aðgerðin birgðafærslurnar **er** valin.  

        Varan **SP-BOM1305 Skrúfgangur Hex M3 ZINK** er roðinn tafarlaust með fullt Væntanlegt magn. Síðan er að **Loka birgðafærslum** síðu.  

    4. Aðgerðin Getubókarfærslur **er** valin.  Athugaðu að líkamssamsetningaraðgerðarfærslu var einnig lokið á augnabliki þegar pöntun var gefin út. Glugganum Getubókarfærslur **er** lokað.

    Hægt er að tæma íhlutavörur handvirkt með notkun notkunar eða framleiðslubókar. Handvirk roði gerir notandanum kleift að leiðrétta magn fyrir bókun. Til dæmis ef þörf er á viðbótarmagni til að þekja lítið gæðahráefni.
4. Skola íhluti handvirkt.  
    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notkunarbók** og velja síðan viðkomandi tengil.  

    2. **Veljið reikniaðgerðina notkun**.  

    3. **Í síðunni** Reikna notkunarbeiðni **á framleiðslupöntuninni** er afmörkun tilgreind fyrir tiltekna pöntun í reitnum **Pöntunarnr.** Svæðinu og velja **síðan OK** hnappinn. Eftir beiðni um runuvinnslu lokar með því að **Notkunarbókarsíðan** fyllir út þá íhluti sem þarfnast handvirkrar notkunar.

    4. Valið **er bóka** aðgerð. Loka notkunarbókinni.

5. Skrá útlag handvirkt fyrir rafspelkunni.  

    Fylla verður út handvirkt í **uppsetningartíma** og **keyra tímasvæði**. Einnig er hægt að tilgreina framleitt magn og rýrnun. Færið inn *3* sem afkastamagn og bókið úttakið.

    1. Veldu þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Úttaksbók** og velja síðan viðkomandi tengil.  

    2. **Stofnið nýja færslubókarlínu á síðunni úttaksbókarlína**.  

    3. **Í Pöntunarnr.** Reit skal tilgreina pöntunina.  

    4. Velja skal **aðgerðina opna leið**.  

        Síðan Frálagsbók **er** aðeins fyllt út með aðgerðarlínunni fyrir rafhringing.

    5. Reiturinn Keyrslutími **er** stilltur á *10*.  

    6. Breyta skal **magnsvæðinu** úr *5* í *3*.

    7. Veldu **Bóka**.  
    8. Loka úttaksbók.

6. Skoðið birgðafærslurnar fyrir framleiðslupöntunina.

    1. Í síðunni fyrir framleiðslupöntunina er aðgerðin birgðafærsla **valin**.  

    Varan **SP-BOM1302, skjár** stjórnborðs er bókuð með magninu *3*, byggð á raunverulegu úttaki, á meðan **SP-BOM1303, hnappurinn** er bókaður með fullt Væntanlegt magn. Síðan er að **Loka birgðafærslum** síðu.

7. Ljúka skal framleiðslupöntuninni.  

    1. **Velja stöðuaðgerðina** Breyta.
    2. Í síðunni sem birtist er nýi Stöðureiturinn **settur** *á lokið* og síðan er **Já** -hnappurinn valinn.  

        Skilaboð birtast með stöðulínu sem endurspeglar sjálfvirka notkun. Þessu er fylgt eftir með staðfestingarskilaboðum um að pöntuninni sé breytt í pöntun með stöðuna *lokið*. Afgreidd framleiðslupöntun hefur sama númer og hún hafði með stöðuna *Útgefin*.
    3. Velja skal **OK** hnappinn til að loka staðfestingarboðunum.

8. Fara yfir vöru-og Getubókarfærslur fyrir framleiðslupöntunina.

    1. Aðgerðin Getubókarfærslur **er** valin.  

        Færslu umbúðaaðgerða lauk í augnablikinu þegar pöntunin var gefin út. Magn framleiddra (úttaks) er 5 *, óháð úttaki fyrra skrefs*. Síðunni Getubókarfærslunum **er** lokað.

    2. Aðgerðin birgðafærslurnar **er** valin.  

        Magnið í birgðafærslu af gerðinni *Framleiðsla* er jafnt úttaksmagni í getubókarfærslunni. Notagagn **SP-BOM1301, hústæki AutoDrip**, og **SP-BOM1304, Ryðfrítt still hitapumpa** er 5 fyrir bæði þar sem Væntanleg framleiðsla og raunveruleg framleiðsla er sú sama. 

    3. Síðan er að **Loka birgðafærslum** síðu.  

Það er það fyrir handvirkar og sjálfvirkar andlitsflúðaíhluti.

## <a name="see-also"></a>Sjá einnig .

[Tæma íhluti eftir úttak aðgerðar](../production-how-to-flush-components-according-to-operation-output.md)  
[Kynning á contoso kaffi sýnigögnum](contoso-coffee-intro.md)  
