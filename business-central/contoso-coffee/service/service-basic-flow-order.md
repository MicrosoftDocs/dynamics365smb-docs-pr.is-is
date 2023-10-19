---
title: Ganga frá þjónustupöntunum á þjónustuvörum
description: Þessi grein leiðbeinir í gegnum nokkra kjarnaferla sem taka við þjónustupöntunum og vörunum.
author: andreipa
ms.author: andreipa
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# <a name="walkthrough-of-service-orders-for-service-items"></a>Ganga frá þjónustupöntunum á þjónustuvörum

Þessi gönguleið sýnir fram á nokkra kjarnaferla:

- Stofna tilfallandi þjónustupöntun og skrá viðgerð á vörunni
- Veita skal Lánsumsókn til viðskiptavinar um tíma frá viðgerð
- Bóka og reikningsfæra þjónustupöntunina
    
## <a name="creating-a-service-order"></a>Þjónustupöntun stofnuð

### <a name="scenario"></a>Aðstæður

Charles, þjónustustjóri, stofnar þjónustupöntun fyrir viðgerðartíma, lánar Lánstæki til viðskiptavinar vegna viðgerðar.

### <a name="steps"></a>Skref

1. Stofnið þjónustupöntunina handvirkt fyrir vöruna sem þarfnast viðgerðar.
   1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn  **þjónustupantanir**
   2. Valið er aðgerðin **Nýtt**.
   3. Færa  **10000**  inn í reitnum viðskm. nr. reitur
   4. Velja  **viðgerð**  fyrir  **reitinn Tegund**  þjónustupöntunarinnar.
   5. Í línunum er valið  **S-100**  sem  **Vörunr.**
2. Einnig
   1. Velja villuleit Línuaðgerðaleitar  **·**  til að kanna mögulegar lausnir.
   2. Velja Línuaðgerðina  **Villa/Resol. Sambönd í kótum**
   3. Velja  *hávaða*  sem  **einkennakóta**
   4. Veldu  *5-2 hávær læti á gerjun*  sem  **faul Code**  og loka síðu. Villukóði, úrlausnarkóði er uppfærður í línum.
3. Lána skiptiborð meðan verið er að lagfæra vöru
   1. Í línurnar er valið  **LOANER1**  sem lánsbúnaður nr. Staðfestu útgefendur lánsbúnaðarins með því að velja  **Já**  til að lána lánsbúnaðinum út. 
   2. Velja aðgerðina  **Aðgerðir sækja þjónustukóta**, velja staðlaðan kóta sem tengist þjónustuflokki og smella á  **í lagi**.
   
### <a name="results"></a>Niðurstöður

- Þjónustupöntun verður stofnuð fyrir vöruna
- Í Þjónustuskjalaskrá þjónustupöntunarinnar verða Verkþættir lánsbúnaðar sýnir.
- Lánveitandi skal hafa bókfærslu til að endurspegla útlánsvexti.
   

## <a name="regsiter-performed-work-mark-loaner-as-returned"></a>Regsiter framkvæmdi vinnu, merkt lánsumsókn sem Skilaskyld.

### <a name="scenario-1"></a>Aðstæður

Þjónustutæknimaður markar lánsbúnað sem skilað er, skráir framkvæmd vinnu.

### <a name="steps-1"></a>Skref

1. Finna þjónustuverkhluta og skrá tíma 
   1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuverk** og svo velja viðeigandi tengil.
   2. Þjónustupöntunin er fundin með til að færa inn tíma.
   3. Velja skal  **aðgerðina vörublað** .
   4. Sláðu inn eftirfarandi upplýsingar

    |Gerð|Nr.|Magn|
    |----|---|--------|  
    |Atriði|SER102|2|

   4. Valið  *er*  lokið  **í reitnum Viðgerðarstöðukóti** 
    
2. Merkja lánsbúnað sem skilabúnað
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánsbúnað** og velja síðan viðkomandi tengil.
   2. Staðsetja skal lánsbúnað til að merkja sem skilað.
   3.  **Velja móttökuaðgerð**  
   4. Staðfesta skil á lánsbúnaðinum með því að velja  **Já**  til að skila lánsbúnaðinum.
      
### <a name="results-1"></a>Niðurstöður

- Í Þjónustuskjalaskrá  **þjónustupöntunarinnar**  verða Verkþættir lánsbúnaðar sýnir.
- Lánveitandi skal hafa bókfærslu til að endurspegla móttökunina.


### <a name="scenario-2"></a>Aðstæður

Charles, þjónustustjóri, bóka Afgreiddar þjónustupöntunina.

1. Finna þjónustupöntunina 
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.
   2. Finna skal þjónustupöntunina sem á að bóka.

2. Á þjónustupöntuninni er reikningurinn bókaður
   1. Velja skal  **aðgerðina Bóka**  til að ljúka þjónustupöntuninni, velja  **senda og reikningsfæra**  aðgerð og velja svo hnappinn í  **lagi** .
   2. Staðfestu opnun bókaðs reiknings með því að velja  **Já**. 
### <a name="results-2"></a>Niðurstöður

-  **bókaður Þjónustureikningurinn**  er stofnaður.
-  **þjónustufærslur**  sem tengjast vörunni og forða eru stofnaðar

## <a name="see-also"></a>Sjá einnig .
