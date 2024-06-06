---
title: Setja upp og vinna úr aðgerð úthýsingar
description: Kynning á hvernig á að setja upp og vinna úr úthýsingaraðgerð í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="set-up-and-process-a-subcontracting-operation"></a>Setja upp og vinna úr aðgerð úthýsingar

Í þessari grein förum við í gegnum skrefin til að nota sýnigögn Contoso Coffee í úthýsingu.

## <a name="scenario"></a>Aðstæður

Þú ert framleiðslustjóri á Contoso Coffee. Vegna takmarkana á afkastagetu ætlar þú að nota úthýsingu til að framleiða vöruna **SP-SCM1009 Airpot**.

Hér býrðu til nýja útgefna framleiðslupöntun fyrir 12 einingar af vörunni SP-SCM1009 Airpot, með leið - SP-SCM1009-SUB-2. Notaðu vinnublað undirverktakasamninga til að stofna innkaupapöntun fyrir framleiðsluna og síða ljúka aðgerðinni með því að taka á móti og reikningsfæra innkaupapöntunina.

## <a name="steps"></a>Skref

1. Stofnaðu nýja útgefna framleiðslupöntun fyrir 12 einingar af vörunni SP-SCM1009, Airpot.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Tegund uppruna** |Atriði|
        |**Upprunanúmer** |SP-SCM1009|
        |**Magn** |100|
    3. Veldu aðgerðina **Uppfæra framleiðslupöntun**.  

2. Skiptu um leið í SP-SCM1009-SUB-2 í framleiðslupöntunarlínunni og uppfærðu síðan framleiðslupöntunina en aðeins fyrir leið.  

    1. Bættu reit framleiðsluleiðarnr. við línurnar í útgefinni framleiðslupöntun.<!--in code, this is marked as visible=false-->

    2. Breyttu reitnum **Leiðarnúmer** úr *SP-SCM1009-SERIAL* í *SP-SCM1009-SUB-2*.  

    3. Veldu aðgerðina **Uppfæra framleiðslupöntun**.  

    4. Á beiðnisíðunni **Uppfæra framleiðslupöntun** skal hreins reitina **Línur** og **Íhlutaþörf** þannig að verkið mun aðeins keyra fyrir leið og veldu síðan hnappinn **Í lagi**.

3. Notaðu vinnublað undirverktakasamninga til að búa til innkaupapöntun fyrir aðgerð undirverktaka í framleiðslupöntuninni sem stofnuð var í skrefi 2.  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublöð undirverktaka** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Reikna undirverktakasamninga**.

    3. Veldu reitinn **Samþykkja aðgerðaboð** fyrir nýju línuna.

    4. Veljið aðgerðina **Framkvæma aðgerðaboð**.  

    5. Á beiðnisíðunni **Framkv. aðg.boð - Beiðni** skal samþykkja öll sjálfgefin gildi og síðan velja hnappinn **Í lagi**.

    6. Þegar runuvinnslunni lýkur skal velja hnappinn **Í lagi** til að loka undirverktakavinnublaðinu,  

4. Taktu á móti og reikningsfærðu innkaupapöntunina.  

    1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  

    2. Á listanum **Innkaupapantanir** skal finna innkaupapöntunina úr lánardrottini 82000 undirverktaka.

    3. Í reitinn **Reikningsnúmer lánardrottins** skal færa inn *542349*.

    4. Í flýtiflipanum **Línur** skal velja línuna og síðan stilla reitinn **Beinn kostnaður** á *18*.

    5. Valið er **Bóka** aðgerðin.  

    6. Í skilaboðum beiðninnar skal velja valkostinn **Taka á móti og reikningsfæra**.  

Úttak vörunnar SP-SCM1009 Airpot er nú skráð.

## <a name="see-also"></a>Sjá einnig .

[Kynning á Contoso Kaffi kynningargögnum](../contoso-coffee-intro.md)  
