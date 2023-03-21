---
title: Sameina sjálfvirka og handvirka birgðaskráningu
description: Kynning fyrir framleiðslustjóra hjá Contoso Coffee sem vill sameina sjálfvirka og handvirka birgðaskráningu.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Kynning: Sameina sjálfvirka og handvirka birgðaskráningu

Í þessari grein förum við í gegnum skrefin til að nota sýnigögn Contoso Coffee í birgðaskráningu.  

## Aðstæður

Þú ert framleiðslustjóri á Contoso Coffee. Stofna þarf nýja framleiðslupöntun fyrir tíu einingar af vörunni SP-SCM1004, AutoDrip. Sumir þættir og aðgerðir verða birgðaskráðar framvirkt, aðrar afturvirkt, eftir því hver skilyrðin eru.

## Skref

> [Athugaðu!] Mundu að laga birgðir með því að bóka birgðabók með opnunarstöðum.

1. Stofnaðu fastáætlaða framleiðslupöntun fyrir fimm einingar af vörunni **SP-SCM1004, AutoDrip** á staðsetningunni *NORÐUR*. Leiðbeiningar er að finna í [Kynning: Stofna fastáætlaða framleiðslupöntun og breyta henni](create-firm-planned-production-order-change.md).  

2. Losa framleiðslupöntunina.

    1. Veldu aðgerðina **Breyta stöðu**.  

    2. Í síðunni sem birtist skal stilla reitinn **Ný staða** á *Losað* og síðan velja hnappinn **Já**.  

        Skilaboð sem eru með stöðustiku birtist og vísar í sjálfvirka notkun. Þessu er fylgt eftir með staðfestingarboðum um að pöntuninni sé breytt til að hún fái stöðuna *Losað*.  

    3. Velja hnappinn **Í lagi** til að loka staðfestingarskilaboðunum.

3. Farðu yfir birgða- og afkastahöfuðbókarfærslur fyrir framleiðslupöntunina.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  

    2. Opnaðu framleiðslupöntunina með 5 einingum af AutoDrip kaffivél.  

    3. Veldu aðgerðina **Birgðabókafærslur**.  

        Varan **SP-BOM1305 Screw Hex M3 Zink** er birgðaskráð um leið með fullu væntu magni. Lokaðu síðunni **Birgðabókafærslur**.  

    4. Veldu aðgerðina **Færslur afkastahöfuðbókar**.  Athugaðu að færslu samsetningaraðgerðar meginhluta var lokið um leið og pöntunin var losuð. Lokaðu glugganum **Færslur afkastahöfuðbókar**.

    Þú getur birgðaskráð íhluti varanna sjálfkrafa með því að nota notkunarbókina eða framleiðslubókina. Handvirk birgðaskráning gerir þér kleift að laga magnið fyrir bókun. Til dæmis ef þörf er á auknu magni til að ná yfir hráefni í lágum gæðum.
4. Birgðaskráðu íhluti handvirkt.  
    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notkunarbók** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Reikna notkun**.  

    3. Á beiðnisíðunni **Reikna notkun**, í flýtiflipanum **Framleiðslupöntun**, skal skilgreina síu fyrir tiltekna pöntun í **Pöntunarnr.**. reit og smellið á hnappinn **Í lagi**. Eftir að beiðnisíða runuvinnslunnar, taktu eftir að síðan **Notkunarbók** fyllist út með íhlutunum sem þarfnast handvirkrar notkunar.

    4. Veldu **Bóka** aðgerðina. Lokaðu notkunarbókinni.

5. Skráðu úttak handvirkt fyrir rafmagnsleiðslur.  

    Fylltu handvirkt út í reitina **Uppsetn.tími** og **Keyrslutími**. Einnig er hægt að tilgreina raunverulegt framleitt magn og rýrrnun. Sláðu inn *3* sem úttaksmagnið og bókaðu úttakið.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Úttaksbók** og velja síðan viðkomandi tengil.  

    2. Á síðunni **Úttaksbók** skal stofna nýja færslubókarlínu.  

    3. Í **Pöntunarnr.** reitinn, tilgreinið röðina.  

    4. Veldu aðgerðina **Opna leið**.  

        Síðan **Úttaksbók** fyllist út með aðgerðarlínu aðeins fyrir rafmagnsleiðslur.

    5. Stillið **Keyrslutími** reitinn á *10*.  

    6. Breyta reitnum **Magn** úr *5* í *3*.

    7. Velja **Bóka**.  
    8. Lokaðu úttaksbókinni.

6. Farðu yfir birgðabókafærslurnar fyrir framleiðslupöntunina.

    1. Á síðunni fyrir framleiðslupöntunina skaltu velja aðgerðina **Birgðabókafærslur**.  

    Varan **SP-BOM1302, stjórnborðsskjár** er bókuð með magn upp á *3* sem byggir á raunverulegu úttaki, en **SP-BOM1303, hnappur** er bókaður með fullu væntu magni. Lokaðu síðunni **Birgðabókafærslur**.

7. Ljúka framleiðslupöntuninni.  

    1. Veldu aðgerðina **Breyta stöðu**.
    2. Á síðunni sem kemur upp skal stilla reitinn **Ný staða** á *Lokið* og síðan velja hnappinn **Já**.  

        Skilaboð birtast með stöðustiku sem sýnir sjálfvirka notkun. Þar á eftir koma staðfestingarskilaboð um að pöntuninni sé breytt í pöntun með stöðuna *Lokið*. Tilbúin framleiðslupöntun er með sama númerið og hún var með með stöðunni *Losuð*.
    3. Velja hnappinn **Í lagi** til að loka staðfestingarskilaboðunum.

8. Farðu aftur yfir birgða- og afkastahöfuðbókarfærslur fyrir framleiðslupöntunina.

    1. Veldu aðgerðina **Færslur afkastahöfuðbókar**.  

        Færslu pökkunaraðgerða var lokið um leið og pöntunin var losuð. Framleitt (úttak) magn er *5* burtséð frá úttaki fyrra skrefsins. Lokaðu síðunni **Færslur afkastahöfuðbókar**.

    2. Veldu aðgerðina **Birgðabókafærslur**.  

        Magnið í færslu afkastahöfuðbókar af gerðinni *Úttak* er jafnt og úttaksmagnið í færslu afkastahöfuðbókar. Notað magn af **SP-BOM1301, Housing AutoDrip** og **SP-BOM1304, Stainless still thermal carafe** er 5 fyrir bæði því að vænt úttak og raunverulegt úttak er það sama. 

    3. Lokaðu síðunni **Birgðabókafærslur**.  

Þetta er allt og sumt um handvirka og sjálfvirka birgðaskráningu íhluta.

## Sjá einnig .

[Birgðaskráning íhluta samkvæmt frálagi aðgerðar](../production-how-to-flush-components-according-to-operation-output.md)  
[Kynning á sýnigögnum Contoso Coffee](contoso-coffee-intro.md)  
