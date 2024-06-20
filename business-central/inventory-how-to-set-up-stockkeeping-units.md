---
title: Hvernig setja á upp birgðaeiningar
description: Nota birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekið afbrigði.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
ms.service: dynamics-365-business-central
---

# Setja upp birgðahaldseiningar

Nota birgðahaldseiningar (birgðahaldseiningar) til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða afbrigði. Með þeim er hægt að bæta við mismunandi upplýsingum um vöru fyrir tiltekna birgðageymslu, til dæmis:

* Vöruhús eða dreifingarmiðstöð
* Afbrigði, svo sem mismunandi hillunúmer og mismunandi áfyllingarupplýsingar, fyrir sömu vöruna  

## Uppsetning birgðahaldseiningar  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Birgðahaldseiningar** og velja síðan viðeigandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. Eftirfarandi reita er krafist: **Vörunr.**, **Kóti birgðageymslu**, og/ eða **Afbrigðiskóti**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar fyrsta birgðahaldseiningin hefur verið sett upp fyrir vöru er gátreiturinn **Birgðahaldseining** er til á **birgðaspjaldinu** valinn.  

Ef stofna á nokkrar birgðahaldseiningar fyrir vöru er keyrslan Stofna birgðahaldseiningu **notuð** . Nánari upplýsingar um keyrslur eru notaðar í [Verkröð til að tímasetja verkhluta](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> Upplýsingarnar á spjaldinu **Birgðaeining er til** hafa forgang á spjaldið **Vara**.

> [!Warning]
> Ef birgðahaldseiningin fæst með framleiðslu **er reiturinn Staðlað kostnaðarverð** ekki notaður við reikningsfærslu og leiðréttingu raunkostnaðar framleiddu vörunnar. Þess í stað er [!INCLUDE [prod_short](includes/prod_short.md)]  gildið í reitnum **Staðlað kostnaðarverð** á birgðaspjaldinu notað og frávik reiknuð saman við kostnaðarhlutdeild þeirrar vöru.<br><br>
> Þótt hægt sé að úthluta framleiðsluuppskriftum og leiðum á birgðahaldseiningar eru samantekt kostnaðarverðs og tengdir útreikningar á kostnaðarhlutdeild ekki tiltækir í birgðahaldseiningum. Nánari upplýsingar um staðlað kostnaðarverð er farið í [Um útreikning á stöðluðu kostnaðarverði](finance-about-calculating-standard-cost.md)

## Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Samsetningardeild](assembly-assemble-items.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
