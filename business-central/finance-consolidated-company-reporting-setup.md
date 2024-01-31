---
title: Setja upp sameiningu fyrirtækis
description: Kynnið ykkur hvernig hægt er að skilgreina hvernig gögn frá mismunandi fyrirtækjum í Business Central eru skráð í samstæðufyrirtæki.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Setja upp sameiningu fyrirtækis

Áður en hægt er að sameina fjárhagsfærslur tveggja eða fleiri félaga (dótturfyrirtækja) í samstæðufyrirtæki, þarf að útbúa bókhaldslykla og samstæðufyrirtækið.  

Það eru tvær leiðir til að setja upp sameiningu, háð margbreytileika fyrirtækja þinna:

* Ef ekki er þörf á ítarlegum stillingum, eins og þar með talið fyrirtæki sem aðeins er hluti af, er hægt að nota  **Uppsetningarleiðbeiningar fyrir samstæðu fyrirtækisins**  til að setja fljótt upp samstæðu. Leiðbeiningarnar aðstoða þig gegnum grunnatriðin.
* Ef þörf er á ítarlegri stillingum er hægt að setja upp samstæðufyrirtækið og fyrirtækiseiningunum sjálfum.
  * Í hverri fyrirtækiseiningu eru tilgreindir fjárhagslyklyklar sem taka á með í samstæðunni og þýðingaraðferðin fyrir hvern lykil.
  * Í samstæðufyrirtækinu er sett upp fyrirtækiseinakort fyrir hvert fyrirtæki sem á að hafa með í samstæðunni. Fyrirtækiseiningin inniheldur upplýsingar eins og dagsetningar fjárhagsára fyrirtækiseiningarinnar og prósentu hvers lykils sem á að taka með í samstæðuna.

## Einföld uppsetning sameiningar

Ef sameiningin er einföld, til dæmis vegna þess að þú átt að eiga fyrirtækiseiningar til að styrkja,  **·**  mun samstæðuhandbókin hjálpa þér með eftirfarandi skrefum:

* Stofnið nýtt samstæðufyrirtæki eða Sameinið fyrirtæki sem stofnað hefur verið til. Fyrirtækið ætti ekki að innihalda færslur.
* Forskoða niðurstöður. [!INCLUDE[prod_short](includes/prod_short.md)] staðfestir að hægt sé að flytja aðalgögnin og færslurnar í samstæðufyrirtækið.

Fylgið eftirfarandi skrefum til að nota leiðbeiningar um uppsetningu með hjálp:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
2. Veljið  **ferli sameiningar** og Ljúkið síðan hverju skrefi í uppsetningarleiðbeiningum fyrir aðstoðarfyrirtæki.

## Ítarleg uppsetning sameiningar

Ef þörf er á fleiri ítarlegum stillingum fyrir samstæðuna, geturðu sett upp samstæðu handvirkt. Til dæmis ef þú ert með fyrirtæki sem þú átt að hluta til, eða þú átt fyrirtæki sem þú vilt ekki vera með.  

### Setja upp fyrirtæki í samstæðu

Fyrst þarf að setja upp samstæðufyrirtækið. Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Til að fræðast meira um uppsetningu fyrirtækis er farið að  [verða klárt fyrir rekstur fyrirtækja](ui-get-ready-business.md).  

Eftirfarandi listi sýnir lykilþætti í samstæðufyrirtækinu.

