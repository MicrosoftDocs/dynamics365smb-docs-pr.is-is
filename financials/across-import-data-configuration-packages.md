---
title: "Nota Excel til að ná í eldri gögn inn í Financials | Microsoft Docs"
description: "Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0151b1c3d8bddd4692c494d1c0e5d1c036da424e
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka
Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í glugganum **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður.  

Ef notandi þekkir RapidStart Services for Microsoft Dynamics, þekkir hann einnig grunnstillingarpakka. Sjálfgefinn grunnstillingarpakki styður algengustu gerðir gagna sem notandi vill flytja inn úr eldra kerfi. Í Excel er þá hægt að bæta við gögnunum úr eldra kerfinu og setja þau upp í samræmi við viðskiptagrunn [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
