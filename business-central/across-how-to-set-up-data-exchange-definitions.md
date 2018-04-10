---
title: "Skilgreina hvernig rafræn gagnaskipti fara fram | Microsoft Docs"
description: "Hægt er að nota ytri veitu, sem býður OCR-þjónustu, til að breyta PDF eða myndaskrám í rafræn skjöl."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4828da068f1e17d031300948e930c9685a2f274d
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-data-exchange-definitions"></a>Setja upp skilgreiningar gagnaskipta
Hægt er að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)] til að skiptast á gögnum í tilgreindum töflum með gögnum á ytri skjölum, til dæmis senda og taka á móti rafrænum skjölum, flytja inn og flytja út bankagögn eða önnur gögn, t.d. launaskrá, gengi gjaldmiðils og vörulista. Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).  

Til að undirbúa gagnaskiptaskilgreiningu fyrir gagnaskrá eða straum er hægt að nota tengt XML-skema til að skilgreina hvaða gagnastak á að hafa með í flýtifliopanum **Dálkskilgreiningar**. Sjá skref 6 í hlutanum „Að lýsa sniði lína og dálka á skrá“. Frekari upplýsingar, sjá [Notkun XML-skema til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Venjulega er gagnaskiptaskilgreiningar settar upp í glugganum **skilgreiningar gagnaskipta** Ef hins vegar er sett upp gagnaskiptaskilgreiningar fyrir þjónustu þar sem gengi gjaldmiðils endurnýjast þarf að hefja ferilinn í einfaldaða **Skipti Gengi Uppfærsla Uppsetning Kort** glugganum.  

> [!NOTE]  
>  Ef skráin sem á að umbreyta er í XML-sniði ætti að túlka hugtakið *„dálkur“* í þessu efnisatriði sem *„XML-einingu sem inniheldur gögn“*.  

Þetta efnisatriði inniheldur eftirfarandi ferli:  

* Til að stofna skilgreiningu gagnaskipta  
* Til að flytja gagnaskiptiskilgreiningu út sem XML skrá til afnota fyrir aðra  
* Til að flytja inn XML-skrá fyrir núverandi skilgreiningu gagnaskipta  

## <a name="to-create-a-data-exchange-definition"></a>Til að stofna skilgreiningu gagnaskipta  
Að stofna skilgreiningu gagnaskipta felur í sér tvö verkefni:  

1. Í **Skilgreiningar gagnaskipta** glugga, lýstu sniði lína og dálka í skránni.  
2. Í **Vörpun gagnaskipta** glugganum skal tengja dálka í gagnaskránni við reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)]  

     Þessu er lýst í eftirfarandi ferli.  

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Að lýsa sniði lína og dálka á skrá.  
1. Í reitnum **Leit** skal færa inn **Gagnaskiptaskilgreiningar** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Á flýtiflipanum **Almennt** skal lýsa gagnaskiptaskilgreiningunni og gagnaskráargerðinni með því að fylla út reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Skilgreining|  
    |---------------------------------|---------------------------------------|  
    |**Kóti**|Færið inn kóða til að auðkenna skilgreiningu gagnaskipta.|  
    |**Heiti**|Færið inn heiti fyrir skilgreiningu gagnaskipta.|  
    |**Skráargerð**|Tilgreinið hvaða tegund af skrá skilgreining gagnaskipta er notað fyrir. Hægt er að velja eftirfarandi þrjár gerðir skjala:<br /><br /> -   **XML**: Lagskiptir efnisstrengir og breytingarmerkingar inni í merkjum sem skilgreina virkni þeirra.<br />-   **Breytilegur texti**: Skráargerð þar sem færslur hafa breytilega lengd og eru aðskilin með tákni, svo sem eins kommu eða semí\-kommu. Einnig þekkt sem *afmörkuð skrá*.<br />-   **Fastur texti**: Færslur eru af sömu lengd, með því að nota talnaborðsstafi og hver færsla er í eigin línu. Einnig þekkt sem *skrá með fastri breidd*.|  
    |**Tegund**|Tilgreinið hvaða tegund af starfsemi skilgreining gagnaskipta er notað fyrir, t.d. **Útflutningur greiðslna**.|  
    |**Meðhöndlunarkóðaeining gagna**|Tilgreinið kóðaeiningu sem flytur gögn inn og út úr töflum í [!INCLUDE[d365fin](includes/d365fin_md.md)]|  
    |**Kóðaeining staðfestingar**|Tilgreinið kóðaeiningu sem er notuð til að sannprófa gögn gegn fyrirfram skilgreindum viðskiptareglum.|  
    |**Les/skrifar kóðaeiningu**|Tilgreinið kóðaeiningu sem vinnur innflutt gögn fyrir vörpun og útflutt gögn eftir vörpun.|  
    |**Les/skrifar XMLport**|Tilgreinið XMLport sem innflutt gagnaskrá eða þjónusta fer gegnum fyrir vörpun og sem flutt gögn fer út um þegar það er skrifað á gagnaskrá eða þjónustu eftir vörpun.|  
    |**Meðhöndlunarkóðaeining ytri gagna**|Tilgreinið kóðaeiningu sem flytur ytri gögn inn og út af Gagnaskiptaramma.|  
    |**Kóðaeining athugasemdar frá notanda**|Tilgreinir kóðaeiningu sem framkvæmir ýmsa hreinsun eftir vörpun, t.d. að merkja línurnar sem fluttar út og eyða tímabundunum færslum.|  
    |**Skráarkóðun**|Tilgreinið kóðun skráar. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Dálkaskiltákn**|Tilgreinið hvernig dálkarnir í skránni eru aðskilin, ef skráin er af gerðinni **Breytilegur texti**|  
    |**Hausalínur**|Tilgreinir hversu margir hausalínur eru í skránni.<br /><br /> Þetta tryggir að gögn í haus séu ekki flutt inn. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Hausamerki**|Ef hauslína er á nokkrum stöðum í skránni skaltu slá inn texta í fyrsta dálkinum á hauslínunni.<br /><br /> Þetta tryggir að gögn í haus séu ekki flutt inn. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Síðufótarmerki**|Ef fótarlína er á nokkrum stöðum í skránni skaltu slá inn texta í fyrsta dálkinum í fótarlínunni.<br /><br /> Þetta tryggir að gögn í síðufót séu ekki flutt inn. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  

