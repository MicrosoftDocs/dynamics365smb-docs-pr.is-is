---
title: "Notkun á QuickBooks Flutningsviðbót | Microsoft Docs"
description: "Lýsir því hvernig skal nota viðbæturnar til að flytja inn viðskiptamenn, lánardrottna, vörur og reikninga frá QuickBooks Desktop til Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>QuickBooks gagnaflutningsviðbótin fyrir Dynamics 365 for Financials
Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna og vara og reikninga úr QuickBooks Desktop í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef fyrirtækið notar QuickBooks er hægt að flytja út viðeigandi upplýsingar og opna síðan leiðarvísi fyrir uppsetningu með hjálp til að hlaða gögnunum upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Nánari upplýsingar eru í [Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Útflutningur gagna frá QuickBooks Desktop
Það þarf að vera búið að flytja suma eða alla viðskiptamenn, lánardrottna og birgðavörur og reikninga sem fyrir eru yfir í skrá á Intuit Interchange sniði (IIF). Viðbótin QuickBooks gagnaflutningar inniheldur sjálfgefna vörpun gagna QuickBooks þannig að þau gögn má nota til að prófa nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtækið. Sjálfgefin vörpun er nægileg í langflestum tilfellum en hægt er að breyta vörpun í leiðarvísi fyrir uppsetningu með hjálp.  
Í QuickBooks felur skráarvalmyndin í sér þann möguleika að flytja út lista. Fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að flytja út eftirfarandi lista:

* Viðskiptamannalisti  
* Lánardrottnalisti  
* Birgðalisti  
* Reikningalisti  

Útfluttu gögnin eru vistuð sem IIF-skrá sem síðan er hægt að hlaða upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>Finna viðbótin QuickBooks gagnaflutningar
Viðbótin QuickBooks gagnaflutningar er sett upp og tilbúin til keyrslu sem samþættur hluti af Gagnaflutningar uppsetningarleiðbeiningar með aðstoð. Ef þú ert tilbúin(n) til hefjast handa, og hefur flutt út þín gögn frá QuickBooks, skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning með hjálp** og velja svo viðeigandi tengil. Veljið **Flytja viðskiptagögn** og fara síðan eftir skrefunum í leiðbeiningunum.  

## <a name="see-also"></a>Sjá einnig
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)  

