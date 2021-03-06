---
title: Stofna og keyra runuvinnslu | Microsoft Docs
description: Þú keyrir runuvinnslu til að vinna gögn og uppfæra upplýsingar, til dæmis að framkvæma tímabundnar bókhaldsaðgerðir eða útreikninga.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 05b65f5b001259fff25d0f59dfc6267d9ee00c7f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782254"
---
# <a name="run-batch-jobs-and-xmlports"></a>Keyra runuvinnslur og XMLports
Keyrsla er forritabútur sem vinnur úr gögnum í einni keyrslu líkt og keyrslan **Leiðrétta gengi**. Til eru runuvinnslur sem framkvæma reikningstímabilsaðgerðir eins og lokun rekstrarreiknings í lok reikningsárs. Margar keyrslur vinna útreikningsvinnu, svo sem útreikning á vöxtum, leiðréttingu á gengi og útreikning á einingaverði.

Keyrslu svipar til skýrslu fyrir utan það að keyrslan nýtir útkomuna til að uppfæra upplýsingar beint, án þess að prenta niðurstöðurnar.

Hægt er að tímasetja hvenær runuvinnsla er keyrð. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Til að keyra keyrslu
1. Til að opna beiðnisíðu fyrir viðkomandi runuvinnslu velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn heiti runuvinnslunnar og velur síðan tengda tengilinn.
2. Ef flýtiflipinn **Valkostir** er í boði fyrir runuvinnsluna er fyllt í reitina til að tilgreina hvað runuvinnslan á að gera.
3. Á síðunni kann að vera einn eða fleiri flýtiflipar með afmörkunum sem hægt er að nota til að takmarka hvaða gögn eru innifalin í keyrslunni. Skilyrði eru sett á ráðlagðar afmarkanir eða fleiri afmörkunum bætt við.
4. Veldu hnappinn **Í lagi** til að hefja keyrsluna.

## <a name="see-also"></a>Sjá einnig
[Röðun, leit og síun í listum](ui-enter-criteria-filters.md)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]