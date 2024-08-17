---
title: Gengið frá framleiðslufrálagi
description: Þessi grein lýsir því hvernig gengið er frá framleiðslufrálagi notanda.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# Ganga frá framleiðslu eða samsetningarfrálagi

Hvernig gengið er frá frálagi úr framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

Í einfaldri vöruhússkilgreiningu fyrir flæði inn (frágang) á **síðunni Birgðageymsluspjald** fyrir birgðageymsluna eru eftirfarandi stillingar virkjaðar:

* Í glugganum **Framl.frálagsgrunnur vöruh. Meðhöndlunarreitur** er birgðafrágangur **valinn**.
* Samsetningarvinnslur styðja ekki birgðafrágang. Samsetningarpöntun er bókuð til að skrá úttak. Ef hólf eru notuð er hægt að færa vörur milli hólfa síðar. Nánari upplýsingar um flutning á [vörum tilfallandi í grunnstillingum vöruhúss](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  
* Frágangur á ekki við fyrir verkefni.

Í ítarlegum vöruhúsaskilgreiningum þar sem birgðageymsla krefst frágangs skal stofna innanhússfrágangsskjal eða hreyfingarskjal til að ganga frá frálaginu.  

## Að ganga frá framleiðsluúttaki með birgðafrágangi

Fyrsta skrefið sem gengið er frá frálagi er að stofna vöruhúsabeiðni á innleið. Þessi beiðni lætur vöruhúsið vita að frálag framleiðslu eða samsetningarpöntunar sé tilbúið til frágangs.

### Stofna innleiðarbeiðni í vöruhúsi:  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  
2. Framleiðslupöntunin sem er tilbúin til frágangs er valin og síðan er reiturinn **Stofna vöruh. á innleið valið. Beiðniaðgerð** .  

> [!NOTE]  
> Einnig er hægt að stofna vöruhúsabeiðni á innleið með því að velja reitinn **Stofna beiðni á innleið** þegar framleiðslupöntun er endurnýjuð. Nánari upplýsingar um [Endurnýjun eða enduráætla framleiðslupantanir](production-how-to-replan-refresh-production-orders.md).  

### Gengið frá frálagi með birgðafrágangi  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðafrágangur** og velja síðan viðkomandi tengil.  
2. Nýr birgðafrágangur er stofnaður. Nánari upplýsingar um frágang á [vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
4. Frágangslínurnar eru fylltar út eftir þörfum.
5. Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókun stofnar vöruhúsafærslur og bókar frálag varanna.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Einnig er hægt að stofna **Birgðafrágang** beint úr útgefnu framleiðslupöntuninni. Nánari upplýsingar um frágang á [vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Þegar birgðafrágangur [!INCLUDE [prod_short](includes/prod_short.md)]  er bókaður er gert ráð fyrir að allar aðgerðir séu bókaðar samkvæmt stöðluðu leiðinni. Það er, frálagsmagnið er bókað samkvæmt síðustu aðgerð. Hægt er að nota frálagsbókina til að bóka frávik í frálagsmagni og uppsetningar- og keyrslutíma. Ef bóka þarf að hluta eftir að birgðafrágangurinn hefur verið stofnaður er hægt að gera það á uppsetningartíma og magni fyrir allar aðgerðir nema þá síðustu. Birgðafrágangurinn stýrir síðustu aðgerð.  

Ef aðeins þarf að bóka uppsetninguna eða keyrslutímann á síðustu aðgerð er afkastað magnið stillt á 0. Hægt er að velja að bóka ekki síðustu línuna með því að eyða henni.

## Gengið frá samsetningar- og framleiðslufrálagi í ítarlegum vöruhúsafbrigðum

Þegar frálag framleiðslu eða samsetningarpöntunar er bókað í vöruhúsi sem notar beinan frágang og tínslu fer frálagið í hólfið sem skilgreint er í framleiðslu- eða samsetningarpöntuninni. Til að fræðast meira um mismunandi leiðir til að færa vörur í vöruhúsinu með ítarlegri grunnstillingu er farið [í Færa vörur í ítarlegri vöruhúsaskilgreiningu](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Ekki er hægt að færa inn upprunaskjalsnúmerið, t.d. númer framleiðslupöntunarinnar, í innanhússfrágangs-, frágangs- eða hreyfingaskjöl fyrir samsetningar- eða framleiðslufrálagsvinnslur.  

## Sjá einnig  

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
