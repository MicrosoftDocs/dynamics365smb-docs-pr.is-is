---
title: Bóka færslu árslokaloka
description: 'Lýsir því hvernig skal opna færslubókina sem þú tilgreindir í runuvinnslunni Loka rekstrarreikningi, og svo endurskoða og bóka lokafærslu ársloka.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: 100
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="post-the-year-end-closing-entry"></a>Bóka færslu árslokaloka

Eftir að runuvinnslan **Loka rekstrarreikningi** hefur verið notuð til að mynda færslu eða færslur fyrir lokun í árslok verður að opna færslubókina sem var tilgreind í runuvinnslunni,  og fara yfir og bóka færslurnar.  

> [!TIP]
> Hægt er að velja að loka eða ekki loka reikningstímabilum og fjárhagsárum í [!INCLUDE [prod_short](includes/prod_short.md)], allt eftir verkferlum fyrirtækisins. Eftirfarandi ferli gerir ráð fyrir að fjárhagsárinu hafi verið lokað með valkostinum *Reikningstímabil*, að lokunarfærsla ársloka hafi verið búin til með runuvinnslunni **Loka rekstrarreikningi** og að nú sé hægt að bóka lokunarfærslu í árslok ásamt jöfnun á færslum á lykli eigin fjár. Fyrirtækið getur valið að vinna á annan hátt, svo sem með því að bóka lokunarfærslu árslokanna sem hluta af lokun fjárhagsársins.

## <a name="to-post-the-year-end-closing-entry"></a>Til að bóka lokunarfærslu ársloka

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.
2. Á síðunni **Færslubækur** í reitnum **Heiti** keyrslu er valin keyrslan sem inniheldur lokunarfærslurnar.
3. Farið er yfir færslurnar.
4. Til að bóka færslubókina er valið aðgerðin **bóka**.

> [!NOTE]  
> Greinist villa birtast villuboð. Ef bókunin heppnast eru bókaðar færslur fjarlægðar úr færslubókinni. Þegar færsla hefur verið bókuð er hún bókuð á alla rekstrarreikninga til að staðan verði núll, og útkoma ársins er færð á efnahagsreikning.

## <a name="see-also"></a>Sjá einnig .

[Fjárhagstímabilum lokað](year-close-account-periods.md)    
[Bækur lokað](year-close-books.md)    
[Loka rekstrarreikningi](year-close-income-statement.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
