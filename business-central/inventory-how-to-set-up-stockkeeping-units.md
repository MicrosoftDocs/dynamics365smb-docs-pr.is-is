---
title: Hvernig setja á birgðahaldseiningar upp
description: Hægt er að nota birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekinn afbrigðiskóta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 5704, 5700, 5702, 5701
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a7314d228eef2ff45c7aaf4e3784290f9b17113
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059413"
---
# <a name="set-up-stockkeeping-units"></a>Setja upp birgðahaldseiningar
Hægt er að nota birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða afbrigðiskóta.  

Birgðahaldseiningar eru viðbót við birgðaspjöldin. Þær koma ekki í staðinn fyrir þau þótt tengsl séu á milli þeirra. Með notkun birgðaeininga er hægt að aðgreina upplýsingar um vöru fyrir tilteknar birgðageymslur (svo sem vöruhús eða dreifingarmiðstöð) eða tiltekin afbrigði (svo sem mismunandi hillunúmer og mismunandi áfyllingarupplýsingar) fyrir sömu vöruna.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Uppsetning birgðaeininga  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðahaldseiningar** og velja síðan viðkomandi tengil.  
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
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]