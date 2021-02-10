---
title: Velja notandaupplifun til að sýna eða fela ítarlegri eiginleika | Microsoft Docs
description: Kynntu þér hvað notandaupplifunin Grunnur og Úrvals þýða fyrir notandaviðmótið, notkunarsvið og fyrirtækið þitt.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 354791b9a1bafb07bc1e16530dc1d07c16d1e49d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747619"
---
# <a name="change-which-features-are-displayed"></a>Breyta því hvaða eiginleikar eru sýndir
[!INCLUDE[prod_short](includes/prod_short.md)] er hannað til að hjálpa stjórnendum að reka fyrirtæki, óháð stærð og margbreytileika þeirra. Varan inniheldur ómissandi eiginleika á borð við fjárhagsskýrslugerð, sölu, kaup og birgðastjórnun. Þegar umsvif fyrirtækis aukast er hægt að kveikja á annarri virkni, t.d. fyrir framleiðslu og þjónustustjórnun.

Hægt er að skilagreina flækjustig vörunnar, og þar með hvaða eiginleika notendur fyrirtækisins fá aðgang að, með því að breyta stillingum **Upplifun** á síðunni **Stofngögn** . Einnig er hægt að breyta upplifunarstillingu með því að bæta við tilteknum viðbótum frá AppSource. Frekari upplýsingar skoða [Sérstilla [!INCLUDE[prod_short](includes/prod_short.md)] Nota viðbætur](ui-extensions.md).

Eftirfarandi tafla lýsir þeim reynslu sem nú er að finna.

| Upplifun | Áhrif á viðmótið |
| --- | --- |
| **Essential** |Sýnir allar aðgerðir og svið fyrir allar algengustu viðskiptavirknir.|
| **Úrvals** |Sýnir allar aðgerðir og svið fyrir alla viðskiptavirkni, þ.á.m. framleiðslu- og þjónustukerfi.|

Upplifanir sem hægt er að velja í [!INCLUDE[prod_short](includes/prod_short.md)] endurspegla leyfi og áskriftarleiðir sem eru skilgreindar fyrir vöruna. Upplýsingar um Essential og Premium áskriftarleiðir má finna í [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) á síðu Microsoft Dynamics 365 Marketing. Sjá einnig [[!INCLUDE[prod_short](includes/prod_short.md)] Leyfisleiðbeiningar](https://go.microsoft.com/fwlink/?linkid=2068931) (krefst aðgangs að CustomerSource eða PartnerSource).

> [!IMPORTANT]  
> Allir reglulegir notendur í lausn verða að sömu áætluninni úthlutað, grunn- eða úrvalsáskrift, áður en hægt er að velja þá upplifun fyrir fyrirtækið. Samkvæmt því getur einn notandi ekki fengið aðgang að eiginleikum úrvalsáskriftar ef einn eða fleiri aðrir notendur geta aðeins fengið aðgang að eiginleikum grunnáskriftar. Þetta á ekki við fyrir óreglulega notendur af gerðinni Team Member, innri stjórnandi, ytri endurskoðandi og úthlutaður stjórnandi, sem hver getur fengið annarri áætlun úthlutað en hinir notendurnir í lausninni.<br /><br /> Aðeins notendur af gerðinni Evaluation eða Premium geta breytt gildinu í reitnum **Upplifun** úr Essential í Premium.

Áður en þú upplifunarstilling fyrirtækis er skilgreind þarf að skilgreina aðgang notenda að sértækum aðgerðum og síðum með því að úthluta heimildasamstæðum. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

Stillingin **Upplifun** gildir um alla notendur í fyrirtæki en hver notandi getur sérstillt eigin upplifun enn frekar með því að breyta útliti og efni á síðu. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Virkjar eiginleika úrvalsáskriftar eftir uppfærslu á áætlun
Áætlunum er úthlutað til notenda í Microsoft 365 stjórnendamiðstöðinni í tengslum við almennu vinnuna til að búa til notendur Business Central. Frekari upplýsingar eru í [Bæta við notendum og úthluta leyfum á sama tíma](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups"></a>Til að uppfæra breytingar á áætlunum í flokkum notenda
Þegar þú hefur gert breytingu á áætlunum notenda í Microsoft 365 stjórnendamiðstöðinni, á borð við að úthluta fleiri notendum á úrvalsáskriftina, verður þú að endurspegla breytinguna í [!INCLUDE[prod_short](includes/prod_short.md)].

1. Skráðu þig inn sem stjórnanda.
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
3. Á síðunni **Notendur** skaltu velja aðgerðina **Endurhlaða alla notendaflokka**.

Allar nýjar upplýsingar um áætlanir notenda og úthlutuðum notendaflokkum þeirra hafa nú verið uppfærðar samkvæmt breytingum áætlunarinnar.

### <a name="to-select-the-premium-experience"></a>Til að velja úrvalsupplifunina
Nú er hægt að halda áfram til að velja nýju upplifunina.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stofngögn** og veldu síðan tengda tengilinn.
2. Á síðunni **Fyrirtækjaupplýsingar** í flýtiflipanum **Notandaupplifun** skal velja úrvalsáskrift í reitnum **Upplifun**.

## <a name="help-assumes-premium-experience"></a>Hjálp gerir ráð fyrir úrvalsupplifun
Allar lýsingar á eiginleikum í notendaskjölum fyrir [!INCLUDE[prod_short](includes/prod_short.md)] gera ráð fyrir **Úrvalsútgáfu** sem þýðir að áskriftirnar ná yfir heildarumfang viðmótseininga.

## <a name="see-also"></a>Sjá einnig .
[Sérstilling verksvæðis](ui-personalization-user.md)  
[Sérstilla Business Central](ui-customizing-overview.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Stofna ný fyrirtæki](about-new-company.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Leyfishandbók](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
