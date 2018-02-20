---
title: "Innkaup á vörum og þjónustu fyrir verk og stjórnun verkbirgða| Microsoft Docs"
description: "Lýsir því hvernig á að hafa umsjón með verkbirgðum og innkaupum á efni og þjónustu í verkum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 498a9f7a1b95b5b27ad8cef55c8b558f5f3a718f
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="manage-job-supplies"></a>Stjórna verkbirgðum
Það er mikilvægur og óaðskiljanlegur hluti af framkvæmd allra verka að hafa umsjón með framboði á vöru, þjónustu og útgjöldum. Nota má birgðamagn eða gera verktengd innkaup með innkaupapöntunum og/eða innkaupareikningum. Sem dæmi má nefna þjónustuverk á tölvu sem krefst þess að nýr diskur sé keyptur. Þá er búinn til innkaupareikningur til kaupa á nýjum diski og verkið, sem nota á diskinn í, er skráð.

Ef innkaupavinnslan krefst þess ekki að efnislegu viðskiptin séu skráð sérstaklega er hægt að vinna innkaup í glugganum **Fjárhagsbók verks**. Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Að kaupa vörur eða þjónustu fyrir verk
Eftirfarandi ferli sýnir hvernig á að nota innkaupareikning til að kaupa vörur fyrir verk. Sömu skref eiga við þegar innkaupapöntun er notuð.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Í reitunum **Verk nr.** og **Verkhluti nr.** eru valdar upplýsingarnar um verkið sem þú vilt kaupa vörur eða þjónustu fyrir. Notaðu **Dálkaval** ef svæðið er ekki sýnilegt. Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).

    Gildið sem valið er í reitnum **Verklínutegund** skilgreinir hvort búin sé til áætlunarlína þegar notkun vörunnar er bókuð. Ef reiturinn inniheldur **Reikningshæft** eru stofnaðar áætlunarlínur sem eru tilbúnar til að vera reikningsfærðar til viðskiptavinar. Frekari upplýsingar eru í [Reikningsfærsla verka](projects-how-invoice-jobs.md).
4. Valið er **Bóka** aðgerðin.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Til að skoða virði innkaupa fyrir verk
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.
2. Opnið viðeigandi verkspjald.

    Á flýtiflipanum **Verkhlutar** sýnir reiturinn **Óafgreiddar pantanir** útistandandi upphæð í staðbundnum gjaldmiðli fyrir vörur í birgðaskrá og þjónustu á innkaupaskjöl fyrir verkhlutalínuna.  

    Reiturinn **Afh. upph. óreikn.færð** sýnir virði vara sem afhentra vara í innkaupaskjölum sem ekki hafa verið reikningsfærðar enn.  
3. Veljið annan hvorn reitinn til að opna í glugganum **Innkaupalínur** þar sem hægt er að fara yfir upplýsingar um línur í tengdum innkaupaskjölum, þ.m.t. hvaða vörum eða þjónustu hefur verið tekið við.

## <a name="to-post-a-job-related-expense"></a>Til að bóka verktengdan kostnað
Ef um óeðlileg útgjöld eða einstök útgjöld er að ræða vegna verks er hægt að nota gluggann **Fjárhagsbók verks** til að bóka slíkt beint á reikning viðeigandi verks.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsbækur verks** og velja svo viðeigandi tengil.  
2. Ný lína er stofnuð og kostnaðarupplýsingar, þar á meðal **Verk nr** og **Verkhluti nr.**, færðar inn í reitina.  
3. Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

