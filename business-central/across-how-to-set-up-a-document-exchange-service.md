---
title: Hvernig á að setja upp skjalaskiptaþjónustu | Microsoft Docs
description: Notaður er ytri þjónustuveitandi til að skiptast á rafrænum skjölum við viðskiptafélögum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0217f077c9c38603b9e3ff945fd47394c5b943bb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384375"
---
# <a name="set-up-a-document-exchange-service"></a>Setja upp skjalaskiptaþjónustu
Notaður er ytri þjónustuveitandi til að skiptast á rafrænum skjölum við viðskiptafélögum. Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Setja upp skjalaskiptaþjónustu  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning gagnaskiptaþjónustu** og veldu síðan tengda tengilinn.  
2. Fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Notandagerandi**|Færa inn allan texta sem hægt er að nota til að auðkenna fyrirtækið í skjalaskiptaferlinu.|  
    |**Leigjandakenni gagnaskipti**|Færa skal inn leigjanda í skjalaþjónustan sem stendur fyrir fyrirtækið. Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.|  
    |**Virk**|Tilgreina hvort þjónustan er virkjuð. **Athugið:** Þegar þjónustan er virkjuð eru minnst tvær verkraðarfærslur stofnaðar til að vinna með umferð rafrænna skjala inn og út úr [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar þú slekkur á þjónustu er verkraðarfærslum eytt.|  
    |**Skráningarvefslóð**|Tilgreina vefsíðuna þar sem nýskráning fyrir skjalskiptiþjónustuna fer fram.|  
    |**Vefslóð þjónustu**|Tilgreina veffang skjalaskiptiþjónustunna sem verður kölluð þegar rafræn skjöl eru send og tekið við þeim.|  
    |**Innskráningarvefslóð**|Tilgreina innskráningarsíðu fyrir skjalaskiptiþjónustuna, sem er þar sem slegið er inn notandanafn og aðgangsorð fyrirtækis til að skrá sig inn í þjónustuna.|  
    |**Lykill neytanda**|Færa skal inn þríliða OAuth-lykilinn fyrir neytendalykilinn. Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.|  
    |**Leyndarmál neytanda**|Færa skal inn leyndarmálið sem verndar neytendalykilinn. Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.|  
    |**Tákn**|Færa skal inn þríliða OAuth-lykilinn fyrir tákn. Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.|  
    |**Leyndarmál greiðslueiningar**|Færa skal inn leyndarmálið sem verndar táknið. Hann er gefinn upp af hálfu veitanda skjalaskiptiþjónustunnar.|  

    > [!NOTE]  
    > Innskráningargögnin þín eru sjálfkrafa dulrituð.

## <a name="see-also"></a>Sjá einnig  
[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Rafræn gagnaskipti](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]