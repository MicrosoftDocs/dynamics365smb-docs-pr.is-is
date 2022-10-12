---
title: Unnið með fjárhagstímabil og fjárhagsár
description: Lærðu hvernig á að vinna með fjárhagstímabil til að skilgreina hvenær fyrirtækið greinir frá fjárhagslegri frammistöðu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 100
ms.date: 08/25/2022
ms.author: bholtorf
ms.openlocfilehash: 93dcf334d65bda2859f8fcd91c976c3d85e6b18f
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605651"
---
# <a name="work-with-accounting-periods-and-fiscal-years"></a>Vinna með bókhaldstímabil og reikningsár

Bókhaldstímabil, einnig þekkt sem Skýrslugerðartímabil, eru tímabil sem fyrirtæki eða stofnun tilkynnir fjárhagslega frammistöðu með því að mynda t.d. rekstrarreikning þeirra eða efnahagsreikning. Venjulega tengjast fjárhagstímabil fjárhagsári fyrirtækis, sem geta innihaldið nokkur fjárhagstímabil, svo sem mánuði eða ársfjórðunga.

Fyrir mörg fyrirtæki fjárhagsárið samræmir ekki almanaksárið, til dæmis þegar reikningsári lýkur 30 Júní heldur en 31. Fyrir nýstofnuð fyrirtæki gæti fjárhagsárið jafnvel í raun verið lengra en 12 mánuðir.  

[!INCLUDE[prod_short](includes/prod_short.md)] Aðeins þarf bókhaldstímabil ef óskað er eftir að loka rekstrarreikningi eða keyra gagnaþjöppunarverk.

Hægt er að nota bókhaldstímabil í skýrslugerð eins og þegar verið er að skoða bókaðar færslur á **síðunni staða/fjárhagsáætlun** þar sem skýrslugerðarbilið er tilgreint. Einn af valkostunum sem þú getur tilgreint er að skrá eftir bókhaldstímabili. Einnig er hægt að byggja á ársskýrslu sem ber saman niðurstöður fyrir mismunandi bókhaldstímabil.

## <a name="creating-a-new-fiscal-year"></a>Stofna nýtt fjárhagsár

Hægt er að stofna bókhaldstímabil í magni með því að **nota keyrsluna Stofna reikningsár** eða gera það handvirkt.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Hvernig á að stofna bókhaldstímabil í bulk

Notaðu runuvinnsluna **Búa til fjárhagsár** til að skipta fjárhagsári niður í tímabil af jafnri lengd.  

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") Táknið, færa inn **reikningstímabil** og velja síðan tengda tengilinn.  
2. Veldu aðgerðina **Stofna ár**.
3. Í reitnum **Upphafsdagsetning** skal slá inn dagsetninguna sem fjárhagsárið byrjar á.  
4. Í reitnum **Fjöldi tímabila** skal slá inn fjölda reikningstímabila sem fjárhagsárið á að skiptast niður í. Hægt er að velja allt að 365 tímabil fyrir hvert ár.  
5. Í reitinn **Lengd tímabils** skal slá inn tímalengd fyrir hvert tímabil. Kenni tímalengdar inniheldur 1M í einn mánuð, 1Q fyrir einn ársfjórðung og 1Y í eitt ár.  
6. Velja **Í lagi**.  

### <a name="how-to-create-accounting-periods-manually"></a>Hvernig á að stofna reikningstímabil handvirkt

Ef reikningstímabil á reikningsári hafa mismunandi tímalengd, eins og 4-4-5 sem notað er í smásölu, er hægt að setja hana upp handvirkt.  
  
1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") Táknið, færa inn **reikningstímabil** og velja síðan tengda tengilinn.  
2. Í reitnum **Upphafsdagsetning** skal slá inn dagsetninguna sem fjárhagsárið byrjar á. Reiturinn **Heiti** sýnir heiti mánaðar.  
3. Veldu gátreitinn **Nýtt fjárhagsár** til að gefa til kynna að þetta sé fyrsta tímabilið á árinu. [!INCLUDE[prod_short](includes/prod_short.md)] mun nota þetta tímabil til að ákvarða hvaða tímabil skuli loka í árslok.
4. Endurtakið skref 2 og 3 fyrir hin tímabilin sem eru eftir.  

## <a name="closing-a-fiscal-year"></a>Reikningsári lokað

Lokun fjárhagsárs er eitt verkanna fyrir lokun bóka. Eftir að fjárhagsári er lokað, eru gátreitirnir **Lokað** og **Dags. læst** valdir fyrir öll tímabilin á árinu. Þú getur ekki opnað ár aftur eða hreinsað gátreitina.

> [!NOTE]  
> Þú verður alltaf að hafa að minnsta kosti eitt opið fjárhagsár. Þegar ári er lokað skal tryggja að nýtt ár hafi verið stofnað. Hafðu einnig í huga að eftir að einu ári er lokað er ekki hægt að breyta upphafsdagsetningunni á næsta ári.

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Fjárhagstímabil** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Loka ári**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Bókun færslna á lokað reikningsár

Enda þótt fjárhagsár sé lokað er enn hægt að bóka fjárhagsfærslur á það. Þegar það er gert eru færslurnar merktar sem bókaðar á lokað fjárhagsár og gátreiturinn **Fært á fyrra ár** er valinn. Sjálfgefið er að þessi gátreitur sé ekki sýndur á síðunni, en þú getur bætt honum við. Næsta skref er að loka rekstrarreikningum og flytja niðurstöður ársins yfir á efnahagsreikning. Endurtaktu þessi skref í hvert skipti sem þú bókar færslur á lokað fjárhagsár.

## <a name="see-also"></a>Sjá einnig .

[Bókum lokað](year-close-books.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Hvernig unnið er með ársskýrslur](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
