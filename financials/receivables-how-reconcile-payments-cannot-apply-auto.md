---
title: "Hvernig á að: afstemma greiðslur sem ekki er hægt að afstemma sjálfkrafa | Microsoft Docs"
description: "hvernig á að: afstemma greiðslur sem ekki er hægt að afstemma sjálfkrafa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7b4c109ebda260ee86e2b955a17389b54493de65
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-payments-that-cannot-be-applied-automatically"></a>hvernig á að: afstemma greiðslur sem ekki er hægt að afstemma sjálfkrafa.
Stundum gætirðu þurft að meðhöndla greiðslur inna á bankareikninginn þinn sem ekki er hægt að jafna við tengdan opinn viðskiptavin, lánardrottin, eða bankareikningsfærslu. Ástæða kann að vera að ekkert skjal sé til í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem hægt er að jafna greiðsluna á, eða tengda skjalið í [!INCLUDE[d365fin](includes/d365fin_md.md)] hefur aðra fjárhæð en færsluupphæðin, t.d. vegna gjaldeyrisviðskipta Í **greiðslubók Afstemming** glugga, allar færsluupphæðir fyrir greiðslur sem ekki eru jafnaðar enn birtast í **mismunur ** reit, þar með talið upphæðir sem ekki er hægt að jafna vegna ástæða eins og þeirrar sem nefd var að ofan.

Greiðslur sem ekki er hægt að jafna geta birst á greiðsluafstemmingarbókarlínum á eftirfarandi mismunandi hætti:

* Gildið í **Mismunur** reit er jafnt og gildið í **færsluupphæð** reitnum sem gefur til kynna að enginn hluti greiðslunnar getur verið jafnaður við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslu.
* Gildið í **Mismunur** reit er lægri en gildið í **færsluupphæð** reitnum sem gefur til kynna að hluti greiðslunnar getur verið jafnaður við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslu. Eftirstandandi hluti greiðslunnar er ekki hægt að jafna og verður að vera afstemmdur handvirkt eða með því að bóka hann beint á reikninginn.

Að afstemma slíka greiðslu, þú getur valið flutnings hnappinn Flytja mismun á reikning og tilgreina síðan hvaða reikning upphæðin í reitnum mismunur verður bókuð á þegar þú bókar greiðsluafstemmingarbók.

**Athuga skal að**: Svipuð virkni er til til að setja upp sjálfvirka afsettmingu á endurteknum greiðslum sem er ekki hægt að jafna við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslur. Fyrir frekar upplýsingar, sjá [Hvernig á að varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Að afstemma greiðslur sem ekki er hægt að jafna
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Greiðsluafstemmingarbækur**, og velja síðan viðeigandi tengil.
2. Opna skal greiðsluafstemmingarbók. Frekari upplýsingar eru í [hvernig á að afstemma greiðslur með því að nota sjálfvirka jöfnun](receivables-how-reconcile-payments-auto-application.md)
3. Veldu **Flytja mismun á reikning** Glugginn **Flytja mismun á reikning** opnast.
4. Í reitnum **Tegund reiknings** tilgreindu tegund reiknings sem greiðsluupphæðin verður bókuð á.
5. Í svæðinu **Bankareikningsnúmer**,  reit, tilgreindu reiknings sem greiðsluupphæð verður bókuð á.
6. Í reitnum **Lýsing** tilgreindu texta sem lýsir þessum beinu greiðslubókun. Sjálfgefið er að textinn í reitnum **Færslutexti ** sé færður inn.
7. Velja hnappinn **Í lagi**.

Ef gildið í í **Mismunur** reit var jafnt og gildið í reitnum á **færsluupphæð** reit þegar þú bókar greiðsluafstemmingarbók, verður öll greiðslan á færslubókarlínu bókuð beint á tilgreindan mótreikning.

Ef gildið í í **Mismunur** reit var lægra en gildið í **færsluupphæð** þá verður aukaleg færslubókarlína stofnuð með sama texta og dagsetningu með mismuninum innsettum í reitinn **færsluupphæð** Á upphaflegu færslubókarlínu er mismunurinn dreginn frá gildinu í **færsluupphæð ** reitnum, og greiðslan verður áfram jöfnuð við tengdan viðskiptavinar-, lánardrottins eða bankareikningsfærslu. Þegar þú bókar greiðsluafstemmingarbók, verður einn hluti greiðslunnar bókuð sem jöfnuð greiðsla. Aðra hluti greiðslu bókast beint á tilgreinda reikninga.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

