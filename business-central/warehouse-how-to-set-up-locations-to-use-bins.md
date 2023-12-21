---
title: Hvernig á að setja upp birgðageymslur til að þær noti hólf
description: Hólf tákna grunnvöruhúsauppbyggingu og eru notuð til að gera tillögur að staðsetningu vöru.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# Setja upp birgðageymslur til að þær noti hólf

Hólar standa fyrir grunnvöruhúsaleiðunum og eru þær notaðar til að leggja til hvar á að setja vörur. Þegar búið er að stofna hólfin eru þau skilgreind sem efni þeirra eða þeim þjónað sem fljótandi hólf án tiltekins innihalds.

Ef nota á hólfaðgerðina í birgðageymslu er kveikt á  **hólfi sem er skylda**  á  **birgðageymsluspjaldinu** . Þegar búið er að kveikja á víxl er svæði fyrir  **hólfakóta**  og  **svæðiskóða**  tiltækt á eftirfarandi skjölum:

* Móttökuhaus vöruhúss
* Móttökulínur vöruhúss
* Vöruhúsafrágangslínur
* Haus vöruhúsaafhendingar
* Afhendingarlínur vöruhúss
* Vöruhúsafrágangslínur

Næsta skref er að hanna vöruflæðið á staðnum með því að tilgreina hólfakóta í uppsetningarsvæðum sem tákna mismunandi flæði.  

> [!NOTE]  
> Stofna verður hólfakóta áður en hægt er að tilgreina þá fyrir birgðageymsluna. Frekari upplýsingar eru í [Stofna hólf](warehouse-how-to-create-individual-bins.md).  

## Til að setja upp birgðageymslur til að þær noti hólf

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2. Veljið birgðageymsluna þar sem á að nota hólf.  
3. Veldu aðgerðina **Breyta**.  
4.  **Á flipanum Vöruhús**  er gátreiturinn Hólfáskilinn  **valinn** .  
5. Ef ekki er notaður beinn frágangur og tínsla í birgðageymslunni er valin aðferðin  **sem nota á til að úthluta sjálfgefnu hólfi á vöru, í**  reitnum sjálfgefið val [!INCLUDE [prod_short](includes/prod_short.md)] .  
6. Opna spjaldið fyrir birgðageymsluna sem setja á upp hólf fyrir.
7.  **Á flipanum hólf**  eru hólfin valin sem nota á sem sjálfgildi fyrir kvittanir, afhendingar, inn-, út-og opin vinnugólfhólf.  

    Hólfakóðar sem tilgreindir eru birtast sjálfkrafa á hausum og í línum ýmissa vöruhúsaskjala. Sjálfgefnu hólfin skilgreina allar upphafs- og lokastaðsetningar vara í vöruhúsinu.  
8. Ef notaður er beinn frágangur og tínsla er hólf fyrir vöruhúsaleiðréttingar valið. Hólfakótinn í  **reitnum kóti**  leiðréttingarhólfs skilgreinir sýndarhólfið þar sem skrá á misræmi í birgðum:

    * Þegar mismunur er skráður í birgðabókarbók vöruhúss
    * Mismunur reiknaður þegar efnislegar birgðir vöruhúss eru skráðar  
9. Valfrjálst: Reitirnir á flipanum hólfstefna  **eru**  fylltir út. Mikilvægustu reitirnir eru **Hólfageturegla**, **Leyfa einingaskipti** og **Kóti frágangssniðmáts**.  
10. Á flýtiflipanum **Vöruhús** skal fylla út reitina **Afgr.tími vara á útl. úr vöruh.**, **Afgr.tími vara á innl. úr vöruh.** og **Kóti grunndagatals**. Til að fá frekari upplýsingar er farið í að  [Setja upp grunndagatöl](across-how-to-assign-base-calendars.md).

## Reiturinn notkunarhólf er fylltur út

Eftirfarandi Flæðirit sýnir hvernig  **reiturinn Kóti hólfakóta**  í framleiðslupöntunaríhlutalínum er fylltur út eftir uppsetningu birgðageymslunnar.

:::image type="content" source="media/binflow.png" alt-text="Reiturinn Kóti hólfs í framleiðslupöntunaríhlutalínum.":::

## Sjá einnig .

[Warehouse Management Overview](design-details-warehouse-management.md)
[Inventory](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
