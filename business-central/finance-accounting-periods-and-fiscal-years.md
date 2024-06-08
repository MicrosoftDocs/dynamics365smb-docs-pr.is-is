---
title: Unnið með reikningstímabil og reikningsár
description: Lærðu hvernig á að vinna með fjárhagstímabil til að skilgreina hvenær fyrirtækið greinir frá fjárhagslegri frammistöðu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '100,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="work-with-accounting-periods-and-fiscal-years"></a>Vinna við reikningstímabil og reikningsár

Reikningstímabil, sem einnig eru þekkt sem skýrslutímabil, eru tímabil þar sem fyrirtæki eða stofnun greinir frá fjárhagslegri frammistöðu, t.d. með því að búa til rekstrarreikning eða efnahagsreikning. Venjulega tengjast fjárhagstímabil fjárhagsári fyrirtækis, sem geta innihaldið nokkur fjárhagstímabil, svo sem mánuði eða ársfjórðunga.

Fyrir mörg fyrirtæki er reikningsárið ekki í samræmi við almanaksárið, til dæmis þegar reikningsári lýkur 30. júní frekar en 31. desember. Fyrir nýstofnuð fyrirtæki gæti reikningsárið í raun verið lengra en 12 mánuðir.  

[!INCLUDE[prod_short](includes/prod_short.md)] krefst aðeins fjárhagstímabila ef þú vilt loka rekstrarreikningi eða keyra gagnaþjöppunarverk.

Hægt er að nota reikningstímabil í skýrslugerð, til dæmis þegar farið er yfir bókaðar færslur á síðunni **Staða/fjárhagsáætlun** þar sem skýrslugerðartímabilið er tilgreint. Einn af þeim valkostum sem þú getur tilgreint til að greina frá eftir reikningstímabili. Einnig er hægt að búa til fjárhagsskýrslu sem ber niðurstöður saman fyrir mismunandi reikningstímabil.

## <a name="creating-a-new-fiscal-year"></a>Stofna nýtt fjárhagsár

Hægt er að búa til mörg reikningstímabil saman með runuvinnslunni **Búa til reikningsár** eða handvirkt.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Hvernig á að búa til reikningstímabil í magni

Notaðu runuvinnsluna **Búa til fjárhagsár** til að skipta fjárhagsári niður í tímabil af jafnri lengd.  

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Reikningstímabil**, velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Stofna ár**.
3. Í reitnum **Upphafsdagsetning** skal slá inn dagsetninguna sem fjárhagsárið byrjar á.  
4. Í reitnum **Fjöldi tímabila** skal slá inn fjölda reikningstímabila sem fjárhagsárið á að skiptast niður í. Hægt er að velja allt að 365 tímabil fyrir hvert ár.  
5. Í reitinn **Lengd tímabils** skal slá inn tímalengd fyrir hvert tímabil. Auðkenni tímalengdar er m.a. 1M fyrir einn mánuð, 1Q fyrir einn fjórðung og 1Y fyrir eitt ár.  
6. Velja **Í lagi**.  

### <a name="how-to-create-accounting-periods-manually"></a>Hvernig á að stofna reikningstímabil handvirkt

Ef reikningstímabilin á fjárhagsárinu eru mismunandi löng, eins og 4-4-5 dagatalið sem notað er í smásölu, getur þú sett þau upp handvirkt.  
  
1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Reikningstímabil**, velja síðan viðkomandi tengil.  
2. Í reitnum **Upphafsdagsetning** skal slá inn dagsetninguna sem fjárhagsárið byrjar á. Reiturinn **Heiti** sýnir heiti mánaðar.  
3. Veldu gátreitinn **Nýtt fjárhagsár** til að gefa til kynna að þetta sé fyrsta tímabilið á árinu. [!INCLUDE[prod_short](includes/prod_short.md)] mun nota þetta tímabil til að ákvarða hvaða tímabil skuli loka í árslok.
4. Endurtakið skref 2 og 3 fyrir hin tímabilin sem eru eftir.  

## <a name="closing-a-fiscal-year"></a>Lokun fjárhagsárs

Lokun fjárhagsárs er eitt verkanna fyrir lokun bóka. Eftir að fjárhagsári er lokað, eru gátreitirnir **Lokað** og **Dags. læst** valdir fyrir öll tímabilin á árinu. Þú getur ekki opnað ár aftur eða hreinsað gátreitina.

> [!NOTE]  
> Þú verður alltaf að hafa að minnsta kosti eitt opið fjárhagsár. Þegar ári er lokað skal tryggja að nýtt ár hafi verið stofnað. Hafðu einnig í huga að eftir að einu ári er lokað er ekki hægt að breyta upphafsdagsetningunni á næsta ári.

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Fjárhagstímabil** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Loka ári**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Bókun færslna á lokað fjárhagsár

Enda þótt fjárhagsár sé lokað er enn hægt að bóka fjárhagsfærslur á það. Þegar það er gert eru færslurnar merktar sem bókaðar á lokað fjárhagsár og gátreiturinn **Fært á fyrra ár** er valinn. Sjálfgefið er að þessi gátreitur sé ekki sýndur á síðunni, en þú getur bætt honum við. Næsta skref er að loka rekstrarreikningum og flytja niðurstöður ársins yfir á efnahagsreikning. Endurtaktu þessi skref í hvert skipti sem þú bókar færslur á lokað fjárhagsár.

## <a name="see-also"></a>Sjá einnig .

[Bókum lokað](year-close-books.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Hvernig á að vinna með fjárhagsskýrslur](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
