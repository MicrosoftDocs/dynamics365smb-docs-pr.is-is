---
title: Unnið með víddir til að rekja og greina gögn á auðveldan hátt
description: Nota skal víddir til að flokka færslur, til dæmis eftir deild eða verki, svo hægt sé að rekja og greina gögn á auðveldan hátt til að stuðla að betri ákvarðanatöku í viðskiptum.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.search.form: 408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e5579df4d63a4f800118ca320d60a984f203022b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517577"
---
# <a name="work-with-dimensions"></a>Vinna með víddir
Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá.  

Til dæmis, í stað þess að setja upp sérstaka aðalbókarreikninga fyrir hverja deild og verkefni, getur þú notað víddir sem grundvöll fyrir greiningu og forðast að þurfa að stofna flókna bókhaldslykla. Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).

Annað dæmi er að setja upp vídd sem kallast *Deild* og nota þá vídd þegar þú bókar söluskjöl. Þetta mun leyfa þér að nota viðskipti upplýsingaöflun tól til að sjá hvaða deild selt hvaða atriði. Því fleiri stærðir sem þú notar, nákvæmari skýrslurnar sem þú getur byggt á viðskiptatengslunum þínum. Til dæmis getur ein sölufærsla innihaldið upplýsingar frá mörgum víddum, t.d.:  

* Reikningurinn sem vörusalan var sendur til  
* Þar sem hluturinn var seldur
* Hver seldi það
* Tegund viðskiptavina sem keypti hana  

## <a name="analyzing-by-dimensions"></a>Greining eftir víddum

Víddir gegna mikilvægu hlutverki í viðskiptagreind, eins og t.d. þegar greiningaryfirlit eru skilgreind. Nánari upplýsingar er að finna í [Greina gögn eftir víddum](bi-how-analyze-data-dimension.md).

> [!TIP]
> Fljótleg leið til að greina færslugögn eftir víddum er að nota afmörkun á samtölum eftir víddum með aðgerðinni **Stilla víddarafmörkun** í bókhaldslyklum og síðum fyrir færslur.

