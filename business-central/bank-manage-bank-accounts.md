---
title: Stjórna bankareikningum| Microsoft Docs
description: Með reglulegu millibili þarf að afstemma bankafjárhagsfærslur við viðkomandi bankafærslur á bankareikningunum þínum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 01/10/2020
ms.author: sgroespe
ms.openlocfilehash: 0d1a38468f5d07a1170027bc728ba16996f2b782
ms.sourcegitcommit: 2f741f442226b8be74586e355f283f365e43220f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947238"
---
# <a name="reconciling-bank-accounts"></a>Afstemming bankareikninga
Ljúka ætti bankaafstemmingu með reglulegu millibili fyrir alla bankareikninga til að tryggja að peningafærslur fyrirtækisins séu réttar. Þetta er gert með því að bera saman og jafna færslur á innri bankareikningum við bankafærslur í bankanum þínum og síðan bóka stöðurnar á innri bankareikningana svo að samtölur verði í boði fyrir fjármálastjóra. Bankaafstemming er einnig hagkvæm leið til að uppgötva og leysa úr greiðslum sem vantar upp á og bókhaldsvillum.

Hægt er að framkvæma verkið á síðunni **Afstemming bankareiknings** þar sem þú jafnar (afstemmir) bankayfirlitslínur í vinstri rúðunni við innri fjárhagsfærslur bankareikningsins þíns í hægri rúðunni. Annars er hægt að framkvæma þetta verk á síðunni **Greiðsluafstemmingarbók** sem hluti af úrvinnslu greiðslnanna sem koma fram á bankayfirliti. Á báðum síðunum geturðu fyllt út upplýsingar um bankayfirlit með því að flytja inn skrá eða straum og þú getur notað sjálfvirkar jöfnunarráðleggingar.

> [!NOTE]  
> Í norður-amerískum útgáfum getur þú einnig framkvæmt bankaafstemmingu á síðunni **Vinnublað bankaafstemmingar** sem er hentar betur fyrir ávísanir og innborganir en býður ekki upp á innflutning á bankayfirlitsskrám. Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu afvelja reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** á síðunni **Fjárhagsgrunnur**. Frekari upplýsingar er hægt að finna í hlutanum „Afstemma bankareikninga“ sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.

Áður en hægt er að stjórna bankareikningum innan [!INCLUDE[d365fin](includes/d365fin_md.md)] verður að setja upp sérhvern bankareikning sem bankareikningsspjald. Þar að auki þarf að setja upp rafrænar þjónustu sem má nota fyrir innflutning bankayfirlits og útflutning greiðsluskrár. Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-setup-banking.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til að | Sjá |
| --- | --- |
| Afstemmið bankareikninga sem sérstakt verk á síðunni **Afstemming bankareiknings**. |[Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md) |
| Afstemma bankareikninga í tengslum við greiðsluvinnslu á síðunni **Greiðsluafstemmingarbók**. |[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learnlearnpathsreconcile-bank-accounts-dynamics-365-business-central"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Flytja bankainnstæður](bank-how-transfer-bank-funds.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Stjórna skuldum](payables-manage-payables.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)
