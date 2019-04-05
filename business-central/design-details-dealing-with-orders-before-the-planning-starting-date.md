---
title: 'Hönnunarupplýsingar: Takast á við pantanir fyrir upphafsdag | Microsoft Docs'
description: Þetta efni lýsir reglunum sem áætlanagerð gildir um pantanir í frystum svæðum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 9fee9eff60b441ef2d4782a77a6fbbbe8b01af03
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800317"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Hönnunarupplýsingar: Takast á við pantanir fyrir upphafsdag
Til að forðast að framboðsáætlun sýnir ómögulegt og því gagnslaus tillögur, vinnur áætlanakerfið tímabilið allt til áætlanagerðarupphafsdags sem fryst svæði þar sem ekkert er áætlað fyrir. Eftirfarandi regla gildir um fryst svæði:  

Allt framboð og eftirspurn fyrir upphafsdagsetningu áætlunartímabilsins verður talin hluti af birgðum eða afhent.  

Í samræmi mun áætlanakerfið ekki, með nokkrum undantekningum, stinga upp á breytingum á framboðspöntunum á frystu svæði og engir pöntunarrakningartenglar eru stofnaðir eða viðhaldið fyrir það tímabil.  

Undantekningar frá þessari reglu eru sem hér segir:  

* Ef áætlaðar tiltækar birgðir, þar með talin summa framboðs og eftirspurnar á frysta svæðinu, eru undir núlli.  
* Ef raðnúmer/lotunúmer þarf á bakfærða pöntun/pantanir.  
* Ef samstæðan framboð-eftirspurn er tengd með pöntun-fyrir-pöntun stefnu.  

Ef fyrstu tiltæku birgðir eru undir núlli leggur áætlanakerfið til neyðarbirgðapöntun daginn fyrir áætlunartímabilið til að ná yfir magnið sem vantar. Þar af leiðandi verða áætlaðar og tiltækar birgðir alltaf minnst núll þegar áætlun fyrir komandi tímabil hefst. Áætlunarlína fyrir þessa birgðapöntun birtir viðvörunartákn og viðbótarupplýsingar birtast við uppflettingu.  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Rað/Lotunúmer og pöntun fyrir pöntun tenglar eru undanþegin frosna reiturum  
Ef raðnúmer/lotunúmer þarf eða pöntun-í-pöntun tengill er til staðar hunsar áætlanakerfið frysta svæðið og skráir magn sem er bakfært frá upphafsdegi og leggur mögulega til aðgerðir til úrbóta ef framboð og eftirspurn eru ekki samstillt. Viðskiptaástæðan fyrir þessari stefnu er að slík sérstök pör eftirspurnar og framboðs verða að passa til að tryggja að þessi tiltekna eftirspurn sé uppfyllt.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
