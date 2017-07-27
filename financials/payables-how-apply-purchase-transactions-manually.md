---
title: "Afstemma greiðslur lánardrottna handvirkt | Microsoft Docs"
description: "Til að vinna, jafna eða afstemma greiðslur eða endurgreiðslur lánardrottins, skal jafna upphæðina við eina eða fleiri opna lánardrottnafærslur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6f0f3e1c14e21fff736b54b4c5f7423e1e909e72
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reconcile-vendor-payments-manually"></a>Hvernig á að: Afstemma greiðslur á lánardrottna handvirkt 
Þegar lánardrottni er greitt eða hann endurgreiðir verður að ákveða hvort jafna eigi greiðsluna eða endurgreiðsluna við eina eða fleiri opnar færslur. Hægt er að tilgreina nákvæma upphæð sem á að jafna við greiðslumóttökuna eða endurgreiðsluna, og svo aðeins að hluta til jafna við lánardrottnabókarfærslur. Jafna þarf öllum lánardrottnafærslum til að fá réttar lánardrottnaupplýsingar og skýrslur á reikningsyfirlitum og vöxtum.

> [!NOTE]  
>   Lánardrottnar kunna stundum að veita endurgreiðslu frekar en kreditreikning sem mótfærslu gegn komandi reikningum, sérstaklega þegar greiddum vörum er skilað eða þegar of mikið var greitt fyrir reikning.

Hægt er að jafna lánardrottnafærslur á þrjá vegu:

* Með því að færa inn upplýsingar í þar til gerða glugga, eins og  glugga **greiðslubókar**  og glugga **greiðsluafstemmingarbókar** .
* Úr skjölum innkaupakreditreiknings
* Úr lánardrottnafærslur eftir að innkaupaskjöl eru bókuð en ekki jöfnuð.

> [!NOTE]  
>   Ef reiturinn **Jöfnunaraðferð** á lánardrottnaspjaldinu er með **Jafna við elstu** þá munu greiðslur sjálfkrafa vera jöfnuð við elstu opnu kreditfærsluna ef þú tilgreinir ekki handvirkt hvaða færslu eigi að jafna við. Ef jöfnunaraðferðin fyrir viðskiptamann er **Handvirkt** verður að jafna færslur handvirkt.

Hægt er að jafna greiðslur á lánardrottna handvirkt á tengd innkaupaskjöl þeirra tengdar við bókun á greiðslum í á glugga **greiðslubókar**. Upplýsingar um að fylla greiðslubók, sjá [hvernig skal: gera greiðslur](payables-make-payments.md)

Einnig má jafna greiðslur á lánardrottna og greiðslur viðskiptamnns, eftir að greiðslur birtast sem neikvæðar bankafærslur í þínum banka. Í **greiðsluafstemmingarbók** glugganum geturðu notað virkni fyrir innflutning bankayfirlits, sjálfvirk jöfnun, og afstemming bankareiknings. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Greiðsla jöfnuð við eina eða margar lánardrottnabókarfærslur
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubók** og velja svo viðeigandi tengil.
2. Í **greiðslubókargluggi** í fyrstu færslubókarlína eru ritaðar viðeigandi upplýsingar um greiðslufærsluna.
3. Til að jafna eina lánardrottnafærslur :
   1. Í reitnum **jöfnunarskjalsnúmer** er valið í reit til að opna **Jafna lánardr.færslur** gluggann.
   2. Í glugganum **Jafna lánardr.færslur** eru valin færsla til að jafna greiðsluna við.
   3. Á línunni í reitnum  **upphæð til jöfnunar** er upphæðin sem jafna á við færsluna færð inn.
4. Eða, til að jafna margar lánardrottnabókarfærslur

   1. Valið er **Jafna Færslur** aðgerð.
   2. Í glugganum **Jafna lánardr.færslur** er valdar eru línurnar með færslunum til að jafna greiðsluna við.
   3. Valið er **stilla jöfnunarkenni** aðgerð.  
   4. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við einstöku færsluna.

      Ef engin færsla er rituð jafnar forritið sjálfkrafa við hámarksupphæðina. Neðst í glugganum  **jafna lánardrottnafærslur** má sjá upphæðina í reitnum jöfnuð upphæð, og einnig hvort jöfnunin stemmir.
5. Velja hnappinn **Í lagi**.
6. Velja **bóka** aðgerðina til að bóka greiðslubókina.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Kreditreikningur jöfnuð við eina eða margar lánardrottnabókarfærslur
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupakreditreikningur** og velja svo viðeigandi tengil.
2. Opna kreditreikningur sem á að nota.
3. Viðeigandi upplýsingar eru ritaðar í hausinn.
4. Til að framkvæma eina lánardrottnafærslu, á **Jöfnun** flýtiflipanum í **Jafna-skjalnúmer** reitnum, veldu færslan sem jafna á kreditreikning við og síðan í reitnum **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við færsluna.
5. Eða, til að jafna margar lánardrottnabókarfærslur

   1. Valið er **Jafna Færslur** aðgerð.
   2. Valdar eru línurnar með færslunum sem á að jafna kreditreikninginn við.
   3. Valið er **stilla jöfnunarkenni** aðgerð.  
   4. Í hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við einstöku færsluna.

       Ef engin færsla er rituð jafnar forritið sjálfkrafa við hámarksupphæðina. Neðst í glugganum  **jafna lánardrottnafærslur** má sjá upphæðina í reitnum **jöfnuð upphæð**, og einnig hvort jöfnunin stemmir.
