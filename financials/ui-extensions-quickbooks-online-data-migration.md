---
title: "Notkun á QuickBooks Flutningsviðbót | Microsoft Docs"
description: "Lýsir því hvernig skal nota viðbæturnar til að yfirfæra viðskiptamenn, lánardrottna, vörur og reikninga frá Quickbooks Online í Finance and Operations, Business Edition."
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8ed245276a6bebd369a3ec32791a9939e8db5aa1
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---

# <a name="the-quickbooks-online-data-migration-extension-for-finance-and-operations-business-edition"></a>QuickBooks Online gagnaflutningsviðbót fyrir Finance and Operations, Business Edition
Þessi viðbót er innifalin í **Gagnaflutningur** uppsetningu með aðstoð til að aðstoða þig við að flytja mikilvæg viðskiptagögn frá QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta er t.d. gagnlegt þegar fyrirtækið þitt er að vaxa, og þú hefur ákveðið að uppfæra stjórnunarforrit fyrirtækisins með því að byrja að nota [!INCLUDE[d365fin](includes/d365fin_md.md)]

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Hvaða gögn get ég flutt inn frá QuickBooks Online?
Þú getur flutt inn eftirfarandi gögn frá QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Viðskiptavinum
* Lánardrottnar
* Birgðir
* Bókhaldslykill
* Upphafsstöðufærsla í fjárhagnum
* Magn á lager fyrir birgðavörur
* Opna skjöl fyrir viðskiptamenn og lánardrottna, eins og t.d. reikningar, kreditreikningar og greiðslur.

Við flytjum aðeins fullar upphæðir í sölu- og innkaupaskjöl. Við uppfærum ekki upphæðir greiddar að hluta. Ef viðskiptamaður hefur t.d. borgað 300 af 500 dollurum á sölureikningi, flytjum við fulla upphæð eða 500. Ef þú hefur fengið greiddan hluta af greiðslum, þarf að uppfæra þær handvirkt, annað hvort áður eða eftir að þú flytur gögn. Við mælum með því að þú jafnir útistandandi færslur áður en þú flytur gögn, bara til þess að gera eftirleikinn auðveldari.

> [!NOTE]  
>   Við flytjum ekki innkaupapantanir eða sölupantanir.

## <a name="before-you-start"></a>Verður að byrja fyrir
Mikilvægur hluti flutningsferlisins er að tilgreina reikningana sem flytja á færslur til. Það er tilvalið að skipuleggja vörpunina áður en þú flytur gögn. Til dæmis, reikningana sem þú bókar færslurnar fyrir:  

* Sala vöru eða þjónustu til viðskiptamanna.
* Innkaup vöru eða þjónustu frá lánardrottnum.  
* Leiðréttingar í fjárhagnum.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]  krefst þess að fjárhagsreikningum hafi verið úthlutað reikningsnúmerum. Vertu viss um að reikningsnúmerum hafi verið úthlutað til reikninganna í QuickBooks Online.

Ef færslur í QuickBooks Online hafa skattaupphæðir, þarf að setja upp skattareikning fyrir þína skattalögsögu í [!INCLUDE[d365fin](includes/d365fin_md.md)] áður en þú getur bókað færslur.

## <a name="how-do-i-start-using-the-extension"></a>Hvernig byrja ég að nota viðbótina?
Auðvelt er að hefjast handa Það eina sem þú þarft að gera er að keyra **Gagnaflutingur** uppsetningu með aðstoðarleiðbeiningum. Svona er það gert:

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning með aðstoð** og velja síðan **Flytja viðskiptagögn**.
2. Fylgdu leiðbeiningunum fyrir hvert skrefi í Uppsetningu með aðstoð.

## <a name="what-do-i-do-after-i-migrate-data"></a>Hvað geri ég eftir gagnaflutninginn?
Þegar gagnaflutningi er lokið, hafa færslur stöðuna **Óbókaðar**, svo þú getur endurskoðað þær og gert leiðréttingar. Til að endurskoða færslurnar, skal farið á síðuna þar þú myndir venjulega finna þær. Til dæmis, til að endurskoða óbókaða sölureikninga, skal farið á síðuna **Sölureikningar**. Til að endurskoða greiðslubækur, skal fara á síðuna **Greiðslubækur**.   

Það eru einkum nokkrir hlutir sem þú þarft að gera:

* Ef færslurnar í QuickBooks Online höfðu breytingarmerkingar eða afsláttarupphæð, verður að bæta upphæðunum handvirkt við tengdar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] áður en þú bókar þær.
* Ef þú ert að nota VSK, þarftu kannski að bæta viðskiptabókunarflokki og vörubókunarflokki við uppsetningu bókana svo þú getir bókað VSK upphæðir.
* Staðfesta upphafsstöðu reikninga í fjárhagnum. QuickBooks Online geymir ekki núgildandi stöðu fyrir alla reikninga, og því gætirðu þurft að leiðrétta upphafstöður.

## <a name="see-also"></a>Sjá einnig
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  

