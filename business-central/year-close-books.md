---
title: Yfirlit yfir verkhluta lokun bóka
description: Kynntu þér ferlið þegar bókum er lokað fyrir fjárhagsárið eða tímabilið og hvað gerist eftir að þú lokar við enda árs.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="closing-the-books"></a>Bókum lokað
Þegar búið er að ganga úr skugga um að allir reikningar séu uppfærðir og búið er að úthluta kostnaði og tekjum, má loka bókunum fyrir reikningsárið eða tímabilið.

Það er ekki nauðsynlegt að loka ári en sé það gert verður auðveldara að nota þær hentugu afmarkanir sem eru í boði. Ekki þarf að óttast að missa færslugögn þegar lokað er því allar upplýsingar eru geymdar, einnig eftir að árinu hefur verið lokað.

## <a name="closing-book-process"></a>Ferli þess að loka bókum
Ferli þess að loka bókum felur í sér þessi aðalverk:

1. Lokun reikningstímabilsins.

    Reikningsár er skilgreint sem eitt eða fleiri opin tímabil á síðunni **Reikningstímabil**. Venjulegt reikningsár inniheldur 12 tímabil sem er einn mánuður hvert, en einnig er hægt að velja aðra aðferð við að skilgreina árið.

    Nánari upplýsingar sjá [Loka fjárhagstímabilum](year-close-account-periods.md).
2. Skráning á færslum fyrra árs.

    Þegar reikningsári er lokað þarf að færa inn fjölda stjórnunaraðgerða (eins og fyrirframgreiddar og uppsafnaðar vörur). Slíkar aðgerðir kallast leiðréttingar á færslum. Engar sérstakar reglur gilda um bókanir slíkra færslna og innihalda þær (líkt og aðrar færslur) gátmerkisreitinn **Seinfærsla** ef þær eru bókaðar á dagsetningu í lokuðu reikningsári. Enda þótt reikningsári hafi verið lokað er enn hægt að bóka fjárhagsfærslur á það.
3. Flytja færslur af rekstrarreikningi yfir á efnahagsreikning.

    Þegar reikningsári er lokað og allar seinfærslur bókaðar þarf að loka rekstrarreikningum og nettótekjur ársins færðar yfir á reikning undir eigið fé á efnahagsreikningi. Notið keyrsluna Loka efnahagsreikningi í þessum tilgangi. Keyrslan vinnur úr öllum fjárhagsreikningum af gerðinni Rekstrarreikningar og býr til færslur sem bakfærir stöðu þeirra. Færslurnar eru settar í færslubók þar sem má bóka þær. Keyrslan bókar þær ekki sjálfkrafa, nema þegar annar skýrslugjaldmiðill er notaður. Þegar annar skýrslugjaldmiðill er notaður, bókar keyrslan beint í færslubókina.

    Nánari upplýsingar, sjá [Loka rekstrarreikningi](year-close-income-statement.md).
4. Bókun lokafærslu árslokareiknings ásamt jöfnunarfærslum eigin fjár.

    Þegar runuvinnslunni Loka rekstrarreikningi er lokið eru færslurnar sem voru myndaðar í verkinu bókaðar. Ef ekki var tilgreindur reikningur óráðstafaðs eigin fjár í keyrslunni, færið inn eina línu með mótfærslu sem bókar nettótekjur í rétta færslubók undir eigið fé á efnahagsreikningi. Bókið síðan færslubókina.

    Nánari upplýsingar, sjá [Bóka lokunarfærslu](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Hvað gerist þegar lokað er
Þegar reikningum er lokað í lok árs færir kerfið hagnað úr reiknuðum hagnaði yfir á reikninginn Óráðstafað eigið fé. Kerfið merkir einnig reikningsárið sem „lokað“ og allar síðari færslur í lokaða árinu sem „færslur fyrra árs“.

Kerfið býr svo til lokunarfærslu, en bókar færsluna ekki sjálfkrafa. Hægt er að gera mótfærslu eða -færslur fyrir eigin fé sem gerir kleift að ákveða hvernig lokunarfærslunni er úthlutað. Til dæmis ef fyrirtækið er með margar deildir, er hægt að láta kerfið búa til eina lokunarfærslu fyrir allar deildir, og þá er hægt að mótfæra færslu fyrir eigin fé hverrar deildar.

Hægt er að bóka á fyrra reikningsár jafnvel eftir lokun rekstrarreiknings ef keyrslan Loka rekstrarreikningi er keyrð aftur síðar.

## <a name="see-also"></a>Sjá einnig

[Unnið með fjárhagstímabil og fjárhagsár](finance-accounting-periods-and-fiscal-years.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
