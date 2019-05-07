---
title: Uppsetning staðlaðra lína fyrir ítrekaða sölu og innkaup | Microsoft Docs
description: Hægt er að setja upp sölu- og innkaupalínur sem eru ítrekaðar og síðan færa þær inn í sölu- og innkaupaskjöl og fylla þannig á fljótlegan hátt út í línurnar með stöðluðum upplýsingum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 35395ad71dbc0717410ed5a910f5bcd0170b1d8c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "936789"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Stofna ítrekaðar sölu- og innkaupalínur
Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp staðlaðar línur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.  

Eftirfarandi ferli sýna hvernig skal vinna með staðlaðar sölulínur á sölureikningi. Það virkar á svipaðan hátt fyrir öll önnur söluskjöl og innkaupaskjöl.  

## <a name="to-set-up-standard-sales-lines"></a>Hvernig á að setja upp staðlaðar sölulínur  
1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðlaðar sölulínur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Staðlaðar sölulínur** skal velja aðgerðina **Nýtt**.  
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Á flýtiflipanum **Línur** skal færa inn upplýsingar í reitina til að undirbúa sölulínur sem endurspegla hinar stöðluðu línur sem þú býst við að nota sem endurteknar línur í söluskjölum.  

> [!NOTE]
> Þú getur ekki skilgreint verð á stöðluðum sölulínum vegna þess að verð, afslættir o.s.frv. er reiknað út á raunverulegu söluskjölunum eftir að þú hefur sett inn staðlaðar sölulínur.

## <a name="to-assign-standard-sales-lines-to-a-customers"></a>Stöðluðum sölulínum úthlutað á viðskiptamenn
Úthlutaðu einum eða fleiri stöðluðum sölulínum til viðskiptavina þannig að hægt sé að setja þá inn á söluskjöl fyrir þann viðskiptavin.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna spjaldið fyrir viðeigandi viðskiptamann.
3. Veljið aðgerðina **Endurteknar sölulínur**.
4. Á síðunni **Endurteknar sölulínur** skal velja kóða fyrir endurteknar sölulínur sem þú vilt geta sett inn á söluskjal fyrir viðskiptavininn.
5. Fylltu út viðbótarreitina til að skilgreina hvenær, hvernig og hvar eigi að nota endurteknar sölulínur. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Endurteknar sölulínur settar inn í sölureikning
Ef endurteknar sölulínur eru til fyrir viðskiptavininn getur þú sett þær inn á allar gerðir söluskjala, t.d. sölureikning. Ef þú hefur virkjað tilkynninguna sem um ræðir, færðu að vita ef endurteknar sölulínur eru til staðar.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Reikningar** og veldu síðan tengda tengilinn.
2. Opnið sölureikningur sem á að setja eina eða fleiri staðlaðar sölulínur inn í.
3. Veljið aðgerðina **Sækja endurteknar sölulínur**.
4. Á síðunni **Endurteknar sölulínur** skal velja uppflettihnappinn á reitnum **Kóði** og síðan velja síðan safn staðlaðra sölulína.

    > [!NOTE]
    > Til að nota sett af ítrekaðar sölulínur með **Búa til ítrekaða sölureikningar** runuvinnslunni, þarftu einnig að fylla inn **Gildir frá dagsetningunni** og **Gildir til dagsetningarinnar** á síðunni **Ítrekaðar sölulínur**. Nánari upplýsingar er að finna í [Að búa til marga sölureikninga með hliðsjón af stöðluðum sölulínum](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Veldu **Í lagi** hnappinn til að setja staðlaðar sölulínur á reikninginn þar sem þú getur endurnýtt þau eins og þær eru eða breyttu upplýsingunum.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Stofna marga sölureikninga byggða á stöðluðum sölulínum
Hægt er að nota runuvinnsluna **Stofna ítrekaða sölureikninga** til að stofna sölureikninga samkvæmt stöðluðum sölulínum sem eru tengdar við viðskiptamenn og með bókunardagsetningum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í stöðluðum sölulínum.

> [!NOTE]
> Á síðunni **Endurteknar sölulínur** er einnig hægt að tilgreina greiðsluaðferð fyrir beingreiðslu og beingreiðsluumboð. Sölureikningar sem eru stofnaðir með runuvinnslunni **Stofna ítrekaða sölureikninga** munu þá innihalda upplýsingar sem krafist er til að innheimta greiðslu fyrir sölureikninga með SEPA-beingreiðslu. Nánari upplýsingar má nálgast á [Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Búa til ítrekaða Sölureikningar** og veldu síðan tengda tengilinn.
2. Á síðunni **Búa til ítrekaða sölureikningar** skaltu fylla inn reitina eftir þörfum.
3. Í **Kóði** síureit skal slá inn kóðann fyrir staðlaðar sölulínur sem eru úthlutað til viðskiptamanns sem þú vilt búa til sölureikninga fyrir.
4. Velja hnappinn **Í lagi**.

Sölureikningar eru stofnaðir fyrir viðskiptamenn með stöðluðum sölukóða viðskiptamanna og öllum tilgreindum upplýsingum um beingreiðslur, fyrir bókun á tilteknum degi.

## <a name="see-also"></a>Sjá einnig  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
