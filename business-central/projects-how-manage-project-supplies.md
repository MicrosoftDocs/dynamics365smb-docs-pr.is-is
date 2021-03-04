---
title: Innkaup á vörum og þjónustu fyrir verk og stjórnun verkbirgða| Microsoft Docs
description: Lýsir því hvernig á að hafa umsjón með verkbirgðum og innkaupum á efni og þjónustu í verkum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7b3abf9ae0cb07e6b3e79fc21ee10467f4f611b6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748944"
---
# <a name="manage-job-supplies"></a>Stjórna verkbirgðum
Það er mikilvægur og óaðskiljanlegur hluti af framkvæmd allra verka að hafa umsjón með framboði á vöru, þjónustu og útgjöldum. Nota má birgðamagn eða gera verktengd innkaup með innkaupapöntunum og/eða innkaupareikningum. Sem dæmi má nefna þjónustuverk á tölvu sem krefst þess að nýr diskur sé keyptur. Þá er búinn til innkaupareikningur til kaupa á nýjum diski og verkið, sem nota á diskinn í, er skráð.

Ef innkaupaferlið krefst þess ekki að efnisleg aðgerð sé skráð sérstaklega er hægt að setja innkaup á síðuna **Fjárhagsbók verks**. Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Að kaupa vörur eða þjónustu fyrir verk
Eftirfarandi ferli sýnir hvernig á að nota innkaupareikning til að kaupa vörur fyrir verk. Sömu skref eiga við þegar innkaupapöntun er notuð.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Í reitunum **Verk nr.** og **Verkhluti nr.** eru valdar upplýsingarnar um verkið sem þú vilt kaupa vörur eða þjónustu fyrir. Notið verkfæri sérstillingar ef reitur er ekki sýnilegur. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

    Gildið sem valið er í reitnum **Verklínutegund** skilgreinir hvort búin sé til áætlunarlína þegar notkun vörunnar er bókuð. Ef reiturinn inniheldur **Reikningshæft** eru stofnaðar áætlunarlínur sem eru tilbúnar til að vera reikningsfærðar til viðskiptavinar. Frekari upplýsingar eru í [Reikningsfærsla verka](projects-how-invoice-jobs.md).
4. Valið er **Bóka** aðgerðin.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Til að skoða virði innkaupa fyrir verk
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.
2. Opnið viðeigandi verkspjald.

    Á flýtiflipanum **Verkhlutar** sýnir reiturinn **Óafgreiddar pantanir** útistandandi upphæð í staðbundnum gjaldmiðli fyrir vörur í birgðaskrá og þjónustu á innkaupaskjöl fyrir verkhlutalínuna.  

    Reiturinn **Afh. upph. óreikn.færð** sýnir virði vara sem afhentra vara í innkaupaskjölum sem ekki hafa verið reikningsfærðar enn.  
3. Þegar smellt er í reitinn opnast glugginn **Innkaupalínur**. Á síðunni má sjá upplýsingar úr innkaupapöntuninni, þ.á.m. hvaða vörur eða forði hafa verið móttekin.

## <a name="to-post-a-job-related-expense"></a>Til að bóka verktengdan kostnað
Ef þú verður fyrir óvenjulegum útgjöldum eða útgöldum sökum eins verks, er hægt að nota síðuna **Verk fjárhagsbókar** til að bóka þau beint í viðeigandi verkreikning.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsbækur verks** og veldu síðan tengda tengilinn.  
2. Ný lína er stofnuð og kostnaðarupplýsingar, þar á meðal **Verk nr** og **Verkhluti nr.**, færðar inn í reitina.  
3. Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]