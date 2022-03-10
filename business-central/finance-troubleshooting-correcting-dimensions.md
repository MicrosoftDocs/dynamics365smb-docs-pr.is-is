---
title: Úrræðaleit og víddarleiðrétting
description: Kynntu þér hvernig á að lagfæra dæmigerðar víddarvillur og hvernig á að leiðrétta víddir eftir að þær eru notaðar í bókuðum færslum.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension, correction, correct, business intelligence
ms.search.form: 116, 540, 2588
ms.date: 09/27/2021
ms.author: bholtorf
ms.openlocfilehash: 91dce6ef4fee44800ab5892a986783139eeed892
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146463"
---
# <a name="troubleshooting-and-correcting-dimensions"></a>Úrræðaleit og víddarleiðrétting

Fjárhagsskýrslugerð og greiningaryfirlit reiða sig oft á gögn úr ýmsum víddum. Þrátt fyrir þær öryggisráðstafanir sem í boði eru gerast stundum mistök sem geta leitt til ónákvæmni. Í þessu efni er lýst nokkrum dæmigerðum villum og útskýrt hvernig eigi að leiðrétta víddarúthlutanir á bókuðum færslum svo að fjárhagsskýrslur séu réttar.

## <a name="troubleshooting-dimensions-errors"></a>Úrræðaleita víddarvillur

Þegar skjala- eða færslubókarlínur sem innihalda víddir eru bókaðar geta ýmsar villur komið upp sem venjulega tengjast rangri víddaruppsetningu eða úthlutun.

> [!NOTE]
> Í eftirfarandi lista yfir hugsanleg villuboð eru kóðarnir *%X* staðgenglar fyrir gagnabreyturnar sem raunverulegu skilaboðin munu innihalda í notendaviðmótinu, háð samhenginu. Til dæmis *%1 %2 er útilokað.* gæti birst í notendaviðmótinu sem „Víddarkóðinn SVÆÐI er útilokaður.“.  

|Gefa út|Villuboð|Möguleg lausn|
|-----|-------------|-----------------|
|Útilokuð vídd|%1 %2 er útilokað.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokuðu víddinni og afblokka hana.<br />-Fjarlægja línu víddasamstæðu fyrir útilokuðu víddina.|
|Eydd vídd|%1 %2 finnst ekki.|-Endurheimta vídd sem vantar.<br />-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með vídd sem vantar og bæta henni við.<br />-Fjarlægja línu víddasamstæðu fyrir vídd sem vantar.|
|Útilokað víddargildi|%1 %2 - %3 er útilokað.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokuðu víddargildi og afblokka það.<br />-Fjarlægja línu víddasamstæðu fyrir útilokaða víddargildið.|
|Eydd víddargildi|    %1 fyrir %2 vantar.|-Endurheimta víddargildi sem vantar.<br />-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með víddargildinu sem vantar og bæta því við.<br />-Fjarlægja línu víddasamstæðu fyrir víddargildið sem vantar.|
|Óheimilt víddargildi|Gerð víddargildis fyrir %1 %2 – %3 má ekki vera %4.|-Breyttu reitnum **Gerð víddargildis** á síðunni **Víddargildi** í **Staðlað** eða **Frá-tala**.<br />-Fjarlægja línu víddasamstæðu fyrir útilokaða víddargildið.|
|Útilokuð víddarsamsetning|Víddirnar %1 og %2 er ekki hægt að nota samtímis.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokuðu víddarsamsetningunni og afblokka hana.<br />-Breyta einni af línum heimildasamstæðu sem stangast á fyrir víddarsamsetninguna.|
|Útilokuð samsetning víddargildis|Víddarsamsetningarnar %1 - %2 og %3 - %4 er ekki hægt að nota samtímis.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokaða víddargildissamsetningu og opnaðu fyrir hana.<br />-Breyta einni af línum heimildasamstæðu sem stangast á fyrir víddargildissamsetninguna.|
|Auður víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Kóði tilskilinn**|-Velja %1 fyrir %2 %3.<br />-Velja %1 fyrir %2 %3 fyrir %4 %5.|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn víddargildi sem er ekki autt fyrir víddina sem stangast á í víddasamstæðunni.|
|Rangur víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Sami kóði**|-Veldu %1 %2 fyrir %3 %4.<br />-Veldu %1 %2 fyrir %3 %4 fyrir %5 %6|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn nauðsynlegt víddargildi fyrir víddina sem stangast á í víddasamstæðunni.|
|Víddargildiskóði sem ekki er auður fyrir auða sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Sami kóði**|-%1 %2 verður að vera auður.<br />-%1 %2 verður að vera auður fyrir %3 %4.|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn auðan víddargildiskóða fyrir víddina sem stangast á í víddasamstæðunni.|
|Óvæntur víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Enginn kóði**|-%1 %2 má ekki nefna.<br />-%1 %2 má ekki nefna fyrir %3 %4|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Fjarlægja línuna sem stangast á úr víddasamstæðunni.|
|Víddarleiðrétting klárast ekki á réttan hátt.||-Veljið **Endurstilla** til að snúa leiðréttingunni aftur í drög. Þetta núllstillir breytingarnar og hægt er að keyra leiðréttingu aftur.|

