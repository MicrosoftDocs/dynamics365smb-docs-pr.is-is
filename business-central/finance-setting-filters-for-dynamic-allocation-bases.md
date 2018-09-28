---
title: "Uppsetning afmarkanir fyrir kvika úthlutunargrunnar | Microsoft Docs"
description: "Kvika úthlutunaraðferðin byggist á breytanlegum gildum. Til dæmis fjöldi starfsmenn í kostnaðarstöð eða seldar vörur af kostnaðarhlut á tilteknu tímabili. Níu forskilgreindir úthlutunargrunnar og tólf kvik dagsetningarsvið eru í boði. Mismunandi afmarkanir eru settar á grundvelli úthlutunargrunns."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ca8e7008c2bfe4a9abeb9d9b7b467a38e2c1971
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

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
 [Dæmi: Skilgreining kvikrar úthlutunar á grundvelli seldra vara](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Setja upp uppruna og markhópa úthlutanna](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md)

