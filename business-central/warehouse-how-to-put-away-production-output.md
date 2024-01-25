---
title: Ganga frá frálagi framleiðslu
description: Í greininni er fjallað um frágang framleiðsluúttaks.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# Ganga frá framleiðslu eða samsetningarfrálagi

Hvernig gengið er frá frálagi úr framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

Í grunnvöruhúsaleiðunum þar sem krafist er frágangsvinnslu þarf að nota  **birgðafrágangsskjalið**  til að bóka framleiðslu framleiðsla og færslufrágang fyrir hana.  

> [!NOTE]  
> Samsetningarferli styðja ekki birgðafrágang. Samsetningarpöntun er bókuð til að skrá úttak. Ef hólf eru notuð er hægt að færa vörur milli hólfa síðar. Frekari upplýsingar um  [flutning vöru tilfallandi í Grunnvöruhúsaleiðunum](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Í ítarlegum vöruhúsafbrigðum þar sem Birgðageymsla krefst bæði frágangs-og móttökuvinnslu þarf að stofna annað hvort innanhússfrágangsskjal eða hreyfingarskjal til að ganga frá frálagi.  

## Að ganga frá framleiðsluúttaki með birgðafrágangi

Fyrsta skrefið til að ganga frá frálagi er að stofna vöruhúsabeiðni á innleið. Þessi beiðni lætur vöruhúsið vita að frálag framleiðslu eða samsetningarpöntunar sé tilbúið til frágangs.

### Stofna innleiðarbeiðni í vöruhúsi:  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losuð framleiðslupöntun** og velja síðan viðkomandi tengil.  
2. Framleiðslupöntunin er valin sem er tilbúin til frágangs og síðan er valið stofna vöruhúsaafhendingar á  **innleið. Biðja um**  aðgerð.  

> [!NOTE]  
> Einnig er hægt að stofna vöruhúsabeiðni á innleið með því að velja reitinn **Stofna beiðni á innleið** þegar framleiðslupöntun er endurnýjuð. Frekari upplýsingar um  [endurnýjun eða enduráætlun framleiðslupantana](production-how-to-replan-refresh-production-orders.md).  

### Gengið frá frálagi með Birgðafrágangi  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðafrágangur** og velja síðan viðkomandi tengil.  
2. Nýr birgðafrágangur er stofnaður. Frekari upplýsingar um það að setja vörur í  [gang með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
4. Fyllt er í Frágangslínurnar eftir þörfum.
5. Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókun stofnar vöruhúsafærslur og bókar afköst varanna.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Einnig er hægt að stofna **Birgðafrágang** beint úr útgefnu framleiðslupöntuninni. Frekari upplýsingar um það að setja vörur í  [gang með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Þegar Birgðafrágangur er bókaður er gert ráð fyrir að allar aðgerðir séu bókaðar í samræmi við staðlaða leið. Það er, afkastamagnið er bókað samkvæmt síðustu aðgerðinni. Hægt er að nota frálagsbókinn til að bóka frávik í afkastamagni og uppsetningu og keyrslutíma. Ef bóka þarf að hluta til eftir að Birgðafrágangur var stofnaður er hægt að gera það með því að setja upp tíma og magn fyrir allar aðgerðir nema í síðasta lagi. Síðustu aðgerðinni er stjórnað af birgðafrágangnum.  

Ef aðeins þarf að bóka uppsetningu eða keyrslutíma síðustu aðgerðar skal stilla afkastamagn síðustu aðgerðar í 0. Þú getur valið að bóka ekki síðustu línuna yfirleitt með því einfaldlega að eyða henni.

## Að ganga frá samsetningu og framleiðsluúttaki í ítarlegum vöruhúsagrunnstillingum

Þegar framleiðsla eða samsetningarpöntun er bókuð í vöruhúsi sem notar beinan frágang og tínslu er frálag sett í hólfið sem skilgreint er í framleiðslu eða samsetningarröðinni. Frekari upplýsingar um mismunandi leiðir til að færa vörur í vöruhúsið með ítarlegum afbrigðum er farið í til að  [flytja vörur í ítarlegar vöruhúsaskilgreiningar](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Ekki er hægt að færa inn númer upprunaskjals, eins og númer framleiðslupöntunarinnar, í innanhússfráganginn, frágang, eða hreyfingarskjöl fyrir samsetningar eða framleiðslufrálagsferli.  

## Sjá einnig  

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
