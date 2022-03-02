---
title: Flytja inn aðalgögn fyrirtækisins í Excel
description: Þú getur flutt út fjárhagsskýrslur og gögn um viðskiptagreind frá Business Central yfir í Excel, eða opnað gögnin í Excel.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.search.form: 9901, 9018, 9020, 9022, 9027
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3161c51160790b2fcc4e702866025e501167b644
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335605"
---
# <a name="exporting-your-business-data-to-excel"></a>Flutningur viðskiptagagna í Excel
Ef ætlunin er að vinna með gögn frá [!INCLUDE[prod_short](includes/prod_short.md)] í Excel, er hægt að opna alla lista í Excel og vinna með þá þar. Með sama hætti, ef notandi vill hætta í áskrift að [!INCLUDE[prod_short](includes/prod_short.md)] getur hann flutt gögnin sín út í Excel svo hann geti tekið þau með sér.

## <a name="opening-lists-in-excel"></a>Opnar lista í Excel
Hægt er að opna gögn í Excel úr hvaða færslubók, lista eða vinnublaði sem er. Notandinn opnar bara síðuna sem hann vill nota og velur svo **Opna í Excel**. Til dæmis, opnar lista yfir viðskiptamenn (leitar að **Viðskiptamenn**), og velur svo **Opna í Excel**. Vafrinn sendir áminningu um að opna að vista myndaða Excel-vinnubók.  

> [!NOTE]
> Notaðu þennan valkost þegar þú vilt ekki gera breytingar og birta þessar breytingar aftur í [!INCLUDE[prod_short](includes/prod_short.md)].  

Hver listi inniheldur nokkra dálka og útflutningur í Excel tekur með alla dálka sem eru í núgildandi yfirliti. Eigi að bæta við eða fjarlægja dálka áður en listinn er opnaður í Excel þarf aðeins að opna flýtivalmyndina fyrir einhvern dálkanna og tilgreina hvaða dálka eigi að skoða. Listi yfir dálka er mismunandi fyrir flesta lista og endurspeglar bygginguna í gagnagrunninum þar sem gögnin eru geymd. Ef vafi leikur á hvers konar gögn tiltekinn dálkur inniheldur er hægt að bæta honum við yfirlitið og fjarlægja hann svo aftur.  

### <a name="edit-data-in-excel"></a>Breyta gögnum í Excel
Upplifun þín af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur innbót fyrir Excel svo þú getir breytt gögnum í Excel. Frekari upplýsingar eru í [Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Flytja út gögn í önnur fjárhagskerfi
Ef notandi ákveður að hætta í áskrift að [!INCLUDE[prod_short](includes/prod_short.md)], getur hann flutt gögnin sín út í Excel og tekið þau með sér í næsta fjárhagskerfi.  

Að sjálfsögðu er hægt að flytja út allar síður en það gæti verið meira en notandi þarf í raun á að halda. Notandi skal því íhuga að flytja út eftirfarandi veigamiklar síður og muna að bæta öllum dálkum við eins og lýst var áður:  

* Bókhaldslykill  
* Viðskiptavinir  
* Lánardrottnar  
* Bankar  
* Birgðir  

Ef notandi vill einnig hafa allar fjárhagsfærslur með líka er það mjög mikið magn af gögnum og útflutningur mun því oft taka meira en nokkrar mínútur. Fjárhagsfærslurnar eru sýndar á síðunni **Fjárhagsfærslur**.  

Við mælum með að notandi íhugi einnig að flytja út gögn af eftirfarandi síðum:  

* Viðskm.færslur  
* Lánardr.færslur  
* Bankareikningsfærslur  
* Birgðafærslur  
* Almennur bókunargrunnur  
* Bókunarflokkar viðskm.  
* Bókunarflokkar lánardrottna  
* Bókunarflokkar vöru  
* Bókunarflokkur banka  
* Fjárhagsáætlanir  
* Fjárhagsáætl.færslur  
* Sölutilboð  
* Sölureikningar  
* Innkaupareikningar  
* Tengiliður  
* Sölumenn  

> [!NOTE]  
> Ef notandi hefur sett upp fleiri en eitt fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)] verður einnig að flytja út viðeigandi gögn úr hverju fyrirtæki.

> [!NOTE]
> Þú verður að hafa að minnsta kosti eina af eftirfarandi heimildum til að opna eða breyta gögnum í Excel:
>    - Heimildasamstæða *D365 Excel útflutningsaðgerð*  
>    - Kerfisheimild 6110 *Leyfa útflutning aðgerðar í Excel*.  

Frekari upplýsingar er að finna í [Að fá yfirlit yfir leyfi notanda](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Uppsögn áskriftar að [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Fjármál](finance.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]