---
title: Hönnunarupplýsingar - Eftirspurn og framboð | Microsoft Docs
description: Eftirspurn er algeng orð notuð fyrir hvers konar vergri eftirspurn, svo sem sölupöntun og íhluti þarft frá framleiðslu röð. Að auki leyfir forritið meira tæknilega tegundir af eftirspurn, svo sem neikvæðar birgðum og innkaupaskil.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: ad6684bb1fefe10fc965c3c8a7780c6aa8a9d685
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800505"
---
# <a name="design-details-demand-and-supply"></a>Hönnunarupplýsingar: jöfnun eftirspurn og framboð
Eftirspurn er algeng orð notuð fyrir hvers konar vergri eftirspurn, svo sem sölupöntun og íhluti þarft frá framleiðslu röð. Að auki leyfir forritið meira tæknilega tegundir af eftirspurn, svo sem neikvæðar birgðum og innkaupaskil.  

 Framboð er það orð sem er mest notað fyrir hvaða tegund af jákvæðu eða innleiðarmagni sem er, eins og birgðir, innkaup, samsetning, framleiðsla eða millifærslu á innleið. Að auki geta söluvöruskil aftur getur einnig táknað framboð.  

 Til að raða út margar uppsprettur eftirspurn og framboð, áætlanakerfi skipuleggur þær á tvær tíma línur sem kallast birgðaforstillingar. Ein forstilling inniheldur eftirspurnartilvik og önnur inniheldur samsvarandi framboðstilvik. Hver atburður táknar eina pöntunarnetsfærslu, t.d. sölulínu, birgðafærslu, eða framleiðslupöntunarlínu.  

 Þegar birgðaforstillingar eru sóttar eru mismunandi eftirspurn-framboð söfn jöfnuð til að skila framboðsáætlun sem uppfyllir listuð markmið.  

 Áætlunarfæribreytur og birgðastig eru aðrar gerðir eftirspurnar og framboðs, sem fara í gegnum samþætta jöfnun til að fylla á birgðavörur. Nánari upplýsingar eru í [Upplýsingar um hönnun: Afgreiðsla endurpöntunarstefna](design-details-handling-reordering-policies.md).  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
 [Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
