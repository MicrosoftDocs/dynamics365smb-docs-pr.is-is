---
title: "Uppsetning og notkun staðlaðra lína fyrir ítrekaða sölu og innkaup | Microsoft Docs"
description: "Hægt er að setja upp sölu- og innkaupalínur sem eru ítrekaðar og síðan færa þær inn í sölu- og innkaupaskjöl og fylla þannig á fljótlegan hátt út í línurnar með stöðluðum upplýsingum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7c5820db4d8aa65ddeddfd5ee27f0a7e89100abf
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Stofna ítrekaðar sölu- og innkaupalínur
Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp staðlaðar línur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.  

Eftirfarandi ferli sýnir hvernig skal vinna með staðlaðar sölulínur. Það virkar á svipaðan hátt fyrir staðlaðar innkaupalínur.  

## <a name="to-set-up-standard-sales-lines"></a>Hvernig á að setja upp staðlaðar sölulínur  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **staðlaður sölukóði** og velja svo viðeigandi tengil.  
2. Í glugganum **Staðlaðar sölulínur** skal velja aðgerðina **Nýtt**.  
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Á flýtiflipanum **Línur** skal færa inn upplýsingar í reitina til að undirbúa sölulínur sem endurspegla hinar stöðluðu línur sem þú býst við að nota sem endurteknar línur í söluskjölum.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Staðlaðar sölulínur settar inn í sölureikning
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningar** og velja svo viðeigandi tengil.
2. Opnið sölureikningur sem á að setja eina eða fleiri staðlaðar sölulínur inn í.
3. Veljið aðgerðina **Sækja endurteknar sölulínur**.
4. Í glugganum **Endurteknar sölulínur** skal velja uppflettihnappinn á reitnum **Kóði** og síðan velja síðan safn staðlaðra sölulína.
5. Velja skal **Í lagi** hnappinn til að setja staðlaðar sölulínur inn á reikninginn, þar sem þú getur endurnotað þær sem fyrir eru eða breytt upplýsingunum.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Stofna marga sölureikninga byggða á stöðluðum sölulínum
Hægt er að nota runuvinnsluna **Stofna ítrekaða sölureikninga** til að stofna sölureikninga samkvæmt stöðluðum sölulínum sem eru tengdar við viðskiptamenn og með bókunardögum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í stöðluðum sölukóða.

Í **Endurteknar sölulínur** glugganum er einnig hægt að tilgreina greiðsluaðferð fyrir beingreiðslu og beingreiðsluumboð. Sölureikningar sem eru stofnaðir með runuvinnslunni **Stofna ítrekaða sölureikninga** munu þá innihalda upplýsingar sem krafist er til að innheimta greiðslu fyrir sölureikninga með SEPA-beingreiðslu. Nánari upplýsingar má nálgast á [Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stofna endurtekna sölureikninga** og velja svo viðeigandi tengil.
2. Í glugganum **Búa til endurtekna sölureikninga** þarf að fylla reitina út eftir þörfum.
3. Í reitnum **Kóði** er færður inn kóðinn fyrir staðlaðar línur sem á að úthluta til viðskiptamanns sem þú vilt stofna sölureikning fyrir.
4. Velja hnappinn **Í lagi**.

Sölureikningar eru stofnaðir fyrir viðskiptamenn með stöðluðum sölukóða viðskiptamanna og öllum tilgreindum upplýsingum um beingreiðslur, fyrir bókun á tilteknum degi.

## <a name="see-also"></a>Sjá einnig  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

