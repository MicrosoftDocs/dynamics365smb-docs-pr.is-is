---
title: Uppsetning bestu venja - Endurpöntunarstefnur | Microsoft Docs
description: Svæðið Endurpöntunarstefna á birgðaspjöldum býður upp á fjórar mismunandi áætlunaraðferðir sem ákvarða hvernig einstaka áætlunarfæribreytur orka hver á aðra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e788fc7af4335eab99ddce35bf2822e52332a9b9
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441448"
---
# <a name="setup-best-practices-reordering-policies"></a>Uppsetning bestu venja: Endurpöntunarstefnur
Svæðið **Endurpöntunarstefna** á birgðaspjöldum býður upp á fjórar mismunandi áætlunaraðferðir sem ákvarða hvernig einstaka áætlunarfæribreytur orka hver á aðra.  

Einn grundvöllur undir bestu venjur til að velja endurpöntunarstefnu er ABC-flokkun vörunnar. Þegar ABC-flokkun er notuð fyrir birgðastjórnun og framboðsáætlun er hlutum stýrt í samræmi við þrjá mismunandi flokka eftir virði þeirra og magni í samræmi við heildarmagn á lager. Virði-rúmmal dreifing á klösunum þremur er sýnd á eftirfarandi töflu.

|Flokkur|Prósenta af heildarbirgðamagni|Prósenta af heildarbirgðavirði|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|C|60-70|10-30|

ABC-flokkunin segir að spara megi vinnu og peninga með því að hafa lausari taum á vörum af lágu virði-magni en á vörum af háu virði-magni. Eftirfarandi mynd sýnir hvaða endurpöntunarstefna í [!INCLUDE[prod_short](includes/prod_short.md)] er best við fyrir A, B og C - vörur, í þessari röð.

![ABC-flokkun.](media/abc_classification.png "abc_classification")

Eftirfarandi tafla gefur upp bestu venjur til að velja milli fjögurra stefna.  

|Uppsetning valkostar|Bestu starfsvenjur|Athugasemd|  
|------------------|-------------------|-------------|  
|**Röð**|Notist fyrir A vörur.<br /><br /> Notist fyrir vörur sem búnar eru til eftir pöntun.<br /><br /> Við framleiðslu skal nota þetta fyrir vörur á efsta stigi og fyrir dýra íhluti og millivörur.<br /><br /> Notist fyrir vörur sem eru keyptar sem beinar afhending og sérstakar pantanir.<br /><br /> Ekki nota ef sjálfvirk frátekning er ekki samþykkt.|Vörur, eins og leðursófar í húsgagnaverslun, eru vörur með háu virði og lágan eða óreglulegan pöntunarhraða og birgðir eru óásættanlegar, eða nauðsynlegar eigindir breytilegar. Besta endurpöntunarstefnan er því sú sem áætlar sérstaklega fyrir hverja eftirspurn.|  
|**Lotu-fyrir-lotu**|Notist fyrir B vörur.<br /><br /> Við framleiðslu skal nota íhluti sem koma fyrir í mörgum uppskriftum. Þetta tryggir að innkaupapantanir eru sameinaðar fyrir sama lánardrottininn svo hægt sé að semja um betra verð.<br /><br /> Notist ef óvissa er um hvaða endurpöntunarstefnu skal velja.|B vörur, eins og borðstofustólar, hafa reglulega og fremur háa pöntunartíðni, en þeim fylgir einnig mikill kostnaðar. Besta endurpöntunarstefnan fyrir B-vörur er sú sem er hagkvæmust með því að pakka saman eftirspurn í endurpöntunarferlinu.<br /><br /> 80 prósent af vörum geta nota þessa reglu.<br /><br /> Má nota án áætlunarfæribreytna.|  
|**Fast endurpöntunarmagn**|Notist fyrir C vörur.<br /><br /> Sameina með færibreytum endurpöntunarmarks.<br /><br /> Við framleiðslu skal nota þetta fyrir íhluti á lægsta stigi.<br /><br /> Ekki nota ef varan er oft frátekin.|C vörur, eins og tebollar, eru verðlitlar vörur með mikilli og reglulegri pöntunartíðni. Besta endurpöntunarstefnan fyrir C-vörur er því sú sem tryggir stöðugt framboð með því að vera alltaf yfir endurpöntunarpunkti.<br /><br /> Taki notandinn frá magn fyrir fjarlæga eftirspurn truflar þar forsendur áætlunarinnar. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar.|  
|**Hámarksmagn**|Notist fyrir C vörur með háan birgðakostnað eða geymslutakmarkanir.<br /><br /> Sameina við eina eða fleiri pöntunarbreytur (lágmarks-/hámarkspöntunarmagn eða fjöldapanta).|C vörur, eins og tebollar, eru verðlitlar vörur með mikilli og reglulegri pöntunartíðni. Besta endurpöntunarstefnan fyrir C-vörur er sú sem tryggir stöðugan fáanleika með því að vera alltaf yfir endurpöntunarpunkti, en undir hámarks birgðamagni.<br /><br /> Til að breyta ráðlagðri röð gætirðu viljað lækka pöntunarmagnið niður í tiltekið hámarksmagn pöntunar, hækkað í tiltekið lágmarksmagn pöntunar, eða sléttað til að passa við tilgreint pöntunarmargfeldi. **Athugið:** Ef endurpöntunarmark er notað haldast birgðir á milli þess og hámarksmagns.|  

## <a name="see-also"></a>Sjá einnig  
 [Uppsetning bestu venjur: Framboðsáætlun](setup-best-practices-supply-planning.md)   
 [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
 [Setja upp flókin notkunarsviðum með því að nota bestu venjur](set-up-complex-application-areas-using-best-practices.md)  
 [Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]