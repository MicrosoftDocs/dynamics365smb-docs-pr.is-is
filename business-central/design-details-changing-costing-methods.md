---
title: Hönnunarupplýsingar - Breyta kostnaðarútreikningum fyrir vörur
description: Lærið að úthluta öðrum kostnaðarútreikningi á vöru þótt varan hafi þegar verið notuð í færslum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'costing methods, costing, item cost'
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: bholtorf
---

# <a name="design-details-change-the-costing-method-for-items"></a><a name="design-details-change-the-costing-method-for-items"></a>Hönnunarupplýsingar: Breyta kostnaðarútreikningi fyrir vörur

Í [!INCLUDE[prod_short](includes/prod_short.md)] er ekki hægt að breyta kostnaðarútreikningi fyrir vöru eftir að varan hefur verið notuð í færslu. Til dæmis eftir að varan hefur verið keypt eða seld. Ef röngum kostnaðarútreikningi var úthlutað á vöru eða vörur, er ekki víst að vandinn uppgötvist fyrr en fjárhagsskýrslugerðin er gerð.

Þetta efnisatriði lýsir hvernig á að leysa úr þessum kringumstæðum. Mælt er með því að skipta vörunni sem er með röngum kostnaðarútreikningi út fyrir nýja vörur og nota samsetningarpöntun til að flytja birgðirnar úr gömlu vörunni til þeirrar nýju.

> [!NOTE]
> Að nota samsetningarpöntun gerir það að verkum að kostnaðurinn heldur áfram að flæða þrátt fyrir að til séu útistandandi innkaupareikningar eða sendingargjöld sem þarf að bóka. Þar að auki er hægt að afturkalla umreikninginn og fá upprunalegt vörumagn til baka ef þörf er á því.

> [!TIP]
> Til að kynna sér ferlið er mælt með því að hafist sé handa með umreikningsferlið með einni vöru eða safn fárra vara.

## <a name="about-costing-methods"></a><a name="about-costing-methods"></a>Um aðferðir kostnaðarútreikninga

Aðferð kostnaðarútreiknings stjórnar kostnaðarútreikningum þegar vörur eru keyptar, mótteknar í birgðum eða seldar. Aðferðir kostnaðarútreikninga hafa áhrif á tímasetningar á upphæðum sem skráðar eru í kostnaði seldra vara sem hefur áhrif á brúttóhagnað. Það er þetta flæði sem reiknar kostnað seldra vara. Kostnaður seldra vara (COGS) og tekjur eru notuð til að ákvarða brúttóhagnað á eftirfarandi hátt:

*brúttóhagnaður* = *tekjur - kostnaður seldra vara*

Þegar birgðavörur eru settar upp verður að úthluta aðferð kostnaðarútreiknings. Aðferðin getur verið breytileg milli fyrirtækja og frá vöru til vöru og er því mikilvægt að velja rétta aðferð. [!INCLUDE[prod_short](includes/prod_short.md)] styður eftirfarandi aðferðir kostnaðarútreikninga:

* Meðaltal
* FIFO
* LIFO
* Staðlað
* Sérstakt

Nánari upplýsingar eru í [Upplýsingar um hönnun: Kostnaðarútreikningar](design-details-costing-methods.md).

## <a name="use-assembly-orders-to-change-costing-method-assignments"></a><a name="use-assembly-orders-to-change-costing-method-assignments"></a>Nota samsetningarpantanir til að breyta úthlutunum á aðferðum kostnaðarútreikninga

Þessi hluti útskýrir eftirfarandi skref til að breyta aðferð kostnaðarútreiknings sem er úthlutað á vöru:

1. Skilgreinið sjálfgefna aðferð kostnaðarútreiknings.
2. Gerið grein fyrir vörunum sem breyta á aðferð kostnaðarútreiknings fyrir og númerið þær aftur.
3. Búið til nýjar vörur með gömlu talnaröðinni og afritið aðalgögnin í runu.
4. Afritið handvirkt tengd aðalgögn úr fyrirliggjandi vöru í nýju vöruna.
5. Ákvarðið birgðamagnið sem á að færa frá upprunalegu vörunni og yfir á nýju vöruna.
6. Flytjið birgðirnar yfir á nýju vöruna.
7. Meðhöndlið birgðamagnið sem er úthlutað samkvæmt eftirspurn.
8. Útilokið upprunalegu vöruna frá frekari notkun.  

