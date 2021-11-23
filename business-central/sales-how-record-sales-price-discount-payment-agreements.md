---
title: Setja upp söluverð og afslætti fyrir viðskiptamenn | Microsoft Docs
description: Lýsir því hvernig setja á upp og nota verð- og afsláttarsamninga fyrir söluskjöl.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8b7943caba8482e39217307be904f368f0ec31c0
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752431"
---
# <a name="record-sales-prices-and-discounts"></a>Skrá söluverð og afslætti
> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út einfaldaðri ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður sem ert að nota þessa útgáfu þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] styður ýmsar aðferðir verlagningar, allt frá „eitt verð fyrir allt“ líkönum, þar sem varan er alltaf seld á sama verði, til sérstakra verðsamninga við tiltekna viðskiptamenn, viðskiptamannahópa eða sértilboð þegar söluherferð er í gangi. Þú gætir til dæmis boðið sérstakt verð á sölupöntun við eftirfarandi skilyrði:

* Þegar hún er fyrir lágmarksmagn
* Hún er fyrir ákveðna tegund af vöru  
* Ef hún er stofnuð á ákveðnum tímabili

Til að nota einfalt verðlagningarlíkan þarf aðeins tilgreina einingarverð fyrir vöru eða tilfang. Það verð verður alltaf notað í söluskjölum. Fyrir flóknari líkön, til dæmis þegar söluherferð er keyrð og ætlunin er að bjóða upp á sérstök verð, er hægt að tilgreina skilyrði fyrir hana á síðunni **Söluverð**. Hægt er að bjóða sérstök verð sem byggja á samsetningum af eftirfarandi: 

* Viðskiptamaður
* Vara
* Mælieining
* Lágmarksmagn
* Dagsetningabil sem skilgreina hvenær verðin eru gild

