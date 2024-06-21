---
title: Endurmeta eignir
description: 'Læra að leiðrétta virði eigna, skrá nýjar upphæðir sem niðurfærslu eða uppfærslu og bóka annan stofnkostnað.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '5628, 5629, 5633'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Endurmeta eignir

Endurmat eigna getur samanstaðið af uppfærslu, niðurfærslu, og leiðréttingum á almennu virði.

Þegar virði eigna eykst er færslubókarlína með uppfærslu í afskriftabókina bókuð. Nýja upphæðin er skráð sem uppfærsla samkvæmt bókunargrunni eigna.

Þegar virði eignar lækkar er bókarlína með lægri upphæð, niðurfærslu í afskriftabókina. Nýtt verð er skráð sem niðurfærslu samkvæmt bókunargrunni eigna.

Endurmat er notað til að laga virði margra eigna, til dæmis, að almennum verðbreytingum. Hægt er að nota keyrsluna **Endurmat eigna** til að breyta ýmsum upphæðum, svo sem upphæðum niðurfærslna og uppfærslna.

## Bókun uppfærslna úr eignafjárhagsbók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.
3. Í reitnum **Eignabókunartegund** er valinn **endurmat**.
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun uppfærslu.

    > [!NOTE]  
    >   Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **Uppfærslureikningur** debetreikning fjárhags og **Mótreikningur uppfærslu** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir endurmat. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Valið er **Bóka** aðgerðin.

## Bóka niðurfærsla úr fjárhagsbók eigna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.
3. Í reitnum **Eignabókunartegund** er valinn **niðurfærsla**.
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun niðurfærslu.

    > [!NOTE]  
    >   Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **niðurfærslureikningur** kreditreikning fjárhags og **Útgjaldareikningur niðurfærslu** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir niðurfærslur. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Valið er **Bóka** aðgerðin.

## Framkvæma almennt endurmat eigna

Endurmat er notað til að laga virði margra eigna, til dæmis, að almennum verðbreytingum. Hægt er að nota keyrsluna **Endurmat eigna** til að breyta ýmsum upphæðum, svo sem upphæðum niðurfærslna og uppfærslna. Velja verður gátreitinn **Leyfa endurmat** á síðunni **Afskriftabók** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurmat eignar** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.
3. Velja hnappinn **Í lagi**.

    Endurmatslínur eru búnar til samkvæmt stillingu í skref 2. Línur eru búnar til annaðhvort í færslubók eigna, allt eftir sniðmáti þínu og uppsetningu keyrslu á síðunni **Eignabókargrunnur**. Frekari upplýsingar eru í [Uppsetning almennra eignaupplýsinga](fa-how-setup-general.md).
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
5. Velja bókina með eignir sem á að endurmeta og síðan valið aðgerðin **Færslur**.  
6. Athugaðu Stofnaðar færslur, og síðan valið **Bóka** aðgerð til að bóka bókina.

    > [!TIP]  
    >   Ef endurmatstölurnar eru aðeins til sýnis er hægt að búa til sérstaka afskriftabók til að geyma þær í. Þá hafa þessar færslur ekki áhrif á aðrar afskriftabækur.

## Bókun annars stofnkostnaðar

Annar stofnkostnaður eignar er bókaður úr innkaupareikningi eða úr eignabók á sama hátt og upphaflegur stofnkostnaður er bókaður. Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).  

Ef afskriftir eru þegar reiknaðar fyrir eignina er reiturinn **Afskr. valinn. Gátreiturinn Stofnkostnaður** til að annar stofnkostnaður að frádregnu hrakvirðinu er afskrifaður í hlutfalli við upphæðina sem áður keypt eign er afskrifuð um. Þessi aðferð tryggir að afskriftatímabilinu sé ekki breytt.  

Afskriftaprósentan er reiknuð sem:  

*P = (heildarafskriftir x 100) / afskriftagrunnur*

*Afskriftaupphæð = (P/100) x (viðbótarstofnkostnaður - hrakvirði)*  

Muna þarf að velja gátreitinn **Afskr. til eignabókunardags** . í reikningnum, eignafjárhagsbókinni eða eignabókarlínunum til að tryggja að afskriftir séu reiknaðar frá síðustu eignabókunardagsetningu til bókunardagsetningar annars stofnkostnaðar.

### Dæmi - Bókun annars stofnkostnaðar

Vél er keypt 1. ágúst, 2000. Stofnkostnaðurinn er 4.800. Afskriftaaðferðin er línuleg til fjögurra ára.

31. ágúst, 2000, er keyrslan **Reikna afskrift** keyrð. Afskriftir eru reiknaðar sem:

*bókfært virði x fjöldi afskriftadaga / heildarfjöldi afskriftadaga = 4800 x 30 / 1440 = 100*  

september, 2000, er sölureikningur bókaður vegna málningar á vélinni. Upphæðin á reikningnum er 480.

Ef gátreiturinn **Afskr. til eignabókunardags** . var valinn á reikningnum fyrir bókun er eftirfarandi útreikningur gerður:  

15 daga afskriftir (frá 01/09/00 til 15/09/00) eru reiknaðar sem:

*bókfært virði x fjöldi afskriftadaga / eftirstandandi fjöldi afskriftadaga = (4800 - 100) x 15 / 1410 = 50*

Ef valið var reiturinn **Afskr. Gátreiturinn Stofnkostnaður** á reikningnum fyrir bókun er eftirfarandi útreikningur gerður:  

*Annar stofnkostnaður er afskrifaður sem ((150 x 100) / 4800) / 100 x 480 = 15*

Afskriftagrunnurinn er núna *5280 = (4800 + 480)* og uppsafnaðar afskriftir eru *165 = (100 + 50 +15)* sem samsvarar 45 daga afskriftum á heildarkaupverði. Útreikningurinn þýðir að eignin er að fullu afskrifuð innan áætlaðs fjögurra ára líftíma.  

Þegar keyrslan **Reikna afskriftir** er keyrð 30/09/00 eru útreikningar með eftirfarandi hætti:  

*Eftirstöðvar afskriftartíma eru 3 ár, 10 mánuðir og 15 dagar = 1395 dagar*  

*Bókfært virði er (5280 -165) = 5115*  

*Afskriftaupphæð fyrir september 2000: 5115 x 15 / 1395 = 55,00*  

*Heildarafskriftir = 165 + 55 = 220*  

Ef gátreiturinn **Afskr. fyrr en eignabókunardags** . var ekki valinn myndi eignin tapa 15 daga afskrift vegna þess að **keyrslan Reikna afskriftir** 09/30/00 myndi reikna afskriftir frá 09/15/00 til 30/09/00. Það merkir að þegar keyrslan **Reikna afskriftir** er keyrð 30/09/00 eru útreikningarnir sem hér segir:  

*Eftirstöðvar líftíma eru 3 ár, 10 mánuðir og 15 dagar = 1395 dagar*  

*Bókfært virði er (4800 + 480 - 100 - 15) = 5165*

*Afskriftaupphæð fyrir september 2000: 5165 x 15 / 1395 = 55,54*  

*Heildarafskriftir = 100 + 15 + 55,54 = 170,54*

## Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
