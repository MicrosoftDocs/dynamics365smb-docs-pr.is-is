---
title: Samsetningarstjórnun | Microsoft Docs
description: Styðja fyrirtæki sem selja viðskiptavinum sínum vörur þar sem íhlutir eru sameinaðir í einföldum ferlum án þess að framleiðsluaðgerðir séu nauðsynlegar en inniheldur eiginleika til að setja saman vörur sem samþættast með fyrirliggjandi eiginleikum, t.d. sölu, áætlunum, frátektum og vöruhúsaaðgerðum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6088b23d48c1ea9e0ec07d245eaefafff11da025
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376863"
---
# <a name="assembly-management"></a>Samsetningardeild
Til að styðja fyrirtæki sem selja viðskiptavinum sínum vörur þar sem íhlutir eru sameinaðir í einföldum ferlum án þess að framleiðsluaðgerðir séu nauðsynlekir inniheldur [!INCLUDE[prod_short](includes/prod_short.md)] eiginleika til að setja saman vörur sem samþættast með fyrirliggjandi eiginleikum, t.d. sölu, áætlunum, frátektum og vöruhúsaaðgerðum.  

 Samsetningarvaran er skilgreind sem seljanleg vara sem inniheldur samsetningaruppskrift. Nánari upplýsingar er að finna í [Vinna með uppskrift.](inventory-how-work-BOMs.md)

 Samsetningarpantanir eru innri pantanir, rétt eins og framleiðslupantanir, sem eru notaðar til að stjórna samsetningarferli og til að tengja söluþarfirnar við viðeigandi vöruhúsaaðgerðir. Samsetningarpantanir eru ólíkar öðrum pöntunartegundum því þær fela í sér bæði frálag og notkun við bókun. Haus samsetningarpöntunarinnar hagar sér svipað og frálagsbókarlína og samsetningarpöntunarlínur haga sér svipað og notkunarfærslubókarlínur.  

 Til að styðja tímanlega birgðaáætlun og getuna til að sérsníða vörur eftir þörfum viðskiptavina er hægt að búa til og tengja samsetningarpantanir sjálfkrafa um leið og sölupöntunarlínan er búin til. Tengingin milli sölueftirspurnarinnar og framboðssamsetningarinnar gerir sölupantanagjörvum kleift að sérsníða samsetningarvöruna hvenær sem er, lofa afhendingardagsetningum samkvæmt framboði íhluta og bóka frálag og afhendingu samsettu vörunnar beint úr sölupöntunarviðmóti. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

 Í eina sölupöntunarlínu er hægt að selja magn sem er tiltækt og sem nauðsynlegt er að tekin séu úr birgðum ásamt magni sem verður að setja saman í pöntunina. Tilteknar reglur eru til staðar til að stýra dreifingu á slíku magni til að tryggja að sameiningarpöntunarmagnið fái forgang yfir birgðamagn í hlutaafhendingum. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Sérstakar virkni er til staðar til að stýra sendingu af sameiningarpantanamagni. Þegar magn samsetningar í pöntun er tilbúið til afhendingar bókar starfsmaðurinn í vöruhúsinu sem stjórnar birgðatínslu fyrir sölupöntunarlínuna sem um ræðir. Þetta stofnar síðan birgðahreyfingu fyrir íhlutina, bókar samsetningarfrálagið og sölupöntunarsendinguna. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu” í [Tína vörur með Birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Nánar um muninn á samsetningu á vörum rétt áður en sölupantanir eru sendar og samsetningu á vörum sem eru ætlaðar fyrir geymslu.|[Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Fylla upp í reiti á brigðageymslukortum í birgðagrunnstillingum til að skilgreina hvernig vörur fljóta til og frá samsetningardeildinni.|[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Sérsníða samsetningaríhlut eftir beiðni viðskiptavinar á meðan söluferlinu stendur og breyta í sölu eftir samþykkt.|[Búa til tilboð með samsetningarpöntun](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Sameina íhluti til að stofna vöru í einfaldri vinnslu, til pöntunar eða geymslu.|[Sameina vörur](assembly-how-to-assemble-items.md)|  
|Selja samsetningarsett sem ekki eru tiltæk með því að búa til tengda samsetningarpöntun til að veita fullt magn eða hluta af magni sölupöntunar.|[Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md)|
|Ef einhverjar samsetningarpöntunarvörur eru þegar í birgðum er hægt að draga það magn frá samsetningarpöntuninni og taka það frá í birgðum.|[Selja birgðavörur í flæðum samsetningar í pöntun](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Þegar verið er að selja samsetningarvörur úr birgðum og allar vörur eru ekki tiltækar, þá er hægt að hefja samsetningarpöntun sem sjálfkrafa veitir hluta af eða allt sölupöntunarmagnið.|[Selja vörur sem eru settar saman í pöntun og birgðavörur saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Búa til sérsniðnar samsetningarvörur fyrir standandi sölupantanir áður en gerðar eru reglulegar eiginlegar sölupantanir í samræmi við standandi pöntunarsamninginn.|[Búa til standandi samsetningarpantanir](assembly-how-to-create-blanket-assembly-orders.md)|
|Afturkalla bókaða samsetningarpöntun, til dæmis ef pöntunin var bókuð með mistökum sem þarf að leiðrétta.|[Afturkalla samsetningarbókun](assembly-how-to-undo-assembly-posting.md)|
|Nánar um muninn á samsetningaruppskriftum og framleiðsluuppskriftum og viðeigandi vinnslumismun.|[Vinna með uppskriftir](inventory-how-work-BOMs.md)|
|Nánar um hvernig samsetningarnotkun og frálag eru meðhöndluð við bókun samsetningarpantana og hvernig afleiddur vörukostnaður og forðakostnaður eru unnir og dreift á fjárhag.|[Hönnunarupplýsingar: Bókun samsetningarpöntunar](design-details-assembly-order-posting.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig

[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Kynning: Handvirk áætlun birgða](walkthrough-planning-supplies-manually.md)  
[Kynning: Selja, setja saman og afhenda sett](walkthrough-selling-assembling-and-shipping-kits.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]