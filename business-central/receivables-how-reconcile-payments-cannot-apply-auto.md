---
title: Afstemma greiðslur með því að nota eiginleikann Flytja mismun á reikning
description: Lýsir því hvernig skal vinna greiðslur sem ekki er hægt að jafna við skjal, til dæmis þegar gengi gjaldmiðla veldur breytingum á upphæðum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: aa43e57adc60f7ec01bd7bf4c3bcdd20cdd476fd
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013818"
---
# <a name="reconcile-payments-that-cannot-be-applied-automatically"></a>Afstemma greiðslur sem ekki er hægt að nota sjálfkrafa
Stundum gætirðu þurft að meðhöndla greiðslur inna á bankareikninginn þinn sem ekki er hægt að jafna við tengdan opinn viðskiptavin, lánardrottin, eða bankareikningsfærslu. Ástæða kann að vera að ekkert skjal sé til í [!INCLUDE[prod_short](includes/prod_short.md)] sem hægt er að jafna greiðsluna á, eða tengda skjalið í [!INCLUDE[prod_short](includes/prod_short.md)] hefur aðra fjárhæð en færsluupphæðin, t.d. vegna gjaldeyrisviðskipta Á síðunni **Greiðsluafstemmingarbók**, birtast allar færsluupphæðir fyrir greiðslur sem eru enn ekki jafnaðar í reitnum **Mismunur**, þar með talið upphæðir sem ekki er hægt að jafna vegna ástæðna eins og þeirrar sem nefnd var hér að ofan.

Greiðslur sem ekki er hægt að jafna geta birst á greiðsluafstemmingarbókarlínum á eftirfarandi mismunandi hætti:

* Gildið í **Mismunur** reit er jafnt og gildið í **færsluupphæð** reitnum sem gefur til kynna að enginn hluti greiðslunnar getur verið jafnaður við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslu.
* Gildið í **Mismunur** reit er lægri en gildið í **færsluupphæð** reitnum sem gefur til kynna að hluti greiðslunnar getur verið jafnaður við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslu. Eftirstandandi hluti greiðslunnar er ekki hægt að jafna og verður að vera afstemmdur handvirkt eða með því að bóka hann beint á reikninginn.

Að afstemma slíka greiðslu, þú getur valið flutnings hnappinn **Flytja mismun á reikning** og tilgreina síðan hvaða reikning upphæðin í reitnum **mismunur** verður bókuð á þegar þú bókar greiðsluafstemmingarbók.

> [!TIP]  
>   Svipuð virkni er til til að setja upp sjálfvirka afstemmingu á endurteknum greiðslum sem er ekki hægt að jafna við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslur. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied-automatically"></a>Að afstemma greiðslur sem ekki er hægt að afstemma sjálfkrafa
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðsluafstemmingarbækur** og veldu síðan tengda tengilinn.
2. Opna skal greiðsluafstemmingarbók. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)
3. Veldu **Flytja mismun á reikning** Síðan **Flytja mismun á reikning** opnast.
4. Í reitnum **Tegund reiknings** tilgreindu tegund reiknings sem greiðsluupphæðin verður bókuð á.
5. Í reitnum **Reikningsnúmer** tilgreindu reiknings sem greiðsluupphæð verður bókuð á.
6. Í reitnum **Lýsing** tilgreindu texta sem lýsir þessum beinu greiðslubókun. Sjálfgefið er að textinn í reitnum **Færslutexti** sé færður inn.
7. Velja hnappinn **Í lagi**.

Ef gildið í í **Mismunur** reit var jafnt og gildið í reitnum á **færsluupphæð** reit þegar þú bókar greiðsluafstemmingarbók, verður öll greiðslan á færslubókarlínu bókuð beint á tilgreindan mótreikning.

Ef gildið í í **Mismunur** reit var lægra en gildið í **færsluupphæð** þá verður aukaleg færslubókarlína stofnuð með sama texta og dagsetningu með mismuninum innsettum í reitinn **færsluupphæð** Á upphaflegu færslubókarlínu er mismunurinn dreginn frá gildinu í **færsluupphæð** reitnum, og greiðslan verður áfram jöfnuð við tengdan viðskiptavinar-, lánardrottins eða bankareikningsfærslu. Þegar þú bókar greiðsluafstemmingarbók, verður einn hluti greiðslunnar bókuð sem jöfnuð greiðsla. Aðra hluti greiðslu bókast beint á tilgreinda reikninga.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]