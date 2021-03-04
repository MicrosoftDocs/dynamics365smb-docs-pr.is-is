---
title: Stofna og keyra runuvinnslu | Microsoft Docs
description: Þú keyrir runuvinnslu til að vinna gögn og uppfæra upplýsingar, til dæmis að framkvæma tímabundnar bókhaldsaðgerðir eða útreikninga.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 04ae13561f44d544d38b04e3a881a0e707b441b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760518"
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