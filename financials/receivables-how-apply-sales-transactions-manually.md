---
title: "Hvernig á að: Afstemma greiðslur viðskiptamanns handvirkt| Microsoft Docs"
description: "Hvernig á að: Afstemma greiðslur viðskiptamanns handvirkt"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 929404a3385a7964136226ae1ee1a8775dd7a62a
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-customer-payments-manually"></a>Hvernig á að: Afstemma greiðslur viðskiptamanns handvirkt
Þegar þú færð kvittun kvittunar frá viðskiptavini eða þú ert með endurgreiðslu í reiðufé þarftu að ákveða hvort þú skulir greiða eða endurgreiða til að loka einum eða fleiri opnum skuldfærslum eða kreditfærslum. Hægt er að tilgreina upphæð sem á að nota. Til dæmis er hægt að færa hlutagreiðslur í færslur í viðskiptamannabók. Ef færslum í viðskiptamannabók er lokað er gengið úr skugga um að upplýsingar á við tölfræði viðskiptamanns, reikningsyfirlit og fjárhagsfærslur séu réttar.

**Athugasemd**: Í glugganum **Viðskiptamannafærslur** merkir rautt letur að tengd greiðsla er komin yfir gjalddaga.

Hægt er að jafna færslur í viðskiptamannabók á ýmsa vegu:

* Með því að færa inn upplýsingar í þar til gerða glugga, eins og **inngreiðslubók** og ** greiðsluafstemmingarbók**.
* Kreditreikningur frá sölu skjöl
* Frá færslur í viðskiptamannabók eftir að söluskjöl eru bókaðar en ekki jafnaðar.

**Athugasemd**: Ef reiturinn **Jöfnunaraðferð** á viðskiptamannaspjaldinu er með **Jafna elstu** þá munu greiðslur sjálfkrafa vera jöfnuð við elstu opnu kreditfærsluna ef ekki er tilgreint handvirkt hvaða færslu eigi að jafna við. Ef jöfnunaraðferðin er **Handvirkt** verður að jafna færslur handvirkt.

Þú getur jafnað viðskiptamannagreiðslur handvirkt í glugganum **inngreiðslubók** Inngreiðslubók er ein tegund færslubóka og því er hægt að nota hana til að bóka hreyfingar í fjárhags-, banka-, viðskiptamanna-, lánardrottna- og eignabækur. Hægt að jafna greiðsluna við eina eða fleiri debetfærslur þegar greiðsla er bókuð eða nota bókaðar færslur síðar.

