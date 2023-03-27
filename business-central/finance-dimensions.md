---
title: Unnið með víddir til að rekja og greina gögn
description: 'Nota skal víddir til að flokka færslur, svo sem eftir deild eða verki, þannig að auðvelt sé að rekja og greina gögn sem hjálpa til við að gera góðar viðskiptaákvarðanir.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# Vinna með víddir

Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá.  

Í stað þess að setja upp sérstaka aðalbókarreikninga fyrir hverja deild og verkefni, getur þú notað víddir sem grundvöll fyrir greiningu og forðast að þurfa að stofna flókna bókhaldslykla. Frekari upplýsingar er að finna í [Viðskiptagreind](bi.md).

Annað dæmi er að setja upp vídd sem kallast *Deild* og síða nota þá vídd þegar þú bókar söluskjöl. Þannig geturðu notað verkfæri viðskiptagreindar til að sjá hvaða deild seldi hvaða vöru. Því fleiri víddir sem þú notar, því nákvæmari verða skýrslurnar sem þú byggir viðskiptaákvarðanir þínar á. Í raun getur ein sölufærsla innihaldið upplýsingar frá mörgum víddum, t.d.:  

* Reikningurinn sem vörusalan var sendur til.  
* Þar sem hluturinn var seldur.
* Hver seldi það.
* Hvaða viðskiptavinur keypti hann.

## Greining eftir víddum

Víddir gegna mikilvægu hlutverki í viðskiptagreind, eins og t.d. þegar greiningaryfirlit eru skilgreind. Frekari upplýsingar eru á [Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)

> [!TIP]
> Fljótleg leið til að greina færslugögn eftir víddum er að nota aðgerðina **Velja víddarafmörkun** til að sía samtölur eftir víddum í bókhaldslyklinum og á síðum fyrir færslur.

