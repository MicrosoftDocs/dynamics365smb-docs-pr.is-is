---
title: Setja upp Staðsetningarspjald og skilgreina flutningsleiðir (inniheldur myndskeið)
description: Ef vörur eru keyptar, geymdar eða seldar á fleiri en einum stað eða vöruhúsi þarf að setja hverja staðsetningu upp með staðsetningarspjaldi og skilgreina flutningsleiðir.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9de6580971f25d092de474c0720b86fab420bbf8
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515512"
---
# <a name="set-up-locations"></a>Uppsetning birgðageymsla

Staðsetningar eru staðir eins og vöruhús þar sem notandi kaupir, geymir eða selur vörur. [!INCLUDE [prod_short](includes/prod_short.md)] notar Staðsetningar til að halda utan um birgðir í bæði einföldum og flóknum vöruhúsaferlum.

Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða. Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Staðsetningarspjöld
Upplýsingar um birgðageymslu, eins og vöruhús eða dreifingarmiðstöð, eru á **síðunni Birgðageymsluspjald**. Hver geymsla fær heiti og kóða. Hægt er að færa birgðageymslukóðann inn annars staðar í forritinu þegar skrá þarf færslur vegna tiltekinnar birgðageymslu.  

Hægt er að færa inn upplýsingar um hólf og um skipan vöruhússins fyrir hverja staðsetningu. Það fer eftir vöruhúsaskipaninni sem er valin, en hægt er að nota valkostina á flýtiflipanum **Hólf** til að skilgreina hólfin sem verða notuð sem sjálfgefin hólf þegar millifærslur fara fram. Ef notaður er beinn frágangur og tínsla er hægt að nota flesta kostina á flýtuflipanum **Hólf** til að tilgreina hvernig eigi að nota mismunandi þróaðar vöruhúsaaðgerðir.  

Sumir valreitir fara eftir stillingum á **síðunni Birgðageymsluspjald** til að takmarka óstuddar uppsetningarsamsetningar.  

**Veldu svæðin** eða **bingóaðgerðir** til að skoða upplýsingar um svæði og hólf sem eru skilgreind fyrir birgðageymsluna.

### <a name="to-set-up-a-location"></a>Staðsetning sett upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.

> [!NOTE]  
> Margir reitir á birgðageymsluspjaldinu tengjast meðhöndlun vara í ferlum á innleið og útleið í vöruhúsi. Þessi svæði eiga ekki við fyrirtæki sem krefjast ekki flókinnar vöruhúsaaðgerða. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Hægt er að breyta uppsetningu staðsetninga síðar en ekki er hægt að breyta uppsetningu staðsetninga sem hafa birgðafærslur.  

Ef þú ert með marga staði getur þú skilgreint flutningsleiðir á milli birgðageymslna. Frekari upplýsingar er að finna [í til að stofna flutningsleið](inventory-how-setup-locations.md#to-create-a-transfer-route). 

### <a name="to-create-a-transfer-route"></a>Flutningsleið búin til

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningsleiðir** og velja síðan viðkomandi tengil.
2. Að öðrum kosti, frá hvaða síðu **Staðsetningarspjalds** sem er má velja aðgerðina **Flutningsleiðir**.
3. Valið er **Nýtt** aðgerð.
4. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nú er hægt að flytja birgðavörur milli tveggja staða. Nánari upplýsingar eru í [Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Hólf

Hólf tákna grunnvöruhúsauppbyggingu og eru notuð til að gera tillögur að staðsetningu vöru. Þegar búið er að stofna hólfin er hægt að skilgreina innihald þeirra eða þau geta virkað sem fljótandi hólf án þess að efni sé tilgreint. Hólf eru aðallega notuð við grunn- og ítarlegar vöruhúsaðgerðir. Ef þú hefur umsjón með birgðum í einfaldari uppsetningu er líklega ekki þörf á hólfum.

Til að nota hólfaaðgerðina á staðnum virkjast virkinn á síðunni Birgðageymsluspjald **með því að velja** reitinn hólf áskilin **á** fastflipanum vöruhús **.** Síðan er vöruflæðið í birgðageymslunni útbúið með því að tilgreina hólfakóða í uppsetningarreitum sem tákna ólík flæði.

> [!NOTE]
> Áður en hægt er að tilgreina hólfakóta á staðsetningu verður að stofna hólfakóta. Nánari upplýsingar er að finna í [Setja upp hólf](warehouse-how-to-create-individual-bins.md) og [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Svæði

Ef stofna á hólfin á svæðum má gera það á síðunni **Svæði**.

[!INCLUDE [prod_short](includes/prod_short.md)] afritar reitina sem stilltir eru fyrir eitthvað tiltekið svæði í hólfin innan þess. Þannig er hægt að úthluta svæði á hólf eða hólfasniðmát (afmörkun hólfa) og nokkrir aðrir reitir fyllast síðan út sjálfkrafa.

Hins vegar er hægt að velja að setja bara upp eitt svæði og skipuleggja vöruhúsið aðeins eftir hólfum. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Sjálfgefnar víddir staðsetningar
Settar eru upp sjálfgefnar víddir fyrir staðsetningu á **síðunni Birgðageymsluspjald** með því að velja **staðsetningu** og svo **víddir**. Sjálfgefnar víddir staðsetningar eru afritaðar í færslubækur og fylgiskjöl þegar birgðageymslan er tilgreind í línu en hægt er að eyða eða breyta víddinni í línunni ef þörf krefur. Hægt er að krefjast þess að fólk tilgreini víddir fyrir tiltekna staði áður en þeir geta bókað færslu. Einnig er hægt að taka með víddargildin birgðageymsluvíddir í **sjálfgefinni forgangsröð** og **víddarsamsetningum** fyrir samsetningar forgangs og víddarreglna.

## <a name="see-also"></a>Sjá einnig

[Stjórna birgðum](inventory-manage-inventory.md)  
[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  
[Stofna hólf](warehouse-how-to-create-individual-bins.md)  
[Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]