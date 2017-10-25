---
title: "Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir | Microsoft Docs"
description: "Samsetningarvörur er hægt að veita annað hvort með því að setja þær saman í pöntun eða setja þær saman í birgðir til að geyma þar til þeirra er óskað í sölupöntun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d5be31ebb84542e1762ffda9bc76a3aa38485095
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir
Samsetningarvörur geta verið veittar í eftirfarandi tvo ferla:  

-   Setja saman í pöntun.  
-   Setja saman í birgðir.  

## Samsetning til pöntunar  
Yfirleitt er *setja saman í pöntun* notað fyrir vörur sem ekki á að setja í birgðir þar sem búist er við að þær verði sérsniðnar að þörfum viðskiptavinar eða vegna þess að lágmarka á birgðakostnað sem því að veita þær rétt í tíma. Stuðningsaðgerðirnar eru meðal annars:  

-   Hæfni til að sérstilla samsetningarvörur þegar tekið er við sölupöntun.  
-   Yfirlit yfir ráðstöfun samsetningaíhlutarins og íhluta hans.  
-   Hæfni til að taka frá samsetningaríhluti án tafar til að tryggja uppfyllingu pöntunar.  
-   Aðgerð til að ákvarða arðsemi sérsniðinnar pöntunar með því að taka saman verð og kostnað.  
-   Samþætting við vöruhús til að gera samsetningu og afhendingu auðveldari.  
-   Hæfni til að setja saman í pöntun þar sem sölutilboð eða standandi sölupöntun er gert.  
-   Hæfni til að sameina birgðamagn með samsetningarpöntunarmagni.  

Í samsetningarpöntunarferlinu er varan samsett út frá sölupöntuninni og með beinan tengil milli samsetningarpöntunarinnar og sölupöntunarinnar.  

