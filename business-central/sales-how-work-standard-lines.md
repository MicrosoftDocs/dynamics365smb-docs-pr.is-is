---
title: Staðlaðar endurteknar sölulínur
description: Setja upp sölulínur sem eru oft notaðar til að setja þær inn í söluskjöl og fylla fljótt út línurnar með stöðluðum upplýsingum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.search.form: 172
ms.date: 07/06/2022
ms.author: edupont
ms.openlocfilehash: 1d4223bb324a10644e0974f8b92564f5bf85dce2
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535617"
---
# <a name="create-recurring-sales"></a>Stofna endurtekna sölu

Ef oft þarf að stofna sölulínur með svipuðum upplýsingum er hægt að setja upp staðlaðar línur sem síðan er hægt að setja inn í ítrekunarsöluskjöl, til dæmis fyrir endurteknar áfyllingarpantanir.  

## <a name="set-up-recurring-sales-lines"></a>Setja upp endurteknar sölulínur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurteknar sölulínur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Endurteknar sölulínur** skal velja aðgerðina **Nýtt**.  
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Á flýtiflipanum **Línur** skal færa inn upplýsingar í reitina til að undirbúa sölulínur sem endurspegla hinar stöðluðu línur sem þú býst við að nota sem endurteknar línur í söluskjölum.  

> [!NOTE]
> Þú getur ekki skilgreint verð á endurteknum sölulínum vegna þess að verð, afslættir o.s.frv. er reiknað út á raunverulegu söluskjölunum eftir að þú hefur sett inn endurteknar sölulínur.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-sales-lines-to-a-customer"></a>Úthluta endurteknum sölulínum á viðskiptavin

Úthlutaðu einum eða fleiri endurteknum sölulínum til viðskiptamanns þannig að hægt sé að setja þá inn á söluskjöl fyrir þann viðskiptamann.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opna spjaldið fyrir viðeigandi viðskiptamann.
3. Veljið aðgerðina **Endurteknar sölulínur**.
4. Á síðunni **Endurteknar sölulínur** skal velja kóða fyrir endurteknar sölulínur sem þú vilt geta sett inn á söluskjal fyrir viðskiptavininn.
5. Reitirnir í öðrum reitum eru fylltir út til að skilgreina hvenær, hvernig eigi að nota endurteknar sölulínur.  

    Ef þú ætlar að nota sett af ítrekuðum sölulínu, með **Búa til ítrekaða sölureikningar** runuvinnslunni, þarftu einnig að fylla inn **Gildir frá dagsetningunni** og **Gildir til dagsetningarinnar** til að takmarka hvenær ítrekaðar sölulínur eru notaðar til að búa til reikninga. Sjá [Create a Multiple sölureikninga byggða á stöðluðum sölulínum fyrir frekari upplýsingar](sales-how-work-standard-lines.md#create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Einnig er hægt að tilgreina greiðsluaðferð fyrir beingreiðslu og beingreiðsluumboð. Sölureikningar sem eru stofnaðir með runuvinnslunni **Stofna ítrekaða sölureikninga** munu þá innihalda upplýsingar sem krafist er fyrir greiðslu með SEPA-beingreiðslu. Nánari upplýsingar má nálgast á [Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)

6. Í þeim fjórum reitum þar sem þú velur hvernig línurnar eru settar inn á fjórum skjalategundum skaltu velja einn af eftirfarandi valkostum:

|Valkostur|Description|
|------|-----------|
|**Handvirkt**|Þú verður að leita handvirkt og setja inn endurtekna sölulínu sem er til fyrir viðskiptamanninn.|
|**Sjálfvirkt**|Ef margar endurteknar sölulínur eru til fyrir viðskiptamanninn færðu tilkynningu þar sem þú getur valið hvaða á að setja inn. Ef aðeins ein endurtekin sölulína er til staðar verður hún sett inn sjálfkrafa.<br /><br />Þetta virkar aðeins ef nýja skjalið var búið til úr skjalalista, til dæmis með því að **Velja nýja** aðgerð á **síðunni sölupantanir**. Það virkar ekki ef skjalið var t.d. búið til úr viðskiptamannaspjaldi.|
|**Spyrja alltaf**|Tilkynning birtist og allar núverandi endurteknar sölulínur eru sýndar þannig að hægt er að velja eina.

## <a name="insert-recurring-sales-lines-on-a-sales-invoice"></a>Setja endurteknar sölulínur á sölureikning

Ef endurteknar sölulínur eru til fyrir viðskiptamanninn getur þú sett þær inn á allar gerðir söluskjala, t.d. sölureikning. Ef notandi hefur virkjað alltaf valkosti um endurtekna bið **á meðan verið er að úthluta endurteknum sölulínum á viðskiptamenn verður notandi upplýstur ef um** endurteknar sölulínur er að ræða.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.
2. Opnið sölureikningur sem á að setja eina eða fleiri staðlaðar sölulínur inn í.
3. Veljið aðgerðina **Sækja endurteknar sölulínur**.
4. Á síðunni **Endurteknar sölulínur** skal velja uppflettihnappinn á reitnum **Kóði** og síðan velja síðan safn staðlaðra sölulína.
5. Veldu **Í lagi** hnappinn til að setja staðlaðar sölulínur á reikninginn þar sem þú getur endurnýtt þau eins og þær eru eða breyttu upplýsingunum.

## <a name="create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Stofna marga sölureikninga byggða á endurteknum sölulínum

Hægt er að nota runuvinnsluna **Stofna ítrekaða sölureikninga** til að stofna sölureikninga samkvæmt stöðluðum sölulínum sem eru tengdar við viðskiptamenn og með bókunardagsetningum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í stöðluðum sölulínum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stofna endurtekna sölureikninga** og velja síðan viðkomandi tengil.
2. Á síðunni **Búa til ítrekaða sölureikningar** skaltu fylla inn reitina eftir þörfum.
3. Í **Kóði** síureit skal slá inn kóðann fyrir staðlaðar sölulínur sem eru úthlutað til viðskiptamanns sem þú vilt búa til sölureikninga fyrir.
4. Velja hnappinn **Í lagi**.

Sölureikningar eru stofnaðir fyrir viðskiptamenn með stöðluðum sölukóða viðskiptamanna og öllum tilgreindum upplýsingum um beingreiðslur, fyrir bókun á tilteknum degi.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Setja upp sölu](sales-setup-sales.md)  
[Stofna endurteknar innkaupalínur](purchasing-how-work-recurring-purchase-lines.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
