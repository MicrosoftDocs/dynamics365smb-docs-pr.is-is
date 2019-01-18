---
title: "Uppsetning bestu venjur - Aðferð kostnaðarútreiknings | Microsoft Docs"
description: "Á birgðaspjaldinu skilgreinir Kostnaðaraðferð hvernig kostnaðarflæði vörunnar er skráð og hvort raunverulegt eða áætlað virði nýtist og sé notað við kostnaðarútreikninginn."
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
ms.sourcegitcommit: b8a5f4dcfa9a4e3f728c8de3786e7d5716ac82c7
ms.openlocfilehash: 0e52344ffe60a03e6bb9a64e798f639e9c3109a9
ms.contentlocale: is-is
ms.lasthandoff: 10/04/2018

---
# <a name="setup-best-practices-costing-method"></a>Uppsetning bestu venjur: Aðferð kostnaðarútreiknings
Á birgðaspjaldinu skilgreinir **Kostnaðaraðferð** hvernig kostnaðarflæði vörunnar er skráð og hvort raunverulegt eða áætlað virði nýtist og sé notað við kostnaðarútreikninginn.  

 Til að tryggja hagkvæmni birgða er mikilvægt að stilla hina réttu aðferð kostnaðarútreiknings samkvæmt tegund vöru og viðskiptaumhverfi.  

 Eftirfarandi tafla gefur upp bestu venjur um uppsetningu reitsins **Kostnaðaraðferð**. Nánari upplýsingar eru í [Upplýsingar um hönnun: Kostnaðarútreikningar](design-details-costing-methods.md).  

|Uppsetning valkostar|Bestu starfsvenjur|Athugasemd|  
|------------------|-------------------|-------------|  
|FIFO|Notið þar sem vörukostnaður er stöðugur.<br /><br /> Notið með vörum með takmarkaðan endingartíma, þar sem elstu vörurnar þarf að selja áður en þær fara fram yfir síðasta söludag.|Kostnaðarverð vöru er raunvirði sérhverrar innhreyfingar vörunnar, valið samkvæmt FIFO-reglunni.<br /><br /> Fyrir verðmat birgða, er gert ráð fyrir að vörur sem settar voru fyrst í birgðir seljist fyrst. **Athugið:** Þegar verð hækkar sýnir efnahagsreikningurinn hærra virði. Þetta þýðir að skattaskuldir aukast, en möguleikar til að fá lánsfé aukast.|  
|LIFO|Notið þar sem birgðamagni er alltaf viðhaldið eða aukið með tímanum.|Kostnaðarverð vöru er raunvirði sérhverrar innhreyfingar vörunnar, valin samkvæmt LIFO-reglunni.<br /><br /> Fyrir verðmat birgða, er gert ráð fyrir að vörur sem settar voru síðast í birgðir seljist fyrst. **Athugið:** Þegar verð hækkar, lækkar virðið á rekstarreikningnum. Þetta þýðir að skattaskuldir minnka, en möguleikar til að fá lánsfé rýrna. **Mikilvægt:** Óheimilt í mörgum löndum/svæðum, þar sem það getur verið notað til að minnka hagnað.|  
|Meðaltal|Notið þar sem vörukostnaður er óstöðugur.<br /><br /> Notið þar sem birgðum er raðað eða blandað saman og er ekki hægt að aðskilja, til dæmis kemísk efni.|Kostnaðarverð vöru er nákvæmur kostnaður þegar tekið var við vörunni.|  
|Sérstakt|Notið í framleiðslu eða viðskiptum með vörur sem auðvelt er að bera kennsl á og hafa frekar hátt kostnaðarverð.<br /><br /> Notist fyrir vörur sem falla undir reglugerð.<br /><br /> Notið fyrir vörur með raðnúmer.|Kostnaðarverð vöru er reiknað sem meðaleiningaverð vara á hverjum tímapunkti eftir innkaup.<br /><br /> Fyrir verðmat birgða er gert ráð fyrir að allar birgðir séu seldar samtímis.|  
|Staðall|Notið þar sem kostnaðarstýring er mikilvæg.<br /><br /> Notið í endurtekingaframleiðslu, til að meta kostnaðinn á beinu efni, beinni framleiðslu og sameiginlegs kostnaðar.<br /><br /> Notið í öguðu umhverfi og þar sem starfsfólkið viðheldur gæðastaðli.|Kostnaðarverð vöru er byggt á áætlun.<br /><br /> Þegar raunkostnaður er innleystur síðar, verður að breyta staðlaða kostnaðarverðinu í raunkostnaðinn, í gegnum fráviksgildi.|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)   
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Setja upp flókin notkunarsviðum með því að nota bestu venjur](set-up-complex-application-areas-using-best-practices.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

