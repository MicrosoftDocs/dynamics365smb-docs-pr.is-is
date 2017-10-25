---
title: "Keyra framleiðslu | Microsoft Docs"
description: "Þegar eftirspurn hefur verið áætluð og efnið sent út samkvæmt framleiðsluuppskriftum, geta raunverulegar framleiðsluaðgerðir hafist og verið framkvæmdar í þeirri röð sem skilgreind er af framleiðslupöntunarleiðinni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: e27ceb91b25669a31d95256385cb7e5acd9160bd
ms.contentlocale: is-is
ms.lasthandoff: 09/27/2017

---
# <a name="manufacturing"></a>Framleiðsla
Þegar eftirspurn hefur verið áætluð og efnið sent út samkvæmt framleiðsluuppskriftum, geta raunverulegar framleiðsluaðgerðir hafist og verið framkvæmdar í þeirri röð sem skilgreind er af framleiðslupöntunarleiðinni.  

Mikilvægur hluti af framleiðslunni, hvað kerfið varðar, er að bóka frálag framleiðslu í gagnagrunninn til að sýna framvindu áætlunarinnar og uppfæra birgðir með fullbúnum vörum. Hægt er að bóka frálag á handvirkan hátt með því að fylla út og bóka færslulínur eftir framleiðsluaðgerðir. Einnig er hægt að bóka á sjálfvirkan hátt með því að nota afturvirka birgðaskráningu. Í slíkum tilvikum er efnisnotkun bókuð sjálfkrafa ásamt frálagi þegar lokið er við framleiðslupöntunina.  

Í stað þess að nota runubók til að bóka frálag margra framleiðslupantana má nota gluggann **Framleiðslubók** til að bóka notkun og/eða frálag fyrir tiltekna framleiðslupöntunarlínu.

Áður en þú getur byrjað að framleiða vöru, er nauðsynlegt að búa til ýmsar uppsetningar, eins og vinnustöðvar, leiðir og framleiðsluuppskriftir. Nánari upplýsingar er að finna í [Uppsetning framleiðslu](production-configure-production-processes.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Skilja hvernig framleiðsla gengur fyrir sig.|[Um framleiðslupantanir](production-about-production-orders.md)|
|Stofnun framleiðslupantana handvirkt|[Hvernig á að: stofna framleiðslupantanir](production-how-to-create-production-orders.md)|
|Útvista öllum eða völdum aðgerðum í framleiðslupöntun til undirverktaka.|[Hvernig á að: Fela undirverktaka framleiðslu](production-how-to-subcontract-manufacturing.md)|
|Skrá og bóka frálag framleiðslu ásamt efnis- og tímanotkun fyrir eina útgefna framleiðslupöntunarlínu.|[Hvernig á að: Bóka notkun og frálag fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md)|  
|Fjöldabóka magn íhluta notað á aðgerð, í færslubók sem getur unnið fjölda áætlaðra framleiðslupantana.|[Hvernig á að: fjöldabóka notkun](production-how-to-post-consumption.md)|
|Bóka magn tilbúinna vara og tíma eytt á aðgerð, í færslubók sem getur unnið fjölda útgefinna framleiðslupantana.|[Hvernig á að: fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md)|  
|Bóka fjölda vara sem framleiddar eru í hverri lokinni aðgerð sem ekki teljast til tilbúinnar vöru heldur sem úrkast.|[Hvernig á að: bóka úrkast](production-how-to-post-scrap.md)|
|Skoða álag á vinnusal sem afleiðingu útgefinna og afgreiddra framleiðslupantana.|[Hvernig á að: skoða álag á vinnu- og vélastöðvar](production-how-to-view-the-load-on-work-centers.md)|      
|Nota gluggann **Afkastagetubók** til að bóka notaða afkastagetu sem ekki er úthlutað á framleiðslupöntun, líkt og viðhaldsvinna.|[Hvernig á að bóka afkastagetu](production-how-to-post-capacities.md)|  
|Reikna út og jafna kostnað við tilbúnar framleiðsluvörur og íhluti sem notaðir voru til afstemmingar.|[Um lokinn framleiðslupantanakostnað](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Sjá einnig  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)      
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

