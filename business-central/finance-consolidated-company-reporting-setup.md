---
title: Setja upp sameiningu fyrirtækis
description: Kynnið ykkur hvernig hægt er að skilgreina hvernig gögn frá mismunandi fyrirtækjum í Business Central eru skráð í samstæðufyrirtæki.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="set-up-company-consolidation"></a>Setja upp sameiningu fyrirtækis

Áður en hægt er að sameina fjárhagsfærslur tveggja eða fleiri fyrirtækja (dótturfyrirtæki) í samstæðufyrirtæki þarf að undirbúa bókhaldslyklana og samstæðufyrirtækið.  

Það eru tvær leiðir til að setja upp sameiningu, háð margbreytileika fyrirtækja þinna:

* Ef ekki er þörf á ítarlegum stillingum, t.d. með fyrirtæki sem aðeins er hluti af, er hægt að nota **uppsetningarleiðbeiningar fyrir samstæðu fyrirtækis** til að setja samsteypu á fljótlegan hátt upp. Leiðbeiningarnar aðstoða þig gegnum grunnatriðin.
* Ef þörf er á ítarlegri stillingum er hægt að setja upp samsteypufyrirtæki og fyrirtækiseiningar sjálfur.
  * Í hverri fyrirtækiseiningu skal tilgreina fjárhagsreikningana sem eiga að vera með í samstæðunni og umreikningsaðferð fyrir hvern reikning.
  * Í samstæðufyrirtækinu er sett upp fyrirtækiseiningarspjald fyrir hvert fyrirtæki sem á að hafa með í samstæðunni. Á spjaldinu eru upplýsingar eins og dagsetningar reikningsárs fyrirtækiseiningarinnar og prósenta hvers reiknings sem á að hafa með í samstæðunni.

## <a name="simple-consolidation-setup"></a>Einföld uppsetning sameiningar

Ef samsteypan er einfaldvirk, til dæmis vegna þess að fyrirtækiseiningin að öllu leyti á að steypa **saman, hjálpar samsteypa fyrirtækisins** við eftirfarandi skref:

* Stofna nýtt samsteypufyrirtæki eða sameina fyrirtæki sem þegar hefur verið stofnað. Fyrirtækið ætti ekki að innihalda færslur.
* Forskoða niðurstöður. [!INCLUDE[prod_short](includes/prod_short.md)] staðfestir að hægt sé að flytja aðalgögn og færslur til samsteypufyrirtækis.

Fylgið eftirfarandi skrefum til að nota leiðbeiningar um uppsetningu með hjálp:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
2. Veljið **Vinnsla samsteypu** og ljúkið svo hverju skrefi í leiðsagnarforritinu Uppsetning samsteypufyrirtækis.

## <a name="advanced-consolidation-setup"></a>Ítarleg uppsetning sameiningar

Ef þörf er á fleiri ítarlegum stillingum fyrir samstæðuna, geturðu sett upp samstæðu handvirkt. Til dæmis ef um er að ræða fyrirtæki sem notandi á að hluta til eða fyrirtæki sem ekki á að taka með.  

### <a name="set-up-the-consolidated-company"></a>Setja upp fyrirtæki í samstæðu

Fyrst þarf að setja upp samstæðufyrirtækið. Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Til að fræðast meira um uppsetningu fyrirtækis er farið í [Undirbúning fyrir viðskipti](ui-get-ready-business.md).  

Eftirfarandi listi sýnir lykilþætti í samstæðufyrirtækinu.

