---
title: Móttaka vara
description: Þetta grein er yfirlit yfir mismunandi leiðir til að taka á móti vörum í vöruhúsi, t.d. vörum með innkaupapöntun eða vörum með vöruhúsamóttöku.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 6cca8d8f9b0ec28b149532581f9bc458022c3cd5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529515"
---
# <a name="receive-items"></a>Móttaka vara

Þegar vörur berast í vöruhús sem er ekki sett upp fyrir vinnslu vöruhúsamóttöku þarf einfaldlega að skrá móttökuna á viðeigandi viðskiptaskjal, eins og t.d. innkaupapöntun, sölvöruskilapöntun, eða millifærslupöntun á innleið.

Þegar vörur berast í vöruhús sem er sett upp fyrir vinnslu vöruhúsamóttöku þarf að sækja línur útgefna upprunaskjalsins sem hrintu móttöku þeirra af stað. Ef þú ert með hólf geturðu annaðhvort samþykkt sjálfgefna hólfið sem er fyllt út eða, ef varan hefur ekki verið notuð fyrr í vöruhúsinu, fylla út hólfið þar sem á að ganga frá vörunni. Síðan þarf að fylla út vörumagnið sem þú móttekur og bóka innhreyfinguna.  

## <a name="receive-items-with-a-purchase-order"></a>Taka á móti vörum með innkaupapöntun

