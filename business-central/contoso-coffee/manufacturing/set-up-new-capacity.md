---
title: Setja upp nýja getu
description: Kynning um hvernig á að setja upp nýja vinnustöð með dagatali afkastagetu fyrir eina vakt í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Kynning: Setja upp nýja afkastagetu

Í þessari grein förum við í gegnum skrefin um hvernig á að nota sýnigögn Contoso Coffee til að stjórna afkastagetu.  

## Aðstæður

Þú ert framleiðslustjóri á Contoso Coffee. Til að bregðast við breytingum á gólfi vinnusalar verður að setja upp nýja vinnustöð, prófunardeild. Nýja vinnustöðin er með eina vélastöð, prófun. Nýju stöðvarnar verða að vera með dagatal afkastagetu fyrir eina vakt frá 08:00 til 16:00, mánudaga til föstudaga.  

## Skref

1. Setja upp vinnustöðina.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnustöðvar** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Nr.** |700|
        |**Heiti** |Prófunardeild|
        |**Kóði vinnustöðvarhóps** |1, Framleiðsludeild|
        |**Innkaupsverð**|3.25|
        |**Útreikningur kostn.verðs**|Tími|
        |**Flæðiaðferð**|Handvirkt|
        |**Alm. vörubókunarflokkur**|ENGINN VSK</br></br>Athugið að þetta val fer eftir bókhaldsuppsetningum og landi/svæði.|
        |**Mælieiningarkóði** |MÍNÚTUR|
        |**Afkastageta** |1|
        |**Skilvirkni** |90|
        |**Dagatalskóði verkstæðis** |1|

        Í reitnum **Dagatalskóði verslunar** þýðir stilling 1 ein vakt frá mánudegi til föstudags.

    3. Lokaðu vinnustöðvarspjaldinu.

2. Setja upp vélastöðina.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **vélastöðvar** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Nr.** |760|
        |**Heiti** |Prófun|
        |**Vinnustöðvarnr.** |700, prófunardeild|
        |**Innkaupsverð**|3.25|
        |**Flæðiaðferð**|Handvirkt|
        |**Alm. vörubókunarflokkur**|ENGINN VSK</br></br>Athugaðu að þetta val fer eftir bókhaldsuppsetningu og landi.|
        |**Afkastageta** |1|
        |**Skilvirkni** |90|
    3. Stækkaðu flýtiflipann **Uppsetning leiðar** og síðan í reitinn **Uppsetningartími** skal færa inn *10*.  

3. Reiknaðu dagatal afkastagetu fyrir vélastöðina.  

    1. Veljið aðgerðina **Dagatal**.  

    2. Á síðunni **Dagatal vélastöðvar**, í flýtiflipanum **Valkostir fylkis**, skal stilla reitinn **Skoða eftir** á *Mánuður*.  

    3. Veljið aðgerðina **Sýna fylki**.  

    4. Á síðunni **Dagatalsfylki vélastöðvar** skal velja aðgerðina **Reikna út**.  

    5. Á síðunni **Reikna dagatal vélastöðvar**, í flýtiflipanum **Valkostir**, skal stilla reitinn **Upphafsdagsetning** á *1. janúar*.  

    6. Stilltu reitinn **Lokadagsetning** á 31. desember.  

    7. Í flýtiflipanum **Vélastöð**, í **Nr.** síureitnum, skal velja *760, Prófun*.  

    8. Velja hnappinn **Í lagi**. Þegar runuvinnslunni lýkur skilar hún þér á síðuna **Fylkisdagatal vélastöðvar**.  

    9. Velja aðgerðina **Uppfæra**.  

    10. Í línunni fyrir vélastöð 760, prófun, skaltu kafa niður í gildið í dálknum fyrir janúar.  

Á síðunni **Dagatalsfærslur** eru daglegar færslur afkastagetu í reitnum **Afkastageta (alls)** fyrir 480 mínútur. Þetta samsvarar einni átta tíma vakt fyrir hvern vinnudag. Einnig sýnir reiturinn **Afkastageta (virk)** 432 mínútur. Þetta stendur fyrir 90 prósent skilvirknihlutfallið sem þú úthlutaðir vélastöðinni.  

## Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](../contoso-coffee-intro.md)  
