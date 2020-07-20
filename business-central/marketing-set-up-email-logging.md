---
title: Setja upp tölvupóstskráningu | Microsoft Docs
description: Kynntu þér hvernig tölvupóstsamskipti milli sölufólks og viðskiptavina geta skapað alvöru sölutækifærum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 07/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9ca381bfebcd6db8e67d8153d4d2bc17eeffad81
ms.sourcegitcommit: f9aec4a72172d9270e14e2938c5550d69508f1aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2020
ms.locfileid: "3532670"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða

Fáðu meira út úr samskiptum sölumanna við núverandi eða mögulega viðskiptavini þína með því að rekja tölvupóstsamskipti og breyta þeim síðan í möguleg tækifæri. [!INCLUDE[d365fin](includes/d365fin_md.md)] getur unnið með Exchange Online til að halda skrá yfir skilaboð á inn- og útleið. Þú getur skoðað og greint innihald skilaboða á síðunni **Samskiptaskráningarfærslur**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Setja upp almenningsmöppur og reglur fyrir tölvupóstsskráningu á Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Næst tengir þú [!INCLUDE[prodshort](includes/prodshort.md)] við Exchange Online.

## <a name="setting-up-d365fin-to-log-email-messages"></a>Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)] til að skrá tölvupóstskilaboð

Hafist handa með tölvupóstskráningu í tveimur einföldum skrefum:

1. Tengdu [!INCLUDE[d365fin](includes/d365fin_md.md)] við Exchange Online fyrir Office 365 áskriftina þína. Exchange Online sér um tölvupóstskilaboðin þín. Við höfum einfaldað þetta skref með því að bjóða upp á uppsetningarleiðbeiningar. Þú þarft bara innskráningarupplýsingar stjórnanda fyrir stjórnandareikning þinn í Office 365. Til að hefja leiðsögnina skaltu fara í **Uppsetning með hjálp** og velja síðan **Setja upp tölvupóstskráningu**.  

2. Gakktu úr skugga um að gild netföng hafi verið slegin inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir sölufólk og tengiliði, sem er háð því hvort um sé að ræða mögulega eða núverandi viðskiptavini. Til að gera það fyrir hvern viðskiptavin eða sölumann skal opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** og kíkja í reitinn **Netfang**.

> [!Tip]
> Eftir að þú hefur lokið skrefum leiðsagnarinnar geturðu athugað hvort tengingin hafi borið árangur. Leitaðu að **Uppsetning markaðssetningar**, veldu **Ferli**, síðan **Aðgerðir** og að lokum **Staðfesta uppsetningu tölvupóstskráningar**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Að skoða tölvupóstsamskipti í samskiptaskránni

[!INCLUDE[d365fin](includes/d365fin_md.md)] býr til færslu á síðunni **Samskiptaskrá** í hvert skipti sem sölumaður og tengiliður skiptast á tölvupóstskilaboðum. Til að skoða samskiptaskrána skaltu opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** fyrir einstaklinginn og velja síðan **Fletta**, **Ferill** og að lokum velja **Samskiptaskráningarfærslur**. Við getum gert nokkra hluti við hverja færslu í skránni, til dæmis:

- Skoðaðu innihald tölvupóstsins sem var sendur á milli með því að smella á aðgerðina **Sýna viðhengi**.
- Breyttu tölvupóstsamskiptum í sölutækifæri - Þú getur skapað tækifæri úr færslu sem lofar góðu og náð sölu út úr henni. Til að gera það skaltu velja færsluna og síðan aðgerðina **Stofna tækifæri**. Nánari upplýsingar er að finna í [Umsjón sölutækifæra](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Sjá einnig
[Stjórnun tengsla](marketing-relationship-management.md)

