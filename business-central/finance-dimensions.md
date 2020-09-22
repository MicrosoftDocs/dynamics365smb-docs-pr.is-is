---
title: Vinna með Víddir| Microsoft Docs
description: Nota skal víddir til að flokka færslur, til dæmis eftir deild eða verki, svo hægt sé að rekja og greina gögn auðveldlega.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/14/2020
ms.author: edupont
ms.openlocfilehash: 05c187adbe7a471a5ba2f240ad4e61e083aa0346
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786372"
---
# <a name="working-with-dimensions"></a>Unnið með víddir
Til að auðvelda greiningu á skjölum, svo sem sölupöntum, geturðu notað stærðir. Víddir eru eiginleikar og gildi sem flokkar færslur svo þú getir fylgst með og greina þær. Til dæmis má vísa til verkefnisins eða deildarinnar sem innganga kom frá.  

Til dæmis, í stað þess að setja upp sérstaka aðalbókarreikninga fyrir hverja deild og verkefni, getur þú notað stærðir. Þetta gefur mikið tækifæri til greininga án þess að búa til flókið kort af reikningum. Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).

Annað dæmi er að setja upp vídd sem kallast *Deild* og nota þá vídd þegar þú bókar söluskjöl. Þetta mun leyfa þér að nota viðskipti upplýsingaöflun tól til að sjá hvaða deild selt hvaða atriði.
Því fleiri stærðir sem þú notar, nákvæmari skýrslurnar sem þú getur byggt á viðskiptatengslunum þínum. Til dæmis getur einn sölutilgangur innihaldið upplýsingar um marga vídd, svo sem:  

* Reikningurinn sem vörusalan var sendur til  
* Þar sem hluturinn var seldur
* Hver seldi það
* Tegund viðskiptavina sem keypti hana  

## <a name="analyzing-by-dimensions"></a>Greining eftir víddum
Virkni víddarinnar gegnir mikilvægu hlutverki í viðskiptaupplýsingum, eins og t.d. þegar verið er að skilgreina greingaryfirlit. Nánari upplýsingar er að finna í [Greina gögn eftir víddum](bi-how-analyze-data-dimension.md).

> [!TIP]
> Hægt er að greina færslugögn út frá víddum á skjótan hátt með því að afmarka samtölur á bókhaldslyklum og færslum á öllum **Færslur** síður út frá víddum. Leitaðu að aðgerðinni **Stilla víddarafmörkun**.

## <a name="dimension-sets"></a>Víddasamstæður
Víddasamstæða er sérstök samsetning víddargilda. Er vistað sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Víddasamstæðan er auðkennd með algengum víddasamstæðukennum sem eru úthlutuð hverri víddasamstæðufærslu sem tilheyrir víddasamstæðunni.  

Þegar þú býrð til dagbókarlínu, skjalhaus eða skjalastiku, getur þú tilgreint samsetningu af víddarmörkum. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

## <a name="setting-up-dimensions"></a>Uppsetning vídda
Hægt er að skilgreina víddirnar og víddargildin til að flokka færslubókum og skjölum, t.d. sölupantanir og innkaupapantanir. Þú setur upp víddir á síðunni **Víddir**, þar sem búin er til ein lína fyrir hverja vídd, svo sem *Verkefni*, *Deild*, *Svæði*, og *Sölumaður*.

Þú setur einnig upp gildi fyrir víddir. Gildi gætu til dæmis verið deildirnar í fyrirtækinu. Hægt er að setja víddir upp í stigveldisröð, svipað og bókhaldslykilinn, svo að hægt verði að stigskipta gögnunum og taka saman milliniðurstöður. Hægt er að skilgreina eins margar víddir og víddargildi og þörf er á og allir í fyrirtækinu geta notað þau.