Þú getur einnig jafnað greiðslur viðskiptamanns og lánardrottins, í **greiðsluafstemmingarbók** glugganum með því að nota virkni fyrir innflutning bankayfirlits, sjálfvirk jöfnun, og afstemming bankareiknings. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md) Einnig er hægt að stemma greiðslur viðskiptamanns byggðar á lista yfir ógreidda söluskjöl í gluganum **skráning greiðslna**. Nánari upplýsingar sjá [hvernig skal: stemma af greiðslur viðskiptamanns úr lista yfir ógreidda söluskjöl](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Til að fylla út og bóka inngreiðslubók:
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **inngreiðslubók**, og velja síðan viðeigandi tengil.
2. Velja skal aðgerðina **Breyta færslubók**.
3. Velja skal viðeigandi keyrslu í reitnum **Heiti keyrslu**.
4. Fylla skal út reitinn **Dagsetning bókunar**.  
5. Í reitnum **Tegund fylgiskjals** er valið **Greiðsla**.

    **Númer fylgiskjals** reiturinn er fylltur út með númeraröðinni sem úthlutað er á rununa.  
6. Nota skal reitinn **Númer utanaðk. skjals** til að geyma kenni, til dæmis tékkanúmer viðskiptamanns.
7. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.
8. Í svæðinu **Bankareikningsnúmer**,  reit, veldu viðkomandi fjárhagsreikningsnúmer.
9. Ef bóka á jöfnunina á sama tíma og bóka skal línur í færslubókinni þarf að gera eftirfarandi.
10. Í reitnum **Tegund mótreiknings** er **fjárhagsreikningur** valinn fyrir greiðslu í reiðufé og **bankareikningur** fyrir aðrar greiðslur.
11. Í reitnum **Mótreikning.** er sjóðsreikningur valinn fyrir greiðslu í reiðufé eða viðeigandi bankareikningur fyrir aðrar greiðslur.
12. Bóka skal færslubókina.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Greiðsla jöfnuð við eina viðskiptamannsfærslu
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **inngreiðslubók**, og velja síðan viðeigandi tengil.
2. Velja skal aðgerðina **Breyta færslubók**.
3. Í fyrstu bókarlínunni eru ritaðar viðeigandi upplýsingar um færsluna sem á að jafna.
4. Í reitnum **Tegund fylgiskjals** er valið **Greiðsla**.
5. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í reitnum **jöfnunarskjalsnúmer** er valið í reit til að opna **Jafna viðskm.færslur** gluggann.
8. Í glugganum **Jafna lánardr.færslur** eru línurnar með færslunum til að jafna greiðsluna við valdar.
9. í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.

    Neðst í glugganum **jafna færslur viðskiptavina ** má sjá upphæðina í reitnum **jöfnuð upphæð** og einnig hvort jöfnunin stemmir.  
10. Velja hnappinn **Í lagi**. Glugginn **inngreiðslubók** sýnir nú færsluna sem færð hefur verið inn valin í reitunum **jöfnunarskjalsgerð** og **jöfnunarskjalsnúmer**. Reitir
11. Inngreiðslubókin er bókuð

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Greiðsla jöfnuð við margar viðskiptamannafærslu:
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **inngreiðslubók**, og velja síðan viðeigandi tengil.
2. Velja skal aðgerðina **Breyta færslubók**.
3. Í fyrstu bókarlínunni eru ritaðar viðeigandi upplýsingar um færsluna sem á að jafna.
4. Í reitnum **Tegund fylgiskjals** er valið **Greiðsla**.
5. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í reitnum **Upphæð** skal færa inn fulla greiðslu sem neikvæða upphæð.
8. Til að jafna greiðslu við margar viðskiptamannafærslur í bókun er veldu aðgerðina **Jafna færslur**.
9. Valdar eru línurnar með færslunum sem á að jafna færsluna við og síðan velja síðan **Setja kenni jöfnunar**.
10. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.

    Neðst í glugganum **jafna færslur viðskiptavina ** má sjá upphæðina í reitnum **jöfnuð upphæð** og einnig hvort jöfnunin stemmir.  
11. Velja hnappinn **Í lagi**.
12. Inngreiðslubókin er bókuð

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Kreditreikningur jafnaður við eina viðskiptamannsfærslu:
1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Sölukreditreikningar**, og velja síðan viðeigandi tengil.
2. Opna skal viðeigandi sölukreditreikning.
3. Til að jafna kreditreikninginn við viðskiptamannsfærslu við bókun, í reitnum **jöfnunarskjalsnúmer.** er Valin færslan til að jafna greiðsluna.
4. Á línunni í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna.  

    Ef engin færsla er rituð jafnar forritið sjálfkrafa við hámarksupphæðina. Neðst í glugganum **jafna færslur viðskiptavina ** má sjá upphæðina í reitnum **jöfnuð upphæð** og einnig hvort jöfnunin stemmir.    
5. Velja hnappinn **Í lagi**. Glugginn **Sölukreditreikningur** sýnir nú færsluna sem færð hefur verið inn valin í reitunum **jöfnunarskjalsgerð** og **jöfnunarskjalsnúmer**. Reitir Og upphæð kreditreikningsins sem á að bóka, leiðrétta fyrir hugsanlegan greiðsluafslátt.
6. Kreditreikningurinn er bókaður.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Kreditreikningur jafnaður við margar viðskiptamannafærslur:
1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Sölukreditreikningar**, og velja síðan viðeigandi tengil.
2. Opna skal viðeigandi sölukreditreikning.
3. Til að jafna greiðslu kreditreikning við margar viðskiptamannafærslur í bókun er veldu aðgerðina **Jafna færslur**.
4. Valdar eru línurnar með færslunum sem á að jafna færsluna við og síðan velja síðan **Setja kenni jöfnunar**.
5. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.  

    Neðst í glugganum **jafna færslur viðskiptavina ** má sjá upphæðina í reitnum **jöfnuð upphæð** og einnig hvort jöfnunin stemmir.  
6. Velja hnappinn **Í lagi**. Glugginn  **sölukreditreikningur** sýnir núna upphæð kreditreikningsins sem á að bóka, leiðréttan fyrir hugsanlegan greiðsluafslátt.
7. Kreditreikningurinn er bókaður.

## <a name="to-apply-posted-customer-ledger-entries"></a>Bókaðar viðskiptamannafærslur jafnaðar:
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Viðskiptamenn**, og velja síðan viðeigandi tengil.
2. Opna skal viðskiptamannsspjald fyrir viðskiptamann með færslur sem á að jafna.
3. Veldu **fjárhagsfærslur** aðgerðina, og Velja síðan línuna með viðkomandi færslu sem verður jöfnunarfærslan.
4. Valið er **Jafna Færslur** aðgerð. **Jafna Viðskm.færslur** glugginn opnast og sýnir opnar færslur fyrir viðskiptamanninn.
5. Valdar eru línurnar með færslunum sem á að jafna færsluna við og síðan velja síðan **Setja kenni jöfnunar**. Aðgerð
6. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.  

    Neðst í glugganum **jafna færslur viðskiptavina ** má sjá upphæðina í reitnum **jöfnuð upphæð**.  
7. Valið er **bóka jöfnun** aðgerð. Glugginn **Bóka jöfnun** birtist með fylgiskjalsnúmeri jöfnunarfærslunnar og nýjustu bókunardagsetningunni.  
8. Velja hnappinn **Í lagi** til að bóka forritið.

    Hafi bókaðar færslur leitt til lokaðra viðskiptamannafærslna þá eru þessar færslur hreinsaðar í reitnum **Opin**.    
9. Til að sjá fjárhagsfærslur skal velja efst í hægra horni **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Viðskiptamenn**, og velja síðan viðeigandi tengil. Fletta að spjaldi fyrir viðeigandi viðskiptamann til að skoða fjárhagsfærslurnar.  

Á færslulistanum sést að ekkert gátmerki er í reitnum **Opin **í línunni sem inniheldur færsluna sem jafnað var við að fullu.  

**Athugasemd**: Eftir að færslan var valin úr glugganum **Jafna viðskm.færslur** eða nokkrar færslur með því að setja **Kenni jöfnunar**, inniheldur reiturinn **Jöfnuð upphæð** í bókarlínunni samantekt eftirstandandi upphæða í bókuðu færslunum sem voru valdar - nema reiturinn sé þegar útfylltur. Ef **Jafna elstu** er valið í reitnum **J** á viðskiptamannaspjaldinu verður greiðslan jöfnuð sjálfkrafa.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Viðskiptamannafærslur jafnaðar hver við aðra í mismunandi gjaldmiðlum:
Ef viðskiptamaður kaupir í einum gjaldmiðli og greiðir í öðrum er enn hægt að jafna reikninginn við greiðsluna.  

Ef færsla (Færsla 1) í einum gjaldmiðli er jöfnuð við færslu (Færsla 2) í öðrum gjaldmiðli notar forritið bókunardagsetninguna í Færslu 1 til að finna viðeigandi gengi til að breyta upphæðunum í Færslu 2. viðeigandi gengi er að finna í glugganum  **Gengi gjaldmiðla**.  

Jafna viðskiptavinarfærslur í mismunandi gjaldmiðlum verður að vera virkt. Fyrir frekar upplýsingar, sjá: [Hvernig á að leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum](finance-how-enable-application-ledger-entries-different-currencies.md)  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Inngreiðslubók**, og velja síðan viðeigandi tengil.
2. Opna færslubókina sem óskað er eftir og fylla inn í fyrstu auðu bókarlínuna með gjaldmiðilskóta.
3. Valið er **Jafna Færslur** aðgerð.
4. Vveldu línuna með færslunni sem á að jafna við færsluna í inngreiðslubók. veldu **Setja kenni jöfnunar ** aðgerðina, og síðan valin færslan sem á að nota til að jafna.
5. Velja hnappinn **Í lagi** til að snúa aftur í inngreiðslubók.
6. Bóka skal sölubókina.  

**Mikilvægt**: Þegar færslur í mismunandi gjaldmiðlum eru jafnaðar er færslum breytt í USD. Jafnvel þó gengið fyrir þessa tvo gjaldmiðla sé fast, t.d. milli USD og EUR, kann að vera einhver afgangur þegar þessum upphæðum er breytt í USD. Þessar litlu afgangsupphæðir eru bókaðar sem hagnaður eða tap á þann reikning sem er tilgreindur í reitunum **Reikningur orðins hagnaðar** eða **Reikningur orðins taps** í glugganum **Gjaldmiðlar**. Reiturinn **Upphæð (USD)** er einnig stilltur á lánardrottnafærslur.  

## <a name="to-correct-an-application-of-customer-entries"></a>Til að leiðrétta jöfnun á færslum viðskiptamanns
Þegar jöfnun er leiðrétt eru leiðréttingarfærslur sem eru sambærilegar upphaflegu færslunni en með andstæðu formerki í reit upphæðar stofnaðar og bókaðar á öllum færslum með öllum almennum fjárhagsbókunum sem runnar eru frá jöfnuninni, svo sem greiðsluafslætti og gjaldmiðilshagnaði/-tapi. Færslurnar sem forritið lokaði eru enduropnaðar.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa inn **Viðskiptamenn**, og velja síðan viðeigandi tengil.
2. Viðeigandi viðskiptamannaspjald er opnað.
3. Valið er **fjárhagsfærslur** aðgerð.
4. Valin er viðeigandi fjárhagsfærsla og veldu svo **Ógilda færslujöfnun** aðgerðina.
5. Einnig er hægt að velja reitinn **Sundurliðuð fjárhagsfærsla** aðgerð.
6. Valin er færslujöfnun og veldu svo **Ógilda færslujöfnun** aðgerðina.
7. Fylla inn í reitina í hausnum og velja svo aðgerðina **Ógilda**.  

**Mikilvægt**: Ef færsla hefur verið jöfnuð með fleiri en einni jöfnunarfærslu verður að ógilda þá nýjustu fyrst.  

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

