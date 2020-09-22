---
title: 'Hvernig á að: Selja birgðavörur með flæði samsetningarpantana | Microsoft Docs'
description: Ef vara er sett upp fyrir samsetning til pöntunar gerir sjálfgefna sölupöntunarvinnslan ráð fyrir því að varan sé ekki til í birgðum og að setja þurfi hana saman fyrir þessa tilteknu sölupöntun. Því er tengd samsetningarpöntun sjálfkrafa búin til þegar vöru er bætt við sölupöntunarlínu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4386888ed1c4803787938161f8c9e1071dd524e4
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786047"
---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>Selja birgðavörur í flæðum samsetningar í pöntun
Ef reiturinn **Samsetningarstefna** á birgðaspjaldi samsetningarvöru inniheldur **Samsetning til pöntunar** gerir sjálfgefna sölupöntunarvinnslan ráð fyrir því að varan sé ekki til í birgðum og að setja þurfi hana saman fyrir þessa tilteknu sölupöntun. Því er tengd samsetningarpöntun sjálfkrafa búin til þegar vöru er bætt við sölupöntunarlínu. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md). Ef hluti magns sölupöntunarinnar er þegar tiltækur í birgðum er hægt að minnka magn samsetningarpöntunarinnar með því að breyta reitnum **Magn til samsetningar til pöntunar** í sölupöntunarlínunni.  

Þetta dæmi er sjaldgæft þar sem búist er við að vörur sem settar eru saman í pöntun séu alltaf sérsniðnar, og líkurnar á því að þær séu í birgðum í þeirri stillingu sem annar viðskiptavinur bað um eru litlar. Ef fyrirtækið á samsetningarpantanir í birgðum vegna skila eða afturkallaðra pantana þarf að tína þetta magn og selja það áður en nýjar pantanir eru settar saman.  

> [!NOTE]  
>  Engin aðgerð er til staðar í sölupöntunum, sem sjálfkrafa aðvarar eða hjálpar til við að draga frá magn samsetningarpöntunar sem eru þegar til staðar. Í staðinn verður að fylgjast með upplýsingum um það hvað er til, svo sem í upplýsingakassanum **Sundurliðun sölulínu**.  

Svipuð virkni er tiltæk þegar verið er að selja samsetningarvörur úr birgðum og hluti af magni eða allt magnið er ekki tiltækt og hægt er að veita með samsetningarpöntun. Frekari upplýsingar eru í [Selja vörur sem eru settar saman í pöntun og birgðavörur saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Tilteknar reglur gilda um reitinn **Magn til afhendingar** í sölupöntunarlíknum sem hafa að geyma samsetningu samsetningarpöntunarmagns og birgðamagns. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).  

Í þessu ferli, er skipt út samsetninarpöntunarmagni við birgðamagn í sölupöntunarlínu. Skrefin eru meðal annars að greina hvort magnið sé tiltækt, draga það magn frá tengdri samsetningarpöntun og taka birgðamagnið síðan frá til að tryggja að það sé tínt og afhent fyrir pöntunina.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Til að selja birgðavörur í flæðum samsetningar í pöntun  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2.  Stofnið sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  
3.  Í sölupöntunarlínu fyrir birgðir sem settar eru saman í pöntun í reitnum **Magn** er fært inn áskilið magn.  
4.  Í upplýsingakassanum **Sundurliðun sölulínu** ákvarðaðu hvort allt eða eitthvað af áskildu magni er tiltækt.  
5.  Í reitnum **Magn til samsetningar til pöntunar** er tiltækt magn dregið frá þannig að einungis ótiltækt magn er sett saman í pöntunina. Reiturinn **Frátekið magn** er minnkaður í samræmi við það til að gefa til kynna að tengillinn á pöntun fyrir pöntun, eða frátektin, á einungis við magn sem á að setja saman.  
6.  Á flýtiflipanum **Línur** skal velja **Aðgerðir** og síðan aðgerðina **Taka frá**.  
7.  Á síðunni **Frátekning** skal velja birgðafærsluna eða línurnar sem hafa að geyma tiltækt magn á flipanum **Taka frá í gildandi línu** og velja svo **Í lagi** hnappinn.  

    Á síðunni **Sölupöntun** í reitnum **Frátekið magn** sem sýnir nú að magn pöntunarlínununnar er tekið frá. Reiturinn **Magn Til að setja saman í pöntun** speglar enn það undirmagn sem þarf að setja saman.  

8.  Gefið sölupöntunina út fyrir tínslu birgðavara og samsetningu ótiltækra vara. Nánari upplýsingar, sjá [Sameina vörur](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Hægt er að fylla út svæðið **Hólfkóði** í sölupöntuninni fyrirfram samkvæmt **Setja saman til pöntunar afhendingarhólfskóði** reitinn eða **Hólfakóði frá samsetningu** svæðinu á birgðageymsluspjaldinu. Í því tilfelli gæti reiturinn **Hólfkóti** í sölupöntunarlínunni verið rangur fyrir þessa samsetningu magns samsetningarpöntunar og birgðasamsetningar. Góð regla er að skoða reitinn **Hólfkóti** og ganga úr skugga um að staðsetningin virki fyrir allt magn. Að öðrum kosti skal færa inn tvenns konar mismunandi magn í aðskildar sölupöntunarlínur.  

## <a name="see-also"></a>Sjá einnig  
[Samsetningardeild](assembly-assemble-items.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
