---
title: "Uppsetning birgðaverðmats og kostnaðar | Microsoft Docs"
description: "Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Uppsetning birgðaverðmats og kostnaðar
Til að ganga úr skugga um að birgðakostnaður sé skráður rétt, er nauðsynlegt að setja upp ýmsa reiti og glugga áður en þú byrjar að framkvæma vörufærslur.

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Velja kostnaðaraðferð fyrir hverja vöru til að stýra því hvernig upphaflegur kostnaður hennar er notaður til að meta birgðavirði og kostnað seldra vara.|[Skrá nýjar vörur](inventory-how-register-new-items.md)|  
|Tryggja að kostnaður sé sjálfkrafa bókaður á fjárhag hvenær sem birgðafærsla er bókuð.|Reiturinn **Sjálfvirk kostnaðarbókun** í glugganum **Uppsetning birgða**|  
|Tryggja að áætlaður kostnaður sé bókaður á fjárhag til að geta séð af bráðabirgðafjárhagsreikningum áætlaðar upphæðir sem eru fallnar í gjalddaga og kostnað seldra vara áður en þær eru reikningsfærðar í raun.|Reiturinn **Áætluð kostnaðarbókun í fjárhag** í glugganum **Uppsetning birgða**|  
|Setja kerfið þannig upp að leiðrétt sé sjálfvirkt vegna allra kostnaðarbreytinga í hvert sinn sem birgðafærslur eru bókaðar.|[Leiðr. kostnað vara](inventory-how-adjust-item-costs.md)|  
|Skilgreina hvort reikna skuli meðalkostnaður aðeins á hverja vöru eða á hverja vöru og hverja birgðahaldseiningu og afbrigði vörunnar.|Reiturinn **Útreikningsgerð meðalkostnaðar** í glugganum **Uppsetning birgða**|  
|Velja tímabilið sem forritið á að nota til að reikna út vegið meðalinnkaupsverð vara sem nota meðalverðsaðferðina.|Reiturinn **Meðalkostnaðartímabil** í glugganum **Uppsetning birgða**|  
|Skilgreina birgðatímabil til að stýra birgðavirði yfir tiltekinn tíma með því að banna bókun færslna á lokuð birgðatímabil.|[Vinna við birgðatímabil](finance-how-to-work-with-inventory-periods.md)|  
|Tryggja að söluvöruskilum sé jafnað á upphaflegu færsluna á útleið til að varðveita birgðavirð.|Reiturinn **Nákvæmar kostnaðarbakfærslur áskildar** í glugganum **Sala & útistandandi**|  
|Tryggja að innkaupaskil sé jafnað á upphaflegu færsluna á innleið til að varðveita birgðavirði.|Reiturinn **Nákvæmar kostnaðarbakfærslur áskildar** í glugganum **Innkaup & viðskiptaskuldir**|
|Setja upp sléttunarreglur sem á að nota þegar vöruverð er leiðrétt eða lagt til eða þegar staðlaður kostnaður er leiðréttur eða lagður til.|Glugginn **Sléttunaraðferð**|  

## <a name="see-also"></a>Sjá einnig  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Unnið með Business Central](ui-work-product.md)  
[Fjármál](finance.md)  

