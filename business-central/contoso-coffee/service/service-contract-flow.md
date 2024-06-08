---
title: Kynning á þjónustusamningum vegna þjónustuvöru
description: Þessi hlutur leiðbeinir þér í gegnum ýmis dæmi sem varða þjónustuvörur og samninga.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Kynning á þjónustusamningum vegna þjónustuvöru

Þessi kynning sýnir nokkur kjarnaferli:

- Stofnun þjónustuvara með sölu
- Stofnun og reikningsfærsla fyrir þjónustusamning
- Þjónustupöntun stofnuð fyrir þjónustusamning
- Úthluta forða á grundvelli þekkingar og svæðis
- Ljúka tímafærslu fyrir þjónustupöntunina
- Bóka og reikningsfæra þjónustupöntun samnings

## <a name="creation-of-service-items"></a>Stofnun þjónustuvöru

### <a name="scenario"></a>Aðstæður

Súsanna, pantanavinnslan, bókar sölupöntun sem selur vöru sem er grunnstillt til að búa til þjónustuvöru.  

### <a name="steps"></a>Skref

1. Ganga úr skugga um að vara **hafi**  **valið Þjónustuvöruflokk** .
   
    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
    2. Varan *S-100* er valin og hún opnuð.
    3. Gildið er athugað í reitnum **Þjónustuvöruflokkur** .
       
2. Sölupöntunin **er** bókuð til að stofna þjónustuvöru fyrir viðskiptamanninn.  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Veljið pöntun fyrir viðskiptavin 10000. Reiturinn Ytri pantanir nr. er *SVC-1*.
    3. Velja skal aðgerðina **Bóka** til að senda vöruna til viðskiptamanns.

### <a name="results"></a>Niðurstöður

- Þjónustuvara er stofnuð fyrir viðskiptamann 10000

## <a name="invoicing-a-service-contract"></a>Reikningsfærsla þjónustusamnings

### <a name="scenario-1"></a>Aðstæður

Charles, þjónustustjóri, stofnar síðan þjónustusamning til að reikningsfæra fyrir reglulegar viðhaldsheimsóknir.

3. Þjónustusamningur stofnaður **fyrir** nýju þjónustuvöruna
    1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustusamningar** og velja síðan viðkomandi tengil.
    2. Valið er aðgerðin **Nýtt**.  
    3. Í staðfestingarsvarglugganum skal velja **Já** til að stofna samning með sniðmáti. 
    4. Valinn er *samningur sem ekki er fyrirframgreiddur - Mánaðarlega*.
    5. Á flýtiflipanum Þjónusta í **Tegund** þjónustupöntunar er fært inn **MAINTEN**.
    6. Eftirfarandi upplýsingar eru færðar inn í línurnar:

    |Nr. þjónustuvöru|Línuvirði|  
    |----------------|----------|  
    |SV000001|6000|

    7. Veljið aðgerðina **Undirrita samning** og staðfestið undirritunina.
    8. Valið er **Já** til að staðfesta stofnun þjónustureiknings. Staðfestingarboð berast með númeri þjónustureiknings.

3. Bóka þjónustureikninginn
   1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustureikningar** og velja síðan viðkomandi tengil.
   2. Finna skal þjónustureikninginn og velja aðgerðina **Bóka** .

### <a name="results-1"></a>Niðurstöður

- Undirritaður þjónustusamningur er stofnaður með færslum
- Bókaður þjónustureikningur er stofnaður

## <a name="create-a-service-order-for-a-service-contract-and-assign-resources"></a>Stofna þjónustupöntun fyrir þjónustusamning og úthluta forða

### <a name="scenario-2"></a>Aðstæður

Charles, þjónustustjóri, stofnar Þjónustupantanir fyrir reglulegar viðhaldspantanir í Þjónustusamningi og skoða síðan Afgreiðslustöð til að úthluta þeim.

### <a name="steps-1"></a>Skref

1. Keyra þjónustupantanir sem uppfylla skuldbindingar virkra þjónustusamninga.
   1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stofna samn.þjónustupantanir** og svo velja viðeigandi tengil.
   2. Upphafs- og lokadagsetningar mánaðarins eru færðar inn í reitina Upphafsdagsetning og Lokadagsetning á flýtiflipanum Valkostir.
   3. Velja skal **Í lagi** til að staðfesta stofnun þjónustupantana. Staðfestingarboð berast með fjölda stofnaðra þjónustupantana.

2. Fara yfir pantanirnar sem bíða úthlutunar í afgreiðslustöð
   1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sendingartafla** og velja síðan tengda tengilinn.
   2. Afgreiðslustöð sýnir allar opnar þjónustupantanir ásamt **fjöldi úthlutana** til að sýna hvort þjónustupöntunum er úthlutað á forða.
   3. Velja aðgerðina **Sýna skjöl** til að opna þjónustupöntun.  Í upplýsingakassanum Þjónustuvörulínur sést hvaða forði er búinn undir að vinna með þessa vöru.

3. Úthluta forða á þjónustupöntunina
   1. Í þjónustupöntuninni skal velja Línuaðgerðina **Úthlutun forða**
   2. Eftirfarandi upplýsingar eru færðar inn fyrir úthlutun forða

    |Nr. þjónustuvöru|Forðanr.|Úthlutunardagsetning|Úthlutaðar stundir|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|t|1|

    3. Úthlutun er breytt í Staða í Virk.
    4. Ef afgreiðslustöð er endurnýjuð er **fjöldi úthlutana** breytt úr 0 í 1 fyrir þjónustupöntunina.

### <a name="results-2"></a>Niðurstöður

- Þjónustupantanir eru stofnaðar fyrir þjónustusamningana
- Þjónustupöntunum er úthlutað á forða til að ljúka verkinu

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Ljúka tímafærslu þjónustupöntunarinnar og bóka þjónustupöntunina

### <a name="scenario-3"></a>Aðstæður

Þjónustutæknimaðurinn skráir tíma sinn beint á móti þjónustupöntuninni og merkir svo pöntunina sem tilbúna.

> [!NOTE]
> Hægt er að færa inn tímafærslu fyrir þjónustupantanir í vinnuskýrslum. Nánari upplýsingar eru í [link to Timesheet ef þessi athugasemd er skynsamleg].

### <a name="steps-2"></a>Skref

1. Finna þjónustupöntunina og færa tímann inn í þjónustulínuna
   1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.
   2. Finna skal þjónustupöntunina til að færa inn tíma fyrir.
   3. Velja skal Línuaðgerðina **Þjónustulína**.
   4. Eftirfarandi upplýsingar eru færðar inn

    |Gerð|Nr.|Magn|Qty.to Nota|
    |----|---|--------|--------|   
    |Forði|RESOURCE1|2|2|

2. Í þjónustupöntuninni er notkunin bókuð
   1.  **Veljið Bóka** aðgerð til að ljúka þjónustupöntuninni, veljið aðgerðina **Afhenda og nota** og veljið **svo Í lagi** hnappinn.

### <a name="results-3"></a>Niðurstöður

- Þjónustufærslur eru stofnaðar sem tengjast þjónustuvörunni, þjónustusamningnum og forðanum.

## <a name="see-also"></a>Sjá einnig .

[Kynning á Contoso Kaffi kynningargögnum](../../contoso-coffee/contoso-coffee-intro.md)  
[Um framleiðslupantanir](../../production-about-production-orders.md)
