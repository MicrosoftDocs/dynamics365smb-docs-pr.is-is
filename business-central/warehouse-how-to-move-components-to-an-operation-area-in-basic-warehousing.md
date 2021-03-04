---
title: Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss
description: Ef vöruvinnsla fer fram í vöruhúsi gæti þurft að færa vörur á milli innri hólfa í samræmi við innri upprunaskjöl.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7812bc0675563b30805f345331423d800645b3ea
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014101"
---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss
Ef vöruvinnsla fer fram í vöruhúsi gæti þurft að færa vörur á milli innri hólfa í samræmi við innri upprunaskjöl, svo sem framleiðslu-, samsetningar- eða þjónustupantanir úr birgðageymslu.  

> [!NOTE]  
>  Upplýsingar um hvernig færa á vörur á milli hólfa án upprunaskjala eru í Innri hreyfing.  

Í ítarlegri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota uppsetningarreitinn **Beinn frágangur og tínsla**, er hægt að nota síðuna **Vinnublað hreyfingar** til að færa vörur milli hólfa. Nánari upplýsingar eru í [Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Í einfaldri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota uppsetningarreitina **Hólf áskilið** og **Krefjast tínslu** er hægt að skrá hreyfingar vara á svæði innri starfsemi samkvæmt innri upprunaskjölum á eftirfarandi hátt:  

-   Með síðunni **Birgðahreyfing**.  
-   Með síðunni **Birgðatínsla**.  

> [!NOTE]  
>  Birgðatínslur bóka einnig neikvæðar birgðafærslur sem notkun og eru aðeins studdar fyrir framleiðsluíhluti. Sjá síðuna Birgðatínsla fyrir frekari upplýsingar  

Til að fá nánari upplýsingar um birgðahreyfingar, sjá síðuna Birgðahreyfingar.  

Tvö mismunandi hlutverk geta stofnað upphafsbirgðahreyfinguna. Samsetningarstarfsmaður, til dæmis, getur stofnað hana úr útgefinni samsetningarpöntun þannig að hún birtist á lista starfsmanns í vöruhúsi yfir verk sem á eftir að gera. Ef búa á til birgðahreyfingu fyrir samsetningarpöntunarlínur sem eru tilbúnar til að láta flytja íhluti í tilgreind hólf sín notar samsetningarstarfsmaðurinn aðgerðina **Stofna birgðahreyfingu**.  

Að öðru kostir getur starfsmaður í vöruhúsi stofnað hana með því að benda á samsetningarpöntunina sem um ræðir. Þessu er lýst í eftirfarandi ferli.  

> [!NOTE]  
>  Ef hreyfing er til staðar fyrir samsetningarpöntun þegar vara er samsett úr sölupöntun er hægt að láta stofna birgðahreyfingaskjalið sjálfkrafa þegar birgðatínsluskjalið sem tekur við fullunnu samsetningarvörunni og bókar afhendingu er búið til. Til að setja þetta upp þarf að velja reitinn **Búa til hreyfingar sjálfvirkt** á **Uppsetning samsetningar** síunni.  
>   
>  Nánari upplýsingar um samsetningarpantanir og almennar vöruhúsaaðgerðir eru í [Meðhöndlun á vörum samsetningpöntunar með birgðatínslum](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Þessi verklýsing sýnir hvernig á að búa til birgðahreyfingu af síðunni **Birgðahreyfing** með því að vísa í útgefna samsetningarpöntun sem upprunaskjal. Ferlið er það sama þegar íhlutir eru færðir fyrir framleiðslupantanir og þjónustupantanir.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Til að færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðahreyfing** og veldu tengda tengilinn.  
2.  Á flýtiflipanum **Almennt** er reiturinn **Nr.** fylltur út . Hægt er að ýta á færslulykilinn til að velja úr númeraröð.  
3.  Í reitnum **Kóti birgðageymslu** er færð inn birgðageymslan þar sem hreyfingin á sér stað.  
4.  Valið er **Sækja upprunaskjöl** aðgerð. Að öðrum kosti er fyllt út í reitinn **Upprunaskjal** og valið svo hnappurinn **AssistEdit** í reitnum **Upprunanúmer**.  
5.  Á síðunni **Upprunaskjöl** er valin samsetningarpöntun sem á að færa íhluta í og veljið svo hnappinn **Í lagi**.  

    Fyrir hvern nauðsynlegan íhlut sem hægt er að flytja, eru ein Taka-lína og ein Setja-lína mynduð á síðunni **Birgðahreyfingar**. Allir reitir nema reiturinn **Magn til afgreiðslu** eru fylltir út fyrirfram samkvæmt upprunaskjalslínunum. Reiturinn **Magn til afgreiðslu** er stilltur á núll þar til magnið sem raunverulega hefur verið flutt er fært inn.  

    Hægt er að breyta hólfakóðanum á Taka-línunni, en aðeins í samræmi við ráðstöfunarmagn. Ef hnappurinn **AssistEdit** er valinn á reitnum **Hólfkóti** í Taka-línu mun síðan **Innihald hólfs** opnast og aðeins sýna hólf þarf sem íhluturinn er tiltækur.  

    Ekki er hægt að breyta hólfkóta í línu. Aðeins hólfkóti sem er skilgreindur á íhlutalínu upprunaskjalsins er samþykktur. Þetta styður þá reglu að hlutverkið sem biður um íhlut, sem er samsetningarstarfsmaður í þessu ferli, eigi að vita hvar eigi að setja íhlutinn. Ef setja á íhluti í annað hólf þarf að fyrst að breyta hólfakótanum í íhlutalínunni og stofna birgðahreyfingalínurnar aftur.  
6.  Í reitnum **Magn til afgreiðslu** er fært inn að fullu eða að hluta til magnið sem raunverulega hefur verið flutt. Gildið á línum Taka og Setja verður að vera það sama. Annars er ekki hægt að skrá hreyfinguna.  

    > [!NOTE]  
    >  Eins og í öðrum vöruhúsaaðgerðum er hægt að skipta Setja-línu með því að velja **Aðgerðir** og svo **Skipta línu**. Í því tilviki verður samtala uppskiptu Setja-línanna tveggja að vera jöfn magninu í Taka-línunni.  

7.  Þegar allt er til reiðu til að skrá hreyfingar sem hafa verið framkvæmdar er aðgerðin **Skrá birgðahreyfingu** valin.  

    Vöruhúsafærslur eru stofnaðar til að spegla að íhlutirnir eru nú til í hólfunum sem tilgreind eru á samsetningarpöntunarlínunum.  

    > [!NOTE]  
    >  Ólíkt því þegar íhlutir eru færðir með birgðatínslu er notkun ekki bókuð þegar birgðahreyfing er skráð. Það skref verður að framkvæma sérstaklega með því að bóka samsetningu pöntunar, frálag og notkun. Frekari upplýsingar, sjá Samsetningarpöntun.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]