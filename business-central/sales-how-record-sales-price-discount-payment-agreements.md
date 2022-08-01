---
title: Skrá sérstök söluverð og afslætti
description: Lýsir því hvernig verðlagning og afsláttarsamningar eru skilgreindir fyrir söluskjöl.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 7022, 7024
ms.date: 06/03/2022
ms.author: bholtorf
ms.openlocfilehash: 2bf0a8881ea896c1728f02f07e5991b284a3ccae
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129849"
---
# <a name="record-special-sales-prices-and-discounts"></a>Skrá sérstök söluverð og afslætti

> [!NOTE]
> 2020 losun Wave 2 kynnt ný, straumlínulagað ferli fyrir uppsetningu og umsjón með verði og afslætti. Ef þú ert nýr viðskiptavinur með nýjustu útgáfuna, þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] styður ýmsar aðferðir við verðhjöðnun, svo sem:

* Eitt verð-passar-allar týpur þar sem vara er alltaf seld á sama verði.
* Sérstökum verðsamningum við tiltekna viðskiptamenn, eða hópa viðskiptavina.
* Herferðir þegar Sala uppfyllir skilyrði fyrir sérstöku tilboði. Til dæmis gætu skilyrðin verið þegar pöntun uppfyllir lágmarksmagn, er á undan ákveðinni dagsetningu eða hefur ákveðna tegund af vöru.  

Til að nota grunnverðslíkan þarf aðeins að tilgreina einingarverð þegar sett er upp vara eða Forði. Það verð verður alltaf notað í söluskjölum. Fyrir ítarlegri líkön, til dæmis, þegar bjóða á upp á Sérstök verð fyrir söluherferð er hægt að tilgreina skilyrði á **síðunni söluverð**. Hægt er að bjóða upp á sérverð eftir samsetningu á eftirfarandi upplýsingum:  

* Viðskiptavinur
* Atriði
* Mælieining
* Lágmarksmagn
* Dagsetningar sem skilgreina tímabilið sem verðin eru gild á.

