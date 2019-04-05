---
title: Hvernig á að setja upp birgðageymslur til að nota hólf | Microsoft Docs
description: Hólf tákna grunnvöruhúsauppbyggingu og eru notuð til að gera tillögur að staðsetningu vöru. Þegar hólfin hafa verið stofnuð er hægt að skilgreina nánar hvaða innihald á að setja í hvert hólf eða nota hólfið sem fljótandi hólf án tiltekins innihalds.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 214de72b86e3d32e5161814a7f65079cbb4136b7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799958"
---
# <a name="set-up-locations-to-use-bins"></a>Setja upp birgðageymslur til að þær noti hólf
Hólf tákna grunnvöruhúsauppbyggingu og eru notuð til að gera tillögur að staðsetningu vöru. Þegar hólfin hafa verið stofnuð er hægt að skilgreina nánar hvaða innihald á að setja í hvert hólf eða nota hólfið sem fljótandi hólf án tiltekins innihalds.  

Ef nota á hólf í birgðageymslu þarf fyrst að virkja aðgerðina á spjaldinu **birgðageymsla** Síðan er vöruflæðið í birgðageymslunni útbúið með því að tilgreina hólfakóða í uppsetningarreitum sem tákna ólík flæði.  

> [!NOTE]  
>  Áður en hægt er að tilgreina hólfkóta í birgðageymsluspjaldinu þarf að stofna hólfkótana. Frekari upplýsingar eru í [Stofna hólf](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Til að setja upp birgðageymslur til að þær noti hólf  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.  
2.  Veljið birgðageymsluna þar sem á að nota hólf.  
3.  Veldu aðgerðina **Breyta**.  
4.  Á flýtiflipanum **Vöruhús** er gátreiturinn **Hólf áskilin** valinn.  
5.  Ef ekki er notaður beinn frágangur og tínsla er í reitnum **Sjálfgefið hólfaval** tilgreind aðferðin sem kerfið a´að nota þegar sjálfgefið hólf er tengt vöru.  
6.  Opna spjaldið fyrir birgðageymsluna sem setja á upp hólf fyrir.
7.  Á flýtiflipanum **Hólf** skal velja hólfin sem nota á sem sjálfgefin fyrir móttökur, afhendingar, á innleið, á útleið og opin vinnslusalarhólf.  
8.  Hólfakótarnir sem valdir eru hér munu birtast sjálfkrafa á hausum og línum vöruhúsaskjala. Sjálfgefnu hólfin skilgreina allar upphafs- og lokastaðsetningar vara í vöruhúsinu.  
9.  Ef notaður er beinn frágangur og tínsla skal velja hólf fyrir vöruhúsaleiðréttingar. Hólfakótinn í svæðinu **Kóti leiðréttingarhólfs** skilgreinir sýndarhólfið þar sem á að skrá misræmi í birgðum við skráningu annað hvort misræmis sem uppgötvast og skráð er í vöru í vöruhúsi færslubókar eða mismunar sem reiknaður er þegar raunbirgðir vöruhúss eru skráðar.  
10. Reitirnir á flýtiflipanum **Hólfareglur** eru fylltir út ef þeir eiga við í vöruhúsinu. Mikilvægustu reitirnir eru **Hólfageturegla**, **Leyfa einingaskipti** og **Kóti frágangssniðmáts**.  
11. Á flýtiflipanum **Vöruhús** skal fylla út reitina **Afgr.tími vara á útl. úr vöruh.**, **Afgr.tími vara á innl. úr vöruh.** og **Kóti grunndagatals**. Frekari upplýsingar eru í [Setja upp grunndagatal](across-how-to-assign-base-calendars.md).

## <a name="filling-the-consumption-bin"></a>Fylla út notkunarhólfið
Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningu staðsetningar.

![Flæðirit hólfa](media/binflow.png "Hólfaflæði")  

## <a name="see-also"></a>Sjá einnig
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
