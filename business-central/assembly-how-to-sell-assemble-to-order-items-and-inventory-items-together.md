---
title: Selja vörur sem eru settar saman í pöntun og birgðavörur saman
description: Ef hluti samsetningarvöru er ekki tiltækur er hægt að stofna samsetningarpöntun fyrir eftirstandandi magn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Selja vörur sem eru settar saman í pöntun og birgðavörur saman

Ef reiturinn **Samsetningarstefna** á birgðaspjaldi samsetningarvöru inniheldur **Samsetning til birgða** gerir sölupöntunarvinnslan ráð fyrir því að varan sé þegar sett saman og hægt sé að taka hana úr birgðum ef hún er tiltæk. Þess vegna er samsetningarpöntun ekki sjálfkrafa stofnuð og tengd við sölupöntunarlínuna. Hins vegar, ef eitthvað eða allt magn er ekki tiltækt er hægt að stofna samsetningarpöntun fyrir eftirstandandi magn. Það er gert með því að fylla út reitinn **Magn til samsetningar í pöntun** í sölupöntunarlínunni. Með þessari stillingu er hægt að setja vöruna saman til pöntunar þótt hún sé sett saman á lager.  

Sveigjanleiki er svipaður þegar selt er samsetning-fyrir-pöntun vörur og eitthvað af magninu er þegar í birgðum. Draga þarf það magn frá samsetningarpöntuninni. Nánari upplýsingar um sölu birgðavara eru notaðar til að [selja birgðavörur í flæði samsetningar í pöntun](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Það eru reglur sem gilda um reitinn **Magn til afhendingar** í sölupöntunarlínum sem innihalda samsetningarmagn og birgðamagn. Nánari upplýsingar um reglurnar fást [í Samsetningaraðstæður](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> Eftirfarandi ferli fylgir ekki sölupöntunarskrefunum sem þarf að fylgja áður en samsetningarpöntun er stofnuð fyrir ekki tiltækt magn.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Til að selja vörur sem eru settar saman í pöntun og birgðavörur saman

1. Á sölupöntunarlínu fyrir vöru sem er sett saman á lager er fært inn magn í reitinn **Magn** sem er yfir birgðum. Síðan **Kanna ráðstöfunargetu** birtist. Nánari upplýsingar um vörur til ráðstöfunar eru skoðaðar með því að skoða [vörur](inventory-how-availability-overview.md) til ráðstöfunar.
2. Í reitinn **Magn til samsetningar til pöntunar** er fært inn gildið úr reitnum **Heildarmagn** .  
3. Gera allar breytingar sem þarf á samsetningaríhlutunum. Nánari upplýsingar um sölu á [vörum sem settar eru saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  
4. Gefa út sölupöntunina til að gera vörurnar tiltækar fyrir tínslu og samsetningu ótilgreindra vara. Nánari upplýsingar um stöðluðu samsetningarskrefin er farið í [Samsetningarvörur](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Reiturinn **Hólfkóti** á sölupöntuninni gæti innihaldið gildið úr reitunum **Hólfakóti samsetningar til afhendingar eða** Hólfakóti **frá**-samsetningar á birgðageymsluspjaldinu. Ef svo er **gæti reiturinn Hólfkóti** á sölupöntunarlínunni verið rangur fyrir þessa samsetningu samsetningar-í-pöntun og samsetningar til birgðamagns. Mælt er með því að tvísvara að hólfið í reitnum **Hólfkóti** virki fyrir allt magn. Að öðrum kosti skal færa inn tvenns konar mismunandi magn í aðskildar sölupöntunarlínur.  

## <a name="see-also"></a>Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
