---
title: Selja birgðavörur í flæðum samsetningar í pöntun
description: Samsettar vörur eru settar saman fyrir sölupantanir með samsetningarpöntun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="selling-inventory-items-in-assemble-to-order-flows" />Selja birgðavörur í flæðum samsetningar í pöntun

 **Ef reiturinn Samsetningarregla**  á birgðaspjaldinu sem um er að ræða  **saman við pöntun** á sölupöntun er gert ráð fyrir að varan sé ekki í birgðum og hún verði að vera sett saman vegna sölupantana. Þegar vörunni er bætt í línu í sölupöntun  [!INCLUDE [prod_short](includes/prod_short.md)]  býr til samsetningarpöntun sem er tengd sölupöntuninni. Til að fræðast nánar um hvernig á að selja samsettar vörur er farið í að  [selja vörur saman til að panta](assembly-how-to-sell-items-assembled-to-order.md). Ef magn sölupöntunar er hins vegar þegar tiltækt í birgðum er hægt að lækka sendingarpöntunarmagnið með því að breyta  **reitunum magn til að setja saman í pöntunarsvæði**  á sölupöntunarlínunni.  

Það er tiltölulega sjaldgæft fyrir fyrirtæki að selja vörur í birgðum sem samsettar vörur. Vörur í samsetningum eru yfirleitt ekki staðlaðar. Þeir eru sérsniðnir að þörfum ákveðinna viðskiptavina. Hins vegar er hægt að hafa magn saman við pöntunarvörur í birgðum vegna skila eða afturköllunar pöntunar. Það magn skal taka til og selja áður en ný Bú eru sett saman.  

> [!NOTE]  
> Til að athuga hvort hvort samsettar vörur eru þegar tiltækar fyrir samsetningar pantana skal nota  **upplýsingakassa Sölulínuupplýsingar**  í sölupöntuninni.  

Það er hægt að gera svipaða hluti þegar vörur eru seldar úr birgðum og eitthvert eða allt magn er ekki tiltækt. Hægt er að veita vantar magn með samsetningarpöntun. Til að fræðast meira um sölu birgða og samsetningarvöru er farið í að  [selja samsettar vörur og birgðavörur saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Það eru reglur sem gilda  **um reitinn Magn til sendingar**  á sölupöntunarlínum sem innihalda samsetninguna magn til pöntunar og birgðamagn. Til að fræðast nánar um reglurnar er farið í  [samsettri atburðarás](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Í þessu ferli, er skipt út samsetninarpöntunarmagni við birgðamagn í sölupöntunarlínu. Eftirfarandi leiðbeiningar veita yfirlit:

1. Ákvarða framboð.
2. Draga úr því magni úr tengdu samsetningarröðinni.
3. Taka birgðamagn frá til að ganga úr skugga um að það sé tekið til og afhent fyrir pöntunina.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows" />Til að selja birgðavörur í flæðum samsetningar í pöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofnið sölupöntun. Til að fræðast um stofnun sölupantana er farið að  [selja afurðir](sales-how-sell-products.md).  
3. Í sölupöntunarlínu sem inniheldur saman pöntunarvöru í  **reitnum Magn**  er magnið fært inn.  
4.  **Í upplýsingakassa Sölulínuupplýsinga**  skal ákvarða hvort eitthvað magn er tiltækt.  
5. Í reitnum **Magn til samsetningar til pöntunar** er tiltækt magn dregið frá þannig að einungis ótiltækt magn er sett saman í pöntunina. Reiturinn **Frátekið magn** er minnkaður í samræmi við það til að gefa til kynna að tengillinn á pöntun fyrir pöntun, eða frátektin, á einungis við magn sem á að setja saman.  
6. Á flýtiflipanum **Línur** skal velja **Aðgerðir** og síðan aðgerðina **Taka frá**.  
7. Á síðunni **Frátekning** skal velja birgðafærsluna eða línurnar sem hafa að geyma tiltækt magn á flipanum **Taka frá í gildandi línu** og velja svo **Í lagi** hnappinn.  

     **Á sölupöntuninni**  er síðan  **Frátekið magn**  sýnir nú að fullt magn fyrir pöntunarlínuna er frátekið.  **Magn til að setja saman við pöntunarsvæði**  endurspeglar samt magnið sem á að setja saman.  

8. Sleppið sölupöntuninni til að gera vörurnar tiltækar fyrir tiltekt og til samsetningar á ótiltæknum vörum. Til að fræðast meira um þing er farið í að  [setja saman atriði](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  **Reiturinn Hólfakóti**  í sölupöntuninni gæti innihaldið gildið úr  **svæðunum sameina-til-Hólfkóti**  eða  **kóti**  frá-samsetning hólfs á birgðageymsluspjaldinu. Ef það er gert  **gæti reiturinn Hólfakóti**  í sölupöntunarlínunni verið rangur fyrir þessa samsetningu samsetja og lagermagns í samsetningum. Það er góð hugmynd að tvöfalda í það að hólfið í  **reitnum Hólfakóti**  virki fyrir allt magn. Að öðrum kosti skal færa inn tvenns konar mismunandi magn í aðskildar sölupöntunarlínur.  

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
