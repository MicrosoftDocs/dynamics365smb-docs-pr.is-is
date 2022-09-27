---
title: Uppsetning texta-Lyklavörpun fyrir endurteknar greiðslur
description: Tengja texta á greiðslum við sérstaka reikninga, til að greiðslur séu bókaðar á reikningana þegar greiðsluafstemmingarbók er bókuð.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.search.form: 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4acc962c596bf2ba8eb857d488eb4fc0045f79cc
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529191"
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu

Á síðunni **vörpun texta á reikning**, sem opnuð er af síðunni **Greiðsluafstemmingarbók**, er hægt að setja upp vörpun á milli texta í greiðslum og tiltekinni debet-, kredit- og mótreikninga til að greiðslurnar séu bókaðar í tiltekna reikninga þegar greiðsluafstemmingarbók er bókuð.

Svipað aðgerð er til til að stemma af umframupphæðir á greiðsluafstemmingarbókarlínum á sérstækum grundvelli. Frekari upplýsingar eru í [Afstemma greiðslur sem ekki er hægt að afstemma sjálfkrafa](receivables-how-reconcile-payments-cannot-apply-auto.md).

Greiðslur sem bókaðar eru samkvæmt vörpun texta á reikning eru ekki jafnaðar við opnar færslur en eru þess í stað eingöngu bókaðar í tilgreinda reikninga, auk þess að mynda fjárhagsfærslur á bankareikningi. Vörpun texta á reikning passar fyrir ítrekaðar inngreiðslur eða gjöld, t.d. ítrekuð kaup eldsneytis eða bankagjöld og vextir, sem gerist reglulega á bankayfirliti og sem ekki þarf tengt viðskiptaskjal. Frekari upplýsingar eru í hlutanum “Dæmi – Vörpun texta á reikning fyrir eldsneytiskostnaði” í þessu efnisatriði.

> [!NOTE]  
>   Greiðslur á afstemmingarbókarlínu eru aðeins stilltar á bókun samkvæmt vörpun texta í reikning ef sjálfvirk jöfnun getur aðeins boðið upp á áreiðanleika samsvörunar sem er **Lítill** eða **Miðlungs**. Ef sjálfvirk jöfnunaraðgerð býður upp á mikinn áreiðanleika samsvörunar er greiðslan sjálfkrafa jöfnuð við eina eða fleiri opnar færslur og greiðslan er ekki bókuð á reikningana sem tilgreindir eru á síðunni **vörpun texta á reikning**. Með öðrum orðum mun **Hár** áreiðanleiki samsvörunar vera með hærri forgang en vörpun texta á reikning.

Á færslubókarlínu greiðsluafstemmingar þar sem greiðslan hefur verið stillt á bókun í samræmi við vörpun texta í reikning inniheldur reiturinn **áreiðanleiki samsvörunar** **Mikið – vörpun texta á reikning** og reitirnir **Tegund reiknings** og **reikningsnúmer** reiturinn inniheldur varpaða reikninga.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Til að varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluafstemmingarbækur** og velja síðan viðkomandi tengil.
2. Opna skal greiðsluafstemmingarbók. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)
3. Valið er **Varpa Texta á Reikning** aðgerð. Síðan **vörpun texta á reikning** opnast.
4. Í reitinn **vörpun texta** skal færa inn þann texta sem er á greiðslum sem á að bóka í tiltekna reikninga án jöfnunar við opnar færslur. Hægt er að færa inn allt að 50 stafi.

    > [!NOTE]  
    >   Ef engar aðrar greiðslur eru til staðar innan vörpunartextans sem um ræðir, þá kemur upp vörpun texta á reikning jafnvel þó aðeins hluti textans á greiðsluskjalinu er til staðar sem vörpunartexti.
5. Í **Númer lánardrottins** reitinn skal færa inn lánardrottinn sem greiðslur verða bókaðar á.
6. Í reitinn **Upprunagerð stöðu** skal tilgreinga hvort greiðslan verður bókuð á fjárhagsreikning eða á viðskiptamann eða lánardrottinn.
7. Í **Upprunanúmer stöðu** skal tilgreina reikninginn sem greiðslan verður bókuð á, allt eftir valinu í reitnum **Upprunagerð stöðu**.

    > [!NOTE]
    > Ekki skal nota **Debetreikningsnúmer** og **Kreditreikningsnúmer** reitina í tengslum við afstemmingu greiðslna. Þeir eru aðeins notaðir fyrir skjöl á innleið. Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md).

8. Endurtakið skref 3 til 7 fyrir allan texta í greiðslum sem á að varpa á reikninga fyrir beina bókun án jöfnunar.

Næst þegar flutt er inn bankayfirlitsskrá eða aðgerðin **Sjálfvirk jöfnun** er valin á síðunni **greiðsluafstemmingarbók** munu bókarlínur fyrir greiðslur sem innihalda tilgreindan vörpunartexta innihalda varpaða reikninga í reitunum **Tegund reiknings** og **reikningsnúmer** reitina. **áreiðanleiki samsvörunar** reiturinn mun innihalda **Mikill - vörpun texta á reikning**. Þetta er háð því skilyrði að sjálfvirk jöfnun getur aðeins boðið upp á áreiðanleika samsvörunar sem er **Lítill** eða **Miðlungs**.

## <a name="example-text-to-account-mapping-for-bank-fees"></a>Dæmi: Vörpun texta á reikning fyrir bankagjöld

Til að bóka alltaf útgjöld sem tengjast gjöldum tiltekins banka, MyBank, til fjárhagslykilsins fyrir bankagjöld og -þóknanir (lykill 60400), skal fylla út línu á síðunni **Vörpun texta á reikning** eins og hér fylgir.

| Varpar texta | Debetreikningsnúmer | Kreditreikningsnúmer | Upprunagerð stöðu | Upprunanúmer stöðu |
| --- | --- | --- | --- | --- |
| MyBank |AUTT |60400|Fjárhagur |AUTT |

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
