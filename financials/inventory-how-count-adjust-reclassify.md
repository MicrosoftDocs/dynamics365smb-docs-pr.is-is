---
title: "Talning, breytingar og endurflokkun birgða| Microsoft Docs"
description: "Lýsir því hvernig skal framkvæma rauntalningu, gera neikvæðar eða jákvæðar leiðréttingar, og hvernig skal breyta upplýsingum, eins og t.d. staðsetningu eða lotunúmer, á birgðahöfuðbókafærslum eða vöruhúsafærslum. "
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Hvernig skal: Telja, breyta og endurflokka birgðir.
Minnst einu sinni á hverju fjárhagsári þarf að telja raunbirgðir (það er, telja allar vörur á lager) til að athuga hvort magnið sem skráð er í kerfinu sé það sama og raunbirgðir á lager. Þegar búið er að finna út úr raunbirgðum þarf að bóka þær í fjárhag þegar fram fer mat á birgðum við lok tímabils.

Þó að allar vörur í birgðum séu taldar minnst einu sinni á ári gæti þurft að telja sumar vörur oftar, kannski vegna þess hve verðmætar þær eru eða vegna þess að mikil hreyfing er á þeim og þær eru stór hluti af rekstrinum. Í þessum tilgangi geturðu úthlutað sérstökum talningatímabilum á þessar vörur. Sjá frekari upplýsingar í „Að framkvæma reglulega talningu" liðnum.

Ef nauðsynlegt er að leiðrétta skráð birgðamagn í tengslum við talningu eða í öðrum tilgangi er hægt að nota birgðabók til þess að breyta færslum í birgðum beint án þess að bóka viðskipti. Að öðrum kosti er hægt að leiðrétta einstaka vöru á birgðaspjaldinu.

Ef nauðsynlegt er að breyta eigindum fyrir birgðafærslur auk magns er hægt að nota endurflokkunarbók vöru. Dæmigerðar eigindir til að endurflokka eru til dæmis rað/lotu númer, gildistími og víddir.

## <a name="to-perform-a-physical-inventory"></a>Að framkvæma Raunbirgðatalningu
Gera verður úttekt á raunbirgðum, það er að telja hvað mikið er til í raun og veru af hverri vöru, til að sjá hvort magnið sem er skráð í kerfinu er í samræmi við vörutalningu í lok hvers reikningsárs, eða oftar. Ef munur er á þessu tvennu verður að bóka hann á birgðareikninginn áður en birgðir eru verðmetnar.

Að frátöldum efnislegu talningarverki felur heildarferlið í sér eftirfarandi þrjú verkefni:

- Reikna væntanlegar birgðir.
- Prenta skýrsluna sem verður notuð við talningu.
- Færa inn og bóka raunveruleg taldar birgðir.

### <a name="to-calculate-the-expected-inventory"></a>Til að reikna væntanlegar birgðir
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Raunbirgðabók** og velja svo viðeigandi tengil.
2. Veljið aðgerðina **Reikna Birgðir**.
3. Í glugganum **Reikna birgðir** tilgreinið skilyrði sem nota á til að stofna færslubókarlínur, t.d. hvort þær eigi að innihalda vörur sem hafa engar birgðir skráðar.
4. Stilla afmarkanir ef aðeins á að reikna birgðir fyrir ákveðnar vörur, hólf, birgðageymslur eða víddir.
5. Velja hnappinn **Í lagi**.

> [!NOTE]  
>   Birgðafærslurnar eru unnar í samræmi við þær upplýsingar sem tilgreindar voru, og línur eru stofnaðar í raunbirgðabókinni. Takið eftir að reiturinn **Magn (raunbirgðir)** færir sjálfkrafa inn sama magn og reiturinn **Magn (reiknað)**. Með þessum eiginleika er ekki nauðsynlegt að færa inn taldar lagerbirgðir fyrir vörur sem er hafa sama magn og reiknað magn. Ef talið magn er annað en það sem skráð er í reitnum **Magn (reiknað)** þarf að skrifa yfir það með magninu sem talið var.