1. Setja upp bókhaldslykil.

    Nánari upplýsingar um uppsetningu bókhaldslykils eru í [Uppsetning eða breytingu á bókhaldslykli](finance-setup-chart-accounts.md).  

    Bókhaldslyklar geta verið eins á milli fyrirtækiseiningar og samstæðufyrirtækis, eða samstæðufyrirtækið getur haft annan bókhaldslykil. Ef bókhaldslykill fyrirtækiseiningar er frábrugðinn bókhaldslykli samsteypufyrirtækis verður að varpa reikningunum á reikninga fyrirtækiseiningarinnar. Nánari upplýsingar eru í hlutanum [Undirbúa fjárhagsreikninga fyrir samsteypu](#glacc) .

2. Fyrirtækiseiningum bætt við.

    Til að steypa saman gögnum nokkurra fyrirtækja þarf að setja dótturfyrirtækin upp sem fyrirtækiseiningar og tilgreina hversu mikið af stöðu þeirra á að taka með. Nánari upplýsingar um fyrirtækiseiningar eru í hlutanum [Bæta við fyrirtækiseiningum](#busunit) .

3. Tilgreina gengi ef þörf krefur.

    Tilgreina gengi ef sameina á gögn fyrir fyrirtækiseiningar sem nota mismunandi gjaldmiðla. Gengin þrjú sem hægt er að nota eru **Meðalgengi (handvirkt)**, **Lokagengi** og **Síðasta lokagengi**. Til að fræðast meira um gengi er farið í hlutann [Tilgreina gengi fyrir samstæður](#exchrates) .

4. Sameina víddarupplýsingar og fjárhagsreikninga.

    Til að fræðast meira er farið í hlutann [Taka með eða útiloka víddir](#dim) .

### <a name="add-business-units"></a><a name="busunit"></a>Bæta við fyrirtækiseiningum

Í samsteypufyrirtækinu skal setja upp hvert fyrirtæki sem á að sameina gögn frá sem fyrirtækiseiningu. Áður en samsteypuskýrsla er keyrð og samsteypuskýrsla búin til er ráðlegt að sannreyna fjárhagsgögnin í hverri fyrirtækiseiningu.

Stór hluti uppsetningar fyrirtækiseiningarinnar er að tilgreina hvernig einingin deilir fjárhagsgögnum hennar með samsteypufyrirtækinu. Valkostir eru handvirkir og sjálfvirkir:

* Til að nota handvirkt ferli á [!INCLUDE [prod_short](includes/prod_short.md)] netinu og innanhúss er hægt að flytja út .xml skrá sem inniheldur fjárhagsfærslur einingarinnar. Síðan er skráin flutt inn í samsteypufyrirtækinu.
* Til að gera gagnaskipti sjálfvirk, til [!INCLUDE [prod_short](includes/prod_short.md)] að á netinu er hægt að nota API sem [!INCLUDE [prod_short](includes/prod_short.md)] veitir samnýtingu gagna í umhverfinu. Ef fyrirtækin eru í sama umhverfi er hægt að nota valkostinn **Gagnagrunnur** .

> [!NOTE]
> Valkosturinn API gerir einnig kleift að deila fjárhagsfærslum úr öðru [!INCLUDE [prod_short](includes/prod_short.md)] umhverfi. Ef nota á API-valkostinn verður notandinn sem grunnstillir samsteypuna að hafa heimild til að fá aðgang að fjárhagsfærslum. Til dæmis veita heimildarsafnin D365 Basic og D365 Read permission Sets aðgang.

#### <a name="set-up-business-unit-currencies"></a>Setja upp gjaldmiðla fyrirtækiseiningar

Þegar samsteypufyrirtæki eru keyrð fyrir fyrirtækiseiningar sem nota erlendan gjaldmiðil þarf að vekja sérstaka athygli á því gengi sem ýmsir hlutar vinnslunnar nota, og jafnvel fleiri svo að þegar samsteypu er endurkeyrð. Til að gera það skal nota síðuna **Setja upp gjaldmiðla fyrir fyrirtækiseiningu** til að fylgjast með genginu auðveldlega.

Síðan **Setja upp gjaldmiðla** fyrirtækiseiningar gefur þér síðustu taxta fyrir meðaltal, lokun og síðustu lokunargengi. Hægt er að fletta upp á genginu í gengistöflunni sem auðveldar staðfestingu á gengi. Hægt er að breyta gengi gildandi keyrslu með því að færa inn gildin eða afrita þau úr fyrri keyrslum. Til að afrita gengi er Valið úr fyrri samstæðu **valið**. Þessi síða er sérlega verðmæt þegar ætlunin er að endurkeyra fyrri samstæðu, þar sem nota þarf fyrri lokunarhraða. Þetta þarf til að endurmeta efnahagsvörur rétt. Síðan **Velja úr fyrri samsteypu** er einnig gagnleg ef bara á að skoða gengin sem voru notuð, til dæmis við úrræðaleit. Síðan er afmarkað við keyrslur sem innihéldu valda fyrirtækiseiningu.

Keyrslan Keyra samstæðu **er ræst** á **listasíðu fyrirtækiseiningar** . Einnig er hægt að finna síðuna **Setja upp gjaldmiðla** fyrirtækiseiningar með því að velja aðgerðina **Gengi** .

> [!NOTE]
> Gengisuppsetningarsíður fyrir meðaltal, lokun og síðustu lokunargengi sem eru tiltækar á spjaldinu **Fyrirtækiseining** verða afskrifaðar í síðari útgáfu. Þó er enn hægt að viðhalda þessu gengi ef fyrirtækiseiningar eru fluttar inn í gegnum skrár.

#### <a name="create-a-business-unit"></a>Stofna fyrirtækiseiningu

1. Skráðu þig inn samstæðufyrirtækið.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
3. Velja skal **Nýtt** og fylla síðan út nauðsynlega reiti á flýtiflipunum **Almennt** og **Fjárhagsreikningar** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Þegar reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út skaltu vera viss um að þú uppfyllir reglur GAAP hvað varðar fjárhagstímabil fyrirtækiseiningar gagnvart móðurfyrirtækinu.
4. Á flýtiflipanum **Gagnainnflutningur** í reitnum **Sjálfgefinn innflutningur** er tilgreint hvernig eigi að samnýta fjárhagsfærslur með samsteypufyrirtækinu:

   * Til að deila gögnum milli fyrirtækja í sama umhverfi skal velja **Gagnagrunnur**.
   * Til að deila gögnum milli fyrirtækja í mismunandi umhverfi skal velja **API** og fylla svo út reitinn **Endastöð** API.
        
        Til að sækja URL endastöðvar skal opna [!INCLUDE [prod_short](includes/prod_short.md)] síðu fyrirtækiseiningarfyrirtækisins **og velja uppsetningaraðgerðina**  **.**  
   * Til að flytja út .xml skrá og samnýta hana handvirkt er skrársnið **valið**.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Undirbúa fjárhagslykla fyrir sameiningu

Bókhaldslykill fyrirtækis sem á að sameina þarf að  tilgreina reikninga fyrir samsteypu. Fyrir hvern bókunarfjárhagsreikning í hverju fyrirtæki þarf að tilgreina fjárhagsreikning í samsteypufyrirtækinu til að færa stöðuna til. Með þessari vörpun er hægt að sameina fyrirtæki sem hafa mismunandi bókhaldslykla.

Ef bókhaldslyklar í fyrirtækjaeiningunni eru ekki þeir sömu og í samstæðufyrirtækinu er nauðsynlegt að búa til fjárhagslykla fyrir samlegðina. Þú getur tilgreint reikninga sem bóka á debet og kredit á, sem og þá aðferð sem nota skal við að umreikna gjaldmiðil í samstæðufyrirtækinu.

1. Í hverju fyrirtækiseiningu [!INCLUDE [prod_short](includes/prod_short.md)] skal ![velja Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Opnaðu kortið fyrir reikninginn og fylltu svo út í reitina á **Samstæða** flýtiflipanum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Ef reiturinn **Samstæðu-debetreikn.**  er ekki fylltur útog **Samstæðu-kreditreikn.**  [!INCLUDE [prod_short](includes/prod_short.md)] gert er ráð fyrir að þeim sé varpað á sömu reikninga í samsteypufyrirtækinu.

> [!TIP]
> Það gætu verið aðstæður þar sem ekki á að taka reikning með í sameiningu. Eigi til dæmis samstæðufyrirtækið að endurspegla aðeins efnahagsreikninga frá dótturfyrirtækjunum. Til að útiloka reikning frá samsteypu skal kveikja á **vífæra samstæðu** fyrir reikninginn.

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Tilgreina gengi gjaldmiðla fyrir samstæður

Ef fyrirtækjaeining notar annan gjaldmiðil en samstæðufyrirtækið, er nauðsynlegt að tiltaka hvaða aðferðir eru notaðar við útreikning gjaldmiðla á hverjum reikningi áður en þú steypir saman. Fyrir hvern fjárhagsreikning ákvarðar innihald reitsins **Umreikniaðferð samstæðunnar** hvaða gengi gjaldmiðla er notað. Í samstæðufyrirtækinu, á hverju spjaldi fyrirtækiseiningar, í reitnum **Gengistafla** gjaldmiðils, er tilgreint hvort samsteypufyrirtæki noti gengi gjaldmiðla frá fyrirtækiseiningunni eða samsteypufyrirtækinu. Ef notað er gengi gjaldmiðla frá samstæðufyrirtækinu er hægt að breyta gengi gjaldmiðla hjá fyrirtækiseiningunni. Fyrir fyrirtækiseiningu, ef **Gengistafla á spjaldi** fyrirtækjaeiningarinnar inniheldur **Staðbundið**, er hægt að breyta genginu af spjaldi fyrirtækjaeiningarinnar. Gengi er afritað af töflunni **Gengi** en það er hægt að breyta þeim áður en samruni á sér stað.

Í eftirfarandi töflu er gengisaðferðum sem hægt er að nota fyrir lykla lýst.

|Gengi | Dæmigerð notkun |
|---|---|
|Meðalgengi (handvirkt) | Þú reiknar handverk meðalgengi tímabilsins sem á að sameina. Reiknaðu meðaltalið annaðhvort sem reiknað meðaltal eða besta mat og tilgreindu niðurstöðurnar fyrir hverja fyrirtækiseiningu. Nota fyrir rekstrarreikning.|
|Lokagengi | Notað fyrir efnahagslykla.|
|Síðasta lokagengi | Gengið sem gilti á gengismarkaði á dagsetningunni sem verið er að undirbúa efnahagsreikning og rekstrarreikning fyrir. Gengið er fært inn fyrir hverja fyrirtækiseiningu. Nota fyrir efnahagsreikninga.|
|Ferill gengis | Gengið sem var í gildi þegar viðskiptin áttu sér stað.|
|Samsett gengi | Upphæðir gildandi tímabils eru umreiknaðar á meðalgengi og bætt við áður skráða stöðu í samstæðufyrirtækinu. Þessi aðferð er gjarnan notuð fyrir framlegðarreikninga. Á þessum reikningum eru upphæðir frá mismunandi tímabilum svo að í þeim eru upphæðir sem eru þýddar með mismunandi gengi.|
|Gengi eiginfjár | Þessi valkostur svipar til **samsettra valkosta**. Mismunur bókast á aðskilda fjárhagsreikninga.|

Til að tilgreina gengi fyrir fyrirtækiseiningu skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Fyrirtækiseiningalisti** skal velja fyrirtækiseininguna og velja svo aðgerðina **Gengi** .  
3. Á síðunni **Uppsetning fyrirtækiseiningar** skal fylla út reitina eins og þörf krefur. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Taka með eða útiloka víddir

Hægt er að sameina víddarupplýsingar sem og fjárhagsreikninga.

* Í víddunum er reiturinn **Kóti samstæðu tilgreindur** eða hann hafður auður.
  * Ef útiloka á vídd í samsteypunni er reiturinn Kóti samstæðu hafður **auður í víddinni og ekki er hægt að velja víddir í reitunum** Afrita víddir **í aðgerðum eða skýrslum samsteypu.** 
  * Til að hafa með víddarupplýsingar í sameiningunni skal skilja reitinn **Samstæðukóði** eftir auðan. Hins vegar virkar samsteypan eingöngu ef víddargildin í fyrirtækiseiningunni eru þau sömu og samsteypufyrirtækið.
  * Ef sameina á víddargildiskóta fyrirtækiseiningarinnar með öðrum víddargildiskóta í samsteypufyrirtækinu er reiturinn Kóti samstæðu fylltur **út** í víddunum.  
* Víddunum er bætt við fjárhagsreikningana.

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Útiloka fyrirtæki frá samstæðu

Ef ekki á að taka fyrirtækiseiningu með í samstæðunni er hægt að útiloka hana. Það er gert með því að fara á spjald fyrirtækiseiningarinnar og hreinsa gátreitinn **Sameina** .

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Taka fyrirtæki í eigu hluta í samstæðu

Ef notandi á aðeins hluta af fyrirtæki er hægt að taka prósentu af hverri færslu sem endurspeglar prósentuna sem notandi á. Ef fyrirtækið á til dæmis 70% af fyrirtækinu felur samsteypan $70 á reikningi fyrir $100. Ef tilgreina á prósentutölu fyrirtækisins sem notandi á er farið á spjald fyrirtækiseiningarinnar og prósentan færð inn í reitinn **Samsteypa %** .  

## <a name="see-also"></a>Sjá einnig

[Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
