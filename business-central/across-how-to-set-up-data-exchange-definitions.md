---
title: Skilgreina hvernig skipst er á gögnum rafrænt
description: Skilgreina hvernig fyrirtæki Miðgengi gögn með ytri skrám eins og rafrænum skjölum, bankagögnum, vörulistum og fleiru.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.search.form: 1210, 1211, 1213, 1214, 1215, 1216, 1217
ms.date: 11/03/2022
ms.author: bholtorf
ms.openlocfilehash: 324fa2e1576deb3f9cb4b082f065218d1576fd78
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744870"
---
# <a name="set-up-data-exchange-definitions"></a>Setja upp skilgreiningar gagnaskipta

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að skiptast á gögnum í tilteknar töflur með gögnum í ytri skrám. Til dæmis til að senda og taka á móti rafrænum skjölum, flytja inn og flytja út bankagögn eða önnur gögn, svo sem launa-, og vöruliði. Frekari upplýsingar um skiptast á [gögnum rafrænt](across-data-exchange.md).  

Til að stofna gagnaskiptaskilgreiningu fyrir gagnaskrá eða streymi er hægt að nota tengda XML-skema til að skilgreina hvaða gagnaeiningar eigi að hafa með á **fastflipa dálkaskilgreininganna**. Sjá skref 6 í hlutanum [Að lýsa sniði lína og dálka í skránni](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Frekari upplýsingar um [notkun XML-skema til að undirbúa Gagnaskiptaskilgreiningar](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Yfirleitt eru settar upp skilgreiningar á gögnum Exchange á **skilgreiningarsíðu** gagnaskipta. Til að uppfæra gengi gjaldmiðla er hins vegar fljótlegra að nýta sér gjaldmiðlaskiptaþjónustu. Frekari upplýsingar um [uppfærslu gengis](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service) gjaldmiðla.

> [!NOTE]  
> Ef skráin sem verið er að umbreyta er á XML-sniðinu á að túlka hugtakið *"dálkur* " í þessari grein sem *"XML-eining sem inniheldur gögn"*.  

Í þessari grein eru eftirfarandi verklagsreglur:  

* Stofna skilgreiningu gagnaskipta.
* Flytja út skilgreiningu gagnaskipta sem XML-skrá til notkunar fyrir aðra.
* Flytja inn XML-skrá fyrir fyrirliggjandi skilgreiningu á gagnaskiptum.

## <a name="create-a-data-exchange-definition"></a>Stofna skilgreiningu gagnaskipta

Að stofna skilgreiningu gagnaskipta felur í sér tvö verkefni:  

1. Á síðunni **Skilgreining gagnaskipta** skal lýsa sniði lína og dálka í skránni. Frekari upplýsingar eru [í til að lýsa sniði lína og dálka í skrárhlutanum](#formatlinescolumns).  
2. Á síðunni **Vörpun gagnaskipta** skal varpa dálkum í gagnaskránni á reiti í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru [í dálkunum til að varpa í gagnaskrána í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields) kafla.  

### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name=formatlinescolumns></a> Snið lína og dálka lýst í skránni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **skilgreiningar** á gögnum um skipti og velja síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.  
3. Á flýtiflipanum **Almennt** skal lýsa gagnaskiptaskilgreiningunni og gagnaskráargerðinni með því að fylla út reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Skilgreining|  
    |---------------------------------|---------------------------------------|  
    |**Kóti**|Færið inn kóða til að auðkenna skilgreiningu gagnaskipta.|  
    |**Heiti**|Færið inn heiti fyrir skilgreiningu gagnaskipta.|  
    |**Skráargerð**|Tilgreinið hvaða tegund skrár Skilgreining gagnaskipta er notuð. Þú getur valið á milli fjögurra skráargerða:<br /><br /> -   **XML**: Lagskiptir efnisstrengir og breytingarmerkingar inni í merkjum sem skilgreina virkni þeirra.<br />-   **Breytilegur texti** : plötur hafa breytilega lengd og eru aðskildar með staf, eins og kommu eða hálf \- ristil, einnig þekkt sem *afmörkuð skrá*.<br />-   **Fastur texti: plötur hafa sömu lengd, með Textatáknum** og hver færsla er í sérstakri línu, einnig þekkt sem *fastbreiddarljós*.<br />- **Json**: Lagskiptir strengir af efni í JavaScript.|  
    |**Tegund**|Tilgreinið hvaða tegund af starfsemi skilgreining gagnaskipta er notað fyrir, t.d. **Útflutningur greiðslna**.|  
    |**Meðhöndlunarkóðaeining gagna**|Tilgreinið kóðaeiningu sem flytur gögn inn og út úr töflum í [!INCLUDE[prod_short](includes/prod_short.md)]|  
    |**Kóðaeining staðfestingar**|Tilgreinið kóðaeiningu sem er notuð til að sannprófa gögn gegn fyrirfram skilgreindum viðskiptareglum.|  
    |**Les/skrifar kóðaeiningu**|Tilgreinið kóðaeiningu sem vinnur innflutt gögn fyrir vörpun og útflutt gögn eftir vörpun.|  
    |**Les/skrifar XMLport**|XMLport Tilgreinið sem innflutta gagnaskrá eða þjónustu áður en hún er vörpun og með útfluttum gögnum þegar hún er skrifuð í gagnaskrá eða þjónustu eftir vörpun.|  
    |**Meðhöndlunarkóðaeining ytri gagna**|Tilgreinið kóðaeiningu sem flytur ytri gögn inn og út af Gagnaskiptaramma.|  
    |**Kóðaeining athugasemdar frá notanda**|Tilgreinir kóðaeiningu sem framkvæmir ýmsa hreinsun eftir vörpun, t.d. að merkja línurnar sem fluttar út og eyða tímabundunum færslum.|  
    |**Skráarkóðun**|Tilgreinið kóðun skráar. **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  
    |**Dálkaskiltákn**|Tilgreinið hvernig dálkarnir í skránni eru aðskilin, ef skráin er af gerðinni **Breytilegur texti**|  
    |**Hausalínur**|Tilgreinir hversu margir hausalínur eru í skránni.<br /><br /> Þessi stilling tryggir að hausagögin séu ekki flutt inn. **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  
    |**Hausamerki**|Ef hauslína er á nokkrum stöðum í skránni skaltu slá inn texta í fyrsta dálkinum á hauslínunni.<br /><br /> Þessi valkostur tryggir að haugögnin séu ekki flutt inn. **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  
    |**Síðufótarmerki**|Ef fótarlína er á nokkrum stöðum í skránni skaltu slá inn texta í fyrsta dálkinum í fótarlínunni.<br /><br /> Þessi valkostur tryggir að síðuneðanmálsgögn eru ekki flutt inn. **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  

   > [!TIP]
   > Til að sjá hvaða kótaeiningar Microsoft notar í skilgreiningum sem eru til staðar í staðalvörunni, skoðið svæðin þrjú **með Codeunit** á **svæðvörpunarsíðunni**, undir **flipanum Almennt**, fyrir hverja skilgreiningu.  

4. Á flýtiflipanum **Línuskilgreiningar** skal lýsa línusniði í gagnaskrá með því að fylla út reitina eins og lýst er í eftirfarandi töflu.  

    > [!NOTE]  
    > Fyrir innflutning á bankayfirlitum er aðeins búin til ein lína fyrir stakt snið bankayfirlitsskár sem á að flytja inn.  
    >
    > Til útflutnings á greiðslum er hægt að stofna línu fyrir hverja greiðslugerð sem á að flytja út. Í slíku tilviki sýnir flýtiflipinn **Dálkskilgreiningar** mismunandi dálkar fyrir hverja tegund greiðslu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Tegund línu**|Tilgreinir línugerðina í skránni.|  
    |**Kóði**|Færið inn kóða til að auðkenna línuna í skránni.|  
    |**Heiti**|Færið inn heiti sem lýsir línunni í skránni.|  
    |**Dálkafjöldi**|Tilgreinið hversu marga dálka línan í gagnaskránni hefur. **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  
    |**Gagnalínumerki**|Tilgreinið stöðu á viðkomandi XML-skema einingarinnar sem sýnir aðalfærslu gagnaskrárinnar. **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  
    |**Nafnbil**|Tilgreinið nafnbil sem er væntanlegt í skránni, til að virkja nafnbils staðfestingu. Þennan reit má hafa auðan ef ekki á að virkja fullgildingu nafnabils.|  
    |**Yfirkóði**|Veljið yfirverk línunnar eins og sýnt er í **reitnum kóti** í tilvikum þar sem Uppsetning gagnaskipta er fyrir skrár með foreldris-og barnafærslum, eins og fyrirsögn skjals og línur.

5. Endurtakið skref 4 til að búa til línu fyrir hver skráargögn sem á að flytja út.  

     Haldið áfram og á flýtiflipanum **Dálkskilgreiningar** skal lýsa línusniði í gagnaskrá með því að fylla út reitina eins og lýst er í eftirfarandi töflu. Hægt er að nota skipulagskrána eins og. XSD-skrá fyrir gagnaskrána til að forfylla Fastflipann með viðeigandi einingum. Frekari upplýsingar um [notkun XML-skema til að undirbúa Gagnaskiptaskilgreiningar](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. **Á flipanum fastir í dálkaskilgreiningum** er valið **aðgerðin Sækja skrárskipulag**.  
7. **Á síðunni sækja Skrárskipulag** skal velja tengda Skipulagsskrá og velja **síðan í lagi**. Línur í flýtiflipanum **Dálkskilgreiningar** eru fylltar út í samræmi við skipulag gagnaskrárinnar.  
8. Fyllioð inn í reitina eins og lýst er í eftirfarandi töflu í flýtiflipanum **Dálkskilgreiningar**.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Dálknr.**|Tilgreinið númerið sem endurspeglar stöðu dálksins í línunni í skránni.<br /><br /> Fyrir XML-skrár skal tilgreina töluna sem endurspeglar gerð staks í skránni sem inniheldur gögnin.|  
    |**Heiti**|Tilgreinið heiti dálksins.<br /><br /> Fyrir XML-skrár skal tilgreina kóðann sem merkir gögnin sem á að skipta um.|  
    |**Tegund gagna**|Tilgreinið hvort gögn til að skipta eru af taginu **Texti**, **Dagsetning** eða **Tugakerfi**|  
    |**Gagnasnið**|Tilgreinið snið gagnanna ef einhver er. Til dæmis **MM-dd-áááá** ef gagnagerðin er  **Dagsetning**. **Til athugunar:** til útflutnings skal tilgreina gagnasnið samkvæmt [!INCLUDE[prod_short](includes/prod_short.md)]. Til að flytja inn skal tilgreina gagnasnið í samræmi við .NET rammann. Frekari upplýsingar á [staðalformi dagsetningar og tíma-strengja](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Menning gagnasniðs**|Tilgreinið svæðissnið svæðis ef það er fyrir. Til dæmis **en-US** ef gagnagerðin er **Tugastafur** til að tryggja að komma sé notuð sem skiltákn milli þúsunda, .000, samkvæmt bandaríska kerfinu. Frekari upplýsingar á [staðalformi dagsetningar og tíma-strengja](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  
    |**Lengd**|Tilgreinið lengd línu af fastri vídd sem inniheldur dálkinn ef gagnaskráin er af gerðinni **Fastur texti**|  
    |**Lýsing**|Tilgreinir lýsingu á dálknum í upplýsingarskyni.|  
    |**Slóð**|Tilgreinið stöðu einingar í tengdum XML skema.|  
    |**Auðkenni neikvæðs formerkis**|Færið inn virðið sem notað er í gagnaskránni til að auðkenna neikvæðar upphæðir, í gagnaskránum sem ekki mega innihalda mínusmerki. Þetta kennimerki er notað til að breyta auðkenndu upphæðunum í mínusmerki við innflutning. **Til athugunar:** Þessi reitur á aðeins við um innflutning.|  
    |**Fasti**|Tilgreinið hvaða gögn sem þú vilt flytja í þessum dálki, ss viðbótarupplýsingar um greiðslugerð. **Til athugunar:** Þessi reitur á aðeins við um útflutning.|  
    |**Textafylling þarf**|Tilgreinið að gögn þurfi að fela í sér textafyllingar.|  
    |**Púði persóna**|Tilgreina skal staffyllingarstaf textans.|  
    |**Réttlæting**|Tilgreina hvort dálkréttlæting sé til vinstri eða hægri.|  

9. Endurtakið skref 8 fyrir hvert dálki eða XML-stak í gagnaskrá sem inniheldur gögn sem á að skiptast á við [!INCLUDE[prod_short](includes/prod_short.md)].  

Næsta skref í því að stofna skilgreiningu gagnaskipta er að ákveða hvaða dálkar eða XML-einingar í gagnaskránni varpast á hvaða reiti í [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Tilgreind vörpun ræðst af tilgangi viðskipta í gagnaskránni sem á að skipta og staðbundnum tilbrigðum. Jafnvel SEPA-bankastaðallinn er einnig með staðbundin afbrigði. [!INCLUDE[prod_short](includes/prod_short.md)] styður innflutning SEPA CAMT bankayfirlitsskrám \-út\-úr\-boxinu. Þetta er kemur fram í **SEPA CAMT** skilgreiningarfærslukóðanum fyrir gangaskipti á síðunni **Skilgreiningar gagnaskipta**. Upplýsingar um tilgreinda reitavörpun þessa SEPA CAMT stuðnings eru í [Reitavörpun við innflutning á SEPA CAMT skrám](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name="to-map-columns-in-the-data-file-to-fields-in-prod_short"></a><a name=mapfields></a> Dálkum varpað á gagnaskrána í reiti í[!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Stundum eru önnur gildi í reitunum sem á að varpa. Til dæmis í One Business App tungumálskóði fyrir Bandaríkin er "BNA" en í öðru er það "US". Það þýðir að þú verður að umbreyta gildinu þegar þú skiptist á gögnum. Þetta gerist í gegnum breytingareglur sem eru skilgreindar fyrir svæðin. Frekari upplýsingar um [umbreytingarreglur](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Sem byrjar í 2022 2, einnig er hægt að flokka eftir hvaða svæði sem er með því að nota lyklaatriðaskrá til að raða niðurstöðum og nýju uppflettigerðirnar **Sléttun** og **reitting**.

1. **Á flipanum Fastlínuskilgreiningar** skal velja línuna þar sem á að varpa dálkum á reiti og velja **síðan Svæðavörpun**. Síðan **Vörpun gagnaskipta** opnast.  
2. Á flýtiflipanum **Almennt** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Töflukenni**|Tilgreinið töflu sem geymir reitina til eða frá sem gögn er skipst á samkvæmt vörpun.|  
    |**Notist sem millitafla**|Tilgreinið hvort taflan sem var valin í **Tafla Kenni** reitnum er millitafla þar sem innflutt gögn eru geymd áður en þeim er varpað á marktöfluna.<br /><br /> Venjulega er notuð millitafla þar sem gagnaskiptaskilgreiningar eru notaðar til að flytja inn og umbreyta rafrænum skjölum, t.d. reikningum lánardrottins í innkaupareikning í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar um skiptast á [gögnum rafrænt](across-data-exchange.md).|  
    |**Heiti**|Sláðu inn heiti fyrir vörpunaruppsetninguna.|  
    |**Lyklavísitölur**|Specifiy lyklaatriðaskrá til að raða Upprunafærslur fyrir útflutning.|
    |**Kóðaeining forvörpunar**|Tilgreinið kóðaeining sem undirbúa vörpun á milli reita í [!INCLUDE[prod_short](includes/prod_short.md)] og ytri gögn.|  
    |**Vörpunarkóðaeining**|Tilgreinið kóðaeiningu sem er notað til að kortleggja tilgreind dálka eða XML-gagnastök í reiti í ​​[!INCLUDE[prod_short](includes/prod_short.md)]|  
    |**Kóðaeining eftirávörpunar**|Tilgreinið kóðaeiningu sem lýkur vörpun á milli reita í [!INCLUDE[prod_short](includes/prod_short.md)] og ytri gagna. **Athugið:** Þegar eiginleiki AMC Banking 365 Fundamentals viðbótarinnar er notaður umreiknar kóðaeiningin útflutt gögn úr [!INCLUDE[prod_short](includes/prod_short.md)] yfir í almennt snið sem er tilbúið til útflutnings. Til að flytja inn breytir kóðaeiningin ytri gögnum í snið sem hægt er að flytja inn í [!INCLUDE[prod_short](includes/prod_short.md)].|
3. **Á flipanum Flýtivörpun** í svæðið skal tilgreina hvaða dálka á hvaða svæði í [!INCLUDE[prod_short](includes/prod_short.md)] með því að fylla út reitina eins og lýst er í eftirfarandi töflum eftir því hvort **notað sem millitöflusvæði** var virkjað eða ekki.  
   * **Með notkun eins og Millitafla** skipta sköpum:

     |Svæði|Lýsing|  
     |--------------------------------- |---------------------------------------|  
     |**Dálknr.**|Tilgreinið hvaða dálk í gagnaskrá sem þú vilt skilgreina kort vörpun fyrir.<br /><br /> Aðeins er hægt að velja dálka sem eru kynntir af línum í flýtiflipanum **Dálkskilgreiningar** á síðunni **Skilgreiningar gagnaskipta**.|
     |**Dálkur yfirskrift**|Tilgreinið yfirskrift dálksins í ytri skránni sem er varpað á svæðið í **reitnum MARKTÖFLUKENNI** þegar verið er að nota millitöflu fyrir gagnainnflutning.|
     |**Kenni reits**|Tilgreinið hvaða reit dálkurinn í **Dálkur nr.** reitnum tengist.<br /><br /> Aðeins er hægt að velja úr reitum sem til eru í töflunni sem tilgreind var í **reitnum TÖFLUKENNI** á **flipanum Almennt**.|
     |**Skýringartexti reits**|Tilgreinið yfirskrift svæðisins í ytri skránni sem er varpað á svæðið í **reitnum Mark töflukenni**, þegar verið er að nota millitöflu fyrir gagnainnflutning.|
     |**Valfrjálst**|Tilgreinið hvort vörpun á að sleppa ef reitur er tómur. Ef þessi valkostur er ekki valinn mun útflutningssvilla eiga sér stað ef reiturinn er auður.|  
     |**Umbreytingarregla**|Tilgreinið regluna sem umbreytir innfluttum texta í studd gildi áður en hægt er að tengja hann við tiltekið svæði. Þegar valið er gildi í þessu svæði er sama gildið fært inn í **reitinn Umbreytingarregla** í **Reitun Exch. Field vörpun svæði buf.** Töflu og öfugt. Sjá næsta kafla fyrir frekari upplýsingar um tiltækar umbreytingarreglur sem hægt er að nota.|
     |**Skrifa yfir gildi**|Tilgreinið að nýtt gildi verði skrifað yfir gildandi gildi.|
     |**Forgangur**|Tilgreinið pöntunina sem á að vinna svæðvarpana úr. Svæðisvörpun með hæsta forgangsnúmeri verður fyrst unnin.|
     |**Margfaldur**|Tilgreinið margfaldarann sem á að nota á talnagögnum, að meðtöldum neikvæðum gildum.|

   * **Með notkun sem Millitöfluskipta** virkjast:

     |Svæði|Lýsing|  
     |---------------------------------|---------------------------------------|  
     |**Dálknr.**|Tilgreinið hvaða dálk í gagnaskrá sem þú vilt skilgreina kort vörpun fyrir.<br /><br /> Aðeins er hægt að velja dálka sem eru kynntir af línum í flýtiflipanum **Dálkskilgreiningar** á síðunni **Skilgreiningar gagnaskipta**.|
     |**Dálkur yfirskrift**|Tilgreinið yfirskrift dálksins í ytri skránni sem er varpað á svæðið í **reitnum MARKTÖFLUKENNI** þegar verið er að nota millitöflu fyrir gagnainnflutning.|
     |**Auðkenni marktöflu**|Tilgreinir töflu sem gildi í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Töflutexti**|Tilgreinir heiti töflunnar í reitnum **Auðkenni marktöflu**, sem er taflan sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Auðkenni markreits**|Tilgreinir reit í marktöflu sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Skýringartexti reits**|Tilgreinir heiti reits í marktöflu sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|
     |**Villuleita aðeins**|Tilgreinið að einingu-til-reitakort sé ekki notað til að umbreyta gögnum heldur aðeins í villuleit gagna.|
     |**Umbreytingarregla**|Tilgreinið regluna sem umbreytir innfluttum texta í studd gildi áður en hægt er að tengja hann við tiltekið svæði. Þegar valið er gildi í þessu svæði er sama gildið fært inn í **reitinn Umbreytingarregla** í **Reitun Exch. Field vörpun svæði buf.** Töflu og öfugt. Sjá næsta kafla fyrir frekari upplýsingar um tiltækar umbreytingarreglur sem hægt er að nota.|
     |**Forgangur**|Tilgreinið pöntunina sem á að vinna svæðvarpana úr. Svæðisvörpun með hæsta forgangsnúmeri verður fyrst unnin.|

4. **Á flipanum Flokkun** á svæðinu eru tilgreindar reglur sem nota skal til að flokka svæðin þegar skráin er stofnuð með því að fylla út svæðin eins og lýst er í eftirfarandi töflu.  

     |Svæði|Lýsing|  
     |--------------------------------- |---------------------------------------|  
     |**Kenni reits**|Sérstilla númer svæðisins í ytri skrá sem er notuð við flokkun og þessi reitur verður að vera stilltur af notanda.|
     |**Skýringartexti reits**|Tilgreinið yfirskrift svæðisins í ytri skránni sem er notuð við flokkun.|

## <a name="transformation-rules"></a>Umbreytingarreglur

Ef gildin í reitunum sem verið er að skrá eru mismunandi verður að nota umbreytingarreglur fyrir skilgreiningar gagnaskipta til að gildin verði þau sömu. Umbreytingarreglur fyrir gagnaskiptaskilgreiningar eru skilgreindar með því að opna fyrirliggjandi skilgreiningu eða búa til nýja skilgreiningu og síðan í flýtiflipanum **Línuskilgreiningar** skal velja **Stjórna** og síðan **Reitavörpun**. Boðið er upp á forskilgreindar reglur, en einnig má búa til sínar eigin. Í eftirfarandi töflu er tegundum umbreytinga lýst sem hægt er að nota.

|Valkostur|Description|
|---------|---------|
|**Hástafir**|Gera alla stafi að hástöfum.|
|**Lágstafir**|Gera alla stafi að lágstöfum.|
|**Hástafir fremst í orði**|Breyta upphafsstaf hvers orðs í hástaf.|
|**Klippa**|Fjarlægja tóm bil fyrir og eftir gildið.|
|**Undirstrengur**|Umbreyta tilteknum hluta gildis. Til að tilgreina hvar eigi að hefja umbreytingu skal velja annaðhvort **Upphafsstaða** eða **Upphafstexti**. Upphafsstaða er tala sem táknar fyrsta stafinn sem á að umbreyta. Upphafstexti er bókstafurinn á undan stafnum sem á að skipta út. Ef ætlunin er að byrja á fyrsta stafnum í gildinu skal nota upphafsstöðu í staðinn. Til að tilgreina hvar á að stöðva umbreytinguna er annaðhvort **valin lengd** sem er Fjöldi stafa sem á að skipta út eða **endatextinn** sem er sá stafur sem er strax á eftir Síðasta staf sem á að umbreyta.|
|**Skipta um**|Finna skal gildi og skipta því út fyrir annað gildi. Þessi umbreyting er gagnleg til að skipta út einföldum gildum eins og tilteknu orði.|
|**Regluleg segð - Skipta út**|Nota skal reglubundna segð sem hluta af aðgerð til að finna og skipta út. Þessi umbreyting er gagnleg til að skipta út mörgum, eða flóknum, gildum.|
|**Fjarlægja stafi sem ekki eru bók-/tölustafir**|Eyddu stöfum sem eru ekki bókstafir eða tölustafir, t.d. tákn eða sérstafir.|
|**Dagsetningarsnið**|Tilgreina hvernig á að birta dagsetningar. Til dæmis er hægt að umbreyta DD-MM-ÁÁÁÁ í ÁÁÁÁ-MM-DD.|
|**Tugatölusnið**|Skilgreina reglur fyrir staðsetningu tugabrota og sléttunarnákvæmni.|
|**Samsvörun í reglulegum segðum**|Nota skal reglulega segð til að finna eitt eða fleiri gildi. Þessi regla svipar til **undirstrengs** og **reglubundinnar tjáningar-skipta**.|
|**Endurmat**|Þessi umbreytingarregla er Ítarlegur valkostur sem krefst aðstoðar frá hönnuði. Það virkjar samþættingartilvik sem þú getur gerst áskrifandi að ef þú vilt nota þinn eigin breytingarkóða. Ef þú ert verktaki og vilt nota þennan valkost, sjá kaflann hér á eftir.|
|**Dag- og tímasetningasnið**|Skilgreinið hvernig birta á núverandi dagsetningu og tíma dags.|
|**Uppfletting svæða**|Nota reiti úr mismunandi töflum. Til að nota það þarftu að fylgja einhverjum reglum. Fyrst skal nota **töflukenni** til að tilgreina kenni töflunnar sem inniheldur færsluna fyrir reitiluppfletting. Síðan, í **REITNUM kenni** upprunasvæðis, skal tilgreina kenni svæðisins sem inniheldur færsluna fyrir Uppfletting svæðisins. Loks skal tilgreina KENNI svæðisins til að finna færsluna fyrir Uppfletting svæðis í **reitnum Mark-kenni**. Að öðrum kosti skal nota **reitinn Uppflettiregla** svæðis til að tilgreina gerð svæðis uppflettinga. **Fyrir marksvæðið** er gildið úr **svæðiskenni** marksins notað, jafnvel þótt það sé autt. **Fyrir upprunalega gildið ef Mark er autt** er upprunalegt gildi notað ef reiturinn er auður.|
|**Umferð**|Slétta gildið í þessu svæði með frekari reglum. Fyrst skal tilgreina sléttunarnákvæmni í **reitnum nákvæmni**. Þá skal í **stefnu** reita tilgreina sléttunarstefnu.|

> [!NOTE]  
> Frekari upplýsingar um dagsetningar og tíma-snið á [staðalformi og tímasniðs-strengir](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### <a name="tip-for-developers-example-of-the-custom-option"></a>Ábending til hönnuða: dæmi um sérvalinn valkost

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

Þegar þú hefur skilgreint reglurnar þínar getur þú prófað þær. **Í prófið** fastflipann, Færið inn dæmi um gildi sem óskað er að umbreyta og Kannaðu niðurstöðurnar með því að velja **Update**.

## <a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Flytja skilgreiningu gagnaskipta sem XML-skrá til notkunar fyrir aðra

Þegar stofnuð hefur verið skilgreining gagngaskipta fyrir tiltekna gagnaskrá er hægt að flytja skilgreiningu gagnaskiptanna út sem XML-skrá sem hægt er að flytja inn. Þessu verki er lýst með eftirfarandi aðferð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **skilgreiningar** á gögnum um skipti og velja síðan tengda tengilinn.  
2. Velja gagnaskiptiskilgreininguna sem á að flytja út.  
3. Velja skal aðgerðina **Skilgreining gagnaskipta í útflutningi**.  
4. Vista xml skrá sem sýnir skilgreiningu gagnaskipta á viðeigandi staðsetningu.  

    Ef skilgreining gagnaskipta hefur þegar verið stofnuð þarftu bara að flytja inn XML skrá í gagnaskiptarammann. Þessu verki er lýst með eftirfarandi aðferð.  

## <a name="import-an-existing-data-exchange-definition"></a>Flytja inn skilgreiningu á fyrirliggjandi gagnaskiptum

1. Vista xml skrá sem sýnir skilgreiningu gagnaskipta á viðeigandi staðsetningu.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **skilgreiningar** á gögnum um skipti og velja síðan tengda tengilinn.  
3. Velja skal aðgerðina **Skilgreining gagnaskipta í innflutningi**.  
4. Veljið skrána sem var vistuð í skrefi 1.  

## <a name="see-also"></a>Sjá einnig .

[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  
[Greiða með AMC Banking 365 Fundamentals viðbótinni eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Skjöl á innleið](across-income-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