### <a name="define-a-default-costing-method"></a><a name="define-a-default-costing-method"></a>Skilgreina sjálfgefna aðferð kostnaðarútreiknings

Til að reyna að koma í veg fyrir hugsanleg mistök er hægt að tilgreina sjálfgefna aðferð kostnaðarútreiknings fyrir nýjar vörur. Þegar einhver stofnar nýja vöru mun [!INCLUDE[prod_short](includes/prod_short.md)] stinga upp á sjálfgefinni aðferð kostnaðarútreiknings. Sjálfgefin aðferð er tilgreind í reitnum **Sjálfgefin aðferð kostnaðarútreiknings** á síðunni **Birgðauppsetning**. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a><a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Gera grein fyrir vörunum sem breyta á aðferð kostnaðarútreiknings fyrir og númera þær aftur

Þú gætir viljað gefa nýju vörunum sömu númerin og vörurnar sem verið er að skipta út eru með. Til að gera það þarf að breyta númerum fyrirliggjandi vara. Ef til að mynda fyrirliggjandi vörunúmerið er „P1000“, er hægt að breyta því í „X-P1000.“ Þetta er handvirk breyting sem þarf að gera fyrir hverja vöru fyrir sig.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a><a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Búa til nýjar vörur með gömlu talnaröðinni og afrita aðalgögnin í runu

Búið til nýju vörurnar með því að nota núverandi talnaröð. Að undanskildum reitnum **Aðferð kostnaðarútreiknings** ættu nýju vörurnar að innihalda sömu aðalgögnin og fyrirliggjandi vörur. Til að flytja aðalgögnin fyrir vöruna, og tengd gögn úr öðrum eiginleikum, skal nota aðgerðina **Afrita vöru** á síðunni **Birgðaspjald**. Frekari upplýsingar er að finna í [Afrita fyrirliggjandi vörur í Búa til nýjar vörur](inventory-how-copy-items.md).

Þegar búið er að stofna nýju vörurnar og flytja aðalgögnin skal úthluta réttri aðferð kostnaðarútreiknings.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a><a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Afrita handvirkt tengd aðalgögn úr upprunalegri vöru í nýju vöruna

Til að koma nýju vörunum að fullu í gagnið þarf að afrita handvirkt sum aðalgögn úr öðrum svæðum eins og útskýrt er í eftirfarandi töflu.

