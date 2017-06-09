---
title: "Uppsetning bókhaldslykla | Microsoft Docs"
description: "Lýsir því hvernig hægt er að breyta bókhaldslyklinum."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 48202a9e9a763dcb22bed9975aa9c4a39d2dc4ae
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Uppsetning eða breyting á bókhaldslykli
Bókhaldslykill sýnir fjárhagslykla sem geyma fjárhagsleg gögn. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.
Hins vegar er hægt að breyta sjálfgefnum lyklum og hægt er að bæta við nýjum lyklum.  

## <a name="adding-or-changing-accounts"></a>Bæta við eða breyta lyklum
Fyrir hvern bókhaldslykil er hægt að opna hvern einstakan fjárhagslykil og bæta við eða breyta stillingum.

**Athugasemd**: Hægt er að eyða fjárhagsreikningi. Áðu en honum er eytt þarf hins vegar eftirfarandi að vera rétt:  

* Staða reikningsins verður að vera núll.  
* Reiturinn **Leyfa eyðingu fjárhagsr.fyrir** verður að vera stilltur í glugganum **Uppsetning fjárhags** og ekki mega vera fjárhagsfærslur í lyklinum frá og með þeim degi.  
* Ef reiturinn **Athuga notkun fjárhagsr.** í glugganum **Uppsetning fjárhags** er valinn má ekki nota lykilinn í neinum bókunarflokkum eða bókunargrunnum.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kemur í veg fyrir að fjárhagsreikningi sé eytt sem geymir gögn sem þarf í bókhaldslyklinum.  

## <a name="see-also"></a>Sjá einnig
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Stjórna bankareikningum](bank-manage-bank-accounts.md)  
[Víddir](finance-dimensions.md)  
[Flytja inn úr öðrum fjárhagskerfum](upload-data.md)  
[Hvernig á að: Vinna með GIFI kóða í Kanada](ca-finance-work-gifi-codes.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
