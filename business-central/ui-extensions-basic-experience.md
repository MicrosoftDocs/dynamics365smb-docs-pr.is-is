---
title: Viðbót grunnupplifunar | Microsoft Docs
description: Þessi viðbót er nútímalegur valkostur í stað Microsoft Dynamics C5.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 19e784695c3864642dd13460e1cb93f6f58d706d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784791"
---
# <a name="the-basic-experience-extension"></a>Viðbót grunnupplifunar
Ef þú hefur verið með Microsoft Dynamics C5 geta samstarfsaðilar Microsoft hjálpað þér að skipta yfir í nútímalega lausn sem byggir á [!INCLUDE[prod_short](includes/prod_short.md)], þannig að þú getir haldið áfram að njóta sömu einföldu möguleikana og Dynamics C5.

Þessi viðbót er ætluð fyrir lítil fyrirtæki og getur stutt við allt að þrjá notendur. Ef þörf er á fleiri notendum þarf að uppfæra í [!INCLUDE[prod_short](includes/prod_short.md)]-leyfi og fjarlægja þessa viðbót.

> [!NOTE]
> Eins og staðan er í dag er þessi viðbót aðeins í boði fyrir viðskiptamenn í Danmörku og á Íslandi. 

## <a name="whats-available"></a>Hvað er í boði
Eftirfarandi tafla lýsir möguleikunum sem eru í boði ef viðbót grunnupplifunar er sett upp.

|Svæði  |Aðgerð  |
|---------|---------|
|**Fjárhagur** |Grunnfjármál, fjárhagsskema, eignir, bankakerfi, bankaafstemming, greiðslur, beingreiðsla, víddir, margir gjaldmiðlar, fjárhagsáætlanir, verkflæði, skjalastjórnun/stafakennsl, sameining, ótakmörkuð fyrirtæki|
|**Viðskiptakröfur/sala** |Grunnviðskiptakröfur, reikningsfærsla sölu, söluafslættir, verðlagning, virðisaukaskattur, tengslastjórnun |
|**Viðskiptaskuldir/innkaup** |Grunnviðskiptaskuldir, reikningsfærsla innkaupa |
|**Verkefnastjórnun** |Verk, verðlagning verks, vinnuskýrslur, úthlutun, verkefni, tilföng |
|**Birgðir** |Grunnbirgðir, staðgenglar vörur, millivísun vöru |

## <a name="getting-started"></a>Hafist handa
Þessi viðbót er aðeins öðruvísi en flestar og þú þarft aðstoð frá samstarfsaðila Microsoft til að setja hana upp. Bara þannig að þú vitir hverju þú mátt búast við, þá er hér mikil yfirsýn yfir það hvað samstarfsaðili Microsoft mun gera.

1. Stofna nýjan [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda. Þetta gæti verið annaðhvort prufuútgáfa eða CSP-útgáfa.
2. Bætið að minnsta kosti einum notanda við sem er úthlutað á leyfi grunnupplifunar á Azure Active Directory-reikningnum.
3. Fjarlægið öll fyrirtæki, þar á meðal sýnifyrirtækið Cronus.
4. Stofnið nýtt fyrirtæki sem inniheldur engin sýnigögn eða uppsetningar.
5. Bætið við **Sýniútgáfu RapidStart** pakkanum. <!--what does the pockage contain?-->
6. Sækið og setjið upp viðbót grunnupplifunar úr AppSource.

## <a name="migrating-data"></a>Gögn flutt
Komdu með Dynamics C5 gögnin þín. Þegar samstarfsaðili Microsoft hefur sett upp viðbót grunnupplifunar færðu tómt fyrirtæki í hendurnar. Auðveld leið til að yfirfæra gögnin úr Dynamics C5 í grunnupplifun er að nota viðbót gagnaflutnings fyrir C5 sem fylgir með í [!INCLUDE[prod_short](includes/prod_short.md)]. Viðbótin flytur viðskiptamenn, lánardrottna, vörur og fjárhagslykla og færslur þeirra.

## <a name="see-also"></a>Sjá einnig
[C5-gagnaflutningsviðbótin](ui-extensions-c5-data-migration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]