Eftir að búið er að setja upp sérstakt verð, [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að reikna besta verð í sölu-og innkaupaskjölum, og í vinnslu-og birgðabókarlínum. Frekari upplýsingar er að finna í [Útreikningur besta verðs](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Hægt er að setja upp tvær gerðir fyrir söluafslætti:

| Afsláttargerð | Lýsing |
| --- | --- |
| **Sölulínuafsláttur** |Upphæð sem sett er inn á sölulínur ef þær innihalda ákveðna samsetningu viðskiptavinar, vöru, lágmarksmagn, mælieiningu eða upphafs/lokadagsetningar. Þessi tegund virkar á sama hátt og fyrir söluverð. |
| **Reikningsafsláttur** |Afsláttarprósenta sem er dregin frá samtölu söluskjals ef summa allra lína í skjalinu fer yfir ákveðið lágmark. |

> [!TIP]  
> Ef aldrei á að selja vöru með afslætti skal skilja afsláttarreitinn á vörusíðunni eftir auðan og ekki hafa með vöruna í neinum uppsetningum línuafslátta.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Að setja upp söluverð fyrir viðskiptamann

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikann, er skrefunum á flipanum upplifun fylgt. 

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Velja skal viðskiptamanninn og síðan velja aðgerðina **Verð**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakt söluverð fyrir viðskiptamanninn.

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

Sjálfgefið er að staða nýrra verðlista sé Drög. Drög að verðlista eru ekki innifalin í verðútreikningum. Þegar búið er að bæta við línum og byrja á að nota verðin skal breyta stöðunni í virka stöðu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**. 
3. Veljið **Nýtt** til að stofna nýja söluverðslista.
4. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt** og **Skattur**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Ef bæta á atriðum á listann er ein af eftirtöldum skrefum bætt við:
   * Til að bæta við mörgum vörum skal velja **Leggja til línur** og síðan færa inn síuskilyrði til að tilgreina gerðir af vörum sem bæta á við. Einnig er hægt að færa inn aðrar stillingar fyrir vörurnar sem eiga sérstaklega við verðlistann. Hægt er að breyta þessum stillingum síðar, ef þörf krefur.
   * Til að afrita vörur úr öðrum verðlista skal velja **Afrita línur** og síðan velja verðlistann sem á að afrita.
   * Til að bæta vörum við handvirkt skal í hnitanetinu í reitnum **Gerð afurðar** velja gerð afurðar sem verðlistinn er fyrir. Fyllið inn í eftirstandandi reiti eftir þörfum, eftir vali. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Til að byrja að nota verðlistann skal í reitnum **Staða** velja **Virkur**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verðlistar sölu og innkaupa notaðir
> [!NOTE]
> Til að nota verðlista þarf stjórnandinn að hafa kveikt á eiginleikauppfærslunni **Ný söluverðsupplifun** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Flestar nýjar upplifanir á söluverðunum eru svipaðar og núverandi upplifun, en þó er nokkur munur. Þeim mismun er lýst í eftirfarandi köflum.

**Á við um gerð** og **Á við um nr.** reitirnir gera kleift að velja hvað verðlisti gildir fyrir, t.d. viðskiptamann eða verðflokk viðskiptamanns. Með notkun **skoðunardálka fyrir** er hægt að sýna eða fela dálka sem eiga við stillingu verð, afslætti eða verð og afslætti.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Fyrirliggjandi verðum breytt þegar kveikt er á eiginleikauppfærslu verðlagningar
Þegar eiginleikauppfærslan **Ný söluverðsupplifun** er virkjuð á síðunni **Eiginleikastjórnun** opnast leiðsögnin **Gagnauppfærsla eiginleika**. Notaðu víxlhnappinn **Nota sjálfgefin verð** á eftirfarandi hátt:

* Ef þú vilt vinna með öll verð á einni síðu skaltu kveikja á honum. Fyrirliggjandi verð verða breytt í eina sjálfgefna Verðskrá fyrir hvert eftirtalinna skjala:

    * Sölur
    * Innkaup
    * Verksala
    * Verkinnkaup 

    Hægt er að breyta öllum verðum þessara svæða á **síðunni verð vinnublaðs**. Sjálfgefnu verðlistarnir verða stilltir á **uppsetningu sölu&**, **innkaupa &** og **uppsetningarsíðum verka**. 

> [!NOTE]
> Ef verð eru aðeins stillt á vöru eða forðaspjöldum verða Sjálfgefnir verðlistar ekki fylltir út með þessum verðum við uppfærslu aðgangsgagna. Hins vegar er hægt að opna sjálfgefna verðlista eða verðsíðu vinnublaðs og nota aðgerðina **Tillögur um línur** til að bæta við verðunum sem stillt eru á vöru- eða tilfangaspjöldum. 

* Til að nota söluverðlista skal slökkva á honum. Fyrirliggjandi verð verða umreiknuð í nýja Verðskrá fyrir hverja samsetningu eftirtalinna hluta: 

* Viðskiptavinur
* Viðskiptavinaflokkur eða herferð
* Upphafs-og lokadagsetningar
* Gjaldmiðlar 

Ef þú ert með margar samsetningar þá færðu marga verðlista.

Ef þegar hefur verið virkjað nýja Verðlagsupplifun er hægt að stofna sjálfgefna verðlista handvirkt eða tilgreina eldri verðlista sem eru sjálfgefnir. Til að stilla núverandi verðlista sem sjálfgefinn skaltu kveikja á víxlhnappnum **Leyfa uppfærslu sjálfgilda** í verðlistanum. Á síðunum **Uppsetning sölugrunns**, **Uppsetning innkaupagrunns** eða **Uppsetning verka** skal síðan stilla verðlistann sem sjálfgefinn.

### <a name="editing-active-price-lists"></a>Virkum verðlistum breytt
Til að gera fólki kleift að breyta verði á virkum verðlistum fyrir vörur, tilföng, viðskiptamenn, lánardrottna eða aðrar einingar sem nota verðlagningu skal kveikja á víxlhnappnum **Leyfa breytingar á virku verði** á síðunum **Uppsetning sölugrunns** og **Uppsetning innkaupagrunns**.   

Þegar slökkt er á víxlhnappnum **Leyfa breytingar á virku verði**, til að uppfæra verð í verðlista þarf að breyta stöðu verðlistans í **Drög**, gera breytinguna og síðan endurvirkja verðlistann.

Síðan **Verðyfirlit** gefur yfirlit yfir öll verð í verðlistum. Hægt er að setja afmarkanir til að þrengja listann yfir verð sem má breyta eða bæta við. Eftir að verð hefur verið breytt verður að nota **aðgerðina sannprófa línur** til að sannreyna verð gagnvart öðrum verðlistalínum. Ef reynt er að sannprófa verð er auðveldara að forðast tvítekningar og umreiknisemi við verðútreikninga. 

> [!NOTE]
> Þegar línu er breytt í virkri Verðskrá verður staða línunnar Dræg og línan verður ekki tekin til greina við verðútreikninga fyrr en aðgerðin sannprófa línur **er notuð**. Eftir að búið er að staðfesta verðið staða línunnar verður virk og hún verður tekin til greina í verðútreikningum.

Til að bæta við nýjum verðum á síðunni **Verðyfirlit** skal nota aðgerðina **Bæta við nýjum línum**. **Vinnublaðssían** opnar og hægt er að bæta við verðlínum annaðhvort með því að leggja þær til grundvallar í skilyrðum, afrita þær úr öðrum verðlistum eða færa þær handvirkt inn. Í kjölfarið er hægt að nota **aðgerðina innleiða verðbreytingu** til að bera saman nýja verð með öðrum verðlistum til að forðast tvítekningar og umbreytingar við verðútreikninga.

## <a name="to-copy-sales-prices"></a>Til að afrita söluverð
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikann, er skrefunum á flipanum upplifun fylgt.

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)  

Ef afrita á söluverð, svo sem söluverð tiltekins viðskiptamanns, og nota í verðflokki viðskiptamanna þarf að keyra **Leggja til söluverð á vinnublaði.** runuvinnslan á síðunni **Vinnublað söluverðs**.  

1. Velja skal ![ljósaperu sem opnar teiknið segja mér eiginleika](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), setja inn **Vinnublað** söluverðs og velja síðan tengda tengilinn.  
2. Velja skal **Leggja til söluverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Söluverð** skal færa þá **tegund sölu** og **kóta sölu** sem gilda í söluverðinu sem á að afrita inn í reitina.  
4. Efst á beiðnisíðunni er fyllt út í reitunum **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.  
5. Ef stofna á nýtt verð í keyrslunni er gátreiturinn **Stofna nýtt verð** valinn.  
6. **Hnappurinn í lagi** er valinn til að færa inn í línurnar á **síðu vinnublaðs** söluverðs með tillögur um nýtt verð, sem gefa til kynna að þær séu gildar fyrir völdu sölugerðina.  

   > [!NOTE]  
   > Keyrslan gerir aðeins tillögur, hún framkvæmir ekki breytingarnar. Ef tillögurnar eru viðunandi og eiga að taka gildi, þ.e. setja þær á síðuna **Söluverð** skal velja aðgerðina **Innleiða verðbreytingar** á síðunni **Vinnublað söluverðs**.

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  
Hægt er að tilgreina hvort nýja verðlistinn muni nota stillingarnar úr hausnum á listanum sem afritað er eða stillingarnar af nýja listanum sem á að afrita. Til að nota stillingarnar úr verðlistanum sem verið er að afrita verð til skal kveikja á **notkun sjálfgildi úr Mark** -víxlun.

1. Velja skal ![ljósapera sem opnar teiknið segja mér eiginleika](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), færa inn **söluverðalista** og velja síðan tengda tengilinn. 
2. Velja skal verðlistann sem á að afrita og velja síðan **Afrita línur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Ekki er hægt að hafa tvo hluti sem hafa sömu stillingar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlistinn er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  
  
---

## <a name="to-bulk-update-item-prices"></a>Til að magnuppfæra vöruverð
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikann, er skrefunum á flipanum upplifun fylgt.

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)

