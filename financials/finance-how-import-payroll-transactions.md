---
title: "Hvernig á að: Flytja inn launafærslur  | Microsoft Docs"
description: "Lýsir hvernig á að flytja launagreiðslur og tengd viðskipti frá launaskráveitanda þínum inn í aðalbókina."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 03/24/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d7ee87a80b4de2bc90086c188e5a53291c52683
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-import-payroll-transactions"></a>Hvernig á að: Flytja inn launafærslur
Fyrir launagreiðslur og tengdar færslur verður að flytja inn og birta fjárhagslegar færslur úr launaveitu í fjárhag. Fyrir þetta þarf fyrst að flytja inn skrá úr launaveitu yfir í gluggann **Færslubók**. Síðan varparðu ytri reikningunum í skránni launagreiðslur á viðeigandi fjárhagsreikninga. Að lokum bókarðu launafærslur samkvæmt reikningsvörpuninni.

**Takið eftir**: Til að nota þessa aðgerð þarf viðbót fyrir innflutning launa að vera uppsett og virkjuð. The Ceridian Payroll og Quickbooks Payroll File Import eftirnafn eru fyrirfram uppsett í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar skoða [Sérstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] Nota viðbætur](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Til að flytja inn launaskrá
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Færslubækur**, og velja síðan viðeigandi tengil.
2. Í viðkomandi færslubókarkeyrslu skal velja **Flytja inn launafærslur**. Uppsetning með hjálp opnast.
3. Fylgdu skrefunum í glugganum **Flytja inn launafærslur**.

    **Ábending**: Þegar ytri launaskrám er varpað í fjárhagsreikningana þína man kerfið þá vörpun næst þegar sömu skýrslur eru fluttar inn. Þetta sparar tíma því ekki þarf að fylla inn svæðið **Reikningnúmer** handvirkt í almennu færslubókinni í hvert sinn sem endurteknar launafærslur eru fluttar inn.   

    Þegar hnappurinn **Í lagi** er valinn í uppsetningu með leiðsögn er glugginn **Almenn færslubók** fullur af línum sem tákna færslurnar sem launaskráin innheldur og búið er að fylla út tilheyrandi lykla í reitunum **Fjárhagsreikningur** í samræmi við þá vörpun sem gerð var í leiðsögninni.
4. Breyta skal eða bóka færslubókarlínur líkt og fyrir allar aðrar færslur í fjárhag. Frekari upplýsingar eru í [hvernig á að: vinna með almenn færslubók](ui-work-general-journals.md).   

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] Notkun viðbóta] (ui-extensions.md)  
[Hvernig á að: Vinna með almennum færslubókum](ui-work-general-journals.md)  

