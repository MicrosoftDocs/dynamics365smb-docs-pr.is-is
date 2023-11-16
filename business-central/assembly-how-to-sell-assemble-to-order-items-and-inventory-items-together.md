---
title: Selja vörur sem eru settar saman í pöntun og birgðavörur saman
description: Ef hluti af saman-lager vöru er ekki tiltækur er hægt að stofna samsetningarpöntun fyrir eftirstandandi magn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Selja vörur sem eru settar saman í pöntun og birgðavörur saman

 **Ef reiturinn Samsetningarregla**  á birgðaspjaldinu sem  **er í samsetningunni er að setja saman lager**, gerir sölupöntunarferlið ráð fyrir að varan sé þegar sett saman og hægt að taka hana úr birgðum ef hún er tiltæk. Þess vegna er samsetningarpöntun ekki sjálfkrafa stofnuð og tengd við sölupöntunarlínuna. Ef magnið er hins vegar ekki tiltækt er hægt að búa til samsetningarpöntun fyrir eftirstandandi magn. Það er gert með því að fylla inn í  **reitinn Magn til að taka saman í pöntunarreit**  á sölupöntunarlínunni. Með þessari stillingu er hægt að setja vöruna saman til pöntunar þótt hún sé sett upp til að setja hana saman við birgðir.  

Þú hefur svipaðan sveigjanleika þegar þú selur samsettar vörur og sumt af magninu er nú þegar í birgðum. Þú munt vilja draga það magn úr samsetningarpöntuninni. Til að fræðast meira um sölu birgðavara er farið í að  [selja birgðavörur í saman-Pöntunarflæði](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Það eru reglur sem gilda  **um reitinn Magn til sendingar**  á sölupöntunarlínum sem innihalda samsetninguna magn til pöntunar og birgðamagn. Til að fræðast nánar um reglurnar er farið í  [samsettri atburðarás](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> Í eftirfarandi ferli eru ekki þau sölupöntunarskref sem þarf að fylgja áður en samsetningarpöntun er stofnuð fyrir tiltækt magn.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Til að selja vörur sem eru settar saman í pöntun og birgðavörur saman

1. Í sölupöntunarlínu fyrir saman birgðir til-vöru, Færið inn magn í  **reitinn Magn**  sem er yfir birgðum. Síðan **Kanna ráðstöfunargetu** birtist. Til að fræðast meira um vöruframboð er farið í að  [Skoða framboð vara](inventory-how-availability-overview.md).
2.  **Í reitnum Magn til að setja saman við röð**  er fært inn gildið úr  **reitnum heildarmagn** .  
3. Gera þær breytingar sem nauðsynlegar eru á samsetningarþáttunum. Læra meira at  [selja vörur saman til að panta](assembly-how-to-sell-items-assembled-to-order.md).  
4. Sleppið sölupöntuninni til að gera vörurnar tiltækar fyrir tiltekt og til samsetningar á ótiltæknum vörum. Til að fræðast meira um stöðluð samsetningarskref er farið í  [setja saman atriði](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  **Reiturinn Hólfakóti**  í sölupöntuninni gæti innihaldið gildið úr  **svæðunum sameina-til-Hólfkóti**  eða  **kóti**  frá-samsetning hólfs á birgðageymsluspjaldinu. Ef það er  **gæti reiturinn Hólfakóti**  í sölupöntunarlínunni verið rangur fyrir þessa samsetningu samsetja og lagermagns í samsetningum. Það er góð hugmynd að tvöfalda í það að hólfið í  **reitnum Hólfakóti**  virki fyrir allt magn. Að öðrum kosti skal færa inn tvenns konar mismunandi magn í aðskildar sölupöntunarlínur.  

## <a name="see-also"></a>Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
