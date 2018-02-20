---
title: "Stjórna bankareikningum| Microsoft Docs"
description: "Með reglulegu millibili þarf að afstemma bankafjárahagsfærslur í Financials við viðkomandi bankafærslur á bankareikningunum þínum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0d126a89064c3e899f864e63647e76f5e59e1666
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="managing-bank-accounts"></a>Stjórnun bankareikninga
Með reglulegu millibili þarf að stemma bankareikningsfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við viðkomandi bankafærslur í bankareikningum í bankanum þínum, og bóka svo stöðuna á þinn bankareikning. Hægt er að framkvæma þetta verk, annað hvort sem hluta af vinnslu á greiðslum sem koma fram á bankayfirliti í **greiðsluafstemmingarbók**. Einnig er hægt að framkvæma verkið sérstaklega úr greiðsluvinnslu, í glugganum **Afstemming bankareiknings** sem styður tékkafærslur. Í báðum tilvikum er fyllt í gluggann með innflutningi á bankayfirlitið í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Stundum þarf að færa upphæðir milli bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að endurspegla millifærslur í bankanum þínum. Þú framkvæmir þetta verk í flugganum **almenn Færslubók** með mismunandi hætti eftir gjaldmiðli sjóðanna.

Áður en hægt er að stjórna bankareikningum verður að stofna sérhvern bankareikning sem bankareikningsspjald. Þar að auki þarf að setja upp rafrænar þjónustu sem má nota fyrir innflutning bankayfirlits og útflutning greiðsluskrár. Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-setup-banking.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
| Afstemma bankareikninga í tengslum við greiðsluvinnslu í glugganum **greiðsluafstemmingarbók** |[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Afstemma bankareikninga sem sérstakt verk í reitinn **afstemming bankareiknings** glugganum, þar með talið tékkafærslur. |[Afstemma bankareikninga hvern fyrir sig](bank-how-reconcile-bank-accounts-separately.md) |
| Bóka færslur milli bankareikninga í sama gjaldmiðli eða í öðrum gjaldmiðlum. |[Flytja bankainnstæður](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Sjá einnig
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Stjórna skuldum](payables-manage-payables.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

