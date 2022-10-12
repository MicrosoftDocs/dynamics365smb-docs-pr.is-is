---
title: Setja upp Staðsetningarspjald og skilgreina flutningsleiðir (inniheldur myndskeið)
description: Ef þú kaupir, geymir eða selur vörur á fleiri en einum stað getur þú stillt upp hverjum stað fyrir sig sem stað.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 07/05/2022
ms.author: bholtorf
ms.openlocfilehash: 882c7c0506439aba55d5b1c2d0cc23bd79db9d6e
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605807"
---
# <a name="set-up-locations"></a>Uppsetning birgðageymsla

Staðsetningar eru staðir eins og vöruhús þar sem notandi kaupir, geymir eða selur vörur. [!INCLUDE [prod_short](includes/prod_short.md)] notar Staðsetningar til að halda utan um birgðir í bæði einföldum og flóknum vöruhúsaferlum.

Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða. Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Staðsetningarspjöld

Upplýsingar um birgðageymslu, eins og vöruhús eða dreifingarmiðstöð, eru á **síðunni Birgðageymsluspjald**. Hver geymsla fær heiti og kóða. Hægt er að færa birgðageymslukóðann inn annars staðar í forritinu þegar skrá þarf færslur vegna tiltekinnar birgðageymslu.  

Hægt er að færa inn upplýsingar um hólf og um skipan vöruhússins fyrir hverja staðsetningu. Á eftir vöruhúsaefnunum er hægt að nota valkostina á **flipanum hólf** til að tilgreina hólfin sem á að nota sjálfgefið fyrir færslur. Ef notaður er beinn frágangur og tínsla eru Valkostirnir á **hólfsvaranum** festing sem skilgreinir hvernig nota á ítarlegar vöruhúsaaðgerðir.  

Sumir valreitir fara eftir stillingum á **síðunni Birgðageymsluspjald** til að takmarka óstuddar uppsetningarsamsetningar.  

**Veldu svæðin** eða **bingóaðgerðir** til að skoða upplýsingar um svæði og hólf sem eru skilgreind fyrir birgðageymsluna.

### <a name="to-set-up-a-location"></a>Staðsetning sett upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.

> [!NOTE]  
> Margir reitir á birgðageymsluspjaldinu tengjast meðhöndlun vara í ferlum á innleið og útleið í vöruhúsi. Þessi svæði eiga ekki við fyrirtæki sem krefjast ekki flókinnar vöruhúsaaðgerða. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Hægt er að breyta skilgreiningunni á birgðageymslu svo framarlega sem hún er ekki með birgðafærslum.  

Ef þú ert með marga staði getur þú skilgreint flutningsleiðir á milli birgðageymslna. Frekari upplýsingar er að finna [í til að stofna flutningsleið](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>Flutningsleið búin til

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningsleiðir** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
4. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nú er hægt að flytja birgðavörur milli tveggja staða. Nánari upplýsingar eru í [Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Hólf

Hólar standa fyrir grunnvöruhúsauppbyggingu og geta stungið upp á hvar setja á vörur. Hólfin geta innihaldið innihald eða verið fljótandi hólf án tiltekins innihalds. 

Ef nota á hólfaðgerðina í birgðageymslu er á **síðunni** Birgðageymsluspjald **á fastflipanum vöruhús** og kveikt á **hólfinu skylda**. Hægt er að hanna vöruflæði á staðnum með því að tilgreina hólfakóta í svæðunum fyrir ferli vöruhússins á **festiflipum hólfa** og **hólfs**.

> [!NOTE]
> Áður en hægt er að tilgreina hólfakóta á staðsetningu verður að stofna hólfakóta. Nánari upplýsingar er að finna í [Setja upp hólf](warehouse-how-to-create-individual-bins.md) og [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Svæði

Ef stofna á hólfin á svæðum má gera það á síðunni **Svæði**. Þegar hólfum er úthlutað á hólf [!INCLUDE [prod_short](includes/prod_short.md)] afritast upplýsingar úr svæðinu yfir í hólfin. Einnig er hægt að velja að setja upp eitt svæði og nota hólf ein til að skipuleggja vöruhúsið. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Sjálfgefnar víddir staðsetningar

Settar eru **upp sjálfgefnar víddir fyrir staðsetningu á síðunni Birgðageymsluspjald** með því að velja **víddir**. Eftir sem áður er sjálfgefnum víddum staðsetningar úthlutað á skjöl þegar valin er birgðageymslan í línu. Ef þörf krefur er hægt að eyða eða breyta víddinni í línunni. **Í reitnum gildisbókun** er hægt að krefjast þess að fólk tilgreini víddir staðsetningar áður en hægt er að bóka færslu. Ef ætlunin er að leyfa fólki að velja aðeins tiltekin víddargildi er hægt að tilgreina gildin í **reitnum leyfð gildi**. Einnig er hægt að taka með víddargildi staðsetningarvídda á **síðunni Forgangur** sjálfgefinnar víddar og fyrir samsetningar af forgangi og víddarreglum á **síðunni víddir vídda**.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Stjórna birgðum](inventory-manage-inventory.md)  
[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  
[Stofna hólf](warehouse-how-to-create-individual-bins.md)  
[Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
