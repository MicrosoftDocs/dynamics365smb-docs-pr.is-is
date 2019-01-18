---
title: "Unnið með fjárhagstímabil og fjárhagsár | Microsoft Docs"
description: "Lærðu hvernig á að vinna með fjárhagstímabil til að skilgreina hvenær fyrirtækið greinir frá fjárhagslegri frammistöðu."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/13/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6f760f546ea02fbc19473c70eb26d8b4c47c0987
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="working-with-accounting-periods-and-fiscal-years"></a>Unnið með fjárhagstímabil og fjárhagsár
Fjárhagstímabil, sem einnig eru þekkt sem skýrslutímabil, eru tímabil þar sem fyrirtæki eða stofnun greinir frá fjárhagslegri frammistöðu, t.d. með því að búa til rekstrarreikning eða efnahagsreikning. Venjulega tengjast fjárhagstímabil fjárhagsári fyrirtækis, sem geta innihaldið nokkur fjárhagstímabil, svo sem mánuði eða ársfjórðunga.

Í mörgum fyrirtækjum samsvarar reikningsárið ekki almanaksárinu. Til dæmis gæti fjárhagsárið endað 30. júní fremur en 31. desember. Fyrir nýstofnuð fyrirtæki gæti fjárhagstímabilið í raun verið lengra en 12 mánuðir. 

[!INCLUDE[d365fin](includes/d365fin_md.md)] krefst aðeins fjárhagstímabila ef þú vilt eingöngu loka rekstrarreikningi eða keyra gagnaþjöppunarverk. 

Hægt er að nota reikningstímabil í skýrslugerð. Til dæmis, þegar þú skoðar bókaðar færslur á síðunni **Staða/fjárhagsáætlun** þar sem hægt er að tilgreina skýrslutímabilið. Einn af þeim valkostum sem þú getur tilgreint til að greina frá eftir reikningstímabili. Þú getur líka byggt upp fjárhagsskema sem ber saman niðurstöður fyrir mismunandi reikningstímabil.

## <a name="creating-a-new-fiscal-year"></a>Stofna nýtt fjárhagsár
Hægt er að búa til mörg reikningstímabil saman með runuvinnslunni **Búa til fjárhagsár** eða handvirkt.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Hvernig skal búa til mörg fjárhagstímabil saman
Notaðu runuvinnsluna **Búa til fjárhagsár** til að skipta fjárhagsári niður í tímabil af jafnri lengd.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningstímabil** og velja svo viðeigandi tengil.  
2. Veldu aðgerðina **Stofna ár**.  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. Í reitnum **Upphafsdagsetning** skal slá inn dagsetninguna sem fjárhagsárið byrjar á.  
4. Í reitnum **Fjöldi tímabila** skal slá inn fjölda reikningstímabila sem fjárhagsárið á að skiptast niður í. Hægt er að velja allt að 365 tímabil fyrir hvert ár.  
5. Í reitinn **Lengd tímabils** skal slá inn tímalengd fyrir hvert tímabil. Sem dæmi, 1M fyrir einn mánuð, 1V fyrir eina viku og 1Y fyrir eitt ár.  
6. Velja **Í lagi**.  

### <a name="how-to-create-accounting-periods-manually"></a>Hvernig á að stofna reikningstímabil handvirkt
Ef reikningstímabilin á fjárhagsárinu eru mismunandi löng, eins og 4-4-5 dagatalið sem notað er í smásölu, getur þú sett þau upp handvirkt.  
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningstímabil** og velja svo viðeigandi tengil.  
2. Í reitnum **Upphafsdagsetning** skal slá inn dagsetninguna sem fjárhagsárið byrjar á. Reiturinn **Heiti** sýnir heiti mánaðar.  
3. Veldu gátreitinn **Nýtt fjárhagsár** til að gefa til kynna að þetta sé fyrsta tímabilið á árinu. [!INCLUDE[d365fin](includes/d365fin_md.md)] mun nota þetta tímabil til að ákvarða hvaða tímabil skuli loka í árslok.
4. Endurtakið skref 2 og 3 fyrir hin tímabilin sem eru eftir.  

## <a name="closing-a-fiscal-year"></a>Lokun fjárhagsárs
Lokun fjárhagsárs er eitt verkanna fyrir lokun bóka. Eftir að fjárhagsári er lokað, eru gátreitirnir **Lokað** og **Dags. læst** valdir fyrir öll tímabilin á árinu. Þú getur ekki opnað ár aftur eða hreinsað gátreitina.

> [!NOTE]  
>  Þú verður alltaf að hafa að minnsta kosti eitt opið fjárhagsár. Þegar ári er lokað skal tryggja að nýtt ár hafi verið stofnað. Hafðu einnig í huga að eftir að einu ári er lokað er ekki hægt að breyta upphafsdagsetningunni á næsta ári.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningstímabil** og velja svo viðeigandi tengil.  
2. Veldu aðgerðina **Loka ári**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Bókun færslna á lokað fjárhagsár
Enda þótt fjárhagsár sé lokað er enn hægt að bóka fjárhagsfærslur á það. Þegar það er gert eru færslurnar merktar sem bókaðar á lokað fjárhagsár og gátreiturinn **Fært á fyrra ár** er valinn. Sjálfgefið er að þessi gátreitur sé ekki sýndur á síðunni, en þú getur bætt honum við. Næsta skref er að loka rekstrarreikningum og flytja niðurstöður ársins yfir á efnahagsreikning. Endurtaktu þessi skref í hvert skipti sem þú bókar færslur á lokað fjárhagsár.

## <a name="see-also"></a>Sjá einnig
[Bókum lokað](year-close-books.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Hvernig skal: Vinna með fjárhagsskemu](bi-how-work-account-schedule.md)  
  






