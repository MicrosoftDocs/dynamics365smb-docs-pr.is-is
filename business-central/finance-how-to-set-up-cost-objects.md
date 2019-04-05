---
title: Hvernig á að setja upp kostnaðarhluti | Microsoft Docs
description: Lærið hvernig á að setja upp kostnaðarhluti, sem eru svipaðir víddum fyrir fjárhaginn.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 616fcbe937e556c17e8beb79f68bc961ea8bbe18
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800695"
---
# <a name="set-up-cost-objects"></a>Uppsetning kostnaðarhluta
Kostnaðurhlutir eru verkefni, afurðair eða þjónustur fyrirtækis. Myndrit kostnaðarhluta er svipað og víddarupplýsingar fyrir fjárhag. Hægt er að setja upp myndritið yfir kostnaðaríhluti á eftirfarandi hátt:  

* Flytja víddargildi í fjárhag í myndrit yfir í kostnaðarhluti. Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.  
* Stofna nýjan kostnaðarhlut sem er óháður fjárhagnum eða bæta nýjum kostnaðarhlut við kostnaðarhlut sem fyrir er. Stofna þarf hvern kostnaðaríhlut sérstaklega.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Til að flytja víddargildi úr fjárhag í kostnaðarhluti  
1.  Stilla vídd sem á að vera kostnaðarliðarvíddin á síðunni **Uppfæra CA víddir**. Aðeins gildi úr þessari vídd er flutt.  
2.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðarhluti** og veldu síðan tengda tengilinn.  
3.  Veljið aðgerðina **Sækja kostnaðarhluti úr vídd** til að flytja víddargildi í myndriti kostnaðarhlutanna. Aðgerðin flytur víddargildin sem skilgreind voru í skrefi 1.  

    > [!NOTE]  
    >  Hægt er að setja reitinn **Stilla kostnaðarhlutavíddir** upp þannig að hann skilgreini einstefnusamstillingu á víddargildum frá fjárhag yfir í myndrit yfir kostnaðarhluti. Ekki er hægt að skilreina samstillingu myndrits yfir kostnaðarhluti við víddargildi úr fjárhag.  

Myndrit kostnaðarhluta inniheldur nú öll tilgreind víddargildi úr fjárhag og inniheldur titla og samtölur.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Til að stofna nýja kostnaðarhluti á síðunni myndrit fyrir kostnaðarliði  
Hægt er að setja upp og vinna með kostnaðarliði í **Kostnaðarliðaspjald** spjaldinu eða á síðunni **Myndrit fyrir kostnaðarliði**. Í þessu ferli eru settir upp kostnaðarliðir á síðunni **Myndrit fyrir kostnaðarliði**.  

1.  Opnaðu síðuna **Myndrit yfir kostnaðarliði** í breytingarstillingu.  
2.  Í reitinn **Kóði** er færður inn kóti kostnaðarliða. Allir kostnaðarhlutir verða að hafa kóta.  
3.  Í reitinn **Heiti** er færður inn heiti kostnaðarliða.  
4.  Velja fellilistaörina í reitnum **Línugerð** til að tilgreina tilgang kostnaðarhlutarins.  

    * Fyrir kostnaðarhluti af línutegundinni **Samtals** skal fylla út reitinn **Samtals frá/til**. Nota skal virkinn **eða**, sem er lóðrétt lína (**&#124;**) til að stilla svið kostnaðarhluta.  
    * Fyrir kostnaðarhluti af línutegundinni **Til-tala** er sjálfkrafa fyllt út í reitinn þegar inndráttarvirknin er notuð.  
5.  Fyllið upp í reitinn **Röðunarpöntun**.  
6.  Velja næstu tómu línu til að stofna nýjan kostnaðarhlut og endurtaka síðan þrep 2 til 5.  
7.  Þegar búið er að setja upp alla kostnaðarhlutina, skal velja aðgerðina **Draga inn kostnaðarhluti**. Velja hnappinn **Já**.  

> [!IMPORTANT]  
>  Ef skilgreiningar voru færðar inn í reitina **Samtals frá/til** fyrir **Loka-upphæð** kostnaðarhluti áður en inndráttaraðgerðin var keyrð þarf að færa þær inn aftur. Aðgerðin skrifar yfir gildin í öllum **Til - tala** reitum.  

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
[Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Stöður milli kostnaðartegundar, kostnaðarstaðar og kostnaðarliðar](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)   
[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md)   
[Um kostnaðarbókhald](finance-about-cost-accounting.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
