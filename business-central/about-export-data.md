---
title: Flyttu út Business Central gögnin þín í Excel
description: Þú getur flutt út fjárhagsskýrslur og gögn um viðskiptagreind frá Business Central yfir í Excel, eða opnað gögnin í Excel.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: adfb0a98f79f3e32656e6e9f6b95172e6a83dd39
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529947"
---
# <a name="export-your-business-data-to-excel" /><a name="export-your-business-data-to-excel"></a>Flytja viðskiptagögn í Excel

Excel er öflugt verkfæri til að vinna með gögn. Þar inni [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að opna hvaða lista sem er í Excel. Þú getur jafnvel breytt gögnum í Excel og sent þau svo aftur í [!INCLUDE [prod_short](includes/prod_short.md)]. Með sama möguleika er auðvelt að taka gögnin með sér ef þú ákveður að segja upp áskriftinni.

## <a name="opening-lists-in-excel" /><a name="opening-lists-in-excel"></a>Opnar lista í Excel

Hægt er að opna gögn í Excel úr hvaða færslubók, lista eða vinnublaði sem er. Notandinn opnar bara síðuna sem hann vill nota og velur svo **Opna í Excel**. Til dæmis, opnar lista yfir viðskiptamenn (leitar að **Viðskiptamenn**), og velur svo **Opna í Excel**. Vafrinn sendir áminningu um að opna að vista myndaða Excel-vinnubók.  

> [!NOTE]
> Notaðu þennan valkost þegar þú vilt ekki gera breytingar og birta þessar breytingar aftur í [!INCLUDE[prod_short](includes/prod_short.md)].  

Hver listi inniheldur nokkra dálka. Útflutningur í Excel inniheldur alla dálka sem eru í núverandi yfirlit. Breyta dálkum með því að opna flýtivalmynd fyrir hvaða dálk sem er og tilgreina svo hvaða dálka á að sjá. Dálkalistinn er mismunandi fyrir flesta lista. Dálkarnir endurspegla uppbyggingu gagnagrunnsins sem geymir gögnin þín. Ef þú ert ekki viss um hvaða tegund gagna tiltekinn dálkur inniheldur skaltu bæta þeim við yfirlitið. Það er alltaf hægt að fjarlægja þá aftur.  

### <a name="edit-data-in-excel" /><a name="edit-data-in-excel"></a>Breyta gögnum í Excel

Upplifun þín af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur innbót fyrir Excel svo þú getir breytt gögnum í Excel. Frekari upplýsingar eru í [Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems" /><a name="exporting-data-to-other-finance-systems"></a>Flytja út gögn í önnur fjárhagskerfi

Ef notandi ákveður að hætta í áskrift að [!INCLUDE[prod_short](includes/prod_short.md)], getur hann flutt gögnin sín út í Excel og tekið þau með sér í næsta fjárhagskerfi.  

Hægt er að flytja út allar síður en það gæti verið meira en notandi þarf í raun á að halda. Notandi skal því íhuga að flytja út eftirfarandi veigamiklar síður og muna að bæta öllum dálkum við eins og lýst var áður:  

* Bókhaldslykill  
* Viðskiptavinir  
* Lánardrottnar  
* Bankar  
* Vörur  

Ef einnig á að hafa allar fjárhagsfærslur með líka er það mjög mikið magn af gögnum og útflutningur mun því oft taka meira en nokkrar mínútur. Fjárhagsfærslurnar eru sýndar á síðunni **Fjárhagsfærslur**.  

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
>
> * Heimildasamstæða *D365 Excel útflutningsaðgerð*  
> * Kerfisheimild 6110 *Leyfa útflutning aðgerðar í Excel*.  

Frekari upplýsingar er að finna í [Að fá yfirlit yfir leyfi notanda](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" /><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" /><a name="see-also"></a>Sjá einnig
[Uppsögn áskriftar að [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Fjármál](finance.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
