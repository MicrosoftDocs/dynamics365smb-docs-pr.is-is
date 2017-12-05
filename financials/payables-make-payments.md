---
title: "Yfirlit yfir umsjónarverkhluta greiðslna til lánardrottna| Microsoft Docs"
description: "Útskýrir verkhluta sem fela í sér stjórnun greiðslna til lánardrottna, eins og að bóka greiðslulínur og sækja yfirlit fyrir gjaldfallna stöðu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: c8766d42b579397e63676c1d46fb8a03cbe24aae
ms.contentlocale: is-is
ms.lasthandoff: 10/17/2017

---
# <a name="making-payments"></a>Framkvæma greiðslur
Þegar greiðslur til lánardrottna eða endurgreiðslur til starfsmanna eru framkvæmdar eru tengdar greiðslulínur bókaðar í glugganum **Greiðslubók**. Hægt er að nota aðgerðina **Greiðslutillögur til lánardrottna** til að finna lánardrottnagreiðslur sem komnar eru á gjalddaga. Einnig er hægt að nota skýrsluna **Lánardrottinn - aldursgreind staða** til að fá yfirlit yfir lánardrottnagreiðslur sem komnar eru á gjalddaga.

Úr greiðslubókinni er hægt að prenta vélfærða tékka eða skrá þegar tékkar eru skrifaðir. Þegar **Vélfærður tékki** er valinn í reitnum **Tegund bankagreiðslu** verður að prenta allar línur sem tákna tékka áður en hægt er að bóka greiðslubókina.

Þegar greiðslurnar eru bókaðar eru þær fluttar í bankaskrá til að hlaða þær upp í banka til meðhöndlunar.

Þegar búið er að framkvæma greiðslur til banka, þarf að jafna þær við tengdar opnar fjárhagsfærslur lánardrottna- eða starfmanna. Hægt er að gera það handvirkt eða með því að flytja inn bankayfirlitsskrá og jafna greiðslur sjálfkrafa. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
|Nota gluggann **Greiðslubók**, sem byggir á færslubókinni, til að bóka greiðslur á lánardrottna eða starfsmanna.|[Vinna í færslubókum](ui-work-general-journals.md)|
| Nota skal aðgerð til að leggja til lánardrottnagreiðslur samkvæmt völdum skilyrðum, eins og gjalddaga, afsláttarskilyrði og greiðslugetu þína. |[Hvernig á að leggja til greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md) |
|Endurgreiða starfsmönnum fyrir persónuleg útgjöld í viðskiptaerindum með því að greiða inn á bankareikning þeirra.|[Hvernig á að: Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).|
| Gefið út tékka vegna lánardrottnagreiðslna, annað hvort útprentaða eða sem vélfærða tékka. Ógilda tékka fyrir eða eftir bókun. |[Hvernig á að: vinna með tékka](payables-how-work-checks.md) |
| Greiða lánardrottni með peningum eða ávísun og bóka greiðsluna um leið og reikningurinn er bókaður. |[Hvernig á að gera skjótt upp Innkaupareikninga](finance-how-to-settle-purchase-invoices-promptly.md) |
| Gakktu úr skugga um að bankinn þinn eingöngu hreinsar staðfestar athuganir og magn með því að senda þeim skrá sem inniheldur seljanda, athugun og greiðsluupplýsingar. |[Hvernig á að: flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md) |
|Flytja greiðslur úr glugganum **Greiðslubók** í bankaskrá sem þú hleður inn í bankann til vinnslu, þar með talið EFT (rafræn sjóðurflutningur) í Norður-Ameríku. |[Hvernig á að: Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

