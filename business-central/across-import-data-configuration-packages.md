---
title: Nota Excel til að flytja inn gögn í Business Central| Microsoft Docs
description: Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 12/04/2019
ms.author: edupont
ms.openlocfilehash: ff9f17e6ac1625dc4d1f27a39fc843d9eaa375d7
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896254"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Innflutningur viðskiptagagna úr öðrum fjárhagskerfum
Þegar notandi skráir sig í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að ákveða að búa til autt fyrirtæki svo hægt sé að hlaða upp eigin gögnum og prófa áfram nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtækið. Það fer eftir því fjárhagskerfi sem fyrirtækið notar í dag hvernig og hvort hægt er að millifæra upplýsingar um viðskiptamenn, lánardrottna, birgðir og bankareikninga.  

Hægt er að ræsa leiðarvísi um uppsetningu með hjálp frá Mitt hlutverk sem hjálpar til við að flytja viðskiptagögn úr Excel-skrá eða öðrum sniðum. Þær skráategundir sem hægt er að hlaða upp fer eftir viðbótunum sem í boði eru. Til dæmis er hægt að yfirfæra gögn úr QuickBooks vegna þess að [!INCLUDE[d365fin](includes/d365fin_md.md)] felur í sér viðbót sem sér um umbreytingu úr QuickBooks. Ef notandi vill yfirfæra gögn úr öðrum fjárhagskerfum þarf annað hvort að athuga hvort viðbót er í boði fyrir það kerfi eða flytja gögnin inn úr Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur sniðmát fyrir viðskiptamenn, lánardrottna og birgðavörur sem hægt er að nota þegar gögnum er hlaðið upp.

Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Á síðunni **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður.  

> [!TIP]  
> Að öðrum kosti skal nota leiðsagnarforrit fyrir gagnafærslu til að flytja inn gögn frá QuickBooks eða Dynamics GP. Nánari upplýsingar, sjá [QuickBooks gagnafærsla](ui-extensions-quickbooks-data-migration.md) eða [Dynamics GP gagnafærsla](ui-extensions-dynamicsgp-data-migration.md).

> [!NOTE]  
> Fyrir stærri innleiðingarverk getur þú notað RapidStart Services fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], sem er víðtækt verkfærasafn til að setja upp nýjar lausnir sem byggjast á viðskiptakröfum viðskiptamanna og uppsetningargögnum. RapidStart Services býður einnig upp á virkni til að flytja inn viðskiptagögn. Nánari upplýsingar er að finna í [Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Til að flytja inn myndir af vörum er hægt að nota þar til gerða aðgerð á síðunni **Uppsetning birgða**. Frekari upplýsingar er að finna í [Flytja inn margar vörumyndir](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Innflutningur gagna úr grunnstillingarpakka
[!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur stillingarpakka sem þú getur flutt út í Excel og sett upp gögnin þín þar. Síðan er hægt að flytja aftur inn gögnin úr Excel. Pakkinn samanstendur af 27 töflum, þar með talið aðalgögnum, svo sem viðskiptavinum, söluaðilum, hlutum og reikningum, öðrum grunnuppsetningartöflum eins og sendingarkostnaði og viðskiptatöflum eins og söluhaus og línum.  

> [!NOTE]  
>   Vinna með stillingarpakka er ítarleg virkni og við mælum með að þú hafir samband við kerfisstjórann þinn. Nánari upplýsingar eru í [Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Unnið með gögn í Excel
Þegar sjálfgefinn grunnstillingarpakki er fluttur út í Excel inniheldur vinnubókin sem búin er til vinnublað fyrir hverja töflu í pakkanum. Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel. Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk. Til dæmis, bætið við auðu vinnublaði og afritið eldri gögnin á það. Búið því næst til Excel-formúlu til að varpa gögnum í umbreytingarvinnublaðinu á milli reitanna í útflutta vinnublaðinu og eldri gögnum viðskiptamanns. Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.  

> [!IMPORTANT]  
>  Ekki breyta dálkum í vinnublöðunum. Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Ekki er hægt að flytja út/flytja inn svæði af gerðinni Blob með Excel.

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
-   Almenn Færslubókarlína
-   Birgðabókarlína
-   Bókunarflokkur viðskm.
-   Bókunarflokkur lánardr.
-   Birgðabókunarflokkur
-   Mælieining
-   Almenn Viðskiptabókunarflokkur
-   Almenn Afurðarbókunarflokkur
-   Almennur bókunargrunnur
-   Umsjónarsvæði
-   Vöruflokkur
-   Söluverð
-   Innkaupsverð

## <a name="see-also"></a>Sjá einnig
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks gagnaflutningur](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Gagnafærsla](ui-extensions-dynamicsgp-data-migration.md)  
[Flytja inn margar vörumyndir](inventory-how-import-item-pictures.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
