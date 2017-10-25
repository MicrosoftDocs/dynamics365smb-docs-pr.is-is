---
title: "Hvernig á að: Breyta fyrirliggjandi staðsetningum í vöruhúsastaðsetningar | Microsoft Docs"
description: "Hægt er að láta birgðageymslu sem til er nota svæði og hólf og vinna sem vöruhúsastað."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 01081b166df81a76bba984bcb679069e59c660c9
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-convert-existing-locations-to-warehouse-locations"></a>Hvernig á að breyta fyrirliggjandi staðsetningum í vöruhúsastaðsetningar
Hægt er að láta birgðageymslu sem til er nota svæði og hólf og vinna sem vöruhúsastað.  

Keyrslan til að gera birgðageymslu virka fyrir vöruhúsaðgerðir stofnar upphafsfærslur vöruhúss fyrir leiðréttingarhólf vöruhúss fyrir allar vörur sem geymdar eru í birgðageymslunni. Þessar upphafsfærslur verða jafnaðar þegar raunbirgðafærslur vöruhúss eru færðar inn eftir keyrslu keyrslunnar.  

Hægt er að stofna svæði og hólf fyrir eða eftir umbreytinguna. Eina hólfið sem þarf að stofna fyrir umbreytinguna er það sem notað verður sem leiðréttingarhólf í framtíðinni.  

> [!IMPORTANT]  
>  Til að hreinsa allar neikvæðar birgðir og öll opin vöruhúsaskjöl áður en birgðageymslu er umbreytt fyrir vöruhúsameðhöndlun skal keyra skýrslu til að finna vörurnar með neikvæðar birgður og opin vöruhúsaskjöl fyrir birgðageymsluna. Frekari upplýsingar eru í Athuga neikvæða birgðastöðu.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Birgðageymsla sett upp sem vöruhúsastaður  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Stofna vöruhúsastað** og velja svo viðeigandi tengil.  
2.  Í reitnum **Kóti birgðageymslu** skal tilgreina birgðageymslu sem á að virkja fyrir úrvinnslu vöruhúss  
3.  Í reitnum **Kóti leiðréttingarhólfs** skal tilgreina hólfinu í birgðageymslunni þar sem ósamstilltar vöruhúsafærslur eru geymdar. Nánari upplýsingar má nálgast á „Samstilla leiðréttar vöruhúsafærslur við tengdar birgðabókafærslur“ hlutanum í [Hvernig skal: Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md).  

    Opnu birgðafærslurnar fyrir tilgreindu birgðageymsluna eru notaðar í kerfinu til að stofna vöruhúsabókarlínur sem leggja saman allar samsetningar á vörunúmeri, afbrigðiskóta, mælieiningarkóta og, ef nauðsynlegt er, lotunúmeri og raðnúmeri í birgðafærslunum. Vöruhúsabókarlínurnar bókast þá. Þessi bókun stofnar vöruhúsafærslur sem setja birgðirnar í leiðréttingarhólf vöruhúss. Kerfið setur einnig **Kóta leiðréttingarhólfs** á Birgðageymsluspjaldið.  

4.  Til að sjá hvaða vörum var bætt í leiðréttingarhólfið í keyrslunni er hægt að keyra skýrsluna **Leiðréttingarhólf vöruhúss**.  
5.  Þegar keyrslunni **Búa til birgðageymslu vöruhúss** er lokið þarf að framkvæma og bóka raunbirgðatalningu vöruhúss. Frekari upplýsingar, sjá [Hvernig skal: Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  Mælt er með því að **Búa til birgðageymslu vöruhúss** runuvinnslan sé keyrð á tíma sem ekki hefur áhrif á dagleg störf í kerfinu. Keyrslan vinnur með hverja færslu í töflunni **Birgðafærsla** og ef margar birgðafærslur eru til staðar getur keyrslan tekið margar klukkustundir.  

 Í þeim birgðageymslum þar sem vöruhúsastjórnunarskjöl voru ekki notuð fyrir umbreytinguna þarf að opna aftur og gefa út öll upprunaskjöl sem voru móttekin eða afhent að hluta fyrir umbreytinguna.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