1. Setja upp bókhaldslykil.

    Til að fá frekari upplýsingar um uppsetningu bókhaldslykils er farið í að  [Setja upp eða breyta bókhaldslyklum](finance-setup-chart-accounts.md).  

    Bókhaldslyklar geta verið eins á milli fyrirtækiseiningar og samstæðufyrirtækis, eða samstæðufyrirtækið getur haft annan bókhaldslykil. Ef Bókhaldslykill fyrirtækiseiningar er frábrugðinn samstæðureikningsskilum verður að varpa reikningunum á reikningana í fyrirtækiseininu. Til að fá frekari upplýsingar er farið í  [undirbúa fjárhagslykla fyrir sameiningu](#glacc) .

2. Bæta við fyrirtækiseiningum.

    Til að sameina gögn nokkurra fyrirtækja þarf að setja dótturfélögin upp sem fyrirtækiseiningar og tilgreina hversu mikið af stöðu þeirra á að taka með. Til að fræðast meira um fyrirtækiseiningar þarf að fara í  [hlutann bæta við fyrirtækiseiningum](#busunit) .

3. Tilgreina gengi, ef þörf krefur.

    Tilgreina gengi ef þú munt sameina gögn fyrir fyrirtækiseiningar sem nota mismunandi gjaldmiðla. Þau þrjú gengi sem hægt er að nota eru  **Meðalgengi (handvirkt)**,  **lokshlutfall** og  **Síðasta lokunarhlutfall**. Frekari upplýsingar um gengi er að fá með því  [að fara í kaflann tilgreina gengi fyrir samstæður](#exchrates) .

4. Upplýsingar um sameiningarvíddir og fjárhagsreikninga.

    Til að fá frekari upplýsingar er farið í  [hlutann hafa eða útiloka](#dim) .

### <a name="busunit"></a>Bæta við fyrirtækiseiningum

Í samstæðufyrirtækinu skal setja upp hvert fyrirtæki sem á að sameina gögn úr sem fyrirtækiseiningu. Áður en sameining er keyrð og samstæðuskýrsla er mynduð er góð hugmynd að sannreyna fjárhagsgögnin í hverri fyrirtækiseiningu.

Stór hluti af því að setja upp fyrirtækiseiningu er að tilgreina hvernig einingin deilir fjárhagslegum gögnum með samstæðufyrirtækinu. Til eru handvirkir og sjálfvirkir Valkostir:

* Ef nota á handvirka vinnslu, fyrir  [!INCLUDE [prod_short](includes/prod_short.md)]  netið og innanhúss, er hægt að flytja út. XML-skrá sem inniheldur fjárhagsfærslur einingarinnar. Síðan er skráin flutt inn í samstæðufyrirtækið.
* Til að gera gagnaskiptin sjálfvirka, fyrir  [!INCLUDE [prod_short](includes/prod_short.md)]  netið er hægt að nota API sem  [!INCLUDE [prod_short](includes/prod_short.md)]  gefur til að samnýta gögn yfir umhverfi. Ef fyrirtækin eru í sama umhverfi er hægt að  **nota gagnagrunnmöguleikann** .

> [!NOTE]
> Valkosturinn API gerir einnig kleift að samnýta fjárhagsfærslur úr öðru  [!INCLUDE [prod_short](includes/prod_short.md)]  umhverfi. Ef nota á API-valkostinn verður notandinn sem samskipar heimild fyrir aðgang að fjárhagsfærslum. Sem dæmi má nefna að D365 grunn-og D365 lestrarleyfi veita aðgang.

1. Skráðu þig inn samstæðufyrirtækið.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
3. Velja  **skal nýtt** og fylla síðan út nauðsynlega reiti á  **flipunum Almennt**  og  **fjárhagsreikningar** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Þegar reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út skaltu vera viss um að þú uppfyllir reglur GAAP hvað varðar fjárhagstímabil fyrirtækiseiningar gagnvart móðurfyrirtækinu.
4.  **Á flýtiflipa gagnainnflutnings**, í  **reitnum Sjálfgefinn innflutningur**, skal tilgreina hvernig á að samnýta fjárhagsfærslur með samstæðufyrirtækinu:

   * Til að samnýta gögn á milli fyrirtækja í sama umhverfi skal velja  **gagnagrunn**.
   * Ef samnýta á gögn á milli fyrirtækja í mismunandi umhverfi er API  **valið** og reiturinn endastöð  **í**  API fylltur út.
        
        Til að fá VEFSLÓÐ endastöðvar, í fyrirtækiseiningar-  [!INCLUDE [prod_short](includes/prod_short.md)] síðunni, skal opna  **síðuna Fyrirtækiseining**  og velja  **uppsetningaraðgerðina** . 
   * Ef flytja á út. XML-skrá og samnýta hana handvirkt skal velja  **skrársnið**.

### <a name="glacc"></a>Undirbúa fjárhagslykla fyrir sameiningu

Bókhaldslykill fyrirtækis sem á að sameina þarf að  tilgreina reikninga fyrir samsteypu. Fyrir hvern bókun fjárhagslykils í hverju fyrirtæki þarf að tilgreina fjárhaginn í samstæðufyrirtækinu til að færa stöðuna í. Þessi vörpun gerir kleift að sameina fyrirtæki sem hafa mismunandi bókhaldslykla.

Ef bókhaldslyklar í fyrirtækjaeiningunni eru ekki þeir sömu og í samstæðufyrirtækinu er nauðsynlegt að búa til fjárhagslykla fyrir samlegðina. Þú getur tilgreint reikninga sem bóka á debet og kredit á, sem og þá aðferð sem nota skal við að umreikna gjaldmiðil í samstæðufyrirtækinu.

1. Í hverri fyrirtækiseiningu  [!INCLUDE [prod_short](includes/prod_short.md)] skal velja þá  ![ljósaperu sem opnar aðgerðina segja.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Opnaðu kortið fyrir reikninginn og fylltu svo út í reitina á **Samstæða** flýtiflipanum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="exchrates"></a>Tilgreina gengi gjaldmiðla fyrir samstæður

Ef fyrirtækjaeining notar annan gjaldmiðil en samstæðufyrirtækið, er nauðsynlegt að tiltaka hvaða aðferðir eru notaðar við útreikning gjaldmiðla á hverjum reikningi áður en þú steypir saman. Fyrir hvern fjárhagsreikning ákvarðar innihald reitsins **Umreikniaðferð samstæðunnar** hvaða gengi gjaldmiðla er notað. Í samstæðufyrirtækinu, á hverju spjaldi fyrirtækiseiningarinnar í **Töflunni Gengi gjaldmiðla** er tilgreint hvort samstæðan noti gengi gjaldmiðla frá fyrirtækiseiningunni eða samstæðufyrirtækinu. Ef notað er gengi gjaldmiðla frá samstæðufyrirtækinu er hægt að breyta gengi gjaldmiðla hjá fyrirtækiseiningunni. Fyrir fyrirtækiseiningu, ef **Gengistafla á spjaldi** fyrirtækjaeiningarinnar inniheldur **Staðbundið**, er hægt að breyta genginu af spjaldi fyrirtækjaeiningarinnar. Gengi er afritað af töflunni **Gengi** en það er hægt að breyta þeim áður en samruni á sér stað.

Í eftirfarandi töflu er gengisaðferðum sem hægt er að nota fyrir lykla lýst.

|Gengi | Dæmigerð notkun |
|---|---|
|Meðalgengi (handvirkt) | Þú reiknar handverk meðalgengi tímabilsins sem á að sameina. Reiknaðu meðaltalið annaðhvort sem reiknað meðaltal eða besta mat og tilgreindu niðurstöðurnar fyrir hverja fyrirtækiseiningu. Nota til rekstrarreikninga skv.|
|Lokagengi | Notað fyrir efnahagslykla.|
|Síðasta lokagengi | Gengið sem gilti á gengismarkaði á dagsetningunni sem verið er að undirbúa efnahagsreikning og rekstrarreikning fyrir. Gengið er fært inn fyrir hverja fyrirtækiseiningu. Nota við efnahagslykla.|
|Ferill gengis | Gengið sem var í gildi þegar viðskiptin áttu sér stað.|
|Samsett gengi | Upphæðir gildandi tímabils eru umreiknaðar á meðalgengi og bætt við áður skráða stöðu í samstæðufyrirtækinu. Yfirleitt er þessi aðferð notuð fyrir varðveislulykla. Í þessum reikningum eru upphæðir frá mismunandi tímabilum þannig að þær innihalda upphæðir sem eru þýddar á mismunandi gengi.|
|Gengi eiginfjár | Þessi valkostur er svipaður  **og samsettur**. Munum eftir mismunandi fjárhagslykli.|

Til að tilgreina gengi gjaldmiðla fyrir fyrirtækiseiningar, skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Listi yfir fyrirtækiseiningar** skal velja fyrirtækiseininguna, og síðan **Meðalgengi (handvirkt)** aðgerðina.  
3. Á síðunni **Breyta gengi gjaldmiðils** hefur efni í reitnum **Viðmiðunargengi** verið afritað úr töflunni **Gengi gjaldmiðils** en hægt er að breyta því. Lokaðu síðunni.  
4. Veldu aðgerðina **Lokagengi**.  
5. Í reitnum **Upphæð viðmiðunargengis** skal færa inn gengið.

### <a name="dim"></a>Taka með eða útiloka víddir

Hægt er að sameina víddarupplýsingar sem og fjárhagsreikninga.

* Í víddunum er reiturinn Kóti  **samsteypu tilgreindur**  eða hann hafður auður.
  * Til að útiloka vídd í samstæðu er reiturinn samstæðukóti  **hafður**  auður í víddinni og ekki velja víddir í  **reitunum afrita víddir**  í neinum samlegðaraðgerðum eða skýrslum.
  * Til að hafa með víddarupplýsingar í sameiningunni skal skilja reitinn **Samstæðukóði** eftir auðan. Hins vegar virkar samsteypan eingöngu ef víddargildin í fyrirtækiseiningunni eru þau sömu og samsteypufyrirtækið.
  * Ef sameina á víddargildiskóta í fyrirtækiseiningu með annan víddargildiskóta í samstæðufyrirtækinu skal fylla út í  **reitinn sameiningarkóti**  á víddunum.  
* Bæta víddunum við fjárhagsreikningana.

### <a name="exclude"></a>Útiloka fyrirtæki frá samstæðu

Ef ekki á að vera rekstrareining í samstæðunni er hægt að útiloka hana. Það er gert með því að fara á Fyrirtækiseiningin og hreinsa  **gátreitinn sameina** .

### <a name="include"></a> Eru að hluta til í eigu fyrirtækja í samstæðu

Ef þú átt aðeins hluti í fyrirtæki getur þú innihaldið prósentu af hverri færslu sem endurspeglar þá prósentu sem þú átt. Ef þú átt t.d. 70% af fyrirtækinu, þá inniheldur Samstæða $70 reikning fyrir $100. Til að tilgreina hlutfall fyrirtækisins sem þú átt, farið á Fyrirtækiseiningin og prósentan fært inn í  **reitinn samstæður%** .  

## Sjá einnig

[Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]