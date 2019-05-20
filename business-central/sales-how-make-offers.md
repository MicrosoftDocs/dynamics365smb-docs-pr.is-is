---
title: Stofna sölutilboð fyrir viðskiptamann | Microsoft Docs
description: Lýsir því hvernig skal stofna sölutilboð eða beiðni um tilboð (RFQ) fylgiskjal, til að skrá tilboð til viðskiptamanns um að selja tilteknar vörur með tilteknum skilmálum.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6083e5ff57ebfb57a31d294e5c565b5bc6a3f8c6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252689"
---
# <a name="make-sales-quotes"></a>Gera sölutilboð
Búið er til sölutilboð til að skrá tilboðið við viðskiptamann um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum. Hægt er að senda sölutilboð til viðskiptamannsins til að miðla tilboðinu. Hægt er að senda skjalið í tölvupósti sem PDF viðhengi. Hægt er að láta meginmálslínur tölvupósts vera útfyllt fyrirfram með tilboði. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Þegar samið er við viðskiptamanninn, er hægt að breyta og endursenda sölutilboðið eins mikið og oft og þörf er á. Þegar viðskiptamaður tekur tilboði, er sölutilboðinu breytt í sölureikning eða sölupöntun þar sem salan er meðhöndluð. Nánari upplýsingar eru í [Reikningsfæra sölu](sales-how-invoice-sales.md) eða [Selja vörur.](sales-how-sell-products.md)

Hægt er að fylla út viðskiptamannsreitina á sölutilboðinu með tveimur leiðum, eftir því hvort viðskiptamaðurinn hefur þegar verið skráður. Sjá lið 2 og 3 í eftirfarandi ferli.

## <a name="to-create-a-sales-quote"></a>Sölutilboð búin til:
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölutilboð** og veldu síðan tengda tengilinn.
2. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

   Aðrir reitir á síðunni **Sölutilboð** innihalda stöðluðum upplýsingum um valinn viðskiptamann. Ef viðskiptamaðurinn er ekki skráður, fylgið eftirfarandi skrefum:
3. Í reitnum **Viðskiptamaður** er fært inn nafn nýs viðskiptamanns.
4. Í svarglugganum um að skrá nýja viðskiptavininn, veljið hnappinn **Já**.
5. Á síðunni **Velja sniðmát fyrir nýjan viðskiptamann**, skal velja sniðmát til að byggja nýja viðskiptamannaspjaldið á og veljið hnappinn **Í lagi**.
6. Nýtt viðskiptamannaspjald sýnir upplýsingarnar á valda viðskiptamannasniðmátinu. Eftirstandandi reitir eru fylltir út. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  
7. Þegar lokið hefur verið við viðskiptamannaspjaldið skal velja hnappinn **Í lagi** til að fara aftur á síðuna **sölutilboð**.

   Margir reitir í sölutilboði eru nú fullir af upplýsingar sem tilgreindar voru á nýja viðskiptamannaspjaldi.  
8. Fylltu í eftirstandandi reikningana á síðunni **sölutilboð** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Nú er hægt að fylla út í sölupöntunarlínur fyrir vörur sem selt er viðskiptamanni eða fyrir einhverri færslu við þann viðskiptamann sem á að skrá í reikning í Fjárhag.   

    Ef endurteknar sölulínur hafa verið settar upp fyrir viðskiptamanninn, svo sem mánaðarlegar endurnýjunarpantanir, er hægt að færa línuna inn í pöntunina með því að velja aðgerðina **Endurteknar sölulínur**.  

9. Á **Línur** Flýtiflipanum í **Tegund** reitnum, veldu hvaða tegund framleiðsluflokks, kostnaðarauka eða færslu þú munt bókað fyrir viðskiptamanninn með sölulínunni.
10. Í reitnum **númer** Reitnum er valin færsla til að bóka samkvæmt gildinu í reitnum **Tegund** reit.

    Þú skilur **nr.** reitur tómur í eftirfarandi tilfellum:
    - Ef línan er ætluð athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    - Ef línan er fyrir vörulistavöru. Velja **Velja vörulistaatriði** aðgerð. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).

11. Í reitnum **Magn** er fært inn hversu margar einingar vöru, kostnaðarauka eða færslu sem línan skráir fyrir viðskiptamanninn.

    > [!NOTE]  
    >   Ef varan er af tegundinni **Vara - Þjónusta** eða **Forði**, er magnið tímaeining, t.d. klukkutímar, eins og gefið er til kynna í reitnum **Mælieiningarkóði** í línunni.  

    Gildið í reitnum **Línuupphæð** er reiknaður sem *Einingarverð* x *Magn*.  

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.  
12. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.  

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða vöruspjaldinu, uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Endurtakið skref 9 til 12 fyrir hverja vöru sem bjóða á viðskiptamanninum.

    Samtölur fyrir neðan línurnar eru sjálfkrafa reiknaðar þegar þú stofna eða breyta línur.  
14. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti**.

    Ef reikningsafslættir hafa verið settir upp fyrir viðskiptamanninn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur %** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð án skatts**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Til að fá **Tilboð í gildi fram að dagsetningu** fyllt út sjálfvirkt með ákveðnum dagafjölda eftir stofnun tilboðs er hægt að fylla út reitinn **Útreikningur á gildistíma tilboðs** á síðunni **Sala & útistandandi**. 

15. Þegar sölutilboðslínunum er lokið, skal velja **Senda í tölvupósti** aðgerðina.
16. Á síðunni **Senda tölvupóst** skal fylla út eftirstandandi reiti og fara yfir innfelld sölutilboð. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).
17. Ef viðskiptamaðurinn samþykkir tilboðið, velja **Búa til Reikning** eða **búa til pöntun** aðgerð.

Sölutilboðið er fjarlægt úr gagnagrunninum. Sölureikningur eða sölupöntun er stofnaður byggður á upplýsingum í sölutilboðinu þar sem hægt er að vinna söluna. Í reitnum **Tilboð nr.** á sölureikningnum eða sölupöntun er hægt að sjá fjölda sölutilboða sem hann var búinn til úr. Nánari upplýsingar eru í [Reikningsfæra sölu](sales-how-invoice-sales.md) eða [Selja vörur.](sales-how-sell-products.md)

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
