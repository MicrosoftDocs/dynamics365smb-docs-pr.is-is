---
title: Jafna færslur í viðskiptamannabók til að afstemma greiðslur | Microsoft Docs
description: Lýsir því hvernig skal jafna inngreiðslur eða endurgreiðslur við eina eða fleiri opnar færslur í viðskiptamannabók og afstemma greiðslur viðskiptamanna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c5f0ba926208d831cac4d5e3b54c5a8e83a9d92c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748594"
---
# <a name="reconcile-customer-payments-with-the-cash-receipt-journal-or-from-customer-ledger-entries"></a>Afstemma greiðslur viðskiptavinar með inngreiðslubók eða úr færslum í viðskiptamannabók
Þegar þú færð kvittun kvittunar frá viðskiptavini eða þú ert með endurgreiðslu í reiðufé þarftu að ákveða hvort þú skulir greiða eða endurgreiða til að loka einum eða fleiri opnum skuldfærslum eða kreditfærslum. Hægt er að tilgreina upphæð sem á að nota. Til dæmis er hægt að færa hlutagreiðslur í færslur í viðskiptamannabók. Ef færslum í viðskiptamannabók er lokað er gengið úr skugga um að upplýsingar á við tölfræði viðskiptamanns, reikningsyfirlit og fjárhagsfærslur séu réttar.

> [!TIP]  
>   Á síðunni **Færslur í viðskiptamannabók** merkir rautt letur að tengd greiðsla er komin yfir gjalddaga. Ef gjaldfallnar greiðslur eru að verða vandamál, getum við hjálpað þér að draga úr tíðni þeirra. Þú getur virkjað **Greiðsludráttarspár** viðbótina sem notar spálíkan, sem við byggðum í Azure Machine-vélnámi, til að spá fyrir um tímasetningu greiðslna. Þessar spár hjálpa þér að fækka útistandandi kröfum og fínstilla innheimtustefnu þína. Ef greiðsla telst til dæmis vera sein getur þú breytt greiðsluskilmálum eða greiðslumáta fyrir viðskiptamanninn. Nánari upplýsingar er að finna í [Greiðsludráttarspár](ui-extensions-late-payment-prediction.md).  

Hægt er að jafna færslur í viðskiptamannabók á ýmsa vegu:

