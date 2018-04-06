---
title: "Hvernig á að ganga frá framleiðslufrálagi | Microsoft Docs"
description: "Hvernig gengið er frá frálagi úr framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a7918a962f3349c68cd7245e9b12f83975aee5ac
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="put-away-production-or-assembly-output"></a>Ganga frá framleiðslu eða samsetningarfrálagi
Hvernig gengið er frá frálagi úr framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslan er sett upp þannig að krafist sé frágangsvinnslu en ekki móttökuvinnslu er skjalið **Birgðafrágangur** notað til að skipuleggja og skrá frágang á frálagi.  

Í ítarlegri vöruhúsagrunnstillingu þarf birgðageymslan bæði frágangsvinnslu og móttökuvinnslu er hægt að stofna annaðhvort innanhúss frágangsskjal eða hreyfingarskjal til að ganga frá frálaginu.  

Fyrsti áfanginn í stofnun birgðafrágangs er að stofna innleiðarbeiðni í vöruhúsi. Þessi beiðni lætur vöruhúsið vita að frálag framleiðslu eða samsetningarpöntunar sé tilbúið til frágangs.

## <a name="to-create-the-inbound-warehouse-request"></a>Stofna innleiðarbeiðni í vöruhúsi:  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **útgefin framleiðslupöntun** og velja svo viðeigandi tengil.  
2.  Í framleiðslupöntuninni sem er tilbúin til frágangs, skal velja aðgerðina **Stofna vöruh.beiðni á innleið**.  

> [!NOTE]  
>  Einnig er hægt að stofna á vöruhúsabeiðni á innleið með því að gátreitinn **Stofna beiðni á innleið** þegar framleiðslupöntun er endurnýjuð. Frekari upplýsingar, sjá [Uppfæra eða enduráætla framleiðslupantanir](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Gengið frá frálagi með Birgðafrágangi  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðafrágangur** og velja svo viðeigandi tengil.  
2.  Nýr birgðafrágangur er stofnaður. Nánari upplýsingar eru í [Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
4.  Frágangslínurnar eru fylltar út.
5.  Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókunin stofnar nauðsynlegar vöruhúsafærslur og bókar frálag varanna.  

Einnig er hægt að stofna **Birgðafrágang** beint úr útgefnu framleiðslupöntuninni. Nánari upplýsingar eru í [Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Þegar birgðafrágangur er bókaður er gert ráð fyrir að allar aðgerðir séu bókaðar í samræmi við staðlaðar leiðir, það er, frálagsmagn er bókað í samræmi við síðustu aðgerð. Hægt er að nota frálagsbók til þess að bóka frávik í frálagsmagni og uppsetningar- og keyrslutíma. Ef nauðsynlegt er að gera hlutabókun þegar búið er að stofna birgðafrágang er hægt að gera það fyrir uppsetningartíma og magn fyrir allar aðgerðir, nema þá síðustu. Í því tilviki er síðustu aðgerð stýrt af birgðafrágangi.  

Ef aðeins þarf að bóka uppsetningar- eða keyrslutíma við síðustu aðgerð skal stilla frálagsmagn síðustu aðgerðar á 0. Einnig er hægt að velja að bóka ekki síðustu línuna með því einfaldlega að eyða henni.  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Gengið frá frálagi með innanhússfrágangi vöruhúss
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innanhússfrágangur vöruhúss** og velja svo viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð.
3. Í haus nýja innanhússfrágangsins þarf að tilgreina að minnsta kosti **kóta birgðageymslu**.  
4. Fylla skal út eina línu fyrir hverja vöru sem flytja á í vöruhúsið. Aðeins þarf að fylla út í reitina **Vörunr.** og **Magn**.  

    > [!NOTE]  
    >  Þegar valinn er **Vörunr.** reitinn, birtist **Innihaldslisti hólfs** í staðinn fyrir **vörulistann**. Það er vegna þess að það á að ganga frá vöru sem er í tilteknu hólfi – Innihaldi hólfs – ekki bara vöru, og þegar er vitað úr hvaða hólfi á að taka vöruna.  

4.  Til að fylla vinnublaðslínurnar með öllu innihaldi hólfsins eða afmörkuðu innihald hólfa í birgðageymslunni, skal velja aðgerðina **Sækja hólfainnihald**.  
5.  Velja aðgerðina **Stofna frágang** og þá fara vörurnar sem taka á úr framleiðslunni í frágangsleiðbeiningar og bíða þess að vera geymdar í vöruhúsinu.  

> [!NOTE]  
>  Þegar vöruhúsið er sett upp þannig að það noti beinan frágang og tínslu er vöruhúsið tengt framleiðslunni með sjálfgefnum framleiðsluhólfunum: Inn- og úthólf framleiðslu og opið búðarhólf sem öll eru skilgreind á flýtiflipanum **Hólf** á birgðageymsluspjaldinu. Þegar frálag framleiðslupöntunar er bókað er frálagið sjálfkrafa sett í **hólf framleiðslu á útleið**. Sama aðferð og lýst var að framan er notuð til að ganga frá framleiðslufrálaginu nema að í stað þess að nota sjálfgefið hólf vörunnar eru vörurnar færðar eða gengið frá þeim úr **hólfi framleiðslu á útleið** yfir í sjálfgefið hólf vörunnar.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Til að tilgreina handvirkt hólf til að geyma vörur úr framleiðslufrálagi  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hreyfingarvinnublað** og velja svo viðeigandi tengil.  
2.  Hausinn er fylltur út og lína stofnuð fyrir hverja vöru sem flytja á í vöruhúsið.  
3.  Reitirnir **Kóti frá-hólfs** og **Kóti til-hólfs** eru fylltir út og magnið fært inn í reitinn **Magn**.  
4.  Til að fylla vinnublaðslínurnar með öllu innihaldi hólfsins eða afmörkuðu innihald hólfa í birgðageymslunni, skal velja aðgerðina **Sækja hólfainnihald**.  
5. Veldu aðgerðina **Stofna hreyfingu**. Vöruhúsahreyfingaleiðbeiningar með Taka- og Setja-línum eru stofnaðar fyrir starfsmenn vöruhúss.  

> [!NOTE]  
>  Ekki er hægt að færa inn upprunaskjalsnúmerið, s.s. Framleiðslupöntun nr., í skjölin innanhússfrágangur, frágangur eða hreyfing í þessum ferlum.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

