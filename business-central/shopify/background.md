---
title: Verk keyrð í bakgrunni og endurkoma
description: Skilgreinið samstillingu gagna milli Viðskiptamiðseðla og Shopify bakgrunns.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 4a67f6fc58fb8b158563ce58baab55e7fda2ccb1
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728600"
---
# <a name="run-tasks-in-the-background"></a>Verk keyrð í bakgrunni

Það er duglegt að keyra sum verkefni samtímis og á sjálfvirkan hátt. Hægt er að framkvæma slík verk í bakgrunni og einnig er hægt að setja áætlun þegar þau verkefni eiga að keyra sjálfkrafa. Til að keyra verkefni í bakgrunni eru tveir mátar studdir:

- Ræstar verkfærslum er raðað strax í gegnum **vinnsluraðarfærslur**.
- Endurteknum verkum er raðað í **Verkraðarafærslur**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Verk keyrð í bakgrunni fyrir sérstaka búð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn heiti **Shopify verkstæðis**, og veldu verkstæðisnafnið af listanum.
2. Valið er verslunin sem á að samstilla vörur til til að opna **Shopify Vinnukortasíðuna**.
3. Gera Samað **-víxlgerð** bakgrunns virka.

Nú, þegar samstillingaraðgerðin er ræst, í stað þess að verk sé keyrt í forgrunni, biður það þig að bíða. Þegar því er lokið er hægt að halda áfram í næstu aðgerð. Verkið er stofnað sem **Verkraðarafærsla** og hefst samstundis með óhindraðra hætti.

## <a name="to-schedule-recurring-tasks"></a>Áætlun endurtekinna verka tímasett

Hægt er að áætla eftirfarandi endurtekna verkþætti þannig að hann sé framkvæmdur á sjálfvirkan hátt. Frekari upplýsingar um röðunarverk í [vinnsluröð](../admin-job-queues-schedule-tasks.md).

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

> [!NOTE]
> Nokkur atriði gætu verið uppfærð með nokkrum verkum, til dæmis þegar pantanir eru fluttar inn, eftir stillingu **Shopify verkstæðiskortsins**, getur kerfið einnig flutt inn og uppfært viðskiptamanna-og/eða afurðargögn. Munið að nota sama vinnsluraðarflokk til að forðast árekstra.

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
