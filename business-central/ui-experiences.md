---
title: Breyta því hvaða eiginleikar eru sýndir
description: 'Kynntu þér hvað notandaupplifunin Grunnur og Úrvals þýða fyrir notandaviðmótið, notkunarsvið og fyrirtækið þitt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: '1,'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Breyta því hvaða eiginleikar eru sýndir

[!INCLUDE[prod_short](includes/prod_short.md)] er hannað til að hjálpa stjórnendum að reka fyrirtæki, óháð stærð og margbreytileika þeirra. Varan inniheldur ómissandi eiginleika á borð við fjárhagsskýrslugerð, sölu, kaup og birgðastjórnun. Þegar umsvif fyrirtækis aukast er hægt að kveikja á annarri virkni, t.d. fyrir framleiðslu og þjónustustjórnun.

Hægt er að skilagreina flækjustig vörunnar, og þar með hvaða eiginleika notendur fyrirtækisins fá aðgang að, með því að breyta stillingum **Upplifun** á síðunni **Stofngögn** . Einnig er hægt að breyta upplifunarstillingu með því að bæta við tilteknum viðbótum frá AppSource. Frekari upplýsingar skoða [Sérstilla [!INCLUDE[prod_short](includes/prod_short.md)] Nota viðbætur](ui-extensions.md).

Eftirfarandi tafla lýsir þeim reynslu sem nú er að finna.

| Upplifun | Áhrif á viðmótið |
| --- | --- |
| **Essential** |Sýnir allar aðgerðir og svið fyrir allar algengustu viðskiptavirknir.|
| **Úrvals** |Sýnir allar aðgerðir og svið fyrir alla viðskiptavirkni, þ.á.m. framleiðslu- og þjónustukerfi.|

Upplifanir sem hægt er að velja í [!INCLUDE[prod_short](includes/prod_short.md)] endurspegla leyfi og áskriftarleiðir sem eru skilgreindar fyrir vöruna. Upplýsingar um Essential og Premium áætlanir má finna [í Business Central](https://go.microsoft.com/fwlink/?linkid=2264940) á markaðssetrinu Microsoft Dynamics 365. Sjá einnig [[!INCLUDE[prod_short](includes/prod_short.md)] leiðbeiningar um leyfisveitingar](https://go.microsoft.com/fwlink/?linkid=2264939).

> [!IMPORTANT]  
> Notendum af gerðinni Teymismeðlimur, Innri stjórnandi, ytri endurskoðandi og Framseljandi er hægt að úthluta annarri áætlun en aðrir notendur í lausninni. Aðeins notendur af gerðinni Evaluation eða Premium geta breytt gildinu í reitnum **Upplifun** úr Essential í Premium.

> [!NOTE]
> Í 2024 gefa út bylgju 1 getur notandi með Premium áætlunina skráð sig inn í fyrirtæki sem notar nauðsynlega áætlun. Hins vegar getur Premium notandinn ekki notað neina eiginleika sem Premium leyfið veitir. Hið sama gildir ekki í gagnstæða átt. Notendur sem eru með nauðsynlega áætlun geta ekki skráð sig inn í fyrirtæki sem notar Premium-áætlunina.

Áður en þú upplifunarstilling fyrirtækis er skilgreind þarf að skilgreina aðgang notenda að sértækum aðgerðum og síðum með því að úthluta heimildasamstæðum. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

Stillingin **Upplifun** gildir um alla notendur í fyrirtæki en hver notandi getur sérstillt eigin upplifun enn frekar með því að breyta útliti og efni á síðu. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## Virkjun iðgjaldaaðgerða eftir að áætlun hefur verið uppfærð

Áætlunum er úthlutað til notenda í stjórnendamiðstöðinni Microsoft 365 í tengslum við almennu vinnuna til að búa til notendur Business Central. Frekari upplýsingar eru í [Bæta við notendum og úthluta leyfum á sama tíma](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### Til að uppfæra breytingar á áætlunum í flokkum notenda

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Þegar breytingar hafa verið gerðar á áætlunum notenda í Microsoft 365 Stjórnunarmiðstöð, eins og t.d. úthlutað fleiri notendum í iðgjaldaáætlunina, verður að uppfæra [!INCLUDE[prod_short](includes/prod_short.md)] til að endurspegla breytinguna.

1. Skráðu þig inn sem stjórnanda.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
3. Á síðunni **Notendur** skal velja **Uppfæra notendur úr Microsoft 365** aðgerð.

### Til að velja úrvalsupplifunina

Nú er hægt að halda áfram til að velja nýju upplifunina.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Upplýsingar um fyrirtæki** og velja síðan viðkomandi tengil.
2. Á síðunni **Fyrirtækjaupplýsingar** í flýtiflipanum **Notandaupplifun** skal velja úrvalsáskrift í reitnum **Upplifun**.

## Hjálp gerir ráð fyrir upplifun iðgjalda

Allar lýsingar á eiginleikum í notendaskjölum fyrir [!INCLUDE[prod_short](includes/prod_short.md)] gera ráð fyrir **Úrvalsútgáfu** sem þýðir að áskriftirnar ná yfir heildarumfang viðmótseininga.

## Sjá einnig .

[Sérstilling verksvæðis](ui-personalization-user.md)  
[Sérstilla Business Central](ui-customizing-overview.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Stofna ný fyrirtæki](about-new-company.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]