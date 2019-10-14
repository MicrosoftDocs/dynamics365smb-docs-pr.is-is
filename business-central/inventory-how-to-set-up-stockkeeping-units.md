---
title: Hvernig á að setja upp birgðahaldseiningar | Microsoft Docs
description: Hægt er að nota birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekinn afbrigðiskóta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7c8ffde6f15bc50af691151ad652bfc5332f1c9f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309773"
---
# <a name="set-up-stockkeeping-units"></a>Setja upp birgðahaldseiningar
Hægt er að nota birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekinn afbrigðiskóta.  

 Birgðahaldseiningar eru viðbót við birgðaspjöldin. Þær koma ekki í staðinn fyrir þau þótt tengsl séu á milli þeirra. Með notkun birgðaeininga er hægt að aðgreina upplýsingar um vöru fyrir tilteknar birgðageymslur (svo sem vöruhús eða dreifingarmiðstöð) eða tiltekin afbrigði (svo sem mismunandi hillunúmer og mismunandi áfyllingarupplýsingar) fyrir sömu vöruna.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Uppsetning birgðaeininga  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðahaldseiningar** og veldu síðan tengda tengilinn.  
2.  Valið er **Nýtt** aðgerð.  
3.  Fært er í reitina á spjaldinu. Eftirfarandi reita er krafist: **Vörunr.**, **Kóti birgðageymslu**, og/ eða **Afbrigðiskóti**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar búið að setja upp fyrstu birgðaeininguna fyrir vöru er **Birgðahaldseiningin er til** gátreitur á **Vara** spjaldinu valið.  

Ef búa á til nokkrar birgðaeiningar fyrir vöru er keyrslan **Stofna birgðahaldseiningu** notuð.  

> [!NOTE]  
>  Upplýsingarnar á spjaldinu **Birgðaeining er til** hafa forgang á spjaldið **Vara**.

> [!Warning]
> Ef birgðahaldseiningin er afhent með framleiðslu er reiturinn **Staðlaður kostnaður** ekki notaður við reikningagerð og leiðréttingu á raunkostnað framleiddrar vöru. Þess í stað er reiturinn **Staðlaður kostnaður** á undirliggjandi birgðaspjaldinu notaður og öll frávik eru reiknuð út á móti kostnaðarhlut þeirrar vöru.<br /><br />
> Þar sem ekki er hægt að úthluta framleiðsluuppskriftum og leið til birgðahaldseininga, eru samanlagt kostnaðarverð og tengdur útreikningur á kostnaðarhlutum einnig ekki tiltæk á birgðahaldseiningar. Í [Um útreikning staðlaðs kostnaðar](finance-about-calculating-standard-cost.md) er fjallað nánar um þetta efni

## <a name="see-also"></a>Sjá einnig  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
