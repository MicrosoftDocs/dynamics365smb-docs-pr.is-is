---
title: Loka rekstrarreikningum | Microsoft Docs
description: Við lok árs, er nauðsynlegt að keyra runuvinnsluna Loka rekstrarreikningi til að loka reikningstímabilunum sem mynda fjárhagsárið.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 20bc194772d1aa0a8caadf0605911d0a214a9ab2
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799772"
---
# <a name="close-income-statement-accounts"></a>Loka rekstrarreikningi
Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í. Til að gera þetta skal keyra Runuvinnslan **Loka rekstrarreikningi** Þetta verk flytur niðurstöðutölur ársins yfir á efnahagsreikning og loka rekstrarreikningum. Það er gert með því að stofna línur í færslubók sem síðan er hægt að bóka.

## <a name="to-run-the-close-income-statement-batch-job"></a>Til að keyra Runuvinnslan Loka rekstrarreikningi
1. Loka reikningsári Reikningsárinu þarf að loka áður en hægt er að setja keyrsluna í gang. Nánari upplýsingar sjá [Loka fjárhagstímabilum](year-close-account-periods.md).
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Loka rekstrarreikningi** og veldu síðan tengda tengilinn.
3. Veldu hnappinn **Í lagi** til að ræsa keyrsluna.

## <a name="about-the-close-income-statement-batch-job"></a>Um Runuvinnslan Loka rekstrarreikningi
Keyrslan vinnur úr öllum fjárhagsreikningum af gerðinni rekstrarreikningar og býr til færslur sem jafna út stöðu þeirra. Þ.e. hver færsla er samtala allra almennra fjárhagsfærslna á reikningnum á reikningsárinu. Þessar nýju færslur eru færðar inn í færslubók þar sem þarf að tilgreina mótreikning og framlegðarreikning í efnahagsreikningi áður en bókað er. Þegar færslubók er bókuð er færsla bókuð á alla rekstrarreikninga til að staðan verði núll og um leið er útkoma ársins færð á efnahagsreikning.

Notandi þarf að bóka þarf bókina sjálfur. Keyrslan bókar færslurnar ekki sjálfkrafa, nema þegar annar skýrslugjaldmiðill er notaður. Þegar annar skýrslugjaldmiðill er notaður, bókar keyrslan beint í færslubókina.

Dagsetningin í línunum sem bætast í færslubókina í keyrslunni verður alltaf lokadagsetning reikningsársins. Lokadagsetningin er hugsuð dagsetning milli síðustu dagsetningar reikningsársins og fyrstu dagsetningar á nýju ári. Kosturinn við að bóka á lokadagsetningu er sá að þá helst rétt staða fyrir venjulegar dagsetningar reikningsársins.

Keyrsluna **Loka rekstrareikningi** má nota mörgum sinnum. Hægt er að bóka á fyrra reikningsár jafnvel eftir lokun rekstrarreiknings ef keyrslan er keyrð aftur.

## <a name="see-also"></a>Sjá einnig
[Bókum lokað](year-close-books.md)  
[Bóka lokafærslu ársloka](year-how-post-year-end-close-entry.md)  
[Opna nýtt reikningsár](finance-how-open-new-fiscal-year.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
