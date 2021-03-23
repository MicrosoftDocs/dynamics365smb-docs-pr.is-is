---
title: Hvernig á að uppfæra staðlað kostnaðarverð | Microsoft Docs
description: Reglulega verður að uppfæra staðlað kostnaðarverð íhluta og leggja nýja kostnaðinn saman við yfirvöruna.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: feeeae5202cfc5ab0bccf1552ce74f74708445d3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391525"
---
# <a name="update-standard-costs"></a>Uppfæra staðlaðan kostnað
Reglulega verður að uppfæra staðlað kostnaðarverð íhluta og leggja nýja kostnaðinn saman við yfirvöruna. Ferlið samanstendur yfirleitt af fjórum eftirtöldum skrefum:  

1.  Uppfærslu kostnaðar á íhluta- og afkastagetustigunum. Frekari upplýsingar, sjá **Leggja til staðlaðan vörukostnað** runuvinnslu.  
2.  Samstilling og samantekt íhluta- og afkastakostnaðarins til að reikna út heildarframleiðslu- eða samsetningarkostnað varanna.  
3.  Innleiða staðlaðan kostnað sem færður var inn þegar fyrri keyrsla var keyrð. Staðlaður kostnaður tekur ekki gildi fyrr en hann er innleiddur. Sjá frekari upplýsingar í Innleiða breytingu á stöðluðu kostnaðarverði.  
4.  Innleiða breytingar til að uppfæra reitinn **Kostn.verð** á birgðaspjaldinu og framkvæma endurmat á birgðum. Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).  

Í [Um útreikning staðlaðs kostnaðar](finance-about-calculating-standard-cost.md) er fjallað nánar um þetta efni.  
## <a name="to-update-standard-costs"></a>að uppfæra staðlað kostnaðarverð  
1.  Keyrslan **Leiðr. kostnað - Birgðafærslur** er keyrð  
2.  Keyrslan **Bóka birgðakostnað á fjárhag** er keyrð  
3.  Opnið **Vinnublað fyrir staðlaðan kostnað** og notið eina eða fleiri af eftirfarandi aðgerðum:  

    1.  Keyrslan **Leggja til staðlaðan vörukostnað** er keyrð.  
    2.  Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.  
    3.  Keyrslan **Leggja til staðlaðan afkastakostnað** er keyrð.  
    4.  Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.
    5. Keyrslan **Leggja saman staðlað kostnaðarverð** er keyrð.
    6.  Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.
    7.  Keyrslan **Innleiða breytingu á stöðluðu kostnaðarverði** er keyrð.  
4.  Skoða og birta skal síðuna **Endurmatsbók** sem hefur verið fyllt með færslum úr fyrri skrefum í þessu ferli.  

## <a name="see-also"></a>Sjá einnig  
 [Um umreikning staðalkostnaðar](finance-about-calculating-standard-cost.md)   
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)   
 [Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md) [Fjármál](finance.md)  
 [Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]