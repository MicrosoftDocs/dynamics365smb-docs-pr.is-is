---
title: "Stofna og vinna með Utanbirgðavörur| Microsoft Docs"
description: "Lýsir því hvernig viðskipti fara fram með vörur sem ekki hægt að geyma í birgðum eða sem ekki er viðhaldið í birgðum."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b51c163dc8eafc462a1fd489d498d44eaeafd24a
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# Hvernig á að: Vinna með Utanbirgðavörur
Þú getur boðið viðskiptamaður þínum tilteknar vörur til þeim til hæginda, vörur sem þú vilt ekki geyma í birgðum fyrr en þú byrjar að selja þær. Þegar á að byrja að viðhalda slíkum vörum í birgðum, er hægt að breyta þeim í venjulegur birgðaspjöld á tvo vegu.

* Úr utanbirgðaspjaldi skal stofna nýtt birgðaspjald á grundvelli sniðmáts.
* Frá sölustaðarlínu af gerðinni **Vara** með tómum **Nr.* reit, veldu ekki atriði í vörulista. Birgðaspjald er sjálfkrafa stofnað fyrir þessa utanbirgðavöru.

> [!NOTE]  
>   Ekki hægt er að velja utanbirgðavöru úr glugganum **Sölureikningur**. Hægt er að velja utanbirgðavöru á úr **Sölutilboð** glugganum, en utanbirgðavöru verður ekki umbreytt í venjulega vöru þegar þú notar **Búa til Pöntun** aðgerð.

Utanbirgðavara hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana. Til að virkja umbreytingu utanbirgðaspjalds í venjulegur birgðaspjald, þarf fyrst að setja upp hvernig númeraröð lánardrottins er breytt í eigin númeraröð vöru.   

## Stofna utanbirgðavöru
Utanbirgðavöruspjöld hafa mikið minni upplýsingar en venjulegur birgðaspjöldum þar sem þær eru aðeins boðnar gegn tilboðum og með öðrum hætti. Af þeirri ástæðu þær þarf að umbreyta þeim í venjulegur birgðaspjöldum áður en hægt bóka sölufærslur fyrir þá.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Utanbirgðavörur** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Setja upp hvernig utanbirgðavörunúmerum er breytt í eigin númeraröð
Til að virkja umbreytingu utanbirgðaspjalds í venjulegt birgðaspjald, þarf fyrst að setja upp hvernig númeraröð lánardrottins er breytt í eigin númeraraðasnið.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Utanbirgðavörur Uppsetning** og velja svo viðeigandi tengil.
2. Fyllið inn í reitina eftir þörfum.

## Breyta utanbirgðavara í venjulega vöru
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Utanbirgðavörur** og velja svo viðeigandi tengil.
2. Opna spjald fyrir utanbirgðavara sem þú vilt umbreyta í venjulega vöru.
3. Í glugganum **utanbirgðavöruspjald** er valið **Stofna vara** aðgerð.

Stofnuð eru Nýtt birgðaspjald með sem er forútfyllt með upplýsingum úr utanbirgðavara og viðeigandi vörusniðmát. Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Hvernig á að: Skrá nýjar vörur](inventory-how-register-new-items.md).

## Selja utanbirgðavara og breyta henni í venjulega vöru
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð. Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er. Nánari upplýsingar eru í [Hvernig á að: selja vörur.](sales-how-sell-products.md)
3. Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.** að vera auður.
4. Veldu aðgerðina **Lína** og veldu síðan **Velja utanbirgðavörur**.

    Utanbirgðavara er breytt í venjulega vöru Stofnuð eru Nýtt birgðaspjald með sem er forútfyllt með upplýsingum úr utanbirgðavara og viðeigandi vörusniðmát.
5. Í **utanbirgðavara** glugganum, veljið utanbirgðavöruna sem þú vilt selja og veljið svo hnappinn **Í lagi**.
6. Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.

Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Hvernig á að: Skrá nýjar vörur](inventory-how-register-new-items.md).

> [!NOTE]  
>   Tilvísunarskrá yfir vöru er sjálfkrafa búin til fyrir lánardrottinn vörunnar á milli vörunúmers lánardrottins og nýja vörunúmers þíns.

## Sjá einnig
[Hvernig á að Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

