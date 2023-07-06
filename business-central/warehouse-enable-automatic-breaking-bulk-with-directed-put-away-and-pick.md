---
title: Einingaskipti með beinum frágangi og tínslu
description: 'Kynntu þér hvernig á að virkja sjálfvirk einingaskipti með beinum frágangi og tínslu ásamt því að einingaskipta í tínslum, frágangi, hreyfingum og fleira.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Virkja sjálfvirk einingaskipti með beinum frágangi og tínslu

Fyrir birgðageymslur sem nota beinan frágang og tínslu getur [!INCLUDE[prod_short](includes/prod_short.md)] skipt stærri mælieiningum niður í smærri mælieiningar þegar stofnaðar eru vöruhúsaleiðbeiningar fyrir upprunaskjöl, framleiðslupantanir eða innri tínslu og frágang. Að einingaskipta getur einnig þýtt að safna saman vörum í smærri mælieiningum sem jafngilda magni stærri mælieiningar í upprunaskjali eða framleiðslupöntun.

## <a name="breakbulk-in-picks"></a><a name="breakbulk-in-picks"></a><a name="breakbulk-in-picks"></a>Einingaskipti í tínslum

Ef þú vilt geyma vörur í nokkrum mismunandi mælieiningum í birgðageymslu og leyfa að sameina þær sjálfkrafa í tínsluferlinu skaltu kveikja á **Leyfa einingaskipti** í birgðageymsluspjaldinu. Eftir á, til að uppfylla verk mun [!INCLUDE [prod_short](includes/prod_short.md)] leita að vöru í sömu mælieiningunni. Ef ekkert finnst mun [!INCLUDE [prod_short](includes/prod_short.md)] stinga upp á því að skipta niður stærri mælieiningu í mælieiningu sem þarf.  

Ef aðeins smærri mælieiningar eru í boði mun [!INCLUDE [prod_short](includes/prod_short.md)] stinga upp á því að safna saman vörur til að uppfylla magnið í afhendingu eða framleiðslupöntun. Í raun er stærri mælieiningunum á upprunaskjalinu í smærri einingar fyrir tínslu.  

## <a name="breakbulk-in-put-aways"></a><a name="breakbulk-in-put-aways"></a><a name="breakbulk-in-put-aways"></a>Einingaskipti í frágangi

Í vöruhúsafrágangi stingur [!INCLUDE [prod_short](includes/prod_short.md)] upp á að setja aðgerðarlínur í mælieiningu frágangsins. Til dæmis gæti það stungið upp á stykkjum þótt vörurnar komi í annarri mælieiningu.  

## <a name="breakbulk-in-movements"></a><a name="breakbulk-in-movements"></a><a name="breakbulk-in-movements"></a>Einingaskipti í hreyfingum

[!INCLUDE [prod_short](includes/prod_short.md)] getur einnig einingaskipt í áfyllingarhreyfingum ef kveikt er á **Leyfa einingaskipti** á síðunni **Reikna út áfyllingu hólfs**.  

Hægt er að skoða niðurstöðu umreikninga úr einni mælieiningu í aðra í einingaskiptalínum í frágangs-, tínslu- eða hreyfingaleiðbeiningum.  

> [!NOTE]  
> Ef reiturinn **Einingaskiptaafmörkun** er valinn í haus vöruhúsaleiðbeininga mun forritið fela einingaskiptalínur þegar stærri mælieiningin mun verða notuð að fullu. Ef til dæmis 12 stykki eru á bretti og nota á öll 12 stykkin mun tínslan þá benda þér á að taka 1 bretti og setja 12 stykki. Hins vegar, ef þú verður að tína aðeins 9 stykki eru einingaskiptu línurnar ekki faldar, jafnvel þótt þú hafir valið reitinn **Sía einingaskipta**. Línurnar eru ekki faldar því þú verður að setja hin þrjú stykkin einhvers staðar í vöruhúsið.  

> [!NOTE]  
> Ef þú vilt að mælieiningarnar virki sem best í vöruhúsinu, líka hvað varðar einingaskipti, ættirðu að reyna að:  
>
> - Setja upp grunnmælieiningu sem minnstu mælieininguna sem búist er við að unnið verði með í vöruhúsaferlum.  
> - Setja upp aukamælieiningar fyrir vöruna sem er margfeldi af grunnmælieiningunni.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Uppsetning samsetningarstjórnunarvinnu fyrir vöruhúsastjórnun](warehouse-setup-warehouse.md)[
 með](assembly-assemble-items.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
