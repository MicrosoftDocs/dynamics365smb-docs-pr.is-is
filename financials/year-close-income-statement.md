---
title: Loka rekstrarreikningum | Microsoft Docs
description: "Við lok árs, er nauðsynlegt að keyra runuvinnsluna Loka rekstrarreikningi til að loka reikningstímabilunum sem mynda fjárhagsárið."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6ddd7b504f6faa856e92c336f889ad08db0b3d8b
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-close-income-statement-accounts"></a>Hvernig á að: Loka rekstrarreikningum
Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í. Til að gera þetta skal keyra Runuvinnslan **Loka rekstrarreikningi** Þetta verk flytur niðurstöðutölur ársins yfir á efnahagsreikning og loka rekstrarreikningum. Það er gert með því að stofna línur í færslubók sem síðan er hægt að bóka.

## <a name="to-run-the-close-income-statement-batch-job"></a>Til að keyra Runuvinnslan Loka rekstrarreikningi
1. Loka reikningsári Reikningsárinu þarf að loka áður en hægt er að setja keyrsluna í gang. Nánari upplýsingar sjá [Hvernig á að: Loka reikningstímabilum](year-close-account-periods.md).
2. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Loka rekstrarreikningi** og velja svo viðeigandi tengil.
3. Veldu hnappinn **Í lagi** til að ræsa keyrsluna.

## <a name="about-the-close-income-statement-batch-job"></a>Um Runuvinnslan Loka rekstrarreikningi
Keyrslan vinnur úr öllum fjárhagsreikningum af gerðinni rekstrarreikningar og býr til færslur sem jafna út stöðu þeirra. Þ.e. hver færsla er samtala allra almennra fjárhagsfærslna á reikningnum á reikningsárinu. Þessar nýju færslur eru færðar inn í færslubók þar sem þarf að tilgreina mótreikning og framlegðarreikning í efnahagsreikningi áður en bókað er. Þegar færslubók er bókuð er færsla bókuð á alla rekstrarreikninga til að staðan verði núll og um leið er útkoma ársins færð á efnahagsreikning.

Notandi þarf að bóka þarf bókina sjálfur. Keyrslan bókar færslurnar ekki sjálfkrafa, nema þegar annar skýrslugjaldmiðill er notaður. Þegar annar skýrslugjaldmiðill er notaður, bókar keyrslan beint í færslubókina.

Dagsetningin í línunum sem bætast í færslubókina í keyrslunni verður alltaf lokadagsetning reikningsársins. Lokadagsetningin er hugsuð dagsetning milli síðustu dagsetningar reikningsársins og fyrstu dagsetningar á nýju ári. Kosturinn við að bóka á lokadagsetningu er sá að þá helst rétt staða fyrir venjulegar dagsetningar reikningsársins.

Keyrsluna **Loka rekstrareikningi** má nota mörgum sinnum. Hægt er að bóka á fyrra reikningsár jafnvel eftir lokun rekstrarreiknings ef keyrslan er keyrð aftur.

## <a name="see-also"></a>Sjá einnig
[Bókum lokað](year-close-books.md)  
[Hvernig á að bóka lokafærslu árslokareiknings](year-how-post-year-end-close-entry.md)  
[Hvernig á að opna Nýtt reikningsár](finance-how-open-new-fiscal-year.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

