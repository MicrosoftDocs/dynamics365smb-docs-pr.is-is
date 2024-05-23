---
title: Skrá sérstök söluverð og afslætti
description: Lýsir því hvernig á að skilgreina verðlagningu og afsláttarsamninga fyrir söluskjöl.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 06/13/2023
ms.custom: bap-template
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '7022, 7024'
ms.service: dynamics-365-business-central
---

# <a name="record-special-sales-prices-and-discounts"></a>Skrá sérstök söluverð og afslætti

> [!NOTE]
> Á útgáfutímabili 2 árið 2020 kynntum við einfaldari ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður sem ert að nota nýjustu útgáfu þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna í [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management) í efni stjórnenda.

[!INCLUDE[prod_short](includes/prod_short.md)] styður ýmsar verðlagningarleiðir eins og:

* „Eitt verð fyrir allt“ líkön þar sem vara er alltaf seld á sama verðinu.
* Sérstakir verðsamningar við tiltekna viðskiptavini, eða hópa viðskiptavina.
* Herferðir þegar sala uppfyllir skilyrði fyrir sértilboð. Til dæmis gætu eftirfarandi skilyrði verið fyrir pöntun:

  * Það uppfyllir lágmarksmagn
  * Það er fyrir ákveðna dagsetningu
  * Hún felur í sér ákveðna tegund vöru  

Til að nota einfalt verðlagningarlíkan þarf aðeins tilgreina einingarverð þegar vara eða tilfang er sett upp. Það verð verður alltaf notað í söluskjölum. Fyrir flóknari líkön, til dæmis þegar boðið er upp á sérverð fyrir söluherferð, er hægt að tilgreina skilyrði á síðunni **Söluverð**. Hægt er að bjóða sérverð sem byggja á samsetningum af eftirfarandi upplýsingum:  

* Viðskiptavinur
* Atriði
* Mælieining
* Lágmarksmagn
* Dagsetningar sem skilgreina tímabilið sem verðin gilda fyrir.

