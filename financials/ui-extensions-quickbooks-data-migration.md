---
title: "Notkun á QuickBooks Flutningsviðbót | Microsoft Docs"
description: "Lýsir því hvernig skal nota viðbæturnar til að flytja inn viðskiptamenn, lánardrottna, vörur og reikninga frá QuickBooks Desktop til Finance and Operations, Business Edition."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 14e0aea700bbb46a612d8e462ace22b10faac7e2
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="the-quickbooks-data-migration-extension-for-finance-and-operations-business-edition"></a>QuickBooks gagnaflutningsviðbót fyrir Finance and Operations, Business Edition
Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna og vara úr QuickBooks í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef fyrirtækið notar QuickBooks er hægt að flytja út viðeigandi upplýsingar og opna síðan leiðarvísi fyrir uppsetningu með hjálp til að hlaða gögnunum upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].  
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