Eftirfarandi lýsir því hvernig skal taka á móti vörum með innkaupapöntun. Skrefin eru svipuð fyrir söluvöruskilapantanir og millifærslupantanir.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir**, velja síðan viðkomandi tengil.
2. Opna innkaupapöntun sem þegar er til eða stofna nýja. Frekari upplýsingar eru á [Skrá innkaup](purchasing-how-record-purchases.md).
3. Í reitnum **Magn til móttöku** er fært inn magnið sem hefur verið móttekið.

   > [!NOTE]
   > Ef móttekið magn er hærra en pantað er á innkaupapöntuninni, samkvæmt reitnum **Magn**, og lánardrottinn hefur verið settur upp til að leyfa umframmóttökur, þá er reiturinn **Umframmóttaka** notaður til að meðhöndla umframmagn. Frekari upplýsingar er að finna í hlutanum [Taka á móti fleiri vörum en pantað er](warehouse-how-receive-items.md#receive-more-items-than-ordered).
4. Valið er **Bóka** aðgerðin.

  Gildið í reitnum **Móttekið magn** er uppfært. Ef um er að ræða móttöku að hluta, getur þetta magn verið lægra en gildið í svæðinu **Magn**.

> [!NOTE]
> Ef vöruhúsaskjal er notað til að bóka móttökuna er ekki hægt að nota aðgerðina **Bóka** á innkaupapöntuninni. Í staðinn hefur starfsmaður vöruhúss þegar bókað magn innkaupapöntunar sem móttekið. Frekari upplýsingar eru í [Vörur mótteknar með vöruhúsamóttöku](warehouse-how-receive-items.md#receive-items-with-a-warehouse-receipt).

## <a name="receive-items-with-a-warehouse-receipt"></a>Taka á móti vörum með vöruhúsamóttöku

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur**, velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  

    Fyllt er út í reitina á flýtiflipanum **Almennt**. Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.  

    Fyrir grunngerð vöruhúss með beinan frágangur og tínsla ef birgðageymslan er með sjálfgefið svæði og hólf fyrir móttökur eru reitirnir **Svæðiskóði** og **Hólfakóði** fylltir út sjálfkrafa en hægt er að breyta þeim eftir þörfum.  

    > [!NOTE]  
    > Ef taka á á móti vörum með öðrum vöruhúsaflokkskótum en flokkskóta hólfsins í reitnum **Hólfkóti** í fylgiskjalshausnum verður að eyða innihaldi reitsins **Hólfkóti** í hausnum áður en upprunaskjalslínurnar eru sóttar fyrir vörurnar.  
3. Valið er **Sækja upprunaskjöl** aðgerð. Síðan **Upprunaskjöl** opnast.

    Í nýrri eða opinni vöruhúsamóttöku er hægt að nota síðuna **Afmörkun til að sækja upprunaskjal** til að sækja þær línur útgefna upprunaskjalsins sem segja til um hvaða vörur á að taka við eða afhenda.

    1. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.  
    3. Skilgreina hvaða gerð af upprunaskjalslínum eigi að sækja með því að fylla út viðeigandi afmörkunarreiti.  
    4. Veljið **Keyra**.  

    Allar útgefnar upprunaskjalslínur sem uppfylla síuskilyrðið eru nú settar inn á síðunni **Vöruhússmóttaka** þar sem síunaraðgerðin var virkjuð. 

    Skilgreindar afmörkunarsamsetningar eru vistaðar á síðunni **Afmarkanir til að sækja upprunaskjöl** þar til þeirra er næst þörf. Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

4. Veldu upprunaskjölin þar sem þú vilt móttaka vörur, veldu síðan **Í lagi**.  

    Upprunaskjalslínurnar birtast á síðunni **Vöruhúsamóttaka**. Reiturinn **Magn til móttöku** hefur verið fylltur út með eftirstöðvum hverrar línu en hægt er að breyta magninu eftir þörfum. Ef gildinu í reitnum  **Hólfkóti** er eytt á flýtiflipanum **Almennt** áður en línurnar eru sóttar þarf að færa inn viðkomandi hólfkóta í hverri móttökulínu.  

    > [!NOTE]  
    >  Til að fylla út í allar línurnar í reitnum **Magn til móttöku** með núlli skal velja aðgerðina **Eyða magni til móttöku**. Til að fylla reitinn aftur með eftirstöðvum er valið **Færa sjálfkr. inn magn til móttöku** aðgerðin.  
    >
    >  Ekki er hægt að taka á móti fleiri vörum en talan í reitnum **Magn eftirstöðva** á upprunaskjalslínunni segir til um. Til að taka á móti fleiri vörum skal sækja annað upprunaskjal sem inniheldur línu fyrir vöruna með því að nota síuvirknina.  

5. Bóka vöruhúsamóttökuna. Magnreitirnir eru uppfærðir í upprunaskjölunum og vörurnar eru skráðar sem hluti fyrirtækisbirgða.  

Ef vöruhúsafrágangur er notaður sendir kerfið móttökulínurnar í vöruhúsafrágangsaðgerðina. Þótt vörurnar hafi verið mótteknar er ekki hægt að tína þær fyrr en gengið hefur verið frá þeim. Mótteknu vörurnar eru ekki greindar sem tiltækar birgðir fyrr en frágangurinn hefur verið skráður.  

Ef vöruhúsafrágangur er ekki notaður, en hólf, skráir kerfið frágang varanna í hólfinu sem er tilgreint í upprunaskjalslínunni.  

> [!NOTE]  
> Ef aðgerðin **Bóka og prenta**, er notuð er móttakan bókuð ásamt því að frágangsleiðbeiningar sem sýna hvaða vörur á að setja í geymslu eru prentaðar.  
>
> Ef staðsetningin notar beinan frágang og tínslu notar kerfið frágangssniðmátin til að reikna út besta staðinn til að ganga frá vörunum. Þetta er síðan prentað í frágangsfyrirmælunum.

## <a name="receive-more-items-than-ordered"></a>Taka á móti fleiri vörum en pantað er

Þegar þú tekur á móti fleiri vörum en þú pantaðir, viltu hugsanlega fá þær afhentar í stað þess að hætta við kvittunina. Til dæmis getur verið ódýrara að halda eftir umframbirgðum en að skila þeim eða seljandi kann að bjóða þér afslátt fyrir að halda þeim.

### <a name="set-up-over-receipts"></a>Setja upp umframmóttöku

Skilgreina verður prósentu sem leyfilegt er að fara umfram pantað magn við móttöku. Þetta er skilgreint með kóða umframmóttöku, sem inniheldur prósentuna í reitnum **Vikmarkaprósenta umframmóttöku**. Síðan er hægt að úthluta kóðanum á spjöld viðkomandi vara og/eða lánardrottna.  

Eftirfarandi lýsir því hvernig skal setja upp og úthluta kóða umframmóttöku á vöru. Skrefin eru svipuð til að setja þetta upp fyrir lánardrottin.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Opna skal birgðaspjald fyrir vöru sem talið er að sé stundum afhent með hærra magni en pantað er.
3. Veldu **Uppfletting** í reitnum **Kóði umframmóttöku**.
4. Valið er aðgerðin **Nýtt**.
5. Á síðunni **Kóðar umframmóttöku** skal stofna eina eða fleiri línur sem skilgreina mismunandi reglur umframmóttöku. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Veldu línu og svo **Í lagi**.

Kóði umframmóttöku er úthlutaður á vöruna. Allar innkaupapantanir eða vöruhúsamóttökur á vörunni leyfa nú móttöku á meira en pöntuðu magni samkvæmt uppgefinni vikmarkaprósentu umframmóttöku.

> [!NOTE]
> Hægt er að setja upp samþykktarverkflæði til að krefjast þess að umframmóttökur verði samþykktar áður en unnið er með þær. Í slíku tilfelli þarf að velja gátreitinn **Samþykktar krafist** á síðunni **Kóðar umframmóttöku**. Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).

### <a name="perform-an-over-receipt"></a>Framkvæma umframmóttöku

Í innkaupalínum og vöruhúsamóttökulínum er reiturinn **Magn umframmóttöku** notaður til að skrá magn umframmóttöku, sem þýðir magn sem fer umfram gildið fyrir pantað magn í reitnum **Magn**.

Þegar unnið er úr umframmóttöku er hægt að hækka gildið í reitnum **Magn til móttöku** upp í móttekið raunmagn. Reiturinn **Magn umframmóttöku** er þá uppfærður til að sýna umframmagnið. Önnur leið er að færa inn umframmagnið í reitinn **Magn umframmóttöku**. Reiturinn **Magn til móttöku** er þá uppfærður til að sýna pantað magn ásamt umframmagni. Eftirfarandi ferli útskýrir hvernig á að fylla út reitinn **Magn til móttöku**.  

1. Í innkaupapöntun eða fylgiskjali vöruhúsamóttöku, þar sem móttekið magn er hærra en pantað magn, skal færa inn raunverulegt móttekið magn í reitinn **Magn til móttöku**.

    Ef aukningin er innan vikmarka sem tilgreind eru af úthlutuðum kóða umframmóttöku verður reiturinn **Magn umframmóttöku** uppfærður til að sýna magnið sem gildið í reitnum **Magn** eykst um.

    Ef aukningin er meiri en sem nemur tilgreindum vikmörkum verður umframmóttaka ekki leyfð. Í slíkum tilfellum er hægt að kanna hvort til sé annar kóði umframmóttöku sem leyfir hana. Annars er aðeins hægt að taka á móti pöntuðu magni og afgreiða þarf umframmagnið á annan hátt, t.d. með því að skila því til lánardrottins.

2. Bókið kvittunina eins og aðrar kvittanir.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] felur ekki í sér virkni til að ræsa sjálfkrafa fjármálastjórnun á umframmóttökum. Þetta þarf að vinna handvirkt í samkomulagi við lánardrottin, til dæmis getur lánardrottinn framsent nýjan eða uppfærðan reikning.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
