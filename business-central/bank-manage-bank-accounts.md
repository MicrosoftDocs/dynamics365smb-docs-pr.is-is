---
title: "Stjórna bankareikningum| Microsoft Docs"
description: "Með reglulegu millibili þarf að afstemma bankafjárhagsfærslur við viðkomandi bankafærslur á bankareikningunum þínum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 62b2bf8987146a69d17bd343f88d31d60a205ffb
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="managing-bank-accounts"></a>Stjórnun bankareikninga
Með reglulegu millibili þarf að stemma bankareikningsfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við viðkomandi bankafærslur í bankareikningum í bankanum þínum, og bóka svo stöðuna á þinn bankareikning. Hægt er að framkvæma þetta verk, annað hvort sem hluta af vinnslu á greiðslum sem koma fram á bankayfirliti í **greiðsluafstemmingarbók**. Einnig er hægt að framkvæma verkið aðskilið úr greiðsluvinnslu á síðunni **Afstemming bankareiknings** þar sem þú jafnar (afstemmir) bankayfirlitslínur í vinstri rúðunni við innri færslur í höfuðbók bankareikningsins þíns í hægri rúðunni. Á báðum síðunum geturðu fyllt út upplýsingar um bankayfirlit með því að flytja inn skrá eða straum og þú getur notað sjálfvirkar jöfnunarráðleggingar.

> [!NOTE]  
> Í norður-amerískum útgáfum getur þú einnig framkvæmt bankaafstemmingu á síðunni **Vinnublað bankaafstemmingar** sem er hentar betur fyrir ávísanir og innborganir en býður ekki upp á innflutning á bankayfirlitsskrám. Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu afvelja reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** á síðunni **Fjárhagsgrunnur**. Frekari upplýsingar er hægt að finna í hlutanum „Afstemma bankareikninga“ sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.

Stundum þarf að færa upphæðir milli bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að endurspegla millifærslur í bankanum þínum. Þú framkvæmir þetta verk á síðunni **almenn Færslubók** með mismunandi hætti eftir gjaldmiðli sjóðanna.

Áður en hægt er að stjórna bankareikningum verður að stofna sérhvern bankareikning sem bankareikningsspjald. Þar að auki þarf að setja upp rafrænar þjónustu sem má nota fyrir innflutning bankayfirlits og útflutning greiðsluskrár. Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-setup-banking.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
| Afstemma bankareikninga í tengslum við greiðsluvinnslu á síðunni **Greiðsluafstemmingarbók**. |[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Afstemma bankareikninga sem sérstakt verk á síðunni **Afstemming bankareiknings**, þar með talið tékkafærslur. |[Afstemma bankareikninga hvern fyrir sig](bank-how-reconcile-bank-accounts-separately.md) |
| Bóka færslur milli bankareikninga í sama gjaldmiðli eða í öðrum gjaldmiðlum. |[Flytja bankainnstæður](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Sjá einnig
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Stjórna skuldum](payables-manage-payables.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

