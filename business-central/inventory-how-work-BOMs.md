---
title: Vinna með uppskriftir
description: Þú stofnar samsetningar- eða framleiðsluuppskrift til að tilgreina íhlutina eða tilföngin sem þarf til að setja saman vöruna sem samsetningaruppskriftin segir til um.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bills of material, assembly BOM, production BOM,
ms.search.form: ''
ms.date: 09/26/2022
ms.author: a-reishima
ms.openlocfilehash: 4b1f1b15c2502ddb894baf733308800846a74206
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606722"
---
# <a name="work-with-bills-of-material"></a>Vinna með uppskriftir

Uppskriftir eru notaðar við uppbyggingu yfirvöru sem verður að vera sett saman úr öðrum vörum eða framleiddar af forða eða vélastöðvum úr íhlutum.

## <a name="assembly-boms-or-production-boms"></a>Samsetning uppskrifta eða framl. uppskrifta

[!INCLUDE[prod_short](includes/prod_short.md)] styður tvær mismunandi tegundir uppskrifta:

| UPPSKRIFTARGERÐ | Almennur Flokkur | Dæmi |
| -------- | ---------------- | ------- |
| [Uppskriftir samsetningar](assembly-how-work-assembly-boms.md) | Vöruhús/samsetning | Vörur sem samanstanda af öðrum vörum, settar saman við grunna eða án forða. |
| [Framl. uppskriftum](production-how-to-create-production-boms.md) | Framleiðsla/framleiðsla | Vörur sem samanstanda af mismunandi íhlutum og undirsamsetningum, framleiddar í vinnu-eða vélastöð. |

Samsetningarpantanir eru notaðar til að gera lokaafurð úr íhlutum með einföldu ferli sem hægt er að vinna með einu eða fleiri tilföngum, sem ekki eru vélar eða vinnustöðvar, eða án nokkurra tilfanga. Til dæmis gæti samsetningarferli falið í sér að velja tvær vínflöskur og einn kaffipoka og pakka þeim sem gjafavöru.  

Samsetningaruppskrift er aðalgögn sem skilgreina hvaða íhlutavörur fara í samsetta endanlega vöru og hvaða forðar er notaðir til að setja saman samsetningarvöruna. Þegar samsetningarvara og magn eru færð inn í haus nýrrar samsetningarpöntunar eru samsetningarpöntunarlínurnar sjálfkrafa fylltar út samkvæmt samsetningaruppskriftinni með eina samsetningarpöntunarlínu fyrir hvern íhlut eða tilfang. Frekari upplýsingar hjá [Samsetningarstjórn](assembly-assemble-items.md).

Framleiðslupantanir er notaðar til að búa til lokavörur úr íhlutum í flóknu ferli sem krefst framleiðsluleiða og vinnu- eða vélastöðva, sem endurspegla framleiðslugetu. Til dæmis getur verið að framleiðsluferli falið í sér að skera stálplötur í einni aðgerð, sjóða þær í þeirri næsta aðgerð og mála endanlegur vöruna í síðustu aðgerðinni. Frekari upplýsingar í [framleiðslu](production-manage-manufacturing.md).

Framleiðsluuppskrift er aðalgögn sem skilgreinir framleiðsluvöru og íhlutina sem notaðir eru í hana. fyrir samsetningarvöru verður framleiðsluuppskrift að vera vottuð og henni úthlutað til framleiðsluvörunnar áður en hægt er að nota hana í framleiðslupöntun. Þegar framleiðsluvaran er færð inn í framleiðslupöntunarlínu, annað hvort handvirkt eða með því að endurnýjun pöntunina, verður framleiðsluuppskriftin framleiðslupöntunaríhlutirnir. Læra meira at [skapa framl. uppskriftir](production-how-to-create-production-boms.md).

Hugtakið forði í framleiðslu er mun flóknara en í samsetningarstjórnun. Vinnustöðvar og vélastöðvar virka sem forði og framleiðsluskref eru sýnd með aðgerðum sem skráðar eru á forða í framleiðslu í framleiðsluleiðum. Frekari upplýsingar á [Stofnleiðum](production-how-to-create-routings.md) gr.

Hægt er að tengja bæði samsetningarpantanir og framleiðslupantanir beint við sölupantanir. Hins vegar er aðeins hægt að nota samsetningarpantanir til að sérsníða endanlegu vöruna beint samkvæmt beiðni viðskiptamanns með sölupöntun.

## <a name="see-also"></a>Sjá einnig .

[Vinna með Samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Birgðir](inventory-manage-inventory.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
