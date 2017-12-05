---
title: "Flytja út gögn úr Financials í Excel | Microsoft Docs"
description: "Þú getur flutt út fjárhagsskýrslur og gögn um viðskiptagreind úr Dynamics 365 Business edition yfir í Excel, eða opnað Financials gögnin í Excel."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 36d3e31300fbdc3a29f345a331cabbf50875c77f
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="exporting-your-business-data-to-excel"></a>Flutningur viðskiptagagna í Excel
Ef ætlunin er að vinna með gögn frá [!INCLUDE[d365fin](includes/d365fin_md.md)] í Excel, er hægt að opna alla lista í Excel og vinna með þá þar. Með sama hætti, ef notandi vill hætta í áskrift að [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] getur hann flutt gögnin sín út í Excel svo hann geti tekið þau með sér.

## <a name="opening-lists-in-excel"></a>Opnar lista í Excel
Hægt er að opna gögn í Excel úr hvaða færslubók, lista eða vinnublaði sem er. Notandinn opnar bara síðuna sem hann vill nota og velur svo **Opna í Excel**. Til dæmis, opnar lista yfir viðskiptamenn (leitar að **Viðskiptamenn**), og velur svo **Opna í Excel**. Vafrinn sendir áminningu um að opna að vista myndaða Excel-vinnubók.  

Hver listi inniheldur nokkra dálka og útflutningur í Excel tekur með alla dálka sem eru í núgildandi yfirliti. Eigi að bæta við eða fjarlægja dálka áður en listinn er opnaður í Excel þarf aðeins að opna flýtivalmyndina fyrir einhvern dálkanna og tilgreina hvaða dálka eigi að skoða. Listi yfir dálka er mismunandi fyrir flesta lista og endurspeglar bygginguna í gagnagrunninum þar sem gögnin eru geymd. Ef vafi leikur á hvers konar gögn tiltekinn dálkur inniheldur er hægt að bæta honum við yfirlitið og fjarlægja hann svo aftur.  

## <a name="exporting-data-to-other-finance-systems"></a>Flytja út gögn í önnur fjárhagskerfi
Ef notandi ákveður að hætta í áskrift að [!INCLUDE[d365fin](includes/d365fin_md.md)], getur hann flutt gögnin sín út í Excel og tekið þau með sér í næsta fjárhagskerfi.  

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
>   Ef notandi hefur sett upp fleiri en eitt fyrirtæki í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] verður einnig að flytja út viðeigandi gögn úr hverju fyrirtæki.

## <a name="see-also"></a>Sjá einnig
[Uppsögn áskriftar að [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](madeira-cancel.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Fjármál](finance.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  

