---
title: Tryggja eignir
description: Þú getur úthlutað einni eða fleirum eignum á eitt tryggingaskírteini með því að bóka í fjárhagsbók vátryggingar af síðunni **Vátryggingabók**.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Tryggja eignir

Nota síðuna **Vátryggingarspjald** til að setja upp vátryggingarskilmála til að ná yfir eina eða fleiri eignir. Hægt er að úthluta einni eign einni vátryggingu eða mörgum eignum á eina vátryggingu.

Þú úthlutar eign á vátryggingarskírteini með því að bóka í vátryggingasviðsbók á síðunni **Vátryggingabók** .

Þar að auki er hægt að úthluta eign á vátryggingarskírteini og stofna vátryggingasviðsfærslur þegar þú bókar kaupverð hennar. Stofnkostnaður er bókaður úr eignabókinni með reitnum **Vátryggingarnúmer.** Fyllt er í reitinn. Kveikja verður á **víxli sjálfvirkrar vátryggingarbókunar** á síðunni **Eignagrunnur** . Nánari upplýsingar [eru í Eigna eign með því að nota eignafjárhagsbók](fa-how-acquire.md#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

 **Ef víxlið sjálfvirkrar vátryggingarbókunar** á **síðunni Eignagrunnur** er ekki kveikt á stofnar bókun kaupanna úr eignabókinni línur á síðunni **Vátryggingabók** . Þessar línur verður að bóka handvirkt.

> [!WARNING]  
> Ef ekki er kveikt á **víxli sjálfvirkrar vátryggingarbókunar** á síðunni **Eignagrunnur** ætti vátryggingabókin að vera byggð á bókarsniðmáti án númeraraða. Þetta er af því að innsett fylgiskjalsnúmerum úr eignabókarlínum munu annars skarast við númeraröðina í vátryggingabók. Nánari upplýsingar um sniðmát færslubókar og keyrsla sjá [Setja upp almennar upplýsingar um eignir](fa-how-setup-general.md).

Þegar eign hefur verið tengd vátryggingu er **Já**  í reitnum **Vátrygging** á eignaspjaldinu. Þegar eign er selt er slökkt á víxlnum sjálfkrafa.

## Stofna eða Breyting á vátryggingaspjöldum:

Þegar upplýsingar um breytingar á tryggingarupphæð berast verður að færa nýju upplýsingarnar inn á síðuna **Vátryggingarspjald** til að tryggja að greining vátryggingasviðs sé rétt.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Trygging** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Nýtt** til að Búa til nýtt kort fyrir vátryggingarskírteini. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Einnig geturðu valið vátryggingarskírteini sem þú vilt breyta og veldu svo aðgerðina **Breyta**.

## Til að Tengja eign við vátryggingarskírteini með því að bóka úr vátryggingabók.

Þú úthlutar eign á vátryggingarskírteini með því að bóka í vátryggingasviðsbók.  

Eftirfarandi ferli útskýrir hvernig stofna vátryggingarbókarlínu handvirkt.  **Ef víxlið fyrir sjálfvirka vátryggingarbókun** er kveikt á síðunni **Eignagrunnur** verða vátryggingabókarlínur sjálfkrafa stofnaðar þegar stofnkostnaður er bókaður. Í því tilfelli er allt sem þarf að gera er að bóka færslubókina.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") í reitnum Leit skal færa inn **Vátryggingabók** og velja síðan viðkomandi tengil.  
2. Opna skal viðeigandi færslubók og fylla færslubókarlínurnar út eftir þörfum.  
3. Til að úthluta mörgum eignum á eina vátryggingarskírteini, skal stofna færslubókarlínur með sömu gildum og í **Vátryggingarnr.** reitnum og öðrum gildum í **Eignanr.** reitnum.  
4. Valið er **Bóka** aðgerðin.  

    > [!NOTE]  
    > Færslurnar í vátryggingabók eru aðeins bókaðir í vátryggingasviðshöfuðbókina.  

## Uppfæra tryggingarvirði eignar

Í eftirfarandi dæmi er sýnt hvernig hægt er að nota keyrsluna **Endurmat vátrygginga** til að uppfæra verðmæti eigna sem eru tryggðar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurmat vátryggingar** og velja síðan viðkomandi tengil.
2. Fyllið inn í reitina eftir þörfum.

    > [!NOTE]  
    >   Í reitnum **Vísitala** skráir þú lækkun uppá 5%, til dæmis, sem 95, en þú skráir aukningu uppá 2% sem 102.  
3. Velja hnappinn **Í lagi**.  

   Keyrslan reiknar þessa nýju tölu sem hlutfall af vátryggðu heildarvirði eins og kemur fram á síðunni **Vátryggingaupplýsingar** og býr til línu í vátryggingabókinni.  
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") í reitnum Leit skal færa inn **Vátryggingabók** og velja síðan viðkomandi tengil.  
5. Opnaðu viðeigandi Vátryggingabók, endurskoðaðu stofnuð gildi og bókaðu þau síðan í vátryggingasviðshöfuðbókina.  

## Eftirlit með vátryggingasviði

[!INCLUDE[prod_short](includes/prod_short.md)] veitir sérhæfðar skýrslu- og tölfræðisíður til að greina vátryggingarskilmála, og hvort eignir þínar eru oftryggðar eða vantryggðar.  

### Yfirlit yfir vátryggingarskírteini

Til að fá yfirlit yfir vátryggingarskilmála þína skaltu forskoða eða prenta **Vátrygging - Listi** skýrsluna. Skýrslan sýnir alla skilmálana og mikilvægustu reitina af vátryggingarspjöldunum.  

### Vátryggingasvið

Ef skoða á hvaða eignir eru vátryggðar eða hvaða vátryggingar gilda fyrir hverja eign er hægt að prenta eða forskoða skýrsluna **Vátrygging - Tryggt heildarv.**.  

#### Of-/vantrygging

Hægt er að kanna hvort eignir séu yfir- eða vantryggingar með eftirfarandi hætti:  

* Síðan **Vátryggingaupplýsingar**. Plústala í reitnum **Yfir-/undirtryggt** merkir að eignin sé yfirtryggð. Neikvæð upphæð merkir að eignin sé vantrygging.  
* Síðan **Eignaupplýsingar** . Veldu reitinn **Vátryggt heildarvirði** til að skoða síðuna **Vátryggingasviðsfærslur**.  
* **Yfir-/undir Vátryggingasvið** skýrslu.  
* **Tryggingagreining** skýrslan  

### Ótrúlegar eignir

Ef ganga á úr skugga um hvort gleymst hafi að úthluta eign á vátryggingu er hægt að prenta eða forskoða skýrsluna **Vátrygging - Ótengdar eignir** . Þessi skýrsla sýnir eignir þar sem upphæðir eru ekki bókaðar í vátryggingasviðsbókina.  

## Skoðun vátryggingasviðsfærslna:

Hægt er að skoða færslurnar sem gerðar hafa verið í vátryggingasviðsbókinni.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Trygging** og velja síðan viðkomandi tengil.  
2. Valin er viðeigandi vátryggingarskírteini og veldu svo **vátryggingasviðsfærslur** aðgerðina.  

## Skoðun á vátryggðu heildarvirði eigna:

Fylkissíða sýnir vátryggingargildin sem eru skráð fyrir hverja vátryggingu fyrir hverja eign sem verður til við bókaðar vátryggingatengdar upphæðir.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Trygging** og velja síðan viðkomandi tengil.  
2. Valin er viðeigandi vátryggingarskírteini og veldu svo **heildarvirði tryggingar á eign** aðgerðina.  
3. Fyllið inn í svæðin eftir þörfum.  
4. Veljið aðgerðina **Sýna fylki**.  
5. Til að skoða undirliggjandi vátryggingasviðsfærslur, velja gildi í fylkinu.  

## Leiðrétting á vátryggingarsviðsfærslum

Ef eign var tengd röngu vátryggingarskilmálunum er hægt að leiðrétta hana með því að búa til tvær endurflokkunarfærslur í vátryggingabókinni.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") í reitnum Leit skal færa inn **Vátryggingabók** og velja síðan viðkomandi tengil.  
2. Stofna eina færslubókarlínu fyrir hverja eign og rétt vátryggingarskírteini þar sem gildið í reitnum **Upphæð** er jákvæð.  
3. Stofna aðra færslubókarlínu fyrir hverja eign og rangt vátryggingarskírteini þar sem gildið í reitnum **Upphæð** er neikvæð.  
4. Valið er **Bóka** aðgerðin.  

Eignin er fjarlægð úr röngu vátryggingarskilmálunum í annarri línu. Eigninni er úthlutað á rétta vátryggingu í fyrstu línu færslubókarinnar.  

## Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]