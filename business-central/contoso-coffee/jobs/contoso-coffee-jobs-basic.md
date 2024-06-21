---
title: Kynning á grunnverkum
description: Þessi grein leiðir þig í gegnum nokkur kjarnaferli í verkefnastjórnun.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Kynning á grunnverkum

Þessi kynning sýnir nokkur kjarnaferli:

- Bæta verkhlutum við verk
- Skrá kostnað tíma og efnis í verk
- Reikningsfæra verk

## Verkhluta bætt við

### Aðstæður  

Simon, verkefnastjóri, vill að skrá þurfi tíma sem kennir viðskiptamanninum hvernig á að nota espresso vélarvöruna. Simon vill nota sérstakan verkhluta í verkinu til að setja upp verkvél á staðnum.

### Skref

1. Verkhlutinn er stofnaður.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
    2. Verkið J00010 er *valið*.
    3.  **Á svæðinu Verkhlutar** skal velja aðgerðina **Ný lína** og færa síðan inn eftirfarandi gildi:
 
    |Nr. verkhluta verkefnis|Heimildasamstæða|Gerð verkhluta verkefnis|
    |------------|-----------|-------------|  
    |220|Þjálfun viðskiptavina|Bóka|

2. Dregið inn verkhlutana.
   1. Á svæðinu Verkhlutar skal finna aðgerðina **Inndráttur** verkhluta.
   2. Staðfesta þarf inndrátt verkhluta með því að **velja Já**.

### Niðurstöður

 - Nú er hægt að skrá tíma og kostnað á nýja verkhlutann

## Skrá tíma- og efniskostnað við verk

### Aðstæður  

Edgin, tæknimaður sem setur vélina upp, þarf að skrá tímann og efnið sem notað er við uppsetningu verksins fyrir innheimtu. Edgin bætti þegar við ferðalögunum og efninu og þarf nú að bæta við tímann fyrir kennslu starfsfólks hvernig á að nota vélina.

### Skref

1. Stofna viðbótarverkbókarlínur.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.  
    2. Velja skal runu *-CONTOSO*. Hægt er að sjá nokkrar línur af tegundinni Forði og Vara sem endurspegla tímann (fyrir tæknimanninn og ökutækið) og efni (vél og birgðir) sem notuð eru.
    3. Ný lína er stofnuð og eftirfarandi gildi færð inn:
 
    |Verk nr.|Nr. verkhluta verkefnis|Gerð|Nr.|Heimildasamstæða|Magn|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Forði|EDGIN|Þjálfun viðskiptavina|1|

2. Bóka tíma og kostnað.
   1. Valið er **Bóka** aðgerðin.
   2. Æskir notanda um að bóka línurnar með því að **velja Já**.

### Niðurstöður

- Verkfærslur og Forðafærslur af tegundinni *Notkun* eru stofnaðar.
- Birgðafærslur eru stofnaðar til að leiðrétta birgðirnar neikvætt.
- Á Verkspjaldinu sýnir Kostnaður og Verð á verkhlutasvæðinu nýju stöðuna sem bíða reikningsfærslu.
- Upplýsingakassinn fyrir verk sýnir samtölur verðsins á Verkspjaldinu.

## Stofnun sölureiknings fyrir verk

### Aðstæður  

Simon þarf að stofna og bóka reikning sem senda á til viðskiptavinarins með tíma og kostnaði frá verkefninu.

### Skref

1. Sölureikningurinn er stofnaður.

    1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
    2. Á listanum yfir verk skal velja aðgerðina **Stofna verksölureikning** .
    3. Reiturinn Verknr **.** Afmörkun á *J00010*.
    4. Velja skal **Í lagi** til að búa til sölureikninginn. Staðfesting berst á því hve margir reikningar eru búnir til.

2. Bóka tíma og útgjaldareikning.

   1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  
   2. Síðasti reikningurinn er valinn til að opna hann til endurskoðunar.
   3. Valið er **Bóka** aðgerðin.

### Niðurstöður

- Verkfærslur og forðafærslur af tegundinni *Sala* eru stofnaðar.
- Á Verkspjaldinu sýnir Kostnaður og Verð á verkhlutasvæðinu nýju reikningsfærðu stöðuna.
- Upplýsingakassinn Fyrir verk sýnir samtölur verðsins í hlutanum Reikningsfært verð á Verkspjaldinu.