6. Velja hnappinn **Í lagi**.  
   Glugginn **innkaupakreditreikningur** sýnir færsluna sem þú hefur valið í **jöfnunarskjalstegund**  reitnum og **jöfnunarskjalsnúmer**. . Glugginn sýnir einnig upphæð kreditreikningsins sem á að bóka, leiðrétta fyrir hugsanlegan greiðsluafslátt.
7. Velja **bóka** hnappur til að bóka innkaupakreditreikningur.

## <a name="to-apply-posted-vendor-ledger-entries"></a>Bókaðar lánardrottnafærslur jafnaðar:
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **lánardrottnar** og velja svo viðeigandi tengil.
2. Viðeigandi lánardrottinn með færslum sem hafa þegar verið bókaðar er opnaður.
3. Valið er **fjárhagsfærslur** aðgerina, og veldu síðan **Jafna Færslur** aðgerð.
4. Í glugganum **jafna lánardrottinsfærslur** má sjá opnar færslur fyrir lánardrottininn.
5. Valin er línan með færslunni sem á að jafna.
6. Valið er **stilla jöfnunarkenni** aðgerð.

    Svæðið **jöfnunarkenni** sýnir þrjár stjörnur ef um er að ræða eins notanda kerfi eða notandakennið ef um er að ræða fjölnotendakerfi.  
7. Fyrir hverri línu í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem jafna á við einstöku færsluna.

    Ef engin færsla er rituð jafnar forritið sjálfkrafa við hámarksupphæðina. Þú getur séð upphæðina í **jöfnuð upphæð** reitnum neðst á glugganum **jafna lánardrottnafærslur**.
8. Valið er **bóka jöfnun** aðgerð.  

    Glugginn **Bóka jöfnun** opnast með fylgiskjalsnúmeri jöfnunarfærslunnar og nýjustu bókunardagsetningunni.
9. Velja hnappinn **Í lagi** til að bóka forritið.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Lánardrottnafærslur jafnaðar hver annarri í mismunandi gjaldmiðlum:
Ef þú kaupir af lánardrottinn í einum gjaldmiðli og greiðir í öðrum er enn hægt að jafna reikninginn við greiðsluna.

Ef færsla (Færsla 1) í einum gjaldmiðli er jöfnuð við færslu (Færsla 2) í öðrum gjaldmiðli notar forritið bókunardagsetninguna í Færslu 1 til að finna viðeigandi gengi til að breyta upphæðunum í Færslu 2. viðeigandi gengi er að finna í glugganum  **Gengi gjaldmiðla**. Ef svo er, verður þú að virkja jöfnun lánardrottnafjárhagsfærslna í mismunandi gjaldmiðlum Fyrir frekar upplýsingar, sjá: [Hvernig á að leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubók** og velja svo viðeigandi tengil.
2. Opna færslubókina sem óskað er eftir og fylla inn í fyrstu auðu bókarlínuna með gjaldmiðilskóta.
3. Valið er **Jafna Færslur** aðgerð.
4. Vveldu línuna með færslunni sem á að jafna við færsluna í útgreiðslubókinni. veldu **Setja kenni jöfnunar** aðgerðina, og síðan valin færslan sem á að nota til að jafna.
5. Velja hnappinn **Í lagi** til að snúa aftur í greiðslubók.
6. Greiðslubókin er bókuð.

> [!IMPORTANT]  
>   Þegar færslur í mismunandi gjaldmiðlum eru jafnaðar hver við aðra, breytir færslurnar í Dollara. Jafnvel þó gengið fyrir hina tvo viðeigandi gjaldmiðla sé fast, t.d. milli USD og EUR, kann að vera einhver afgangur þegar þessum upphæðum í erlendum gjaldmiðlum er breytt í USD. Þessar litlu afgangsupphæðir eru bókaðar sem hagnaður eða tap á þann reikning sem er tilgreindur í reitunum **Reikningur orðins hagnaðar** eða **Reikningur orðins taps** í glugganum **Gjaldmiðlar**. Reiturinn **Upphæð (USD)** er einnig stilltur á viðeigandi lánardrottnafærslur.

## <a name="to-unapply-an-application-of-vendor-entries"></a>Til að afjafna jöfnun á færslum lánardrottins
Þegar röng jöfnun er ógilt eru leiðréttingarfærslur sem eru sambærilegar upphaflegu færslunni en með andstæðu formerki í reit upphæðar stofnaðar og bókaðar á öllum færslum með öllum almennum fjárhagsbókunum sem runnar eru frá jöfnuninni, svo sem greiðsluafslætti og gjaldmiðilshagnaði/-tapi. Færslurnar sem forritið lokaði eru enduropnaðar.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **lánardrottnar** og velja svo viðeigandi tengil.
2. Viðeigandi lánardrottnaspjald er opnað.
3. Valið er **fjárhagsfærslur** aðgerð.
4. Valin er viðeigandi fjárhagsfærsla og veldu svo **Ógilda færslujöfnun** aðgerðina.
5. Einnig er hægt að velja reitinn **Sundurliðuð fjárhagsfærsla** aðgerð.
6. Valin er færslujöfnun og veldu svo **Ógilda færslujöfnun** aðgerðina.
7. Fylla inn í reitina í hausnum og velja svo aðgerðina **Ógilda**.

> [!IMPORTANT]  
>   Ef færsla hefur verið jöfnuð með fleiri en einni jöfnunarfærslu verður að ógilda þá nýjustu fyrst.

## <a name="see-also"></a>Sjá einnig
[Viðskiptaskuldir](payables-manage-payables.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

