---
title: Uppsetning afmarkanir fyrir kvika úthlutunargrunnar | Microsoft Docs
description: Kvika úthlutunaraðferðin byggist á breytanlegum gildum. Til dæmis fjöldi starfsmenn í kostnaðarstöð eða seldar vörur af kostnaðarhlut á tilteknu tímabili. Níu forskilgreindir úthlutunargrunnar og tólf kvik dagsetningarsvið eru í boði. Mismunandi afmarkanir eru settar á grundvelli úthlutunargrunns.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 35f9a542d57bfe27c9a9ee48f4a41af7071cdd47
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241963"
---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Uppsetning afmarkanir fyrir Kvik úthlutunargrunnar.
Kvika úthlutunaraðferðin byggist á breytanlegum gildum. Til dæmis fjöldi starfsmenn í kostnaðarstöð eða seldar vörur af kostnaðarhlut á tilteknu tímabili. Níu forskilgreindir úthlutunargrunnar og tólf kvik dagsetningarsvið eru í boði. Mismunandi afmarkanir eru settar á grundvelli úthlutunargrunns.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Uppsetning afmarkanir fyrir Kvik úthlutunargrunnar.  
 Eftirfarandi tafla sýnir hvaða afmarkanir eru mögulegar fyrir mismunandi úthlutunargrunna og hvaða gildi eru leyfileg í reitunum **Nr. afmörkunar** og **Afmörkun hóps**. Ýtið á F1 í reitnum **Kóði gagnaafmörkunar** til að sjá nákvæmari lýsingu.  

|**Grunnur**|**Númersafmörkun**|**Kóti gagnaafmörkunar**|**Afmörkun kostnaðarstaðar**|**Afmörkun kostnaðarhlutar**|**Afmörkun hópa**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Fjárhagsfærslur|Fjárhagsreikningur|Já|Já|Já|Á ekki við|  
|Fjárhagsáætl.færslur|Fjárhagsreikningur|Já|Já|Já|Heiti fjárhagsáætl.|  
|Kostnaðartegundarfærslur|Tegund kostnaðar|Já|Já|Já|Á ekki við|  
|Færslur kostnaðaráætlana|Tegund kostnaðar|Já|Já|Já|Heiti áætlunar|  
|Fjöldi starfsmanna|Á ekki við|Já|Já|Já|Á ekki við|  
|Seldar vörur (magn )|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|  
|Keyptar vörur (magn)|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|  
|Seldar vörur (upphæð )|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|  
|Keyptar vörur (upphæð)|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|  

## <a name="see-also"></a>Sjá einnig  
[Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md)
