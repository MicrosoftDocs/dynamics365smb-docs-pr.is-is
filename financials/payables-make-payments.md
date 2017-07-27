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
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a>Framkvæma greiðslur
Þegar greiðslur til lánardrottna eru framkvæmdar eru tengdar greiðslulínur bókaðar í glugganum **Greiðslubók**. Hægt er að nota aðgerðina **Greiðslutillögur til lánardrottna** til að finna greiðslur sem komnar eru á gjalddaga. Einnig er hægt að nota skýrsluna **Lánardrottinn - aldursgreind staða** til að fá yfirlit yfir greiðslur sem komnar eru á gjalddaga.

Úr greiðslubókinni er hægt að prenta vélfærða tékka eða skrá þegar tékkar eru skrifaðir. Þegar **Vélfærður tékki** er valinn í reitnum **Tegund bankagreiðslu** verður að prenta allar línur sem tákna tékka áður en hægt er að bóka greiðslubókina.

Þegar greiðslurnar eru bókaðar eru þær fluttar í bankaskrá til að hlaða þær upp í banka til meðhöndlunar.

Þegar búið er að framkvæma greiðslur til banka, þarf að jafna þær við tengdar opnar lánardrottnafærslur. Hægt er að gera það handvirkt eða með því að flytja inn bankayfirlitsskrá og jafna greiðslur sjálfkrafa. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og stemma af bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
| Nota skal aðgerð til að leggja til lánardrottnagreiðslur samkvæmt völdum skilyrðum, eins og gjalddaga, afsláttarskilyrði og greiðslugetu þína. |[Hvernig á að leggja til greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md) |
| Gefið út tékka vegna greiðslna, annað hvort útprentaða eða sem vélfærða tékka. Ógilda tékka fyrir eða eftir bókun. |[Hvernig á að: vinna með tékka](payables-how-work-checks.md) |
| Gakktu úr skugga um að bankinn þinn eingöngu hreinsar staðfestar athuganir og magn með því að senda þeim skrá sem inniheldur seljanda, athugun og greiðsluupplýsingar. |[Hvernig á að: flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md) |
|Flytja greiðslur úr glugganum **Greiðslubók** í bankaskrá sem þú hleður inn í bankann til vinnslu, þar með talið EFT (rafræn sjóðurflutningur) í Norður-Ameríku. |[Hvernig á að: Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

