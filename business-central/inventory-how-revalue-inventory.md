---
title: Stofna nýjar virðisfærslur fyrir vörur í birgðum| Microsoft Docs
description: Lýsir því hvernig skal auka eða rýra virðisfærslur einnar eða fleiri vara í birgðum með því að bóka núgildandi og útreiknað virði þeirra.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5f4028a7c081bf73c23c57bcb4707d678b4e47d6
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393075"
---
# <a name="revalue-inventory"></a>Endurmat birgða
Ef endurmeta á til hækkunar eða lækkunar birgðavirði vöru eða tiltekinnar færslu vegna vöru verður að nota endurmatsbókina.

## <a name="to-revalue-inventory"></a>Að endurmeta birgðir
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Endurmatsbók** og veldu síðan tengda tengilinn.
2. Veljið aðgerðina **Reikna út birgðavirði**.
3. Á síðunni **Reikna út birgðavirði** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velja hnappinn **Í lagi**.
5. Á síðunni **Endurmatsbók** í reitnum **Kostnaðarverð (Endurmetið)** er fært inn nýja kostnaðarverðið. Einnig er hægt að færa inn nýja samtölu í reitinn **Birgðavirði (endurmetið)**.

    Viðeigandi reitir eru uppfærðir sjálfkrafa. Bent er á að í reitnum **Upphæð** er sýnd breytingin í birgðavirði valinnar birgðafærslu. Þar er reiknaður út munurinn á reitunum **Birgðavirði (útreiknað)** og **Birgðavirði (endurmetið)**.
6. Þegar öllum línunum í endurmatsbókinni er lokið skal velja aðgerðina **Bóka**.

Nýjar færslur eru nú stofnaðar til að endurspegla endurmöt sem bókuð hafa verið. Hægt er að skoða ný gildi á viðkomandi birgðaspjaldi.

## <a name="see-also"></a>Sjá einnig
[Hönnunarupplýsingar: Endurmat](design-details-revaluation.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]