---
title: Endurmeta eignir
description: Kynntu þér hvernig skal laga virði eigna, skrá nýjar upphæðir sem niðurfærslu eða uppfærslu og bóka viðbótarkaupverð.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5628, 5629, 5633
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ba537dd27fedfb204483d81815380d0910676c20
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532215"
---
# <a name="revalue-fixed-assets"></a>Endurmeta eignir

Endurmat eigna getur samanstaðið af uppfærslu, niðurfærslu, og leiðréttingum á almennu virði.

Þegar virði eignar hefur hækkað, er bókuð færslubókarlínu með hærri upphæð, uppfærslu í afskriftabókina. Nýtt verð er skráð sem uppfærslu samkvæmt bókunargrunni eigna.

Þegar virði eignar hefur lækkað, bókarðu færslubókarlínu með lægri upphæð, niðurfærslu, í afskriftabók. Nýtt verð er skráð sem niðurfærslu samkvæmt bókunargrunni eigna.

Endurmat er notað til að laga virði margra eigna, til dæmis, að almennum verðbreytingum. Hægt er að nota keyrsluna **Endurmat eigna** til að breyta ýmsum upphæðum, svo sem upphæðum niðurfærslna og uppfærslna.

## <a name="to-post-an-appreciation-from-the-fixed-asset-gl-journal"></a>Bóka uppfærslu úr fjárhagsbók eigna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.
3. Í reitnum **Eignabókunartegund** er valinn **endurmat**.
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun uppfærslu.

    > [!NOTE]  
    >   Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **Uppfærslureikningur** debetreikning fjárhags og **Mótreikningur uppfærslu** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir endurmat. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Valið er **Bóka** aðgerðin.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a>Bóka niðurfærsla úr fjárhagsbók eigna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.
3. Í reitnum **Eignabókunartegund** er valinn **niðurfærsla**.
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun niðurfærslu.

    > [!NOTE]  
    >   Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **niðurfærslureikningur** kreditreikning fjárhags og **Útgjaldareikningur niðurfærslu** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir niðurfærslur. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Valið er **Bóka** aðgerðin.

## <a name="to-perform-general-revaluation-of-fixed-assets"></a>Framkvæma almennt endurmat eigna

Endurmat er notað til að laga virði margra eigna, til dæmis, að almennum verðbreytingum. Hægt er að nota keyrsluna **Endurmat eigna** til að breyta ýmsum upphæðum, svo sem upphæðum niðurfærslna og uppfærslna. **Leyfa endurmat** gátreiturinn á síðunni **Afskriftabók** verður að vera valinn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurmat eignar** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.
3. Velja hnappinn **Í lagi**.

    Endurmatslínur eru búnar til samkvæmt stillingu í skref 2. Línur eru búnar til annaðhvort í færslubók eigna, allt eftir sniðmáti þínu og uppsetningu keyrslu á síðunni **Eignabókargrunnur**. Frekari upplýsingar eru í [Uppsetning almennra eignaupplýsinga](fa-how-setup-general.md).
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
5. Velja bókina með eignir sem á að endurmeta og síðan valið aðgerðin **Færslur**.  
6. Athugaðu Stofnaðar færslur, og síðan valið **Bóka** aðgerð til að bóka bókina.

    > [!TIP]  
    >   Ef endurmatstölurnar eru aðeins til sýnis er hægt að búa til sérstaka afskriftabók til að geyma þær í. Þá hafa þessar færslur ekki áhrif á aðrar afskriftabækur.

## <a name="to-post-additional-acquisition-costs"></a>Bókun Viðbótarkaupverðs

Annar stofnkostnaður eignar er bókaður eins og upphaflegi stofnkostnaðurinn: úr innkaupareikningi eða úr eignabók. Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).  

Ef afskriftir hafa þegar verið reiknaðar fyrir eignina er sett gátmerki í reitinn **Afskr. kaupverðs** til að annar stofnkostnaður að frádregnu hrakvirði verði afskrifaður í hlutfalli við upphæðina sem áður keypt eign hefur þegar verið afskrifuð um. Þetta tryggir að afskriftatímabilið breytist ekki.  

Afskriftaprósentan er reiknuð sem:  

*P = (heildarafskriftir x 100) / afskriftagrunnur*

*Afskriftaupphæð = (P/100) x (viðbótarstofnkostnaður - hrakvirði)*  

Muna þarf að setja gátmerkið í reitinn **Afskr. til eignabókunardags.** í reikningi, eignafjárhagsbókar- eða eignabókarlínurnar til að tryggja að afskrift sé reiknuð frá síðasta eignabókunardegi til bókunardags annars kaupverðs.

### <a name="example---posting-additional-acquisition-costs"></a>Dæmi - bókun viðbótar stofnkostnaðar

Vél er keypt 1. ágúst, 2000. Stofnkostnaðurinn er 4.800. Afskriftaaðferðin er línuleg til fjögurra ára.

31. ágúst, 2000, er keyrslan **Reikna afskrift** keyrð. Afskriftir eru reiknaðar sem:

*bókfært virði x fjöldi afskriftadaga / heildarfjöldi afskriftadaga = 4800 x 30 / 1440 = 100*  

september, 2000, er sölureikningur bókaður vegna málningar á vélinni. Upphæðin á reikningnum er 480.

Ef valið var **Afskr. til eignabókunardags.** gátreiturinn á reikningnum fyrir bókun, fara fram eftirfarandi útreikningar:  

15 daga afskriftir (frá 01/09/00 til 15/09/00) eru reiknaðar sem:

*bókfært virði x fjöldi afskriftadaga / eftirstandandi fjöldi afskriftadaga = (4800 - 100) x 15 / 1410 = 50*

Ef valið var **Afskr. kaupverðs.** gátreiturinn á reikningnum fyrir bókun, fara fram eftirfarandi útreikningar:  

*Annar stofnkostnaður er afskrifaður um ((150 x 100) / 4800) / 100 x 480 = 15*

Afskriftagrunnurinn er núna *5280 = (4800 + 480)* og uppsafnaðar afskriftir eru *165 = (100 + 50 +15)* sem samsvarar 45 daga afskriftum á heildarkaupverði. Það merkir að eignin verði að fullu afskrifuð innan áætlaðs fjögurra ára líftíma.  

Þegar keyrslan **Reikna afskriftir** er keyrð 30/09/00 eru útreikningar með eftirfarandi hætti:  

*Eftirstöðvar afskriftartíma eru 3 ár, 10 mánuðir og 15 dagar = 1395 dagar*  

*Bókfært virði er (5280 -165) = 5115*  

*Afskriftaupphæð fyrir september 2000: 5115 x 15 / 1395 = 55,00*  

*Heildarafskriftir = 165 + 55 = 220*  

Ef þú valdir ekki gátreitinn **Afskr. þar til eignabókunardags.** glatar eignin 15 daga afskriftum vegna þess að runuvinnslan **Reikna afskriftir** sem keyrð er á 30/09/00 reiknar afskriftir frá 15/09/00 til 30/09/00. Það merkir að þegar keyrslan **Reikna afskriftir** er keyrð 30/09/00 eru útreikningarnir sem hér segir:  

*Eftirstöðvar líftíma eru 3 ár, 10 mánuðir og 15 dagar = 1395 dagar*  

*Bókfært virði er (4800 + 480 - 100 - 15) = 5165*

*Afskriftaupphæð fyrir september 2000: 5165 x 15 / 1395 = 55,54*  

*Heildarafskriftir = 100 + 15 + 55,54 = 170,54*

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/paths/manage-advanced-fixed-assets-transactions/)

## <a name="see-also"></a>Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
