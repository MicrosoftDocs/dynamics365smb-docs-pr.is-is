---
title: Selja samsetningarpöntunarvörur og birgðavörur saman | Microsoft Docs
description: Ef samsetningarvara er sett upp fyrir samsetningu á lager gerir sjálfgefna sölupöntunarvinnslan ráð fyrir því að varan sé nú þegar samsett og að tína megi hana úr birgðum ef hún er til ráðstöfunar. Ef hluti magnsins (eða allt magnið) er ekki tiltækt er hægt að stofna samsetningarpöntun fyrir eftirstandandi magn á fljótlegan hátt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 95feecd98debfe6595ca66b23bf38085f245f025
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304116"
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Selja vörur sem eru settar saman í pöntun og birgðavörur saman
Ef reiturinn **Samsetningarstefna** á birgðaspjaldi samsetningarvöru inniheldur **Setja saman í lager** gerir sjálfgefna sölupöntunarvinnslan ráð fyrir því að varan sé nú þegar samsett og að tína megi hana úr birgðum ef hún er til ráðstöfunar. Því er engin samsetningarpöntun búin til sjálfkrafa og tengd við sölupöntunarlínuna. Ef hluti magnsins eða allt magnið er ekki tiltækt er hægt að stofna samsetningarpöntun fyrir eftirstandandi magn með því að fylla út í reitinn **Magn til samsetningar til pöntunar** í sölupöntunarlínunni. Með þeim hætti er hægt að setja saman vöru til pöntunar jafnvel þótt hún sé sjálfgefið uppsett til að vera sett saman í birgðir.  

Svipaður sveigjanleiki er til þegar verið er að selja vörur sem á að safna í pöntunina og hluti magnsins er í birgðum sem á að draga frá samsetningarpöntuninni. Frekari upplýsingar eru í [Selja birgðavörur í flæðum samsetningar í pöntun](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
>  Tilteknar reglur gilda um reitinn **Magn til afhendingar** í sölupöntunarlíknum sem hafa að geyma samsetningu samsetningarpöntunarmagns og birgðamagns. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).  

> [!NOTE]  
>  Eftirfarandi ferli inniheldur ekki stöðluðu sölupöntunarskrefin sem þarf að fylgja áður en samsetningarpöntun er stofnuð fyrir ótiltækt magn.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Til að selja vörur sem eru settar saman í pöntun og birgðavörur saman  
1.  Í sölupöntunarlínu fyrir birgðir sem stillt eru til að vera safnað í birgðir, færið inn magn í reitinn **Magn** sem er umfram birgðir. Síðan **Kanna ráðstöfunargetu** birtist. Frekari upplýsingar, sjá [Skoða tiltækileika vöru](inventory-how-availability-overview.md).
2.  Athugið reitinn **Heildarmagn** (neikvætt gildi), sem færa á inn í næsta skrefi.  
3.  Í reitnum **Magn til samsetningar til pöntunar** er færður inn gildið úr fyrra skrefi.  
4.  Gera breytingar á samsetningaríhlutum. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  
5.  Haldið er áfram til að losa sölupöntunina, útbúa hana fyrir tínslu birgðavara og samsetningu ótiltækra vara. Nánari upplýsingar um þessar stöðluðu aðgerðir við samsetningu eru í [Sameina vörur](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Hægt er að fylla út svæðið **Hólfkóði** í sölupöntuninni fyrirfram samkvæmt **Setja saman til pöntunar afhendingarhólfskóði** eða **Hólfakóði frá samsetningu** svæðinu á birgðageymsluspjaldinu. Í því tilfelli gæti reiturinn **Hólfkóti** í sölupöntunarlínunni verið rangur fyrir þessa samsetningu magns samsetningarpöntunar og birgðasamsetningar. Góð regla er að skoða reitinn **Hólfkóti** og ganga úr skugga um að staðsetningin virki fyrir allt magn. Að öðrum kosti skal færa inn tvenns konar mismunandi magn í aðskildar sölupöntunarlínur.  

## <a name="see-also"></a>Sjá einnig  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