Til að magnuppfæra vöruverð, eins og að hækka öll verð með prósentum, er hægt að fylla út vinnublaðssíðu söluverðs með því að nota eftirfarandi runuvinnslur:

* **Leggja til söluverð á Wksh.** Bendir til breytinga á annan af tveim leiðum. Annað hvort með því að beita leiðréttingarstuðli að núverandi söluverði eða með því að afrita fyrirliggjandi samninga um söluverð til annarra viðskiptamanna, verðflokka viðskiptamanna eða söluherferðir.
* **Leggja til vöruverð á vinnublaði** Bendir til breytinga á annan af tveim leiðum. Annaðhvort með því að beita leiðréttingarstuðli að núverandi einingarverði á birgðaspjöldum, eða með því að leggja til verð fyrir nýjar samsetningar af gjaldmiðli, mælieiningum, o. frv. Keyrslan verður ekki breytt í einingaverð á vörum.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnublað söluverðs** og veldu síðan tengda tengilinn.  
2. Veldu **Leggja til vöruverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Vara** er reiturinn **Nr.** fylltur út eða **Birgðabókunarflokkur** eða aðrir reitir með upprunalegu vöruverði sem á að uppfæra.  
4. Efst á beiðnisíðunni er fyllt út í **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.
5. Ef þú vilt að keyrslan leiðrétti sjálfkrafa tillögur að vöruverðum skal slá inn leiðréttingu í reitinn **Leiðréttingarstuðull**. Til dæmis myndir þú slá inn 1,15 í **Leiðréttingarstuðull** fyrir 15% hækkun á vöruverði.  
6. Ef runuvinnslan á að stofna ný verð skal kveikja á víxlhnappnum **Stofna nýtt verð**.  
7. **Hnappurinn í lagi** er valinn til að færa inn í línurnar á **síðu vinnublaðs** söluverðs með leiðbeinandi nýju verði.
8. Til að innleiða tillögurnar skal nota aðgerðina **Innleiða verðbreytingar**. Keyrslan stofnar tillögur en útfærir þær ekki. 

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)