Að auki, eftir að þú hefur sett upp sérverð, getur [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa reiknað út besta verðið í sölu- og innkaupaskjölum og í færslubókarlínum vinnu og vöru. Frekari upplýsingar er að finna í [Útreikningur besta verðs](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

Fyrir söluafslætti er hægt að setja upp og nota eftirfarandi gerðir:

| Afsláttargerð | Description |
| --- | --- |
| **Sölulínuafsláttur** |Upphæð sem er notuð í sölulínum ef til er ákveðin samsetning af viðskiptamanni, vöru, lágmarksmagni, mælieiningu eða upphafs- eða lokadagsetningum. Þessar samsetningar virka á sama hátt og fyrir söluverð. |
| **Reikningsafsláttur** |Afsláttarprósenta sem er dregin frá samtölu söluskjals ef summa allra lína í skjalinu fer yfir ákveðið lágmark. |

> [!TIP]  
> Ef aldrei á að selja vöru með afslætti skal skilja afsláttarreitinn á vörusíðunni eftir auðan og ekki hafa með vöruna í neinum uppsetningum línuafslátta.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Að setja upp söluverð fyrir viðskiptamann

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum Núgildandi upplifun. 

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Velja skal viðskiptamanninn og síðan velja aðgerðina **Verð**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakt söluverð fyrir viðskiptamanninn.

---

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  
Sjálfgefið er að staða nýrra verðlista sé Drög. Drög að verðlistum eru ekki með í verðútreikningum. Þegar búið er að bæta við línum og byrja á að nota verðin skal breyta stöðunni í virka stöðu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**. 
3. Veljið **Nýtt** til að stofna nýja söluverðslista.
4. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt** og **Skattur**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Hægt er að bæta vörum við listann á eftirfarandi hátt:
   * Til að bæta við mörgum vörum skal velja **Leggja til línur** og síðan færa inn síuskilyrði til að tilgreina gerðir af vörum sem bæta á við. Það má færa inn aðrar stillingar fyrir vörurnar. Þessar stillingar eiga aðeins við um verðlistann. Þú getur breytt þeim síðar ef þörf er á.
   * Til að afrita vörur úr öðrum verðlista skal velja **Afrita línur** og síðan velja verðlistann sem á að afrita.
   * Til að bæta vörum við handvirkt skal í reitnum **Gerð afurðar** í línu velja gerð afurðar sem verðlistinn er fyrir. Fyllið inn í eftirstandandi reiti eftir þörfum, eftir vali. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Til að byrja að nota verðlistann skal í reitnum **Staða** velja **Virkur**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verðlistar sölu og innkaupa notaðir
> [!NOTE]
> Til að nota verðlista þarf stjórnandinn að hafa kveikt á eiginleikauppfærslunni **Ný söluverðsupplifun** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

**Á við um gerð** og **Á við um nr.** reitirnir gera kleift að velja hvað verðlisti gildir fyrir, t.d. viðskiptamann eða verðflokk viðskiptamanns. Notaðu reitinn **Skoða dálka fyrir** til að sýna dálka sem gilda aðeins um verð, afslætti eða verð og afslætti.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Fyrirliggjandi verðum breytt þegar kveikt er á eiginleikauppfærslu verðlagningar
Þegar eiginleikauppfærslan **Ný söluverðsupplifun** er virkjuð á síðunni **Eiginleikastjórnun** opnast leiðsögnin **Gagnauppfærsla eiginleika**. Notaðu víxlhnappinn **Nota sjálfgefin verð** á eftirfarandi hátt:

* Ef þú vilt vinna með öll verð á einni síðu skaltu kveikja á honum. Fyrirliggjandi verðum er breytt í einn sjálfgefinn verðlista fyrir hvert af eftirfarandi:

    * Sölur
    * Innkaup
    * Verksala
    * Verkinnkaup 

    Síðan er hægt að breyta öllum verðum fyrir þessi svæði á síðunni **Vinnublað verðs**. Sjálfgefnir verðlistar eru stilltir á síðunum **Uppsetning sölugrunns**, **Uppsetning innkaupagrunns** og **Uppsetning verka**. 

    > [!NOTE]
    > Ef verð eru aðeins stillt á vöru- eða tilfangaspjöldum verða sjálfgefnir verðlistar ekki fylltir út með þessum verðum við gagnauppfærslu. Hins vegar er hægt að opna sjálfgefna verðlista eða verðsíðu vinnublaðs og nota aðgerðina **Tillögur um línur** til að bæta við verðunum sem stillt eru á vöru- eða tilfangaspjöldum. 

* Til að nota söluverðlista skal slökkva á honum. Núgildandi verðum verður breytt í nýjan verðlista fyrir hverja samsetningu af viðskiptamanni, viðskiptamannahópi eða söluherferð og upphafs- og lokadagsetningum og gjaldmiðlum. Ef þú ert með margar samsetningar færðu marga verðlista.

Ef þú hefur þegar virkjað nýju verðupplifunina getur þú búið til sjálfgefna verðlista handvirkt eða tilgreint núverandi verðlista sem sjálfgefinn. Til að stilla núverandi verðlista sem sjálfgefinn skaltu kveikja á víxlhnappnum **Leyfa uppfærslu sjálfgilda** í verðlistanum. Á síðunum **Uppsetning sölugrunns**, **Uppsetning innkaupagrunns** eða **Uppsetning verka** skal síðan stilla verðlistann sem sjálfgefinn.

### <a name="editing-active-price-lists"></a>Virkum verðlistum breytt
Til að gera fólki kleift að breyta verði á virkum verðlistum fyrir vörur, tilföng, viðskiptamenn, lánardrottna eða aðrar einingar sem nota verðlagningu skal kveikja á víxlhnappnum **Leyfa breytingar á virku verði** á síðunum **Uppsetning sölugrunns** og **Uppsetning innkaupagrunns**. 

Þegar slökkt er á víxlhnappnum **Leyfa breytingar á virku verði**, til að uppfæra verð í verðlista þarf að breyta stöðu verðlistans í **Drög**, gera breytinguna og síðan endurvirkja verðlistann.

Síðan **Verðyfirlit** gefur yfirlit yfir öll verð í verðlistum. Hægt er að setja afmarkanir til að þrengja listann. Þegar verðum hefur verið breytt þarf að nota aðgerðina **Staðfesta línur** til að staðfesta verðin gagnvart öðrum verðlistalínum. Að staðfesta verð hjálpa til dæmis við að koma í veg fyrir tvítekningu eða árekstra á verðum. 

> [!NOTE]
> Þegar línu er breytt í virkum verðlista verður staða línunnar að drögum og línan verður ekki höfð með í verðútreikningum fyrr en þú notar aðgerðina **Staðfesta línur**. Þegar verð hefur verið staðfest verður staða línunnar virk og hún verður notuð í verðútreikningum.

Til að bæta við nýjum verðum á síðunni **Verðyfirlit** skal nota aðgerðina **Bæta við nýjum línum**. Síðan **Vinnublað verðs** opnast þar sem verðlínum er bætt við á eftirfarandi hátt:

* Með því að leggja þær til út frá skilyrði
* Afrita þær úr öðrum verðlistum
* Færa þær inn handvirkt. 

Eftir á er hægt að nota aðgerðina **Innleiða verðbreytingu** til að bera nýju verðin saman við aðra verðlista til að forðast tvítekningar.

## <a name="to-copy-sales-prices"></a>Til að afrita söluverð
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum Núgildandi upplifun.

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)  

Ef afrita á söluverð, svo sem söluverð tiltekins viðskiptamanns, og nota í verðflokki viðskiptamanna þarf að keyra **Leggja til söluverð á vinnublaði.** runuvinnslan á síðunni **Vinnublað söluverðs**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað söluverðs** og velja síðan viðkomandi tengil.  
2. Velja skal **Leggja til söluverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Söluverð** skal færa þá **tegund sölu** og **kóta sölu** sem gilda í söluverðinu sem á að afrita inn í reitina.  
4. Efst á beiðnisíðunni er fyllt út í reitunum **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.  
5. Ef stofna á nýtt verð í keyrslunni er gátreiturinn **Stofna nýtt verð** valinn.  
6. Veldu hnappinn **Í lagi** til að setja nýtt verð í línurnar á síðunni **Vinnublað söluverðs** með nýju verðtillögunum og gefður til kynna að það gildi fyrir þá tegund sölu sem var valin.  

   > [!NOTE]  
   > Keyrslan gerir aðeins tillögur, hún framkvæmir ekki breytingarnar. Ef tillögurnar eru viðunandi og eiga að taka gildi, þ.e. setja þær á síðuna **Söluverð** skal velja aðgerðina **Innleiða verðbreytingar** á síðunni **Vinnublað söluverðs**.

---

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Söluverðlistar** og veldu síðan tengda tengilinn. 
2. Velja skal verðlistann sem á að afrita og velja síðan **Afrita línur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Ekki er hægt að hafa tvær línur sem eru með sömu stillingarnar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  
  
---

## <a name="to-bulk-update-item-prices"></a>Til að magnuppfæra vöruverð
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum Núgildandi upplifun.

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)

