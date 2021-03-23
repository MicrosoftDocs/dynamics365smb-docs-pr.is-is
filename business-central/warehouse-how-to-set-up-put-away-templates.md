---
title: Hvernig á að setja upp Frágangssniðmát | Microsoft Docs
description: Ef notaður er beinn frágangur og tínsla er stungið upp á því hólfi sem best hentar vörunum á hverjum tíma samkvæmt frágangssniðmátinu sem sett hefur verið upp fyrir vöruhúsið, hólfaflokkuninni sem hólfin hafa fengið, og hámarks- og lágmarksmagninu sem sett hefur verið upp fyrir föst hólf.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b6064bbad133ca521e5cb44667b9ead1368c1e0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382340"
---
# <a name="set-up-put-away-templates"></a>Setja upp frágangssniðmát

Ef notaður er beinn frágangur og tínsla er stungið upp á því hólfi sem best hentar vörunum á hverjum tíma samkvæmt frágangssniðmátinu sem sett hefur verið upp fyrir vöruhúsið, hólfaflokkuninni sem hólfin hafa fengið, og hámarks- og lágmarksmagninu sem sett hefur verið upp fyrir föst hólf.  

Hægt er að setja upp fleiri en eitt frágangssniðmát og velja eitt þeirra fyrir almenna stjórnun á frágangi í vöruhúsinu. Einnig er hægt að velja frágangssniðmát fyrir hverja þá vöru eða birgðahaldseiningu sem hefur sérstakar kröfur um frágang.  

## <a name="to-set-up-put-away-templates"></a>Frágangssniðmát sett upp

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frágangssniðmát** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.  
3. Færður er inn kóti sem er einkvæmt kenni sniðmátsins sem á að stofna.  
4. Stutt lýsing er færð inn ef vill.  
5. Fyrsta línan er fyllt út með hólfaþörfunum sem á fyrst og fremst að uppfylla þegar tillaga er gerð um frágang.

    Ef e.d. er óskað eftir sjálfgefinni frágangsaðferð sem á að byggja á föstum hólfum skal velja svæðið **Finna fast hólf**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Önnur línan er fyllt út með hólfaþörfunum sem ættu að vera annar kostur til að uppfylla þegar hólf er fundið fyrir frágang. Seinni línan er aðeins notuð ef hólf sem uppfyllir skilyrðin í fyrstu línunni finnst ekki.  
7. Haldið er áfram að fylla út línur þar til lýst hefur verið öllum viðunandi hólfastaðsetningum á að nota í frágangi.  
8. Í síðustu línunni í frágangssniðmátinu skal velja gátreitinn **Finna fljótandi hólf**.  

Hægt er að stofna mismunandi frágangssniðmát og nota þau eftir hentugleikum. Fyrst er notast við frágangssniðmátið sem valið hefur verið fyrir vöruna eða birgðahaldseininguna. Ef þeir reitir eru ekki fylltir út, er frágangssniðmátið sem valið er fyrir vöruhúsið á flýtiflipanum **Hólfareglur** á birgðageymsluspjaldinu notað.  

## <a name="see-also"></a>Sjá einnig

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]