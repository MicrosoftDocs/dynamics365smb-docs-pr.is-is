---
title: Móttaka vara
description: Þessi grein er yfirlit yfir mismunandi leiðir til að taka á móti vörum í vöruhúsi, til dæmis vörur með innkaupapöntun eða vörur með vöruhúsamóttöku.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 8bd79a13bb7ecc806fea0dcdea33ec604bd98c41
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460887"
---
# <a name="receive-items"></a>Móttaka vara

Þegar vörur berast í vöruhús sem er ekki sett upp fyrir vinnslu vöruhúsamóttöku þarf einfaldlega að skrá móttökuna á viðeigandi viðskiptaskjal, eins og t.d. innkaupapöntun, sölvöruskilapöntun, eða millifærslupöntun á innleið.

Þegar vörur berast í vöruhús sem er sett upp fyrir vinnslu vöruhúsamóttöku þarf að sækja línur útgefna upprunaskjalsins sem hrintu móttöku þeirra af stað. Ef hólf eru hólfin er annað hvort hægt að samþykkja sjálfgefna hólfið sem er útfyllt eða ef varan hefur aldrei áður verið móttekin í vöruhúsinu, fyllt út í hólfið þar sem ganga á frá vörunni. Þá þarf að fylla út magn varanna sem hafa verið mótteknar og bóka móttökunina.  

## <a name="receive-items-with-a-purchase-order"></a>Taka við vörum með innkaupapöntun

