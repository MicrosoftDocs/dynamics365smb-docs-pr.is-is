---
title: "Hvernig á að setja upp Kostnaðarstaði | Microsoft Docs"
description: "Kostnaðarstaðir eru deildir og framlegðarstöðvar sem bera ábyrgð á kostnaði og tekjum. Myndrit kostnaðarstaða er svipað og víddarupplýsingar fyrir fjárhag."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7362518cbade8132fb07f49e7b2e9be67c4bce29
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cost-centers"></a>Uppsetning kostnaðarstaða
Kostnaðarstaðir eru deildir og framlegðarstöðvar sem bera ábyrgð á kostnaði og tekjum. Myndrit kostnaðarstaða er svipað og víddarupplýsingar fyrir fjárhag. Hægt er að setja upp myndritið yfir kostnaðarstaði á eftirfarandi hátt:  

-   Flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði. Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.  
-   Stofna nýjan kostnaðarstað sem er óháður fjárhagnum eða bæta nýjum kostnaðarstað við kostnaðarstað sem fyrir er. Stofna þarf hvern kostnaðarstað sérstaklega.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Til að flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði  
1.  Setja upp vídd sem á að vera kostnaðarstaðarvíddin í glugganum **Uppfæra Kostnaðarbókhaldsvíddir**. Aðeins gildi úr þessari vídd er flutt.  
2.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðarstaði** og veldu síðan tengda tengilinn.  
3.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Sækja úr víddinni kostnaðarstaðir** til að flytja víddargildi í myndriti kostnaðarstaðanna. Aðgerðin flytur víddargildin sem skilgreind voru í skrefi 1.  

    > [!NOTE]  
    >  Hægt er að setja reitinn **Stilla kostnaðarstaðavíddir** upp þannig að hann skilgreini einstefnusamstillingu á víddargildum frá fjárhag yfir í myndrit yfir kostnaðarstaði. Ekki er hægt að skilreina samstillingu myndrits yfir kostnaðarstaði við víddargildi úr fjárhag.  

Myndrit kostnaðarstaða inniheldur nú öll tilgreind víddargildi úr fjárhag og inniheldur titla og samtölur.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a>Til að stofna nýja kostnaðarstaði í glugganum Myndrit fyrir kostnaðarstaði  
Hægt er að setja upp og vinna með kostnaðarstaði í **Kostnaðarstaðaspjald** spjaldinu eða í glugganum **Myndrit fyrir kostnaðarstaði**. Í þessu ferli eru settir upp kostnaðarstaðir í glugganum **Myndrit fyrir kostnaðarstaði**.  

1. Opna gluggann **myndrit yfir kostnaðarstaði** í breytingarstillingu.  
2. Í reitinn **Kóði** er færður inn kóti kostnaðarstaðarins. Allir kostnaðarstaðir verða að hafa kóta.  
3. Í reitinn **Heiti** er fært inn heiti kostnaðarstaðarins.  
4. Velja fellilistaörina í reitnum **Línugerð** til að tilgreina tilgang kostnaðarstaðarins.  

    - Fylla þarf út í reitinn **Samtala** fyrir kostnaðarstaði af gerðinni **Samtals**. Nota skal virkinn **eða**, sem er lóðrétt lína (**&#124;**) til að stilla svið kostnaðarstaða.  
    - Fyrir kostnaðarstaði af línutegundinni **Til-tala** er sjálfkrafa fyllt út í reitinn þegar inndráttarvirknin er notuð.  
5.  Fyllið upp í reitina **Röðunarpöntun** og **Undirflokkar kostnaðar**.  
6.  Velja næstu tómu línu til að stofna nýjan kostnaðarstað og endurtaka síðan þrep 2 til 5.  
7.  Þegar búið er að setja upp alla kostnaðarstað skal velja aðgerðina **Draga inn kostnaðarstaði**. Velja hnappinn **Já**.  

> [!IMPORTANT]  
>  Ef skilgreiningar voru færðar inn í **Samtölur** reitina fyrir **Loka-samtala** kostnaðarstaði áður en inndráttaraðgerðin var keyrð þarf að færa þær inn aftur. Aðgerðin skrifar yfir gildin í öllum **Til-tala** reitum.  

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)   
[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md)   
[Um kostnaðarbókhald](finance-about-cost-accounting.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

