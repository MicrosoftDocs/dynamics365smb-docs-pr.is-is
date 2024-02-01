---
title: Hvernig á að setja upp birgðaeiningar
description: Notið birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekið afbrigði.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/19/2023
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
ms.service: dynamics-365-business-central
---

# Setja upp birgðahaldseiningar

Nota á birgðahaldseiningar (SKUs) til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða afbrigði. Þeir leyfa að bæta við mismunandi upplýsingum um vöru á tilteknum stað, til dæmis:

* Vöruhús eða dreifingarmiðstöð
* Vöruvíddasamsetningar eins og mismunandi Hillunúmer og mismunandi áfyllingarupplýsingar fyrir sömu vöru  

## Uppsetning birgðaeininga  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðahaldseiningar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. Eftirfarandi reita er krafist: **Vörunr.**, **Kóti birgðageymslu**, og/ eða **Afbrigðiskóti**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar fyrsta birgðaeiningin fyrir vöru  **hefur verið sett upp er gátreiturinn í birgðaeiningunni til staðar**  á  **birgðaspjaldinu**  valinn.  

Ef búa á til nokkrar birgðaeiningar fyrir vöru er keyrslan **Stofna birgðahaldseiningu** notuð. Til að fræðast meira um runuvinnslur er farið að  [nota Starfbiðraðir til að áætla verk](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> Upplýsingarnar á spjaldinu **Birgðaeining er til** hafa forgang á spjaldið **Vara**.

> [!Warning]
> Ef BIRGÐAHALDSEINING er í gegnum framleiðslu,  **er reiturinn staðlaður kostnaður**  ekki notaður við reikningsfærslu og leiðréttingu á raunverulegum kostnaði framleiddra vörunnar.  [!INCLUDE [prod_short](includes/prod_short.md)] Í staðinn notar gildið í  **reitnum Staðlað kostnaðarverð**  á birgðaspjaldinu og frávik eru reiknuð miðað við kostnaðarhlutdeild þeirrar vöru.<br><br>
> Þó að hægt sé að úthluta framleiðsluuppskriftum og-leiðum á SKUs eru kostnaðarinnrúllar og tengdir útreikningar kostnaðarhluta ekki tiltækir á SKUs. Nánari upplýsingar um staðalkostnað er að fá með því að  [Reikna út staðlaðan kostnað](finance-about-calculating-standard-cost.md)

## Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Warehouse Management Overview](design-details-warehouse-management.md)
[Inventory](inventory-manage-inventory.md)  
[Samsetningardeild](assembly-assemble-items.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
