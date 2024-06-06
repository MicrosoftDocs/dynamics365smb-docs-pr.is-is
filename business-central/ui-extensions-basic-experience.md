---
title: Grunnupplifun | Microsoft-skjöl
description: Þessi viðbót er nútímalegur valkostur í stað Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 11/10/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Grunnupplifunarviðbótin

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Ef þú hefur verið með Microsoft Dynamics C5 geta samstarfsaðilar Microsoft hjálpað þér að skipta yfir í nútímalega lausn sem byggir á [!INCLUDE[prod_short](includes/prod_short.md)], þannig að þú getir haldið áfram að njóta sömu einföldu möguleikana og Dynamics C5.

Þessi viðbót er ætluð fyrir lítil fyrirtæki og getur stutt við allt að þrjá notendur. Ef þörf er á fleiri notendum verður að uppfæra [!INCLUDE[prod_short](includes/prod_short.md)] í leyfi og fjarlægja þessa viðbót.

> [!NOTE]
> Eins og staðan er í dag er þessi viðbót aðeins í boði fyrir viðskiptamenn í Danmörku og á Íslandi.

## Hvað er í boði

Eftirfarandi tafla lýsir möguleikunum sem eru í boði ef viðbót grunnupplifunar er sett upp.

|Svæðarit  |Aðgerð  |
|---------|---------|
|**Fjárhagur** |Grunnfjármál, fjárhagsskýrslur, eignir, bankakerfi, bankaafstemming, greiðslur, beingreiðsla, víddir, margir gjaldmiðlar, fjárhagsáætlanir, verkflæði, skjalastjórnun/stafakennsl, sameining, ótakmörkuð fyrirtæki|
|**Viðskiptakröfur/sala** |Grunnviðskiptakröfur, reikningsfærsla sölu, söluafslættir, verðlagning, virðisaukaskattur, tengslastjórnun |
|**Viðskiptaskuldir/innkaup** |Grunnviðskiptaskuldir, reikningsfærsla innkaupa |
|**Verkefnastjórnun** |Verk, verðlagning verks, vinnuskýrslur, úthlutun, verkefni, tilföng |
|**Birgðir** |Grunnbirgðir, staðgenglar vörur, millivísun vöru |

## Hafist handa

Þessi viðbót er aðeins öðruvísi en flestir og þú þarft hjálp frá félaga Microsoft til að setja upp og setja hana upp. Svo að vitað sé við hverju má búast er hér mikil yfirsýn yfir það sem samstarfsaðili Microsoft gerir.

1. Stofna nýjan [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda. Þetta gæti verið annaðhvort prufuútgáfa eða útgáfa skýjalausnarveitu (CSP).
2. Bæta við að minnsta kosti einum notanda sem hefur fengið grunnupplifunarleyfi á reikningnum þínum Microsoft Entra .
3. Fjarlægið öll fyrirtæki, þar á meðal sýnifyrirtækið Cronus.
4. Stofna nýtt fyrirtæki sem inniheldur engin sýnigögn eða uppsetningar.
5. Bætið við **Sýniútgáfu RapidStart** pakkanum. <!--what does the package contain?-->
6. Sækið og setjið upp viðbót grunnupplifunar úr AppSource.

## Gögn flutt

Komdu með Dynamics C5 gögnin þín. Þegar Microsoft-félaginn setur upp grunnupplifunarviðbótina verður þú með tómt fyrirtæki. Auðveld leið til að yfirfæra gögnin úr Dynamics C5 í grunnupplifun er að nota viðbót gagnaflutnings fyrir C5 sem fylgir með í [!INCLUDE[prod_short](includes/prod_short.md)]. Viðbótin flytur viðskiptamenn, lánardrottna, vörur og fjárhagslykla og færslur þeirra.

## Sjá einnig .

[C5-gagnaflutningsviðbótin](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