4. Á flýtiflipanum **Línuskilgreiningar** skal lýsa línusniði í gagnaskrá með því að fylla út reitina eins og lýst er í eftirfarandi töflu.  

    > [!NOTE]  
    >  Fyrir innflutning á bankayfirlitum er aðeins búin til ein lína fyrir stakt snið bankayfirlitsskár sem á að flytja inn.  
    >   
    >  Til útflutnings á greiðslum er hægt að stofna línu fyrir hverja greiðslugerð sem á að flytja út. Í slíku tilviki sýnir flýtiflipinn **Dálkskilgreiningar** mismunandi dálkar fyrir hverja tegund greiðslu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Kóti**|Færið inn kóða til að auðkenna línuna í skránni.|  
    |**Heiti**|Færið inn heiti sem lýsir línunni í skránni.|  
    |**Dálkafjöldi**|Tilgreinið hversu margir dálkar línan í gagnaskrá hefur. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Gagnalínumerki**|Tilgreinið stöðu á viðkomandi XML-skema einingarinnar sem sýnir aðalfærslu gagnaskrárinnar. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Nafnbil**|Tilgreinið nafnbil sem er væntanlegt í skránni, til að virkja nafnbils staðfestingu. Þennan reit má hafa auðan ef ekki á að virkja fullgildingu nafnabils.|  

