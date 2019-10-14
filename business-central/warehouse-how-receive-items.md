---
title: Hvernig á að taka á móti vörum | Microsoft Docs
description: Þegar vörur berast í vöruhús sem er sett upp fyrir vinnslu vöruhúsamóttöku þarf að sækja línur útgefna upprunaskjalsins sem hrintu móttöku þeirra af stað.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ea8d952f6ef88415b0fef27c1694ad7d29672e64
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310455"
---
# <a name="receive-items"></a>Móttaka vara
Þegar vörur berast í vöruhús sem er ekki sett upp fyrir vinnslu vöruhúsamóttöku þarf einfaldlega að skrá móttökuna á viðeigandi viðskiptaskjal, eins og t.d. innkaupapöntun, sölvöruskilapöntun, eða millifærslupöntun á innleið.

Þegar vörur berast í vöruhús sem er sett upp fyrir vinnslu vöruhúsamóttöku þarf að sækja línur útgefna upprunaskjalsins sem hrintu móttöku þeirra af stað. Ef hólf eru notuð er annaðhvort hægt að samþykkja sjálfgefna hólfið sem er fyllt út eða, ef varan hefur ekki verið notuð fyrr í vöruhúsinu, fylla út hólfið þar sem á að taka vöruna frá. Síðan þarf að fylla út magn varanna sem hafa verið mótteknar og bóka móttökuna.  

## <a name="to-receive-items-with-a-purchase-order"></a>Vörur mótteknar með innkaupapöntun
Eftirfarandi lýsir því hvernig skal taka á móti vörum með innkaupapöntun. Skrefin eru svipuð fyrir söluvöruskilapöntun og millifærslupantanir.  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda hlekkinn.
2. Opna innkaupapöntun sem þegar er til eða stofna nýja. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Í reitnum **Magn til móttöku** er fært inn magnið sem hefur verið móttekið.

    Gildið í reitnum **Móttekið magn** er uppfært. Ef um er að ræða móttöku að hluta, getur þetta magn verið lægra en gildið í svæðinu **Magn**.
4. Valið er **Bóka** aðgerðin.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Vörur mótteknar með vöruhúsamóttöku
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **vöruhúsamóttaka** og veldu síðan tengda tengilinn.  
2.  Valið er **Nýtt** aðgerð.  

    Fyllt er út í reitina á flýtiflipanum **Almennt**. Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.  

    Fyrir grunngerð vöruhúss með beinan frágangur og tínsla ef birgðageymslan er með sjálfgefið svæði og hólf fyrir móttökur eru reitirnir **Svæðiskóði** og **Hólfakóði** fylltir út sjálfkrafa en hægt er að breyta þeim eftir þörfum.  

    > [!NOTE]  
    >  Ef taka á á móti vörum með öðrum vöruhúsaflokkskótum en flokkskóta hólfsins í reitnum **Hólfkóti** í fylgiskjalshausnum verður að eyða innihaldi reitsins **Hólfkóti** í hausnum áður en upprunaskjalslínurnar eru sóttar fyrir vörurnar.  
3.  Valið er **Sækja upprunaskjöl** aðgerð. Síðan **Upprunaskjöl** opnast.

    Í nýrri eða opinni vöruhúsamóttöku er hægt að nota síðuna **Afmörkun til að sækja upprunaskjal** til að sækja þær línur útgefna upprunaskjalsins sem segja til um hvaða vörur á að taka við eða afhenda.

    1. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.  
    3. Skilgreina hvaða gerð af upprunaskjalslínum eigi að sækja með því að fylla út viðeigandi afmörkunarreiti.  
    4. Velja skal aðgerðina **Keyra**.  

    Allar útgefnar upprunaskjalslínur sem uppfylla afmörkunarskilyrðin eru nú settar inn á síðunni **Vöruhússmóttaka** þar sem afmörkunaraðgerðin er virkjuð.  

    Skilgreindar afmörkunarsamsetningar eru vistaðar á síðunni **Afmarkanir til að sækja upprunaskjöl** þar til þeirra er næst þörf. Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

4.  Valin eru þau upprunaskjöl sem móttaka á vörur fyrir og smellt á **Í lagi** hnappinn.  

    Línurnar úr upprunaskjölunum birtast á síðunni **Vöruhúsamóttaka**. Reiturinn **Magn til móttöku** hefur verið fylltur út með eftirstöðvum hverrar línu en hægt er að breyta magninu eftir þörfum. Ef gildinu í reitnum  **Hólfkóti** er eytt á flýtiflipanum **Almennt** áður en línurnar eru sóttar þarf að færa inn viðkomandi hólfkóta í hverri móttökulínu.  

    > [!NOTE]  
    >  Til að fylla út í reitinn **Magn til móttöku** í öllum línum með núlli er valin aðgerðin **Eyða magni til móttöku**. Til að fylla reitinn aftur með eftirstöðvum er valið **Færa sjálfkr. inn magn til móttöku** aðgerðin.  

    > [!NOTE]  
    >  Ekki er hægt að taka á móti fleiri vörum en talan í reitnum **Magn eftirstöðva** á upprunaskjalslínunni segir til um. Til að taka á móti fleiri vörum skal sækja annað upprunaskjal sem inniheldur línu fyrir vöruna með því að nota afmörkun til að sækja upprunaskjöl með vörunni.  

5.  Bóka vöruhúsamóttökuna. Magnreitirnir eru uppfærðir í upprunaskjölunum og vörurnar eru skráðar sem hluti fyrirtækisbirgða.  

Ef vöruhúsafrágangur er notaður sendir kerfið móttökulínurnar í vöruhúsafrágangsaðgerðina. Þó vörurnar hafi verið mótteknar er ekki hægt að tína þær fyrr en gengið hefur verið frá þeim. Mótteknu vörurnar eru ekki greindar sem tiltækar birgðir fyrr en frágangurinn hefur verið skráður.  

Ef vöruhúsafrágangur er ekki notaður, en hólf, skráir kerfið frágang varanna í hólfinu sem er tilgreint í upprunaskjalslínunni.  

> [!NOTE]  
>  Ef aðgerðin **Bóka og prenta**, er notuð er móttakan bókuð ásamt því að frágangsleiðbeiningar sem sýna hvaða vörur á að setja í geymslu eru prentaðar.  
>   
>  Ef staðsetningin notar beinan frágang og tínslu notar kerfið frágangssniðmátin til að reikna út besta staðinn til að ganga frá vörunum. Þetta er síðan prentað í frágangsfyrirmælunum.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
