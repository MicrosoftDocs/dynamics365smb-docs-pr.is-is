---
title: Úrræðaleit og leiðrétta víddir
description: Fræðast um hvernig á að leysa dæmigerðar víddarvillur og hvernig á að leiðrétta víddir eftir að þær eru notaðar í bókuðum færslum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 08/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Úrræðaleit og leiðrétta víddir

Fjárhagsskýrslugerð og greiningaryfirlit reiða sig oft á gögn úr ýmsum víddum. Þrátt fyrir þær öryggisráðstafanir sem í boði eru gerast stundum mistök sem geta leitt til ónákvæmni. Þessi grein lýsir nokkrum dæmigerðum villum og útskýrir hvernig á að leiðrétta víddarúthlutun í bókuðum færslum þannig að fjárhagsskýrslur séu réttar.

## Úrræðaleit fyrir víddarvillur

Þegar bókuð eru skjöl eða færslubókarlínur með víddum geta ýmsar villur orðið. Hins vegar eru þær yfirleitt tengdar röngu víddaruppsetningu eða úthlutun.

> [!NOTE]
> Í eftirfarandi lista yfir hugsanleg villuboð eru kóðarnir *%X* staðgenglar fyrir gagnabreyturnar sem raunverulegu skilaboðin munu innihalda í notendaviðmótinu, háð samhenginu. Til dæmis *%1 %2 er útilokað.* gæti birst í notendaviðmótinu sem „Víddarkóðinn SVÆÐI er útilokaður.“.  

|Gefa út|Villuboð|Möguleg lausn|
|-----|-------------|-----------------|
|Útilokuð vídd|%1 %2 er útilokað.|-Finna óbókuð skjöl sem innihalda víddasamstæða með víddinni sem lokað er á og afloka.<br />-Fjarlægja línu víddasamstæðu fyrir útilokuðu víddina.|
|Eydd vídd|%1 %2 finnst ekki.|-Endurheimta vídd sem vantar.<br />-Finna óbókuð skjöl sem innihalda víddasamstæða með týndu víddinni og bæta henni við.<br />-Fjarlægja línu víddasamstæðu fyrir vídd sem vantar.|
|Útilokað víddargildi|%1 %2 - %3 er útilokað.|-Finna óbókuð skjöl sem innihalda víddasamstæða með lokaða víddargildi og afloka það.<br />-Fjarlægja línu víddasamstæðu fyrir útilokaða víddargildið.|
|Eydd víddargildi|    %1 fyrir %2 vantar.|-Endurheimta víddargildi sem vantar.<br />-Finna óbókuð skjöl sem innihalda víddasamstæða með víddargildi sem vantar og bæta því við.<br />-Fjarlægja línu víddasamstæðu fyrir víddargildið sem vantar.|
|Óheimilt víddargildi|Gerð víddargildis fyrir %1 %2 – %3 má ekki vera %4.|-Breyttu reitnum **Gerð víddargildis** á síðunni **Víddargildi** í **Staðlað** eða **Frá-tala**.<br />-Fjarlægja línu víddasamstæðu fyrir útilokaða víddargildið.|
|Útilokuð víddarsamsetning|Víddirnar %1 og %2 er ekki hægt að nota samtímis.|-Finna óbókuð skjöl sem innihalda víddasamstæða með víddasamsetningunni sem lokað er á og opna hana af.<br />-Breyta einni af heimildasamstæða línum sem stangast á fyrir víddarsamsetninguna.|
|Útilokuð samsetning víddargildis|Víddarsamsetningarnar %1 - %2 og %3 - %4 er ekki hægt að nota samtímis.|-Finna óbókuð skjöl sem innihalda víddasamstæða með lokaðri samsetningu víddargildi og opna það af.<br />-Breyta einni af heimildasamstæða línum víddargildi.|
|Auður víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Kóði tilskilinn**|-Velja %1 fyrir %2 %3.<br />-Velja %1 fyrir %2 %3 fyrir %4 %5.|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færa skal inn víddargildi utanblanks fyrir víddina sem misræmi er í víddasamstæða.|
|Rangur víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Sami kóði**|-Veldu %1 %2 fyrir %3 %4.<br />-Veldu %1 %2 fyrir %3 %4 fyrir %5 %6|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn nauðsynlegt víddargildi fyrir víddina sem stangast á í víddasamstæðunni.|
|Kóti utanblank-víddargildi fyrir auða sjálfgefna vídd þar sem **sami kóti er í reitnum** Virðisbókun **·**|-%1 %2 verður að vera auður.<br />-%1 %2 verður að vera auður fyrir %3 %4.|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn auðan víddargildiskóða fyrir víddina sem stangast á í víddasamstæðunni.|
|Óvæntur víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Enginn kóði**|-%1 %2 má ekki nefna.<br />-%1 %2 má ekki nefna fyrir %3 %4|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Fjarlægja línuna sem stangast á úr víddasamstæðunni.|
|Víddarleiðrétting lýkur ekki rétt.||-Veljið **Endurstilla** til að snúa leiðréttingunni aftur í drög. Þetta núllstillir breytingarnar og hægt er að keyra leiðréttingu aftur.|