5. Endurtakið skref 4 til að búa til línu fyrir hver skráargögn sem á að flytja út.  

     Haldið áfram og á flýtiflipanum **Dálkskilgreiningar** skal lýsa línusniði í gagnaskrá með því að fylla út reitina eins og lýst er í eftirfarandi töflu. Hægt er að nota skipulagsskrá, t.d. .XSD-skrá, fyrir gagnaskrá til að fylla út í flýtiflipann með viðeigandi einingum. Frekari upplýsingar má finna í [Notkun XML-skema til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. Veljið **Sækja skipulagsskrá** á flýtiflipanum **Dálkskilgreiningar**.  
7. Í glugganum **Sækja skráaskipan** skal velja viðeigandi skipulagsskrá og svo hnappinn **Í lagi**. Línur í flýtiflipanum **Dálkskilgreiningar** eru fylltar út í samræmi við skipulag gagnaskrárinnar.  
8. Fyllioð inn í reitina eins og lýst er í eftirfarandi töflu í flýtiflipanum **Dálkskilgreiningar**.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Dálknr.**|Tilgreinið númerið sem endurspeglar stöðu dálksins á línu í skránni.<br /><br /> Fyrir XML-skrár skal tilgreina töluna sem endurspeglar gerð staks í skránni sem inniheldur gögnin.|  
    |**Heiti**|Tilgreinið heiti dálksins.<br /><br /> Fyrir XML-skrár skal tilgreina kóðann sem merkir gögnin sem á að skipta um.|  
    |**Tegund gagna**|Tilgreinið hvort gögn til að skipta eru af taginu **Texti**, **Dagsetning** eða **Tugakerfi**|  
    |**Gagnasnið**|Tilgreinið snið gagnanna ef einhver er. Til dæmis **MM-dd-áááá** ef gagnagerðin er  **Dagsetning**. **Athugið:**  Til að flytja út, tilgreinið gagnasnið í samræmi við [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til að flytja inn skal tilgreina gagnasnið í samræmi við .NET rammann. Frekari upplýsingar eru í [strengjum með sniðum fyrir staðlaðar dagsetningar og tíma](http://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Menning gagnasniðs**|Tilgreinið menningu gagnasniðs, ef einhver er. Til dæmis **en-US** ef gagnagerðin er **Tugastafur** til að tryggja að komma sé notuð sem skiltákn milli þúsunda, .000, samkvæmt bandaríska kerfinu. Frekari upplýsingar eru í [strengjum með sniðum fyrir staðlaðar dagsetningar og tíma](http://go.microsoft.com/fwlink/?LinkID=323466). **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Lengd**|Tilgreinið lengd línu af fastri vídd sem inniheldur dálkinn ef gagnaskráin er af gerðinni **Fastur texti**|  
    |**Lýsing**|Færið inn lýsingu á dálknum til upplýsingar.|  
    |**Slóð**|Tilgreinið stöðu einingar í tengdum XML skema.|  
    |**Auðkenni neikvæðs formerkis**|Færið inn virðið sem notað er í gagnaskránni til að auðkenna neikvæðar upphæðir, í gagnaskránum sem ekki mega innihalda mínusmerki. Þetta kennimerki er notað til að breyta auðkenndu upphæðunum í mínusmerki við innflutning. **Athugið:**  Þessi reitur er aðeins gildur fyrir innflutning.|  
    |**Fasti**|Tilgreinið hvaða gögn sem þú vilt flytja í þessum dálki, ss viðbótarupplýsingar um greiðslugerð. **Athugið**: Þessi reitur er aðeins gildur fyrir útflutning.|  

9. Endurtakið skref 8 fyrir hvert dálki eða XML-stak í gagnaskrá sem inniheldur gögn sem á að skiptast á við [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Næsta skref í því að stofna skilgreiningu gagnaskipta er að ákveða hvaða dálkar eða XML-einingar í gagnaskránni varpast á hvaða reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Tilgreind vörpun ræðst af tilgangi viðskipta í gagnaskránni sem á að skipta og staðbundnum tilbrigðum. Jafnvel SEPA-bankastaðallinn er einnig með staðbundin afbrigði. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður innflutning SEPA CAMT bankayfirlitsskrám \-út\-úr\-boxinu. Þetta er kemur fram í **SEPA CAMT** skilgreiningarfærslukóðanum fyrir gangaskipti í glugganum **Skilgreiningar gagnaskipta**. Upplýsingar um tilgreinda reitavörpun þessa SEPA CAMT stuðnings eru í [Reitavörpun við innflutning á SEPA CAMT skrám](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Að tengja dálka í gagnaskránni við reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)]   
1. Á flýtiflipanum **Línuskilgreiningar** skal velja línuna sem á að varpa dálkum í reiti fyrir og velja svo **Reitavörpun**. Glugginn **Vörpun gagnaskipta** opnast.  
2. Á flýtiflipanum **Almennt** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Töflukenni**|Tilgreinið töflu sem geymir reitina til eða frá sem gögn er skipst á samkvæmt vörpun.|  
    |**Notist sem millitafla**|Tilgreinið hvort taflan sem var valin í **Tafla Kenni** reitnum er millitafla þar sem innflutt gögn eru geymd áður en þeim er varpað á marktöfluna.<br /><br /> Venjulega er notuð millitafla þar sem gagnaskiptaskilgreiningar eru notaðar til að flytja inn og umbreyta rafrænum skjölum, t.d. reikningum lánardrottins í innkaupareikning í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).|  
    |**Heiti**|Sláðu inn heiti fyrir vörpunaruppsetninguna.|  
    |**Kóðaeining forvörpunar**|Tilgreinið kóðaeining sem undirbúa vörpun á milli reita í [!INCLUDE[d365fin](includes/d365fin_md.md)] og ytri gögn.|  
    |**Vörpunarkóðaeining**|Tilgreinið kóðaeiningu sem er notað til að kortleggja tilgreind dálka eða XML-gagnastök í reiti í ​​[!INCLUDE[d365fin](includes/d365fin_md.md)]|  
    |**Kóðaeining eftirávörpunar**|Tilgreinið kóðaeiningu sem lýkur vörpun á milli reita í [!INCLUDE[d365fin](includes/d365fin_md.md)] og ytri gagna. **Athugið:**  Þegar búnaður fyrir umreikningsþjónustu bankagagna er notaður umreiknar kóðaeiningin útflutt gögn úr [!INCLUDE[d365fin](includes/d365fin_md.md)] yfir í almennt snið sem er tilbúið til útflutnings. Til að flytja inn breytir kóðaeiningin ytri gögnum í snið sem hægt er að flytja inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  Á flýtiflipanum **Reitavörpun** skal tilgrina hvaða dálkum á að varpa í hvaða reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að fylla út reitina sem lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Dálknr.**|Tilgreinið hvaða dálk í gagnaskrá sem þú vilt skilgreina kort vörpun fyrir.<br /><br /> Aðeins er hægt að velja dálka sem eru kynntir af línum í flýtiflipanum **Dálkskilgreiningar** í **Skilgreiningar gagnaskipta** glugganum.|  
    |**Reitarkenni**|Tilgreinið hvaða reit dálkurinn í **Dálkur nr.** reitnum tengist.<br /><br /> Aðeins er hægt að velja úr reitum sem eru til í töflunni sem tilgreind var í reitnum **Tafla** á flýtiflipanum **Almennt**.|  
    |**Valfrjálst**|Tilgreinið að vörpun verði sleppt ef reiturinn er auður. **Athugið:** Ef þessi gátreitur er ekki valinn kemur útflutningsvilla upp ef reiturinn er auður. **Athugið**: Þessi reitur er aðeins gildur fyrir útflutning.|  
    |**Auðkenni marktöflu**|Aðeins sýnilegur þegar **Nota sem millitöflu** reitur er valinn.<br /><br /> Tilgreinir töflu sem gildi í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|  
    |**Yfirskrift marktöflu**|Aðeins sýnilegur þegar **Nota sem millitöflu** reitur er valinn.<br /><br /> Tilgreinir heiti töflunnar í reitnum **Auðkenni marktöflu**, sem er taflan sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|  
    |**Auðkenni markreits**|Aðeins sýnilegur þegar **Nota sem millitöflu** reitur er valinn.<br /><br /> Tilgreinir reit í marktöflu sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|  
    |**Yfirskrift markreits**|Aðeins sýnilegur þegar **Nota sem millitöflu** reitur er valinn.<br /><br /> Tilgreinir heiti reits í marktöflu sem gildið í reitnum **Skýringartexti dálks** er varpað á, þegar notuð er millitafla fyrir gagnainnflutning.|  
    |**Valfrjálst**|Aðeins sýnilegur þegar **Nota sem millitöflu** reitur er valinn.<br /><br /> Tilgreinið hvort vörpun á að sleppa ef reitur er tómur. Ef þessi gátreitur er ekki valinn kemur útflutningsvilla upp ef reiturinn er auður.|  

Gagnaskiptaskilgreining er tilbúin til virkjunar fyrir notendur. Frekari upplýsingar er að finna í [Setja upp Rafræn skjöl Sending Móttaka](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Setja upp SEPA kreditfærslu](finance-how-to-set-up-sepa-credit-transfer.md), [Hvernig á að: Setja upp SEPA beingreiðslu](finance-how-to-set-up-sepa-direct-debit.md), og [Setja upp umreikningsþjónustu fyrir bankagögn eða SEPA kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

Þegar stofnuð hefur verið skilgreining gagngaskipta fyrir tiltekna gagnaskrá er hægt að flytja skilgreiningu gagnaskiptanna út sem xml-skrá sem hægt er að nota til að virkja í flýti innflutning á umræddri gagnaskrá. Þessu er lýst í eftirfarandi ferli.  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Til að flytja gagnaskiptiskilgreiningu út sem XML skrá til afnota fyrir aðra  
1. Í reitnum **Leit** skal færa inn **Gagnaskiptaskilgreiningar** og velja síðan viðkomandi tengil.  
2. Velja gagnaskiptiskilgreininguna sem á að flytja út.  
3. Velja skal aðgerðina **Skilgreining gagnaskipta í útflutningi**.  
4. Vista xml skrá sem sýnir skilgreiningu gagnaskipta á viðeigandi staðsetningu.  

    Ef skilgreining gagnaskipta hefur þegar verið stofnuð þarftu bara að flytja inn XML skrá í gagnaskiptarammann. Þessu er lýst í eftirfarandi ferli.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Til að flytja inn núverandi skilgreiningu gagnaskipta  
1. Vista xml skrá sem sýnir skilgreiningu gagnaskipta á viðeigandi staðsetningu.  
2. Í reitnum **Leit** skal færa inn **Gagnaskiptaskilgreiningar** og velja síðan viðkomandi tengil.  
3. Valið er **Nýtt** aðgerð. Glugginn **Skilgreining gagnaskipta** opnast.  
4. Velja skal aðgerðina **Skilgreining gagnaskipta í innflutningi**.  
5. Veljið skrána sem var vistuð í skrefi 1.  

## <a name="see-also"></a>Sjá einnig  
[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Setja upp SEPA-kreditfærslur](finance-how-to-set-up-sepa-credit-transfer.md)  
[Setja upp SEPA-beingreiðslur](finance-how-to-set-up-sepa-direct-debit.md)  
[Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Skjöl á innleið](across-income-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

