---
title: Setja upp tölvupóstskráningu | Microsoft Docs
description: Kynntu þér hvernig tölvupóstsamskipti milli sölufólks og viðskiptavina geta skapað alvöru sölutækifærum.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 08/26/2019
ms.author: bholtorf
ms.openlocfilehash: e42618be17ff4f9bfe0d54a88e70d5a1841568c1
ms.sourcegitcommit: 8d9f08304b2f3b5504332bc626383797564ac5e3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920467"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða
Fáðu meira út úr samskiptum sölumanna við núverandi eða mögulega viðskiptavini þína með því að rekja tölvupóstsamskipti og breyta þeim síðan í möguleg tækifæri. [!INCLUDE[d365fin](includes/d365fin_md.md)] getur unnið með Exchange Online til að halda skrá yfir skilaboð á inn- og útleið. Þú getur skoðað og greint innihald skilaboða á síðunni **Samskiptaskráningarfærslur**.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a>Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)] til að skrá tölvupóstskilaboð
Hafist handa með tölvupóstskráningu í tveimur einföldum skrefum:

1. Tengdu [!INCLUDE[d365fin](includes/d365fin_md.md)] við Exchange Online fyrir Office 365 áskriftina þína. Exchange Online sér um tölvupóstskilaboðin þín. Við höfum einfaldað þetta skref með því að bjóða upp á uppsetningarleiðbeiningar. Þú þarft bara innskráningarupplýsingar stjórnanda fyrir stjórnandareikning þinn í Office 365. Til að hefja leiðsögnina skaltu fara í **Uppsetning með hjálp** og velja síðan **Setja upp tölvupóstskráningu**. 
2. Gakktu úr skugga um að gild netföng hafi verið slegin inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir sölufólk og tengiliði, sem er háð því hvort um sé að ræða mögulega eða núverandi viðskiptavini. Til að gera það fyrir hvern viðskiptavin eða sölumann skal opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** og kíkja í reitinn **Netfang**.

> [!Tip]
> Eftir að þú hefur lokið skrefum leiðsagnarinnar geturðu athugað hvort tengingin hafi borið árangur. Leitaðu að **Uppsetning markaðssetningar**, veldu **Ferli**, síðan **Aðgerðir** og að lokum **Staðfesta uppsetningu tölvupóstskráningar**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Að skoða tölvupóstsamskipti í samskiptaskránni
[!INCLUDE[d365fin](includes/d365fin_md.md)] býr til færslu á síðunni **Samskiptaskrá** í hvert skipti sem sölumaður og tengiliður skiptast á tölvupóstskilaboðum. Til að skoða samskiptaskrána skaltu opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** fyrir einstaklinginn og velja síðan **Fletta**, **Ferill** og að lokum velja **Samskiptaskráningarfærslur**. Við getum gert nokkra hluti við hverja færslu í skránni, til dæmis:

* Skoðaðu innihald tölvupóstsins sem var sendur á milli með því að smella á aðgerðina **Sýna viðhengi**.
* Breyttu tölvupóstsamskiptum í sölutækifæri - Þú getur skapað tækifæri úr færslu sem lofar góðu og náð sölu út úr henni. Til að gera það skaltu velja færsluna og síðan aðgerðina **Stofna tækifæri**. Nánari upplýsingar er að finna í [Umsjón sölutækifæra](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Sjá einnig
[Stjórnun tengsla](marketing-relationship-management.md)

