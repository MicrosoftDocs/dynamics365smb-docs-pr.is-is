---
title: "Nota Excel til að flytja inn gögn í Financials| Microsoft Docs"
description: "Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka
Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í glugganum **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður.  

> [!NOTE]  
> Grunnstillingarpakkar eru hluti af RapidStart Services fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], víðtækt verkfærasafn til að setja upp nýjar lausnir sem byggjast á viðskiptakröfum viðskiptavina og uppsetningargögnum. RapidStart Services býður einnig upp á virkni til innflutnings á eldri gögnum. Nánari upplýsingar er að finna í [Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

> [!TIP]  
>   Að öðrum kosti skal nota leiðsagnarforrit fyrir gagnafærslu til að flytja inn gögn frá QuickBooks eða Dynamics GP. Nánari upplýsingar, sjá [QuickBooks gagnafærsla](ui-extensions-quickbooks-data-migration.md) eða [Dynamics GP gagnafærsla](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="working-with-data-in-excel"></a>Unnið með gögn í Excel
Þegar sjálfgefinn grunnstillingarpakki er fluttur út í Excel inniheldur vinnubókin sem búin er til vinnublað fyrir hverja töflu í pakkanum. Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel. Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk. Til dæmis, bætið við auðu vinnublaði og afritið eldri gögnin á það. Búið því næst til Excel-formúlu til að varpa gögnum í umbreytingarvinnublaðinu á milli reitanna í útflutta vinnublaðinu og eldri gögnum viðskiptamanns. Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.  

> [!IMPORTANT]  
>  Ekki breyta dálkum í vinnublöðunum. Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="tables-in-the-default-configuration-package"></a>Töflur í sjálfgefnum grunnstillingarpakka
Sjálfgefni grunnstillingarpakkinn styður eftirfarandi töflur:

-   Greiðsluskilmálar
-   Verðflokkur viðskiptamanna
-   Afhendingarmáti
-   Sölumaður/innkaupaaðili
-   Birgðageymsla
-   Fjárhagsreikningur
-   Viðskiptavinur
-   Lánardrottinn
-   Atriði
-   Söluhaus
-   Sölulína
-   Innkaupahaus
-   Innkaupalína
-   Fh.færslubókarlína
-   Birgðabókarlína
-   Bókunarflokkur viðskm.
-   Bókunarflokkur lánardr.
-   Birgðabókunarflokkur
-   Mælieining
-   Alm. viðskiptabókunarflokkur
-   Alm. vörubókunarflokkur
-   Almennur bókunargrunnur
-   Umsjónarsvæði
-   Vöruflokkur
-   Söluverð
-   Innkaupsverð

## <a name="importing-customer-data"></a>Flytur inn viðskiptamannagögn
Eftir að gögn um viðskiptamenn eru færð inn í Excel, eru gögnin flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í glugganum **Grunnstillingarpakkar** eru gögnin flutt inn úr Excel-skránni og hægt er að sannprófa að gögnin séu í samræmi við [!INCLUDE[d365fin](includes/d365fin_md.md)] áður en pakkinn er notaður.

## <a name="see-also"></a>Sjá einnig
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks gagnaflutningur](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Gagnafærsla](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

