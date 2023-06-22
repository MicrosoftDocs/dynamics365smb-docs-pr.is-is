---
title: Setja upp beinan frágang og tínslu
description: Beinn frágangur og tínsla gefur aðgerðir til að keyra vöruhúsið á skilvirkan hátt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 11/07/2022
ms.author: bholtorf
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick" />Setja upp vörur og birgðageymslur fyrir beinan frágang og tínslu

Þegar vöruhús er sett upp fyrir beinan frágang og tínslu fást aðgerðir sem gera rekstur vöruhússins mun skilvirkari. Svo að þessar aðgerðir nýtist til fulls þarf að veita viðbótarupplýsingar um vörurnar sem hjálpa til við að reikna út skilvirkustu og bestu aðferðirnar til að stýra vöruhúsaaðgerðum. 

## <a name="to-set-up-an-item-for-directed-put-away-and-pick" />Varan sett upp fyrir beinan frágang og tínslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Opnaðu kort fyrir vöruna sem á að setja upp fyrir beinan frágang og tínslu er valin.
3. Á flýtiflipanum **Vöruhús** á birgðaspjaldinu eru reitirnir fylltir út til að tilgreina hvernig fara skuli með vöruna í vöruhúsinu.  
4. Veldu **Mælieining**.
5.  **Á síðunni mælieiningar**  vöru er hægt að skilgreina mælieiningar sem hægt er að umþjappa vörunni með því að tilgreina hæð, breidd, lengd, rúmmál og þyngd.
6. Veldu **Innihald hólfs** aðgerðina.
7. Á síðunni **Innihald hólfs** er hægt að skilgreina birgðageymsluna og hólfið sem tengja á vörunni. Reiturinn **Sjálfgefið** er ekki notaður þegar vöruhúsið er sett upp fyrir beinan frágang og tínslu.  

## <a name="to-start-using-directed-put-away-and-pick" />Byrjað að nota beinan frágang og tínslu

Beinn frágangur og tínsla gefa kost á þróaðri vöruhúsaaðgerðum sem auka mjög skilvirkni og áreiðanleika gagna. Fyrst þarf að setja upp nokkrar færibreytur í vöruhúsinu.  

Ef nota á beinan frágang og tínslu þarf að virkja aðgerðina á birgðageymsluspjaldinu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2. Veljið staðsetninguna þar sem nota á stýrðan frágang og tínslu og veldu svo aðgerðina **Breyta**.  
3.  **Á flipanum Vöruhús**  er valinn  **gátreiturinn beinn frágangur og tínsla** .  

Ekki þarf að fylla út aðra reiti á birgðageymsluspjaldinu fyrr en seinna í uppsetningarferlinu.  

> [!NOTE]  
> Ekki er hægt að setja vöruhúsið upp til að nota hólf þegar opnar birgðafærslur eru í birgðageymslunni.  

Síðan þarf að skilgreina tegundir hólfa. Frekari upplýsingar eru í [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md). Tegund hólfsins tilgreinir hvernig ákveðið hólf er notað í úrvinnslu vöruflæðis um vöruhúsið. Hægt er að úthluta hólfategund bæði á svæði og hólf.  

Einnig er hægt að skilgreina kóta vöruhúsaflokkana ef vöruhúsið flytur vörur sem þurfa Sérstök GEYMSLUSKILYRÐI. Vöruhúsaflokkskóðar eru notaðir þegar ráðleggingar eru gefnar um staðsetningu vara í hólf. Vöruhúsaflokkskóðum er úthlutað á vöruflokka, sem er svo úthlutað á vörur og birgðahaldseiningar, eða á svæði og hólf sem geta mætt geymsluþörfum vöruhúsaflokkskóðanna.  

Þú ert tilbúinn að setja upp svæði, ef þú vilt. Notkun svæða fækkar reitum sem fylla þarf út þegar hólf eru sett upp þar sem hólf sem stofnuð eru innan svæða erfa nokkra af eiginleikum svæðisins. Svæði auðvelda einnig nýjum starfsmönnum og afleysingafólki að ná áttum í vöruhúsinu. Athugið að flæði er stjórnað af hólfum, því er hægt er að nota hólf og hafa aðeins eitt svæði.  

## <a name="to-set-up-a-zone-in-your-warehouse" />Svæði sett upp í vöruhúsinu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2. Staðsetningin þar sem á að setja upp svæði er valin og birgðageymsluspjald opnað og svo **Staðir** valin.  
3. Á síðunni **Svæði** skal fyllt í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar færibreytu svæðis er breytt munu öll hólf sem stofnuð eru eftir það fá nýju eiginleikana en eldri hólf haldast óbreytt.  

> [!NOTE]  
> Ef vinna á án svæða þarf engu að síður að búa til einn svæðiskóta, sem hefur enga skilgreiningu utan kótans.  

Næsta skref er að skilgreina hólf. Frekari upplýsingar á  [Setja upp staðsetningar til að nota hólf](warehouse-how-to-set-up-locations-to-use-bins.md).  

Auk þess þarf að stofna frágangssniðmát og talningartímabil. Frekari upplýsingar er að  [Setja upp frágang sniðmáta](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also" />Sjá einnig

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
