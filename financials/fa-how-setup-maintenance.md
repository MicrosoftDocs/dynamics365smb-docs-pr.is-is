---
title: "Uppsetning eignaviðhalds| Microsoft Docs"
description: "Til að stjórna viðgerðum á og þjónustu við eignir, ertu tilteknar almennar upplýsingar um viðhald, kóðar fyrir tegund verks, og bókunarlykil fyrir kostnað."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cdf1183fb5383311dc34d8c2c619a1eddf7e8851
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-fixed-asset-maintenance"></a>Hvernig á að: Uppsetning eignarviðhalds
Til að halda utan um viðhald eigna, þarf fyrst að setja upp nokkrar almennar viðhaldsupplýsingar, bókunarlykil viðhaldskostnaðar og viðhaldskóta fyrir tegundir vinnu, svo sem Venjubundin Þjónusta eða Viðgerð.

## <a name="to-set-up-general-maintenance-information"></a>Uppsetning almennra viðhaldsupplýsinga:
Ef settir eru upp reitir fyrir viðhald er hægt að bóka viðhaldskostnað úr eignabók.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **eignir** og velja svo viðeigandi tengil.
2. Valin er eignin fyrir hverja skilgreina á vátryggingasvið fyrir, og velja síðan **Breyta** aðgerð.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Viðhald**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Uppsetning viðhaldskóta
Þegar viðhaldskostnaður er bókaður úr færslubók fyllt í reitinn **viðhaldskóði** til að skrá hvers konar viðhald hefur verið framkvæmt eins og venjubundin þjónusta eða viðgerð.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Viðhald** og velja svo viðeigandi tengil.
2. Í **Viðhald** glugganum skal setja upp kóta fyrir mismunandi tegundir viðhaldsvinnu.

## <a name="to-set-up-maintenance-expense-accounts"></a>Uppsetning reikninga viðhaldskostnaðar
Til að bóka viðhaldskostnað, verður fyrst að Færa inn reikningsnúmer í gluggann **Eignabókunarflokkar**.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **FA bókunarflokkar** og velja svo viðeigandi tengil.
2. Reiturinn **Reikningur viðhaldskostnaðar** er fylltur út fyrir hvern bókunarhóp.

> [!NOTE]  
>   Til að skilgreina að viðhaldskostnaði er úthlutað á deildir eða verkefni, eru settir upp úthlutunarlyklar. Nánari upplýsingar sjá [Hvernig á að setja upp almenna eiginleika eigna](fa-how-setup-general.md).

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