* Með því að slá inn upplýsingar á þar til gerðar síður:
    * Síðan **Greiðsluafstemmingarbók**. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * Síðan **Skráning greiðslna**. Frekari upplýsingar eru í [Samræma greiðslur viðskiptamanna úr lista yfir ógreidd söluskjöl](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
    * **Inngreiðslubók**. Þessu er lýst að neðan.
* Með því að fylla út reitinn **Jöfnunarskjalsnúmer** í skjölum sölukreditreiknings. Þessu er lýst að neðan.
* Með því að nota aðgerðina **Stilla jöfnunarkenni** í færslu viðskiptamannabókar. Þessu er lýst að neðan.

> [!NOTE]  
>   Ef reiturinn **Jöfnunaraðferð** á viðskiptamannaspjaldinu er með **Jafna við elstu** þá munu greiðslur sjálfkrafa vera jöfnuð við elstu opnu kreditfærsluna ef ekki er tilgreint handvirkt hvaða færslu eigi að jafna við. Ef jöfnunaraðferðin er **Handvirkt** verður að jafna færslur handvirkt.

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Til að fylla út og bóka inngreiðslubók:
Inngreiðslubók er ein tegund færslubóka og því er hægt að nota hana til að bóka hreyfingar í fjárhags-, banka-, viðskiptamanna-, lánardrottna- og eignabækur. Hægt að jafna greiðsluna við eina eða fleiri debetfærslur þegar greiðsla er bókuð eða nota bókaðar færslur síðar.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Inngreiðslubók** og veldu síðan tengda tengilinn.
2. Velja skal aðgerðina **Breyta færslubók**.
3. Velja skal viðeigandi keyrslu í reitnum **Heiti keyrslu**.
4. Fylla skal út reitinn **Dagsetning bókunar**.  
5. Í reitnum **Tegund fylgiskjals** er valið **Greiðsla**.

    Reiturinn **Númer fylgiskjals** er fylltur út með númeraröðinni sem úthlutað er á keyrsluna.  
6. Nota skal reitinn **Númer utanaðk. skjals** til að geyma kenni, til dæmis tékkanúmer viðskiptamanns.
7. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.
8. Í reitnum **Reikningsnr.**, veldu viðkomandi fjárhagsreikning.
9. Ef bóka á jöfnunina á sama tíma og bóka skal línur í færslubókinni þarf að gera eftirfarandi.
10. Í reitnum **Tegund mótreiknings** er **fjárhagsreikningur** valinn fyrir greiðslu í reiðufé og **bankareikningur** fyrir aðrar greiðslur.
11. Í reitnum **Mótreikningur nr.** er sjóðsreikningur valinn fyrir greiðslu í reiðufé eða viðeigandi bankareikningur fyrir aðrar greiðslur.
12. Bóka skal færslubókina.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Greiðsla jöfnuð við eina viðskiptamannsfærslu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Inngreiðslubók** og veldu síðan tengda tengilinn.
2. Velja skal aðgerðina **Breyta færslubók**.
3. Í fyrstu bókarlínunni eru ritaðar viðeigandi upplýsingar um færsluna sem á að jafna.
4. Í reitnum **Tegund fylgiskjals** er valið **Greiðsla**.
5. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í reitnum **Jafna við skjal nr.** er valinn reiturinn til að opna **Jafna viðskiptamannafærslur** síðuna .
8. Á síðunni **Jafna lánardr.færslur** eru línurnar með færslunum til að jafna greiðsluna við valdar.
9. í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.

    Neðst á síðunni **Jafna færslur viðskiptavina** má sjá upphæðina í reitnum **Jöfnuð upphæð** og einnig hvort jöfnunin stemmir.  
10. Velja hnappinn **Í lagi**. Síðan **inngreiðslubók** sýnir nú færsluna sem færð hefur verið inn valin í reitunum **jöfnunarskjalsgerð** og **jöfnunarskjalsnúmer**.
11. Inngreiðslubókin er bókuð

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Greiðsla jöfnuð við margar viðskiptamannafærslu:
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Inngreiðslubók** og veldu síðan tengda tengilinn.
2. Velja skal aðgerðina **Breyta færslubók**.
3. Í fyrstu bókarlínunni eru ritaðar viðeigandi upplýsingar um færsluna sem á að jafna.
4. Í reitnum **Tegund fylgiskjals** er valið **Greiðsla**.
5. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í reitnum **Upphæð** skal færa inn fulla greiðslu sem neikvæða upphæð.
8. Til að jafna greiðslu við margar viðskiptamannafærslur í bókun er veldu aðgerðina **Jafna færslur**.  
9. Valdar eru línurnar með færslunum sem á að jafna færsluna við og síðan velja síðan **Setja kenni jöfnunar**.  
10. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.

    Neðst á síðunni **Jafna færslur viðskiptavina** má sjá upphæðina í reitnum **Jöfnuð upphæð** og einnig hvort jöfnunin stemmir.  
11. Velja hnappinn **Í lagi**.
12. Inngreiðslubókin er bókuð

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Kreditreikningur jafnaður við eina viðskiptamannsfærslu:
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölukreditreikningar** og veldu síðan tengda tengilinn.
2. Opna skal viðeigandi sölukreditreikning.
3. Til að jafna kreditreikninginn við eina viðskiptamannabókarfærslu þegar bókað er skal fara í reitnum **Jafna við skjal nr.** skal svo velja færsluna sem jafna á greiðsluna við.
4. Á línunni í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna.  

    Ef engin færsla er rituð jafnar forritið sjálfkrafa við hámarksupphæðina. Neðst á síðunni **Jafna færslur viðskiptavina** má sjá upphæðina í reitnum **Jöfnuð upphæð** og einnig hvort jöfnunin stemmir.    
5. Velja hnappinn **Í lagi**. Síðan **sölukreditreikningur** sýnir nú færsluna sem færð hefur verið inn valin í reitunum **jöfnunarskjalsgerð** og **jöfnunarskjalsnúmer**. Og upphæð kreditreikningsins sem á að bóka, leiðrétta fyrir hugsanlegan greiðsluafslátt.
6. Kreditreikningurinn er bókaður.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Kreditreikningur jafnaður við margar viðskiptamannafærslur:
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölukreditreikningar** og veldu síðan tengda tengilinn.
2. Opna skal viðeigandi sölukreditreikning.
3. Til að jafna greiðslu kreditreikning við margar viðskiptamannafærslur í bókun er veldu aðgerðina **Jafna færslur**.
4. Valdar eru línurnar með færslunum sem á að jafna færsluna við og síðan velja síðan **Setja kenni jöfnunar**.
5. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.  

    Neðst á síðunni **Jafna færslur viðskiptavina** má sjá upphæðina í reitnum **Jöfnuð upphæð** og einnig hvort jöfnunin stemmir.  
6. Velja hnappinn **Í lagi**. Síðan **sölukreditreikningur** sýnir núna upphæð kreditreikningsins sem á að bóka, leiðréttan fyrir hugsanlegan greiðsluafslátt.
7. Kreditreikningurinn er bókaður.

## <a name="to-apply-posted-customer-ledger-entries"></a>Bókaðar viðskiptamannafærslur jafnaðar:
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna skal viðskiptamannsspjald fyrir viðskiptamann með færslur sem á að jafna.
3. Veldu **fjárhagsfærslur** aðgerðina, og Velja síðan línuna með viðkomandi færslu sem verður jöfnunarfærslan.
4. Valið er **Jafna Færslur** aðgerð. Síðan **Jafna Viðskm.færslur** opnast og sýnir opnar færslur fyrir viðskiptamanninn.
5. Valdar eru línurnar með færslunum sem á að jafna færsluna við og síðan velja síðan **Setja kenni jöfnunar**. Aðgerð
6. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna. Ef engin færsla er rituð jafnar forritið við hámarksupphæðina.  

    Neðst á síðunni **Jafna færslur viðskiptavina** má sjá upphæðina í reitnum **Jöfnuð upphæð**.  
7. Valið er **bóka jöfnun** aðgerð. Síðan **Bóka jöfnun** birtist með fylgiskjalsnúmeri jöfnunarfærslunnar og nýjustu bókunardagsetningunni.  
8. Velja hnappinn **Í lagi** til að bóka forritið.

    Hafi bókaðar færslur leitt til lokaðra viðskiptamannafærslna þá eru þessar færslur hreinsaðar í reitnum **Opin**.    
9. Til að sjá fjárhagsfærslurnar skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn. Fletta að spjaldi fyrir viðeigandi viðskiptamann til að skoða fjárhagsfærslurnar.  

Á færslulistanum sést að ekkert gátmerki er í reitnum **Opin** í línunni sem inniheldur færsluna sem jafnað var við að fullu.  

> [!NOTE]  
>   Eftir að færslan var valin af síðunni **Jafna viðskm.færslur** eða nokkrar færslur með því að setja **Kenni jöfnunar**, inniheldur reiturinn **Jöfnuð upphæð** í bókarlínunni samantekt eftirstandandi upphæða í bókuðu færslunum sem voru valdar - nema reiturinn sé þegar útfylltur. Ef **Jafna elstu** er valið í reitnum **J** á viðskiptamannaspjaldinu verður greiðslan jöfnuð sjálfkrafa.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Viðskiptamannafærslur jafnaðar hver við aðra í mismunandi gjaldmiðlum:
Ef viðskiptamaður kaupir í einum gjaldmiðli og greiðir í öðrum er enn hægt að jafna reikninginn við greiðsluna.  

Ef færsla (Færsla 1) í einum gjaldmiðli er jöfnuð við færslu (Færsla 2) í öðrum gjaldmiðli notar forritið bókunardagsetninguna í Færslu 1 til að finna viðeigandi gengi til að breyta upphæðunum í Færslu 2. Viðeigandi gengi er að finna á síðunni **Gengi gjaldmiðla**.  

Jafna viðskiptavinarfærslur í mismunandi gjaldmiðlum verður að vera virkt. Frekari upplýsingar eru í [Leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Inngreiðslubók** og veldu síðan tengda tengilinn.
2. Opna færslubókina sem óskað er eftir og fylla inn í fyrstu auðu bókarlínuna með gjaldmiðilskóta.
3. Valið er **Jafna Færslur** aðgerð.
4. Vveldu línuna með færslunni sem á að jafna við færsluna í inngreiðslubók. veldu **Setja kenni jöfnunar** aðgerðina, og síðan valin færslan sem á að nota til að jafna.
5. Velja hnappinn **Í lagi** til að snúa aftur í inngreiðslubók.
6. Bóka skal sölubókina.  

> [!IMPORTANT]  
>   Þegar færslur í mismunandi gjaldmiðlum eru jafnaðar er færslum breytt í USD. Jafnvel þó gengið fyrir þessa tvo gjaldmiðla sé fast, t.d. milli USD og EUR, kann að vera einhver afgangur þegar þessum upphæðum er breytt í USD. Þessar litlu afgangsupphæðir eru bókaðar sem hagnaður eða tap á þann reikning sem er tilgreindur í reitunum **Reikningur orðins hagnaðar** eða **Reikningur orðins taps** á síðunni **Gjaldmiðlar**. Reiturinn **Upphæð (USD)** er einnig stilltur á lánardrottnafærslur.  

## <a name="to-correct-an-application-of-customer-entries"></a>Til að leiðrétta jöfnun á færslum viðskiptamanns
Þegar jöfnun er leiðrétt eru leiðréttingarfærslur sem eru sambærilegar upphaflegu færslunni en með andstæðu formerki í reit upphæðar stofnaðar og bókaðar á öllum færslum með öllum almennum fjárhagsbókunum sem runnar eru frá jöfnuninni, svo sem greiðsluafslætti og gjaldmiðilshagnaði/-tapi. Færslurnar sem forritið lokaði eru enduropnaðar.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Viðeigandi viðskiptamannaspjald er opnað.
3. Valið er **fjárhagsfærslur** aðgerð.
4. Valin er viðeigandi fjárhagsfærsla og veldu svo **Ógilda færslujöfnun** aðgerðina.
5. Einnig er hægt að velja reitinn **Sundurliðuð fjárhagsfærsla** aðgerð.
6. Valin er færslujöfnun og veldu svo **Ógilda færslujöfnun** aðgerðina.
7. Fylla inn í reitina í hausnum og velja svo aðgerðina **Ógilda**.  

> [!IMPORTANT]  
>   Ef færsla hefur verið jöfnuð með fleiri en einni jöfnunarfærslu verður að ógilda þá nýjustu fyrst.  

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
