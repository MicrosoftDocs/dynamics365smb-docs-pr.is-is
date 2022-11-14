---
title: Einingaskipti með beinum frágangi og tínslu
description: Lærðu hvernig á að gera sjálfvirka rofa magnaða með beinan frágang og tínslu, ásamt rofbulgi í tínslum, frágangi, hreyfingum og fleiru.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 5703, 7352
ms.date: 11/04/2022
ms.author: bholtorf
ms.openlocfilehash: d5e8ab6f0e60ab8874669c7e5127411acc58957b
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744678"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Virkja sjálfvirk einingaskipti með beinum frágangi og tínslu

Fyrir staðsetningar sem nota beinan frágang og tínslu er [!INCLUDE[prod_short](includes/prod_short.md)] hægt að rjúfa stærri mælieiningar í smærri mælieiningum þegar það stofnar vöruhúsaleiðbeiningar fyrir upprunaskjöl, framleiðslupantanir eða innri tínslur og frágang. Einingaskiptafjöldi getur einnig þýtt að safna vörum í smærri mælieiningar til að jafna út magn stærri mælieininga á upprunaskjali eða framleiðslupöntun.

## <a name="breakbulk-in-picks"></a>Einingamagn í pallbílum  

Ef geyma á vörur í nokkrum mismunandi mælieiningum á stað og leyfa þeim að vera sjálfkrafa sameinaðar í tiltektarferlinu skal kveikja á **Einingaskiptalaginu** á birgðageymsluspjaldinu. Eftir á til að uppfylla verk [!INCLUDE [prod_short](includes/prod_short.md)] verður að leita að vöru í sömu mælieiningu. Ef hann finnur ekki einn, [!INCLUDE [prod_short](includes/prod_short.md)] stingur upp á að þú brjóir stærri mælieiningu inn á mælieininguna sem er nauðsynleg.  

Ef aðeins smærri mælieiningar eru tiltækar [!INCLUDE [prod_short](includes/prod_short.md)] verður að leggja til að vörum sé safnað til að uppfylla magnið í afhendingunni eða framleiðslupöntuninni. Í raun er stærri mælieiningunum á upprunaskjalinu í smærri einingar fyrir tínslu.  

## <a name="breakbulk-in-put-aways"></a>Einingafrágangur í frágangi  

Í vöruhúsafrágangi er [!INCLUDE [prod_short](includes/prod_short.md)] lagt til stað aðgerðarlína í frágangsmælieiningunni. Til dæmis gæti hún stungið upp á stykkjum þó að vörurnar komi í aðra mælieiningu.  

## <a name="breakbulk-in-movements"></a>Rofmagn í hreyfingum  

[!INCLUDE [prod_short](includes/prod_short.md)] Einnig er hægt að einingamagn í áfyllingarhreyfingum ef **einingaskipti** skipta á **síðunni reikna reikningsafáfyllingar** eru kveikt.  

Hægt er að skoða niðurstöðu umreikninga úr einni mælieiningu í aðra í einingaskiptalínum í frágangs-, tínslu- eða hreyfingaleiðbeiningum.  

> [!NOTE]  
> Ef reiturinn **Einingaskiptaafmörkun** er valinn í haus vöruhúsaleiðbeininga mun forritið fela einingaskiptalínur þegar stærri mælieiningin mun verða notuð að fullu. Ef bretti eru 12 stykki og þú notar öll 12 stykkin velur tínslan þá að taka 1 bretti og setur 12 stykki. Ef hins vegar þarf að velja aðeins 9 stykki einingaskiptalínur eru ekki faldar þótt reiturinn einingaskiptaafmörkun **hafi verið valinn**. Línurnar eru ekki faldar því þá þarf að setja eftirstandandi þrjú stykki einhvers staðar í vöruhúsið.  

> [!NOTE]  
> Ef mælieiningarnar eiga að vera ákjósanlega í vöruhúsinu, einnig í tengslum við rofmagn, ætti að reyna að:  
>
> - Setja upp grunnmælieiningu sem minnstu mælieininguna sem búist er við að unnið verði með í vöruhúsaferlum.  
> - Setja upp aukamælieiningar fyrir vöruna sem er margfeldi af grunnmælieiningunni.  

## <a name="see-also"></a>Sjá einnig  

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md)
[samsetningarstýring](assembly-assemble-items.md)
[hönnunar upplýsingar: vöruhúsastjórnun](design-details-warehouse-management.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]