Til að uppfæra verð fyrir margar vörur þarf að búa til nýjam verðlista og afrita síðan línurnar úr fyrirliggjandi verðlista. Þegar línur eru afritaðar er hægt að nota síur til að tilgreina hvað eigi að afrita og hægt er að tilgreina heiltölu eða tugabrot í reitnum **Leiðréttingarstuðull** til að hækka eða lækka verð. Verðlistinn verður að vera í stöðunni **Drög**. Ef þörf krefur er hægt að gera eldri verðlistann óvirkan.

> [!NOTE]
> Ekki er hægt að hafa tvær línur sem hafa sömu stillingar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  

---

## <a name="best-price-calculation"></a>Útreikningur besta verðs

Þegar búið er að skrá sérstakt verð og línuafslátt fyrir sölu og innkaup [!INCLUDE[prod_short](includes/prod_short.md)] reiknar besta verðið í sölu-og innkaupaskjölum og í vinnslu-og birgðabókarlínum.

Besta verðið er lægsta verðið með hæsta línuafslátt sem leyfður er á tiltekinni dagsetningu. [!INCLUDE[prod_short](includes/prod_short.md)] reiknar út besta verðið þegar það bætir við einingarverði og afsláttarprósentu línuafsláttar í skjala-og færslubókarlínum.