Þegar vara sem setja á saman í pöntun er sett inn í sölulínu er samsetningarpöntun sjálfkrafa búin til með haus sem byggir á sölulínunni og með línur sem byggja á samsetningaruppskrift vörunnar margfaldarði með pöntunarmagninu. Hægt er að nota gluggann **Setja saman í pöntunarlínur** til að sjá tengdar samsetningarpöntunarlínur til að auðvelda sérstillingu á samsetningaríhlut og á afhendingardegi sem byggist á upplýsingum um framboð íhluta. Frekari upplýsingar, sjá [Hvernig skal: Selja vörur sem eru settar saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Þótt það sé ekki hluti af sjálfgefnu ferli er hægt að selja birgðamagn ásamt sameiningarpöntunarmagninu. Frekari upplýsingar, sjá [Hvernig á að selja birgðavörur með flæði samsetningarpantana](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 Til að virkja þetta ferli er verður reiturinn **Samsetningarregla** á birgðaspjaldinu að vera **Sameina í pöntun**.  

## Setja saman í birgðir  
 Yfirleitt er *setja saman í birgðir* notað fyrir vörur sem á að setja saman á undan sölu, s.s. þegar söluherferð fyrir sett er undirbúin og þau geymd í birgðum áður en þær eru pantaðar. Þessar vörur eru yfirleitt staðlaðar vörur eins og innpökkuð sett sem þú býður ekki upp á að séu sérsniðin eftir beiðni viðskiptavina.  

 Í sameina á lager vinnslunni, er varan sett saman án sölueftirspurnar og er geymd á lager í vöruhúsinu sem birgðavara fyrir seinni sölu eða notkun sem millivara. Frekari upplýsingar, sjá [Hvernig skal: Setja saman vörur](assembly-how-to-assemble-items.md). Frá þessum tímapunkti er varan tínd og unnin sem stök vara og meðhöndluð sem fullunnin framleiðsluvara.  

 Þegar vara sem setja á saman í birgðir er færð inn í sölulínu er línan eins og allar aðrar vörur sem seldar eru úr birgðum. Til dæmis, er ráðstöfunin athuguð eingöngu fyrir samsetningarvöruna.  

> [!NOTE]  
>  Þótt það sé ekki hluti af sjálfgefnu ferli er hægt að setja saman vörur til pöntunar jafnvel þótt hún sé gerð til að vera sett saman á lager. Frekari upplýsingar, sjá [Hvernig á að selja samsetningarpöntunarvörur og birgðavörur saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 Til að virkja þetta ferli er verður reiturinn **Samsetningarregla** á birgðaspjaldinu að vera **Setja saman í birgðir**.  

## Samsetningaraðstæður  
 Almenn reglu í samsetningarstjórnun er að þegar samsetningarpöntunarmagn er sameinað í sölupöntunarlínu, verður að afhenda það á undan birgðamagninu.  

 Ef samsetningarpöntun tengist sölupöntunarlínu verður gildið í reitnum **Magn sett saman í pöntun** í sölupöntunarlínunni afritað í reitinn **Magn sett saman** í gegnum **Magn** í haus samsetningarpöntunarinnar. Frekari upplýsingar, sjá [Hvernig skal: Selja vörur sem eru settar saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

 Auk þess er gildið í reitnum **Magn sett saman** tengt við reitinn **Magn afhent** á sölupöntunarlínunni og þessi tengsl stjórna afhendingu magns samsetningarpöntunar, bæði að hluta og að öllu leyti. Þetta á við bæði þegar fullt magn í sölulínu eru setta saman í pöntun og í samsetningartilvikum þar sem einn hlut sölulínumagnsins er settur saman í pöntun og annar hluti er afhentur úr birgðum. Í samsetningaraðstæðum fæst meiri sveigjanleiki við afhendingu að hluta til þar sem hægt er að breyta reitnum **Magn sett saman** innan fyrirframskilgreindra reglna til að tilgreina hversu margar einingar eigi að afhenta að hluta til úr birgðum og hversu margar eigi að afhenta með því að setja saman í pöntun.  

 Þurfi að setja saman og afhenda allt magn sölulínunnar er gildið í reitnum **Magn afhent** afritað í reitinn **Magn sett saman** í tengdu samsetningarpöntuninni þegar afhendingarmagni er breytt. Þetta tryggir að það magn sem verið er að afhenda sé að fullu lagt fram af magninu sem setja á saman í pöntun.  

 Í samsetningaraðstæðum er gildið í **Magn afhent** ekki afritað í reitinn **Magn sett saman** í haus samsetningarpöntunar. Í staðinn er sjálfgefið gildi sett inn í reitinn **Magn sett saman** sem er reiknað út frá reitnum **Magn afhent** samkvæmt forskilgreindri reglu sem tryggir að magn samsetningarpöntunar sé afhent fyrst.  

 Eigi að víkja frá þessu sjálfgildi, til dæmis ef aðeins á að setja saman meira eða minna en magnið í reitnum **Magn afhent**, má breyta reitnum **Magn sett saman** en þó aðeins samkvæmt reglunum hér að neðan  

 Dæmi um það hvers vegna breyta ætti magni til að setja saman, er að notandi vill bóka afhendingu að hluta á birgðamagni áður en samsetningarfrálagið er afhent.  

 Eftirfarandi útskýrir reglurnar sem skilgreina lágmarks- og hámarksgildi sem hægt er að færa handvirkt inn í **Magn sett saman** til að víkja frá sjálfgildinu í samsetningardæmi. Taflan sýnir samsetningardæmi þar sem reiturinn **Magn afhent** í tengdu sölupöntunarlínunni er breytt úr 7 í 4 og **Magn sett saman** verður þess vegna að sjálfgefnu 4.  

||Sölupantanalína|Samsetningarpöntunarhaus|  
|-|----------------------|---------------------------|  
||**Magn**|**Magn til afhendingar**|**Magn til samsetningar til pöntunar**|**Afhent magn**|**Magn**|**Magn til samsetningar**|**Samsett magn**|**Eftirstöðvar (magn)**|  
|Byrjun|10|7|7|0|7|7|0|7|  
|Breyting||4||||4 (sett inn sjálfgefið)|||  

 Byggt á ofangreindar aðstæðna, notandi getur aðeins breytt reitnum **Magn sett saman** á eftirfarandi hátt:  

-   Lágmarksmagn sem hægt er að færa inn er 1. Það er vegna þess að það verður í það minnsta að setja saman eina einingu svo hægt sé að selja fjórar einingar, að því gefnu að þær þrjár sem eftir standa séu tiltækar sem birgðir.  
-   Hámarksmagn sem hægt er að færa inn er 4. Þetta er til að tryggja það að ekki sé meira af þessari Samsetning til pöntunar vöru framleitt en það sem vantar fyrir söluna.  

## Sjá einnig  
[Samsetningardeild](assembly-assemble-items.md)  
[Hvernig á að: Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

