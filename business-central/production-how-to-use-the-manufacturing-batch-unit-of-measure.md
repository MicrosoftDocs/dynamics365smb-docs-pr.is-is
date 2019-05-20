---
title: Hvernig á að nota mælieiningu framleiðslukeyrslu | Microsoft Docs
description: Ef vara er sett á lager eftir einni mælieiningu en framleidd eftir annarri, verður framleiðslupöntunin að notar mælieiningu framleiðslukeyrslu til að reikna út rétt magn íhluta. Dæmi um útreikning með mælieiningu framleiðslukeyrslu er þegar framleiddur hlutur er merktur á lager í stykkjum en framleiddur í tonnum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 52801c3303a06488416b8b82fac3f761ec0705e7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252390"
---
# <a name="work-with-manufacturing-batch-units-of-measure"></a>Vinna með mælieiningu framleiðslukeyrslu
Ef vara er sett á lager eftir einni mælieiningu en framleidd eftir annarri er framleiðslupöntun stofnuð sem notar mælieiningu framleiðslukeyrslu til að reikna út rétt magn íhluta meðan á keyrslunni **Endurnýjun framleiðslupöntunar** stendur. Dæmi um útreikning með mælieiningu framleiðslukeyrslu er þegar framleiddur hlutur er merktur á lager í stykkjum en framleiddur í tonnum.  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a>Til að stofna framleiðsluuppskrift með því að nota keyrslumælieininguna:  
1.  Mælieining framleiðslukeyrslu er sett upp sem mælieiningarvalkostur á síðunni **Mælieiningar vöru** á vörunni sem á að framleiða. Keyrslumælieiningin kemur ekki í staðinn fyrir Grunnmælieininguna á vörunni.  
2.  Stofnuð er framleiðsluuppskrift fyrir vöruna sem er sett upp með mælieiningu framleiðslukeyrslu. Frekari upplýsingar eru í [Stofna framleiðsluuppskriftir](production-how-to-create-production-boms.md).  
3.  Í reitnum **Mælieiningarkóti** er mælieining framleiðslukeyrslu valin.  
4.  Fyrir hverja framleiðsluuppskriftarlínu í reitnum **Magn á** er slegið inn magnið af þessum vöruíhlut sem þarf til að stofna þessa keyrslumælieiningu.  
5.  Opna **Birgðaspjald** fyrir vöruna sem á í hlut.  

    Á flýtiflipanum **Áfyllingu**, í reitnum **Framleiðsluuppskriftarnr.**, er framleiðsluuppskriftin valin sem stofnuð var fyrir ofan.  
6.  Stofnaður er framleiðslupöntunarhaus með því að nota vöruna sem er sett upp með mælieiningu framleiðslukeyrslu. Frekari upplýsingar eru í [Stofna framleiðslupantanir](production-how-to-create-production-orders.md).  
7.  Veldu aðgerðina **Uppfæra** og veldu síðan **Í lagi** hnappinn.  

Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, og velja svo aðgerðina **Íhlutir** til að skoða niðurstöðurnar. Kerfið reiknar út rétt magn íhluta sem þarf til að fullnægja framleiðsluuppskriftinni á grundvelli mælieiningu framleiðslukeyrslu.  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a>Til að reikna út Mælieiningu framleiðslukeyrslu á Framleiðslupöntun:  
1.  Stofnaður er framleiðslupöntunarhaus með því að nota vöruna sem er sett upp með mælieiningu framleiðslukeyrslu.  
2.  Í reitnum **Vörunr.** í Framleiðslupöntunarlínunni er slegið inn sama vörunúmer og notað er í hausnum.  
3.  Í reitnum **Magn** er slegið inn sama magn og er notað í hausnum.  
4.  Í reitnum **Mælieiningarkóti** er mælieiningarkóti framleiðslukeyrslu valinn.  
5.  Velja aðgerðina **Uppfæra**.
6.  Á flýtiflipanum **Reikna** skal hreinsa gátreitinn **Línur**.  
7.  Velja hnappinn **Í lagi**.  
8.  Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, og velja svo aðgerðina **Íhlutir** til að skoða niðurstöðurnar. Rétt magn íhluta sem þarf til að fullnægja framleiðsluuppskriftinni er reiknað út á grundvelli mælieiningu framleiðslukeyrslu.  

## <a name="see-also"></a>Sjá einnig  
[Stofna leiðir](production-how-to-create-routings.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)     
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Áætlun](production-planning.md)   
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
