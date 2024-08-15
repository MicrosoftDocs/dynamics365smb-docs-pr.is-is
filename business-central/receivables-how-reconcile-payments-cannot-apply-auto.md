---
title: Notkun millifærslumismunar á reikningaaðgerð til að stemma af greiðslur
description: 'Lýsir því hvernig á að vinna úr greiðslum sem ekki er hægt að jafna við skjal, til dæmis þegar gengi veldur mismunandi upphæðum.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Stemma af greiðslur sem ekki er hægt að jafna sjálfvirkt
Stundum þarf að meðhöndla greiðslur á bankareikning sem ekki er hægt að jafna við tengda opna viðskiptamanna-, lánardrottna- eða bankareikningsfærslu. Ástæður geta verið þær að ekkert fylgiskjal er til í [!INCLUDE[prod_short](includes/prod_short.md)] því að hægt sé að jafna greiðsluna við eða tengda fylgiskjalið í [!INCLUDE[prod_short](includes/prod_short.md)] hefur aðra upphæð en viðskiptaupphæðina, til dæmis vegna gengis. Á síðunni **Greiðsluafstemmingarbók** birtast allar færsluupphæðir fyrir greiðslur sem enn hafa ekki verið jafnaðar í reitnum **Mismunur**, þar á meðal upphæðir sem ekki er hægt að jafna vegna ástæðna eins og að ofan.

Aðferðirnar til að leysa úr þessum gerðum af ójöfnuðum greiðslum:
* Handvirk jöfnun
* Nota vörpun texta á reikning
* Flytja umframupphæð í færslubókarlínu til að stofna og bóka nauðsynlega færslu, svo sem endurgreiðslu á ofgreiðslu.

Greiðslur sem ekki er hægt að jafna geta birst í færslubókarlínum greiðsluafstemmingar á eftirfarandi mismunandi hátt:

* Gildið í **Mismunur** reit er jafnt og gildið í **færsluupphæð** reitnum sem gefur til kynna að enginn hluti greiðslunnar getur verið jafnaður við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslu.
* Gildið í **Mismunur** reit er lægri en gildið í **færsluupphæð** reitnum sem gefur til kynna að hluti greiðslunnar getur verið jafnaður við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslu. Ekki er hægt að jafna eftirstandandi hluta greiðslunnar og afstemma hana handvirkt eða með því að bóka hana beint á reikning.

Að afstemma slíka greiðslu, þú getur valið aðgerina **Flytja mismun á reikning** og tilgreina síðan hvaða reikning upphæðin í reitnum **mismunur** verður bókuð á þegar þú bókar greiðsluafstemmingarbók. Þetta er hægt að gera annaðhvort af síðunni **Greiðsluafstemmingarbók** eða af síðunni **Yfirlit greiðslujöfnunar** sem er opnuð með því að velja gildið í reitnum **Áreiðanleiki samsvörunar** eða með því að velja reitinn **Mismunur**.

> [!TIP]  
>   Svipuð virkni er til til að setja upp sjálfvirka afstemmingu á endurteknum greiðslum sem er ekki hægt að jafna við tengda opna viðskiptavina-, lánardrottna- eða bankareikningsfærslur. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## Til að stemma af greiðslur sem ekki er hægt að jafna sjálfvirkt
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluafstemmingarbækur** og velja síðan viðkomandi tengil.
2. Opna skal greiðsluafstemmingarbók. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)
3. Veldu **Flytja mismun á reikning** Síðan **Flytja mismun á reikning** opnast.
4. Í reitnum **Tegund reiknings** tilgreindu tegund reiknings sem greiðsluupphæðin verður bókuð á.
5. Í reitnum **Reikningsnúmer** tilgreindu reiknings sem greiðsluupphæð verður bókuð á.
6. Í reitnum **Lýsing** tilgreindu texta sem lýsir þessum beinu greiðslubókun. Sjálfgefið er að textinn í reitnum **Færslutexti** sé færður inn.
7. Velja hnappinn **Í lagi**.

Ef gildið í í **Mismunur** reit var jafnt og gildið í reitnum á **færsluupphæð** reit þegar þú bókar greiðsluafstemmingarbók, verður öll greiðslan á færslubókarlínu bókuð beint á tilgreindan mótreikning.

Ef gildið í í **Mismunur** reit var lægra en gildið í **færsluupphæð** þá verður aukaleg færslubókarlína stofnuð með sama texta og dagsetningu með mismuninum innsettum í reitinn **færsluupphæð** Á upphaflegu færslubókarlínu er mismunurinn dreginn frá gildinu í **færsluupphæð** reitnum, og greiðslan verður áfram jöfnuð við tengdan viðskiptavinar-, lánardrottins eða bankareikningsfærslu. Þegar þú bókar greiðsluafstemmingarbók, verður einn hluti greiðslunnar bókuð sem jöfnuð greiðsla. Aðra hluti greiðslu bókast beint á tilgreinda reikninga.

## Sjá einnig .
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]