Ef á að uppfæra mörg vöruverð í einu, t.d. hækka öll vöruverð um sömu prósentuna, er hægt að fylla út **Vinnublað söluverðs** með því að nota eftirfarandi runuvinnslur:

* **Leggja til vöruverð á vinnublaði** leggur til breytingar með því að nota leiðréttingarstuðul á fyrirliggjandi söluverð eða með því að afrita núverandi samninga um söluverð á aðra viðskiptamenn, viðskiptamannahópa eða söluherferðir.
* **Leggja til vöruverð á vinnublaði** leggur til breytingar með því að nota leiðréttingarstuðul á fyrirliggjandi einingarverð í vöruspjöldum eða með því að leggja til verð fyrir nýjar samsetningar af gjaldmiðli, mælieiningu og svo framvegis. Einingarverðum á vörum er ekki breytt.    

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað söluverðs** og velja síðan viðkomandi tengil.  
2. Veldu **Leggja til vöruverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Vara** er reiturinn **Nr.** fylltur út eða **Birgðabókunarflokkur** eða aðrir reitir með upprunalegu vöruverði sem á að uppfæra.  
4. Efst á beiðnisíðunni er fyllt út í **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.
5. Ef þú vilt að keyrslan leiðrétti sjálfkrafa tillögur að vöruverðum skal slá inn leiðréttingu í reitinn **Leiðréttingarstuðull**. Til dæmis myndir þú slá inn **1,15** í **Leiðréttingarstuðulinn** fyrir **15%** hækkun á vöruverði.  
6. Ef runuvinnslan á að stofna ný verð skal kveikja á víxlhnappnum **Stofna nýtt verð**.  
7. Veldu **Í lagi** til að setja nýju verðtillögurnar í línurnar á síðunni **Vinnublað söluverðs**.
8. Til að innleiða tillögurnar skal nota aðgerðina **Innleiða verðbreytingar**. Runuvinnslan býr til tillögur en innleiðir þær ekki.

