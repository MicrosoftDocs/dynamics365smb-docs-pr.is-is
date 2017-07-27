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
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a>Hvernig á að: Stofna ítrekaðar sölu- og innkaupalínur
Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp staðlaðar línur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.  

Eftirfarandi ferli sýnir hvernig skal vinna með staðlaðar sölulínur. Það virkar á svipaðan hátt fyrir staðlaðar innkaupalínur.  

## <a name="to-set-up-standard-sales-lines"></a>Hvernig á að setja upp staðlaðar sölulínur  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **staðlaður sölukóði** og velja svo viðeigandi tengil.  
2. Í glugganum **Staðlaðar sölulínur** skal velja aðgerðina **Nýtt**.  
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Á flýtiflipanum **Línur** skal færa inn upplýsingar í reitina til að undirbúa sölulínur sem endurspegla hinar stöðluðu línur sem þú býst við að nota sem endurteknar línur í söluskjölum.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Staðlaðar sölulínur settar inn í sölureikning
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningar** og velja svo viðeigandi tengil.
2. Opnið sölureikningur sem á að setja eina eða fleiri staðlaðar sölulínur inn í.
3. Veljið aðgerðina **Sækja endurteknar sölulínur**.
4. Í glugganum **Endurteknar sölulínur** skal velja uppflettihnappinn á reitnum **Kóði** og síðan velja síðan safn staðlaðra sölulína.
5. Velja skal **Í lagi** hnappinn til að setja staðlaðar sölulínur inn á reikninginn, þar sem þú getur endurnotað þær sem fyrir eru eða breytt upplýsingunum.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Stofna marga sölureikninga byggða á stöðluðum sölulínum
Hægt er að nota **Búa til endurtekna sölureikninga.** runuvinnsluna til að stofna sölureikninga samkvæmt stöðluðum sölulínum sem eru tengdar við viðskiptamenn og með bókunardögum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í stöðluðum sölukóða.

Í **Endurteknar sölulínur** glugganum er einnig hægt að tilgreina greiðsluaðferð fyrir beingreiðslu og beingreiðsluumboð. Sölureikningarnir sem eru stofnaðir með **Búa til endurtekna sölureikninga.** runuvinnslunni munu þá innihalda upplýsingar sem eru nauðsynlegar til innheimta greiðslu fyrir sölureikningana með SEPA-beingreiðslum. Nánari upplýsingar má nálgast á Innheimta greiðslur með SEPA-beingreiðslum

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stofna endurtekna sölureikninga** og velja svo viðeigandi tengil.
2. Í glugganum **Stofna endurtekna sölureikninga** skal fylla inn í reitina eins og þörf krefur.
3. Í reitnum **Kóði** er færður inn kóðinn fyrir staðlaðar línur sem á að úthluta til viðskiptamanns sem þú vilt stofna sölureikning fyrir.
4. Velja hnappinn **Í lagi**.

Sölureikningar eru stofnaðir fyrir viðskiptamenn með stöðluðum sölukóða viðskiptamanna og öllum tilgreindum upplýsingum um beingreiðslur, fyrir bókun á tilteknum degi.

## <a name="see-also"></a>Sjá einnig  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