### <a name="to-print-the-report-used-when-counting"></a>Til að prenta skýrsluna sem er notuð við talningu
1. Í glugganum **Raunbirgðabók** sem inniheldur útreikning áætlaðra birgða skal velja **Prenta** aðgerðina.
2. Í glugganum **Raunbirgðalisti** tilgreinið hvort skýrslan skuli sýna reiknað magn og hvort skýrslan eigi að birta birgðavörur eftir rað-/lotunúmerum.
3. Setjið upp afmarkanir ef aðeins á að prenta skýrsluna fyrir ákveðnar vörur, hólf, birgðageymslur eða víddir.
4. Velja hnappinn **Prenta**.

Starfsmenn geta nú haldið áfram að telja birgðir og skrá hugsanlegt misræmi þegar skýrslan er prentuð.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Til að færa inn og bóka raunverulegar taldar birgðir.
1. Í hverri línu í **Raunbirgðabók** glugganum, þar sem tiltækt raunbirgðamagn, samkvæmt rauntalningu, er annað en reiknað magn, er fært inn raunbirgðamagn í reitinn **Magn raunbirgðir**.

    Viðeigandi reitir eru uppfærðir í samræmi við það.

    > [!NOTE]  
>   Ef við raunbirgðatalningu kemur í ljós munur vegna vara hafi verið bókaðar með röngum birgðageymslukótum er munurinn ekki færður inn í raunbirgðabókina. Í staðinn skal nota endurflokkunarbók eða millifærslupöntun til að beina vörunum á rétta staði. Frekari upplýsingar, sjá Vöruendurflokkunarbók Eða hvernig á að stofna Millifærslupantanir

2. Til að leiðrétta reiknað magn í raunverulegt talið magn skal velja aðgerðina **Bóka**.

    Bæði birgðafærslur og raunbirgðabókarfærslur eru stofnaðar. Opna birgðaspjaldið til að skoða raunbirgðafærslur sem leiða af því.

3. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.
4. Til að staðfesta birgðatalningu skal opna það birgðaspjald sem um ræðir, og veljið síðan aðgerðina **Raunbirgðafjárhagsfærslur**.

# <a name="to-perform-cycle-counting"></a>Að framkvæma reglulega talningu
Þó að allar vörur í birgðum séu taldar minnst einu sinni á ári gæti þurft að telja sumar vörur oftar, kannski vegna þess hve verðmætar þær eru eða vegna þess að mikil hreyfing er á þeim og þær eru stór hluti af rekstrinum. Í þessum tilgangi geturðu úthlutað sérstökum talningatímabilum á þessar vörur.

> [!NOTE]  
>   Ef birgðageymslan notar beinan frágang og tínslu þarf fyrst að nota gluggann **Vöruh.- Raunbirgðabók** og síðan aðgerðina **Reikna vöruhúsaleiðréttingu** í glugganum **Birgðabók**.

## <a name="to-set-up-counting-periods"></a>Talningatímabil sett upp
Raunbirgðir eru vanalega taldar með jöfnu millibili, til dæmis mánaðarlega, ársfjórðungslega eða árlega. Hægt er að setja upp þau talningatímabil sem þarf.

