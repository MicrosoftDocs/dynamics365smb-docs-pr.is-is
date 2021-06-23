---
title: Uppsetning staðsetningarspjalds og skilgreining flutningsleiða
description: Þú býrð til staðsetningarspjald fyrir hvern stað sem birgðavara er geymd á, til dæmis vöruhús eða dreifingarmiðstöð, og setur upp leiðir til að flytja vörur á milli staða.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184325"
---
# <a name="set-up-locations"></a>Uppsetning birgðageymsla

Ef vörur eru keyptar, geymdar eða seldar á fleiri en einum stað eða vöruhúsi þarf að setja hverja staðsetningu upp með staðsetningarspjaldi og skilgreina flutningsleiðir. [!INCLUDE [prod_short](includes/prod_short.md)] notar staðsetningar til að hjálpa til við að fylgjast með birgðum í bæði einfaldari tilvikum og flóknari vöruhúsferli.

Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða. Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Staðsetningarspjöld

Staðsetningarkortið tilgreinir upplýsingar um staðsetninguna, t.d. vöruhús eða dreifingarmiðstöð. Hver geymsla fær heiti og kóða. Hægt er að færa birgðageymslukóðann inn annars staðar í forritinu þegar skrá þarf færslur vegna tiltekinnar birgðageymslu.  

Hægt er að færa inn upplýsingar um hólf og um skipan vöruhússins fyrir hverja staðsetningu. Það fer eftir vöruhúsaskipaninni sem er valin, en hægt er að nota valkostina á flýtiflipanum **Hólf** til að skilgreina hólfin sem verða notuð sem sjálfgefin hólf þegar millifærslur fara fram. Ef notaður er beinn frágangur og tínsla er hægt að nota flesta kostina á flýtuflipanum **Hólf** til að tilgreina hvernig eigi að nota mismunandi þróaðar vöruhúsaaðgerðir.  

Sumir valreitir eru gerðir gráir og óvirkir með öðrum stillingum á síðunni **Birgðageymsluspjald** til að takmarka óstuddar uppsetningarsamsetningar.  

Veldu **Svæði** eða **Hólf** aðgerðin til að skoða upplýsingar um svæði og hólf sem gætu verið skilgreint fyrir birgðageymsluna.

### <a name="to-create-a-location-card"></a>Staðsetningarspjald búið til

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.

> [!NOTE]  
> Margir reitir á birgðageymsluspjaldinu vísa til meðhöndlunar vara í vöruhúsaferli á inn- og útleið. Reitirnir skipta ekki máli fyrir fyrirtæki sem þurfa ekki flóknari vöruhúsavirkni. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Hægt er að breyta uppsetningu staðsetninga síðar en ekki er hægt að breyta uppsetningu staðsetninga sem hafa birgðafærslur.  

Því næst er hægt að skilgreina flutningsleiðir milli staða ef margir staðir eru til staðar.  

### <a name="to-create-a-transfer-route"></a>Flutningsleið búin til

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flutningsleiðir** og veldu síðan tengda tengilinn.
2. Að öðrum kosti, frá hvaða síðu **Staðsetningarspjalds** sem er má velja aðgerðina **Flutningsleiðir**.
3. Valið er **Nýtt** aðgerð.
4. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nú er hægt að flytja birgðavörur milli tveggja staða. Nánari upplýsingar eru í [Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Hólf

Hólf tákna grunnvöruhúsauppbyggingu og eru notuð til að gera tillögur að staðsetningu vöru. Þegar hólfin hafa verið stofnuð er hægt að skilgreina nánar hvaða innihald á að setja í hvert hólf eða nota hólfið sem fljótandi hólf án tiltekins innihalds. Hólf eru aðallega notuð við grunn- og ítarlegar vöruhúsaðgerðir. Ef þú hefur umsjón með birgðum í einfaldari uppsetningu er líklega ekki þörf á hólfum.

Ef nota á hólf í birgðageymslu þarf fyrst að virkja aðgerðina á spjaldinu **Staðsetningin** með því að velja **Hólf áskilin** reitinn á flipanum **Vöruhús**. Síðan er vöruflæðið í birgðageymslunni útbúið með því að tilgreina hólfakóða í uppsetningarreitum sem tákna ólík flæði.

> [!NOTE]
> Áður en hægt er að tilgreina hólfkóta í birgðageymsluspjaldinu þarf að stofna hólfkótana.

Nánari upplýsingar er að finna í [Setja upp hólf](warehouse-how-to-create-individual-bins.md) og [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Svæði

Ef stofna á hólfin á svæðum má gera það á síðunni **Svæði**.

[!INCLUDE [prod_short](includes/prod_short.md)] afritar reitina sem stilltir eru fyrir eitthvað tiltekið svæði í hólfin innan þess. Þannig er hægt að úthluta svæði á hólf eða hólfasniðmát (afmörkun hólfa) og nokkrir aðrir reitir fyllast síðan út sjálfkrafa.

Hins vegar er hægt að velja að setja bara upp eitt svæði og skipuleggja vöruhúsið aðeins eftir hólfum. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Sjá einnig

[Stjórna birgðum](inventory-manage-inventory.md)  
[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  
[Stofna hólf](warehouse-how-to-create-individual-bins.md)  
[Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]