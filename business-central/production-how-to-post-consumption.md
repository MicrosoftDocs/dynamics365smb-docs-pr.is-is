---
title: Fjöldabóka notkun
description: Ef flæðiaðferðin er stillt á Handvirk þarf að bóka íhlutina handvirkt með notkunarbók.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000846, 99000850'
ms.date: 03/08/2023
ms.author: bholtorf
---
# Fjöldabóka framleiðslunotkun

Ef birgðaskráningaraðferðin er  **Handvirk** skal nota notkunarbók til að bóka íhlutina handvirkt.  

> [!NOTE]
> Ef sett hefur verið gátmerki í reitinn **Krefjast tínslu** á birgðageymsluspjaldinu til að sýna að birgðageymslan krefjist tínsluvinnslu þarf ekki að nota þessa runuvinnslu. [!INCLUDE[prod_short](includes/prod_short.md)] mun sjá um notkun þegar birgðatínslan er bókuð. Sjá  [tínslu fyrir framleiðslu í Grunnvöruvöruhúsi til að fá frekari upplýsingar](warehouse-how-to-pick-for-production.md).  

Einnig er hægt að setja [!INCLUDE[prod_short](includes/prod_short.md)] upp þannig að það bóki sjálfvirkt (*flæða*) íhluti þegar byrjar eða endar framleiðslupantanir. Nánari upplýsingar eru í [Leyfa flæði íhluta samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md).

## Bóka notkun fyrir eina eða fleiri framleiðslupantanalínur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notkunarbók** og velja síðan viðkomandi tengil.  
2. Reitirnir eru fylltir út með framleiðslupöntunargögnunum og notkunargögnunum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Notið aðgerðina **Reikna notkun** til að mynda færslubókarlínur úr framleiðslupöntunum sem byggja á raunverulegu frálagi (magni tilbúinnar vöru sem tilkynnt hefur verið um) eða væntanlegu frálagi (magni tilbúinnar vöru sem stefnt er að því að framleiða).

    > [!NOTE]
    > Ef birgðageymsluspjaldið var skilgreint til að krefjast tínsluvinnu vöruhúss, þá má aðeins slá inn magn sem þegar er búið að tína í gegnum vöruhúsaaðgerð í reitinn **Magn** á síðunni **Notkunarbók**, ekki neitt reiknað magn. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Velja **Bóka** aðgerðina til að bóka notkunina. Tengdar birgðir eru minnkaðar.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Sjá einnig

[Framleiðsla](production-manage-manufacturing.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
