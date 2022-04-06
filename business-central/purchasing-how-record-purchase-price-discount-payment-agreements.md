---
title: Skrá sérstakt söluverð og sérstaka afslætti
description: Þú getur skilgreint mismunandi varaverð og afsláttarsamninga og úthlutað þeim til innkaupaskjala fyrir lánardrottna.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 85445267dac39103ed9851604182f09cc9819ea0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522669"
---
# <a name="record-special-purchase-prices-and-discounts"></a>Skrá sérstakt söluverð og sérstaka afslætti
> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út einfaldaðri ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður sem ert að nota þessa útgáfu þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Skilgreina verður mismunandi verð- og afsláttarsamninga sem gilda þegar vörur eru keyptar frá mismunandi lánardrottnum svo að þeim reglum og gildum sem samkomulag hefur náðst um sé beitt á innkaupaskjöl sem gerð eru fyrir lánardrottininn.

Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[prod_short](includes/prod_short.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur. Frekari upplýsingar er að finna í [Útreikningur besta verðs](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

Hvað varðar verð, er hægt að hafa sérstakt söluverð í sölulínunum ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða upphafs-/ lokadagsetningu er til staðar.

Hvað varðar afslátt, er hægt að setja upp og nota tvær tegundir innkaupaafsláttar:

| Afsláttargerð | Lýsing |
| --- | --- |
| **Innkaupalínuafsláttur** |Afsláttarupphæð sem er sett inn í sölulínur ef tiltekin samsetning á lánardrottni, vöru, lágmarksmagni, mælieiningu, eða upphafs-/ lokadagsetningu er til staðar. Þetta virkar á sama háttog fyrir innkaupsverð. |
| **Reikningsafsláttur** |Hlutfallsafsláttur sem er dreginn frá heildarupphæð skjalsins ef upphæðin í öllum línum í söluskjali fer fram yfir ákveðið lágmark. |

Vegna þess að innkaupalínuafslættir og innkaupaverð byggjast á samsetningu vöru og lánardrottins er einnig hægt að færa þessa grunnstillingu inn af birgðaspjaldinu, þar sem reglurnar og gildin eru skilgreind. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Að setja upp sérstakt innkaupsverð fyrir lánardrottin

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Opna skal viðeigandi lánardrottnaspjald og velja síðan aðgerðina **Verð**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyllt er út lína fyrir hverja samsetningu sem lánardrottinn veitir innkaupalínuafsláttur fyrir.

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience)  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Veldu lánardrottin og veldu svo aðgerðina **Söluverðlistar**. 
3. Veljið **Nýtt** til að stofna nýja innkaupaverðlista.
4. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt** og **Skattur**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Til að bæta vörum við listann skal gera eitt af eftirfarandi:
   * Til að bæta við mörgum vörum skal velja **Leggja til línur** og síðan færa inn síuskilyrði til að tilgreina gerðir af vörum sem bæta á við. Einnig er hægt að færa inn nokkrar aðrar stillingar fyrir vörurnar sem eru tilgreindar sérstaklega í verðlistanum. Þú getur breytt þessu síðar ef þörf er á.
   * Til að afrita vörur úr öðrum verðlista skal velja **Afrita línur** og síðan velja verðlistann sem á að afrita.
   * Til að bæta vörum við handvirkt skal í hnitanetinu í reitnum **Gerð afurðar** velja gerð afurðar sem verðlistinn er fyrir. Fyllið inn í eftirstandandi reiti eftir þörfum, eftir vali. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Til að byrja að nota verðlistann skal í reitnum **Staða** velja **Virkur**.

---

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Að setja upp línuafslátt fyrir lánardrottin
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Opna skal viðeigandi lánardrottinsspjald og veljið síðan aðgerðina **Línuafslættir**.

    Reiturinn **Tegund innkaupa** er fylltur út fyrirfram með **Lánardrottinn** og í reitnum **Innkaupakóði** er númer lánardrottins.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyllt er út lína fyrir hverja samsetningu sem lánardrottinn veitir innkaupalínuafsláttur fyrir.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Að setja upp reikningsafslátt fyrir lánardrottin
Þegar lánardrottnar þínir hafa veitt þér upplýsingar um hvaða reikningsafslætti þeir veita eru færðir inn reikningsafsláttarkóðar á lánardrottnaspjöldin og sett upp skilyrði fyrir hvern kóða.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Opna skal spjald lánardrottins sem getur veitt reikningsafslátt.
3. Í reitnum **Reikningsafsláttarkóði** er valinn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir lánardrottin.

    > [!NOTE]  
    >   Fyrirliggjandi lánardrottnaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til lánardrottna með því að velja nafn annars lánardrottins sem hefur sömu skilmála.

    Næsta skref er að setja upp nýja skilmála fyrir reikningsafslátt.
4. Á síðunni **Lánardrottnaspjald** skal velja aðgerðina **Nota sniðmát**. Síðan **Reikningsafsláttur lánardr.** opnast.
5. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilyrði í ISK.
6. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
7. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
8. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem lánardrottinn mun fá mismunandi reikningsafslátt í.

Reikningsafsláttur er nú settur upp og úthlutað á umræddan lánardrottin. Þegar valinn er lánardrottinskóði í reitnum **Kóði reikningsafsláttar** á öðrum lánardrottnaspjöldum er sama reikningsafslætti úthlutað þeim lánardrottini.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Regla valin fyrir bókun á innkaupaafslætti:  
Þegar innkaupareikningur er bókaður sem hefur að geyma eina eða fleiri tegundir afsláttar er hægt að velja á milli tveggja reglna til að bóka afsláttarupphæðir. Hægt er að bóka afslátt sérstaklega eða hægt er að draga afslátt frá reikningsafslætti.  

Áður en hægt er að gera þetta verður að vera búið að setja upp nauðsynlega reikninga til að bóka afsláttarupphæðir í bókhaldslyklinum. Einnig verður að gæta þess að rétt reikningsnúmer hafi verið sett í almennu bókunaruppsetninguna í reitunum **Afsláttarreikningur Innkaupalínu** og **Afsláttarreikningur Innkaupabirgða**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slá inn **Uppsetning innkaupa og viðskiptaskulda** og velja svo viðeigandi tengil.
2. Í reitnum **Afsláttarbókun** er valin ein af eftirfarandi reglum fyrir bókun afsláttar.

|**Afsláttarbókunarregla**|**Reikningsafsláttur**|**Línuafsláttur**|  
|------------------------------------|--------------------------|-----------------------|  
|**Allur afsláttur**|Bókað sérstaklega|Bókað sérstaklega|  
|**Reikningsafsláttur**|Bókað sérstaklega|Dregið frá|  
|**Línuafslættir**|Dregið frá|Bókað sérstaklega|  
|**Enginn afsláttur**|Dregið frá|Dregið frá|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Afslættir Innkaupareiknings og Þjónustugjöld
Hafi skilyrði fyrir reikningsafslátt fyrir lánardrottna verið ákveðinn er hægt að færa þau inn. Þá verður afslátturinn reiknaður út þegar innkaupareikningur er fylltur út.  

 Áður en hægt er að nota reikningsafslátt í innkaupum verður að tilgreina hjá hvaða lánardrottnum er hægt að fá afslátt.  

 Afsláttarprósentur eru tengdar við ákveðnar reikningsupphæðir á síðunni **Reikn.afsl. lánardr.**. Hægt er að færa inn hvaða prósentutölu sem er inn á hverja síðu. Hver lánardrottinn getur haft sína eigin síðu, eða hægt er að tengja nokkra lánardrottna saman á síðu.  

 Til viðbótar við afsláttarprósentu er hægt að tengja ákveðið þjónustugjald við ákveðna reikningsupphæð.  

 Skilmála um reikningsafslátt innlendra lánardrottna má tilgreina í SGM og í erlendum gjaldmiðli hjá erlendum lánardrottnum.  

 Hægt er að láta [!INCLUDE[prod_short](includes/prod_short.md)] reikna sjálfkrafa út reikningsafslátt fyrir beiðnir, standandi pantanir, pantanir, reikninga eða kreditreikninga.  

> [!TIP]  
>  Áður en hafist er handa við að setja upplýsingarnar inn í forritið er gott að útbúa uppkast af því afsláttarformi sem á að nota. Þetta gerir auðveldara að átta sig á því hvaða lánardrottna er hægt að tengja við sama reikningsafsláttarsíðu. Eftir því sem setja þarf upp færri síður er þeim mun fljótlegra að færa inn grunnupplýsingarnar.

## <a name="best-price-calculation"></a>Útreikningur besta verðs
Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[prod_short](includes/prod_short.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur.

Besta verð er lægsta leyfilega verð með hæsta leyfilega línuafslættinum þennan tiltekna dag. [!INCLUDE[prod_short](includes/prod_short.md)] reiknar þetta sjálfkrafa þegar það setur einingarverð og línuafsláttarprósentuna fyrir vörur í nýja skjalinu og í færslubókarlínum.

> [!NOTE]  
>   Eftirfarandi lýsir því hvernig besta verð er reiknað fyrir sölu. Útreikningurinn er sá sami fyrir innkaup.

1. [!INCLUDE[prod_short](includes/prod_short.md)]kannar samsetningu reikningsfærslu á viðskiptamann og vöru og velur svo rétt viðeigandi verð og afslátt samkvæmt eftirfarandi skilyrðum:

    - Er þessi viðskiptamaður með sérstakan samning um verð eða línuafslætti, eða tilheyrir viðskiptamaðurinn hóp með slíkan samning?
    - Fellur varan eða vöruafsláttarflokkurinn á línunni undir þessa samninga?
    - Er pöntunardagsetningin (eða bókunardagsetning reikningsins og kreditreikningsins) á milli upphafs- og lokadagsetningar verðs/línuafsláttar?
    - Er mælieiningarkóti tilgreindur? Ef svo er leitar [!INCLUDE[prod_short](includes/prod_short.md)] að verði/línuafslætti með sama mælieiningarkóða og verði/afslætti án mælieiningarkóða.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kannar hvort einhverjir samningar um verð/afslátt í eiga við um skjalið eða færslubókarlínuna og bætir svo við viðeigandi einingaverði og prósentu línuafsláttar samkvæmt eftirfarandi skilyrðum:

    - Er krafa um lágmarksmagn til staðar í samningi um verð/afslátt sem er uppfyllt?
    - Er krafa um gjaldmiðil til staðar í samningi um verð/afslátt sem er uppfyllt? Ef svo er, er lægsta verðið og hæsti línuafsláttur fyrir þann gjaldmiðil bætt við, jafnvel þótt SGM myndi veita betra verð. Ef ekkert verð/línuafsláttur er til í tilgreindum gjaldmiðilskóða, setur [!INCLUDE[prod_short](includes/prod_short.md)] inn lægsta verðið og hæsta línuafsláttinn í SGM.

Ef ekkert verð finnst fyrir vörurnar á línunni er síðasta innkaupsverð eða einingaverð sótt af birgðaspjaldinu eða birgðahaldseiningarspjaldinu.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/set-up-prices-discounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]