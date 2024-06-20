---
title: Yfirferð þjónustupantana fyrir þjónustuvörur
description: Þessi grein leiðir þig í gegnum nokkur kjarnaferla sem fela í sér þjónustupantanir og vörur.
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-service-orders-for-service-items"></a>Yfirferð þjónustupantana fyrir þjónustuvörur

Þessi leiðsögn sýnir nokkra kjarnaferla:

- Búðu til ad hoc þjónustupöntun og skráðu viðgerð á hlutnum
- Veittu viðskiptavinum lánshlut til viðgerðartíma
- Bókaðu og reikningsfærðu þjónustupöntunina
    
## <a name="creating-a-service-order"></a>Að búa til þjónustupöntun

### <a name="scenario"></a>Aðstæður

Charles, þjónustustjóri, býr til þjónustupöntun fyrir viðgerðaratburðarás, lánar lánveitanda til viðskiptavinar til viðgerðartíma.

### <a name="steps"></a>Skref

1. Búðu til þjónustupöntun handvirkt fyrir vöruna sem þarfnast viðgerðar.
   1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Þjónustupantanir**
   2. Valið er aðgerðin **Nýtt**.
   3. Sláðu inn **10000** í viðskiptavinarnúmerið. reitur
   4. Veldu **REPAIR** fyrir reitinn **Þjónustupöntunartegund** .
   5. Í línunum skaltu velja **S-100** sem **vörunr.**.
2. Valfrjálst
   1. Veldu línuaðgerðina **Úrræðaleit** til að athuga mögulegar lausnir.
   2. Veldu línuaðgerðina **Billa/úrlausn. Codes Sambönd**
   3. Veldu *NOISE* sem **Einkenniskóða**
   4. Veldu *5-2 Hávær hávaði við bruggun* sem **Bilunarkóði** og lokaðu síðunni. Bilunarkóði, upplausnarkóðar eru uppfærðir í línum.
3. Lána varahlut á meðan verið er að gera við hlutinn
   1. Í línunum skaltu velja **LOANER1** sem lánveitanda nr. Staðfestu útgáfu lánveitanda með því að velja **Já** til að lána lánveitanda. 
   2. Veldu aðgerðina Aðgerðir **Fá Std. Þjónustukóðar**, veldu staðlaðan kóða sem tengist þjónustuhópnum og veldu **Ok**.
   
### <a name="results"></a>Niðurstöður

- Þjónustupöntun er búin til fyrir vöruna
- Þjónustuskjalaskrá þjónustupöntunarinnar sýnir starfsemi lánveitanda.
- Lánveitandinn hefur fjárhagsfærslu til að endurspegla útlánið.
   

## <a name="register-performed-work-mark-loaner-as-returned"></a>Skráðu unnin verk, merktu lánveitanda sem skilað.

### <a name="scenario-1"></a>Aðstæður

Þjónustutæknir merkir lánveitanda sem skilaðan, skráir unnin störf.

### <a name="steps-1"></a>Skref

1. Finndu þjónustuverkefnið og skráðu tíma 
   1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuverk** og svo velja viðeigandi tengil.
   2. Finndu þjónustupöntunina til að slá inn tíma fyrir.
   3. Veldu aðgerðina **Item Worksheet** .
   4. Sláðu inn eftirfarandi upplýsingar

    |Gerð|Nr.|Magn|
    |----|---|--------|  
    |Atriði|SER102|2|

   4. Veldu *FINISHED* í reitnum **Viðgerðarstöðukóði** 
    
2. Merktu lánveitanda sem skilaðan
   1. Veldu ![peru sem opnar Segðu mér eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánsbúnað** og velja síðan viðkomandi tengil.
   2. Finndu lánveitanda til að merkja sem skilað.
   3. Veldu aðgerðina **Receive**  
   4. Staðfestu skil lánsmanns með því að velja **Já** til að skila lánveitanda.
      
### <a name="results-1"></a>Niðurstöður

-  **Þjónustuskjalaskrá þjónustupöntunarinnar**  sýnir starfsemi lánveitanda.
- Lánveitandinn hefur fjárhagsfærslu til að endurspegla kvittunina.


### <a name="scenario-2"></a>Aðstæður

Charles, þjónustustjóri, birtir fullgerða þjónustupöntun.

1. Finndu þjónustupöntunina 
   1. Veldu ![peru sem opnar Segðu mér eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.
   2. Finndu þjónustupöntunina sem þú vilt senda.

2. Bókaðu reikninginn á þjónustupöntuninni
   1. Veldu aðgerðina **Posta** til að ljúka þjónustupöntuninni, veldu **Send og reikning** aðgerðina og veldu síðan  **OK** hnappur.
   2. Staðfestu opnun bókaðs reiknings með því að velja **Já**. 
### <a name="results-2"></a>Niðurstöður

-  **Bókaður þjónustureikningur** er búinn til.
-  **Þjónustubókarfærslurnar** sem tengjast vörunni og tilföngunum eru búnar til

## <a name="see-also"></a>Sjá einnig .
[Kynning á þjónustusamningum fyrir þjónustuvörur](service-contract-flow.md)  
[Þjónusta](../../service-service.md)
