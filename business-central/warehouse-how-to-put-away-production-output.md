---
title: Ganga frá frálagi framleiðslu
description: Hvernig gengið er frá frálagi úr framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Birgðafrágang er hægt að framkvæma á eftirfarandi vegu.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: e93c4d5abd6b6c3136e95838d10895a8fb1b2b90
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134547"
---
# <a name="put-away-production-or-assembly-output"></a>Ganga frá framleiðslu eða samsetningarfrálagi

Hvernig gengið er frá frálagi úr framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslan er sett upp þannig að krafist sé frágangsvinnslu er skjalið **Birgðafrágangur** notað til að bóka framleiðsluúttak og skrá frágang úttaks.  

> [!NOTE]  
> Frágangur birgða er ekki studdur fyrir samsetningarferli. Samsetningarpöntun er bókuð til að skrá úttak. Ef hólf eru notuð er hægt að færa vörur milli hólfa síðar meir. Frekari upplýsingar eru í [Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Í ítarlegri vöruhúsagrunnstillingu þarf birgðageymslan bæði frágangsvinnslu og móttökuvinnslu er hægt að stofna annaðhvort innanhúss frágangsskjal eða hreyfingarskjal til að ganga frá frálaginu.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Að ganga frá framleiðsluúttaki með birgðafrágangi

Fyrsti áfanginn í stofnun birgðafrágangs er að stofna innleiðarbeiðni í vöruhúsi. Þessi beiðni lætur vöruhúsið vita að frálag framleiðslu eða samsetningarpöntunar sé tilbúið til frágangs.

### <a name="to-create-the-inbound-warehouse-request"></a>Stofna innleiðarbeiðni í vöruhúsi:  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  
2.  Í framleiðslupöntuninni sem er tilbúin til frágangs, skal velja aðgerðina **Stofna vöruh.beiðni á innleið**.  

> [!NOTE]  
> Einnig er hægt að stofna vöruhúsabeiðni á innleið með því að velja reitinn **Stofna beiðni á innleið** þegar framleiðslupöntun er endurnýjuð. Frekari upplýsingar, sjá [Uppfæra eða enduráætla framleiðslupantanir](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Gengið frá frálagi með Birgðafrágangi  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðafrágangur** og velja síðan viðkomandi tengil.  
2.  Nýr birgðafrágangur er stofnaður. Nánari upplýsingar eru í [Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
4.  Frágangslínurnar eru fylltar út.
5.  Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókunin stofnar nauðsynlegar vöruhúsafærslur og bókar frálag varanna.  

Einnig er hægt að stofna **Birgðafrágang** beint úr útgefnu framleiðslupöntuninni. Nánari upplýsingar eru í [Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Þegar birgðafrágangur er bókaður er gert ráð fyrir að allar aðgerðir séu bókaðar í samræmi við staðlaðar leiðir, það er, frálagsmagn er bókað í samræmi við síðustu aðgerð. Hægt er að nota frálagsbók til þess að bóka frávik í frálagsmagni og uppsetningar- og keyrslutíma. Ef nauðsynlegt er að gera hlutabókun þegar búið er að stofna birgðafrágang er hægt að gera það fyrir uppsetningartíma og magn fyrir allar aðgerðir, nema þá síðustu. Í því tilviki er síðustu aðgerð stýrt af birgðafrágangi.  

Ef aðeins þarf að bóka uppsetningar- eða keyrslutíma við síðustu aðgerð skal stilla frálagsmagn síðustu aðgerðar á 0. Einnig er hægt að velja að bóka ekki síðustu línuna með því einfaldlega að eyða henni.  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Að ganga frá samsetningu og framleiðsluúttaki í ítarlegum vöruhúsagrunnstillingum
Þegar framleiðsla eða samsetningarpöntun er bókuð í vöruhúsi sem er sett upp til að nota stýrðan frágang og tínslu er framleiðslan sett í hólfið sem skilgreint er í framleiðslu- eða samsetningarpöntuninni. 

Eftirfarandi tafla sýnir mismunandi leiðir til að færa vörur innan vöruhúss með ítarlegum grunnstillingum þar sem framkvæma þarf allar vöruhúsaaðgerðir í stýrðu verkflæði. 

|**Til að**|**Sjá**|  
|------------|-------------|  
|Færa vörur með vöruhúsahreyfingarvinnublaðinu.|[Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Stofnaðu frágang innanhúss til að ganga frá framleiddum eða samsettum vörum í ítarlegum vöruhúsaaðgerðum.|[Stofna innanhússfrágang](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Ekki er hægt að færa inn upprunaskjalsnúmerið, s.s. Framleiðslupöntun nr., í skjölin innanhússfrágangur, frágangur eða hreyfing í þessum ferlum.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
