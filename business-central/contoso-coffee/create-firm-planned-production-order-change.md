---
title: Stofna fastáætlaða framleiðslupöntun og breyta henni
description: Kynning fyrir framleiðslustjóra hjá Contoso Coffee sem vill stofna fastáætlaða framleiðslupöntun og síðan breyta henni.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Kynning: Stofna fastáætlaða framleiðslupöntun og breyta henni

Í þessari grein förum við í gegnum skrefin til að nota sýnigögn Contoso Coffee til að vinna með framleiðslupantanir.  

## Aðstæður

Eduardo, framleiðslustjóri hjá Contoso Coffee, verður að stofna nýja framleiðslupöntun fyrir 10 einingar af vörunni **SP-SCM1009, Airpot** sem þarf að afhenda 28. apríl. Hann áætlar þetta aftur í tímann og staðfestir að hann geti hafið pöntunina 27. apríl.  

Stuttu eftir að hann lýkur þessu verki er hann beðinn um að auka pöntunina upp í 50 einingar. Þegar hann gerir það ýtir aðgerð röðunar afturábak upphafsdagsetningu pöntunarinnar of snemma. Þannig að hann færir pöntunina fram frá 23. apríl til að geta ákveðið raunhæfari lokadag.  

## Skref

1. Stofnaðu upphaflegu framleiðslupöntunina fyrir 10 einingum af vörunni **SP-SCM1009, Airpot**.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fastáætluð framl.pöntun** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Tegund uppruna** |Atriði|
        |**Upprunanúmer** |SP-SCM1009|
        |**Magn** |10|
        |**Skiladagur**|Apríl 28  |

    3. Veldu aðgerðina **Uppfæra framleiðslupöntun**.  

    4. Á síðunni **Uppfæra framleiðslupöntun** samþykkir þú allar sjálfgefnar stillingar og velur svo hnappinn **Í lagi** til að hefja ferlið.  

        Í núverandi uppsetningu notar þetta ferli áætlanagerð aftur í tímann. Í nýju línunni í framleiðslupöntuninni er upphafsdagsetningin 26. apríl.  

2. Breyttu magni framleiðslupöntunarinnar í 50 einingar og tímasettu pöntunina.  

    1. Í flýtiflipanum **Línur** fyrir **Framleiðsluuppskrift** skal velja nýlega viðbættri línu og síðan í reitinn **Magn** skal slá inn *50*.  

3. Veldu aðgerðina **Uppfæra framleiðslupöntun**.  

    Upphafsdegi hefur nú verið ýtt aftur til 20. apríl. Þetta er ekki ásættanleg dagsetning fyrir Eduardo.

4. Settu í gang áætlanagerð fram í tímann fyrir framleiðslupöntunina.

    1. Í flýtiflipanum **Tímasetja** skal stilla reitinn **Upphafsdagur** á *23. apríl*.

    Upphaf pöntunarinnar er nú 25. apríl og lokadagurinn er 2. maí. Gjalddagi pöntunarinnar er settur degi síður, 3. maí. Eduardo veit nú að það mun taka til 3. maí að afhenda aukna pöntun.

> [!NOTE]
> Áætlun pöntunar með því að breyta upphafs- eða lokadegi krefst ekki runuvinnslunnar **Uppfæra framleiðslupöntun** því að allar dagsetningar endurreiknast sjálfkrafa.

Nýja framleiðslupöntunin er nú sett upp og kröfur Eduardo eru uppfylltar.  

## Sjá einnig .

[Kynning á sýnigögnum Contoso Coffee](contoso-coffee-intro.md)  
