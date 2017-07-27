---
title: "GIFI kóðar í Kanada| Microsoft Docs"
Description: "Í Kanada er hægt að setja upp kóða fyrir Almenna atriðaskrá um fjárhagsupplýsingar (GIFI) og úthluta þeim til bókunarreikninga."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Hvernig á að: Vinna með GIFI kóða í Kanada
Fjárhagsupplýsingar geta innihaldið fjárhagsreikninga, skýrslur, rekstrarreikninga, efnahagsreikninga og yfirlit yfir óráðstafað eigið fé. Fjárhagsupplýsingar eru flokkaðar með kóðum. Notkun kóða hjálpar hinu opinbera að vinna upplýsingar, undirbúa rafræn skattskil og staðfesta upplýsingar um skatta rafrænt. Notkun kóða auðveldar einnig hagstofum og slíkum stofnunum vinnuna, þar sem fjárhagsupplýsingar eru aðgengilegri. Nánari upplýsingar eru á vefsíðu [Tekjuskrifstofu Kanada](http://www.cra-arc.gc.ca/).

Tekjuskrifstofa Kanada notar kóða úr Almennri atriðaskrá um fjárhagsupplýsingar (General Index of Financial Information, GIFI) til að safna saman, sannprófa, og vinna ársreikninga og vsk-upplýsingar rafrænt. Það er best að úthluta GIFI kóðum aðeins á bókunarreikninga, til þess að allar samtölur séu gerðar af hugbúnaðinum sem notaður er fyrir undirbúning vsk-skatts.

Þegar reikningur er tengdur GIFI kóða er hann skráður í tekjuskrifstofunni undir þeim kóða. Margir sameinaðir reikningar geta haft sama GIFI kóða, en hver reikningur getur aðeins haft einn GIFI kóða.

Hægt er að flytja út upplýsingar um stöðu eftir GIFI kóða og vista útfluttu skrána í Excel, sem er gagnlegt við að flytja upplýsingar til hugbúnaðarins sem notaður er fyrir undirbúning vsk-skatts.

## <a name="to-set-up-gifi-codes"></a>Uppsetning GIFI kóða
Í Dynamics NAV þarf að setja upp GIFI kóða fyrir fjárhagsreikninga, skýrslur, efnahagsreikninga, tekjureikninga og yfirlit yfir óráðstafað eigið fé.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **GIFI-kóðar** og velja svo viðeigandi tengil.
2. Í glugganum **GIFI kóðar** skal velja aðgerðina **Nýtt**.
3. Setjið upp GIFI kóða með því að fylla í reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>Til að tengja GIFI kóða við fjárhagsreikninga
Til að tilkynna fjárhagslegar upplýsingar eftir GIFI kóða þarf hver GIFI kóði að vera tengdur við viðeigandi reikninga í bókhaldslyklinum.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.
2. Veljið viðeigandi fjárhagsreikning og veljið svo aðgerðina **Breyta**.
3. Í flýtiflipanum **Kostnaðarbókhald** í svæðinu **GIFI kóði** er viðeigandi GIFI kóði valinn.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Til að skoða reikningsstöður með GIFI kóða skýrslunni.
Hægt er að skoða stöðu reikninga eftir GIFI kóða með því að nota skýrsluna **Staða reikninga eftir GIFI kóða**.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningsstaða eftir GIFI-kóðum** og velja svo viðeigandi tengil.
2. Tilgreina þarf hvað eigi að taka með í skýrslunni með því að fylla í reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="to-export-balance-information-using-gifi-codes"></a>Til að flytja út reikningsupplýsingar með því að nota GIFI kóða
Hægt er að flytja út reikningsupplýsingar með því að nota GIFI kóða og vista útfluttu skrána í Excel. Hægt er að breyta, vista eða eyða skrám. Skrána má nota til að flytja upplýsingar til hugbúnaðarins sem notaður er fyrir undirbúning vsk-skatts.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Flytja GIFI upplýsingar í Excel** og velja svo viðeigandi tengil.
2. Skilgreina þarf hvað eigi að flytja út í Excel með því að fylla í reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja hnappinn **Í lagi**.

> [!NOTE]  
>   Excel-skráin hefur eftirfarandi eiginleika:

* Staðan er sléttuð í næstu prósentu en gildi reitsins viðheldur sömu prósentu og í fjárhag.
* Neikvæð númer eru sýnd sem jákvæð númer í svigum. Í samræmi við það er talan -123 sýnd sem (123).

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)   
[Uppsetning Fjármála](finance-setup-finance.md)

