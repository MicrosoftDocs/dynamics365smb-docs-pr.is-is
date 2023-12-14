---
title: Skilgreina hvernig rafræn gagnaskipti fara fram
description: 'Skilgreindu hvernig Business Central skiptir á gögnum með ytri skrám eins og rafrænum skjölum, bankagögnum, vörulistaatriðum og fleiru.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# Setja upp skilgreiningar gagnaskipta

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að skiptast á gögnum í tilteknum töflum með gögnum á ytri skrám. Til að senda og taka á móti rafrænum skjölum skal til dæmis flytja inn og út bankagögn eða önnur gögn eins og launaskrá og vörulistaatriði. Frekari upplýsingar í [Rafræn gagnaskipti](across-data-exchange.md).  

Til að búa til gagnaskiptaskilgreiningu fyrir gagnaskrá eða straum er hægt að nota tengt XML-skema til að skilgreina hvaða gagnastak á að hafa með í flýtiflipanum **Dálkskilgreiningar**. Sjá skref 6 í hlutanum [Að lýsa sniði lína og dálka í skránni](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Frekari upplýsingar í [Nota XML-skemu til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Venjulega eru gagnaskiptaskilgreiningar settar upp á síðunni **Gagnaskiptaskilgreining**. Til að uppfæra gengi gjaldmiðla er hins vegar fljótlegra að nota þjónustu fyrir gengi gjaldmiðils. Lærðu meira á [Uppfærðu gengi gjaldmiðla](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Ef skráin sem verið er að umbreyta er á XML-sniði ætti að túlka hugtakið *„dálkur“* í þessari grein sem *„XML-einingu sem inniheldur gögn“*.  

Þessi grein inniheldur eftirfarandi ferla:  

* Stofnaðu skilgreiningu gagnaskipta.
* Flyttu út gagnaskiptaskilgreiningu sem XML-skrá til afnota fyrir aðra.
* Flyttu inn XML-skrá fyrir núverandi gagnaskiptaskilgreiningu.

## Stofna gagnaskiptaskilgreiningu

Að stofna skilgreiningu gagnaskipta felur í sér tvö verkefni:  

1. Á síðunni **Skilgreining gagnaskipta** skal lýsa sniði lína og dálka í skránni. Frekari upplýsingar er að finna í hlutanum [Að lýsa sniði lína og dálka á skránni](#formatlinescolumns).  
2. Á síðunni **Vörpun gagnaskipta** skal varpa dálkum í gagnaskránni á reiti í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í hlutanum [Að varpa dálkum í gagnaskránni í reiti í [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name=formatlinescolumns></a>Að lýsa sniði lína og dálka í skrá

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gagnaskiptaskilgreiningar** og veldu síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Á flýtiflipanum **Almennt** skal lýsa gagnaskiptaskilgreiningunni og gagnaskráargerðinni með því að fylla út reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Skilgreining|  
    |---------------------------------|---------------------------------------|  
    |**Kóti**|Færið inn kóða til að auðkenna skilgreiningu gagnaskipta.|  
    |**Heiti**|Færið inn heiti fyrir skilgreiningu gagnaskipta.|  
    |**Skráargerð**|Tilgreindu hvaða gerð skráar gagnaskiptaskilgreiningin er notuð fyrir. Þú getur valið á milli fjögurra skráargerða:<br /><br /> -   **XML**: Lagskiptir efnisstrengir og breytingarmerkingar inni í merkjum sem skilgreina virkni þeirra.<br />-   **Breytilegur texti**: Skráargerð þar sem færslur hafa breytilega lengd og eru aðskilin með tákni, svo sem kommu eða semí\-kommu, einnig þekkt sem *afmörkuð skrá*.<br />-   **Fastur texti**: Færslur eru af sömu lengd, nota talnaborðsstafi og hver færsla er í eigin línu, einnig þekkt sem *skrá með fastri breidd*.<br />- **Json**: Lagskiptir strengir af efni í JavaScript.|  
    |**Tegund**|Tilgreinið hvaða tegund af starfsemi skilgreining gagnaskipta er notað fyrir, t.d. **Útflutningur greiðslna**.|  
    |**Meðhöndlunarkóðaeining gagna**|Tilgreinið kóðaeiningu sem flytur gögn inn og út úr töflum í [!INCLUDE[prod_short](includes/prod_short.md)]|  
    |**Kóðaeining staðfestingar**|Tilgreinið kóðaeiningu sem er notuð til að sannprófa gögn gegn fyrirfram skilgreindum viðskiptareglum.|  
    |**Les/skrifar kóðaeiningu**|Tilgreinið kóðaeiningu sem vinnur innflutt gögn fyrir vörpun og útflutt gögn eftir vörpun.|  
    |**Les/skrifar XMLport**|Tilgreindu XMLport sem innflutt gagnaskrá eða þjónusta fer í gegnum fyrir vörpun og sem flutt gögn fara út um þegar þau eru skrifuð á gagnaskrá eða þjónustu eftir vörpun.|  
    |**Meðhöndlunarkóðaeining ytri gagna**|Tilgreinið kóðaeiningu sem flytur ytri gögn inn og út af Gagnaskiptaramma.|  
    |**Kóðaeining athugasemdar frá notanda**|Tilgreinir kóðaeiningu sem framkvæmir ýmsa hreinsun eftir vörpun, t.d. að merkja línurnar sem fluttar út og eyða tímabundunum færslum.|  
    |**Skráarkóðun**|Tilgreinið kóðun skráar. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Dálkaskiltákn**|Tilgreinið hvernig dálkarnir í skránni eru aðskilin, ef skráin er af gerðinni **Breytilegur texti**|  
    |**Hausalínur**|Tilgreinir hversu margir hausalínur eru í skránni.<br /><br /> Þessi stilling tryggir að gögn í haus séu ekki flutt inn. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Hausamerki**|Ef hauslína er á nokkrum stöðum í skránni skaltu slá inn texta í fyrsta dálkinum á hauslínunni.<br /><br /> Þessi valkostur tryggir að gögn í haus séu ekki flutt inn. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Síðufótarmerki**|Ef fótarlína er á nokkrum stöðum í skránni skaltu slá inn texta í fyrsta dálkinum í fótarlínunni.<br /><br /> Þessi valkostur tryggir að gögn í fæti séu ekki flutt inn. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  

   > [!TIP]
   > Til að sjá hvaða kóðaeiningar Microsoft notar í núverandi skilgreiningum í stöðluðu vörunni, skal yfirfara reitina þrjá fyrir **Kóðaeiningu** á síðunni **Reitavörpun**, undir flýtiflipanum **Almennt**, fyrir hverja skilgreiningu.  

4. Á flýtiflipanum **Línuskilgreiningar** skal lýsa línusniði í gagnaskrá með því að fylla út reitina eins og lýst er í eftirfarandi töflu.  

    > [!NOTE]  
    > Fyrir innflutning á bankayfirlitum er aðeins búin til ein lína fyrir stakt snið bankayfirlitsskár sem á að flytja inn.  
    >
    > Til útflutnings á greiðslum er hægt að stofna línu fyrir hverja greiðslugerð sem á að flytja út. Í slíku tilviki sýnir flýtiflipinn **Dálkskilgreiningar** mismunandi dálkar fyrir hverja tegund greiðslu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Gerð línu**|Tilgreinir línugerðina í skránni.|  
    |**Kóði**|Færið inn kóða til að auðkenna línuna í skránni.|  
    |**Heiti**|Færið inn heiti sem lýsir línunni í skránni.|  
    |**Dálkafjöldi**|Tilgreinið hversu marga dálka línan í gagnaskránni hefur. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Gagnalínumerki**|Tilgreinið stöðu á viðkomandi XML-skema einingarinnar sem sýnir aðalfærslu gagnaskrárinnar. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Nafnbil**|Tilgreinið nafnbil sem er væntanlegt í skránni, til að virkja nafnbils staðfestingu. Þennan reit má hafa auðan ef ekki á að virkja fullgildingu nafnabils.|  
    |**Yfirkóði**|Tilgreinið yfireiningu línunnar sem er sýnd í reitnum **Kóði** þar sem uppsetning gagnaskipta er fyrir skrár með yfir- og undirfærslum, t.d. skjalahaus og línum.

5. Endurtakið skref 4 til að búa til línu fyrir hver skráargögn sem á að flytja út.  

     Haldið áfram og á flýtiflipanum **Dálkskilgreiningar** skal lýsa línusniði í gagnaskrá með því að fylla út reitina eins og lýst er í eftirfarandi töflu. Hægt er að nota skipulagsskrá, t.d. .xsd-skrá, fyrir gagnaskrá til að fylla út í flýtiflipann með viðeigandi einingum. Frekari upplýsingar í [Nota XML-skemu til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. Veljið aðgerðina **Sækja skráaskipan** á flýtiflipanum **Dálkskilgreiningar**.  
7. Á síðunni **Sækja skráaskipan** skal velja tengda skráaskipan og svo velja hnappinn **Í lagi**. Línur í flýtiflipanum **Dálkskilgreiningar** eru fylltar út í samræmi við skipulag gagnaskrárinnar.  
8. Fyllioð inn í reitina eins og lýst er í eftirfarandi töflu í flýtiflipanum **Dálkskilgreiningar**.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Dálknr.**|Tilgreinið númerið sem endurspeglar stöðu dálksins í línunni í skránni.<br /><br /> Fyrir XML-skrár skal tilgreina töluna sem endurspeglar gerð staks í skránni sem inniheldur gögnin.|  
    |**Heiti**|Tilgreinið heiti dálksins.<br /><br /> Fyrir XML-skrár skal tilgreina kóðann sem merkir gögnin sem á að skipta um.|  
    |**Tegund gagna**|Tilgreinið hvort gögn til að skipta eru af taginu **Texti**, **Dagsetning** eða **Tugakerfi**|  
    |**Gagnasnið**|Tilgreinið snið gagnanna ef einhver er. Til dæmis **MM-dd-áááá** ef gagnagerðin er  **Dagsetning**. **Athugið:**  Til að flytja út, tilgreinið gagnasnið í samræmi við [!INCLUDE[prod_short](includes/prod_short.md)]. Til að flytja inn skal tilgreina gagnasnið í samræmi við .NET rammann. Frekari upplýsingar er að finna í [Strengir staðlaðs dagsetningar- og tímasniðs](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Menning gagnasniðs**|Tilgreinið svæðisbundið gagnasnið, ef það er til staðar. Til dæmis **en-US** ef gagnagerðin er **Tugastafur** til að tryggja að komma sé notuð sem skiltákn milli þúsunda, .000, samkvæmt bandaríska kerfinu. Frekari upplýsingar er að finna í [Strengir staðlaðs dagsetningar- og tímasniðs](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Lengd**|Tilgreinið lengd línu af fastri vídd sem inniheldur dálkinn ef gagnaskráin er af gerðinni **Fastur texti**|  
    |**Lýsing**|Tilgreinir lýsingu á dálknum í upplýsingarskyni.|  
    |**Slóð**|Tilgreinið stöðu einingar í tengdum XML skema.|  
    |**Auðkenni neikvæðs formerkis**|Færið inn virðið sem notað er í gagnaskránni til að auðkenna neikvæðar upphæðir, í gagnaskránum sem ekki mega innihalda mínusmerki. Þetta kennimerki er notað til að breyta auðkenndu upphæðunum í mínusmerki við innflutning. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Fasti**|Tilgreinið hvaða gögn sem þú vilt flytja í þessum dálki, ss viðbótarupplýsingar um greiðslugerð. **Athugið**: Þessi reitur er aðeins gildur fyrir útflutning.|  
    |**Fylling texta nauðsynleg**|Tilgreinið að gögnin verða að innihalda textafyllingu.|  
    |**Fyllingarstafur**|Tilgreinið fyllingarstaf textans.|  
    |**Jöfnun**|Tilgreinið hvort dálkurinn sé hægri- eða vinstrijafnaður.|  

9. Endurtakið skref 8 fyrir hvert dálki eða XML-stak í gagnaskrá sem inniheldur gögn sem á að skiptast á við [!INCLUDE[prod_short](includes/prod_short.md)].  

Næsta skref í því að stofna skilgreiningu gagnaskipta er að ákveða hvaða dálkar eða XML-einingar í gagnaskránni varpast á hvaða reiti í [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Tilgreind vörpun ræðst af tilgangi viðskipta í gagnaskránni sem á að skipta og staðbundnum tilbrigðum. Jafnvel SEPA-bankastaðallinn er einnig með staðbundin afbrigði. [!INCLUDE[prod_short](includes/prod_short.md)] styður innflutning SEPA CAMT bankayfirlitsskrám \-út\-úr\-boxinu. Þetta er kemur fram í **SEPA CAMT** skilgreiningarfærslukóðanum fyrir gangaskipti á síðunni **Skilgreiningar gagnaskipta**. Upplýsingar um tilgreinda reitavörpun þessa SEPA CAMT stuðnings eru í [Reitavörpun við innflutning á SEPA CAMT skrám](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name=mapfields></a>Að tengja dálka í gagnaskránni við reiti í [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Stundum eru önnur gildi í reitunum sem á að varpa. Til dæmis, í einu viðskiptaforriti er tungumálakóðinn fyrir Bandaríkin „U.S.“ en í öðru er hann „US.“ Það þýðir að þú verður að umbreyta gildinu þegar þú skiptist á gögnum. Þetta gerist í gegnum breytingareglur sem eru skilgreindar fyrir svæðin. Frekari upplýsingar er að finna í [Reglur umbreytinga](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Þú getur líka flokkað eftir hvaða reit sem er, notað lykilvísitöluna til að flokka niðurstöður og nýju umbreytingargerðirnar **Núnmundun** og **Reitaleit**.

1. Á flýtiflipanum **Línuskilgreiningar** skal velja línuna sem á að varpa dálkum í reiti fyrir og velja svo **Reitavörpun**. Síðan **Vörpun gagnaskipta** opnast.  
2. Á flýtiflipanum **Almennt** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Töflukenni**|Tilgreinið töflu sem geymir reitina til eða frá sem gögn er skipst á samkvæmt vörpun.|  
    |**Notist sem millitafla**|Tilgreinið hvort taflan sem var valin í **Tafla Kenni** reitnum er millitafla þar sem innflutt gögn eru geymd áður en þeim er varpað á marktöfluna.<br /><br /> Venjulega er notuð millitafla þar sem gagnaskiptaskilgreiningar eru notaðar til að flytja inn og umbreyta rafrænum skjölum, t.d. reikningum lánardrottins í innkaupareikning í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar í [Rafræn gagnaskipti](across-data-exchange.md).|  
    |**Heiti**|Sláðu inn heiti fyrir vörpunaruppsetninguna.|  
    |**Lykilvísir**|Tilgreinið lykilvísi til að raða upprunafærslum fyrir útflutning.|
    |**Kóðaeining forvörpunar**|Tilgreinið kóðaeining sem undirbúa vörpun á milli reita í [!INCLUDE[prod_short](includes/prod_short.md)] og ytri gögn.|  
    |**Vörpunarkóðaeining**|Tilgreinið kóðaeiningu sem er notað til að kortleggja tilgreind dálka eða XML-gagnastök í reiti í ​​[!INCLUDE[prod_short](includes/prod_short.md)]|  
    |**Kóðaeining eftirávörpunar**|Tilgreinið kóðaeiningu sem lýkur vörpun á milli reita í [!INCLUDE[prod_short](includes/prod_short.md)] og ytri gagna. **Athugið:** Þegar eiginleiki AMC Banking 365 Fundamentals viðbótarinnar er notaður umreiknar kóðaeiningin útflutt gögn úr [!INCLUDE[prod_short](includes/prod_short.md)] yfir í almennt snið sem er tilbúið til útflutnings. Til að flytja inn breytir kóðaeiningin ytri gögnum í snið sem hægt er að flytja inn í [!INCLUDE[prod_short](includes/prod_short.md)].|
3. Á flýtiflipanum **Reitavörpun** skal tilgreina hvaða dálkum á að varpa í hvaða reiti í [!INCLUDE[prod_short](includes/prod_short.md)] með því að fylla út reitina eins og því er lýst í eftirfarandi töflum, eftir því hvort reiturinn **Notist sem millitafla** var virkur eða ekki.  
   * Með slökkt á **Notist sem millitafla**:

     |Svæði|Lýsing|  
     |--------------------------------- |---------------------------------------|  
     |**Dálknr.**|Tilgreinið hvaða dálk í gagnaskrá sem þú vilt skilgreina kort vörpun fyrir.<br /><br /> Aðeins er hægt að velja dálka sem eru kynntir af línum í flýtiflipanum **Dálkskilgreiningar** á síðunni **Skilgreiningar gagnaskipta**.|
     |**Texti kóða**|Tilgreinið skýringartexta dálksins í ytri skrá sem varpað er í reitinn í reitnum **Auðkenni marktöflu** þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Kenni reits**|Tilgreinið hvaða reit dálkurinn í **Dálkur nr.** reitnum tengist.<br /><br /> Aðeins er hægt að velja úr reitum sem eru til í töflunni sem tilgreind var í reitnum **Töflukenni** á flýtiflipanum **Almennt**.|
     |**Texti reits**|Tilgreinið skýringartexta reitsins í ytri skrá sem varpað er í reitinn í reitnum **Auðkenni marktöflu** þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Valfrjálst**|Tilgreinið hvort vörpun á að sleppa ef reitur er tómur. Ef þessi valkostur er ekki valinn kemur upp útflutningsvilla ef reiturinn er auður.|  
     |**Umbreytingarregla**|Tilgreinið reglu sem umbreytir innfluttum texta í stutt gildi áður en hægt er varpa því í tiltekinn reit. Þegar gildi er valið í þessum reit er sama gildið slegið inn í reitinn **Umbreytingarregla** í töflunni **Biðminni vörpunar gagnaskiptareits** og öfugt. Frekari upplýsingar um tiltækar umbreytingarreglur sem hægt er að nota er að finna í næsta hluta.|
     |**Skrifa yfir gildi**|Tilgreinið að skrifað verði yfir núverandi gildi með nýju.|
     |**Forgangur**|Tilgreinið röðina sem vinna þarf úr reitarvörpunum. Fyrst verður unnið úr reitavörpuninni með hæsta forgangsnúmerið.|
     |**Margfaldari**|Tilgreinið margfeldi sem á að nota á talnagögn, þar á meðal neikvæð gildi.|

   * Með kveikt á **Notist sem millitafla**:

     |Svæði|Lýsing|  
     |---------------------------------|---------------------------------------|  
     |**Dálknr.**|Tilgreinið hvaða dálk í gagnaskrá sem þú vilt skilgreina kort vörpun fyrir.<br /><br /> Aðeins er hægt að velja dálka sem eru kynntir af línum í flýtiflipanum **Dálkskilgreiningar** á síðunni **Skilgreiningar gagnaskipta**.|
     |**Texti kóða**|Tilgreinið skýringartexta dálksins í ytri skrá sem varpað er í reitinn í reitnum **Auðkenni marktöflu** þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Auðkenni marktöflu**|Tilgreinir töflu sem gildi í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Töflutexti**|Tilgreinir heiti töflunnar í reitnum **Auðkenni marktöflu**, sem er taflan sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Auðkenni markreits**|Tilgreinir reit í marktöflu sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Texti reits**|Tilgreinir heiti reits í marktöflu sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Aðeins sannprófa**|Tilgreinið að vörpun frá einingu í reit er ekki notuð til að umbreyta gögnum heldur aðeins til að sannprófa gögn.|
     |**Umbreytingarregla**|Tilgreinið reglu sem umbreytir innfluttum texta í stutt gildi áður en hægt er varpa því í tiltekinn reit. Þegar gildi er valið í þessum reit er sama gildið slegið inn í reitinn **Umbreytingarregla** í töflunni **Biðminni vörpunar gagnaskiptareits** og öfugt. Frekari upplýsingar um tiltækar umbreytingarreglur sem hægt er að nota er að finna í næsta hluta.|
     |**Forgangur**|Tilgreinið röðina sem vinna þarf úr reitarvörpunum. Fyrst verður unnið úr reitavörpuninni með hæsta forgangsnúmerið.|

4. Á flýtiflipanum **Reitarflokkun** skal tilgreina reglur sem á að nota til að flokka reitina þegar skráin er búin til með því að fylla út reitina eins og lýst er í eftirfarandi töflu.  

     |Svæði|Lýsing|  
     |--------------------------------- |---------------------------------------|  
     |**Kenni reits**|Tilgreinið númer reitsins í ytri skránni sem notað er fyrir flokkun og þessi reitur verður að vera stilltur af notanda.|
     |**Texti reits**|Tilgreinið skýringartexta reitsins í ytri skránni sem er notuð fyrir flokkun.|

## Umbreytingarreglur

Ef gildin í reitunum sem verið er að skrá eru mismunandi verður að nota umbreytingarreglur fyrir skilgreiningar gagnaskipta til að gildin verði þau sömu. Umbreytingarreglur fyrir gagnaskiptaskilgreiningar eru skilgreindar með því að opna fyrirliggjandi skilgreiningu eða búa til nýja skilgreiningu og síðan í flýtiflipanum **Línuskilgreiningar** skal velja **Stjórna** og síðan **Reitavörpun**. Boðið er upp á forskilgreindar reglur, en einnig má búa til sínar eigin. Í eftirfarandi töflu er tegundum umbreytinga lýst sem hægt er að nota.

|Valkostur|Description|
|---------|---------|
|**Hástafir**|Gera alla stafi að hástöfum.|
|**Lágstafir**|Gera alla stafi að lágstöfum.|
|**Hástafir fremst í orði**|Breyta upphafsstaf hvers orðs í hástaf.|
|**Klippa**|Fjarlægja tóm bil fyrir og eftir gildið.|
|**Undirstrengur**|Umbreyta tilteknum hluta gildis. Til að tilgreina hvar eigi að hefja umbreytingu skal velja annaðhvort **Upphafsstaða** eða **Upphafstexti**. Upphafsstaða er tala sem táknar fyrsta stafinn sem á að umbreyta. Upphafstexti er bókstafurinn á undan stafnum sem á að skipta út. Ef ætlunin er að byrja á fyrsta stafnum í gildinu skal nota upphafsstöðu í staðinn. Til að tilgreina hvar eigi að stöðva umbreytinguna er annaðhvort valið **Lengd**, sem er fjöldi stafa sem á að skipta út, eða **Endatexti**, sem er sá stafur sem strax á eftir síðasta stafnum sem á að umbreyta.|
|**Skipta um**|Finna skal gildi og skipta því út fyrir annað gildi. Þetta umbreyting er gagnleg til að skipta út einföldum gildum, t.d. tilteknu orði.|
|**Regluleg segð - Skipta út**|Nota skal reglubundna segð sem hluta af aðgerð til að finna og skipta út. Þetta umbreyting er gagnleg til að skipta út mörgum eða flóknari gildum.|
|**Fjarlægja stafi sem ekki eru bók-/tölustafir**|Eyddu stöfum sem eru ekki bókstafir eða tölustafir, t.d. tákn eða sérstafir.|
|**Dagsetningarsnið**|Tilgreina hvernig á að birta dagsetningar. Til dæmis er hægt að umbreyta DD-MM-ÁÁÁÁ í ÁÁÁÁ-MM-DD.|
|**Tugatölusnið**|Skilgreina reglur fyrir staðsetningu tugabrota og sléttunarnákvæmni.|
|**Samsvörun í reglulegum segðum**|Nota skal reglulega segð til að finna eitt eða fleiri gildi. Þessi regla er svipuð og valkostirnir **Undirstrengur** og **Regluleg segð**.|
|**Endurmat**|Þessi umbreytingarregla er ítarlegur valkostur sem krefst aðstoðar frá þróunaraðila. Það virkjar samþættingartilvik sem hægt er að gerast áskrifandi að ef áhugi er fyrir því að nota eigin umbreytingarkóða. Ef þú ert þróunaraðili og vilt nota þennan valkost skaltu skoða hlutann hér fyrir neðan.|
|**Dag- og tímasetningasnið**|Skilgreinið hvernig á að birta núverandi dagsetningu og tíma dags.|
|**Uppfletting í svæðum**|Notið reiti úr mismunandi töflum. Til að nota þetta þarf að fylgja nokkrum reglum. Notið fyrst **Töflukenni** til að tilgreina auðkenni töflunnar sem inniheldur færsluna fyrir reitaruppflettingu. Í reitnum **Auðkenni upprunareits** skal síðan tilgreina auðkenni reitsins sem inniheldur færsluna fyrir reitaruppflettingu. Að lokum skal í reitnum **Auðkenni markreits** tilgreina auðkenni reitsins til að finna færsluna fyrir reitaruppflettingu. Einnig er hægt að nota reitinn **Regla reitaruppflettingar** til að tilgreina gerð reitaruppflettingar. Fyrir reitinn **Markgildi** er gildið úr **Auðkenni markreits** notað, jafnvel þótt það sé autt. Fyrir reitinn **Upprunalegt ef markgildi er autt** er upprunalegt gildi notað ef markgildið er autt.|
|**Sléttun**|Sléttið gildið í þessum reit með nokkrum viðbótarreglum. Fyrst skal tilgreina sléttunarnákvæmni í reitnum **Nákvæmni**. Síðan skal tilgreina sléttunarstefnu í reitnum **Stefna**.|

> [!NOTE]  
> Frekari upplýsingar um dagsetningar- og tímasnið er að finna í [Strengir staðlaðs dagsetningar- og tímasniðs](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### Ábending til þróunaraðila: Dæmi um sérstillta valkosti

Eftirfarandi dæmi sýnir hvernig á að innleiða eigin umbreytingarkóða.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Þegar búið er að skilgreina reglurnar er hægt að prófa þær. Á flýtiflipanum **Prófun** skal slá inn dæmi um gildi sem á að umbreyta og síðan athuga niðurstöðurnar með því að velja **Uppfæra**.

## Flytja út gagnaskiptaskilgreiningu sem XML-skrá til afnota fyrir aðra

Þegar stofnuð hefur verið skilgreining gagngaskipta fyrir tiltekna gagnaskrá er hægt að flytja skilgreiningu gagnaskiptanna út sem XML-skrá sem hægt er að flytja inn. Þessu verki er lýst í eftirfarandi ferli.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gagnaskiptaskilgreiningar** og veldu síðan viðkomandi tengil.  
2. Velja gagnaskiptiskilgreininguna sem á að flytja út.  
3. Velja skal aðgerðina **Skilgreining gagnaskipta í útflutningi**.  
4. Vista xml skrá sem sýnir skilgreiningu gagnaskipta á viðeigandi staðsetningu.  

    Ef skilgreining gagnaskipta hefur þegar verið stofnuð þarftu bara að flytja inn XML skrá í gagnaskiptarammann. Þessu verki er lýst í eftirfarandi ferli.  

## Flytja inn fyrirliggjandi gagnaskiptaskilgreiningu

1. Vista xml skrá sem sýnir skilgreiningu gagnaskipta á viðeigandi staðsetningu.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gagnaskiptaskilgreiningar** og veldu síðan viðkomandi tengil.  
3. Velja skal aðgerðina **Skilgreining gagnaskipta í innflutningi**.  
4. Veljið skrána sem var vistuð í skrefi 1.  

## Sjá einnig .

[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  
[Greiða með AMC Banking 365 Fundamentals viðbótinni eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Skjöl á innleið](across-income-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
