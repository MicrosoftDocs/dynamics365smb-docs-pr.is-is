---
title: Keyra verk í bakgrunni og endurtekið
description: Grunnstilltu samstillingu gagna á milli Business Central og Shopify í bakgrunni.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 4a67f6fc58fb8b158563ce58baab55e7fda2ccb1
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728600"
---
# <a name="run-tasks-in-the-background"></a>Keyra verk í bakgrunni

Það er skilvirkt að keyra sum verkefni samtímis og á sjálfvirkan hátt. Þú getur framkvæmt slík verk í bakgrunni og getur einnig sett áætlun um hvenær þú vilt að þessi verk keyri sjálfkrafa. Til að keyra verk í bakgrunni eru tvær stillingar studdar:

- Verk sem ræst eru handvirkt eru tímasett strax í gegnum **Verkraðarfærslur**.
- Endurtekin verk eru tímasett í **Verkraðarfærslur**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Keyra verk í bakgrunni fyrir tiltekna verslun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn nafn **Shopify verslunar** og veldu heiti verslunar af listanum.
2. Veljið verslunina þar sem á að samtilla vörur til að opna síðuna **Shopify verslunarspjald**.
3. Virkjaðu **Leyfa samstillingar í bakgrunni**.

Núna, þegar samstillingaraðgerð er ræst, í stað þess að verk keyri í forgrunni, biður hún þig um að bíða. Þegar þessu lokið geturðu farið yfir í næstu aðgerð. Verkið er búið til sem **Verkraðarfærsla** og hefst strax á ekki útilokandi hátt.

## <a name="to-schedule-recurring-tasks"></a>Að tímasetja endurtekin verk

Þú getur tímasett eftirfarandi endurteknar aðgerðir sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar um tímasetningu verka er að finna í [Verkröð](../admin-job-queues-schedule-tasks.md).

|Verkefni|Hlutur|
|------|------------|
|**Samstilla pantanir frá Shopify**|Skýrsla 30104 Samstilla pantanir frá Shopify|
|**Vinna úr Shopify pöntunum**|Skýrsla 30103 Shopify stofna sölupantanir|
|**Samstilla sendingar við Shopify**|Skýrsla 30109 Samstilla sendingu við Shopify|
|**Samstilla vörur og/eða verð**|Skýrsla 30108 Shopify samstilla vörur|
|**Samstilla birgðir**|Skýrsla 30102 Samstilla birgðir við Shopify|
|**Samstilla myndir**|Skýrsla 30107 Shopify samstilla myndir|
|**Samstilla viðskiptamenn**|Skýrsla 30100 Shopify samstilla viðskiptamenn|
|**Samstilla greiðslur**|Skýrsla 30105 Shopify samstilla greiðslur|

> [!NOTE]
> Sumar einingar gætu verið uppfærðar af nokkrum verkum, t.d. þegar þú flytur inn pantanir, eftir því hver stillingin er í **Shopify verslunarspjald**, kerfið gæti einnig flutt inn og uppfært viðskiptamanna- og/eða framleiðslugögn. Mundu að nota sama verkraðarflokkinn til að forðast árekstra.

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
