---
title: Hvernig á að nota vörusamsafn í framleiðslu | Microsoft Docs
description: Þegar grunndagatal er sérsniðið fyrir fyrirtækið eða einhvern viðskiptafélaga eru breytingar á frídögum og virkum dögum færðar inn.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/05/2018
ms.author: sgroespe
ms.openlocfilehash: c3cb9f82688f89f00f934d1468492cfa752742fd
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800558"
---
# <a name="work-with-production-families"></a>Vinna með framleiðslusamsafn
Framleiðslusamsafn er hópur einstakra vara sem byggðar eru á líku framleiðsluferli. Með því að mynda framleiðslusamsöfn er hægt að framleiða sumar vörur tvisvar eða oftar í einni vinnslu, en þetta fínstillir efnisnotkun.

Í reit **Magn** á síðunni **Samsafn** er fært inn magnið sem framleitt hefur verið þegar allt samsafnið hefur verið framleitt einu sinni.

## <a name="example"></a>Dæmi
Við stönsun er hægt að framleiða fjögur stykki af sömu vörunni úr einni plötu og 10 stykki af annarri, ólíkri vöru, á sama tíma. Stansvélin mótar öll 14 stykkin í einu þrepi.

Stofnun framleiðslusamsafna dregur úr úrkastsmagninu vegna þess að það sem myndi venjulega vera afgangsúrkast, við framleiðslu stærri stykkja, er í staðinn notað til að framleiða minni hluti.

## <a name="to-set-up-a-production-family"></a>Uppsetning framleiðslusamsafns
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjölskyldur** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Framleiðsla byggt á framleiðslusamsafni
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fastáætluð framl.pantanir** og veldu síðan tengda tengilinn.
2. Stofna nýja framleiðslupöntun Frekari upplýsingar eru í [Stofna framleiðslupantanir](production-how-to-create-production-orders.md).
3. Í reitnum **Gerð uppruna**, veljið **Samsafn**.  
4. Í reitnum **Forðanr.** er viðeigandi framleiðslusamsafn valið.

## <a name="see-also"></a>Sjá einnig
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Áætlun](production-planning.md)   
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
