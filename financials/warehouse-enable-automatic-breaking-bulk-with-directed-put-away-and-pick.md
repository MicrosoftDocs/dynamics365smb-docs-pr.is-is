---
title: "Sjálfvirk einingaskipti með beinum frágangi og tínslu | Microsoft Docs"
description: "Í birgðageymslum sem nota beinan frágang og tínslu er hægt að skipta stærri mælieiningum í smærri þegar stofnaðar eru vöruhúsaleiðbeiningar sem uppfylla þarfir upprunaskjala, framleiðslupantana eða tínslu og frágangs innanhúss."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 910596b9716ff944a1e491076b599ab6c39c8859
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Hvernig skal: Virkja sjálfvirk einingaskipti með beinum frágangi og tínslu
Í birgðageymslum sem nota beinan frágang og tínslu er hægt að skipta einingum sjálfkrafa í [!INCLUDE[d365fin](includes/d365fin_md.md)], það er, skipta stærri mælieiningum í smærri þegar stofnaðar eru vöruhúsaleiðbeiningar sem uppfylla þarfir upprunaskjala, framleiðslupantana eða tínslu og frágangs innanhúss. Að skipta einingum getur stundum einnig þýtt að safna saman smærri mælieiningum, ef með þarf, til að mæta útleiðarbeiðnum með því að skipta stærri mælieiningum upprunaskjalsins eða framleiðslupöntunarinnar í smærri mælieiningar sem tiltækar eru í vöruhúsinu.   

## <a name="breakbulking-in-picks"></a>Einingum er skipt í tínslum  
Ef geyma á vörur í nokkrum mismunandi mælieiningum og leyfa að sameina þær sjálfkrafa í tínsluferlinu, skal velja reitinn **Leyfa einingaskipti** á birgðageymsluspjaldinu.  

Til að ljúka verki er sjálfkrafa leitað að vöru með sömu mælieiningu. En ef ekki er hægt að finna vöruna með þeim forsendum og reitur er valinn, verður lagt til í kerfinu að skipta stærri mælieiningu í mælieininguna sem þörf er á.  

Ef kerfið finnur aðeins smærri mælieiningar er lagt til að vöru sé safnað saman til að fylla upp í magnið í afhendingunni eða framleiðslupöntuninni. Í raun er stærri mælieiningunum á upprunaskjalinu í smærri einingar fyrir tínslu.  

## <a name="breakbulking-in-put-aways"></a>Einingum skipt í frágangi  
Í vöruhúsafrágangi eru sjálfkrafa lagðar til Setja-aðgerðarlínur í mælieiningu frágangs, til dæmis stykkjum, jafnvel þótt vörurnar berist með annarri mælieiningu.  

## <a name="breakbulking-in-movements"></a>Einingum skipt í hreyfingum  
Kerfið skiptir einingum einnig sjálfkrafa í áfyllingarhreyfingum ef sjálfgefna gátmerkið í reitnum **Leyfa einingaskipti** á flýtiflipanum **Valkostur** í glugganum **Reikna áfyllingu hólfs** er ekki fjarlægt.  

Hægt er að skoða niðurstöðu umreikninga úr einni mælieiningu í aðra í einingaskiptalínum í frágangs-, tínslu- eða hreyfingaleiðbeiningum.  

> [!NOTE]  
>  Ef reiturinn **Einingaskiptaafmörkun** er valinn í haus vöruhúsaleiðbeininga mun kerfið fela einingaskiptalínur þegar stærri mælieiningin mun verða notuð að fullu. Ef 12 stykki eru á bretti og nota á öll 12 stykkin er notandanum bent á að taka 1 bretti og setja 12 stykki. Þurfi hins vegar aðeins að tína 9 stykki eru einingaskiptalínurnar ekki faldar, jafnvel þó reiturinn **Einingaskiptaafmörkun** sé valinn því að einhvers staðar þarf að setja hin þrjú stykkin í vöruhúsinu.  

> [!NOTE]  
>  Ef mælieiningarnar eiga að skila hámarksafköstum í vöruhúsinu, einnig í tengslum við einingaskiptaaðgerðir, skal reyna eins og kostur er að:  
>   
> - Setja upp grunnmælieiningu sem minnstu mælieininguna sem búist er við að unnið verði með í vöruhúsaferlum.  
> - Setja upp aukamælieiningar fyrir vöruna sem er margfeldi af grunnmælieiningunni.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