> [!NOTE]  
> Eftirfarandi lýsir því hvernig besta verð er reiknað fyrir sölu. Fyrir innkaup eru Útreikningarnir Svipaðir en er byggður á tiltækum færibreytum. Til dæmis eru Vöruafsláttarflokkar ekki studdir fyrir innkaup.

1. [!INCLUDE[prod_short](includes/prod_short.md)]kannar samsetningu reikningsfærslu á viðskiptamann og vöru og velur svo rétt viðeigandi verð og afslátt samkvæmt eftirfarandi skilyrðum:

    * Er þessi viðskiptamaður með sérstakan samning um verð eða línuafslætti, eða tilheyrir viðskiptamaðurinn hóp með slíkan samning?
    * Fellur varan eða vöruafsláttarflokkurinn á línunni undir þessa samninga?
    * Er pöntunardagsetningin (eða bókunardagsetning reikningsins og kreditreikningsins) á milli upphafs- og lokadagsetningar verðs/línuafsláttar?
    * Er mælieiningarkóti tilgreindur? Ef svo er leitar [!INCLUDE[prod_short](includes/prod_short.md)] að verði/línuafslætti með sama mælieiningarkóða og verði/afslætti án mælieiningarkóða.

2. [!INCLUDE[prod_short](includes/prod_short.md)] Athugar hvort einhver verð-/afsláttarsamningar eigi við upplýsingar í skjalinu eða færslubókarlínunni. Þar setur hann inn viðeigandi einingaverð og línuafsláttarprósentu með eftirfarandi skilyrðum:

    * Er krafa um lágmarksmagn til staðar í samningi um verð/afslátt sem er uppfyllt?
    * Er krafa um gjaldmiðil til staðar í samningi um verð/afslátt sem er uppfyllt? Ef svo er, er lægsta verðið og hæsti línuafsláttur fyrir þann gjaldmiðil bætt við, jafnvel þótt staðbundinn gjaldmiðill myndi veita betra verð. Ef ekkert verð-/afsláttarsamkomulag er fyrir tilgreindan gjaldmiðilskóta skal [!INCLUDE[prod_short](includes/prod_short.md)] Setja inn lægsta verðið og hæsta línuafsláttinn í staðbundna gjaldmiðilinn þinn.

Ef ekkert verð finnst fyrir vörurnar á línunni er síðasta innkaupsverð eða einingaverð sótt af birgðaspjaldinu eða birgðahaldseiningarspjaldinu.

## <a name="sales-invoice-discounts-and-service-charges"></a>Afslættir Sölureiknings og Þjónustugjöld

Þegar reikningsafslættir eru notaðir fer afslátturinn sem er veittur eftir því hve reikningsupphæðin er há. Á síðunni **Reikningsafsláttur viðskm** er einnig hægt að leggja þjónustugjald á reikninga sem eru yfir tiltekinni upphæð.  

Áður en hægt er að veita reikningsafslátt af sölu þarf að tilgreina tilteknar upplýsingar. Taka þarf eftirfarandi ákvarðanir:  

* Hvaða Viðskiptavinir fái þessa tegund afsláttar?  
* Hvaða afsláttarprósentur þú notar?  

Ef þú vilt að reikningsafslættir séu reiknaðir sjálfkrafa skal á síðunni **Uppsetning sölugrunns** kveikja á víxlhnappnum **Reikna út reikningsafslátt**.  

Hægt er að tilgreina hvort veita eigi reikningsafslátt þegar reikningur uppfyllir ákveðin skilyrði fyrir hvern viðskiptavin. Til dæmis þegar reikningsupphæð er nógu stór. Reikningsafsláttur getur verið í staðbundnum gjaldmiðli fyrir innlenda viðskiptavini eða í erlendri mynt til erlendra viðskiptavina.  

Afsláttarprósentur eru **tengiltvinnupphæðir á tilteknar reikningsupphæðir á síðunni reikningsafsláttarafsláttur** fyrir hvern viðskiptamann. Hægt er að færa inn hvaða prósentutölu sem er. Hver viðskiptamaður getur haft sína eigin síðu, eða þá að hægt er að tengja nokkra viðskiptamenn saman á síðu.  

