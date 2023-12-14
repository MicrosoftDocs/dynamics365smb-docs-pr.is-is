---
title: Yfirferð þjónustusamninga fyrir þjónustuvörur
description: Þessi grein leiðir þig í gegnum ýmsar aðstæður sem fela í sér þjónustuhluti og samninga.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
---

# Yfirferð þjónustusamninga fyrir þjónustuvörur

Þessi leiðsögn sýnir nokkra kjarnaferla:

- Stofnun þjónustuvara í gegnum sölu
- Gerð og reikningsfærsla fyrir þjónustusamning
- Að búa til þjónustupöntun fyrir þjónustusamning
- Úthlutaðu auðlind byggt á kunnáttu og svæði
- Ljúktu við tímafærsluna fyrir þjónustupöntunina
- Bókaðu og reikningsfærðu samningsþjónustupöntunina

## Gerð þjónustuhluta

### Aðstæður  

Susan, pöntunarvinnsla, birtir sölupöntun sem selur hlut sem er stilltur til að búa til þjónustuvöru.  

### Skref

1. Athugaðu að **Item** hafi **Service Item Group** valið.
   
    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
    2. Veldu hlutinn *S-100* og opnaðu hann.
    3. Athugaðu gildið í reitnum **Þjónustuvöruflokkur** .
       
2. Settu **sölupöntunina** til að búa til þjónustuvöruna fyrir viðskiptavininn.  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Veldu pöntun fyrir viðskiptavin 10000. Ytri pantanir nr. er *SVC-1*.
    3. Veldu **Post** aðgerðina til að senda vöruna til viðskiptavinarins.

### Niðurstöður

- Þjónustuvara er búin til fyrir viðskiptavin 10000

##  Innheimta þjónustusamnings

### Aðstæður

Charles, þjónustustjóri, býr síðan til þjónustusamning til að reikningsfæra fyrir reglulegar viðhaldsheimsóknir.

3. Búðu til **þjónustusamning** fyrir nýja þjónustuhlutinn
    1. Veldu ![peru sem opnar Segðu mér eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustusamningar** og velja síðan viðkomandi tengil.
    2. Valið er aðgerðin **Nýtt**.  
    3. Í staðfestingarglugganum skaltu velja **Já** til að búa til samning með sniðmáti. 
    4. Veldu *Ófyrirframgreiddur samningur - mánaðarlega*.
    5. Á flýtiflipanum Þjónusta, í **Þjónustupöntunartegund**, sláðu inn **VIÐHALDA**.
    6. Sláðu inn eftirfarandi upplýsingar í línurnar:

    |Nr. þjónustuvöru|Línuvirði|  
    |----------------|----------|  
    |SV000001|6000|

    7. Veldu **Skrifaðu undir samning** aðgerðina og staðfestu undirritunina.
    8. Veldu **Já** til að staðfesta stofnun þjónustureiknings. Þú færð staðfestingarskilaboð með þjónustureikningsnúmerinu.

3. Bókaðu þjónustureikninginn
   1. Veldu ![peru sem opnar Segðu mér eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustureikningar** og velja síðan viðkomandi tengil.
   2. Finndu þjónustureikninginn og veldu  **Post** aðgerðina.

### Niðurstöður

- Undirritaður þjónustusamningur er búinn til, með fjárhagsfærslum
- Bókaður þjónustureikningur er búinn til

## Stofna þjónustupöntun fyrir þjónustusamning og úthluta tilföngum

### Aðstæður  

Charles, þjónustustjóri, býr til þjónustupantanir fyrir reglubundnar viðhaldspantanir samkvæmt þjónustusamningi og fer síðan yfir sendingarráðið til að úthluta þeim.

### Skref

1. Keyra þjónustupantanir sem uppfylla skyldur virkra þjónustusamninga.
   1. Veldu ![peru sem opnar Segðu mér eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stofna samn.þjónustupantanir** og svo velja viðeigandi tengil.
   2. Sláðu inn upphafs- og lokadagsetningar mánaðarins í reitunum Upphafsdagsetning og Lokadagsetning á flýtiflipanum Valkostir
   3. Veldu **Í lagi** til að staðfesta stofnun þjónustupantana. Þú færð staðfestingarskilaboð með fjölda stofnaðra þjónustupantana.

2. Skoðaðu pantanir sem bíða úthlutunar í gegnum sendingarráð
   1. Veldu ![peru sem opnar Segðu mér eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sendingartafla** og velja síðan tengda tengilinn.
   2. Sendingarráð sýnir allar opnar þjónustupantanir ásamt **nr. af úthlutunum** til að sýna hvort þjónustupantanir séu úthlutaðar til auðlindar.
   3. Að velja **Sýna skjöl** aðgerðina til að opna þjónustupöntun.  Þú sérð að upplýsingakassinn fyrir þjónustuvörulínur sýnir hvaða auðlindir eru færar í að vinna með þennan hlut.

3. Úthluta tilföng til þjónustupöntunarinnar
   1. Í þjónustupöntuninni skaltu velja Línuaðgerðina **Aðfangaúthlutun**
   2. Sláðu inn eftirfarandi upplýsingar fyrir tilfangaúthlutun

    |Nr. þjónustuvöru|Forðanr.|Úthlutunardagsetning|Úthlutaðar stundir|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|t|1|

    3. Úthlutuninni er breytt í Staða í Virk.
    4. Við að endurnýja sendingarborðið sýnir **fjölda úthlutana** breytt úr 0 í 1 fyrir þjónustupöntunina.

### Niðurstöður

- Þjónustupantanir eru búnar til fyrir þjónustusamningana
- Þjónustupantunum er úthlutað til auðlindar til að ljúka verkinu

## Ljúktu við tímafærsluna fyrir þjónustupöntunina og bókaðu þjónustupöntunina

### Aðstæður  

Þjónustutæknir skráir tíma sinn beint við þjónustupöntunina og merkir síðan pöntun sem lokið.

> [!NOTE]
> Hægt er að slá inn tímafærslu fyrir þjónustupantanir í gegnum tímaskýrslur. Fyrir frekari upplýsingar, sjá [tengill á tímablað ef þessi athugasemd er skynsamleg].

### Skref

1. Finndu þjónustupöntunina og sláðu inn tímann í þjónustulínuna
   1. Veldu ![peru sem opnar Segðu mér eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.
   2. Finndu þjónustupöntunina til að slá inn tíma fyrir.
   3. Veldu Línuaðgerðina **Þjónustulína**.
   4. Sláðu inn eftirfarandi upplýsingar

    |Gerð|Nr.|Magn|Qty.to Neyta|
    |----|---|--------|--------|   
    |Forði|RESOURCE1|2|2|

2. Bókaðu neyslu á þjónustupöntuninni
   1. Veldu aðgerðina **Posta** til að ljúka þjónustupöntuninni, veldu **Send og neytið** aðgerðina og veldu síðan  **OK** hnappur.

### Niðurstöður

- Þjónustubókarfærslur eru búnar til í tengslum við þjónustuvöru, þjónustusamning og tilföng

## Sjá einnig .

[Kynning á Contoso Coffee Demo Data](../../contoso-coffee/contoso-coffee-intro.md)  
[Um framleiðslupantanir](../../production-about-production-orders.md)