|Svæði  |Hvað á að afrita  |Hvernig á að afrita það  |
|---------|---------|---------|
|Birgðir |Birgðahaldseiningar (BHE) |Athugið hvort birgðahaldseining sé tilgreind fyrir upprunalegu vöruna. Ef áætlunarfæribreytur hafa verið slegnar inn fyrir hvert birgðahaldseiningaspjald þarf að stofna handvirkt birgðahaldseininguna fyrir nýju vöruna. Ef færibreyturnar eru ekki tilgreindar, er hægt að nota runuvinnsluna **Stofna birgðahaldseiningu** af síðunni **Birgðaspjald** til að stofna gögnin.|
| |Staðgengilsvörur |Athugið hvort einhverjar staðgengilsvörur séu skilgreindar fyrir upprunalegu vöruna. Ef svo er skal flytja gögnin yfir í nýju vöruna. Til að skoða staðgengilsvörur skal nota aðgerðina **Staðgenglar** á síðunni **Birgðaspjald**. |
| |Greiningarskýrslur |Farið yfir skýrslur vörugreininga, sölugreininga og innkaupagreininga. Fyrir þá sem vísa til upprunalegra vara, er annaðhvort hægt að stofna nýja greiningarskýrslu með tilvísun í nýju vöruna (halda upprunalegri greiningarskýrslu til að nota sem feril) eða leiðrétta skýrslurnar þannig að þær vísi til nýju varanna. |
| |Staðlaðar færslubækur |Athugið hvort staðlaðar færslubækur vísi í upprunalegu vöruna og flytji gögnin til nýju vörunnar þegar á þarf að halda. Þessar upplýsingar finnast í stöðluðum færslubókum, sem eru aðgengilegar í birgðabókinni.  |
|Sölur |Fyrirframgreiðsluprósenta sölu | Athugið hvort einhverjar fyrirframgreiðsluprósentur sölu eru skilgreindar fyrir upprunalegu vöruna og flytjið gögnin yfir í nýju vöruna. Til að skoða fyrirframgreiðsluprósentur, á síðunni **Birgðaspjald**, skal velja **Sölur** og síðan **Fyrirframgreiðsluprósentur**.|
|Innkaup |Fyrirframgreiðsluprósenta innkaupa |Athugið hvort einhverjar fyrirframgreiðsluprósentur innkaupa eru skilgreindar fyrir upprunalegu vöruna og flytjið gögnin yfir í nýju vöruna. Til að skoða fyrirframgreiðsluprósentur, á síðunni **Birgðaspjald**, skal velja **Innkaup** og síðan **Fyrirframgreiðsluprósentur**. |
|Vöruhús |Innihald hólfs |Yfirfarið innihald hólfs sem skilgreint er fyrir upprunalega vöru. Ef dálkar á borð við lágmarks Magn, hámarks Magn, sjálfgefið og sérstakt hafa verið slegnir inn handvirkt og ef svo er þarf að stofna hólfainnihald fyrir nýju vöruna. Ef svo er ekki þarf ekki að grípa til neinna aðgerða. [!INCLUDE[prod_short](includes/prod_short.md)] vinnur með færslurnar þegar vöruhúsaskjöl og færslubækur eru skráðar.|
|Vinnsla |Verð verks |Athugið hvort verð verka eru skilgreind fyrir upprunalegu vöruna og flytjið gögnin yfir í nýju vöruna. Þessar upplýsingar eru aðgengilegar á síðunni **Verkspjald** í hlutanum **Upplýsingar um verk - fjöldi verða** á **Upplýsingakassasvæði**. |
|Þjónusta |Hæfnistilfangaþjónusta |Athugið hvort hæfnistilfangaþjónusta er skilgreind fyrir upprunalegu vöruna og flytjið gögnin yfir í nýju vöruna. Til að skoða hæfnistilfangaþjónustu skal nota aðgerðina **Hæfnistilfang** á síðunni **Birgðaspjald**.  |
| |Þættir þjónustuvöru |Athugið hvort þættir eru skilgreindir fyrir upprunalegu þjónustuvöruna og flytjið gögnin yfir í nýju vöruna. Til að skoða þætti þjónustuvöru, á síðunni **Birgðaspjald**, skal nota aðgerðina **Þjónustuvara** til að opna lista yfir tengdar þjónustuvörur og síðan velja aðgerðina **Þættir**.  |
|Framleiðsla |Framl.uppskriftir |Athugið hvort einhverjar framleiðsluuppskriftir innihaldi upprunalegu vöruna og skiptið henni út fyrir nýju vöruna. Til að skipta út upprunalegu vörunni, á síðunni **Framleiðsluuppskriftir**, skal velja aðgerðina **Skipta út vöru framleiðsluuppskriftar**. |
|Samsetning |Samsetningaruppskrift |Athugið hvort einhverjar framleiðsluuppskriftir innihaldi upprunalegu vöruna og skiptið henni út handvirkt fyrir nýju vöruna. |