Þegar víddir og gildi eru sett upp, er hægt að skilgreina altækar víddir og flýtivísanir í víddir á síðunni **Uppsetning fjárhags** sem verður alltaf í boði til að velja sem reiti í færslubókar- og skjalalínum, án þess að þurfa fyrst að opna síðuna **Víddir**. Frekari upplýsingar eru í [Að setja upp altækar víddir og flýtivísanir í víddir](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Altækar víddir** eru notaðar sem afmarkanir, t.d. á skýrslur, runuvinnslur og XMLports. Hægt er að nota eingöngu tvær altækar víddir, svo veldu því víddir sem verða notaðar oft.
* **Flýtivísanir í víddir** eru tiltækar sem reitir í færslubókar- og fylgiskjalslínum. Hægt er að stofna allt að sex af þeim.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Til að setja upp sjálfgefnar víddir fyrir viðskiptavini, lánardrottna, og aðra reikninga
Hægt er að setja upp sjálfgefna vídd fyrir tiltekinn stakan reikning. Víddin verður afrituð í færslubókina eða fylgiskjalið þegar reikningsnúmerið er fært inn í línu, en hægt er að eyða eða breyta kóðanum í línunni ef það á við. Einnig er hægt að búa til vídd og krefjast þess að í henni þurfi að bóka færslu með ákveðinni tegund reiknings.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Víddir** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Víddir** skal velja viðkomandi vídd og svo **Sjálfg. vídd reikningsteg.** aðgerðina.  
4.  Fylla þarf út línu fyrir hverja nýja vídd sem skal setja upp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Ef gera á vídd að skyldu án þess að úthluta sjálfgildi á víddina er reiturinn **Víddargildiskóti** hafður auður og **Kóti tilskilinn** valið í reitnum **Virðisbókun**.  

> [!WARNING]  
>  Ef nota skal reikning í **Leiðrétta gengi** keyrslunni eða **Bóka birgðakostnað í fjárhagsbók** keyrslunni má ekki velja **tilskilinn kóða** eða **sama kóða**. Þessar keyrslur geta ekki notað víddarkóta.  

> [!NOTE]  
>  Ef tilgreina verður aðra vídd fyrir reikning en sjálfgefnu víddina sem fyrir er fyrir tegund reiknings verður að setja upp sjálfgefna vídd fyrir þann reikning. Sjálfgefna víddin fyrir þennan eina reikning kemur þá í stað sjálfgefnu víddarinnar fyrir tegund reiknings.  

### <a name="to-set-up-default-dimension-priorities"></a>Að setja upp sjálfgefinn víddarforgang  
Mismunandi tegundir reikninga, eins og til dæmis viðskiptamannsreikningur og vörureikningur, geta haft mismunandi sjálfgefnar víddir uppsettar. Þar af leiðandi getur forritið lagt til fleiri en eina sjálfgefna vídd fyrir hverja færslu. Til að forðast slíka árekstra er hægt að láta forgangsreglur gilda í hverju tilviki.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forgangur sjálfgefinnar víddar** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Sjálgefin forgangur vídda** í reitinn **Upprunakóði** er færður inn upprunakóði færslutöflunnar sem sjálfgefinn víddaforgangur gildir fyrir.  
3.  Fyllt er út lína fyrir hvern forgang sjálfgefinnar víddar sem á að setja upp fyrir valinn upprunakóta.
4.  Ferlið er endurtekið fyrir hvern upprunakóða þar sem á að setja upp sjálfgefinn víddarforgang.  

> [!IMPORTANT]  
>  Ef settar eru upp tvær töflur með sama forgangi fyrir sama upprunakóta velur [!INCLUDE[d365fin](includes/d365fin_md.md)] alltaf töfluna með lægsta kennið.  

### <a name="to-set-up-dimension-combinations"></a>Að setja upp samsettar víddir  
Til að forðast að bóka færslur með mótsagnarkenndum eða óviðkomandi víddum er hægt að loka eða takmarka tilteknar samsetningar tveggja vídda. Lokuð víddarsamsetning þýðir að ekki er hægt að bóka báðar víddir í sömu færslu sama hver víddargildin eru. Með takmarkaðri víddarsamsetningu er hægt að bóka báðar víddir í sömu færslu en aðeins með tilteknum víddargildasamsetningum.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Víddarsamsetningar** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Víddarsamsetningar** er smellt á reitinn fyrir samsetningu vídda og síðan valinn einn af eftirfarandi valkostum.  

    |Svæði|Description|
    |----------------------------------|---------------------------------------|  
    |**Engin takmörkun**|Engar hömlur eru í gildi fyrir þessa víddasamsetningu. Öll víddargildi eru leyfð.|  
    |**Takmarkað**|Þessi víddarsamsetning hefur ákveðnar hömlur sem fara eftir víddargildunum sem slegin eru inn. Skilgreina þarf takmarkanirnar á síðunni **Samsetning víddargilda** .|  
    |**Lokað**|Þessi víddarsamsetning er ekki leyfð.|  

3.  Ef valinn var kosturinn **Takmarkað** verður að skilgreina hvaða samsetningar víddargilda eru læstar. Það er gert með því að velja reitinn til þess að skilgreina víddarsamsetninguna.  
4.  Nú er valin samsetning víddargilda og **Lokað** slegið inn í reitinn. Óútfylltur reitur þýðir að samsetning víddargilda er leyfð. Þetta er endurtekið ef margar samsetningar eru lokaðar.  

> [!NOTE]  
>  Sömu víddir birtast í báðum röðum og dálkum og þess vegna birtast allar víddarsamsetningar tvisvar. [!INCLUDE[d365fin](includes/d365fin_md.md)] sýnir stillingarnar í báðum reitum sjálfvirkt. Ekki er hægt að velja neitt í reitunum úr vinstra horni uppi og niður því þeir reitir hafa sömu vídd í báðum röðum og dálkum.  
>   
>  Valinn kostur er ekki sýnilegur fyrr en farið er út úr reitnum.  
>   
>  Til að sýna nafn víddarinnar fremur en kótann er hægt að haka við reitinn **Sýna heiti dálks** .

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Að setja upp altækar víddir og flýtivísanir í víddir
Hægt er að nota altækar víddir og flýtivísanir í víddir sem síu hvar sem er í [!INCLUDE[d365fin](includes/d365fin_md.md)], þ.m.t. í skýrslum, runuvinnslum og greiningaryfirlitum. Alltaf er hægt að setja altækar víddir og flýtivísanir í víddir beint inn án þess að opna fyrst síðuna **Víddir**. Í færslubókar- og skjalalínum er hægt að velja altækar víddir og flýtivísanir í víddir í reit í línunni. Hægt er að setja upp tvær altækar víddir og átta flýtivísanir í víddir. Veldu víddirnar sem þú notar mest.

> [!Important]  
> Breyting á altækri vídd eða flýtivídd krefst þess að færslur sem bókaðar eru með vídd séu uppfærðar. Hægt er að framkvæma þetta verk með virkninni **Breyta altækum víddum** en það getur verið tímafrekt og getur haft áhrif á afköst og töflur kunna að vera læstar meðan á uppfærslunni stendur. Þess vegna skaltu velja altækar víddir og flýtivísanir í víddir vandlega svo þú þurfir ekki að breyta þeim seinna. <br /><br />
> Frekari upplýsingar er að finna í [Til að breyta altækri vídd](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Þegar þú bætir við eða breytir altækri vídd eða flýtivídd ertu sjálfkrafa skráður út og aftur inn svo nýja gildið er undirbúið til notkunar alls staðar í forritinu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsgrunnur** og veldu síðan tengda tengilinn.
2. Í flýtiflipanum **Víddir** skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Að breyta altækum víddum
Breyting á altækri vídd eða flýtivídd uppfærir allar færslur sem bókaðar eru með vídd. Þar sem þetta ferli kann að vera tímafrekt og getur haft áhrif á afköst eru tvær mismunandi stillingar til staðar til að aðlaga ferlið að stærð gagnagrunnsins.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsgrunnur** og veldu síðan tengda tengilinn.
2. Veldu aðgerðina **Breyta altækum víddum**.
3. Efst á síðunni skaltu velja einn af eftirfarandi valkostum til að skilgreina í hvaða stillingu runuvinnslan er keyrð.

    |Valkostur|Description|
    |-|-|
    |**Í röð**|(Sjálfgefið) Allri víddarbreytingunni er lokið í einni færslu þar sem allar færslur eru færðar í víddirnar sem þær höfðu áður en breytingin átti sér stað.<br /><br />Mælt er með þessum valkosti ef fyrirtækið inniheldur tiltölulega fáar færslur þar sem það tekur stystan tíma að ljúka. Ferlið læsir mörgum töflum og lokar fyrir aðra notendur þangað til það er gert. Athugaðu að í stórum gagnagrunnum er hugsanlega ekki hægt að ljúka þessu ferli í þessari stillingu. Í því tilfelli skaltu nota valkostinn **Samhliða**.|
    |**Samhliða**|(Veldu gátreitinn **Samhliða vinnsla**.) Víddarbreytingin er keyrð í mörgum bakgrunnskeyrslum og aðgerðinni er skipt niður í margar færslur.<br /><br />Mælt er með þessum valkosti fyrir stóra gagnagrunna eða fyrirtæki með margar færslur þar sem það tekur stystu stund að ljúka. Athugið að með þessari stillingu hefst uppfærslan ekki ef fleiri en ein gagnagrunnslota er virk.|  

4. Í reitunum **Altæk vídd 1 - Kóði** og/eða **Altæk vídd 2 - Kóði** skaltu slá inn nýju víddina/víddirnar. Núverandi víddir birtast gráar á bak við reitina.
5. Ef **Röð** var valið skaltu velja aðgerðina **Byrja**.
6. Ef þú hefur valið stillinguna **Samhliða** skaltu velja aðgerðina **Undirbúa**.

    Flipinn **Skráarfærslur** er fylltur út með upplýsingum um víddirnar sem verður breytt.
7. Skráðu þig út af [!INCLUDE[d365fin](includes/d365fin_md.md)] og skráðu þig svo aftur inn.
8. Veldu aðgerðina **Ræsa** til að hefja samhliða vinnslu víddarbreytinganna.

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
>   Til að setja upp stigveldi verða kóðarnir að vera í stafrófsröð. Þar á meðal eru kóðarnir fyrir víddargildin sem eru fengin í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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

## <a name="using-dimensions"></a>Notkun vídda
Í skjalinu eins og sölupöntun, er hægt að bæta við víddaupplýsingum fyrir bæði einstaka fylgiskjalslínu og skjalið sjálft. Til dæmis, í **Sölupöntun** síðunni getur þú slegið inn víddarmörk fyrir fyrstu tvær flýtivísanirnar á einstökum sölulínum og þú getur bætt við stærri víddarupplýsingum ef þú velur hnappinn **Víddir**.  

Ef þú vinnur í dagbók í staðinn geturðu bætt við víddargögn við færslu á sama hátt ef þú hefur sett upp flýtileiðarmörk sem reitir beint á blaðalínum.  

Hægt er að setja upp sjálfgefnar víddir fyrir reikninga eða reikningstegundir, svo að víddir og víddargildi eru fyllt út sjálfkrafa.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Að skoða altækar víddir á fjárhagsfærslusíðum  
Altækar\-víddir eru alltaf skilgreindar og nefndar af fyrirtækjum. Til að sjá altæku víddirnar fyrir fyrirtæki skal opna síðuna **Uppsetning fjárhags**.  

Á fjárhagsfærslusíðu er hægt að sjá hvort altækar víddir hafi verið stofnaðar fyrir færslurnar. Altæku víddirnar tvær eru ólíkar hinum víddunum þar sem hægt er að nota þær sem afmarkanir hvar sem er innan [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókhaldslykill** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Bókhaldslykill** skal velja aðgerðina **Fjárhagsfærslur**.  
3.  Til að sjá aðeins viðeigandi færslur þarf að setja inn eina eða fleiri afmarkanir á síðuna.  
4.  Til að sjá allar víddir fyrir færslu skal velja færsluna og svo aðgerðina **Víddir**.  

> [!NOTE]  
>  Síðan **Bókfærsluvíddir** sýnir víddir einnar bókfærslu í einu. Þegar skrunað er um fjárhagsfærslurnar breytist innihald síðunnar **Fjárhagsfærsluvíddir** í samræmi við það.

## <a name="troubleshooting-dimensions-errors"></a>Úrræðaleita víddarvillur
Þegar skjala- eða færslubókarlínur sem innihalda víddir eru bókaðar geta ýmsar villur komið upp sem venjulega tengjast rangri víddaruppsetningu eða úthlutun.

> [!NOTE]
> Í eftirfarandi lista yfir hugsanleg villuboð eru kóðarnir *%X* staðgenglar fyrir gagnabreyturnar sem raunverulegu skilaboðin munu innihalda í notendaviðmótinu, háð samhenginu. Til dæmis *%1 %2 er útilokað.* gæti birst í notendaviðmótinu sem „Víddarkóðinn SVÆÐI er útilokaður.“.  

|Gefa út|Villuboð|Möguleg lausn|
|-----|-------------|-----------------|
|Útilokuð vídd|%1 %2 er útilokað.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokuðu víddinni og afblokka hana.<br />-Fjarlægja línu víddasamstæðu fyrir útilokuðu víddina.|
|Eydd vídd|%1 %2 finnst ekki.|-Endurheimta vídd sem vantar.<br />-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með vídd sem vantar og bæta henni við.<br />-Fjarlægja línu víddasamstæðu fyrir vídd sem vantar.|
|Útilokað víddargildi|%1 %2 - %3 er útilokað.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokuðu víddargildi og afblokka það.<br />-Fjarlægja línu víddasamstæðu fyrir útilokaða víddargildið.|
|Eydd víddargildi|   %1 fyrir %2 vantar.|-Endurheimta víddargildi sem vantar.<br />-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með víddargildinu sem vantar og bæta því við.<br />-Fjarlægja línu víddasamstæðu fyrir víddargildið sem vantar.|
|Óheimilt víddargildi|Gerð víddargildis fyrir %1 %2 – %3 má ekki vera %4.|-Breyttu reitnum **Gerð víddargildis** á síðunni **Víddargildi** í **Staðlað** eða **Frá-tala**.<br />-Fjarlægja línu víddasamstæðu fyrir útilokaða víddargildið.|
|Útilokuð víddarsamsetning|Víddirnar %1 og %2 er ekki hægt að nota samtímis.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokuðu víddarsamsetningunni og afblokka hana.<br />-Breyta einni af línum heimildasamstæðu sem stangast á fyrir víddarsamsetninguna.|
|Útilokuð samsetning víddargildis|Víddarsamsetningarnar %1 - %2 og %3 - %4 er ekki hægt að nota samtímis.|-Finna óbókuð fylgiskjöl sem innihalda víddasamstæðuna með útilokaða víddargildissamsetningu og opnaðu fyrir hana.<br />-Breyta einni af línum heimildasamstæðu sem stangast á fyrir víddargildissamsetninguna.|
|Auður víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Kóði tilskilinn**|-Velja %1 fyrir %2 %3.<br />-Velja %1 fyrir %2 %3 fyrir %4 %5.|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn víddargildi sem er ekki autt fyrir víddina sem stangast á í víddasamstæðunni.|
|Rangur víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Sami kóði**|-Veldu %1 %2 fyrir %3 %4.<br />-Veldu %1 %2 fyrir %3 %4 fyrir %5 %6|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn nauðsynlegt víddargildi fyrir víddina sem stangast á í víddasamstæðunni.|
|Víddargildiskóði sem ekki er auður fyrir auða sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Sami kóði**|-%1 %2 verður að vera auður.<br />-%1 %2 verður að vera auður fyrir %3 %4.|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Færðu inn auðan víddargildiskóða fyrir víddina sem stangast á í víddasamstæðunni.|
|Óvæntur víddargildiskóði fyrir sjálfgefna vídd þar sem reiturinn **Virðisbókun** inniheldur **Enginn kóði**|-%1 %2 má ekki nefna.<br />-%1 %2 má ekki nefna fyrir %3 %4|-Breyta reitnum **Virðisbókun** á síðunni **Sjálfgefin vídd**.<br />-Fjarlægja línuna sem stangast á úr víddasamstæðunni.|

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