> [!NOTE]
> Greiningaryfirlit nota oft gögn úr víddum. Ef kemur í ljós að röng vídd hafi verið notuð í bókuðum fjárhagsfærslum er hægt að leiðrétta víddargildin og uppfæra greiningaryfirlitin. Það mun hjálpa til við að halda fjárhagsskýrslum og greiningum nákvæmum. Frekari upplýsingar er að finna í [Úrræðaleit og víddarleiðréttingar](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Víddasamstæður

Víddasamstæða er sérstök samsetning víddargilda. Hún er vistuð sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Auk þess er hver víddasamstæða og víddasamstæðufærsla í henni skilgreind eftir almennu auðkenni víddasamstæðu.  

Þegar þú býrð til dagbókarlínu, skjalhaus eða skjalastiku, getur þú tilgreint samsetningu af víddarmörkum. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

## Uppsetning vídda

Hægt er að skilgreina víddir og víddargildi til að flokka færslubækur og skjöl, t.d. sölupantanir og innkaupapantanir. Þú setur upp víddir á síðunni **Víddir**, þar sem búin er til ein lína fyrir hverja vídd, svo sem *Verkefni*, *Deild*, *Svæði*, og *Sölumaður*.

Þú setur einnig upp gildi fyrir víddir. Gefum okkur að gildi tákni deildir fyrirtækisins. Hægt er að setja víddargildi upp í stigveldisskipan líkt og bókhaldslykillinn. Það þýðir að hægt er að skipta gögnunum niður í mismunandi stig og taka saman undirsöfn af víddargildum. Hægt er að skilgreina eins margar víddir og víddargildi og þörf er á og allir í fyrirtækinu geta notað þau.

Þegar víddir og gildi eru sett upp er hægt að skilgreina altækar víddir og flýtivíddir á síðunni **Fjárhagsgrunnur**. Þessar víddir eru síðan alltaf í boði til að velja sem reiti í færslubókar- og skjalalínum og fjárhagsfærslum án þess að opna fyrst síðuna **Víddir**. Frekari upplýsingar er að finna í hlutanum [Að setja upp altækar víddir og flýtivíddir](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Altækar víddir** eru notaðar sem afmarkanir, t.d. á skýrslur, runuvinnslur og XMLports. Hægt er að nota eingöngu tvær altækar víddir, svo veldu því víddir sem verða notaðar oft.
* **Flýtivísanir í víddir** eru tiltækar sem reitir í færslubókum, skjalalínum og fjárhagsfærslum. Hægt er að stofna allt að átta af þeim.  

> [!NOTE]
> Eftir að þú hefur notað nýja vídd í hvaða færslu sem er, svo sem línu eða nýja færslu, getur þú ekki eytt víddinni, jafnvel þótt þú birtir ekki færsluna. Það er vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] það býr strax til víddasett fyrir línuna eða færsluna. Frekari upplýsingar er að finna í hlutanum [Víddarsamstæður](finance-dimensions.md#dimension-sets).

### Til að setja upp sjálfgefnar víddir fyrir viðskiptavini, lánardrottna, og aðra reikninga

Hægt er að setja upp sjálfgefna vídd fyrir tiltekinn stakan reikning. Víddin er afrituð í færslubókina eða skjalið þegar reikningsnúmerið er fært inn í línu, en hægt er að eyða eða breyta kóðanum í línunni ef það á við. Einnig er hægt að krefjast víddar til að bóka færslu á tiltekna reikningstegund. > 

> [!NOTE]
> Sjálfgefin víddarforgangur opnar fyrir atburðarás í sölu og innkaupum sem þú vilt hugsanlega að greiða sérstaka athygli fyrir. Þegar sjálfgefin víddarforgangur er notaður í sölu-og innkaupaskjölum  [!INCLUDE [prod_short](includes/prod_short.md)]  telur alltaf víddin í hausnum sem kemur frá viðskiptavini eða lánardrottni. Þetta gildir um víddir sem eru stilltar handvirkt eða sjálfgefið og á það sérstaklega við þegar sjálfgefnar víddir eru notaðar á birgðageymslum og í vörum en ekki á viðskiptavini eða lánardrottna.
>
> **T.d**.
>
> Þú hefur atburðarás með eftirfarandi víddarstillingum:
>
> * Viðskiptamaður án sjálfgefinna vídda
> * Vara með ADM sem víddargildið fyrir víddina DEILD
> * Birgðageymsla með PROD sem víddargildið DEILDAVÍDD
> * Forgangur sjálfgefinnar víddar er stilltur sem viðskiptamaður > vara > Birgðageymsla
>
> Þegar nýtt skjal er stofnað í þessu dæmi eru víddir notaðar sem hér segir:
>
> * Ef nýtt skjal er stofnað og staðsetning bætt við er sjálfgefna gildið fyrir nýju línurnar framl. Þegar línum með vörum er  [!INCLUDE [prod_short](includes/prod_short.md)]  bætt við verður að halda framl þar sem hún kemur úr haus skjalsins.
>
> * Ef búið er til nýtt skjal og bætt við vörum sem hafa ADM-víddargildið og síðan er tilgreind staðsetning í haus skjalsins er  [!INCLUDE [prod_short](includes/prod_short.md)]  spurt hvort skrifa eigi yfir línurnar sem til eru vegna þess að árekstur verður.
>
> Við mælum með að þú prófraar uppsetningu sjálfgefinna vídda, forgangsröðunar og svo pöntunina þar sem gögn eru færð inn í fylgiskjöl.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Víddir** og velja síðan viðkomandi tengil.  
2. Á síðunni **Víddir** skal velja viðkomandi vídd og síðan velja aðgerðina **Sjálfg. vídd reikningstegundar**.  
3. Fylltu út línu fyrir hverja nýja sjálfgefna vídd sem á að setja upp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Ef þú vilt gera kröfu um vídd en vilt ekki úthluta sjálfgefnu gildi á víddina skaltu reitinn **Víddargildiskóði** eftir auðan, síðan velja **Kóði áskilinn** í reitnum **Gildisbókun**.  

> [!WARNING]  
> Ef nota skal reikning í runuvinnslunni **Leiðrétta gengi** eða **Bóka birgðakostnað í fjárhag** skal ekki velja **Kóði áskilinn** eða **Sami kóði**. Þessar keyrslur geta ekki notað víddarkóta.  

> [!NOTE]  
> Ef tilgreina verður aðra vídd fyrir reikning en sjálfgefnu víddina sem úthlutuð er á reikningstegundina þarf að setja upp nýja sjálfgefna vídd fyrir reikninginn. Sjálfgefna víddin fyrir þennan reikning kemur þá í stað sjálfgefnu víddarinnar fyrir tegund reiknings.  

### Að setja upp sjálfgefinn víddarforgang

Mismunandi tegundir reikninga, eins og viðskiptamannareikningur og vörureikningur, geta verið með mismunandi sjálfgefnar víddir. Þar af leiðandi gæti færsla verið með meira en eina sjálfgefna vídd sem stungið er upp á. Til að forðast slíka árekstra er hægt að láta forgangsreglur gilda í hverju tilviki.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forgangur sjálfgefinnar víddar**, velja síðan viðkomandi tengil.  
2. Á síðunni **Forgangur sjálfgefinnar víddar**, í reitinn **Upprunakóði** skal færa inn upprunakóði fyrir færslutöfluna þar sem forgangur sjálfgefinnar víddar verður notaður.  
3. Fylltu út lína fyrir hvern forgang sjálfgefinnar víddar sem á að setja upp fyrir valinn upprunakóða.
4. Endurtaktu ferlið fyrir hvern upprunakóða sem á að setja upp forgang sjálfgefinnar víddar fyrir.  

> [!IMPORTANT]  
> Ef settar eru upp tvær töflur með sama forgangi fyrir sama upprunakóða velur [!INCLUDE[prod_short](includes/prod_short.md)] alltaf töfluna með lægsta töflukenninu.  

### Að setja upp samsettar víddir

Til að forðast að bóka færslur með mótsagnarkenndum eða óviðkomandi víddum er hægt að loka eða takmarka tilteknar samsetningar tveggja vídda. Útilokuð víddarsamsetning þýðir að ekki er hægt að bóka báðar víddir í sömu færsluna sama hver víddargildin eru. Á hinn bóginn þýðir takmörkuð víddarsamsetning að hægt að bóka báðar víddirnar í sömu færsluna en aðeins fyrir ákveðnar samsetningar víddargilda.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Víddasamsetningar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Víddarsamsetningar** skal velja reit víddarsamsetningar sem þú vilt úr eftirfarandi valkostum.  

    |Svæði|Lýsing|
    |----------------------------------|---------------------------------------|  
    |**Engin takmörkun**|Engar hömlur eru í gildi fyrir þessa víddasamsetningu. Öll víddargildi eru leyfð.|  
    |**Takmarkað**|Þessi víddarsamsetning hefur ákveðnar hömlur sem fara eftir víddargildunum sem slegin eru inn. Skilgreina þarf takmarkanirnar á síðunni **Samsetning víddargilda** .|  
    |**Lokað**|Þessi víddarsamsetning er ekki leyfð.|  

3. Ef valinn var kosturinn **Takmarkað** verður að skilgreina hvaða samsetningar víddargilda eru læstar. Það er gert með því að velja reitinn til þess að skilgreina samsetningu víddargildisins.  
4. Nú er valin samsetning víddargilda og **Lokað** slegið inn í reitinn. Auður reitur þýðir að samsetning víddargildis er leyfð. Þetta er endurtekið ef margar samsetningar eru lokaðar.  

> [!NOTE]  
> Sömu víddir birtast í báðum línum og dálkum, sem þýðir að allar víddarsamsetningar birtast tvisvar sinnum. [!INCLUDE[prod_short](includes/prod_short.md)] sýnir stillingarnar í báðum reitum sjálfvirkt. Ekki er hægt að velja neitt í reitunum í vinstra horni uppi og niðri því þeir reitir eru með sömu víddina í báðum línum og dálkum.  
>
> Valinn kostur er ekki sýnilegur fyrr en farið er út úr reitnum.  
>
> Til að sýna nafn víddarinnar fremur en kótann er hægt að haka við reitinn **Sýna heiti dálks** .

### Að setja upp altækar víddir og flýtivísanir í víddir

Hægt er að nota altækar víddir og flýtivísanir í víddir sem síur í [!INCLUDE[prod_short](includes/prod_short.md)], þ.m.t. í skýrslum, runuvinnslum, fjárhagsfærslusíðum og greiningaryfirlitum. Alltaf er hægt að setja altækar víddir og flýtivíddir beint inn án þess að opna fyrst síðuna **Víddir**. Í færslubókar- og skjalalínum er hægt að velja altækar víddir og flýtivísanir í víddir í reit í línunni. Hægt er að setja upp tvær altækar víddir og átta flýtivísanir í víddir. Veldu víddirnar sem þú notar mest.

> [!IMPORTANT]
> Breyting á altækri vídd eða flýtivídd krefst þess að færslur sem bókaðar eru með vídd séu uppfærðar. Til að breyta altækri vídd er hægt að nota aðgerðina **Breyta altækum víddum**, en það getur verið tímafrekt, getur haft áhrif á afköst og töflur kunna að vera læstar meðan á uppfærslunni stendur. Gakktu úr skugga um að þú veljir altækar víddir og flýtivíddir vandlega svo þú þurfir ekki að breyta þeim síðar. Til að breyta flýtivísun í vídd skal nota aðgerðina **Breyta víddum**.
>
> Fáðu frekari upplýsingar í hlutanum [Að breyta altækum víddum](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Þegar þú bætir við eða breytir altækri vídd eða flýtivídd ertu sjálfkrafa skráður út og aftur inn svo nýja gildið er undirbúið til notkunar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags**, velja síðan viðkomandi tengil.
2. Í flýtiflipanum **Víddir** skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Að breyta altækum víddum

Þegar altækri vídd eða flýtivídd er breytt eru allar færslur sem bókaðar eru með þeirri vídd uppfærðar. Þar sem þetta ferli kann að vera tímafrekt og getur haft áhrif á afköst eru tvær mismunandi stillingar til staðar til að aðlaga ferlið að stærð gagnagrunnsins.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Breyta altækum víddum**.
3. Veldu efst á síðunni eina af eftirfarandi tveimur stillingum til að keyra runuvinnsluna.

    |Valkostur|Lýsing|
    |-|-|
    |**Í röð**|(Sjálfgefið) Breytingin er gerð í einni færslu sem snýr við öllum færslum í víddirnar sem voru áður en breytingin átti sér stað.<br /><br />Mælt er með þessum valkosti ef fyrirtækið er með tiltölulega fáar færslur, en þá tekur runuvinnslan stystan tíma að klárast. Ferlið læsir mörgum töflum og lokar fyrir aðra notendur þangað til það er gert. Athugaðu að með stóra gagnagrunna er ekki víst að ferlið klárist í þessari stillingu. Í því tilfelli skaltu nota valkostinn **Samhliða**.|
    |**Samhliða**|Víddarbreytingin gerist í mörgum bakgrunnskeyrslum og aðgerðinni er skipt niður í margar færslur. Til að nota þennan valkost þarf að kveikja á **Hliðstæðri vinnslu**. <br /><br />Mælt er með þessum valkosti fyrir stóra gagnagrunna eða fyrirtæki með margar bókaðar færslur vegna þess að það tekur stystan tíma að klárast. Athugaðu að í þessari stillingu hefst uppfærsluferlið ekki ef fleiri en ein gagnagrunnslota er virk.|  

4. Í reitunum **Altæk vídd 1 - Kóði** og/eða **Altæk vídd 2 - Kóði** skaltu slá inn nýju víddina/víddirnar. Núverandi víddir birtast gráar á bak við reitina.
5. Gerið eitt af eftirfarandi, allt eftir stillingunni:
    * Í stillingunni **Eftir röð** skal velja aðgerðina **Byrja**.
    * Í stillingunni **Hliðsætt** skal velja aðgerðina **Undirbúa**.

    Flipinn **Kladdafærslur** er fullur af upplýsingum um víddirnar sem á að breyta.
6. Skráðu þig úr [!INCLUDE[prod_short](includes/prod_short.md)] og inn aftur.
7. Veldu aðgerðina **Byrja** til að hefja hliðstæða vinnslu víddarbreytinganna.

### Dæmi um uppsetningu víddar

Segjum að fyrirtækið vilji rekja færslur út frá skipulagseiningum og landfræðilegum staðsetningum. Til þess að gera það er hægt að setja upp tvær víddir á síðunni **Víddir**:

* **SVÆÐI**  
* **DEILD**  

| Kóði | Name | Texti kóta | Texti afmörkunar |
| --- | --- | --- | --- |
| SVÆÐI |Svæði |Svæðiskóði |Svæðisafmörkun |
| DEILD |Deild |Deildarkóði |Afmörkun deildar |

Fyrir **SVÆÐI** skal bæta við eftirfarandi víddargildum:

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

Fyrir tvö helstu landsvæðin, N- og S-Ameríku og Evrópu, skal bæta við undirflokkum fyrir svæði með því að draga inn víddargildin. Þetta gera þér kleift að tilkynna um sölu eða kostnað á svæðum og fá samtölur fyrir stærri landfræðileg svæði. Einnig er hægt að velja að nota lönd, svæði, sýslur eða borgir sem víddargildi eftir því hver gerð fyrirtækisins er.

> [!NOTE]  
> Til að setja upp stigveldi verða kóðarnir að vera í stafrófsröð. Þetta á við um kóða víddargildanna sem gefin eru upp í [!INCLUDE[prod_short](includes/prod_short.md)].  

Fyrir **DEILD** skal bæta við eftirfarandi víddargildum:

| Kóði | Nafn | Tegund víddargildis |
| --- | --- | --- |
| STJÓRN |Stjórnun |Staðlað |
| FRAML |Framleiðsla |Staðlað |
| SALA |Sölur |Staðlað |

Með þessari uppsetningu geturðu bætt við þínum tveimur víddum sem tveimur altækum víddum á síðunni **Fjárhagsgrunnur**. Þetta þýðir að hægt er að nota SVÆÐI og DEILD sem síur fyrir fjárhagsfærslur og einnig á allar skýrslur. Báðar altæku víddirnar eru líka sjálfkrafa tiltækar til notkunar á færslulínum og skjalahausum sem flýtivísanir í víddir.

## Fá yfirlit um víddir sem eru notaðar oftar en einu sinni

Síðan **Sjálfgefnar víddir á margar línur** tilgreinir hvernig flokkur reikninga notar víddir og víddargildi. Hægt er að setja þetta upp með því að auðkenna marga reikninga og tilgreina síðan sjálfgefnar víddir og víddargildi fyrir þá. Eftir það leggur forritið til þessar víddir og víddargildi í hvert skipti sem einn af þessum reikningum er notaður, eins og í færslubókarlínu. Það auðveldar bókun fyrir notandann þar sem sjálfkrafa er fyllt inn í víddarreiti. Athugaðu hins vegar að hægt að breyta víddargildunum sem stungið er upp á, t.d. færslubókarlínu.

Síðan **Sjálfgefnar víddir-á margar línur** inniheldur eftirfarandi reiti:

|Svæði|Lýsing|
|-----|-----------|  
|**Víddarkóti**|Sýnir allar víddir sem eru skilgreindar sem sjálfgefnar víddir fyrir einn eða fleiri auðkennda reikninga. Ef þessi reitur er valinn er hægt að sjá lista yfir tiltækar víddir. Ef vídd er valin verður sú vídd skilgreind sem sjálfgefin vídd fyrir alla auðkennda reikninga.|
|**Gildiskóti víddar**|Sýnir annað hvort eitt víddargildi eða hugtakið (Misræmi). Ef víddargildi er í reitnum hafa allir upplýstir reitir sama sjálfgefna víddargildið í vídd. Ef hugtakið (misræmi) er sýnt í reitnum, þá eru ekki allir auðkenndir reikningar með sama sjálfgefna víddargildið fyrir vídd. Þegar reiturinn **Víddarkóði** er valinn sérðu lista yfir öll tiltæk víddargildi fyrir vídd. Ef valið er víddargildi verður það skilgreint sem sjálfgefið víddargildi fyrir alla auðkennda reikninga.|
|**Virðisbókun**|Sýnir annað hvort ein virðisbókunarregla eða hugtakið (Misræmi). Ef virðisbókunarregla er í reitnum hafa allir auðkenndir reitir sömu sjálfgefnu virðisbókunarregluna í víddargildi. Ef hugtakið (misræmi) er sýnt í reitnum, þá eru ekki allir auðkenndir reikningar með sömu reglu virðisbókunar fyrir víddargildi. Þegar reiturinn **Virðisbókun** er valinn birtist listi yfir reglur virðisbókunar fyrir vídd. Ef valin er virðisbókunarregla er hún notuð á alla auðkennda reikninga.|

## Nota víddir

Í skjalinu eins og sölupöntun, er hægt að bæta við víddaupplýsingum fyrir bæði einstaka fylgiskjalslínu og skjalið sjálft. Þannig að á síðunni **Sölupöntun** geturðu slegið inn víddargildi fyrir fyrstu tvær flýtivíddirnar á einstökum sölulínum, síðan bætt við meiri víddarupplýsingum ef þú velur hnappinn **Víddir**.  

Ef þú vinnur í dagbók í staðinn geturðu bætt við víddargögn við færslu á sama hátt ef þú hefur sett upp flýtileiðarmörk sem reitir beint á blaðalínum.  

Einnig er hægt að setja upp sjálfgefnar víddir fyrir reikninga eða reikningstegundir þannig að víddir og víddargildi eru fyllt út sjálfkrafa.

### Að skoða altækar víddir á fjárhagsfærslusíðum

Altækar víddir eru alltaf skilgreindar og nefndar af fyrirtækjum. Til að sjá altæku víddirnar fyrir fyrirtæki skal opna síðuna **Uppsetning fjárhags**.

Á fjárhagsfærslusíðu er hægt að sjá hvort altækar víddir hafi verið stofnaðar fyrir færslurnar. Altæku víddirnar tvær eru ólíkar hinum víddunum því hægt er að nota þær sem síur hvar sem er í [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill**, velja síðan viðkomandi tengil.  
2. Á síðunni **Bókhaldslykill** skal velja aðgerðina **Fjárhagsfærslur**.  
3. Til að sjá aðeins færslur sem eiga við þarf að setja inn eina eða fleiri síur á síðuna.  
4. Til að sjá allar víddir fyrir færslu skal velja færsluna og svo velja aðgerðina **Víddir**.  

> [!NOTE]  
> Síðan **Fjárhagsfærsluvíddir** sýnir víddirnar, eina fjárhagsfærslu í einu. Þegar þú flettir í gegnum fjárhagsfærslurnar sérðu efni síðunnar **Fjárhagsfærsluvíddir** breytast í samræmi við það.

## Sjá tengda [Microsoft þjálfun](/training/modules/dimensions-dynamics-365-business-central/index)

## Sjá einnig .

[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
