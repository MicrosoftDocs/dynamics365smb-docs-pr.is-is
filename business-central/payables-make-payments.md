---
title: Yfirlit yfir umsjónarverkhluta greiðslna til lánardrottna| Microsoft Docs
description: Útskýrir verkhluta sem fela í sér stjórnun greiðslna til lánardrottna, eins og að bóka greiðslulínur og sækja yfirlit fyrir gjaldfallna stöðu.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 02/08/2019
ms.author: edupont
ms.openlocfilehash: f2ff92af7dbf6c751cde795d3546d90c8d76a62b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799747"
---
# <a name="making-payments"></a>Framkvæma greiðslur

Þegar þú framkvæmir greiðslur til lánardrottna eða viðskiptamanna, eða endurgreiðir starfsmönnum, bókar þú tengdar greiðslulínur í **Greiðslubók** síðunni. Greiðslubókin er almenn færslubók sem er fínstillt til að framkvæma greiðslur og inniheldur fjölda öflugra aðgerða, svo sem **Greiðslutillögur til lánardrottna** aðgerð sem finnur lánardrottnagreiðslur sem eru komnar á gjalddaga, og **Lánardrottinn - aldursgreind samantekt** skýrsla sem sýnir yfirlit lánardrottnagreiðslna á gjalddaga.  

Þú getur byrjað að framkvæma greiðsluna af listum, kortum og fjárhagsfærslum fyrir lánardrottna, viðskiptamenn og starfsmenn. Hver af þessum síðum hefur hnapp sem byrjar greiðsluflæðið og hjálpar þér að fylla út í greiðslubókina.  

Úr greiðslubókinni er hægt að prenta vélfærða tékka eða skrá þegar tékkar eru skrifaðir. Þegar **Vélfærður tékki** er valinn í reitnum **Tegund bankagreiðslu** verður að prenta allar línur sem tákna tékka áður en hægt er að bóka greiðslubókina.

Þegar greiðslurnar eru bókaðar eru þær fluttar í bankaskrá til að hlaða þær upp í banka til meðhöndlunar.

Þegar búið er að framkvæma greiðslur til banka, þarf að jafna þær við tengdar opnar fjárhagsfærslur lánardrottna- eða starfmanna. Hægt er að gera það handvirkt eða með því að flytja inn bankayfirlitsskrá og jafna greiðslur sjálfkrafa. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
|Skilja grunnaðgerðir síðunnar **Greiðslubók**, sem byggir á færslubókinni, til að búa sig undir að bóka greiðslur til lánardrottna eða starfsmanna.|[Vinna í færslubókum](ui-work-general-journals.md)|
|Bóka greiðslur til lánardrottna eða starfsmanna og endurgreiðslur til viðskiptamanna og valfrjálst jafna greiðslur til tengdra ógreiddra reikninga/kreditreikninga til að loka þeim sem greiddum.|[Skrá greiðslur og endurgreiðslur](payables-how-post-payments-refunds.md)|
| Nota skal aðgerð á síðunni **Greiðslubók** til að leggja til lánardrottnagreiðslur samkvæmt völdum skilyrðum, eins og gjalddaga, afsláttarskilyrði og greiðslugetu þína. |[Greiðslutillögur til lánardr.](payables-how-suggest-vendor-payments.md) |
| Gefið út tékka vegna lánardrottnagreiðslna eða endurgreiðslna til viðskiptavina, annað hvort sem útprent eða sem vélfærðan tékka. Ógilda tékka fyrir eða eftir bókun. |[Framkvæma ávísanagreiðslur](payables-how-work-checks.md) |
|Framkvæma rafrænar greiðslur með því að flyta út greiðslur í bankaskrá sem þú hleður inn í bankann til úrvinnslu, þar með talið EFT (rafræn millifærsla) í Norður-Ameríku. |[Framkvæma rafrænar greiðslur](payables-how-export-payments-bank-file.md)|
|Gerðu rafrænar greiðslur í samræmi við SEPA-kreditfærslustaðla ESB.|[Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Greiða lánardrottni með peningum eða ávísun og bóka greiðsluna um leið og reikningurinn er bókaður. |[Greiða innkaupareikninga tímanlega](finance-how-to-settle-purchase-invoices-promptly.md) |
| Gakktu úr skugga um að bankinn þinn eingöngu hreinsar staðfestar athuganir og magn með því að senda þeim skrá sem inniheldur seljanda, athugun og greiðsluupplýsingar. |[Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md) |

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
