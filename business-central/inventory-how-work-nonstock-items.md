---
title: Stofna og stjórna vörulistaatriðum
description: Lýsir hvernig á að eiga viðskipti með hluti sem eru í lista seljanda yfir vörur en ekki í eigin lista yfir vörur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8e90de738a03887518ba8e4c33e0185da3134a6b
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060007"
---
# <a name="work-with-catalog-items"></a>Vinna með vörulistaatriði
Þú getur boðið ákveðnar vörur til viðskiptamanna þinna til þæginda, sem þú vilt ekki stjórna í kerfinu þínu fyrr en þú byrjar að selja þær. Þegar þú vilt byrja að stjórna slíkum vörum í kerfinu þínu, getur þú breytt þeim í venjuleg birgðaspjöld á tvo vegu.

* Búa til nýtt birgðaspjald byggt á sniðmáti úr spjaldi vörulistaatriðis.
* Frá sölupöntunarlínu af gerðinni **Vara** með reitinn **Nei** tóman skaltu velja vörulistaatriði. Birgðaspjald er þá sjálfkrafa búið til fyrir vörulistaatriðið.

> [!NOTE]  
> Ekki hægt er að velja vörulistaatriði á síðunni **Sölureikningur**.<br /><br />
> Hægt er að velja vörulistaatriði af **Sölutilboð** síðunni, en vörulistaatriði verður ekki umbreytt í venjulega vöru þegar þú notar **Búa til Pöntun** aðgerð.

Vörulistaatriði hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana. Til að virkja umbreytingu vörulistaatriðisspjalds í venjulegur birgðaspjald þarftu fyrst að setja það upp hvernig númeraröð lánardrottins er breytt í eigin vörunúmer.   

> [!Important]
> Vörulistaatriði má ekki rugla saman við vörur sem eru ekki vörur í birgðum sem eru reglulegar vörur sem eru gefnar tegundina **Ekki í birgðum**, til að halda þeim ekki tiltækum og fyrir utan kostnaðarútreikningur, til dæmis vegna þess að þeir eru aðeins notaðir innbyrðis og eru lágir kostnaður. Nánari upplýsingar er að finna í [Um vörugerðir](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Til að búa til vörulistaatriði
Vörulistaatriðaspjöld hafa miklu minni upplýsingar en venjulegir birgðaspjald vegna þess að þú notar þær aðeins til að bjóða upp á vitna og á annan hátt. Af þeirri ástæðu þær þarf að umbreyta þeim í venjulegur birgðaspjöldum áður en hægt bóka sölufærslur fyrir þá.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Til að setja upp hvernig vörulistaatriðisnúmer eru breytt í eigin númeraröð
Til að virkja umbreytingu vörulistaatriðisspjals í venjulegur birgðaspjald þarftu fyrst að setja það upp hvernig númeraröð lánardrottins er breytt í eigin númeraraðasnið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning vörulistaatriðis** og velja síðan viðkomandi tengil.
2. Fyllið inn í reitina eftir þörfum.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Til að breyta vörulistaatriði í venjulegt atriði
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir vörulistaatriði sem þú vilt breyta í venjulegt atriði.
3. Á síðunni **Birgðaspjald vörulista** er valin aðgerðin **Stofna atriði**.

Stofnað er nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát. Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Til að selja vörulistaatriði og breyta því í venjulegt atriði
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð. Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3. Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.** að vera auður.
4. Veldu aðgerðina **Lína** og veldu síðan **Velja vörulistaatriði** aðgerð.

    Vörulistaatriði breytt í venjulegt atriði. Stofnuð eru Nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát.
5. Á síðunni **Vörulistaatriði**, veljið vörulistaatriðið sem á að selja og svo hnappinn **Í lagi**.
6. Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.

Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

> [!NOTE]  
>   Vörutilvísun er sjálfkrafa vara milli vörunúmers lánardrottins og nýja vörunúmersins þíns. Frekari upplýsingar er að finna í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)|  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]