---
title: Setja upp fjármálaferli| Microsoft Docs
description: Kynntu þér verkhlutana í því að setja upp fjármál í fyrirtækinu sem hentar öllum þínum þörfum tengdum bókhaldi, endurskoðun eða bókunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a659fd4edfcbeccf65204f30685ce5b3cf527399
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381932"
---
# <a name="setting-up-finance"></a>Uppsetning Fjármála
Áður en þú getur byrjað að reka fyrirtækið þitt verður þú að tilgreina reglur og sjálfgefin gildi fyrir það hvernig stjórna á fjárhagsferlum fyrir fyrirtækið. Fyrsta skrefið er að setja upp kjarna bókhaldsskráningar fyrirtækisins - bókhaldslyklana. Síðan eru settir upp bókunarflokkar, sem gera ferli úthlutunar sjálfgefinna almennra bókunarreikninga til viðskiptamanna, lánardrottna og vara skilvirkara.

Hægt er að setja upp suma fjárhagsuppsetningu sjálfkrafa með uppsetningarleiðbeiningum með hjálp og suma verður að gera handvirkt. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).

Hægt er að nota víddir til að bæta mismunandi gerðum upplýsinga við öll viðskipti. Hægt er að setja upp grunnvíddir fyrirtækisins, svo sem Verkefni og Deildir. Síðar er hægt að bæta við fleiri víddum eftir þörfum, og setja upp tímabundnar víddir sem nota á í takmarkaðan tíma, til dæmis í tengslum við söluherferð. Frekari upplýsingar er að finna í [Unnið með víddir](finance-dimensions.md).

Ljúka þarf mörgum af uppsetningarverkhlutunum áður en hægt er að hefja skráningu fjárhagslegra samskipta, en hægt er að breyta flestum stillingum síðar. Sumir uppsetningarverkhlutarnir eru valfrjálsir, til dæmis eru Bókun m. fyrirtækja og Samstæður aðeins sett upp ef unnið er með mörg fyrirtæki. Suma uppsetningarverk, svo sem tilgreiningu tímabilsins þar sem bókanir eru leyfðar, þarf hugsanlega að endurtaka með reglulegu millibili.  

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til að | Sjá |
| --- | --- |
| Tilgreinið hvernig viðskiptavinir eiga að greiða og hvernig á að greiða lánardrottnum. |[Setja upp greiðsluhætti](finance-payment-methods.md) |
| Tilgreindu greiðsluskilmála til að sjá um gjalddaga og reikna hugsanlega út greiðsluafslætti.|[Setja upp greiðsluskilmála](finance-payment-terms.md) |
| Tilgreinið bókunarhópa sem kortleggja aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. |[Uppsetning bókunarflokka](finance-posting-groups.md)|
|Búðu til fjárhagsskema og skilgreindu lyklategundir til að skilgreina efni fjárhagsgrafa og skýrslna á borð við efnahagsreikning og skýrslur tekjuyfirlits.|[Undirbúa fjárhagsskýrslugerð með fjárhagsskemu og lyklategundum](bi-how-work-account-schedule.md)|
|Hægt er að setja upp vikmörk þannig að kerfið loki reikningi jafnvel þótt greiðsla, að meðteknum afslætti, nái ekki upp í fulla upphæð á reikningnum.|[Unnið með greiðsluvikmörk og greiðsluafsláttarvikmörk](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Uppsetning fjárhagstímabila. |[Unnið með fjárhagstímabil og fjárhagsár](finance-accounting-periods-and-fiscal-years.md) |
|Setja upp áminningarskilmála til að aðstoða við innheimtu á gjaldföllnum greiðslum.|[Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md)|
| Skilgreinið hvernig VSK upphæðir, sem fengnar eru fyrir sölu, eru sendar inn til skattayfirvalda. |[Setja upp virðisaukaskatt (VSK)](finance-setup-vat.md)|
|Undirbúa að nota óinnleystan VSK í tengslum við greiðslumátann reiðufé.|[Uppsetning óinnleyst virðisaukaskatts fyrir reiðufé](finance-setup-unrealized-vat.md)|
| Settu eiginleika sölu og innkaupa upp þannig að hægt sé að vinna með erlenda gjaldmiðla.|[Leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum](finance-how-enable-application-ledger-entries-different-currencies.md)
|Skilgreindu eina eða fleiri viðbótargjaldmiðla þannig að upphæðir séu sjálfkrafa skráðar í bæði SGM og í öðrum skýrslugjaldmiðli fyrir hverja fjárhagsfærslu og aðrar færslur.|[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)|
|Stilla reglulega jafngildi viðbótargjaldmiðils til að bæta upp sveiflur í gengi.|[Uppfæra gengi](finance-how-update-currencies.md)|
|Skilgreina marga vexti sem á að nota fyrir mismunandi tímabil vegna seinkunar á greiðslum fyrir viðskiptafærslur.|[Setja upp marga vexti](finance-how-to-set-up-multiple-interest-rates.md)|
|Undirbúa að slétta reikningsupphæðir sjálfvirkt þegar reikningar eru stofnaðir.|[Uppsetning sléttunargerðar reikninga](finance-set-up-invoice-rounding.md)|
| Bæta nýjum reikningum við eldri bókhaldslykil. |[Uppsetning bókhaldslykilsins](finance-setup-chart-accounts.md) |
| Setjið upp viðskiptaupplýsingar (BI) töflur til að greina sjóðstreymi. |[Setja upp sjóðstreymisgreiningu](finance-setup-cash-flow-analyses.md) |
|Gera virka reikningsfærslu viðskiptamanns sem er ekki uppsettur í kerfið.|[Uppsetning staðgreiðsluviðskiptamanna](finance-how-to-set-up-cash-customers.md)|
| Uppsetning á Intrastat skýrslugerð, og senda inn skýrsluna til yfirvalda. | [Setja upp og skrá Intrastat](finance-how-setup-report-intrastat.md)|
|Gakktu úr skugga um að færsla úr færslubók sé úthlutað á nokkra mismunandi reikninga þegar færslubókin er bókuð, annaðhvort magn, prósenta eða upphæð.|[Nota úthlutunarlykla í færslubókum](ui-how-use-allocation-keys-general-journals.md)|
|Settu upp upprunakóða og ástæðukóða sem hægt er að nota til að fylgjast með endurskoðunarslóðum|[Uppsetning upprunakóða og ástæðukóða fyrir endurskoðunarslóðir](finance-setup-trail-codes.md)|
|Tilgreina sjálfgefnar skýrslur sem á að nota fyrir mismunandi skjalagerðir.|[Skýrsluval í Business Central](across-report-selections.md)|

> [!TIP]
> Það fer eftir landfræðilegri staðsetningu þinni hvaða reiti sumar síður innihalda sem ekki er lýst í greinunum sem eru gefnar upp hér vegna þess að þær gilda um staðbundna virkni eða sérstillingar. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Unnið með víddir](finance-dimensions.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]