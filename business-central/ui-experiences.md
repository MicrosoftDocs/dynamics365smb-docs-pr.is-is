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
ms.date: 10/08/2019
ms.author: sgroespe
ms.openlocfilehash: 8c9223176968d048d167b3b8509cab26343ee9f1
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775332"
---
# <a name="change-which-features-are-displayed"></a>Breyta því hvaða eiginleikar eru sýndir
[!INCLUDE[d365fin](includes/d365fin_md.md)] er hannað til að hjálpa stjórnendum að reka fyrirtæki, óháð stærð og margbreytileika þeirra. Varan inniheldur ómissandi eiginleika á borð við fjárhagsskýrslugerð, sölu, kaup og birgðastjórnun. Þegar umsvif fyrirtækis aukast er hægt að kveikja á annarri virkni, t.d. fyrir framleiðslu og þjónustustjórnun.

Hægt er að skilagreina flækjustig vörunnar, og þar með hvaða eiginleika notendur fyrirtækisins fá aðgang að, með því að breyta stillingum **Upplifun** á síðunni **Stofngögn** . Einnig er hægt að breyta upplifunarstillingu með því að bæta við tilteknum viðbótum frá AppSource. Frekari upplýsingar skoða [Sérstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] Nota viðbætur](ui-extensions.md).

Eftirfarandi tafla lýsir þeim reynslu sem nú er að finna.

| Upplifun | Áhrif á viðmótið |
| --- | --- |
| **Essential** |Sýnir allar aðgerðir og svið fyrir allar algengustu viðskiptavirknir.|
| **Úrvals** |Sýnir allar aðgerðir og svið fyrir alla viðskiptavirkni, þ.á.m. framleiðslu- og þjónustukerfi.|

Upplifanir sem hægt er að velja í [!INCLUDE[d365fin](includes/d365fin_md.md)] endurspegla leyfi og áskriftarleiðir sem eru skilgreindar fyrir vöruna. Upplýsingar um Essential og Premium áskriftarleiðir má finna í [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) á síðu Microsoft Dynamics 365 Marketing. Sjá einnig [[!INCLUDE[d365fin](includes/d365fin_md.md)] Leyfisleiðbeiningar](https://go.microsoft.com/fwlink/?linkid=2068931) (krefst aðgangs að CustomerSource eða PartnerSource).

> [!IMPORTANT]  
> Allir reglulegir notendur í lausn verða að sömu áætluninni úthlutað, grunn- eða úrvalsáskrift, áður en hægt er að velja þá upplifun fyrir fyrirtækið. Samkvæmt því getur einn notandi ekki fengið aðgang að eiginleikum úrvalsáskriftar ef einn eða fleiri aðrir notendur geta aðeins fengið aðgang að eiginleikum grunnáskriftar. Þetta á ekki við fyrir óreglulega notendur af gerðinni Team Member, innri stjórnandi, ytri endurskoðandi og úthlutaður stjórnandi, sem hver getur fengið annarri áætlun úthlutað en hinir notendurnir í lausninni.<br /><br /> Aðeins notendur af gerðinni Evaluation eða Premium geta breytt gildinu í reitnum **Upplifun** úr Essential í Premium.

Áður en þú upplifunarstilling fyrirtækis er skilgreind þarf að skilgreina aðgang notenda að sértækum aðgerðum og síðum með því að úthluta heimildasamstæðum. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

Stillingin **Upplifun** gildir um alla notendur í fyrirtæki en hver notandi getur sérstillt eigin upplifun enn frekar með því að breyta útliti og efni á síðu. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Virkjar eiginleika úrvalsáskriftar eftir uppfærslu á áætlun
Áætlunum er úthlutað til notenda í stjórnendamiðstöðinni Office 365 í tengslum við almennu vinnuna til að búa til notendur Business Central. Frekari upplýsingar, sjá [Bæta notendum við Office 365 fyrir fyrirtæki](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

### <a name="to-update-plan-changes-in-users-groups"></a>Til að uppfæra breytingar á áætlunum í flokkum notenda
Þegar þú hefur gert breytingu á áætlunum notenda í stjórnendamiðstöðinni Office 365, á borð við að úthluta fleiri notendum á úrvalsáskriftina, verður þú að endurspegla breytinguna í [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Skráðu þig inn sem stjórnanda.
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
3. Á síðunni **Notendur** skaltu velja aðgerðina **Endurhlaða alla notendaflokka**.

Allar nýjar upplýsingar um áætlanir notenda og úthlutuðum notendaflokkum þeirra hafa nú verið uppfærðar samkvæmt breytingum áætlunarinnar.

### <a name="to-select-the-premium-experience"></a>Til að velja úrvalsupplifunina
Nú er hægt að halda áfram til að velja nýju upplifunina.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stofngögn** og veldu síðan tengda tengilinn.
2. Á síðunni **Fyrirtækjaupplýsingar** í flýtiflipanum **Notandaupplifun** skal velja úrvalsáskrift í reitnum **Upplifun**.

## <a name="help-assumes-premium-experience"></a>Hjálp gerir ráð fyrir úrvalsupplifun
Allar lýsingar á eiginleikum í notendaskjölum fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] gera ráð fyrir **Úrvalsútgáfu** sem þýðir að áskriftirnar ná yfir heildarumfang viðmótseininga.

## <a name="see-also"></a>Sjá einnig .
[Sérstilling verksvæðis](ui-personalization-user.md)  
[Sérstilla Business Central](ui-customizing-overview.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Stofna ný fyrirtæki](about-new-company.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Leyfishandbók](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
