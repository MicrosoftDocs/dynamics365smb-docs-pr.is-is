---
title: Hvernig á að setja upp birgðageymslur til að þær noti hólf
description: Hólf tákna grunnvöruhúsauppbyggingu og eru notuð til að gera tillögur að staðsetningu vöru.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="set-up-locations-to-use-bins"></a>Setja upp birgðageymslur til að þær noti hólf

Hólf tákna grunnvöruhúsasamsetninguna og þau eru notuð til að leggja til hvar setja eigi vörur. Þegar hólfin hafa verið stofnuð skilgreinast innihald þeirra eða láta þau þjóna sem fljótandi hólf án tiltekins innihalds.

Til að nota hólfaaðgerðina í birgðageymslu er kveikt á hólfinu **áskilin** vífæri á **birgðageymsluspjaldinu** . Þegar kveikt hefur verið á VÍV eru reitirnir **Hólfkóti** og **Svæðiskóti** tiltækir á eftirfarandi skjölum:

* Vöruhúsamóttökuhaus
* Vöruhúsamóttökulínur
* Frágangslínur vöruhúss
* Vöruhúsaafhendingarhaus
* Vöruhúsaafhendingarlínur
* Frágangslínur vöruhúss

Næsta skref er að hanna vöruflæðið í birgðageymslunni með því að tilgreina hólfakóta í uppsetningarreitum sem tákna mismunandi flæði.  

> [!NOTE]  
> Stofna verður hólfakóta áður en hægt er að tilgreina þá fyrir birgðageymsluna. Frekari upplýsingar eru í [Stofna hólf](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Til að setja upp birgðageymslur til að þær noti hólf

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2. Veljið birgðageymsluna þar sem á að nota hólf.  
3. Veldu aðgerðina **Breyta**.  
4. Á flýtiflipanum **Vöruhús** er gátreiturinn Hólf áskilið **valinn**.  
5. Ef ekki er notaður beinn frágangur og tínsla er valin aðferðin sem **nota á til að úthluta vöru sjálfgefnu hólfi í** reitnum Sjálfgefið hólfaval [!INCLUDE [prod_short](includes/prod_short.md)] .  
6. Opna spjaldið fyrir birgðageymsluna sem setja á upp hólf fyrir.
7. Á flýtiflipanum **Hólf** eru valin hólf sem á að nota sem sjálfgildi fyrir móttökur, afhendingar, á innleið, útleið og opin vinnusalarhólf.  

    Hólfakótarnir sem eru tilgreindir birtast sjálfkrafa á hausum og línum ýmissa vöruhúsaskjala. Sjálfgefnu hólfin skilgreina allar upphafs- og lokastaðsetningar vara í vöruhúsinu.  
8. Ef notaður er beinn frágangur og tínsla skal velja hólf fyrir vöruhúsaleiðréttingar. Hólfakótinn í reitnum **Kóti** leiðréttingarhólfs skilgreinir sýndarhólfið sem skrá á misræmi í birgðum:

    * Þegar mismunur kemur upp sem skráður er í birgðabók vöruhúss
    * Mismunur reiknaður þegar raunbirgðir vöruhúss eru skráðar  
9. Valfrjálst: Fyllt er í reitina á flýtiflipanum **Hólfareglur** . Mikilvægustu reitirnir eru **Hólfageturegla**, **Leyfa einingaskipti** og **Kóti frágangssniðmáts**.  
10. Á flýtiflipanum **Vöruhús** skal fylla út reitina **Afgr.tími vara á útl. úr vöruh.**, **Afgr.tími vara á innl. úr vöruh.** og **Kóti grunndagatals**. Nánari upplýsingar eru í [Setja upp grunndagatöl](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin"></a>Notkunarhólfið fyllt út

Eftirfarandi flæðirit sýnir hvernig **reiturinn Hólfkóti** í íhlutalínum framleiðslupöntunar er fylltur út samkvæmt uppsetningu birgðageymslu.

:::image type="content" source="media/binflow.png" alt-text="Reiturinn Hólfkóti í framleiðslupöntunaríhlutalínum.":::

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