---

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)

Til að uppfæra verð fyrir margar vörur þarf að búa til nýjam verðlista og afrita síðan línurnar úr fyrirliggjandi verðlista. Þegar línur eru afritaðar er hægt að nota síur til að tilgreina hvað eigi að afrita og hægt er að tilgreina heiltölu eða tugabrot í reitnum **Leiðréttingarstuðull** til að hækka eða lækka verð. Verðlistinn verður að vera í stöðunni **Drög**. Ef þörf krefur er hægt að gera eldri verðlistann óvirkan.

> [!NOTE]
> Ekki er hægt að hafa tvær línur sem eru með sömu stillingarnar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  

## <a name="sales-invoice-discounts-and-service-charges"></a>Afslættir Sölureiknings og Þjónustugjöld
Þegar reikningsafslættir eru notaðir fer afslátturinn sem er veittur eftir því hve reikningsupphæðin er há. Á síðunni **Reikningsafsláttur viðskm** er einnig hægt að leggja þjónustugjald á reikninga sem eru yfir tiltekinni upphæð.  

Ef þú vilt að reikningsafslættir séu reiknaðir sjálfkrafa skal á síðunni **Uppsetning sölugrunns** kveikja á víxlhnappnum **Reikna út reikningsafslátt**.  

Fyrir hvern viðskiptamann er hægt að tilgreina hvort bjóða eigi upp á reikningsafslætti ef skilyrðin eru uppfyllt. Til dæmis ef reikningsupphæðin er nógu há. Skilmála um reikningsafslátt innlendra viðskiptamanna má tilgreina í staðbundinn gjaldmiðill og í erlendum gjaldmiðli hjá erlendum viðskiptamönnum.  

Afsláttarprósentur eru tengdar við ákveðnar reikningsupphæðir á síðunni **Reikningsafsláttur viðskiptamanns** fyrir hvern viðskiptavin. Hægt er að færa inn hvaða prósentutölu sem er. Hver viðskiptamaður getur haft sína eigin síðu, eða þá að hægt er að tengja nokkra viðskiptamenn saman á síðu.  

Til viðbótar við eða í staðinn fyrir afsláttarprósentu er hægt að tengja ákveðið þjónustugjald við ákveðna reikningsupphæð.  

Frekari þjálfun fyrir afslætti á sölum er að finna í [Setja upp afslætti fyrir viðskiptamenn þína](/learn/modules/customer-discounts-dynamics-365-business-central/index) í Microsoft Learn.  

---

### <a name="calculating-invoice-discounts-on-sales"></a>Reikna reikningsafsl. á sölu

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sölulínuafsláttur stofnaður fyrir viðskiptamann
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. Ef ekki er kveikt á eiginleikauppfærslunni skal fylgja þessum skrefum á flipanum Núgildandi upplifun.

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið svo aðgerðina **Línuafslættir**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakan sölulínuafslátt fyrir viðskiptamanninn.

