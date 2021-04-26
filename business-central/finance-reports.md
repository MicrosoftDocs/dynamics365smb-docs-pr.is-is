---
title: Fjárhagsskýrslur í Business Central
description: Finnið út hvaða fjárhagsskýrslur eru í boði í staðlaðri útgáfu Business Central til að halda utan um reksturinn.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a36e40796978ddd20df818c3bccb1e148d50a4e1
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783773"
---
# <a name="financial-reports-in-business-central"></a>Fjárhagsskýrslur í Business Central

Fjárhagsskýrslugerð fyrir [!INCLUDE [prod_short](includes/prod_short.md)] gerir fjármála og viðskiptafagfólk kleift að búa til, viðhalda, innleiða og skoða reikningsskil. Það býður upp á fleiri valkosti en hefðbundið skýrslugerð skorður til að hjálpa að hanna mismunandi gerðir af skýrslum. [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur nokkrar skýrslur, rakningaraðgerðir og verkfæri sem aðstoða endurskoðendur eða stjórnendur sem bera ábyrgð á skýrslugjöf til fjármáladeildarinnar. Fjárhagsskýrslugerð felur í sér stuðning fyrir víddir, þannig að lyklahlutar eða víddir séu strax í boði. Engin verkfæri til viðbótar eða skilgreiningu skref eru nauðsynleg.  

## <a name="reports"></a>Skýrslur

Eftirfarandi tafla lýsir sumum helstu skýrslunum í fjárhagsskýrslugerð.

|Skýrsla |Description  |
|---------|---------|
|**Leiðr. kostnað - Birgðafærslur** | Leiðréttir birgðavirði í virðisfærslum til að hægt sé að nota réttan kostnað við uppfærslu fjárhags og til að talnagögn um sölu og hagnað séu rétt. Leiðrétting kostnaðar flytur allar kostnaðarbreytingar úr færslum á innleið, til dæmis færslur fyrir innkaup eða framleiðslufrálag, í viðeigandi færslur á útleið, til dæmis sölu og millifærslur.  |
|**Prófjöfnuður**| Sýnir bókhaldslykla samkvæmt stöðum og hreyfingum. Hægt er að velja að skoða prófjöfnuð fyrir tilteknar víddir. Hægt er að nota skýrsluna í lok fjárhagstímabils eða reikningsárs. |
|**Prófjöfnuður eftir tímabili**  | Sýnir upphafsstöðu fjárhagsreikningsins, hreyfingar á völdu tímabili (mánuði, fjórðungi eða ári) og lokastöðuna.         |
|**Prófjöfnuður - Áætlun** | Hér kemur fram samanburður á prófjöfnuði og áætlun. Hægt er að velja að skoða prófjöfnuð fyrir tilteknar víddir. Hægt er að nota skýrsluna í lok fjárhagstímabils eða reikningsárs.        |
|**Ítarlegur prófjöfnuður** |sýnir sundurliðaðan prófjöfnuð fyrir tilgreinda fjárhagsreikninga. Hægt er að nota skýrsluna í lok fjárhagstímabils eða reikningsárs. Hægt er að velja reikninga í skýrsluna með því að setja afmörkun.         |
|**Prófjöfnuður - Fyrra ár**|Hér kemur fram prófjöfnuður í samanburði við tölur fyrra árs. Hægt er að velja að skoða prófjöfnuð fyrir tilteknar víddir. Hægt er að nota skýrsluna í lok fjárhagstímabils eða reikningsárs. Athugið að með *fyrra ári* er átt við sama tímabil og á árinu áður.|
|**Fjárhagsskema**|Fjárhagsskema er hægt að nota til þess að birta fjárhagsreikninga á annan hátt en í bókhaldslyklinum. Fjárhagsskemu má t.d. nota til að fá skýrslur með lykiltölum.|
<|**Efnahagsreikningur** (Fjárhagsskema eða Excel) eða **Prófjöfnuður** |         |
|**Sjóðstreymisyfirlit** (Fjárhagsskema) |         |
|**Samantekt/upplýsingar um prófjöfnuð** |         |
|**Rekstrarreikningur** (Fjárhagsskema eða Excel)||
|**Fjárhagsáætlun** ||-->

## <a name="tasks"></a>Verk

Eftirfarandi greinar lýsa sumum lykilverkum til að greina stöðu fyrirtækisins:

* [Greina raunverulegar og áætlaðar upphæðir](bi-how-analyze-actual-versus-budget.md)  
* [Undirbúa fjárhagsskýrslugerð með fjárhagsskemu og lyklategundum](bi-how-work-account-schedule.md)  
* [Setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md)  
* [Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
* [Stofna greiningarskýrslur](bi-how-create-analysis-views-reports.md)  
* [Stofna skýrslur með XBRL](bi-create-reports-with-xbrl.md)  
* [Stjórna ástæðu fyrir aðgangi að gagnagrunni](admin-data-access-intent.md)  

## <a name="see-also"></a>Sjá einnig .

[Stofna kostnaðaráætlanir](finance-create-cost-budgets.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Nota skýrslur fyrir lokun](year-prepare-preclose-reports.md)  
[Undirbúningur lokunaryfirlits](year-prepare-close-statement.md)  
[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Unnið með víddir](finance-dimensions.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjármál](finance.md)  
[Yfirlit yfir staðbundna virkni](about-localization.md)  
[Endurskoðandi upplifun í [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]