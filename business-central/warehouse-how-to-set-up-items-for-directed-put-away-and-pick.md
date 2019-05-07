---
title: Setja upp beinan frágang og tínslu | Microsoft Docs
description: Þegar vöruhús er sett upp fyrir beinan frágang og tínslu fást aðgerðir sem gera rekstur vöruhússins mun skilvirkari.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2492ebf0d9987bd126fa963c6d7d940c6a114796
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "914811"
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Setja upp vörur og birgðageymslur fyrir beinan frágang og tínslu
Þegar vöruhús er sett upp fyrir beinan frágang og tínslu fást aðgerðir sem gera rekstur vöruhússins mun skilvirkari. Svo að þessar aðgerðir nýtist til fulls þarf að veita viðbótarupplýsingar um vörurnar sem hjálpa til við að reikna út skilvirkustu og bestu aðferðirnar til að stýra vöruhúsaaðgerðum. Nánari upplýsingar eru í [Upplýsingar um hönnun: Uppsetning vöruhúss](design-details-warehouse-setup.md).

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Varan sett upp fyrir beinan frágang og tínslu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.  
2.  Opnaðu kort fyrir vöruna sem á að setja upp fyrir beinan frágang og tínslu er valin.
3. Á flýtiflipanum **Vöruhús** á birgðaspjaldinu eru reitirnir fylltir út til að tilgreina hvernig fara skuli með vöruna í vöruhúsinu.  
4.  Veldu **Mælieining**.
5. Á síðunni **Mælieiningar vöru** skal fylla út reitina til að skilgreina mismunandi mælieiningar sem hægt er að hafa vöruna í, þar á meðal hæð, breidd, lengd, rúmmál og þyngd fyrir mælieininguna.
6. Veldu **Innihald hólfs** aðgerðina.
7. Á síðunni **Innihald hólfs** er hægt að skilgreina birgðageymsluna og hólfið sem tengja á vörunni. Reiturinn **Sjálfgefið** er ekki notaður þegar vöruhúsið er sett upp fyrir beinan frágang og tínslu.  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a>Til að virkja aðgerðir fyrir stýrðan frágang og tínslu.  
Beinn frágangur og tínsla gefa kost á þróaðri vöruhúsaaðgerðum sem auka mjög skilvirkni og áreiðanleika gagna. Fyrst þarf að setja upp nokkrar færibreytur í vöruhúsinu.  

Ef nota á beinan frágang og tínslu þarf að virkja aðgerðina á birgðageymsluspjaldinu.    
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.  
2.  Veljið staðsetninguna þar sem nota á stýrðan frágang og tínslu og veldu svo aðgerðina **Breyta**.  
3.  Á flýtiflipanum **Vöruhús** skal velja gátreitinn **Beinn frágangur og tínsla**.  

Ekki þarf að fylla út aðra reiti á birgðageymsluspjaldinu fyrr en seinna í uppsetningarferlinu.  

> [!NOTE]  
>  Ekki er hægt að setja vöruhús upp með hólfum ef það er með opnar birgðafærslur.  

Síðan þarf að skilgreina tegundir hólfa. Frekari upplýsingar eru í [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md). Tegund hólfsins tilgreinir hvernig ákveðið hólf er notað í úrvinnslu vöruflæðis um vöruhúsið. Hægt er að úthluta hólfategund bæði á svæði og hólf.  

Einnig er hægt að skilgreina kóta vöruhúsaflokka ef vörur í vöruhúsinu krefjast mismunandi geymsluskilyrða. Vöruhúsaflokkskóðar eru notaðir þegar ráðleggingar eru gefnar um staðsetningu vara í hólf. Vöruhúsaflokkskóðum er úthlutað á vöruflokka, sem er svo úthlutað á vörur og birgðahaldseiningar, eða á svæði og hólf sem geta mætt geymsluþörfum vöruhúsaflokkskóðanna.  

Nú er allt til reiðu fyrir uppsetningu svæðanna eigi að nota svæði í vöruhúsinu. Notkun svæða fækkar reitum sem fylla þarf út þegar hólf eru sett upp þar sem hólf sem stofnuð eru innan svæða erfa nokkra af eiginleikum svæðisins. Svæði auðvelda einnig nýjum starfsmönnum og afleysingafólki að ná áttum í vöruhúsinu. Athugið að flæði er stjórnað af hólfum, því er hægt er að nota hólf og hafa aðeins eitt svæði.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>Svæði sett upp í vöruhúsinu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.  
2.  Staðsetningin þar sem á að setja upp svæði er valin og birgðageymsluspjald opnað og svo **Staðir** valin.  
3.  Á síðunni **Svæði** skal fyllt í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar færibreytu svæðis er breytt munu öll hólf sem stofnuð eru eftir það fá nýju eiginleikana en eldri hólf haldast óbreytt.  

> [!NOTE]  
>  Ef vinna á án svæða þarf engu að síður að búa til einn svæðiskóta, sem hefur enga skilgreiningu utan kótans.  

Næsta skref í uppsetningu vöruhúss er að skilgreina hólfin. Frekari upplýsingar eru í [Setja upp birgðageymslur til að þær noti hólf](warehouse-how-to-set-up-locations-to-use-bins.md).  

Auk þess þarf að stofna frágangssniðmát og talningartímabil. Frekari upplýsingar eru í [Setja upp frágangssniðmát](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
