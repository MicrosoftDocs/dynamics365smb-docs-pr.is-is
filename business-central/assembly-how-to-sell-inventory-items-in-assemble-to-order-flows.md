---
title: Selja birgðavörur í flæðum samsetningar í pöntun
description: Samsetningarvörur í pöntun eru settar saman fyrir sölupantanir með samsetningarpöntun.
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
# Selja birgðavörur í flæðum samsetningar í pöntun

Ef reiturinn **Samsetningarstefna** á birgðaspjaldi samsetningarvöru inniheldur **Samsetning-til-pöntun** gerir sölupöntunarferlið ráð fyrir því að varan sé ekki í birgðum og verði að vera sett saman fyrir sölupantanir. Þegar vörunni er bætt við línu á sölupöntun [!INCLUDE [prod_short](includes/prod_short.md)]  stofnar samsetningarpöntun sem tengist sölupöntuninni. Nánari upplýsingar um hvernig á að selja samsetningarvörur fyrir pöntun er farið í [Selja vörur sem settar eru saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md). Hins vegar, ef eitthvað af magni sölupöntunar er þegar tiltækt í birgðum er hægt að minnka samsetningarpöntunarmagnið með því að breyta reitnum **Magn til samsetningar í Pöntun** á sölupöntunarlínunni.  

Það er tiltölulega sjaldgæft að fyrirtæki selji birgðavörur sem samsetningarvörur í pöntun. Vörur sem eru settar saman eftir pöntun eru yfirleitt ekki staðlaðar. Þær eru sérsniðnar til að uppfylla sérstakar kröfur viðskiptavina. Hins vegar gæti verið magn vöru í birgðum settar saman vegna afturkallana eða afturkallana pantana. Það magn skal tína og selja áður en nýtt er sett saman.  

> [!NOTE]  
> Til að kanna hvort samsetningarvörur í pöntun séu þegar tiltækar fyrir samsetningarpantanir er upplýsingakassinn **sölulínuupplýsinga** notaður í sölupöntuninni.  

Hægt er að gera svipaða hluti þegar verið er að selja samsetningarvörur úr birgðum og sumt eða allt magnið er ekki tiltækt. Hægt er að gefa magnið sem vantar með samsetningarpöntun. Nánari upplýsingar um sölu birgða og samsetningarvara eru settar [saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) í Selja samsetningarvörur og Vörur í birgðum.  

> [!NOTE]  
> Það eru reglur sem gilda um reitinn **Magn til afhendingar** í sölupöntunarlínum sem innihalda samsetningarmagn og birgðamagn. Nánari upplýsingar um reglurnar fást [í Samsetningaraðstæður](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Í þessu ferli, er skipt út samsetninarpöntunarmagni við birgðamagn í sölupöntunarlínu. Eftirfarandi skref gefa yfirlit:

1. Ákvarða ráðstöfunarmagn.
2. Minnkun þess magns úr tengdu samsetningarpöntuninni.
3. Taka frá birgðamagn til að ganga úr skugga um að það sé tínt og afhent fyrir pöntunina.  

## Til að selja birgðavörur í flæðum samsetningar í pöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofnið sölupöntun. Til að fá upplýsingar um stofnun sölupantana er farið í [Selja vörur](sales-how-sell-products.md).  
3. Magnið er fært inn í sölupöntunarlínu sem inniheldur vörusamsetningar fyrir pöntun í reitnum **Magn** .  
4.  **Í upplýsingakassa sölulínu** er ákvarðað hvort eitthvað af öllu magni er til ráðstöfunar.  
5. Í reitnum **Magn til samsetningar til pöntunar** er tiltækt magn dregið frá þannig að einungis ótiltækt magn er sett saman í pöntunina. Reiturinn **Frátekið magn** er minnkaður í samræmi við það til að gefa til kynna að tengillinn á pöntun fyrir pöntun, eða frátektin, á einungis við magn sem á að setja saman.  
6. Á flýtiflipanum **Línur** skal velja **Aðgerðir** og síðan aðgerðina **Taka frá**.  
7. Á síðunni **Frátekning** skal velja birgðafærsluna eða línurnar sem hafa að geyma tiltækt magn á flipanum **Taka frá í gildandi línu** og velja svo **Í lagi** hnappinn.  

    Á síðunni **Sölupöntun** sýnir reiturinn **Frátekið magn** nú að allt magnið fyrir pöntunarlínuna er frátekið. Reiturinn **Magn til samsetningar til pöntunar** sýnir samt magnið sem á að setja saman.  

8. Gefa út sölupöntunina til að gera vörurnar tiltækar fyrir tínslu og samsetningu ótilgreindra vara. Nánari upplýsingar um samsetningu vöru er farið í [Samsetningarvörur](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Reiturinn **Hólfkóti** á sölupöntuninni gæti innihaldið gildið úr reitunum **Hólfakóti samsetningar til afhendingar eða** Hólfakóti **frá**-samsetningar á birgðageymsluspjaldinu. Ef svo er **gæti reiturinn Hólfkóti** á sölupöntunarlínunni verið rangur fyrir þessa samsetningu magns samsetningar og magns sem sett er saman til á lager. Mælt er með því að tvísvara að hólfið í reitnum **Hólfkóti** virki fyrir allt magn. Að öðrum kosti skal færa inn tvenns konar mismunandi magn í aðskildar sölupöntunarlínur.  

## Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