> [!NOTE]
> Greiningaryfirlit nota oft gögn úr víddum. Ef kemur í ljós að röng vídd hafi verið notuð í bókuðum fjárhagsfærslum er hægt að leiðrétta víddargildin og uppfæra greiningaryfirlitið. Það hjálpar til við að halda fjárhagsskýrslum og greiningum nákvæmum. Frekari upplýsingar eru í [Úrræðaleit og víddarleiðrétting](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

## <a name="dimension-sets"></a>Víddasamstæður

<!--we describe what they are, but not their value.-->
Víddasamstæða er sérstök samsetning víddargilda. Er vistað sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Víddasamstæðan er auðkennd með algengum víddasamstæðukennum sem eru úthlutuð hverri víddasamstæðufærslu sem tilheyrir víddasamstæðunni.  

Þegar þú býrð til dagbókarlínu, skjalhaus eða skjalastiku, getur þú tilgreint samsetningu af víddarmörkum. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

## <a name="setting-up-dimensions"></a>Uppsetning vídda

Hægt er að skilgreina víddirnar og víddargildin til að flokka færslubókum og skjölum, t.d. sölupantanir og innkaupapantanir. Þú setur upp víddir á síðunni **Víddir**, þar sem búin er til ein lína fyrir hverja vídd, svo sem *Verkefni*, *Deild*, *Svæði*, og *Sölumaður*.

Þú setur einnig upp gildi fyrir víddir. Gildi gætu til dæmis verið deildirnar í fyrirtækinu. Hægt er að setja víddir upp í stigveldisröð, svipað og bókhaldslykilinn, svo að hægt verði að stigskipta gögnunum og taka saman milliniðurstöður. Hægt er að skilgreina eins margar víddir og víddargildi og þörf er á og allir í fyrirtækinu geta notað þau.

Þegar víddir og gildi eru sett upp, er hægt að skilgreina altækar víddir og flýtivísanir í víddir á síðunni **Uppsetning fjárhags** sem verður alltaf í boði til að velja sem reiti í færslubókar- og skjalalínum, og fjárhagsfærslum án þess að þurfa fyrst að opna síðuna **Víddir**. Frekari upplýsingar eru í [Að setja upp altækar víddir og flýtivísanir í víddir](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Altækar víddir** eru notaðar sem afmarkanir, t.d. á skýrslur, runuvinnslur og XMLports. Hægt er að nota eingöngu tvær altækar víddir, svo veldu því víddir sem verða notaðar oft.
* **Flýtivísanir í víddir** eru tiltækar sem reitir í færslubókum, skjalalínum og fjárhagsfærslum. Hægt er að stofna allt að átta af þeim.  

> [!NOTE]
> Eftir að þú hefur notað nýja vídd í hvaða færslu sem er, svo sem línu eða nýja færslu, getur þú ekki eytt víddinni, jafnvel þótt þú birtir ekki færsluna. Það er vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] það býr strax til víddasett fyrir línuna eða færsluna. Frekari upplýsingar eru í [Víddarsamstæður](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Til að setja upp sjálfgefnar víddir fyrir viðskiptavini, lánardrottna, og aðra reikninga

Hægt er að setja upp sjálfgefna vídd fyrir tiltekinn stakan reikning. Víddin verður afrituð í færslubókina eða fylgiskjalið þegar reikningsnúmerið er fært inn í línu, en hægt er að eyða eða breyta kóðanum í línunni ef það á við. Einnig er hægt að búa til vídd og krefjast þess að í henni þurfi að bóka færslu með ákveðinni tegund reiknings.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Víddir** og velja síðan viðkomandi tengil.  
2. Á síðunni **Víddir** skal velja viðkomandi vídd og svo **Sjálfg. vídd reikningsteg.** aðgerðina.  
3. Fylla þarf út línu fyrir hverja nýja vídd sem skal setja upp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Ef gera á vídd að skyldu án þess að úthluta sjálfgildi á víddina er reiturinn **Víddargildiskóti** hafður auður og **Kóti tilskilinn** valið í reitnum **Virðisbókun**.  

> [!WARNING]  
> Ef nota skal reikning í **Leiðrétta gengi** keyrslunni eða **Bóka birgðakostnað í fjárhagsbók** keyrslunni má ekki velja **tilskilinn kóða** eða **sama kóða**. Þessar keyrslur geta ekki notað víddarkóta.  

> [!NOTE]  
> Ef tilgreina verður aðra vídd fyrir reikning en sjálfgefnu víddina fyrir tegund reiknings verður að setja upp sjálfgefna vídd fyrir þann reikning. Sjálfgefna víddin fyrir þennan reikning kemur þá í stað sjálfgefnu víddarinnar fyrir tegund reiknings.  

### <a name="to-set-up-default-dimension-priorities"></a>Að setja upp sjálfgefinn víddarforgang

Mismunandi tegundir reikninga, eins og til dæmis viðskiptamannsreikningur og vörureikningur, geta haft mismunandi sjálfgefnar víddir uppsettar. Þar af leiðandi getur forritið lagt til fleiri en eina sjálfgefna vídd fyrir hverja færslu. Til að forðast slíka árekstra er hægt að láta forgangsreglur gilda í hverju tilviki.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forgangur sjálfgefinnar víddar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Sjálgefin forgangur vídda** í reitinn **Upprunakóði** er færður inn upprunakóði færslutöflunnar sem sjálfgefinn víddaforgangur gildir fyrir.  
3. Fyllt er út lína fyrir hvern forgang sjálfgefinnar víddar sem á að setja upp fyrir valinn upprunakóta.
4. Ferlið er endurtekið fyrir hvern upprunakóða þar sem á að setja upp sjálfgefinn víddarforgang.  

> [!IMPORTANT]  
> Ef settar eru upp tvær töflur með sama forgangi fyrir sama upprunakóta velur [!INCLUDE[prod_short](includes/prod_short.md)] alltaf töfluna með lægsta kennið.  

### <a name="to-set-up-dimension-combinations"></a>Að setja upp samsettar víddir

Til að forðast að bóka færslur með mótsagnarkenndum eða óviðkomandi víddum er hægt að loka eða takmarka tilteknar samsetningar tveggja vídda. Lokuð víddarsamsetning þýðir að ekki er hægt að bóka báðar víddir í sömu færslu sama hver víddargildin eru. Með takmarkaðri víddarsamsetningu er hægt að bóka báðar víddir í sömu færslu en aðeins með tilteknum víddargildasamsetningum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Víddasamsetningar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Víddarsamsetningar** er smellt á reitinn fyrir samsetningu vídda og síðan valinn einn af eftirfarandi valkostum.  

    |Svæði|Description|
    |----------------------------------|---------------------------------------|  
    |**Engin takmörkun**|Engar hömlur eru í gildi fyrir þessa víddasamsetningu. Öll víddargildi eru leyfð.|  
    |**Takmarkað**|Þessi víddarsamsetning hefur ákveðnar hömlur sem fara eftir víddargildunum sem slegin eru inn. Skilgreina þarf takmarkanirnar á síðunni **Samsetning víddargilda** .|  
    |**Lokað**|Þessi víddarsamsetning er ekki leyfð.|  

3. Ef valinn var kosturinn **Takmarkað** verður að skilgreina hvaða samsetningar víddargilda eru læstar. Það er gert með því að velja reitinn til þess að skilgreina víddarsamsetninguna.  
4. Nú er valin samsetning víddargilda og **Lokað** slegið inn í reitinn. Óútfylltur reitur þýðir að samsetning víddargilda er leyfð. Þetta er endurtekið ef margar samsetningar eru lokaðar.  

> [!NOTE]  
> Sömu víddir birtast í báðum röðum og dálkum og þess vegna birtast allar víddarsamsetningar tvisvar. [!INCLUDE[prod_short](includes/prod_short.md)] sýnir stillingarnar í báðum reitum sjálfvirkt. Ekki er hægt að velja neitt í reitunum úr vinstra horni uppi og niður því þeir reitir hafa sömu vídd í báðum röðum og dálkum.  
>
> Valinn kostur er ekki sýnilegur fyrr en farið er út úr reitnum.  
>
> Til að sýna nafn víddarinnar fremur en kótann er hægt að haka við reitinn **Sýna heiti dálks** .

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Að setja upp altækar víddir og flýtivísanir í víddir

Hægt er að nota altækar víddir og flýtivísanir í víddir sem síur í [!INCLUDE[prod_short](includes/prod_short.md)], þ.m.t. í skýrslum, runuvinnslum, fjárhagsfærslusíðum og greiningaryfirlitum. Alltaf er hægt að setja altækar víddir og flýtivísanir í víddir beint inn án þess að opna fyrst síðuna **Víddir**. Í færslubókar- og skjalalínum er hægt að velja altækar víddir og flýtivísanir í víddir í reit í línunni. Hægt er að setja upp tvær altækar víddir og átta flýtivísanir í víddir. Veldu víddirnar sem þú notar mest.

> [!Important]  
> Breyting á altækri vídd eða flýtivídd krefst þess að færslur sem bókaðar eru með vídd séu uppfærðar. Til að breyta altækri vídd skal nota virknina **Breyta altækum víddum**, en það getur verið tímafrekt og getur haft áhrif á afköst og töflur kunna að vera læstar meðan á uppfærslunni stendur. Þess vegna skaltu velja altækar víddir og flýtivísanir í víddir vandlega svo þú þurfir ekki að breyta þeim seinna. Til að breyta flýtivísun í vídd skal nota aðgerðina **Breyta víddum**. <br /><br />
> Frekari upplýsingar er að finna í [Til að breyta altækri vídd](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Þegar þú bætir við eða breytir altækri vídd eða flýtivídd ertu sjálfkrafa skráður út og aftur inn svo nýja gildið er undirbúið til notkunar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.
2. Í flýtiflipanum **Víddir** skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Að breyta altækum víddum

Breyting á altækri vídd eða flýtivídd uppfærir allar færslur sem bókaðar eru með vídd. Þar sem þetta ferli kann að vera tímafrekt og getur haft áhrif á afköst eru tvær mismunandi stillingar til staðar til að aðlaga ferlið að stærð gagnagrunnsins.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Breyta altækum víddum**.
3. Efst á síðunni skaltu velja einn af eftirfarandi valkostum til að skilgreina í hvaða stillingu runuvinnslan er keyrð.

    |Valkostur|Description|
    |-|-|
    |**Í röð**|(Sjálfgefið) Breytingin er gerð í einni færslu sem snýr við öllum færslum í víddirnar sem voru áður en breytingin átti sér stað.<br /><br />Mælt er með þessum valkosti ef fyrirtækið inniheldur tiltölulega fáar færslur þar sem það tekur stystan tíma að ljúka. Ferlið læsir mörgum töflum og lokar fyrir aðra notendur þangað til það er gert. Athugaðu að í stórum gagnagrunnum er hugsanlega ekki hægt að ljúka þessu ferli í þessari stillingu. Í því tilfelli skaltu nota valkostinn **Samhliða**.|
    |**Samhliða**|Víddarbreytingin gerist í mörgum bakgrunnskeyrslum og aðgerðinni er skipt niður í margar færslur. Til að nota þennan valkost þarf að kveikja á **Hliðstæðri vinnslu**. <br /><br />Mælt er með þessum valkosti fyrir stóra gagnagrunna eða fyrirtæki með margar bókaðar færslur vegna þess að það tekur stystu stund að ljúka. Athugið að með þessari stillingu hefst uppfærslan ekki ef fleiri en ein gagnagrunnslota er virk.|  

4. Í reitunum **Altæk vídd 1 - Kóði** og/eða **Altæk vídd 2 - Kóði** skaltu slá inn nýju víddina/víddirnar. Núverandi víddir birtast gráar á bak við reitina.
5. Gerið eitt af eftirfarandi, allt eftir stillingunni:
    * Í stillingunni **Eftir röð** skal velja aðgerðina **Byrja**.
    * Í stillingunni **Hliðsætt** skal velja aðgerðina **Undirbúa**.

    Flipinn **Skráarfærslur** er fylltur út með upplýsingum um víddirnar sem verður breytt.
6. Skráðu þig úr [!INCLUDE[prod_short](includes/prod_short.md)] og inn aftur.
7. Veldu aðgerðina **Ræsa** til að hefja samhliða vinnslu víddarbreytinganna. <!--is this also dependent on the mode?-->

### <a name="example-of-dimension-setup"></a>Dæmi um uppsetningu víddar

Segjum sem svo, að fyrirtækið vilji rekja færslur út frá skipulagseiningum og landfræðilegum staðsetningum. Til þess að gera það, er hægt að setja upp tvær víddir á síðunni **Víddir**:

* **SVÆÐI**  
* **DEILD**  

| Kóði | Name | Texti kóta | Texti afmörkunar |
| --- | --- | --- | --- |
| SVÆÐI |Svæði |Svæðiskóði |Svæðisafmörkun |
| DEILD |Deild |Deildarkóði |Afmörkun deildar |

Fyrir **SVÆÐI**, skal bæta við eftirfarandi víddargildum:

| Kóði | Name | Tegund víddargildis |
| --- | --- | --- |
| 10 |Suður-, Mið- og Norður-Ameríka |Frá-tala |
| 20 |Norður-Ameríka |Staðlað |
| 30 |Kyrrahafið |Staðlað |
| 40 |Suður-Ameríka |Staðlað |
| 50 |Norður- og Suður-Ameríka, Samtals |Til-tala |
| 60 |Evrópa |Frá-tala |
| 70 |ESB |Staðlað |
| 80 |Utan-ESB |Staðlað |
| 90 |Evrópa, Samtals |Til-tala |

Fyrir tvö helstu landsvæðin, N- og S-Ameríku og Evrópu, skal bæta við undirflokkum fyrir svæði með því að draga inn víddargildin. Þetta gera notanda kleift að tilkynna á sölu- eða kostnað í svæðum og fá samtölur fyrir stærri landfræðileg svæði. Einnig er væri hægt að velja að nota lönd og svæðum sem víddargildi, eða sýslur og borgir, það fer eftir gerð fyrirtækisins.

> [!NOTE]  
> Til að setja upp stigveldi verða kóðarnir að vera í stafrófsröð. Þar á meðal eru kóðarnir fyrir víddargildin sem eru fengin í [!INCLUDE[prod_short](includes/prod_short.md)].  

Fyrir **DEILD**, skal bæta við eftirfarandi víddargildum:

| Kóði | Name | Tegund víddargildis |
| --- | --- | --- |
| STJÓRN |Stjórnun |Staðlað |
| FRAML |Framleiðsla |Staðlað |
| SALA |Sölur |Staðlað |

Með þessari uppsetningu geturðu bætt við þínum tveimur víddum sem tveimur altækum víddum á síðunni **Uppsetning Fjárhagsgrunns**. Þetta þýðir að hægt er að nota SVÆÐI og DEILD sem afmarkanir á fjárhagsfærslur og einnig á allar skýrslur og fjárhagsáætlanir. Báðar altæku víddirnar eru líka sjálfkrafa tiltækar til notkunar á færslulínum og skjalahausum sem flýtivísanir í víddir.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Fá yfirlit um víddir sem eru notaðar oftar en einu sinni

Síðan **Sjálfgefnar víddir á margar línur** tilgreinir hvernig flokkur reikninga notar víddir og víddargildi. Það er gert með því að upplýsa marga reikninga og tilgreina síðan sjálfgefnar víddir og víddargildi fyrir alla reikninga sem hafa verið upplýstir á reikningalistanum. Þegar sjálfgefnar víddir fyrir upplýsta reikninga eru tilgreindar leggur forritinu þær víddir og víddargildi til í hvert skipti sem einhver af þessum reikningum er notaður, til dæmis í bókarlínu. Það auðveldar bókun fyrir notandann þar sem sjálfkrafa er fyllt inn í víddarreiti. Hinsvegar er hægt að breyta víddargildunum sem kerfið leggur til, t.d. á bókarlínu.

Síðan **Sjálfgefnar víddir-á margar línur** inniheldur eftirfarandi reiti:

|Svæði|Description|
|-----|-----------|  
|**Víddarkóti**|Sýnir allar víddir sem hafa verið skilgreindar sem sjálfgefnar víddir fyrir einn eða fleiri auðkenndan reikning. Ef smellt er reitinn er hægt að skoða lista yfir öll tiltæk víddargildi. Ef valin er vídd eru víddirnar sem eru valdar skilgreindar sem sjálfgefnar víddir fyrir alla auðkennda reikninga.|
|**Gildiskóti víddar**|Sýnir annað hvort eitt víddargildi eða hugtakið (Misræmi). Ef víddargildi er í reitnum hafa allir upplýstir reitir sama sjálfgefna víddargildið í vídd. Ef hugtakið (Misræmi) er í reitnum hafa allir upplýstir reitir ekki sama sjálfgefna víddargildið í vídd. Ef smellt er reitinn er hægt að skoða lista yfir öll tiltæk víddargildi í vídd. Ef valið er víddargildi eru víddargildin sem eru valin skilgreind sem sjálfgefin víddargildi fyrir alla auðkennda reikninga.|
|**Virðisbókun**|Sýnir annað hvort ein virðisbókunarregla eða hugtakið (Misræmi). Ef virðisbókunarregla er í reitnum hafa allir auðkenndir reitir sömu sjálfgefnu virðisbókunarregluna í víddargildi. Ef hugtakið (Misræmi) er í reitnum hafa allir auðkenndir reitir ekki sömu sjálfgefnu virðisbókunarregluna í víddargildi. Ef reiturinn Virðisbókun er valinn er hægt að skoða lista yfir virðisbókunarreglur. Ef valin er virðisbókunarregla er hún notuð fyrir alla auðkennda reikninga.|

## <a name="use-dimensions"></a>Nota víddir
Í skjalinu eins og sölupöntun, er hægt að bæta við víddaupplýsingum fyrir bæði einstaka fylgiskjalslínu og skjalið sjálft. Til dæmis, í **Sölupöntun** síðunni getur þú slegið inn víddarmörk fyrir fyrstu tvær flýtivísanirnar á einstökum sölulínum og þú getur bætt við stærri víddarupplýsingum ef þú velur hnappinn **Víddir**.  

Ef þú vinnur í dagbók í staðinn geturðu bætt við víddargögn við færslu á sama hátt ef þú hefur sett upp flýtileiðarmörk sem reitir beint á blaðalínum.  

Hægt er að setja upp sjálfgefnar víddir fyrir reikninga eða reikningstegundir, svo að víddir og víddargildi eru fyllt út sjálfkrafa.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Að skoða altækar víddir á fjárhagsfærslusíðum

Altækar\-víddir eru alltaf skilgreindar og nefndar af fyrirtækjum. Til að sjá altæku víddirnar fyrir fyrirtæki skal opna síðuna **Uppsetning fjárhags**.  

Á fjárhagsfærslusíðu er hægt að sjá hvort altækar víddir hafi verið stofnaðar fyrir færslurnar. Altæku víddirnar tvær eru ólíkar hinum víddunum þar sem hægt er að nota þær sem afmarkanir hvar sem er innan [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á síðunni **Bókhaldslykill** skal velja aðgerðina **Fjárhagsfærslur**.  
3. Til að sjá aðeins viðeigandi færslur þarf að setja inn eina eða fleiri afmarkanir á síðuna.  
4. Til að sjá allar víddir fyrir færslu skal velja færsluna og svo aðgerðina **Víddir**.  

> [!NOTE]  
> Síðan **Bókfærsluvíddir** sýnir víddir einnar bókfærslu í einu. Þegar skrunað er um fjárhagsfærslurnar breytist innihald síðunnar **Fjárhagsfærsluvíddir** í samræmi við það.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]