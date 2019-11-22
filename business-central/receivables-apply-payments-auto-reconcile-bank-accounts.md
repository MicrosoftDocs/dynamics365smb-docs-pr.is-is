---
title: Afstemming bankareikninga og greiðslujöfnun | Microsoft Docs
description: Útskýrir verkhluta sem fela í sér afstemmingu bankareikninga, krafna og skulda reikninga, bókanir inngreiðslna og útgjalda og sjálfvirka greiðslujöfnun.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 60a3cd3398e8a90160ab311dba1ae75fe70305b2
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692512"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Jafna greiðslur sjálfkrafa og afstemma bankareikninga
Þú verður að reglulega samræma bankareikninga þína, kröfur og skuldir reikninga með því að sækja greiðslur skráð í bankanum til tengdra ógreiddra reikninga og lánshæfiseinkna eða annarra opna færslna í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þú getur gert þetta verkefni á síðunni **Greiðsluafstemmingarbók** með því að flytja inn bankareikningsskrá eða fæða til að skrá greiðslurnar fljótt. Greiðslur eru beittar til að opna viðskiptavinar- eða seljanda bókasafns færslur sem eru byggðar á samsvörun milli greiðslustaðs og upplýsinga um innganga. Hægt er að skoða og breyta sjálfvirk jafnanir áður en færslubókin er bókuð. Þú getur valið að loka öllum opnum bankareikningsfærslum sem tengjast jöfnuðu fjárhagsfærslunum þegar þú bókar færslubókina. Bankareikningurinn er sjálfkrafa sáttur þegar allar greiðslur eru sóttar.

Einnig er hægt að afstemma bankareikninga án þess að greiðslujafna samtímis. Þetta verk er framkvæmt á síðunni **Afstemming bankareiknings**. Frekari upplýsingar í [Afstemma Bankareikning Sérstaklega](bank-how-reconcile-bank-accounts-separately.md).   

Til að flytja inn bankareikninga sem bankafæða þarftu fyrst að setja upp og virkja Envestnet Yodlee Bank Feed þjónustu og síðan tengja bankareikninga þína við tengda bankareikninga. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).  

Einnig er hægt að nota AMC Banking 365 Fundamentals viðbótina til að umbreyta bankayfirliti sem þú fékkst úr bankanum þínum í gagnastraum sem hægt er að flytja inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nánari upplýsingar um það eru í [Notkun AMC Banking 365 Fundamentals viðbótarinnar](ui-extensions-amc-banking.md).  

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

| Til | Sjá |
| --- | --- |
| Jafna greiðslur við opnar viðskiptavina- eða lánardrottnafærslur með því að flytja inn bankayfirlit, og afstemma bankareikning þegar allar greiðslur eru jafnaðar. |[Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md) |
| Jafnaðu greiðslur handvirkt með því að skoða ítarlegar upplýsingar um samsvöruð gögn og tillögur um mögulegar færslur til að jafna greiðslur á. |[Endurskoða eða sækja um greiðslur eftir sjálfvirkan umsókn](receivables-how-review-apply-payments-auto-application.md) |
| Leysa greiðslur sem ekki er hægt að beita sjálfkrafa við tengda opna aðalbókarfærslur. Til dæmis vegna þess að fjárhæðirnar eru mismunandi, eða vegna þess að tengd aðalbókaratriði er ekki til. |[Afstemma greiðslur sem ekki er hægt að nota sjálfkrafa](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Tengja skal texta á greiðslum við tiltekinn viðskiptamanns-, lánardrottins- eða fjárhagsreikning til að bóka alltaf endurtekna móttöku eða útgjöld reiðufés á þá reikninga þegar engin skjöl eru til til að beita þessu. |[Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
