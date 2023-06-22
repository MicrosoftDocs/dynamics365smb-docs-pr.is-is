---
title: Breyta fyrirliggjandi staðsetningum í vöruhúsastaðsetningar
description: Hægt er að láta birgðageymslu sem til er nota svæði og hólf og vinna sem vöruhúsastað.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 15
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="convert-existing-locations-to-warehouse-locations" />Breyta fyrirliggjandi staðsetningum í vöruhúsastaðsetningar
Hægt er að láta birgðageymslu sem til er nota svæði og hólf og vinna sem vöruhúsastað.  

Keyrslan til að gera birgðageymslu virka fyrir vöruhúsaðgerðir stofnar upphafsfærslur vöruhúss fyrir leiðréttingarhólf vöruhúss fyrir allar vörur sem geymdar eru í birgðageymslunni. Þessar upphafsfærslur verða jafnaðar þegar raunbirgðafærslur vöruhúss eru færðar inn eftir keyrslu keyrslunnar.  

Hægt er að stofna svæði og hólf fyrir eða eftir umbreytinguna. Eina hólfið sem þarf að stofna fyrir umbreytinguna er það sem notað verður sem leiðréttingarhólf í framtíðinni.  

> [!IMPORTANT]  
>  Til að hreinsa allar neikvæðar birgðir og öll opin vöruhúsaskjöl áður en birgðageymslu er umbreytt fyrir vöruhúsameðhöndlun skal keyra skýrslu til að finna vörurnar með neikvæðar birgður og opin vöruhúsaskjöl fyrir birgðageymsluna. Frekari upplýsingar eru í Athuga neikvæða birgðastöðu.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location" />Birgðageymsla sett upp sem vöruhúsastaður
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stofna staðsetningu vöruhúss** og velja síðan viðkomandi tengil.  
2.  Í reitnum **Kóti birgðageymslu** skal tilgreina birgðageymslu sem á að virkja fyrir úrvinnslu vöruhúss  
3.  Í reitnum **Kóti leiðréttingarhólfs** skal tilgreina hólfinu í birgðageymslunni þar sem ósamstilltar vöruhúsafærslur eru geymdar. Frekari upplýsingar er að finna í [Að samstilla leiðréttar vöruhúsafærslur við tengdar birgðabókafærslur](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).  

    Opnu birgðafærslurnar fyrir tilgreindu birgðageymsluna eru notaðar í kerfinu til að stofna vöruhúsabókarlínur sem leggja saman allar samsetningar á vörunúmeri, afbrigðiskóta, mælieiningarkóta og, ef nauðsynlegt er, lotunúmeri og raðnúmeri í birgðafærslunum. Vöruhúsabókarlínurnar bókast þá. Þessi bókun stofnar vöruhúsafærslur sem setja birgðirnar í leiðréttingarhólf vöruhúss. Kerfið setur einnig **Kóta leiðréttingarhólfs** á Birgðageymsluspjaldið.  

4.  Til að sjá hvaða vörum var bætt í leiðréttingarhólfið í keyrslunni er hægt að keyra skýrsluna **Leiðréttingarhólf vöruhúss**.  
5.  Þegar keyrslunni **Búa til birgðageymslu vöruhúss** er lokið þarf að framkvæma og bóka raunbirgðatalningu vöruhúss. Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir með færslubókum](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  Mælt er með því að **Búa til birgðageymslu vöruhúss** runuvinnslan sé keyrð á tíma sem ekki hefur áhrif á dagleg störf í kerfinu. Keyrslan vinnur með hverja færslu í töflunni **Birgðafærsla** og ef margar birgðafærslur eru til staðar getur keyrslan tekið margar klukkustundir.  

 Í þeim birgðageymslum þar sem vöruhúsastjórnunarskjöl voru ekki notuð fyrir umbreytinguna þarf að opna aftur og gefa út öll upprunaskjöl sem voru móttekin eða afhent að hluta fyrir umbreytinguna.  

## <a name="see-also" />Sjá einnig
[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
