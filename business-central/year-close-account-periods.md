---
title: Loka fjárhagstímabilum fyrir fjárhagsár
description: Þessi grein lýsir því hvernig skal loka fjárhagstímabilum sem mynda fjárhagsárið fyrir árslokalokun.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/25/2021
ms.author: jswymer
ms.openlocfilehash: 5f668104fe6b0bbd9dbbf9295034547e298df916
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435999"
---
# <a name="close-accounting-periods"></a>Loka fjárhagstímabilum
Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í.

## <a name="to-close-accounting-periods"></a>Fjárhagstímabilum lokað:
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagstímabil** og velja síðan viðkomandi tengil.
2. Á síðunni **Fjárhagstímabil** skal velja aðgerðina **Loka ári**.

    Ef fleiri en eitt reikningsár er opið elsta er að elsta sjálfkrafa valið til að vera lokað. Það birtir boð með árinu sem á að loka þar sem er útskýrt hvað gerist ef árinu er lokað.
3. Til að loka árinu skal velja hnappinn **Já**.

Reikningsárið er lokað og reitirnir **Lokað** og **Dags. læst** fyrir öll tímabil á árinu eru valdir. Ekki er lengur hægt að opna reikningsárið eða fjarlægja gátmerkið í reitunum **Læst** eða **Dags. læst**.

> [!NOTE]  
>   Ekki er hægt að loka reikningsári fyrr en nýtt hefur verið stofnað. Bent er á að þegar fjárhagssári hefur verið lokað er ekki hægt að breyta upphafsdagsetningu næsta fjárhagsárs.

Enda þótt reikningsári hafi verið lokað er enn hægt að bóka fjárhagsfærslur á það. Þegar það er gert eru færslurnar merktar sem bókaðar á lokað reikningsár og reiturinn **seinfærsla** verður valinn.

Þegar reikningsári hefur verið lokað verður að loka reikningum á rekstrarreikningi og færa ársniðurstöður yfir á reikning á efnahagsreikningi. Hægt er að endurtaka þetta í hvert sinn sem lokaða reikningsárið er bókað.

## <a name="see-also"></a>Sjá einnig

[Bókum lokað](year-close-books.md)  
[Bóka lokafærslu ársloka](year-how-post-year-end-close-entry.md)  
[Unnið með fjárhagstímabil og fjárhagsár](finance-accounting-periods-and-fiscal-years.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]