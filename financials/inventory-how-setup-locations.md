---
title: "Uppsetning staðsetningarspjalds og skilgreining flutningsleiða| Microsoft Docs"
description: "Þú býrð til staðsetningarspjald fyrir hvern stað sem birgðavara er geymd á, til dæmis vöruhús eða dreifingarmiðstöð, og setur upp leiðir til að flytja vörur á milli staða."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7d82b1c63bb1da367736f8dd044640b583493af8
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations"></a>Hvernig á að setja upp birgðageymslur
Ef vörur eru keyptar, geymdar eða seldar á fleiri en einum stað eða vöruhúsi þarf að setja hverja staðsetningu upp með staðsetningarspjaldi og skilgreina flutningsleiðir.

Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða. Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

## <a name="to-create-a-location-card"></a>Staðsetningarspjald búið til
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Í glugganum **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.

> [!NOTE]  
> Margir reitir á birgðageymsluspjaldinu vísa til meðhöndlunar vara í vöruhúsaferli á inn- og útleið. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md). 

## <a name="to-create-a-transfer-route"></a>Flutningsleið búin til
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Flutningsleiðir** og velja svo viðeigandi tengil.
2. Einnig, úr hvaða **Staðsetningarspjaldi** glugga sem er má velja **Flutningsleiðir**.
3. Valið er **Nýtt** aðgerð.
4. Í glugganum **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nú er hægt að flytja birgðavörur milli tveggja staða. Nánari upplýsingar eru í [Hvernig á að: Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Sjá einnig
[Stjórna birgðum](inventory-manage-inventory.md)  
[Hvernig á að: Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sérstillir þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