> [!IMPORTANT]
> Ef nýja aðferð kostnaðarútreikningsins er stöðluð ætti að slá inn gildi í reitinn **Staðlað kostnaðarverð** á síðunni **Birgðaspjald**. Hægt er að nota síðuna **Vinnublað staðlaðs kostnaðarverðs** til að stilla kostnaðarhlutdeildina á viðeigandi hátt. Frekari upplýsingar eru í [Uppfæra staðlað kostnaðarverð](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a><a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Ákvarða birgðamagnið sem á að færa frá upprunalegu vörunni og yfir á nýju vöruna

> [!NOTE]
> Þetta skref tekur ekki tillit til magns sem er tekið með í ósendum pöntunum. Frekari upplýsingar er að finna í [Meðhöndla birgðamagn sem er úthlutað á eftirspurn](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Notið raunbirgðabók til að búa til lista yfir magnið í birgðum. Eftir því hver uppsetning vöruhúsastaðsetningar er, skal nota eitt af eftirfarandi:

* Raunbirgðabækur
* Vöruh. Raunbirgðabækur

Báðar færslubækurnar geta reiknað birgðamagn vörunnar, þ.m.t. staðsetningu, afbrigði, hólf og geymslustað. Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir með færslubókum](inventory-how-count-adjust-reclassify.md).

### <a name="transfer-the-inventory-to-the-new-item"></a><a name="transfer-the-inventory-to-the-new-item"></a>Flytja birgðir yfir í nýju vöruna

Stofnið og bókið samsetningarpantanir til að flytja kostnað og birgðamagn úr upprunalegu vörunni og yfir í nýju vöruna. Samsetningarpantanir geta breytt einni vöru í aðra á meðan hún varðveitir kostnaðinn. Þetta hjálpar til við að tryggja að nettósamtölur fyrir birgðarreikning og kostnað seldra vara verði ekki fyrir áhrifum (nema þegar nýja aðferð kostnaðarútreikningsins er stöðluð, en í slíku tilfelli er hægt að dreifa kostnaðinum á fráviksreikninga). Nánari upplýsingar, sjá [Samsetningarstjórnun](assembly-assemble-items.md).

Þegar samsetningarpantanir eru stofnaðar skal nota upplýsingarnar úr raunbirgðabók eða vöruhúsi. Raunbirgðabók. Eftirfarandi töflur útskýra upplýsingarnar í skýrslunum sem færa á inn í hausinn og línurnar á samsetningarpöntuninni.

#### <a name="header"></a><a name="header"></a>Haus

|Svæði  |Gildi sem á að færa inn  |
|---------|---------|
|Vörunr. |Númer nýju vörunnar. |
|Magn |Magnið í raunbirgðabók.<br> **Athugið:** Magnið sem er reiknað af raunbirgðabókum inniheldur ekki magnið sem er í pöntunum sem hefur ekki enn verið sent.  |
|Afbrigðiskóði |Sá sami og í raunbirgðabók.  |
|Kóti birgðageymslu  |Sá sami og í raunbirgðabók. |
|Mælieiningarkóði |Sá sami og í raunbirgðabók. |
|Hólfkóti |Sá sami og í raunbirgðabók. |

#### <a name="lines"></a><a name="lines"></a>Línur

|Svæði  |Gildi sem á að færa inn  |
|---------|---------|
|Tegund |Vara |
|Fj. |Númer upprunalegu vörunnar. |
|Magn á |1 |
|Afbrigðiskóði |Sá sami og í raunbirgðabók. |
|Kóti birgðageymslu  |Sá sami og í raunbirgðabók. |
|Mælieiningarkóði |Sá sami og í raunbirgðabók. |

> [!NOTE]
> Samsetningarpöntun getur aðeins meðhöndlað eina birgðahaldseiningu fyrir vöru hverju sinni. Stofna þarf samsetningarpöntun fyrir hverja samsetningu birgðahaldseiningar sem er með magn í birgðum.

> [!NOTE]
> Fyrir vöruhúsastaðsetningu gæti þurft að stofna tiltektir áður en hægt er að bóka samsetningarpöntunina. Til að rannsaka það skal fara yfir uppsetningu fyrir tiltekt á síðunni **Birgðageymsluspjald**. Frekari upplýsingar eru í [Setja upp vörur og birgðageymslur fyrir beinan frágang og tínslu](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a><a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Meðhöndla birgðamagnið sem er úthlutað samkvæmt eftirspurn

Best er að birgðir fyrir upprunalega vöru fari niður í núll eftir að birgðamagn er flutt. Hins vegar geta verið útistandandi pantanir, vinnublöð og færslubækur (sjá töfluna hér að neðan) sem þurfa enn magn fyrir upprunalegu vöruna. Magnið getur einnig verið útilokað vegna frátekningar eða vörurakningar.

**Dæmi** Til eru 1000 stk. í birgðum og 20 stk. eru frátekin fyrir sölupöntun sem hefur ekki verið send. Í slíku tilfelli gætirðu ákveðið að halda þessum 20 stykkjum. í gömlu vörunni þannig að hægt sé að uppfylla útistandandi pöntun.

> [!NOTE]
> Virk svæði eru til staðar sem geta haft áhrif á magnið, eins og kemur fram í töflunni hér að neðan, þannig að það getur verið erfitt að finna réttu upphæðina. Til öryggis, samkvæmt dæminu hér að ofan, getur þú valið að halda 100 stykkjum. og flutt hin 900 stykkin. í staðinn. Önnur leið til að gera þetta væri að vinna úr skjölum og færslubókum þannig að aðeins lítill viðráðanlegur fjöldi sé eftir. Enn annar valkostur er að flytja allt magnið í nýju vöruna og flytja síðan sumt af því aftur í upprunalegu vöruna með því að nota samsetningarpöntunina.

Eftirfarandi tafla sýnir virk svæði þar sem hugsanlega er útistandandi magn.

|Svæði  |Hvar á að leita að útistandandi magni  |
|---------|---------|
|Sölur |Söluskjöl, þ.m.t. pantanir, vöruskilapantanir, reikningar, tilboð, standandi pantanir og kreditreikningar |
|Birgðir |Birgðabækur, frátekningar, vörurakning og vinnublað staðlaðs kostnaðarverðs |
|Innkaup |Innkaupaskjöl, þ.m.t. pantanir, vöruskilapantanir, reikningar, tilboð, standandi pantanir og kreditreikningar |
|Áætlun |Innkaupatillögublað, áætlanavinnublað og pantanaáætlun |
|Vöruhús |Flutningspantanir, vöruhúsaafhendingar, vöruhúsabækur og vöruhúsatínsla, -frágangur og hreyfingar, innri tínsla og frágangur og vinnublöð hólfastofnunar |
|Samsetning |Samsetningarskjöl, þ.m.t. pantanir, skilapantanir og standandi pantanir |
|Verk |Verkáætlunarlínur og verkbókarlínur |
|Þjónusta |Þjónustuskjöl og þjónustusamningar |
|Framleiðsla |Framleiðslupantanir (áætlaðar, fastáætlaðar og losaðar) |

### <a name="block-the-original-item-from-further-use"></a><a name="block-the-original-item-from-further-use"></a>Útiloka upprunalega vöru frá frekari notkun

Þegar birgðastaða fyrir upprunalega vöru er núll er hægt að útiloka vöruna til að koma í veg fyrir að hún sé notuð í nýjum færslum. Til að útiloka vöruna, á síðunni **Birgðaspjald**, skal kveikja á víxlhnappnum **Útilokað**. Frekari upplýsingar er að finna í [Loka á vörur í sölum eða innkaupum](inventory-how-block-items.md).

## <a name="summary"></a><a name="summary"></a>Samantekt

Að breyta aðferð kostnaðarútreiknings fyrir vörur sem hafa verið notaðar í færslum er ferli, og ekki hefðbundin aðgerð í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að nota skrefin sem lýst er í þessu efnisatriði sem sniðmát fyrir ferlið.

Ferlið getur verið tímafrekt út af mörgum handvirkum skrefum. En að gefa sér tíma til að klára þau mun lágmarka þau áhrif sem mistök geta haft í för með sér í fjárhagnum.

Við mælum með eftirfarandi:

1. Metið hagkvæmni ferlisins með því að prófa eina, eða hugsanlega nokkrar, dæmigerðar vörur í gegnum allt ferlið.
2. Íhugið að hafa samband við reynslumikinn samstarfsaðila sem getur hjálpað þér í ferlinu.

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Yfirlit](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