## <a name="changing-dimension-assignments-after-posting"></a>Breyta víddarúthlutunum eftir bókun

Ef kemur í ljós að röng vídd hafi verið notuð í bókuðum fjárhagsfærslum er hægt að leiðrétta víddargildin og uppfæra greiningaryfirlitið. Það hjálpar til við að halda fjárhagsskýrslum og greiningum nákvæmum.

> [!IMPORTANT]
> Eiginleikar til að leiðrétta víddir eru einungis ætlaðir til að hjálpa við nákvæma fjárhagsskýrslugerð. Víddarleiðréttingar aðeins við um fjárhagsfærslurnar. Þær breyta ekki víddum sem eru úthlutaðar á færslur í öðrum fjárhag vegna sömu viðskipta. Misræmi verður á milli vídda sem eru úthlutaðar í fjárhag og undirfjárhag.

### <a name="setting-up-dimension-corrections"></a>Uppsetning víddarleiðréttinga

Tvö atriði þarf að hafa í huga þegar víddarleiðréttingar eru settar upp:

* Eru til víddir sem ekki á að leyfa fólki að breyta? Á síðunni **Stillingar víddarleiðréttingar** skal tilgreina víddirnar sem á að hindra breytingar á.
* Hver á að fá leyfi til að breyta víddum? Til að leyfa fólki að gera breytingar skal úthluta notendunum heimildinni **D365 DIM CORRECTION**. Heimildirnar gera þeim kleift að stofna víddarleiðréttingar, keyra þær og afturkalla ef þess gerist þörf. Þeir munu einnig geta tilgreint útilokaðar víddir. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a>Vídd leiðrétt

Hægt er að velja handvirkt eina eða fleiri fjárhagsfærslur eða nota síur til að velja safn af færslum. Ef þörf er á er einnig hægt að bæta við eða eyða víddum. 

1. Til að hefja víddarleiðréttingu skal nota eina af eftirfarandi síðum:

    * Á síðunni **Fjárhagur/skrá**, með því að velja skrá, og síðan velja aðgerðina **Leiðrétta víddir**. Þetta setur af stað leiðréttingu á færslunum í valdri skrá.
    * Á síðunni **Fjárhagsfærslur** með því að velja aðgerðina **Víddarleiðrétting**. 

2. Í reitinn **Lýsing** skal færa inn upplýsingar um breytingarnar. Aðrir gætu notað þessar upplýsingar síðar til að komast að því hvað var gert.
3. Í flýtiflipanum **Valdar fjárhagsfærslur** skal velja færslurnar sem eiga við.

    > [!IMPORTANT]
    > Þegar vali er breytt verða gildin í flýtiflipanum **Breytingar á víddarleiðréttingu** endurstillt. Því skal alltaf velja færslurnar áður en breytingar á víddargildi eru tilgreindar.

   Eftirfarandi tafla lýsir valkostunum.

   |Valkostur  |Description  |
   |---------|---------|
   |Allar tengdar færslur     |Bætið við fjárhagsfærslum sem er í sömu fjárhagsskránni.|   
   |Bæta við eftir síu     |Notið síuskilyrði þegar fjárhagsfærslum er bætt við.|
   |Handvirkt val     |Veljið ákveðnar fjárhagsfærslur.         |
   |Bæta við eftir víddum     |Síið fjárhagsfærslur eftir víddum.         |
   |Fjarlægja færslur     |Hættið við val á fjárhagsfærslum.         |
   |Stjórna valskilyrðum     |Fylgist með valferlinu og afturkallið val ef þess gerist þörf.         |

