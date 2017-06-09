---
title: "Hvernig á að loka Fjárhagstímabilum | Microsoft Docs"
description: "Útskýrir Hvernig á að loka Fjárhagstímabilum"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 69bea225084f239523c4ed67471b52ad91e914d9
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-close-accounting-periods"></a>Hvernig á að loka Fjárhagstímabilum
Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í.

## <a name="to-close-accounting-periods"></a>Fjárhagstímabilum lokað:
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Fjárhagstímabil**, og velja síðan viðeigandi tengil.
2. Í glugganum **Reikningstímabil ** skal velja **loka ári** aðgerðina.

    Ef fleiri en eitt reikningsár er opið elsta er að elsta sjálfkrafa valið til að vera lokað. Það birtir boð með árinu sem á að loka þar sem er útskýrt hvað gerist ef árinu er lokað.
3. Til að loka árinu skal velja hnappinn **Já**.

Reikningsárið er lokað og reitirnir **Lokað** og **Dags. læst** fyrir öll tímabil á árinu eru valdir. Ekki er lengur hægt að opna reikningsárið eða fjarlægja gátmerkið í reitunum **Læst** eða **Dags. læst**.

**Athugasemd**: Ekki er hægt að loka reikningsári fyrr en nýtt hefur verið stofnað. Bent er á að þegar fjárhagssári hefur verið lokað er ekki hægt að breyta upphafsdagsetningu næsta fjárhagsárs.

Enda þótt reikningsári hafi verið lokað er enn hægt að bóka fjárhagsfærslur á það. Þegar það er gert eru færslurnar merktar sem bókaðar á lokað reikningsár og reiturinn **seinfærsla** verður valinn.

Þegar reikningsári hefur verið lokað verður að loka reikningum á rekstrarreikningi og færa ársniðurstöður yfir á reikning á efnahagsreikningi. Hægt er að endurtaka þetta í hvert sinn sem lokaða reikningsárið er bókað.

## <a name="see-also"></a>Sjá einnig
[Bókum lokað](year-close-books.md)  
[Hvernig á að bóka lokafærslu árslokareiknings](year-how-post-year-end-close-entry.md)  
[Hvernig á að opna Nýtt reikningsár](finance-how-open-new-fiscal-year.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

