---
title: Verk keyrð í bakgrunni
description: Skilgreinið samstillingu gagna milli Viðskiptamiðseðla og Shopify bakgrunns.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: f353edb4c505fd7b3eb498392abca3ce481b6009
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768096"
---
# <a name="run-tasks-in-the-background"></a>Verk keyrð í bakgrunni

Það er duglegt að keyra sum verkefni samtímis og á sjálfvirkan hátt. Hægt er að framkvæma slík verk í bakgrunni og einnig er hægt að setja áætlun þegar þau verkefni eiga að keyra sjálfkrafa. Til að keyra verkefni í bakgrunni eru tveir mátar studdir:

- Verk ræst handvirkt er raðað strax í gegnum **Vinnsluraðarfærslur**
- Endurteknum verkum er raðað í færslum í **vinnslu**

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Verk keyrð í bakgrunni fyrir sérstaka búð

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn heiti **Shopify verkstæðis**, og veldu verkstæðisnafnið af listanum.
2. Veljið verslunina þar sem á að samstilla vörur til að opna **Shopify spjald** -síðu verkstæðis.
3. Leyfa Samvirkjun **bakgrunns virkt**.

Nú, þegar samstillingaraðgerðin er ræst, í stað þess að verk sé keyrt í forgrunni, biður það þig að bíða. Þegar því er lokið er hægt að halda áfram í næstu aðgerð. Verkið er stofnað sem **Verkraðarafærsla** og hefst samstundis á óhindraan hátt.

## <a name="to-schedule-recurring-tasks"></a>Áætlun endurtekinna verka tímasett

Hægt er að áætla eftirfarandi endurtekna verkþætti þannig að hann sé framkvæmdur á sjálfvirkan hátt. Nánari upplýsingar um röðunarverk er að finna [í vinnslubiðröð](../admin-job-queues-schedule-tasks.md).

|Verkefni|Hlutur|
|------|------------|
|**Samstilla pantanir frá Shopify**|Skýrsla 30104 Samkeyrsla pantana frá Shopify|
|**Vinna Shopify pantanir**|Skýrsla 30103 Shopify Stofna sölupantanir|
|**Samstilla sendingar í Shopify**|Skýrsla 30109 Samkeyrsla sendinga til Shopify|
|**Samstilla vörur og/eða verð**|Skýrsla 30108 Shopify Samkeyrsla afurða|
|**Samstilla birgðir**|Skýrsla 30102 Samkeyrsla Kauphallarinnar að Shopify|
|**Samstilla myndir**|Skýrsla 30107 Shopify samkeyrðir myndir|
|**Viðskiptavinir samkaupa**|Skýrsla 30100 Shopify Samkeyrsla viðskiptavina|
|**Samstilla greiðslur**|Skýrsla 30105 Shopify samkeyrslur greiðslur|

## <a name="see-also"></a>Sjá einnig

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
