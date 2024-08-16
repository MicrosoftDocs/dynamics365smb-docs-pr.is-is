---
title: Loka rekstrarreikningi
description: 'Við lok árs, er nauðsynlegt að keyra runuvinnsluna Loka rekstrarreikningi til að loka reikningstímabilunum sem mynda fjárhagsárið.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Loka rekstrarreikningi

Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í. Til að gera þetta skal keyra Runuvinnslan **Loka rekstrarreikningi** Þetta verk flytur niðurstöðutölur ársins yfir á efnahagsreikning og loka rekstrarreikningum. Það er gert með því að stofna línur í færslubók sem síðan er hægt að bóka.

## Til að keyra Runuvinnslan Loka rekstrarreikningi

1. Loka reikningsári Reikningsárinu þarf að loka áður en hægt er að setja keyrsluna í gang. Nánari upplýsingar sjá [Loka fjárhagstímabilum](year-close-account-periods.md).
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Loka rekstrarreikningi** og velja síðan viðkomandi tengil.
3. Veldu hnappinn **Í lagi** til að ræsa keyrsluna.

## Um keyrsluna Loka rekstrarreikningi

Keyrslan vinnur úr öllum fjárhagsreikningum af gerðinni rekstrarreikningar og býr til færslur sem jafna út stöðu þeirra. Þ.e. hver færsla er samtala allra almennra fjárhagsfærslna á reikningnum á reikningsárinu. Þessar nýju færslur eru færðar inn í færslubók þar sem þarf að tilgreina mótreikning og framlegðarreikning í efnahagsreikningi áður en bókað er. Þegar færslubók er bókuð er færsla bókuð á alla rekstrarreikninga til að staðan verði núll og um leið er útkoma ársins færð á efnahagsreikning.

Notandi þarf að bóka þarf bókina sjálfur. Keyrslan bókar færslurnar ekki sjálfkrafa nema þegar annar skýrslugjaldmiðill er notaður. Þegar annar skýrslugjaldmiðill er notaður, bókar keyrslan beint í færslubókina.

Dagsetningin í línunum sem bætast í færslubókina í keyrslunni verður alltaf lokadagsetning reikningsársins. Lokadagsetningin er hugsuð dagsetning milli síðustu dagsetningar reikningsársins og fyrstu dagsetningar á nýju ári. Kosturinn við að bóka á lokadagsetningu er sá að þá helst rétt staða fyrir venjulegar dagsetningar reikningsársins.

Keyrsluna **Loka rekstrareikningi** má nota mörgum sinnum. Hægt er að bóka á fyrra reikningsár jafnvel eftir lokun rekstrarreiknings ef keyrslan er keyrð aftur.

## Sjá einnig .

[Bækur lokað](year-close-books.md)    
[Bóka lokunarfærslu ársloka](year-how-post-year-end-close-entry.md)    
[Vinna við reikningstímabil og reikningsár](finance-accounting-periods-and-fiscal-years.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]