## Breyting á víddarúthlutunum eftir bókun

Ef röng vídd uppgötvast í bókuðum fjárhagur færslum er hægt að leiðrétta víddargildin og uppfæra greiningaryfirlitin. Leiðréttingin hjálpar til við að halda fjárhagsskýrslum og greina nákvæmar.

> [!IMPORTANT]
> Eiginleikar til að leiðrétta víddir eru einungis ætlaðir til að hjálpa við nákvæma fjárhagsskýrslugerð. Víddarleiðréttingar aðeins við um fjárhagsfærslurnar. Þær breyta ekki víddum sem eru úthlutaðar á færslur í öðrum fjárhag vegna sömu viðskipta. Misræmi verður á milli vídda sem eru úthlutaðar í fjárhag og undirfjárhag.

### Setja upp víddaleiðréttingar

Tvö atriði þarf að hafa í huga þegar víddarleiðréttingar eru settar upp:

* Eru til víddir sem ekki á að leyfa fólki að breyta? Á síðunni **Stillingar víddarleiðréttingar** skal tilgreina víddirnar sem á að hindra breytingar á.
* Hver getur breytt víddum? Til að leyfa fólki að gera breytingar skal úthluta notendunum heimildinni **D365 DIM CORRECTION**. Heimildirnar gera þeim kleift að stofna víddarleiðréttingar, keyra þær og afturkalla ef þess gerist þörf. Einnig er hægt að tilgreina víddir sem lokaðar eru á. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md). 

### Leiðrétta vídd

Hægt er að velja handvirkt eina eða fleiri fjárhagsfærslur eða nota síur til að velja safn af færslum. Ef þörf er á er einnig hægt að bæta við eða eyða víddum. 

1. Til að hefja víddarleiðréttingu skal nota eina af eftirfarandi síðum:

    * Á síðunni **Fjárhagsdagbækur**, með því að velja dagbók, og velja **síðan réttar víddir** . Þessi aðgerð hefst leiðrétting á færslum í valinni dagbók.
    * Á síðunni **fjárhagur færslur** með því að velja aðgerðina **Réttar víddir** . 

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

### Staðfesta víddaleiðréttingar

Áður en leiðrétting er keyrð er góð hugmynd að staðfesta hana fyrst. Staðfesting leitar að takmörkunum í virðisbókun fyrir fjárhagsreikninga, takmarkanir fyrir víddir og hvort víddargildin séu útilokuð. Meðan á staðfestingu stendur er staða leiðréttingar stillt á **Staðfesting í gangi**. Þegar leiðrétting er staðfest er útkoman sýnd í reitnum **Staða staðfestingar**. Ef villur fundust er hægt að nota aðgerðina **Skoða villur** til að kanna þær nánar. Þegar villa hefur verið lagfærð þarf að nota aðgerðina **Enduropna** til að keyra leiðréttinguna eða nýja staðfestingu.

