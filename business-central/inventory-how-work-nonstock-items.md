---
title: "Búa til og stjórna vörulistaatriðum| Microsoft Docs"
description: "Lýsir hvernig á að eiga viðskipti með hluti sem eru í lista seljanda yfir vörur en ekki í eigin lista yfir vörur."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: feef36443adef82329fe47573dd05cc6941b9d87
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-catalog-items"></a>Vinna með vörulistaatriði
Þú getur boðið ákveðnar vörur til viðskiptamanna þinna til þæginda, sem þú vilt ekki stjórna í kerfinu þínu fyrr en þú byrjar að selja þær. Þegar þú vilt byrja að stjórna slíkum vörum í kerfinu þínu, getur þú breytt þeim í venjuleg birgðaspjöld á tvo vegu.

* Búa til nýtt birgðaspjald byggt á sniðmáti úr spjaldi vörulistaatriðis.
* Frá sölupöntunarlínu af gerðinni **Vara** með reitinn **Nei** tóman skaltu velja vörulistaatriði. Birgðaspjald er þá sjálfkrafa búið til fyrir vörulistaatriðið.

> [!NOTE]  
> Ekki hægt er að velja vörulistaatriði úr glugganum **Sölureikningur**.<br /><br />
> Hægt er að velja vörulistaatriði úr **Sölutilboð** glugganum, en vörulistaatriði verður ekki umbreytt í venjulega vöru þegar þú notar **Búa til Pöntun** aðgerð.

Vörulistaatriði hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana. Til að virkja umbreytingu vörulistaatriðisspjalds í venjulegur birgðaspjald þarftu fyrst að setja það upp hvernig númeraröð lánardrottins er breytt í eigin vörunúmer.   

> [!Important]
> Vörulistaatriði má ekki rugla saman við vörur sem eru ekki vörur í birgðum sem eru reglulegar vörur sem eru gefnar tegundina **Ekki í birgðum**, til að halda þeim ekki tiltækum og fyrir utan kostnaðarútreikningur, til dæmis vegna þess að þeir eru aðeins notaðir innbyrðis og eru lágir kostnaður. Nánari upplýsingar er að finna í [Um vörugerðir](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Til að búa til vörulistaatriði
Vörulistaatriðaspjöld hafa miklu minni upplýsingar en venjulegir birgðaspjald vegna þess að þú notar þær aðeins til að bjóða upp á vitna og á annan hátt. Af þeirri ástæðu þær þarf að umbreyta þeim í venjulegur birgðaspjöldum áður en hægt bóka sölufærslur fyrir þá.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörulistaatriði** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Til að setja upp hvernig vörulistaatriðisnúmer eru breytt í eigin númeraröð
Til að virkja umbreytingu vörulistaatriðisspjals í venjulegur birgðaspjald þarftu fyrst að setja það upp hvernig númeraröð lánardrottins er breytt í eigin númeraraðasnið.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning vörulistaatriðis** og veldu síðan tengda tengilinn.
2. Fyllið inn í reitina eftir þörfum.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Til að breyta vörulistaatriði í venjulegt atriði
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörulistaatriði** og veldu síðan tengda tengilinn.
2. Opnaðu spjaldið fyrir vörulistaatriði sem þú vilt breyta í venjulegt atriði.
3. Í glugganum **Birgðaspjald vörulista** er valin aðgerðin **Stofna atriði**.

Stofnuð eru Nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát. Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Til að selja vörulistaatriði og breyta því í venjulegt atriði
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð. Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3. Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.** að vera auður.
4. Veldu aðgerðina **Lína** og veldu síðan **Velja vörulistaatriði** aðgerð.

    Vörulistaatriði breytt í venjulegt atriði. Stofnuð eru Nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát.
5. Í **Vörulistaatriði** glugganum, veljið vörulistaatriðið sem á að selja og svo hnappinn **Í lagi**.
6. Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.

Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

> [!NOTE]  
>   Tilvísunarskrá yfir vöru er sjálfkrafa búin til fyrir lánardrottinn vörunnar á milli vörunúmers lánardrottins og nýja vörunúmers þíns.

## <a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)|  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

