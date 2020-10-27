---
title: Uppsetning staðlaðra lína fyrir ítrekaða sölu og innkaup | Microsoft Docs
description: Hægt er að setja upp sölu- og innkaupalínur sem eru ítrekaðar og síðan færa þær inn í sölu- og innkaupaskjöl og fylla þannig á fljótlegan hátt út í línurnar með stöðluðum upplýsingum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 66a0e679a97bff7071a20197c804143cf11539d2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910481"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Stofna ítrekaðar sölu- og innkaupalínur
Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp staðlaðar línur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.  

Eftirfarandi ferli sýna hvernig skal vinna með staðlaðar sölulínur á sölureikningi. Það virkar á svipaðan hátt fyrir öll önnur söluskjöl og innkaupaskjöl.  

## <a name="to-set-up-recurring-sales-lines"></a>Uppsetning endurtekinna sölulína

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Endurteknar sölulínur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Endurteknar sölulínur** skal velja aðgerðina **Nýtt** .  
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Á flýtiflipanum **Línur** skal færa inn upplýsingar í reitina til að undirbúa sölulínur sem endurspegla hinar stöðluðu línur sem þú býst við að nota sem endurteknar línur í söluskjölum.  

> [!NOTE]
> Þú getur ekki skilgreint verð á endurteknum sölulínum vegna þess að verð, afslættir o.s.frv. er reiknað út á raunverulegu söluskjölunum eftir að þú hefur sett inn endurteknar sölulínur.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>Endurteknum sölulínum úthlutað á viðskiptamann

Úthlutaðu einum eða fleiri endurteknum sölulínum til viðskiptamanns þannig að hægt sé að setja þá inn á söluskjöl fyrir þann viðskiptamann.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna spjaldið fyrir viðeigandi viðskiptamann.
3. Veljið aðgerðina **Endurteknar sölulínur** .
4. Á síðunni **Endurteknar sölulínur** skal velja kóða fyrir endurteknar sölulínur sem þú vilt geta sett inn á söluskjal fyrir viðskiptavininn.
5. Fylltu út viðbótarreitina til að skilgreina hvenær, hvernig og hvar eigi að nota endurteknar sölulínur.  

    Ef þú ætlar að nota sett af ítrekuðum sölulínu, með **Búa til ítrekaða sölureikningar** runuvinnslunni, þarftu einnig að fylla inn **Gildir frá dagsetningunni** og **Gildir til dagsetningarinnar** til að takmarka hvenær ítrekaðar sölulínur eru notaðar til að búa til reikninga. Nánari upplýsingar er að finna í [Að búa til marga sölureikninga með hliðsjón af stöðluðum sölulínum](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Einnig er hægt að tilgreina greiðsluaðferð fyrir beingreiðslu og beingreiðsluumboð. Sölureikningar sem eru stofnaðir með runuvinnslunni **Stofna ítrekaða sölureikninga** munu þá innihalda upplýsingar sem krafist er fyrir greiðslu með SEPA-beingreiðslu. Nánari upplýsingar má nálgast á [Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)

6. Í þeim fjórum reitum þar sem þú velur hvernig línurnar eru settar inn á fjórum skjalategundum skaltu velja einn af eftirfarandi valkostum:

|Valkostur|Description|
|------|-----------|
|**Handvirkt**|Þú verður að leita handvirkt og setja inn endurtekna sölulínu sem er til fyrir viðskiptamanninn.|
|**Sjálfvirkt**|Ef margar endurteknar sölulínur eru til fyrir viðskiptamanninn færðu tilkynningu þar sem þú getur valið hvaða á að setja inn. Ef aðeins ein endurtekin sölulína er til staðar verður hún sett inn sjálfkrafa.<br /><br />Athugið að þetta virkar aðeins ef nýja skjalið var búið til úr skjalalista, til dæmis með því að velja aðgerðina **Nýtt** á síðunni **Sölukynning** . Það virkar ekki ef skjalið var t.d. búið til úr viðskiptamannaspjaldi.|
|**Spyrja alltaf**|Tilkynning birtist og allar núverandi endurteknar sölulínur eru sýndar þannig að hægt er að velja eina.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Endurteknar sölulínur settar inn í sölureikning

Ef endurteknar sölulínur eru til fyrir viðskiptamanninn getur þú sett þær inn á allar gerðir söluskjala, t.d. sölureikning. Ef þú hefur virkjað valkostina **Spyrja alltaf** verður látið vita ef endurteknar sölulínur eru til.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Reikningar** og veldu síðan tengda tengilinn.
2. Opnið sölureikningur sem á að setja eina eða fleiri staðlaðar sölulínur inn í.
3. Veljið aðgerðina **Sækja endurteknar sölulínur** .
4. Á síðunni **Endurteknar sölulínur** skal velja uppflettihnappinn á reitnum **Kóði** og síðan velja síðan safn staðlaðra sölulína.
5. Veldu **Í lagi** hnappinn til að setja staðlaðar sölulínur á reikninginn þar sem þú getur endurnýtt þau eins og þær eru eða breyttu upplýsingunum.

## <a name="to-create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Stofna marga sölureikninga byggða á endurteknum sölulínum
Hægt er að nota runuvinnsluna **Stofna ítrekaða sölureikninga** til að stofna sölureikninga samkvæmt stöðluðum sölulínum sem eru tengdar við viðskiptamenn og með bókunardagsetningum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í stöðluðum sölulínum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Búa til endurtekna sölureikninga** og veldu síðan tengda tengilinn.
2. Á síðunni **Búa til ítrekaða sölureikningar** skaltu fylla inn reitina eftir þörfum.
3. Í **Kóði** síureit skal slá inn kóðann fyrir staðlaðar sölulínur sem eru úthlutað til viðskiptamanns sem þú vilt búa til sölureikninga fyrir.
4. Velja hnappinn **Í lagi** .

Sölureikningar eru stofnaðir fyrir viðskiptamenn með stöðluðum sölukóða viðskiptamanna og öllum tilgreindum upplýsingum um beingreiðslur, fyrir bókun á tilteknum degi.

## <a name="see-also"></a>Sjá einnig

[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