Annaðhvort er hægt að keyra leiðréttingu strax eða tímasetja hana fram í tímann. Ef leiðréttingar eru keyrðar á stóru gagnasafni er mælt með því að tímasetja það til keyrslu utan vinnustunda. Frekari upplýsingar er að finna í [Víddarleiðréttingar á stórum gagnasöfnum](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### Afturkalla leiðréttingu

Þegar vídd hefur verið leiðrétt og útkoman er ekki þér að skapi geturðu notað aðgerðina **Afturkalla** til að endurstilla fyrra gildið. Hins vegar er aðeins hægt að afturkalla nýjustu leiðréttinguna. Áður en leiðrétting er afturkaluð er hægt að staðfesta breytingarnar sem eru afleiðingar afturkræfrar aðgerðar. Til dæmis er villuleit gagnleg ef víddartakmörkunum hefur breyst eftir að leiðréttingin var gerð.

Ef aðgerðin Afturkalla er ekki tiltæk, til dæmis vegna þess að margar leiðréttingar eru fyrir hendi, er hægt að nota aðgerðina **Afrita í Drög** til að hefja nýja leiðréttingu fyrir sömu færslur.

### Víddaleiðréttingar í stórum gagnasöfnum

Farið varlega þegar stór færslusöfn eru leiðrétt, t.d. söfn sem innihalda meira en 10.000 færslur. Ef það er hægt þá mælum við með að nota síur til að keyra leiðréttingar á smærri gagnasöfnum. Það er einnig góð hugmynd að keyra leiðréttingar utan venjulegs vinnutíma. 

### Nota greiningaryfirlit með víddaleiðréttingum

Ef **Uppfæra við bókun** er virkt fyrir greiningaryfirlit [!INCLUDE[prod_short](includes/prod_short.md)] , getur það uppfært yfirlitið þegar fylgiskjöl og færslubækur eru bókuð. Einnig er hægt að uppfæra yfirlit með þessari stillingu virkjaða með niðurstöður víddarleiðréttinga. Til að gera það skal kveikja á **Uppfæra greiningaryfirlit**. Uppfærsla greiningaryfirlita getur haft áhrif á afköst, sérstaklega fyrir stór gagnasöfn, þannig að mælt er með því að greiningaryfirlit séu uppfærð eingöngu fyrir lítil gagnasöfn.  

### Skoða leiðréttingar á eldri víddum

Ef fjárhagur færsla var leiðrétt er hægt að rannsaka breytingarnar með aðgerðinni **Ferill víddaleiðréttinga** .

### Meðhöndla ófullnægjandi leiðréttingar

Ef leiðréttingu er ekki lokið birtist viðvörun á leiðréttingarspjaldinu. Ef það gerist er hægt að nota aðgerðina **Endurstilla** til að snúa leiðréttingunni aftur í drög og afturkalla breytingarnar. Síðan er hægt að keyra leiðréttinguna aftur.

> [!NOTE]
> Endurstilling ólokinnar leiðréttingar hefur ekki áhrif á uppfærslur greiningaryfirlita vegna þess að þær gerast undir lok leiðréttingarferlisins.

### Nota kostnaðarbókhald með leiðréttum fjárhagsfærslum

Þegar víddir hafa verið leiðréttar eru gögnin um kostnaðarbókhald ekki samstillt. Kostnaðarbókhald notar víddir til að leggja saman upphæðir fyrir kostnaðarstöðvar og kostnaðarhluti og keyra kostnaðarúthlutanir. Ef víddum er breytt fyrir fjárhagsfærslur ætti líklega að keyra kostnaðarbókhaldslíkönin aftur. Það fer eftir gögnunum sem voru uppfærð og hvernig getu kostnaðarbókhalds er sett upp gæti þurft að:

* Eyða aðeins nokkrum kostnaðardagbókum og keyra úthlutanir aftur.
* Eyða öllu og keyra öll líkönin aftur.

Tilgreina verður handvirkt hvar víddarleiðréttingar hafa áhrif á kostnaðarbókhald og hvar uppfærslu er þörf. [!INCLUDE[prod_short](includes/prod_short.md)] veitir ekki sjálfvirka leið til að gera það.

## Sjá einnig .

[Vinna með víddir](finance-dimensions.md)    
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
