---
title: "Setja upp vörpun texta á reikning fyrir endurteknar greiðslur | Microsoft Docs"
description: "Tengja texta á greiðslum við sérstaka reikninga, til að greiðslur séu bókaðar á reikningana þegar greiðsluafstemmingarbók er bókuð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: deb05c6294edeb892606154b38de2aa406abf6a2
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Hvernig á að varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu
Í glugganum **vörpun texta á reikning**, sem opnaður er úr glugganum **Greiðsluafstemmingarbók**, er hægt að setja upp vörpun á milli texta í greiðslum og tiltekinni debet-, kredit- og mótreikninga til að greiðslurnar séu bókaðar í tiltekna reikninga þegar greiðsluafstemmingarbók er bókuð.

> [!NOTE]  
>   Efnisatriði á líka við um það þegar þú notar **Vörpun texta á reikning** aðgerðina frá skráningu skjals á innleið til að aðstoða við umbreytingu rafrænna skjala sem fengin eru frá ytri þjónustu yfir í skjöl í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md)   

Svipað aðgerð er til til að stemma af umframupphæðir á greiðsluafstemmingarbókarlínum á sérstækum grundvelli. Frekari upplýsingar eru í [hvernig á að afstemma greiðslur sem ekki er hægt að afstemma sjálfkrafa](receivables-how-reconcile-payments-cannot-apply-auto.md).

Greiðslur sem bókaðar eru samkvæmt vörpun texta á reikning eru ekki jafnaðar við opnar færslur en eru þess í stað eingöngu bókaðar í tilgreinda reikninga, auk þess að mynda fjárhagsfærslur á bankareikningi. Vörpun texta á reikning passar fyrir ítrekaðar inngreiðslur eða gjöld, t.d. ítrekuð kaup eldsneytis eða bankagjöld og vextir, sem gerist reglulega á bankayfirliti og sem ekki þarf tengt viðskiptaskjal. Frekari upplýsingar eru í hlutanum “Dæmi – Vörpun texta á reikning fyrir eldsneytiskostnaði” í þessu efnisatriði.

> [!NOTE]  
>   Greiðslur á afstemmingarbókarlínu eru aðeins stilltar á bókun samkvæmt vörpun texta í reikning ef sjálfvirk jöfnun getur aðeins boðið upp á áreiðanleika samsvörunar sem er **Lítill** eða **Miðlungs**. Ef sjálfvirk jöfnunaraðgerð býður upp á mikinn áreiðanleika samsvörunar er greiðslan sjálfkrafa jöfnuð við eina eða fleiri opnar færslur og greiðslan er ekki bókuð á reikningana sem tilgreindir eru í glugganum **vörpun texta á reikning**. Með öðrum orðum mun **Hár** áreiðanleiki samsvörunar vera með hærri forgang en vörpun texta á reikning.

Á færslubókarlínu greiðsluafstemmingar þar sem greiðslan hefur verið stillt á bókun í samræmi við vörpun texta í reikning inniheldur reiturinn **áreiðanleiki samsvörunar** **Mikið – vörpun texta á reikning** og reitirnir **Tegund reiknings** og **reikningsnúmer** reiturinn inniheldur varpaða reikninga 

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Til að varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðsluafstemmingarbækur** og velja svo viðeigandi tengil.
2. Opna skal greiðsluafstemmingarbók. Frekari upplýsingar eru í [hvernig á að afstemma greiðslur með því að nota sjálfvirka jöfnun](receivables-how-reconcile-payments-auto-application.md)
3. Valið er **Varpa Texta á Reikning** aðgerð. Glugginn **vörpun texta á reikning** opnast.
4. Í reitinn **vörpun texta** skal færa inn þann texta sem er á greiðslum sem á að bóka í tiltekna reikninga án jöfnunar við opnar færslur. Hægt er að færa inn allt að 50 stafi.

    > [!NOTE]  
>   Ef engar aðrar greiðslur eða skjöl á innleið eru til staðar innan vörpunartextans sem um ræðir, þá kemur upp vörpun texta á reikning jafnvel þó aðeins hluti textans á greiðsluskjalinu eða skjali á innleið er til staðar sem vörpunartexti.
5. Í **Númer lánardrottins** reitinn skal færa inn númer lánardrottins sem skjöl á innleið með vörpunartextanum verða stofnuð fyrir, eða greiðslur verða bókaðar á. Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md)      
6. Í reitinn **Debetreikningsnúmer** skal færa inn reikninginn sem greiðslur með vörpunartextann verða bókaðar í ef þær eru greiðslur á innleið. Fyrir greiðslur á innleið, er táknið í reitnum **Upphæð Yfirlits** jákvæð.
7. Í reitinn **Kreditreikningsnúmer** skal færa inn reikninginn sem greiðslur með vörpunartextann verða bókaðar í ef þær eru greiðslur á innleið. Fyrir greiðslur á útleið, er táknið í reitnum **Upphæð Yfirlits** er neikvætt.
8. Í reitinn **Upprunagerð stöðu** skal tilgreinga hvort greiðslan verður bókuð á fjárhagsreikning eða á viðskiptamann eða lánardrottinn.
9. Í **Upprunanúmer stöðu** skal tilgreina reikninginn sem greiðslan verður bókuð á, allt eftir valinu í reitnum **Upprunagerð stöðu**.
10. Endurtakið skref 4 til 8 fyrir allan texta í greiðslum sem á að varpa á reikninga fyrir beina bókun án jöfnunar.

Næst þegar flutt er inn bankayfirlitsskrá eða aðgerðin **Sjálfvirk jöfnun** er valin í glugganum **greiðsluafstemmingarbók** munu bókarlínur fyrir greiðslur sem innihalda tilgreindan vörpunartexta innihalda varpaða reikninga í reitunum **Tegund reiknings** og **reikningsnúmer** reitina. **áreiðanleiki samsvörunar** reiturinn mun innihalda **Mikill - vörpun texta á reikning**. Þetta er háð því skilyrði að sjálfvirk jöfnun getur aðeins boðið upp á áreiðanleika samsvörunar sem er **Lítill** eða **Miðlungs**.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Dæmi – Vörpun texta á reikning fyrir eldsneytiskostnaði
Til að bóka alltaf eldsneytiskostnað sem stofnað er til á Shell-bensínstöðvum í fjárhagsreikning fyrir bensín (reikningur 8510) skal fylla út línu í glugganum **vörpun texta á reikning** eins og hér segir.

| Varpar texta | Debetreikningsnúmer | Kreditreikningsnúmer | Upprunagerð stöðu | Upprunanúmer stöðu |
| --- | --- | --- | --- | --- |
| Skel |AUTT |8510 |Fjárhagsreikningur |AUTT |

> [!TIP]  
>   Frekari upplýsingar um hvernig skal vinna með reiti og dálka, sjá [Vinna með [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md). Nánari upplýsingar um hvernig finna má tilteknar síður eru í [Leita](ui-search.md).

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Hvernig á að: Setja upp Envestnet Yodlee bankastreymisþjónustu](bank-how-setup-bank-statement-service.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

