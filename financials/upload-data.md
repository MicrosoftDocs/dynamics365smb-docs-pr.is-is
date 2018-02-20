---
title: "Flytja eldri viðskiptagögn inn í Finance and Operations, Business Edition | Microsoft Docs"
description: "Hægt er að flytja gögn fyrir viðskiptamenn, lánardrottna og birgðir, til dæmis úr Excel, QuickBooks, eða Dynamics GP inn í Finance and Operations, Business Edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QuickBooks, transfer, import, migrate, initialize, implement
ms.date: 09/25/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f1339468507efc474c709f35fa04d61ca7e5b9a2
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Innflutningur viðskiptagagna úr öðrum fjárhagskerfum
Þegar notandi skráir sig í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að ákveða að búa til autt fyrirtæki svo hægt sé að hlaða upp eigin gögnum og prófa áfram nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtækið. Það fer eftir því fjárhagskerfi sem fyrirtækið notar í dag hvernig og hvort hægt er að millifæra upplýsingar um viðskiptamenn, lánardrottna, birgðir og bankareikninga.  

Hægt er að ræsa leiðarvísi um uppsetningu með hjálp frá upphafssíðu sem hjálpar til við að flytja viðskiptagögn úr Excel-skrá eða öðrum sniðum. Þær skráategundir sem hægt er að hlaða upp fer eftir viðbótunum sem í boði eru. Til dæmis er hægt að yfirfæra gögn úr QuickBooks vegna þess að [!INCLUDE[d365fin](includes/d365fin_md.md)] felur í sér viðbót sem sér um umbreytingu úr QuickBooks. Ef notandi vill yfirfæra gögn úr öðrum fjárhagskerfum þarf annað hvort að athuga hvort viðbót er í boði fyrir það kerfi eða flytja gögnin inn úr Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]  inniheldur sniðmát fyrir viðskiptamenn, lánardrottna og birgðavörur sem hægt er að nota þegar gögnum er hlaðið upp.  

## <a name="importing-data-from-quickbooks-desktop-quickbooks-online-or-dynamics-gp"></a>Innflutningur gagna úr QuickBooks Desktop, QuickBooks Online eða Dynamics GP
Ef fyrirtækið notar QuickBooks eða Dynamics GP í dag er hægt að flytja út viðeigandi upplýsingar í skrá. Síðan er hægt að opna leiðarvísi um uppsetningu með hjálp til að flytja gögnin.
Ef IFF-skráin inniheldur til dæmis viðskiptamenn og lánardrottna er hægt að ákveða að flytja aðeins gögn viðskiptamanna. Síðan er hægt að flytja aðrar upplýsingar síðar.  

Uppsetning með hjálp hefur valkost um að breyta sjálfgefnum grunnstillingum yfirfærslunnar, en mælt með því að nota aðeins þessa ítaruppsetningu ef notandi er vanur að vinna með gagnagrunnstöflur. Í langflestum fyrirtækjum mun sjálfgefin vörpun frá QuickBook eða Dynamics GP í [!INCLUDE[d365fin](includes/d365fin_md.md)] flytja þær upplýsingar sem notandi þarf á að halda.  

Nánari upplýsingar, sjá [QuickBooks Desktop gagnafærsla](ui-extensions-quickbooks-data-migration.md) [QuickBooks gagnafærsla á netinu](ui-extensions-quickbooks-online-data-migration.md) eða [Dynamics GP gagnafærsla](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="importing-data-from-configuration-packages"></a>Innflutningur gagna úr grunnstillingarpakka
[!INCLUDE[d365fin](includes/d365fin_md.md)]  inniheldur stillingarpakka sem þú getur flutt út í Excel og sett upp gögnin þín þar. Síðan er hægt að flytja aftur inn gögnin úr Excel. Pakkinn samanstendur af 27 töflum, þar með talið aðalgögnum, svo sem viðskiptavinum, söluaðilum, hlutum og reikningum, öðrum grunnuppsetningartöflum eins og sendingarkostnaði og viðskiptatöflum eins og söluhaus og línum.  

> [!NOTE]  
>   Vinna með stillingarpakka er ítarleg virkni og við mælum með að þú hafir samband við kerfisstjórann þinn. Nánari upplýsingar eru í [Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka](across-import-data-configuration-packages.md)  
[QuickBooks Desktop gagnafærsla](ui-extensions-quickbooks-data-migration.md)  
[QuickBooks gagnaflutningur á netinu](ui-extensions-quickbooks-online-data-migration.md)  
[Dynamics GP Gagnafærsla](ui-extensions-dynamicsgp-data-migration.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)   
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

