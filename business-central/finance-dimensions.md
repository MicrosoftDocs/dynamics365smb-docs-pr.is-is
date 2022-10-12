---
title: Unnið með víddir til að rekja og greina gögn á auðveldan hátt
description: Víddir eru notaðar til að flokka færslur, svo sem eftir deild eða verki, þannig að auðvelt sé að rekja og greina gögn sem hjálpa til við að gera góðar viðskiptaákvarðanir.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.search.form: 408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253
ms.date: 08/24/2022
ms.author: edupont
ms.openlocfilehash: dcb7ad52194729888ddefda16eeb99ef0423122a
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605624"
---
# <a name="work-with-dimensions"></a>Vinna með víddir

Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá.  

Svo að í stað þess að setja upp aðgreinda fjárhagslykla fyrir hverja deild og verk, er hægt að nota víddir sem grundvöll fyrir greiningu og forðast að stofna flókinn bókhaldslykil. Frekari upplýsingar á [viðskiptagreind](bi.md).

Annað dæmi er að setja upp vídd sem heitir *deild* og nota svo víddina þegar söluskjöl eru bókuð. Með þessum hætti er hægt að nota verkfæri viðskiptagreindar til að sjá hvaða deild seldi vörurnar. Því fleiri víddir sem þú notar, þeim mun ítarlegri eru skýrslurnar sem þú grunnaðir um viðskiptaákvarðanir á. Í raun getur ein sölufærsla innihaldið upplýsingar úr mörgum víddum, svo sem:  

* Lykillinn sem Vörusalan var bókaður í.  
* Þar sem varan var seld.
* Sem seldi það.
* Hvaða viðskiptavinur keypti hann.

## <a name="analyzing-by-dimensions"></a>Greint eftir víddum

Víddir gegna mikilvægu hlutverki í viðskiptagreind, eins og t.d. þegar greiningaryfirlit eru skilgreind. Frekari upplýsingar er að greina í [greiningu gagna eftir víddum](bi-how-analyze-data-dimension.md).

> [!TIP]
> Fljótleg leið til að greina færslugögn eftir víddum er að nota **aðgerðina stilla víddarafmörkun** til að sía samtölur eftir víddum í bókhaldslyklum og á síðum færslna.

