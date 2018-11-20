---
title: "Hönnunarupplýsingar - Forgangsraða pöntunum | Microsoft Docs"
description: "Kynntu þér hvernig skal forgangsraða til að mæta kröfum framboðs og eftirspurnar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6e09ad64750493f99210d47516410d8471a83011
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-prioritizing-orders"></a>Hönnunarupplýsingar: forgangsraða Pantanir
Innan tiltekinnar birgðahaldseiningar, táknar umbeðin eða tiltæk dagsetning hæsta forgang; eftirspurn í dag ætti að mæta áður en eftirspurn næstu viku er mætt. En auk þessarar heildarforgangs, mun áætlanakerfi einnig benda hvaða tegund af eftirspurn ætti að vera uppfyllt áður en önnur er uppfyllt. Eins mun það stinga upp á hvaða uppruna framboðs ætti að jafna áður en aðrar framboðsuppsprettur eru jafnaðar. Þetta er gert í samræmi við forgang pöntunar.  

Hlaðin eftirspurn og framboð hafa áhrif á forstillingu fyrir áætlaðar birgðir samkvæmt eftirfarandi forgangi:  

## <a name="priorities-on-the-demand-side"></a>Forgangur eftirspurnarmegin  
1. Þegar afhent: birgðafærsla  
2. Vöruskilapöntun innkaupa  
3. Sölupöntun  
4. Þjónustupöntun  
5. Framleiðsluíhlutaþörf  
6. Samsetningarpöntunarlína  
7. Flutningspantanir á útleið.  
8. Standandi pöntun (sem hefur ekki þegar verið notuð í annarri sölupöntun)  
9. Spá (sem hefur ekki þegar verið notuð í annarri sölupöntun)  

> [!NOTE]  
>  Innkaupaskil eru yfirleitt ekki notuð í framboðsáætlun. Þau ætti að alltaf að taka úr lotunni sem á að skila. Ef ekki er tekið frá gegna innkaupaskil hlutverki í framboðinu og eru fremst í forgangsröðinni til að komast hjá því að áætlanakerfið leggi til birgðapöntun bara til að þjóna innkaupaskilum.  

## <a name="priorities-on-the-supply-side"></a>Forgangur framboðsmegin  
1. Þegar í birgðum: birgðafærsla (sveigjanleiki áætlunar = enginn)  
2. Söluskilapöntun (sveigjanleiki í áætlun = enginn)  
3. Flutningspöntun á innleið  
4. Framleiðslupöntun  
5. Samsetningarpöntun  
6. Innkaupapöntun  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Forgangur sem tengist stöðu eftirspurnar og framboðs  
Burtséð frá forgangi sem fylgir gerð eftirspurnar og framboðs skilgreinir núverandi staða pantana í vinnsluferlinu einnig forgang. Til dæmis hafa vöruhúsaaðgerðir áhrif og staða sölu, innkaupa, flutnings, samsetningar og framleiðslupantana er tekin með í reikninginn:  

1. Að hluta meðhöndlað (Sveigjanleiki áætlunar = Enginn)  
2. Þegar í vinnslu í vöruhúsi (sveigjanleiki áætlunar = enginn)  
3. Útgefið - allar pantanategundir (áætlunarsveigjanleiki = ótakmarkað)  
4. Fastáætluð framleiðslupöntun (sveigjanleiki áætlunar = ótakmarkaður)  
5. Áætlað/opið – allar pantanagerðir (Sveigjanleiki áætlunar = Ótakmarkaður)  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

