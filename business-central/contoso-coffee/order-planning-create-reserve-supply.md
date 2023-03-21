---
title: Nota pantanaáætlun til að búa til og taka frá framboð
description: Kynning til að komast að því hvernig á að nota pantanaáætlun til að stofna nauðsynlega framleiðslupöntun fyrir framboðið í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Kynning: Nota pantanaáætlun til að búa til og taka frá framboð

Í þessari grein förum við í gegnum skrefin til að nota sýnigögn Contoso Coffee í pantanaáætlun.

## Aðstæður

Þú ert framleiðslustjóri á Contoso Coffee. Þú stofnaðir framleiðslupöntun fyrir 100 einingar af vörunni **SP-SCM1009 Airpot** og þú vilt áætla undirsamsetningar fyrir þessa pöntun. Þú notar pantanaáætlun til að stofna nauðsynlega framleiðslupöntun fyrir framboðið. Vegna þess að þú ert að stofna framleiðslupöntunina til að uppfylla kröfur tiltekinnar pöntunar ákveður þú að taka frá úttak framleiðslupöntunarinnar.  

## Skref

1. Stofnaðu nýju útgefnu framleiðslupöntunina fyrir 100 einingar af vörunni **SP-SCM1009 Airpot**.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Tegund uppruna** |Atriði|
        |**Upprunanúmer** |SP-SCM1009|
        |**Magn** |100|
    3. Veldu aðgerðina **Uppfæra framleiðslupöntun**.  

    Taktu eftir númerinu á útgefinni framleiðslupöntun.

2. Opnaðu síðuna **Pantanaáætlun** og reiknaðu nýja áætlun.

    1. Veldu aðgerðina **Áætlun**.  

    2. Á síðunni **Pantanaáætlun** er smellt á **Reikna áætlun** aðgerðina.  

    3. Flettu niður að eftirspurnarlínunni sem stendur fyrir útgefna framleiðslupöntun sem var stofnuð áður.  

    4. Stækkaðu línurnar til að skoða upplýsingarnar fyrir eftirspurnarlínuna. Staðfestu að þetta er tillaga fyrir framleiðslupöntun upp á 100 einingar af vörunni 1001.  

3. Stofnaðu nýja framleiðslupöntun fyrir 100 einingar af vörunni **SP-BOM2000, Samsetn. vatnsgeymis** og taktu frá úttak þessarar framleiðslupöntunar fyrir hönd tengdrar yfirpöntunar.  

    1. Veldu gátreitinn í reitnum **Taka frá** í eftirspurnarlínunni fyrir 100 einingarnar af vörunni SP-BOM2000.

    2. Velja **búa til Pantanir** aðgerð.  

    3. Stilltu reitinn **Búa til pantanir fyrir** í *Virku línunni*.  

    4. Stilltu reitinn **Stofna framleiðslupöntun** á *Fastáætlað*.

    5. Veldu hnappinn **Í lagi** til að stofna framleiðslupöntun.

    6. Á síðunni **Pantanaáætlun** skal staðfesta að eftirspurnarlínan fyrir 100 einingar af vörunni 1001 sé fjarlægð.

Það er allt og sumt um pantanaáætlun í [!INCLUDE [prod_short](../includes/prod_short.md)].  

## Sjá einnig .

[Kynning á sýnigögnum Contoso Coffee](contoso-coffee-intro.md)  
[Um framleiðslupantanir](../production-about-production-orders.md)  