Til viðbótar við eða í staðinn fyrir afsláttarprósentu er hægt að tengja ákveðið þjónustugjald við ákveðna reikningsupphæð.  

> [!TIP]  
> Áður en hafist er handa við að setja upplýsingarnar inn í forritið er gott að útbúa uppkast af því afsláttarformi sem á að nota. Þannig er auðveldara að átta sig á því hvaða viðskiptamenn er hægt að tengja við sama reikningsafsláttarsíðu. Eftir því sem setja þarf upp færri síður, þeim mun fljótlegra er að færa inn grunnupplýsingarnar.

Frekari þjálfun fyrir afslætti á sölum er að finna í [Setja upp afslætti fyrir viðskiptamenn þína](/learn/modules/customer-discounts-dynamics-365-business-central/index) í Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Reikna reikningsafsl. á sölu

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sölulínuafsláttur stofnaður fyrir viðskiptamann
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikann, er skrefunum á flipanum upplifun fylgt.

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið svo aðgerðina **Línuafslættir**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakan sölulínuafslátt fyrir viðskiptamanninn.

> [!NOTE]
> Þegar söluverðið **og** Sölulínuafsláttin **eru opnuð** frá tilteknum viðskiptamanni **eru reitirnir sölutegund síu** og **Kóti sölukóða** stilltir fyrir viðskiptavininn og ekki er hægt að breyta honum eða fjarlægja hann.
>
> Til að setja upp verð eða línuafslætti fyrir alla viðskiptamenn, verðflokk viðskiptamanns eða herferð verður að opna síðurnar af birgðaspjaldi. Einnig er hægt að nota síðuna **Vinnublað söluverðs** fyrir söluverð. Frekari upplýsingar eru í [Til að magnuppfæra vöruverð](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**.
3. Opnið verðlistann þar sem tilgreina á línuafsláttinn.
4. Stofnið nýja línu eða veljið fyrirliggjandi línu og fyllið svo út í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Í reitnum **Skilgreinir** skal velja annaðhvort **Verð og afsláttur** eða aðeins **Afsláttur**. 
6. Í reitnum **Línuafsláttur %** skal tilgreina afsláttarprósentuna.

    > [!TIP]
    > Ef verið er að breyta fyrirliggjandi línu er hægt að sía línurnar með því að velja viðeigandi valkost í reitnum **Skoða dálka fyrir**.

    > [!NOTE]  
    > Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála. Til að setja upp sérstaka skilmála reikningsafsláttar fyrir viðskiptamann skal stilla reitinn **Kóði reikningsafsláttar** á viðskiptamannakóða viðskiptamanns og síðan halda áfram yfir í næsta skref.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Að setja upp reikningsafslátt fyrir viðskiptamann
Þegar búið er að ákveða hvaða viðskiptamenn eiga rétt á reikningsafslætti skal færa inn reikningsafsláttarkótann á síðum viðskiptamannaspjald. Setjið síðan upp skilmálana fyrir hvern kóta.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna skal síðu viðskiptamanns sem getur fengið reikningsafslátt.
3. Í reitinn **Reikningsafsláttarkóði** er færður inn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir viðskiptamanninn. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála.

Næsta skref er að setja upp nýja skilmála fyrir sölureikningsafslætti.

1. Á síðunni **Viðskiptamenn** skal velja aðgerðina **Reikningsafslættir**. Síðan **Reikningsafsláttur viðskm.** opnast.
2. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilyrði í ISK.
3. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
4. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
5. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem viðskiptamaðurinn mun fá mismunandi reikningsafslátt í.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Uppsetning verðflokka viðskiptamanna](sales-how-to-set-up-customer-price-groups.md)  
[Uppsetning afsláttarflokka viðskiptamanna](sales-how-to-set-up-customer-discount-groups.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]