> [!Note]
> Þegar síðurnar **Söluverð** og **Sölulínuafslættir** frá tilteknum viðskiptamanni eru til staðar eru reitirnir **Sölugerðarafmörkun** og **Sölukóðaafmörkun** stillt fyrir viðskiptamanninn og ekki er hægt að breyta eða fjarlægja þær.
>
> Til að setja upp verð eða línuafslætti fyrir alla viðskiptamenn, verðflokk viðskiptamanns eða herferð verður að opna síðurnar af birgðaspjaldi. Einnig er hægt að nota síðuna **Vinnublað söluverðs** fyrir söluverð. Frekari upplýsingar eru í [Til að magnuppfæra vöruverð](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

---

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**.
3. Opnið verðlistann þar sem tilgreina á línuafsláttinn.
4. Stofnið nýja línu eða veljið fyrirliggjandi línu og fyllið svo út í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Í reitnum **Skilgreinir** skal velja annaðhvort **Verð og afsláttur** eða aðeins **Afsláttur**. 
6. Í reitnum **Línuafsláttur %** skal tilgreina afsláttarprósentuna.

    > [!TIP]
    > Hægt er að sía línurnar með því að velja viðeigandi valkost í reitnum **Skoða dálka fyrir**.
    > [!NOTE]  
    > Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Að nota nöfn viðskiptamanna sem kóða gerir þér kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála. Til að setja upp sérstaka skilmála reikningsafsláttar fyrir viðskiptamann skal stilla reitinn **Kóði reikningsafsláttar** á viðskiptamannakóða viðskiptamanns og síðan halda áfram yfir í næsta skref.
---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Að setja upp reikningsafslátt fyrir viðskiptamann
Eftir að ákveðið hefur verið hvaða viðskiptamenn geti fengið reikningsafslátt eru færðir inn reikningsafsláttarkóðar á viðskiptamannaspjöldin og sett upp skilyrði fyrir hvern kóða.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opna skal síðu viðskiptamanns sem getur fengið reikningsafslátt.
3. Í reitinn **Reikningsafsláttarkóði** er færður inn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir viðskiptamanninn. 

> [!NOTE]  
> Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Að nota nöfn viðskiptamanna sem kóða gerir þér kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála.

Settu nú upp skilmála sölureikningsafslátta.

1. Á síðunni **Viðskiptamenn** skal velja aðgerðina **Reikningsafslættir**. Síðan **Reikningsafsláttur viðskm.** opnast.
2. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilyrði í ISK.
3. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
4. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
5. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem viðskiptamaðurinn mun fá mismunandi reikningsafslátt í.

---

## <a name="best-price-calculation"></a>Útreikningur besta verðs
Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[d365fin](includes/d365fin_md.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur.

Besta verð er lægsta leyfilega verð með hæsta leyfilega línuafslættinum þennan tiltekna dag. [!INCLUDE[d365fin](includes/d365fin_md.md)] reiknar þetta sjálfkrafa þegar það setur einingarverð og línuafsláttarprósentuna fyrir vörur í nýja skjalinu og í færslubókarlínum.

> [!NOTE]  
> Eftirfarandi lýsir því hvernig besta verð er reiknað fyrir sölu. Útreikningurinn er sá sami fyrir innkaup.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)]kannar samsetningu reikningsfærslu á viðskiptamann og vöru og velur svo rétt viðeigandi verð og afslátt samkvæmt eftirfarandi skilyrðum:

    - Er þessi viðskiptamaður með sérstakan samning um verð eða línuafslætti, eða tilheyrir viðskiptamaðurinn hóp með slíkan samning?
    - Fellur varan eða vöruafsláttarflokkurinn á línunni undir þessa samninga?
    - Er pöntunardagsetningin (eða bókunardagsetning reikningsins og kreditreikningsins) á milli upphafs- og lokadagsetningar verðs/línuafsláttar?
    - Er mælieiningarkóti tilgreindur? Ef svo er leitar [!INCLUDE[d365fin](includes/d365fin_md.md)] að verði/línuafslætti með sama mælieiningarkóða og verði/afslætti án mælieiningarkóða.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kannar hvort einhverjir samningar um verð/afslátt í eiga við um skjalið eða færslubókarlínuna og bætir svo við viðeigandi einingaverði og prósentu línuafsláttar samkvæmt eftirfarandi skilyrðum:

    - Er krafa um lágmarksmagn til staðar í samningi um verð/afslátt sem er uppfyllt?
    - Er krafa um gjaldmiðil til staðar í samningi um verð/afslátt sem er uppfyllt? Ef svo er, er lægsta verðið og hæsti línuafsláttur fyrir þann gjaldmiðil bætt við, jafnvel þótt staðbundinn gjaldmiðill myndi veita betra verð. Ef ekkert verð/línuafsláttur er til í tilgreindum gjaldmiðilskóða, setur [!INCLUDE[d365fin](includes/d365fin_md.md)] inn lægsta verðið og hæsta línuafsláttinn í staðbundnum gjaldmiðli.

Ef ekkert verð finnst fyrir vörurnar á línunni er síðasta innkaupsverð eða einingaverð sótt af birgðaspjaldinu eða birgðahaldseiningarspjaldinu.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]