Birgðatalningatímabilin sem á að nota eru sett upp og síðan er einu slíku úthlutað á hverja vöru. Þegar raunbirgðir eru taldar og aðgerðin **Reikna talningatímabil** er notuð í raunbirgðabók eru línur fyrir vörurnar búnar til sjálfkrafa.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Talningartímabil raunbirgða** og velja svo viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Talningatímabili úthlutað á vöru  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.  
2. Varan sem úthluta á talningartímabili er valin.  
3. Á reitnum **Kóti talningartímabils raunbirgða** skal velja viðkomandi talningartímabil.  
4. Velja **Já** til að breyta kótanum og reikna út fyrsta talningartímabilið fyrir vöruna. Næst þegar valið er að reikna út talningatímabil í raunbirgðabók vöruhúss, birtist varan sem lína í glugganum **Vöruval raunbirgða**. Nú er hægt að byrja telja vöruna með reglulegu millibili.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Að hefja talningu byggða á talningartímabilum
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Raunbirgðabók** og velja svo viðeigandi tengil.
2. Veljið **Reikna talningartímabil** aðgerðina.

    Glugginn **Vöruval raunbirgða** opnast þar sem vörurnar sem talningatímabil hafa verið sett upp fyrir sem þarf að telja eru samkvæmt talningartímabilum þeirra.
3. Framkvæma raunbirgðatalningu. Frekari upplýsingar, sjá „Framkvæma raunbirgðatalningu“ hlutann.

## <a name="to-adjust-the-inventory-of-one-item"></a>Leiðrétta birgðastöðu einnar vöru
Eftir að búið er að telja vöru á birgðasvæði er hægt að nota eiginleikann **Leiðrétta birgðir** til að skrá raunverulegt magn í birgðum.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.
2. Veljið þá vöru sem leiðrétta birgðir fyrir og veldu svo **leiðrétta birgðir** aðgerðina.
3. Í reitnum **nýjar birgðir** skaltu slá inn birgðamagn sem þú vilt skrá fyrir vöruna.
4. Velja hnappinn **Í lagi**.

Birgðir vörunnar hafa nú verið leiðréttar. Nýja magni er birt í reitnum **Núverandi birgðir** í glugganum **leiðrétta birgðir** og í reitnum **birgðir** í glugganum **vöruspjald**.

Einnig er hægt að nota aðgerðina **Leiðrétta birgðir** sem einfalda leið til að staðsetja keypta vöru í birgðum ef þú ætlar ekki að nota gluggann innkaupareikningur til að skrá innkaupin. Nánari upplýsingar eru í [Hvernig á að: Skrá innkaup](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Eftir að þú hefur leiðrétt birgðir þarftu að uppfæra þær með núverandi útreiknuðu virði. Frekari upplýsingar eru í [Hvernig á að: Endurmeta birgðir](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Leiðrétta birgðamagn einnar eða fleiri vöru
Í glugganum **Birgðabók** er hægt að bóka birgðafærslu beint til að leiðrétta birgðaskrá í tengslum við innkaup, sölu og jákvæða eða neikvæða leiðréttingu án þess að nota fylgiskjöl.

Ef birgðabókin er oft notuð til að bóka sömu eða svipaðar færslubókarlínur, til dæmis í tengslum við efnisnotkun, er hægt að nota **Stöðluðu birgðabókina** til að auðvelda þessa endurteknu vinnu. Frekari upplýsingar, sjá hlutann „Staðlaðar færslubækur“ [Unnið með almennar færslubækur](ui-work-general-journals.md).

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðafærslubækur** og velja svo viðeigandi tengil.
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Veljið aðgerðina **bóka** til að gera birgðaleiðréttingarnar.

> [!NOTE]  
>   Eftir að þú hefur leiðrétt birgðir þarftu að uppfæra þær með núverandi útreiknuðu virði. Frekari upplýsingar eru í [Hvernig á að: Endurmeta birgðir](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Að endurflokka lotunúmer vöru
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðaendurflokkunarbækur** og velja svo viðeigandi tengil.
2. Í glugganum **Birgðaendurflokkunarbók** skal fylla út reitina eins og þörf krefur.
3. Að í **Lotunúmer** reitinn, færið inn núverandi lotunúmer vörunnar.
4. Í reitinn **nýtt lotunr.** færið inn nýja lotunúmer vörunnar.
5. Valið er **bóka** aðgerð.

## <a name="see-also"></a>Sjá einnig
[Birgðir](inventory-manage-inventory.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

