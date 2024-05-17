---
title: Loka fjárhagstímabilum fyrir reikningsár
description: Þessi grein lýsir því hvernig skal loka fjárhagstímabilum sem mynda fjárhagsárið fyrir árslokalokun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: '100,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
---
# <a name="close-accounting-periods"></a>Loka fjárhagstímabilum

Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í.

## <a name="to-close-accounting-periods"></a>Fjárhagstímabilum lokað:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagstímabil** og velja síðan viðkomandi tengil.
2. Á síðunni **Fjárhagstímabil** skal velja aðgerðina **Loka ári**.

    Ef fleiri en eitt reikningsár er opið elsta er að elsta sjálfkrafa valið til að vera lokað. Skilaboð bera kennsl á árið sem verður lokað og niðurstöður lokunar þess.
3. Til að loka árinu skal velja hnappinn **Já**.

Reikningsárið er lokað og reitirnir **Lokað** og **Dags. læst** fyrir öll tímabil á árinu eru valdir. Ekki er lengur hægt að opna reikningsárið eða fjarlægja gátmerkið í reitunum **Læst** eða **Dags. læst**.

> [!NOTE]  
> Ekki er hægt að loka reikningsári áður en nýtt er stofnað. Bent er á að eftir að reikningsári hefur verið lokað er ekki hægt að breyta upphafsdagsetningu næsta reikningsárs.

Enda þótt fjárhagsár sé lokað er enn hægt að bóka fjárhagsfærslur á það. Þegar það er gert eru færslurnar merktar sem bókaðar á lokað reikningsár og reiturinn **Fyrra færsla** er valinn.

Þegar reikningsári hefur verið lokað verður að loka reikningum á rekstrarreikningi og færa ársniðurstöður yfir á reikning á efnahagsreikningi. Hægt er að endurtaka þetta í hvert sinn sem lokaða reikningsárið er bókað.

## <a name="see-also"></a>Sjá einnig .

[Bókum lokað](year-close-books.md)  
[Bóka lokafærslu ársloka](year-how-post-year-end-close-entry.md)  
[Unnið með fjárhagstímabil og fjárhagsár](finance-accounting-periods-and-fiscal-years.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
