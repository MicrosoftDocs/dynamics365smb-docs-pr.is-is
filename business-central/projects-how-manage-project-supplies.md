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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 78a11b0c20f8ef6c1c190f38cc5dcfcee918c8e2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191236"
---
# <a name="manage-job-supplies"></a>Stjórna verkbirgðum
Það er mikilvægur og óaðskiljanlegur hluti af framkvæmd allra verka að hafa umsjón með framboði á vöru, þjónustu og útgjöldum. Nota má birgðamagn eða gera verktengd innkaup með innkaupapöntunum og/eða innkaupareikningum. Sem dæmi má nefna þjónustuverk á tölvu sem krefst þess að nýr diskur sé keyptur. Þá er búinn til innkaupareikningur til kaupa á nýjum diski og verkið, sem nota á diskinn í, er skráð.

Ef innkaupaferlið krefst þess ekki að efnisleg aðgerð sé skráð sérstaklega er hægt að setja innkaup á síðuna **Fjárhagsbók verks**. Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Að kaupa vörur eða þjónustu fyrir verk
Eftirfarandi ferli sýnir hvernig á að nota innkaupareikning til að kaupa vörur fyrir verk. Sömu skref eiga við þegar innkaupapöntun er notuð.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Í reitunum **Verk nr.** og **Verkhluti nr.** eru valdar upplýsingarnar um verkið sem þú vilt kaupa vörur eða þjónustu fyrir. Notaðu **Dálkaval** ef svæðið er ekki sýnilegt. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

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
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
