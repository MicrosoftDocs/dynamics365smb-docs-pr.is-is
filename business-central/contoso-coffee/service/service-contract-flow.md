---
title: Ganga frá þjónustusamningum vegna þjónustuvara
description: Þessari grein fylgja leiðbeiningar um ýmsar aðstæður sem varða þjónustuliði og samninga.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Ganga frá þjónustusamningum vegna þjónustuvara

Þessi gönguleið sýnir fram á nokkra kjarnaferla:

- Stofnun þjónustuvara í gegnum sölu
- Stofnun og Reikningsfærsla fyrir þjónustusamning
- Þjónustupöntun stofnuð fyrir þjónustusamning
- Úthluta forða sem byggir á kunnáttu og sviði
- Ljúka tímafærslunni fyrir þjónustupöntunina
- Bóka og reikningsfæra Samningsþjónustupöntunina

## <a name="creation-of-service-items"></a>Stofnun þjónustuvara

### <a name="scenario"></a>Aðstæður

Susan, pöntunarörgjörvinn, bókar sölupöntun sem er skilgreind til að mynda þjónustuvöru.  

### <a name="steps"></a>Skref

1. Athuga skal að  **Vara**  er valin með  **þjónustuvöruflokki** .
   
    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
    2. Veldu vöru  *S-100*  og Opnaðu hana.
    3. Athuga skal gildið í  **reitnum Þjónustuvöruflokkur** .
       
2. Sölupöntunin  **er**  bókuð til að stofna þjónustuvöru fyrir viðskiptamanninn.  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Veljið pöntun fyrir viðskiptavin 10000. Ytri pantanirnar nr. Er  *svc-1*.
    3.  **Veljið aðgerðina Bóka**  til að senda vöruna til viðskiptavinarins.

### <a name="results"></a>Niðurstöður

- Þjónustuvara verður útbúin fyrir viðskiptavin 10000

## <a name="invoicing-a-service-contract"></a>Reikningsfæra þjónustusamning

### <a name="scenario-1"></a>Aðstæður

Charles, þjónustustjóri, býr svo til þjónustusamning til að reikningsfæra fyrir reglulegum viðhaldsheimsóknum.

3.  **Stofna þjónustusamninginn**  fyrir nýju þjónustuvöruna
    1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustusamningar** og velja síðan viðkomandi tengil.
    2. Valið er aðgerðin **Nýtt**.  
    3. Í staðfestingarglugganum skaltu velja  **Já**  til að stofna samning með því að nota sniðmát. 
    4. Veljið  *án fyrirframgreidds samnings-mánaðarlega*.
    5. Á flipanum þjónusta, í  **Tegund** þjónustupöntunarinnar, skal færa inn  **mainten**.
    6. Í línurnar eru færðar inn eftirfarandi upplýsingar:

    |Nr. þjónustuvöru|Línuvirði|  
    |----------------|----------|  
    |SV000001|6000|

    7. Velja skal  **aðgerðina undirrita samning**  og staðfesta undirritun.
    8. Velja  **skal Já**  til að staðfesta stofnun þjónustureiknings. Þú færð staðfestingarpóst með númeri Þjónustreiknings.

3. Bóka þjónustureikninginn
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustureikningar** og velja síðan viðkomandi tengil.
   2. Finna skal þjónustureikninginn og velja  **aðgerðina Bóka** .

### <a name="results-1"></a>Niðurstöður

- Undirritaður verði samningur um undirritaðan þjónustusamning, með færslum
- Bókaður Þjónustureikningur verður stofnaður

## <a name="creating-a-service-order-for-a-service-contract-and-assign-resources"></a>Þjónustupöntun stofnuð fyrir þjónustusamning og úthlutað forða

### <a name="scenario-2"></a>Aðstæður

Charles, þjónustustjóri, mun stofna þjónustupantanir fyrir reglulegar viðhaldspantanir samkvæmt þjónustusamningi og yfirfara síðan Sendingarborð til að úthluta þeim.

### <a name="steps-1"></a>Skref

1. Keyrið þjónustupöntunum sem munu uppfylla skyldur virkra þjónustusamninga.
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stofna samn.þjónustupantanir** og svo velja viðeigandi tengil.
   2. Færið inn upphafs-og lokadagsetningar mánaðarins í reitunum Upphafsdagsetning og Lokadagsetning í Fastflipanum Valkostir.
   3. Valið  **er í lagi**  til að staðfesta stofnun þjónustupantana. Þú færð staðfestingarpóst með fjölda stofnaða þjónustupantana.

2. Fara yfir pantanirnar sem bíða úthlutunar í gegnum Sendingarborð
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sendingartafla** og velja síðan tengda tengilinn.
   2. Sendingarstjórnin sýnir allar opnar þjónustupantanir ásamt  **Nr. af úthlutunum**  til að sýna hvort þjónustupöntunum hefur verið úthlutað forða.
   3.  **Aðgerðin Sýna skjöl**  valin til að opna þjónustupöntun.  Í þessum þætti sést að Upplýsingakassi þjónustuvörulínur sýnir hvaða tilföng eru hæfð til að vinna með þessa vöru.

3. Úthluta forða til þjónustupöntunarinnar
   1. Í þjónustupöntuninni er valið úthlutun **forðagætuúthlutunar**
   2. Færið inn eftirfarandi upplýsingar fyrir Forðsúthlutunina

    |Nr. þjónustuvöru|Forðanr.|Úthlutunardagsetning|Úthlutaðar stundir|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|t|1|

    3. Úthlutuninni verður breytt í virka stöðu.
    4. Verkröðunarstjórnin mun sýna  **Engar úthlutanir**  sem breytt hefur verið úr 0 til 1 fyrir þjónustupöntunina.

### <a name="results-2"></a>Niðurstöður

- Þjónustupantanir verða stofnaðar fyrir þjónustusamninga
- Þjónustupöntunum verður úthlutað til forða til að ljúka vinnunni

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Ljúka tímafærslunni fyrir þjónustupöntunina og bóka þjónustupöntunina

### <a name="scenario-3"></a>Aðstæður

Þjónustutæknimenn munu skrá tíma sinn beint á móti þjónustupöntuninni, síðan merkja pöntun sem tilbúna.

> [!NOTE]
> Hægt er að færa inn tímafærslu fyrir þjónustupantanir með vinnuskýrslum. Frekari upplýsingar er að finna á [hlekkur á tímablað ef þetta athugast á vit].

### <a name="steps-2"></a>Skref

1. Finna þjónustupöntunina og færa tímann inn í Þjónustulínuna
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.
   2. Þjónustupöntunin er fundin með til að færa inn tíma.
   3. Veljið þjónustulínu  **línuaðgerðarinnar**.
   4. Sláðu inn eftirfarandi upplýsingar

    |Gerð|Nr.|Magn|Qty.to neyta|
    |----|---|--------|--------|   
    |Forði|RESOURCE1|2|2|

2. Í þjónustupöntuninni er notkunin bókuð
   1. Velja skal  **aðgerðina Bóka**  til að ljúka þjónustupöntuninni, velja  **skipið og neyta**  aðgerðar og velja svo hnappinn í  **lagi** .

### <a name="results-3"></a>Niðurstöður

- Þjónustufærslur verða stofnaðar í tengslum við þjónustuvöruna, þjónustusamninginn og forða-

## <a name="see-also"></a>Sjá einnig .
