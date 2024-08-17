---
title: Bókum lokað
description: Kynntu þér ferlið þegar bókum er lokað fyrir fjárhagsárið eða tímabilið og hvað gerist eftir að þú lokar við enda árs.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Bókum lokað
Þegar búið er að ganga úr skugga um að allir reikningar séu uppfærðir og búið er að úthluta kostnaði og tekjum, má loka bókunum fyrir reikningsárið eða tímabilið.

Það er ekki nauðsynlegt að loka ári en það gerir það auðveldar notendum að nýta þá hentugu afmörkunarvalkosti sem eru í boði. Ekki þarf að óttast að missa færslugögn þegar lokað er því allar upplýsingar eru geymdar, einnig eftir að árinu hefur verið lokað.

## Lokunarbókarferli
Ferli þess að loka bókum felur í sér þessi aðalverk:

1. Lokun reikningstímabilsins.

    Reikningsár er skilgreint sem eitt eða fleiri opin tímabil á síðunni **Reikningstímabil**. Venjulegt reikningsár inniheldur 12 tímabil sem er einn mánuður hvert, en einnig er hægt að velja aðra aðferð við að skilgreina árið.

    Nánari upplýsingar sjá [Loka fjárhagstímabilum](year-close-account-periods.md).
2. Skráning á færslum fyrra árs.

    Þegar reikningsári er lokað þarf að færa inn fjölda stjórnunaraðgerða (eins og fyrirframgreiddar og uppsafnaðar vörur). Slíkar aðgerðir kallast leiðréttingar á færslum. Engar sérstakar reglur gilda um bókun þessara færslna og gátmerki er í reitnum **Færsla** (líkt og aðrar færslur) ef þær eru bókaðar á dagsetningu í lokuðu reikningsári. Enda þótt reikningsári hafi verið lokað er enn hægt að bóka fjárhagsfærslur á það.
3. Flytja færslur af rekstrarreikningi yfir á efnahagsreikning.

    Þegar reikningsári er lokað og allar seinfærslur bókaðar þarf að loka rekstrarreikningum og nettótekjur ársins færðar yfir á reikning undir eigið fé á efnahagsreikningi. Notið keyrsluna Loka efnahagsreikningi í þessum tilgangi. Keyrslan vinnur úr öllum fjárhagsreikningum af gerðinni Rekstrarreikningar og býr til færslur sem bakfærir stöðu þeirra. Færslurnar eru settar í færslubók þar sem má bóka þær. Keyrslan bókar þær ekki sjálfkrafa nema þegar annar skýrslugjaldmiðill er notaður. Þegar annar skýrslugjaldmiðill er notaður, bókar keyrslan beint í færslubókina.

    Nánari upplýsingar, sjá [Loka rekstrarreikningi](year-close-income-statement.md).
4. Bókun lokafærslu árslokareiknings ásamt jöfnunarfærslum eigin fjár.

    Þegar runuvinnslunni Loka rekstrarreikningi er lokið eru færslurnar sem voru myndaðar í verkinu bókaðar. Ef ekki var tilgreindur framlegðarreikningur í keyrslunni er færð inn ein lína með mótfærslu sem bókar nettótekjur á réttan fjárhagur reikning undir eigið fé á efnahagsreikningi. Bókið síðan færslubókina.

    Nánari upplýsingar, sjá [Bóka lokunarfærslu](year-how-post-year-end-close-entry.md).

## Hvað gerist þegar þú lokar

Þegar reikningum er lokað í lok árs færir kerfið hagnað úr reiknuðum hagnaði yfir á reikninginn Óráðstafað eigið fé. Kerfið merkir einnig reikningsárið sem „lokað“ og allar síðari færslur í lokaða árinu sem „færslur fyrra árs“.

Kerfið býr þá til lokunarfærslu en bókar færsluna ekki sjálfkrafa. Notandinn hefur tækifæri á að mótfæra eiginfjárreikningsfærslu eða færslur sem gerir notandanum kleift að ákveða hvernig lokunarfærslunni er úthlutað. Til dæmis ef fyrirtækið er með margar deildir, er hægt að láta kerfið búa til eina lokunarfærslu fyrir allar deildir, og þá er hægt að mótfæra færslu fyrir eigin fé hverrar deildar.

Hægt er að bóka á fyrra reikningsár jafnvel eftir lokun rekstrarreiknings ef keyrslan Loka rekstrarreikningi er keyrð aftur síðar.

## Sjá einnig .

[Vinna við reikningstímabil og reikningsár](finance-accounting-periods-and-fiscal-years.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]