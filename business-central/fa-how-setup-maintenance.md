---
title: "Uppsetning eignaviðhalds| Microsoft Docs"
description: "Til að stjórna viðgerðum á og þjónustu við eignir, ertu tilteknar almennar upplýsingar um viðhald, kóðar fyrir tegund verks, og bókunarlykil fyrir kostnað."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: aef3d672bf01425a36bdd599e18d9ee9dac73b2d
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-fixed-asset-maintenance"></a>Uppsetning eignarviðhalds
Til að halda utan um viðhald eigna, þarf fyrst að setja upp nokkrar almennar viðhaldsupplýsingar, bókunarlykil viðhaldskostnaðar og viðhaldskóta fyrir tegundir vinnu, svo sem Venjubundin Þjónusta eða Viðgerð.

## <a name="to-set-up-general-maintenance-information"></a>Uppsetning almennra viðhaldsupplýsinga:
Ef settir eru upp reitir fyrir viðhald er hægt að bóka viðhaldskostnað úr eignabók.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.
2. Valin er eignin fyrir hverja skilgreina á vátryggingasvið fyrir, og velja síðan **Breyta** aðgerð.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Viðhald**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Uppsetning viðhaldskóta
Þegar viðhaldskostnaður er bókaður úr færslubók fyllt í reitinn **viðhaldskóði** til að skrá hvers konar viðhald hefur verið framkvæmt eins og venjubundin þjónusta eða viðgerð.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðhald** og veldu síðan tengda tengilinn.
2. Í **Viðhald** glugganum skal setja upp kóta fyrir mismunandi tegundir viðhaldsvinnu.

## <a name="to-set-up-maintenance-expense-accounts"></a>Uppsetning reikninga viðhaldskostnaðar
Til að bóka viðhaldskostnað, verður fyrst að Færa inn reikningsnúmer í gluggann **Eignabókunarflokkar**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignabókunarflokkar** og veldu síðan tengda tengilinn.
2. Reiturinn **Reikningur viðhaldskostnaðar** er fylltur út fyrir hvern bókunarhóp.

> [!NOTE]  
>   Til að skilgreina að viðhaldskostnaði er úthlutað á deildir eða verkefni, eru settir upp úthlutunarlyklar. Frekari upplýsingar eru í [Setja upp almenna eiginleika eigna](fa-how-setup-general.md).

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