> [!NOTE]
> Greiningaryfirlit nota oft gögn úr víddum. Ef röng vídd hefur verið notuð í bókuðum fjárhagsfærslum er hægt að leiðrétta víddargildin og uppfæra greiningaryfirlitin. Þetta hjálpar til við að halda fjárhagslegum skýrslum og greiningum nákvæmar. Frekari upplýsingar eru í [úrræðaleit og Leiðréttingarvíddum](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets"></a>Víddasamstæður

Víddasamstæða er sérstök samsetning víddargilda. Þær eru geymdar sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Að auki, hverja víddasamstæðu, og víddasamstæðufærslu innan þess, er auðkennd með sameiginlegu VÍDDASAMSTÆÐUAUÐKENNI.  

Þegar þú býrð til dagbókarlínu, skjalhaus eða skjalastiku, getur þú tilgreint samsetningu af víddarmörkum. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

## <a name="setting-up-dimensions"></a>Setja upp víddir

Hægt er að skilgreina víddir og víddargildi til að flokka færslubækur og skjöl, svo sem sölupantana og innkaupapantanir. Þú setur upp víddir á síðunni **Víddir**, þar sem búin er til ein lína fyrir hverja vídd, svo sem *Verkefni*, *Deild*, *Svæði*, og *Sölumaður*.

Þú setur einnig upp gildi fyrir víddir. Segjum að gildin gildi fyrir deildir fyrirtækisins. Hægt er að setja upp víddargildin í stigveldisskipan sem svipar til bókhaldslykilsins. Það þýðir að gögn geta verið brotin niður í ýmis stig kornvirkni, og undirmengi víddargilda. Hægt er að skilgreina eins margar víddir og víddargildi og þörf er á og allir í fyrirtækinu geta notað þau.

Þegar víddir og gildi eru sett upp er hægt að skilgreina altækar og flýtivísanir í víddir á **uppsetningarsíðu** fjárhags. Þessar víddir eru síðan alltaf tiltækar til að velja sem reiti í færslubók og fylgiskjalslínum og færslum án þess að opna **víddarsíðuna** fyrst. Frekari upplýsingar eru [í hlutanum til að setja upp altækar og flýtivísanir í víddir](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Altækar víddir** eru notaðar sem afmarkanir, t.d. á skýrslur, runuvinnslur og XMLports. Hægt er að nota eingöngu tvær altækar víddir, svo veldu því víddir sem verða notaðar oft.
* **Flýtivísanir í víddir** eru tiltækar sem reitir í færslubókum, skjalalínum og fjárhagsfærslum. Hægt er að stofna allt að átta af þeim.  

> [!NOTE]
> Eftir að þú hefur notað nýja vídd í hvaða færslu sem er, svo sem línu eða nýja færslu, getur þú ekki eytt víddinni, jafnvel þótt þú birtir ekki færsluna. Það er vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] það býr strax til víddasett fyrir línuna eða færsluna. Frekari upplýsingar eru [í kaflanum Víddasamstæður](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Til að setja upp sjálfgefnar víddir fyrir viðskiptavini, lánardrottna, og aðra reikninga

Hægt er að setja upp sjálfgefna vídd fyrir tiltekinn stakan reikning. Víddin er afrituð í færslubókina eða skjalið þegar reikningsnúmerið er fært í línu, en hægt er að eyða eða breyta kóta í línunni ef við á. Einnig er hægt að krefjast víddar fyrir bókun færslu í sérstaka gerð lykils.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **víddir** og veljið síðan tengda tengilinn.  
2. **Á síðunni víddir** skal velja viðeigandi vídd og velja **síðan lykilgerð sjálfgefinnar sundaðgerðar**.  
3. Lína er fyllt út fyrir hverja nýja sjálfgefna vídd sem á að setja upp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Ef gera á kröfu um vídd en ekki á að úthluta sjálfgildi á víddina er **reiturinn Kóti** víddargildis hafður auður og síðan valinn **Kóti sem er áskilinn** í **reitnum gildisbókun**.  

> [!WARNING]  
> Ef lykill er notaður í **keyrslunni Leiðrétta gengi** eða **Bóka birgðakostnaður** þarf ekki að velja **áskilið** eða **sama kóta**. Þessar keyrslur geta ekki notað víddarkóta.  

> [!NOTE]  
> Ef lykill verður að hafa aðra vídd en sjálfgefna vídd sem úthlutað er á lykilgerðinni verður að setja upp nýja sjálfgefna vídd fyrir lykilinn. Sjálfgefna víddin fyrir þennan reikning kemur þá í stað sjálfgefnu víddarinnar fyrir tegund reiknings.  

### <a name="to-set-up-default-dimension-priorities"></a>Að setja upp sjálfgefinn víddarforgang

Mismunandi reikningstegundir, svo sem viðskiptavinalykil og vörureikningur, geta haft mismunandi sjálfgefnar víddir. Þar af leiðandi gæti færsla verið með fleiri en eina tillögu að sjálfgefinni vídd. Til að forðast slíka árekstra er hægt að láta forgangsreglur gilda í hverju tilviki.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **sjálfgefna Víddarforgangsröðun**, velja síðan tengda tengilinn.  
2. **Á síðunni kóti** sjálfgefinnar víddar **, í** reitnum Upprunakóti, er ritaður upprunakóti færslutöflunni sem sjálfgefin Forgangur víddar gildir um.  
3. Fyllt er út í línu fyrir hvern forgang sjálfgefins víddar sem óskað er eftir fyrir valinn upprunakóta.
4. Þetta er endurtekið fyrir hvern upprunakóta sem setja á upp sjálfgefinn víddarforgang.  

> [!IMPORTANT]  
> Ef tvær töflur eru settar upp með sama forgangi fyrir sama upprunakóta [!INCLUDE[prod_short](includes/prod_short.md)] velur alltaf töfluna með lægsta TÖFLUKENNI.  

### <a name="to-set-up-dimension-combinations"></a>Að setja upp samsettar víddir

Til að forðast að bóka færslur með mótsagnarkenndum eða óviðkomandi víddum er hægt að loka eða takmarka tilteknar samsetningar tveggja vídda. Læst víddarsamsetning þýðir að ekki er hægt að bóka báðar víddir í sömu færslunni óháð því hver víddargildin eru. Takmörkuð víddarsamsetning er á móti þýðir að hægt er að bóka báðar víddir í sömu færslu en þó aðeins fyrir tilteknar samsetningar víddargilda.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Víddasamsetningar** og velja síðan viðkomandi tengil.  
2. **Á síðunni víddarsamsetningar** er valinn reiturinn Víddasamsetning sem óskað er eftir.  

    |Svæði|Lýsing|
    |----------------------------------|---------------------------------------|  
    |**Engin takmörkun**|Engar hömlur eru í gildi fyrir þessa víddasamsetningu. Öll víddargildi eru leyfð.|  
    |**Takmarkað**|Þessi víddarsamsetning hefur ákveðnar hömlur sem fara eftir víddargildunum sem slegin eru inn. Skilgreina þarf takmarkanirnar á síðunni **Samsetning víddargilda** .|  
    |**Lokað**|Þessi víddarsamsetning er ekki leyfð.|  

3. Ef valinn var kosturinn **Takmarkað** verður að skilgreina hvaða samsetningar víddargilda eru læstar. Það er gert með því að velja svæðið til að skilgreina samsetningu víddargildis.  
4. Nú er valin samsetning víddargilda og **Lokað** slegið inn í reitinn. Autt svæði merkir að samsetning víddargildis er heimil. Þetta er endurtekið ef margar samsetningar eru lokaðar.  

> [!NOTE]  
> Sömu víddir birtast í báðum röðum og dálkum sem þýðir að allar víddarsamsetningar birtast tvisvar sinnum. [!INCLUDE[prod_short](includes/prod_short.md)] sýnir stillingarnar í báðum reitum sjálfvirkt. Ekki er hægt að velja neitt í svæðunum úr efra horninu vinstra megin og niður því þau svæði hafa sömu víddina í báðum röðum og dálkum.  
>
> Valinn kostur er ekki sýnilegur fyrr en farið er út úr reitnum.  
>
> Til að sýna nafn víddarinnar fremur en kótann er hægt að haka við reitinn **Sýna heiti dálks** .

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Að setja upp altækar víddir og flýtivísanir í víddir

Hægt er að nota altækar víddir og flýtivísanir í víddir sem síur í [!INCLUDE[prod_short](includes/prod_short.md)], þ.m.t. í skýrslum, runuvinnslum, fjárhagsfærslusíðum og greiningaryfirlitum. Hægt er að setja inn altækar víddir og flýtivísanir beint án þess að **opna fyrst síðuna víddir**. Í færslubókar- og skjalalínum er hægt að velja altækar víddir og flýtivísanir í víddir í reit í línunni. Hægt er að setja upp tvær altækar víddir og átta flýtivísanir í víddir. Veldu víddirnar sem þú notar mest.

> [!IMPORTANT]
> Ef altækrar eða Flýtivídd er breytt þurfa allar færslur sem bókaðar eru með víddinni að vera uppfærðar. Til að breyta altækrar víddar er hægt að nota aðgerðina breyta altækum **víddum**, en sem getur verið tímafrek, getur það haft áhrif á afköst og hægt er að læsa töflum meðan á uppfærslu stendur. Gakktu úr skugga um að þú veljir altækar og flýtivísanir víddir vandlega svo þú verður ekki að breyta þeim síðar. Til að breyta flýtivísun í vídd skal nota aðgerðina **Breyta víddum**.
>
> Frekari upplýsingar eru [í hlutanum til að breyta altækum víddum](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Þegar altækrar eða flýtivíddar er bætt við eða breytt er sjálfkrafa skrifað yfir og aftur í svo nýja gildið sé tilbúið til notkunar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **fjárhagsskipulag**, velja síðan tengda tengilinn.
2. Í flýtiflipanum **Víddir** skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Að breyta altækum víddum

Þegar altækum víddum eða flýtivísun er breytt eru allar færslur sem bókaðar eru með víddinni uppfærðar. Þar sem þetta ferli kann að vera tímafrekt og getur haft áhrif á afköst eru tvær mismunandi stillingar til staðar til að aðlaga ferlið að stærð gagnagrunnsins.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Breyta altækum víddum**.
3. Efst á síðunni skal velja eina af eftirfarandi hamum til að keyra runuvinnsluna.

    |Valkostur|Lýsing|
    |-|-|
    |**Í röð**|(Sjálfgefið) Breytingin er gerð í einni færslu sem snýr við öllum færslum í víddirnar sem voru áður en breytingin átti sér stað.<br /><br />Mælt er með þessum valkosti ef fyrirtækið er með tiltölulega fáar bókaðar færslur, í því tilfelli tekur keyrslan styprutíma að ljúka. Ferlið læsir mörgum töflum og lokar fyrir aðra notendur þangað til það er gert. Hafa þarf í huga að með stórum gagnagrunnum gæti ferlið ekki verið fullklárað í þessum ham. Í því tilfelli skaltu nota valkostinn **Samhliða**.|
    |**Samhliða**|Víddarbreytingin gerist í mörgum bakgrunnskeyrslum og aðgerðinni er skipt niður í margar færslur. Til að nota þennan valkost þarf að kveikja á **Hliðstæðri vinnslu**. <br /><br />Við mælum með þessum valkosti fyrir stóra gagnagrunna eða fyrirtæki með mikið af bókuðum færslum þar sem því lýkur í styka tíma. Athugið að í þessum ham fer uppfærsluferlið ekki í gang ef fleiri en ein virk gagnagrunnslota er í gangi.|  

4. Í reitunum **Altæk vídd 1 - Kóði** og/eða **Altæk vídd 2 - Kóði** skaltu slá inn nýju víddina/víddirnar. Núverandi víddir birtast gráar á bak við reitina.
5. Gerið eitt af eftirfarandi, allt eftir stillingunni:
    * Í stillingunni **Eftir röð** skal velja aðgerðina **Byrja**.
    * Í stillingunni **Hliðsætt** skal velja aðgerðina **Undirbúa**.

    **Flipinn kladdafærslur** er fylltur út með upplýsingum um víddir sem á að breyta.
6. Skrá út af [!INCLUDE[prod_short](includes/prod_short.md)], skrá síðan aftur inn.
7. **Velja upphafs** Aðgerðir til að hefja samhliða vinnslu víddarbreytinganna.

### <a name="example-of-dimension-setup"></a>Dæmi um víddaruppsetningu

Segjum að fyrirtækið vilji rekja færslur sem byggðar eru á stjórnskipulagi og landfræðilegum stöðum. Til að gera það eru settar upp tvær víddir á **víddunum** síða:

* **SVÆÐI**  
* **DEILD**  

| Kóði | Name | Texti kóta | Texti afmörkunar |
| --- | --- | --- | --- |
| SVÆÐI |Svæði |Svæðiskóði |Svæðisafmörkun |
| DEILD |Deild |Deildarkóði |Afmörkun deildar |

Fyrir **svæði** skal bæta við eftirfarandi víddargildum:

| Kóði | Nafn | Tegund víddargildis |
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

Fyrir tvö helstu landsvæðin, N- og S-Ameríku og Evrópu, skal bæta við undirflokkum fyrir svæði með því að draga inn víddargildin. Þetta gerir þér kleift að tilkynna um sölu eða kostnað á svæðum og fá samtölur fyrir stærri landsvæðin. Einnig var hægt að velja að nota lönd, svæði, sýslur eða borgir sem víddargildi, eftir því hvaða fyrirtæki á í viðskiptum.

> [!NOTE]  
> Til að setja upp stigveldi verða kóðarnir að vera í stafrófsröð. Þar á meðal eru kótar víddargildanna sem eru í [!INCLUDE[prod_short](includes/prod_short.md)].  

Fyrir **deild** skal bæta við eftirfarandi víddargildum:

| Kóði | Nafn | Tegund víddargildis |
| --- | --- | --- |
| STJÓRN |Stjórnun |Staðlað |
| FRAML |Framleiðsla |Staðlað |
| SALA |Sölur |Staðlað |

Með þessari uppsetningu er hægt að bæta við tveimur víddum sem altækum víddunum tveimur á **uppsetningarsíðu** fjárhags. Það þýðir að hægt er að nota svæði og DEILD sem afmarkanir fyrir fjárhagsfærslur, sem og á öllum skýrslum. Báðar altæku víddirnar eru líka sjálfkrafa tiltækar til notkunar á færslulínum og skjalahausum sem flýtivísanir í víddir.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Yfirlit yfir víddir sem eru notaðar í mörgum tímum

**Sjálfgefnar víddir-mörg** síða Tilgreinir hvernig Flokkur lykla notar víddir og víddargildi. Hægt er að setja þetta upp með því að auðkenna marga lykla og tilgreina síðan sjálfgefnar víddir og víddargildi fyrir þau. Eftir það er forritið stungið upp á þessum víddum og víddargildum í hvert sinn sem einn af þessum lyklum er notaður eins og í færslubókarlínu. Það auðveldar bókun fyrir notandann þar sem sjálfkrafa er fyllt inn í víddarreiti. Athugaðu þó að lagt er til að hægt sé að breyta víddargildunum í, til dæmis, í færslubókarlínu.

Síðan **Sjálfgefnar víddir-á margar línur** inniheldur eftirfarandi reiti:

|Svæði|Lýsing|
|-----|-----------|  
|**Víddarkóti**|Sýnir allar víddir sem eru skilgreindar sem sjálfgefnar víddir á einn eða fleiri auðkennda lykla. Með því að velja þennan reit er hægt að skoða lista yfir allar tiltækar víddir. Ef vídd er valin er víddin skilgreind sem sjálfgefin vídd fyrir alla upplýsta lykla.|
|**Gildiskóti víddar**|Sýnir annað hvort eitt víddargildi eða hugtakið (Misræmi). Ef víddargildi er í reitnum hafa allir upplýstir reitir sama sjálfgefna víddargildið í vídd. Ef hugtakið (misræmi) er sýnt í svæðinu hafa ekki allir upplýstir lyklar sama sjálfgefna víddargildið fyrir vídd. Þegar valið er **reitinn Kóti víddar** er hægt að skoða lista yfir öll tiltæk víddargildi fyrir vídd. Ef valið er víddargildi verður það skilgreint sem sjálfgefið víddargildi fyrir alla upplýsta reikninga.|
|**Virðisbókun**|Sýnir annað hvort ein virðisbókunarregla eða hugtakið (Misræmi). Ef virðisbókunarregla er í reitnum hafa allir auðkenndir reitir sömu sjálfgefnu virðisbókunarregluna í víddargildi. Ef hugtakið (misræmi) er sýnt í svæðinu verða ekki allir upplýstir reikningar með sömu gildisbókunarreglu fyrir víddargildi. Þegar reiturinn gildisbókun **er valin** er hægt að skoða lista yfir gildisbókunarreglur fyrir vídd. Ef gildisbókunarregla er valin verður hún jöfnuð við alla upplýsta lykla.|

## <a name="use-dimensions"></a>Nota víddir

Í skjalinu eins og sölupöntun, er hægt að bæta við víddaupplýsingum fyrir bæði einstaka fylgiskjalslínu og skjalið sjálft. Svo á **sölupöntunarsíðunni**, þá gætir þú fært víddargildi fyrir fyrstu tvær flýtivísanir víddanna í einstakar sölulínur, síðan bætast við fleiri víddarupplýsingar ef valin **er hnappurinn víddir**.  

Ef þú vinnur í dagbók í staðinn geturðu bætt við víddargögn við færslu á sama hátt ef þú hefur sett upp flýtileiðarmörk sem reitir beint á blaðalínum.  

Einnig er hægt að setja upp sjálfgefnar víddir fyrir lykla eða gerðir reikninga svo víddir og víddargildi séu sjálfkrafa fyllt út.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Að skoða altækar víddir á fjárhagsfærslusíðum

Altækar víddir eru alltaf skilgreindar sem fyrirtæki og fyrirtæki sem nefnast. Til að sjá altæku víddirnar fyrir fyrirtæki skal opna síðuna **Uppsetning fjárhags**.

Á fjárhagsfærslusíðu er hægt að sjá hvort altækar víddir hafi verið stofnaðar fyrir færslurnar. Altækar víddir tvær eru frábrugðnar öðrum víddum þínum því hægt er að nota þær sem afmarkanir hvar sem er í [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **bókhaldslykil** og veljið síðan tengda tengilinn.  
2. Á síðunni **Bókhaldslykill** skal velja aðgerðina **Fjárhagsfærslur**.  
3. Til að sjá aðeins færslur sem skipta máli er sett ein eða fleiri afmarkanir á síðuna.  
4. Til að sjá allar víddir færslunnar skaltu velja færsluna og velja **svo aðgerðina víddir**.  

> [!NOTE]  
> **Síðan birgðafærsla** birtir víddir einnar færslu í einu. Þú munt sjá eftir því sem þú flettir í gegnum færslurnar, efnið á **víddarsíðunni** breytist í samræmi við það.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
