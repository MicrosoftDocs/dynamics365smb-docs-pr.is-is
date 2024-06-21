---
title: Stofna nýja leið
description: Kynning til að komast að því hvernig á að færa inn allar upplýsingarnar fyrir nýja leið handvirkt í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---
# Kynning: Búa til nýja leið

Í þessari grein tökum við þig í gegnum skrefin til að nota Contoso Coffee kynningu gögn til að setja handvirkt upp nýja framleiðsluleið í [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## Aðstæður

Oscar, ferlahönnuður hjá Contoso Coffee, ákveður að búa til nýja leið með heitinu *Ný slóð*. Þar sem leiðin er ólíkt öðrum leiðum á Contoso-kaffi verður Oscar að handfæra allar upplýsingarnar fyrir leiðina.  

## Skref

1. Búðu til leiðarhausinn.  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðir** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Nr.** |1099|
        |**Lýsing** |Ný slóð|
2. Búðu til leiðarlínurnar.

    1. Í flýtiflipanum **Línur** skal bæta við nýrri línu og síðan fylla út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Aðgerðarnr.** |10|
        |**Tegund** |Vinnustöð|
        |**Nr.** |100|
        |**Uppsetn.tími** |20|
        |**Keyrslutími** |15|

    2. Bættu við nýrri línu og fylltu síðan í reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Aðgerðarnr.** |20|
        |**Tegund** |Vinnustöð|
        |**Nr.** |200|
        |**Uppsetn.tími** |30|
        |**Keyrslutími** |5|
3. Leiðin vottuð.

    1. Í reitnum **Staða** skal velja *Vottað*.  

Nýja leiðin er nú uppsett.  

## Sjá einnig .

[Kynning á Contoso Kaffi kynningargögnum](../contoso-coffee-intro.md)  