Eftirfarandi lýsir því hvernig skal taka á móti vörum með innkaupapöntun. Skrefin eru svipuð fyrir þá sem eru í sölu vöruskilapöntunum og flutningspantanir.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **innkaupapantanir** og veljið síðan tengda tengilinn.
2. Opna innkaupapöntun sem þegar er til eða stofna nýja. Frekari upplýsingar við [skráningu innkaupa](purchasing-how-record-purchases.md).
3. Í reitnum **Magn til móttöku** er fært inn magnið sem hefur verið móttekið.

   > [!NOTE]
   > Ef móttekið magn er hærra en pantað er á innkaupapöntuninni, samkvæmt reitnum **Magn**, og lánardrottinn hefur verið settur upp til að leyfa umframmóttökur, þá er reiturinn **Umframmóttaka** notaður til að meðhöndla umframmagn. Frekari upplýsingar eru [í til að taka á móti fleiri atriðum en pöntuðum](warehouse-how-receive-items.md#receive-more-items-than-ordered) kafla.
4. Valið er **Bóka** aðgerðin.

  Gildið í reitnum **Móttekið magn** er uppfært. Ef um er að ræða móttöku að hluta, getur þetta magn verið lægra en gildið í svæðinu **Magn**.

> [!NOTE]
> Ef vöruhúsaskjal er notað til að bóka móttökuna er ekki hægt að nota aðgerðina **Bóka** á innkaupapöntuninni. Í staðinn hefur starfsmaður vöruhúss þegar bókað magn innkaupapöntunar sem móttekið. [Frekari upplýsingar til að taka á móti vörum við vöruhúsamóttöku](warehouse-how-receive-items.md#receive-items-with-a-warehouse-receipt).

## <a name="receive-items-with-a-warehouse-receipt"></a>Taka við vörum með vöruhúsamóttöku

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **vöruhúsamóttökur** og velja síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.  

    Reitirnir á flipanum Almennt **eru** fylltir út. Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.  

    Fyrir grunngerð vöruhúss með beinan frágangur og tínsla ef birgðageymslan er með sjálfgefið svæði og hólf fyrir móttökur eru reitirnir **Svæðiskóði** og **Hólfakóði** fylltir út sjálfkrafa en hægt er að breyta þeim eftir þörfum.  

    > [!NOTE]  
    > Ef taka á á móti vörum með öðrum vöruhúsaflokkskótum en flokkskóta hólfsins í reitnum **Hólfkóti** í fylgiskjalshausnum verður að eyða innihaldi reitsins **Hólfkóti** í hausnum áður en upprunaskjalslínurnar eru sóttar fyrir vörurnar.  
3. Valið er **Sækja upprunaskjöl** aðgerð. Síðan **Upprunaskjöl** opnast.

    Í nýrri eða opinni vöruhúsamóttöku er hægt að nota **afmarkanirnar til að sækja upprunaskjöl.** -síðu til að sækja útgefnar upprunaskjalslínur sem skilgreina hvaða vörur á að taka á móti eða senda.

    1. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    2. Ef setja á upp nýja síu er lýsandi kóti færður inn í **reitinn Kóti** og síðan er aðgerðin breyta **valin**.  
    3. Skilgreinið gerð upprunaskjallínanna sem á að sækja með því að fylla út í viðeigandi afmörkunarreiti.  
    4. Veljið **Keyra**.  

    Allar útgefnar upprunaskjalslínur sem uppfylla skilyrði afmörkunar eru nú settar inn á **síðuna vöruhúsamóttaka** þar sem síuaðgerðin var virkjuð. 

    Afmörkunarsamsetningar sem skilgreindar eru eru vistaðar á **afmörkunum til að sækja Upprunadoktora.** síða þar til næst þegar þörf er á henni. Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

4. Velja skal upprunaskjölin sem á að taka á móti vörunum og velja **síðan í lagi**.  

    Upprunaskjalslínurnar birtast á **síðunni vöruhúsamóttaka**. Reiturinn **Magn til móttöku** hefur verið fylltur út með eftirstöðvum hverrar línu en hægt er að breyta magninu eftir þörfum. Ef gildinu í reitnum  **Hólfkóti** er eytt á flýtiflipanum **Almennt** áður en línurnar eru sóttar þarf að færa inn viðkomandi hólfkóta í hverri móttökulínu.  

    > [!NOTE]  
    >  Til að fylla út allar línur í **reitnum Magn til móttöku** með núlli er valið **Eyða magni til að taka** við aðgerðinni. Til að fylla reitinn aftur með eftirstöðvum er valið **Færa sjálfkr. inn magn til móttöku** aðgerðin.  
    >
    >  Ekki er hægt að taka á móti fleiri vörum en talan í reitnum **Magn eftirstöðva** á upprunaskjalslínunni segir til um. Til að taka við fleiri vörum er sótt annað upprunaskjal sem inniheldur línu fyrir vöruna með því að nota síuaðgerðina.  

5. Bóka vöruhúsamóttökuna. Reitirnir Magn eru uppfærðir á upprunaskjölunum og eru vörurnar skráðar sem hluti af birgðum fyrirtækisins.  

Ef vöruhúsafrágangur er notaður eru móttökulínurnar sendar í frágangsaðgerðina vöruhúsafrágangur. Þær vörur, sem þó berast, er ekki hægt að tína fyrr en búið er að ganga frá þeim. Mótteknu vörurnar eru ekki greindar sem tiltækar birgðir fyrr en frágangurinn hefur verið skráður.  

Ef vöruhúsafrágangur er ekki notaður, en hólf eru frágangsatriðin í hólfinu sem tilgreind eru í upprunaskjalslínunni skráð.  

> [!NOTE]  
> Ef aðgerðin **Bóka og prenta**, er notuð er móttakan bókuð ásamt því að frágangsleiðbeiningar sem sýna hvaða vörur á að setja í geymslu eru prentaðar.  
>
> Ef staðsetningin notar beinan frágang og tínslu notar kerfið frágangssniðmátin til að reikna út besta staðinn til að ganga frá vörunum. Þetta er síðan prentað í frágangsfyrirmælunum.

## <a name="receive-more-items-than-ordered"></a>Tekið við fleiri atriðum en pantað

Þegar þú tekur á móti fleiri vörum en þú pantaðir, viltu hugsanlega fá þær afhentar í stað þess að hætta við kvittunina. Til dæmis getur verið ódýrara að halda eftir umframbirgðum en að skila þeim eða seljandi kann að bjóða þér afslátt fyrir að halda þeim.

### <a name="set-up-over-receipts"></a>Setja upp yfir-móttökur

Skilgreina verður prósentu sem leyfilegt er að fara umfram pantað magn við móttöku. Þetta er skilgreint með ómóttökukóta sem er prósenta í **svæðinu yfir-Kvittunarvikmörk**. Síðan er hægt að úthluta kóðanum á spjöld viðkomandi vara og/eða lánardrottna.  

Eftirfarandi lýsir því hvernig skal setja upp og úthluta kóða umframmóttöku á vöru. Skrefin eru svipuð og að setja þetta upp fyrir lánardrottinn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **atriði** og veljið síðan tengda tengilinn.
2. Opnaðu kortið fyrir vöru sem þig grunar að gæti stundum skilað með hærra magni en pantað var.
3. Veljið **uppflettingu** í **reitnum yfir-móttökukóti**.
4. Valið er aðgerðin **Nýtt**.
5. Á síðunni **Kóðar umframmóttöku** skal stofna eina eða fleiri línur sem skilgreina mismunandi reglur umframmóttöku. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Veldu línu og veldu **síðan í lagi**.

Kóði umframmóttöku er úthlutaður á vöruna. Allar innkaupapantanir eða vöruhúsamóttökur á vörunni leyfa nú móttöku á meira en pöntuðu magni samkvæmt uppgefinni vikmarkaprósentu umframmóttöku.

> [!NOTE]
> Hægt er að setja upp samþykktarverkflæði sem krefjast þess að fleiri móttökur séu samþykktar áður en hægt er að afgreiða þær. Í slíku tilfelli þarf að velja gátreitinn **Samþykktar krafist** á síðunni **Kóðar umframmóttöku**. Frekari upplýsingar um [Stofna verkflæði](across-how-to-create-workflows.md).

### <a name="perform-an-over-receipt"></a>Framkvæma framkvittun

Í innkaupalínur og móttökulínum **innkaupa er reiturinn yfir-Móttaka magn** notaður til að skrá magn sem móttekið er, sem þýðir magn, umfram magn pöntuðu af magni í **reitnum Magn**.

Þegar afgreitt er á milli kvittunar er hægt að auka gildið í **reitnum Magn til móttöku** í móttekið magn. Reiturinn **Magn umframmóttöku** er þá uppfærður til að sýna umframmagnið. Önnur leið er að færa inn umframmagnið í reitinn **Magn umframmóttöku**. Reiturinn **Magn til móttöku** er þá uppfærður til að sýna pantað magn ásamt umframmagni. Eftirfarandi ferli útskýrir hvernig á að fylla út reitinn **Magn til móttöku**.  

1. Í innkaupapöntun eða vöruhúsamóttöku þar sem móttekið magn er hærra en pantað er fært inn magnið sem í raun fékkst í **reitnum Magn til móttöku**.

    Ef Hækkunin er innan vikmarka sem tilgreind eru í úthlutuðu magni yfir-kvittunarkóta **er svæðið yfir-innhreyfinga magn** uppfært til að sýna magnið með því að fara yfir gildið í **reitnum Magn**.

    Ef aukningin er meiri en sem nemur tilgreindum vikmörkum verður umframmóttaka ekki leyfð. Í slíkum tilfellum er hægt að kanna hvort til sé annar kóði umframmóttöku sem leyfir hana. Annars er aðeins hægt að taka á móti pöntuðu magni og þarf umframmagnið að fara aðra leið, eins og að skila því til lánardrottins.

2. Bókið kvittunina eins og aðrar kvittanir.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] felur ekki í sér virkni til að ræsa sjálfkrafa fjármálastjórnun á umframmóttökum. Þetta þarf að vinna handvirkt í samkomulagi við lánardrottin, til dæmis getur lánardrottinn framsent nýjan eða uppfærðan reikning.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