Þegar sérverð hafa [!INCLUDE[prod_short](includes/prod_short.md)]  verið sett upp getur það reiknað út besta verð á sölu- og innkaupaskjölum og í línum í verk- og birgðabókum. Frekari upplýsingar má finna á [Útreikningur besta verðs](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Til að fá söluafslátt er hægt að setja upp tvær gerðir:

| Afsláttargerð | Heimildasamstæða |
| --- | --- |
| **Sölulínuafsláttur** |Bæta við upphæð í sölulínum sem hafa ákveðna samsetningu á viðskiptamanni, vöru, lágmarksmagni, mælieiningu eða upphafs- og lokadagsetningu. Þetta virkar á sama hátt og fyrir söluverð. |
| **Reikningsafsláttur** |Afsláttarprósenta sem er dregin frá samtölu söluskjals ef summa allra lína í skjalinu fer yfir ákveðið lágmark. |

> [!TIP]  
> Ef aldrei á að selja vöru með afslætti skal skilja afsláttarreitinn á vörusíðunni eftir auðan og ekki hafa með vöruna í neinum uppsetningum línuafslátta.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Að setja upp söluverð fyrir viðskiptamann

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum „Núverandi upplifun“. 

#### [Núverandi reynsla](#tab/current-experience/)

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Velja skal viðskiptamanninn og síðan velja aðgerðina **Verð**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakt söluverð fyrir viðskiptamanninn.

#### [Ný reynsla](#tab/new-experience/)  

Sjálfgefið er að staða nýrra verðlista sé **Drög**. Drög að verðlistum eru ekki tekin með í verðútreikningum. Þegar búið er að bæta við línum og byrja á að nota verðin skal breyta stöðunni í **Virka** stöðu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**. 
3. Veljið **Nýtt** til að stofna nýja söluverðslista.
4. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt** og **Skattur**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Til að bæta vörum við listann skal gera eitt af eftirfarandi:
   * Til að bæta við mörgum vörum skal velja **Leggja til línur** og síðan færa inn síuskilyrði til að tilgreina gerðir af vörum sem bæta á við. Einnig er hægt að færa inn aðrar stillingar fyrir vörurnar sem eiga við um verðlistann. Þú getur breytt þessum stillingum síðar ef þörf er á.
   * Til að afrita vörur úr öðrum verðlista skal velja **Afrita línur** og síðan velja verðlistann sem á að afrita.
   * Til að bæta vörum við handvirkt skal í hnitanetinu í reitnum **Gerð afurðar** velja gerð afurðar sem verðlistinn er fyrir. Fyllið inn í eftirstandandi reiti eftir þörfum, eftir vali. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Til að byrja að nota verðlistann skal í reitnum **Staða** velja **Virkur**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verðlistar sölu og innkaupa notaðir

> [!NOTE]
> Til að nota verðlista þarf stjórnandinn að hafa kveikt á eiginleikauppfærslunni **Ný söluverðsupplifun** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna í [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management) í efni stjórnenda.

Mest af nýju upplifuninni af söluverði svipar til núverandi upplifunar, en nokkrir hlutir eru öðruvísi. Þessi mismuni er lýst í eftirfarandi hlutum.

**Á við um gerð** og **Á við um nr.** reitirnir gera kleift að velja hvað verðlisti gildir fyrir, t.d. viðskiptamann eða verðflokk viðskiptamanns. Með því að nota **Skoða dálka fyrir** er hægt að sýna eða fela dálka sem tengjast því að stilla verð, afslætti eða verð og afslætti.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Fyrirliggjandi verðum breytt þegar kveikt er á eiginleikauppfærslu verðlagningar

Þegar eiginleikauppfærslan **Ný söluverðsupplifun** er virkjuð á síðunni **Eiginleikastjórnun** opnast leiðsögnin **Gagnauppfærsla eiginleika**. Notaðu víxlhnappinn **Nota sjálfgefin verð** á eftirfarandi hátt:

* Ef þú vilt vinna með öll verð á einni síðu skaltu kveikja á honum. Fyrirliggjandi verðum verður breytt í einn sjálfgefinn verðlista fyrir hvert af eftirfarandi skjölum:

  * Sölur
  * Innkaup
  * Verksala
  * Verkinnkaup

  Hægt er að breyta öllum verðum fyrir þessi svæði á síðunni **Vinnublað verðs**. Sjálfgefnir verðlistar verða stilltir á síðunum Sölugrunnur, **Innkaupagrunnur** **og** Verkagrunnur **.** 

> [!NOTE]
> Ef verð eru aðeins stillt á vöru- eða forðaspjölum verða sjálfgefnir verðlistar ekki fylltir út með þessum verðum við gagnauppfærslu. Hins vegar er hægt að opna sjálfgefna verðlista eða síðuna **Vinnublað verðs** og nota aðgerðina **Tillögur um línur** til að bæta við verðunum sem stillt eru á vöru- eða forðaspjöldum.

* Til að nota söluverðlista skal slökkva á honum. Fyrirliggjandi verðum verður breytt í nýjan verðlista fyrir hverja samsetningu af eftirfarandi atriðum:

  * Viðskiptavinur
  * Viðskiptamannaflokkur eða söluherferð
  * Upphafs- og lokadagsetningar
  * Gjaldmiðlar

Ef þú ert með margar samsetningar færðu marga verðlista.

Ef þú hefur þegar virkjað nýju verðupplifunina getur þú búið til sjálfgefna verðlista handvirkt eða tilgreint núverandi verðlista sem sjálfgefinn. Til að stilla núverandi verðlista sem sjálfgefinn skaltu kveikja á víxlhnappnum **Leyfa uppfærslu sjálfgilda** í verðlistanum. Á síðunum Sölugrunnur, **Innkaup eða Uppsetning verka, á síðunum** Sölugrunnur **, Innkaup** eða **Uppsetning** verka, er verðlistinn stilltur sem sjálfgefinn.

### <a name="editing-active-price-lists"></a>Breyta virkum verðlistum

Til að gera fólki kleift að breyta verði á virkum verðlistum fyrir vörur, tilföng, viðskiptamenn, lánardrottna eða aðrar einingar sem nota verðlagningu skal kveikja á víxlhnappnum **Leyfa breytingar á virku verði** á síðunum **Uppsetning sölugrunns** og **Uppsetning innkaupagrunns**.

Þegar slökkt er á víxlhnappnum **Leyfa breytingar á virku verði**, til að uppfæra verð í verðlista þarf að breyta stöðu verðlistans í **Drög**, gera breytinguna og síðan endurvirkja verðlistann.

Síðan **Verðyfirlit** gefur yfirlit yfir öll verð í verðlistum. Hægt er að setja síur til að þrengja listann yfir verð sem þú gætir viljað breyta eða bæta við. Þegar verðum hefur verið breytt þarftu að nota aðgerðina **Staðfesta línur** til að staðfesta verðin á móti öðrum verðlistalínum. Með því að staðfesta verð er hægt að koma í veg fyrir tvítekningar og tvíræðni við verðútreikninga.

> [!NOTE]
> Þegar línu er breytt í virkum verðlista verður staða línunnar að **Drögum** og línan verður ekki tekin til greina í verðútreikningum fyrr en þú notar aðgerðina **Staðfesta línur**. Þegar verð hefur verið staðfest verður staða línunnar **Virk** og hún verður notuð í verðútreikningum.

Til að bæta við nýjum verðum á síðunni **Verðyfirlit** skal nota aðgerðina **Bæta við nýjum línum**. Síðan **Vinnublað verðs** opnast og þú getur bætt við verðlínum annaðhvort með því að leggja þau til samkvæmt skilyrði, afrita þau úr öðrum verðlistum eða slá þau inn handvirkt. Eftir á er hægt að nota aðgerðina **Innleiða verðbreytingu** til að bera nýju verðin saman við aðra verðlista til að forðast tvítekningar og tvíræðni í verðútreikningum.

#### <a name="create-sales-price-lines-based-on-the-unit-price"></a>Stofna söluverðslínur á grundvelli einingarverðs

1. Á síðunni **Vinnublað verðs** skal velja aðgerðina **Tillögur um línur**.
2. Á síðunni **Verðlínur - Stofna nýja** skal fylla út reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Vörusía** skal skilgreina síur fyrir valda **Vörutegund**
4. Veldu reitinn **Sjálfgefið** til að tilgreina stillingar eins og:
   * Hvaða einingum verðlistanum á að vera úthlutað til.
   * Dagsetningar þegar verðið gildir.
   * Gjaldmiðilskóðinn.
   * Síu fyrir gerð upphæðar sem skilgreinir dálkana sem birtast í línum verðlistans.
5. Velja **Í lagi**. Nýjum línum verður bætt við síðuna **Vinnublað verðs** með völdum stillingum og einingarverðum úr birgðaspjöldunum.
6. Breyta línunum sem eru búnar til með nýja einingarverðinu eða afsláttunum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="create-sales-price-lines-based-on-existing-price-lists"></a>Stofna sölulínur á grundvelli fyrirliggjandi verðlista

1. Á síðunni **Vinnublað verðs** skal velja aðgerðina **Afrita línur**.
2. Á síðunni **Verðlínur - Afrita fyrirliggjandi** skal velja fyrirliggjandi verðlista í reitnum **Úr verðlista**.
3. Í reitnum **Verðlínusía** skal skilgreina síur fyrir vörurnar í völdum verðlista.
4. Veldu reitinn **Sjálfgefið** til að tilgreina stillingar eins og:
   * Hvaða einingum verðlistanum á að vera úthlutað til.
   * Dagsetningar þegar verðið gildir.
   * Gjaldmiðilskóðinn.
   * Síu fyrir gerð upphæðar sem skilgreinir dálkana sem birtast í línum verðlistans.
5. Fylltu út hina reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Velja **Í lagi**. Nýjum línum verður bætt við síðuna **Vinnublað verðs** með völdum stillingum.
7. Breyta línunum sem eru búnar til með nýja einingarverðinu eða afsláttunum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-sales-prices"></a>Til að afrita söluverð

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum „Núverandi upplifun“.

#### [Núverandi reynsla](#tab/current-experience/)  

Ef afrita á söluverð, svo sem söluverð tiltekins viðskiptamanns, og nota í verðflokki viðskiptamanna þarf að keyra **Leggja til söluverð á vinnublaði.** runuvinnslan á síðunni **Vinnublað söluverðs**.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnublað söluverðs** og veldu síðan tengda tengilinn.  
2. Velja skal **Leggja til söluverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Söluverð** skal færa þá **tegund sölu** og **kóta sölu** sem gilda í söluverðinu sem á að afrita inn í reitina.  
4. Efst á beiðnisíðunni er fyllt út í reitunum **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.  
5. Eigi keyrslan að stofna nýtt verð er gátreiturinn **Stofna nýtt verð** valinn.  
6. Veldu hnappinn **Í lagi** til að setja nýtt verð í línurnar á síðunni **Vinnublað söluverðs** með nýju verðtillögunum sem gefur til kynna að þau gildi fyrir þá tegund sölu sem var valin.  

   > [!NOTE]  
   > Keyrslan gerir aðeins tillögur, hún framkvæmir ekki breytingarnar. Ef tillögurnar eru viðunandi og eiga að taka gildi, þ.e. setja þær á síðuna **Söluverð** skal velja aðgerðina **Innleiða verðbreytingar** á síðunni **Vinnublað söluverðs**.

#### [Ný reynsla](#tab/new-experience/)  

Hægt er að tilgreina stillingarnar sem verðlistinn á að nota:

* Stillingarnar í hausnum eru notaðar á listanum sem verið er að afrita.
* Stillingarnar af listanum sem verið er að afrita í eru notaðar. Til að nota stillingarnar úr verðlistanum sem þú afritar verðin í skaltu kveikja á **Nota sjálfgefið úr markmiði**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Söluverðlistar** og veldu síðan tengda tengilinn.
2. Velja skal verðlistann sem á að afrita og velja síðan **Afrita línur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Ekki er hægt að vera með tvo hluti með sömu stillingar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  
  
---

## <a name="to-bulk-update-item-prices"></a>Til að magnuppfæra vöruverð

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum „Núverandi upplifun“.

#### [Núverandi reynsla](#tab/current-experience/)

Til að uppfæra mörg vöruverð í einu, t.d. hækka öll verð um sömu prósentuna, er hægt að fylla út síðuna „Vinnublað söluverðs“ með því að nota eftirfarandi runuvinnslur:

* **Leggja til söluverð á vinnublaði** Leggur til breytingar á annarri af tveimur leiðum:

  * Með því að nota leiðréttingarstuðul við fyrirliggjandi söluverð.
  * Með því að afrita fyrirliggjandi söluverðssamninga yfir á aðra viðskiptamenn, verðflokka viðskiptamanna eða söluherferðir.

* **Leggja til vöruverð á vinnublaði** Leggur til breytingar á annarri af tveimur leiðum:

  * Með því að nota leiðréttingarstuðul við fyrirliggjandi einingarverð á birgðaspjöldum.
  * Með því að leggja til verð fyrir nýjar samsetningar af gjaldmiðli, mælieiningum og svo fram vegar.

  Þessi keyrsla breytir ekki einingarverði vara.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnublað söluverðs** og veldu síðan tengda tengilinn.  
2. Veldu **Leggja til vöruverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Vara** er reiturinn **Nr.** fylltur út eða **Birgðabókunarflokkur** eða aðrir reitir með upprunalegu vöruverði sem á að uppfæra.  
4. Efst á beiðnisíðunni er fyllt út í **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.
5. Ef þú vilt að runuvinnslan leiðrétti sjálfkrafa tillögur að vöruverðum skal slá inn leiðréttingu í reitinn **Leiðréttingarstuðull**. Til dæmis myndir þú slá inn 1,15 í **Leiðréttingarstuðul** fyrir 15% hækkun á vöruverði.  
6. Ef runuvinnslan á að stofna ný verð skal kveikja á víxlhnappnum **Stofna nýtt verð**.  
7. Veldu hnappinn **Í lagi** til að setja nýju verðtillögurnar í línurnar á síðunni **Vinnublað söluverðs**.
8. Til að innleiða tillögurnar skal nota aðgerðina **Innleiða verðbreytingar**. Runuvinnslan býr til tillögur en innleiðir þær ekki. 

#### [Ný reynsla](#tab/new-experience/)

Til að uppfæra verð fyrir margar vörur þarf að búa til nýjam verðlista og afrita síðan línurnar úr fyrirliggjandi verðlista. Þegar línur eru afritaðar er hægt að nota síur til að tilgreina hvað eigi að afrita og hægt er að tilgreina heiltölu eða tugabrot í reitnum **Leiðréttingarstuðull** til að hækka eða lækka verð. Verðlistinn verður að vera í stöðunni **Drög**. Ef þörf krefur er hægt að gera eldri verðlistann óvirkan.

> [!NOTE]
> Ekki er hægt að hafa tvær línur sem eru með sömu stillingar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  

---

## <a name="best-price-calculation"></a>Útreikningur besta verðs

Þegar búið er að skrá sérverð og línuafslátt fyrir sölu og innkaup [!INCLUDE[prod_short](includes/prod_short.md)]  skal reikna út besta verðið á sölu- og innkaupaskjölum og í verk- og birgðabókarlínum.

Besta verðið er lægsta verðið með hæsta leyfilega línuafsláttinn á tilteknum degi. [!INCLUDE[prod_short](includes/prod_short.md)] reiknar út bestu verðin þegar það bætir einingarverðum og línuafsláttarprósentum við skjala- og færslubókarlínur.

> [!NOTE]  
> Eftirfarandi lýsir því hvernig besta verð er reiknað fyrir sölu. Fyrir innkaup er útreikningurinn svipaður en byggir á tiltækum færibreytum. Til dæmis eru vöruafsláttarflokkar ekki studdir fyrir innkaup.

1. [!INCLUDE[prod_short](includes/prod_short.md)]kannar samsetningu reikningsfærslu á viðskiptamann og vöru og velur svo rétt viðeigandi verð og afslátt samkvæmt eftirfarandi skilyrðum:

    * Er þessi viðskiptamaður með sérstakan samning um verð eða línuafslætti, eða tilheyrir viðskiptamaðurinn hóp með slíkan samning?
    * Fellur varan eða vöruafsláttarflokkurinn á línunni undir þessa samninga?
    * Er dagsetningin innan upphafs- og lokadagsetningar verð-/afsláttarsamningsins? Fyrir reikninga og kreditreikninga er þetta dagsetningin í reitnum **Bókunardags** . í fylgiskjalshausnum. Fyrir öll önnur skjöl er það dagsetningin í reitnum **Pöntunardags** . á hausum þeirra.
    * Er mælieiningarkóti tilgreindur? Ef svo er leitar [!INCLUDE[prod_short](includes/prod_short.md)] að verði/línuafslætti með sama mælieiningarkóða og verði/afslætti án mælieiningarkóða.

2. [!INCLUDE[prod_short](includes/prod_short.md)] athugar hvort einhverjir verð-/afsláttarsamningar eigi við um upplýsingar í skjala- eða færslubókarlínunni. Síðan setur það inn viðeigandi einingarverð og línuafsláttarprósentu með því að nota eftirfarandi skilyrði:

    * Er krafa um lágmarksmagn til staðar í samningi um verð/afslátt sem er uppfyllt?
    * Er krafa um gjaldmiðil til staðar í samningi um verð/afslátt sem er uppfyllt? Ef svo er, er lægsta verðið og hæsti línuafsláttur fyrir þann gjaldmiðil bætt við, jafnvel þótt staðbundinn gjaldmiðill myndi veita betra verð. Ef enginn verð-/afsláttarsamningur er til fyrir tilgreindan gjaldmiðilskóða setur [!INCLUDE[prod_short](includes/prod_short.md)] inn lægsta verðið og hæsta línuafsláttinn í innlendum gjaldmiðli.

Ef ekkert verð finnst fyrir vörurnar á línunni er síðasta innkaupsverð eða einingaverð sótt af birgðaspjaldinu eða birgðahaldseiningarspjaldinu.

## <a name="sales-invoice-discounts-and-service-charges"></a>Afslættir Sölureiknings og Þjónustugjöld

Þegar reikningsafslættir eru notaðir fer afslátturinn sem er veittur eftir því hve reikningsupphæðin er há. Á síðunni **Reikningsafsláttur viðskm** er einnig hægt að leggja þjónustugjald á reikninga sem eru yfir tiltekinni upphæð.  

Áður en hægt er að veita reikningsafslátt af sölu þarf að tilgreina tilteknar upplýsingar. Taka verður eftirfarandi ákvarðanir:  

* Hvaða viðskiptamönnum eigi að veita þessa tegund afsláttar?  
* Hvaða afsláttarprósentu þú ætlar að nota?  

Ef þú vilt að reikningsafslættir séu reiknaðir sjálfkrafa skal á síðunni **Uppsetning sölugrunns** kveikja á víxlhnappnum **Reikna út reikningsafslátt**.  

Hægt er að tilgreina hvort veita eigi reikningsafslætti þegar reikningur uppfyllir ákveðin skilyrði fyrir hvern viðskiptamann. Til dæmis þegar reikningsupphæðin er nógu há. Reikningsafslættir geta verið í innlendum gjaldmiðli fyrir innlenda viðskiptamenn eða í erlendum gjaldmiðli fyrir erlenda viðskiptamenn.  

Afsláttarprósentur eru tengdar við ákveðnar reikningsupphæðir á síðunni **Reikningsafslættir viðskiptamanns** fyrir hvern viðskiptamann. Hægt er að færa inn hvaða prósentutölu sem er. Hver viðskiptamaður getur haft sína eigin síðu, eða þá að hægt er að tengja nokkra viðskiptamenn saman á síðu.  

Til viðbótar við eða í staðinn fyrir afsláttarprósentu er hægt að tengja ákveðið þjónustugjald við ákveðna reikningsupphæð.  

> [!TIP]  
> Áður en þessar upplýsingar eru færðar inn er gott að útbúa uppkast af því afsláttarformi sem á að nota. Formið gerir auðveldara um vik að átta sig á því hvaða viðskiptamenn er hægt að tengja við sömu reikningsafsláttarsíðu. Eftir því sem setja þarf upp færri síður, þeim mun fljótlegra er að færa inn grunnupplýsingarnar.

Frekari þjálfun í afsláttum í sölu er að finna í [Setja upp afslætti fyrir viðskiptamenn þína](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="calculating-invoice-discounts-on-sales"></a>Reikna reikningsafslátt á sölu

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sölulínuafsláttur stofnaður fyrir viðskiptamann

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum „Núverandi upplifun“.

#### [Núverandi reynsla](#tab/current-experience/)  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið svo aðgerðina **Línuafslættir**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakan sölulínuafslátt fyrir viðskiptamanninn.

> [!NOTE]
> Þegar síðurnar **Söluverð** og **Sölulínuafslættir** frá tilteknum viðskiptamanni eru til staðar eru reitirnir **Sía sölutegundar** og **Sía sölukóða** stilltir fyrir viðskiptamanninn og ekki er hægt að breyta eða fjarlægja þá.
>
> Til að setja upp verð eða línuafslætti fyrir alla viðskiptamenn, verðflokk viðskiptamanns eða herferð verður að opna síðurnar af birgðaspjaldi. Einnig er hægt að nota síðuna **Vinnublað söluverðs** fyrir söluverð. Frekari upplýsingar er að finna í [Til að magnuppfæra vöruverð](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Ný reynsla](#tab/new-experience/)  

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

Þegar búið er að ákveða hvaða viðskiptamenn geta fengið reikningsafslátt skal færa inn kóða reikningsafsláttar á viðskiptamannasíðunum. Settu síðan upp skilmálana fyrir hvern kóða.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna skal síðu viðskiptamanns sem getur fengið reikningsafslátt.
3. Í reitinn **Reikningsafsláttarkóði** er færður inn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir viðskiptamanninn.

> [!NOTE]  
> Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála.

Haltu áfram með uppsetningu nýrra afsláttarskilmála sölureiknings.

1. Á síðunni **Viðskiptamenn** skal velja aðgerðina **Reikningsafslættir**. Síðan **Reikningsafsláttur viðskm.** opnast.
2. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem skilyrði reikningsafsláttar í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilyrði í ISK.
3. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
4. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
5. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem viðskiptamaðurinn mun fá mismunandi reikningsafslátt í.

## <a name="see-also"></a>Sjá einnig .

[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Uppsetning verðflokka viðskiptamanna](sales-how-to-set-up-customer-price-groups.md)  
[Uppsetning afsláttarflokka viðskiptamanna](sales-how-to-set-up-customer-discount-groups.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