4. Í flýtiflipanum **Breytingar víddarleiðréttinga** skal velja víddina sem á að breyta í reitnum **Víddarkóði** og nýja gildið í reitnum **Nýr víddargildiskóði**.
5. Til að staðfesta leiðréttinguna skal velja **Staðfesta víddarbreytingar**. Frekari upplýsingar er að finna í [Víddarleiðréttingar staðfestar](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Veljið **Keyra**.

### <a name="validating-dimension-corrections"></a>Víddarleiðréttingar staðfestar

Áður en leiðrétting er keyrð er góð hugmynd að staðfesta hana fyrst. Staðfesting leitar að takmörkunum í virðisbókun fyrir fjárhagsreikninga, takmarkanir fyrir víddir og hvort víddargildin séu útilokuð. Meðan á staðfestingu stendur er staða leiðréttingar stillt á **Staðfesting í gangi**. Þegar leiðrétting er staðfest er útkoman sýnd í reitnum **Staða staðfestingar**. Ef villur fundust er hægt að nota aðgerðina **Skoða villur** til að kanna þær nánar. Þegar villa hefur verið lagfærð þarf að nota aðgerðina **Enduropna** til að keyra leiðréttinguna eða nýja staðfestingu.

Annaðhvort er hægt að keyra leiðréttingu strax eða tímasetja hana fram í tímann. Ef leiðréttingar eru gerðar á stóru gagnasafni er mælt með því að áætla keyrsluna utan vinnutíma. Frekari upplýsingar er að finna í [Víddarleiðréttingar á stórum gagnasöfnum](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a>Leiðrétting afturkölluð

Þegar vídd hefur verið leiðrétt og útkoman er ekki þér að skapi geturðu notað aðgerðina **Afturkalla** til að endurstilla fyrra gildið. Hins vegar er aðeins hægt að afturkalla nýjustu leiðréttinguna. Áður en leiðrétting er afturkölluð er hægt að staðfesta breytingarnar sem afturköllunin gerir. Þetta er til dæmis gagnlegt ef takmarkanir vídda hafa breyst eftir að leiðréttingin var gerð.

Ef afturköllunaraðgerðin er ekki í boði, t.d. vegna þess að margar breytingar hafa verið gerðar, er hægt að nota aðgerðina **Afrita í drög** til að hefja nýja leiðréttingu á sömu færslunum.

### <a name="dimension-corrections-on-large-data-sets"></a>Víddarleiðréttingar á stórum gagnasöfnum

Farið varlega þegar stór færslusöfn eru leiðrétt, t.d. söfn sem innihalda meira en 10.000 færslur. Ef það er hægt þá mælum við með að nota síur til að keyra leiðréttingar á smærri gagnasöfnum. Það er einnig góð hugmynd að keyra leiðréttingar utan venjulegs vinnutíma. 

### <a name="using-analysis-views-with-dimension-corrections"></a>Greiningaryfirlit og víddarleiðréttingar notaðar

Ef **Uppfæra við bókun** er virkjað fyrir greiningaryfirlit, getur [!INCLUDE[prod_short](includes/prod_short.md)] skoðað þegar skjöl og færslubækur eru bókaðar. Einnig er hægt að uppfæra yfirlit með þessari stillingu virkjaða með niðurstöður víddarleiðréttinga. Til að gera það skal kveikja á **Uppfæra greiningaryfirlit**. Uppfærsla greiningaryfirlita getir haft áhrif á afköst, sérstkaklega fyrir stór gagnasöfn, og því er mælt með að greiningaryfirlit séu aðeins uppfærð fyrir lítil gagnasöfn.  

### <a name="viewing-historical-dimension-corrections"></a>Ferill víddarleiðréttinga skoðaður

Ef fjárhagsfærsla hefur verið leiðrétt er hægt að kanna breytinguna með því að nota aðgerðina **Ferill víddarleiðréttinga**.

### <a name="handling-incomplete-corrections"></a>Afgreiðsla ólokinna leiðréttinga

Ef leiðrétting klárast ekki mun viðvörun birtast á leiðréttingarspjaldinu. Ef það gerist er hægt að nota aðgerðina **Endurstilla** til að snúa leiðréttingunni aftur í drög og afturkalla breytingarnar. Síðan er hægt að keyra leiðréttinguna aftur.

> [!NOTE]
> Endurstilling ólokinnar leiðréttingar hefur ekki áhrif á uppfærslur greiningaryfirlita vegna þess að þær gerast undir lok leiðréttingarferlisins.

### <a name="using-cost-accounting-with-corrected-gl-entries"></a>Kostnaðarbókhald með leiðréttum fjárhagsfærslum notað

Þegar búið er að leiðrétta víddir verða gögn kostnaðarbókhalds ósamstillt. Kostnaðarbókhald notar víddir til að safna saman upphæðum fyrir kostnaðarstaði og kostnaðarhluti og til að keyra kostnaðarúthlutanir. Að breyta víddum fyrir fjárhagsfærslur mun líklega þýða að þú endurkeyrir líkön kostnaðarbókhaldsins. Hvort sem þú þarft aðeins að eyða nokkrum kostnaðarskrám og endurkeyra úthlutanir, eða þú þarft að eyða öllu og endurkeyra öll líkönin þín, fer eftir gögnunum sem hafa verið uppfærð og hvernig möguleikar kostnaðarbókhaldsins eru settir upp. Það þarf að auðkenna handvirkt hvar víddarleiðréttingar hafa áhrif á kostnaðarbókhald og hvar er þörf á uppfærslum. [!INCLUDE[prod_short](includes/prod_short.md)] býður ekki upp á sjálfvirka leið til að gera það sem stendur.

## <a name="see-also"></a>Sjá einnig

[Vinna með víddir](finance-dimensions.md)
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
