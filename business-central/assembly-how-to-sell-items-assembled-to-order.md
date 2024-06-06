---
title: Selja hluti sem eru settir saman í pöntun
description: Læra að selja vöru sem er sett saman í pöntun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# Selja hluti sem eru settir saman í pöntun

Ekki er búist við að vörur sem settar eru upp fyrir samsetningar-í-pöntun verði í birgðum og verða settar saman þegar þær eru innifaldar á sölupöntun. Vara er sett upp fyrir samsetningu eftir pöntun þegar í reitnum **Samsetningarstefna** á birgðaspjaldinu er **Samsetning eftir pöntun**. Þegar varan er færð inn í sölupöntunarlínu er samsetningarpöntun sjálfkrafa stofnuð og tengd við sölupöntunina.  

> [!NOTE]  
> Ef vörur sem eru settar saman eftir pöntun eru þegar í birgðum er hægt að draga magnið frá samsetningarpöntuninni og taka það frá úr birgðum. Nánari upplýsingar um sölu birgðavara [í flæði samsetningar í pöntun](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Í þessu ferli er sala vöru sem verður sett saman samkvæmt óskum viðskiptamannsins meðhöndluð. Leiðbeiningarnar fela í sér: 

* Sölupöntunarlína stofnuð.
* Sérstilling samsetningarvörunnar með því að breyta íhlutum hennar og forða.
* Athuga ráðstöfunarmagn til að stofna afgreiðsludagsetningu.
* Gefa út sölupöntunina sem á að setja saman og afhenda strax.  

> [!NOTE]  
> Eftirfarandi ferli tekur ekki með skref til að stofna staðlaða sölupöntun sem gerist á undan skrefinu þar sem samsetning-á-pöntun vara er færð inn í sölupöntunarlínu. Nánari upplýsingar um stofnun sölupantana á [Selja vörur með sölupöntun viðskiptamanns](sales-how-sell-products.md).  

## Til að selja vöru sem er sett saman í pöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofnið sölupöntun. 
3. Í reitnum **númer** færið inn vöru sem stillt eru til að setja saman í pöntun.  
4. Í reitnum **Kóti birgðageymslu** er tilgreind sú birgðageymsla sem varan mun verða seld frá. Samsetningarferlið fer fram í þeirri birgðageymslu.  
5. Í reitnum **Magn** er fært inn hversu margar einingar á að selja.  

    > [!NOTE]  
    >  Ef einn eða fleiri íhlutir í umbeðnu samsetningarvörumagni eru ekki tiltækir opnast viðvörunarsíða um ráðstöfunarmagn. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Samsetningarpöntun er stofnuð og tengd sölupöntunarlínunni. Skiladagsetning samsetningarpöntunarinnar er afhendingardagsetning sölupöntunarlínunnar.  

    Magnið sem á að selja er afritað í reitinn **Magn til samsetningar í pöntun**, sem gefur til kynna að vöruuppsetningin vænti þess að sett verði saman allt magnið í sölulínunni. Hægt er að minnka magnið sem á að setja saman, til dæmis ef vitað er að sumar vörur eru þegar til. Nánari upplýsingar um sölu birgðavara [í flæði](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md) samsetningar í pöntun.  

6. Ef viðskiptamaðurinn vill viðbótarvöru í setti skal á flýtiflipanum **Línur** velja aðgerðina **Lína**, velja aðgerðina **Setja saman til pöntunar** og velja svo aðgerðina **Setja saman til pöntunarlínur** til að skoða og breyta stöðluðum samsetningaríhlutum. Að öðrum kosti skal velja reitinn **Magn til samsetningar til pöntunar**.  
7. Á síðunni **Setja saman til pöntunarlínur** er búin til ný lína af tegundinni **Vara** fyrir viðbótarsamsetningaríhlutinn.  

    Einnig er hægt að sérstilla pöntunina með því að auka magn einnar staðlaðrar vöru í pökkuninni. Hægt er að gera þetta með því að auka gildið í reitnum **Magn á** á viðkomandi samsetningarpöntunarlínu.  

    > [!NOTE]  
    >  Síðan **Setja saman til pöntunarlínur** inniheldur aðeins grunnreiti til að sérstilla íhlutalistann, bæta við vörurakningarnúmerum eða leysa vandamál með tiltækum íhlutum. Til að bæta við upplýsingum um samsetningarpöntun, svo sem upphafsdagsetningu samsetningarpöntunar, skal velja aðgerðina **Sýna skjöl** . Þá opnast fullt yfirlit yfir samsetningarpöntunina sem er tengd við sölupöntunarlínuna. Ekki er hægt að breyta innihaldi flestra reita í samsetningarpöntunarhausnum og ekki er hægt að bóka samsetningarafköst úr honum. Bóka verður afhendingu sölupöntunarlínunnar.  
    >
    >  Á tengdum samsetningarpöntunum er aðeins hægt að breyta reitnum **Upphafsdagsetning** . Ef upphafsdagsetningunni er breytt tilgreina samsetningarstarfsmenn að þeir séu að hefja samsetningu á undan skiladeginum. Öllum reitum í línunum á tengdu samsetningarpöntuninni er hægt að breyta svo að vöruhússstarfsmenn geti fært inn notkunartölur við vinnsluna.  

8. Fara skal yfir eða bregðast við vandamálum með ráðstöfun íhluta. Til dæmis er staðgengdarvara valin.  
9. Loka síðunni **Setja saman í pöntunarlínur**. Tengda samsetningarpöntunin er tilbúin og starfsmenn geta hafist handa við að setja saman sérsniðnu vörurnar.  
10. Á sölupöntuninni skal velja **Losa** aðgerðina til að tilkynna samsetningardeildinni að sem samsetningarferlið geti hafist. Nánari upplýsingar um [samsetningarvörur](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Staðgenglar vöru skipta ekki sjálfkrafa út vöru fyrir aðra vöru, til dæmis þegar sölupöntun er stofnuð eða uppskrift. Þess í stað verður þú varaður við því að staðgengill sé tiltækur.

## Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]