---
title: Setja upp sérstakt söluverð og afslætti fyrir viðskiptamenn | Microsoft Docs
description: Lýsir því hvernig skal skilgreina varaverðlagningu og aflsáttarsamkomulag sem þú vilt að sé í söluskjölunum þegar verið er að selja til mismunandi viðskiptamanna.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6d358afec4689a3543245295427d5fae992dd680
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436777"
---
# <a name="record-special-sales-prices-and-discounts"></a>Skrá sérstök söluverð og afslætti
> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út einfaldaðri ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður sem ert að nota þessa útgáfu þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Skilgreina þarf verð- og afsláttarsamninga sem gilda þegar selt er til viðskiptamanna þannig að umsamdar reglur og gildi séu notuð í söluskjölum.

Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[prod_short](includes/prod_short.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur. Frekari upplýsingar er að finna í [Útreikningur besta verðs](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Hvað varðar verð er hægt að hafa sérstakt söluverð sett í sölulínur ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða tupphafs-/ lokadagsetningu er til staðar. Frekari upplýsingar er að finna í hlutunum [Að setja upp söluverð fyrir viðskiptamann](#to-set-up-a-sales-price-for-a-customer) og [Útreikningur besta verðs](#best-price-calculation).  

Hvað varðar afslætti er hægt að setja upp og nota tvær tegundir söluafsláttar:

| Afsláttargerð | Lýsing |
| --- | --- |
| **Sölulínuafsláttur** |Afsláttarupphæð sem er sett inn í sölulínu ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða upphafs-/ lokadagsetningu er til staðar. Þetta virkar á sama hátt og fyrir söluverð. |
| **Reikningsafsláttur** |Afsláttarprósenta sem er dregin frá samtölu söluskjals ef summa allra lína í skjalinu fer yfir ákveðið lágmark. |

Af því að söluverð og afsláttur á sölulínur byggist á samsetningu vöru og viðskiptamanns þá má einnig framkvæma þessa grunnstillingu í birgðasíðu vörunnar þar sem reglurnar og gildin eiga við.

> [!TIP]  
> Ef aldrei á að selja vöru með afslætti skal skilja afsláttarreitinn á vörusíðunni eftir auðan og ekki hafa með vöruna í neinum uppsetningum línuafslátta.

**Á við um gerð** og **Á við um nr.** reitirnir gera kleift að velja hvað þessi verðlisti gildi fyrir, t.d. viðskiptamann eða verðflokk viðskiptamanns. Með því að nota **Skoða dálka fyrir** er hægt að sýna eða fela dálka sem tengjast því að stilla verð, afslætti eða verð og afslætti.

Hægt er að setja upp verðlistalínur handvirkt eða nota til dæmis aðgerðina **Leggja til línur** til að búa til ný verð fyrir valdar vörur, vöruafsláttarflokka, tilföng og aðrar gerðir afurða. Ef valið er Leggja til línur, mun síðan Verðlínur - Búa til nýtt gera kleift að stilla síur til að velja afurðir þar sem á að búa til nýjar verðlistalínur. Einnig er hægt að tilgreina hvort eigi að hafa með lágmarksmagn þegar verð eru reiknuð, leiðréttingarstuðulinn sem nota á fyrir nýjar verðlistalínur og sléttunaraðferðina til að nota fyrir verð. Aðgerðin **Afrita línur** gerir kleift að afrita fyrirliggjandi verðlistalínur á milli verðlista.

Sjálfgefið er að staða nýrra verðlista sé Drög. Þegar búið er að bæta við línum og verðreikningsvélin á að hafa þær með, er hægt að breyta stöðunni í „Virk“.

Til að yfirfara verðlista og verð sem gilda fyrir tiltekna viðskiptamenn eða lánardrottna skal á síðunni **Viðskiptamaður** velja **Söluverðlistar** eða á síðunni **Lánardrottinn** velja **Innkaupsverðlistar**. Hægt er að skoða verðlistalínur í ýmsum verðlistum með því að velja **Söluverð** eða **Innkaupaverð** á síðunum **Vara** og **Tilfang**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Að setja upp söluverð fyrir viðskiptamann

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**.  

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Velja skal viðskiptamanninn og síðan velja aðgerðina **Verð**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakt söluverð fyrir viðskiptamanninn.

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**. 
3. Veljið **Nýtt** til að stofna nýja söluverðslista.
4. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt** og **Skattur**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Til að bæta vörum við listann skal gera eitt af eftirfarandi:
   * Til að bæta við mörgum vörum skal velja **Leggja til línur** og síðan færa inn síuskilyrði til að tilgreina gerðir af vörum sem bæta á við. Einnig er hægt að færa inn nokkrar aðrar stillingar fyrir vörurnar sem eru tilgreindar sérstaklega í verðlistanum. Þú getur breytt þessu síðar ef þörf er á.
   * Til að afrita vörur úr öðrum verðlista skal velja **Afrita línur** og síðan velja verðlistann sem á að afrita.
   * Til að bæta vörum við handvirkt skal í hnitanetinu í reitnum **Gerð afurðar** velja gerð afurðar sem verðlistinn er fyrir. Fyllið inn í eftirstandandi reiti eftir þörfum, eftir vali. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Til að byrja að nota verðlistann skal í reitnum **Staða** velja **Virkur**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Afslættir Sölureiknings og Þjónustugjöld
Þegar reikningsafslættir eru notaðir fer afslátturinn sem er veittur eftir því hve reikningsupphæðin er há. Á síðunni **Reikningsafsláttur viðskm** er einnig hægt að leggja þjónustugjald á reikninga sem eru yfir tiltekinni upphæð.  

Áður en hægt er að veita reikningsafslátt af sölu þarf að tilgreina tilteknar upplýsingar. Ákveða verður eftirfarandi:  

- Hvaða viðskiptamönnum eigi að veita þessa tegund afsláttar  
- Hvaða afsláttarprósentu eigi að nota  

Ef reikningsfæra á afslætti til að verða reiknaðir sjálfvirkt, geturðu tilgreint þetta á síðunni **Uppsetning Sala & Útistandandi**.  

Við hvern viðskiptamann er hægt að tilgreina hvort veita eigi reikningsafslátt ef skilyrðum er fullnægt (það er, ef reikningurinn nær ákveðinni upphæð). Skilmála um reikningsafslátt innlendra viðskiptamanna má tilgreina í staðbundinn gjaldmiðill og í erlendum gjaldmiðli hjá erlendum viðskiptamönnum.  

Afsláttarprósentur eru tengdar við ákveðnar reikningsupphæðir á síðunni **Reikningsafsláttur viðskiptamanns** fyrir hvern viðskiptavin. Hægt er að færa inn hvaða prósentutölu sem er. Hver viðskiptamaður getur haft sína eigin síðu, eða þá að hægt er að tengja nokkra viðskiptamenn saman á síðu.  

Til viðbótar við (eða í staðinn fyrir) afsláttarprósentu er hægt að tengja ákveðið þjónustugjald við ákveðna reikningsupphæð.  

> [!TIP]  
> Áður en hafist er handa við að setja upplýsingarnar inn í forritið er gott að útbúa uppkast af því afsláttarformi sem á að nota. Þannig er auðveldara að átta sig á því hvaða viðskiptamenn er hægt að tengja við sama reikningsafsláttarsíðu. Eftir því sem setja þarf upp færri síður, þeim mun fljótlegra er að færa inn grunnupplýsingarnar.

Frekari þjálfun fyrir afslætti á sölum er að finna í [Setja upp afslætti fyrir viðskiptamenn þína](/learn/modules/customer-discounts-dynamics-365-business-central/index) í Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Reikna reikningsafsl. á sölu

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sölulínuafsláttur stofnaður fyrir viðskiptamann
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. 

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið svo aðgerðina **Línuafslættir**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakan sölulínuafslátt fyrir viðskiptamanninn.

> [!Note]
> Þegar síðurnar **Söluverð** og **Sölulínuafslættir** frá tilteknum viðskiptamanni eru til staðar eru reitirnir **Sölugerðarafmörkun** og **Sölukóðaafmörkun** stillt fyrir viðskiptamanninn og ekki er hægt að breyta eða fjarlægja þær.
>
> Til að setja upp verð eða línuafslætti fyrir alla viðskiptamenn, verðflokk viðskiptamanns eða herferð verður að opna síðurnar af birgðaspjaldi. Einnig er hægt að nota síðuna **Vinnublað söluverðs** fyrir söluverð. Frekari upplýsingar eru í [Til að magnuppfæra vöruverð](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**.
3. Opnið verðlistann þar sem tilgreina á línuafsláttinn.
4. Kveikið á **Leyfa línuafsl.**.
5. Stofnið nýja línu eða veljið fyrirliggjandi línu og fyllið svo út í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Í reitnum **Skilgreinir** skal velja annaðhvort **Verð og afsláttur** eða aðeins **Afsláttur**. 
7. Í reitnum **Línuafsláttur %** skal tilgreina afsláttarprósentuna.

    > [!TIP]
    > Ef verið er að breyta fyrirliggjandi línu er hægt að sía línurnar með því að velja viðeigandi valkost í reitnum **Skoða dálka fyrir**.

    > [!NOTE]  
    > Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála. Til að setja upp sérstaka skilmála reikningsafsláttar fyrir viðskiptamann skal stilla reitinn **Kóði reikningsafsláttar** á viðskiptamannakóða viðskiptamanns og síðan halda áfram yfir í næsta skref.

8. Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Reikningsafslættir**. Síðan **Reikningsafsl. viðskm.** opnast.
9. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilmála í staðbundnum gjaldmiðli.
10. Í reitinn **Lágmarksupphæð** er einnig hægt að færa inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
11. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
12. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem viðskiptamaðurinn mun fá mismunandi reikningsafslátt í.

Reikningsafsláttur er nú settur upp og úthlutað á viðskiptamanninn. Þegar valinn er kóði viðskiptamannsins í reitnum **Reikningsafsl.kóði** á öðrum viðskiptamannaspjöldum er sama reikningsafslætti úthlutað þeim viðskiptamönnum.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Að setja upp reikningsafslátt fyrir viðskiptamann
Eftir að ákveðið hefur verið hvaða viðskiptamenn geti fengið reikningsafslátt eru færðir inn reikningsafsláttarkóðar á viðskiptamannaspjöldin og sett upp skilyrði fyrir hvern kóða.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opna skal síðu viðskiptamanns sem getur fengið reikningsafslátt.
3. Í reitinn **Reikningsafsláttarkóði** er færður inn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir viðskiptamanninn. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála.

Næsta skref er að setja upp nýja skilmála fyrir sölureikningsafslætti.

1. Á síðunni **Viðskiptamenn** skal velja aðgerðina **Reikningsafslættir**. Síðan **Reikningsafsláttur viðskm.** opnast.
2. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilmála í staðbundnum gjaldmiðli.
3. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
4. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
5. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem viðskiptamaðurinn mun fá mismunandi reikningsafslátt í.

## <a name="to-copy-sales-prices"></a>Söluverð afritað:
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. 

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

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

Staða verðlistans verður að vera **Drög**. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Söluverðlistar** og veldu síðan tengda tengilinn. 
2. Velja skal verðlistann sem á að afrita og velja síðan **Afrita línur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Ekki er hægt að hafa tvær línur sem eru með sömu stillingarnar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  
  
---

## <a name="to-bulk-update-item-prices"></a>Til að magnuppfæra vöruverð
Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. 

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)

Ef magnuppfæra á vöruverð, t.d. hækka öll vöruverð um einhverja prósentu, er nauðsynlegt að keyra **Leggja til vöruverð á vinnublaði** keyrsla. Þú getur fundið tengil á keyrsluna á síðunni **Vinnublað söluverðs**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað söluverðs** og velja síðan viðkomandi tengil.  
2. Veldu **Leggja til vöruverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Vara** er reiturinn **Nr.** fylltur út eða **Birgðabókunarflokkur** eða aðrir reitir með upprunalegu vöruverði sem á að uppfæra.  
4. Efst á beiðnisíðunni er fyllt út í **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.
5. Ef þú vilt að keyrslan leiðrétti sjálfkrafa tillögur að vöruverðum skal slá inn leiðréttingu í reitinn **Leiðréttingarstuðull**. Til dæmis myndir þú slá inn 1,15 í **Leiðréttingarstuðull** fyrir 15% hækkun á vöruverði.  
6. Ef stofna á nýtt verð í keyrslunni er reiturinn **Stofna nýtt verð** valinn.  
7. Veldu hnappinn **Í lagi** til að setja nýtt verð í línurnar á síðunni **Vinnublað söluverðs** með nýju verðtillögunum og gefður til kynna að það gildi fyrir þá tegund **Hlutar** sem var valinn.  

> [!NOTE]
> Keyrslan gerir aðeins tillögur, hún framkvæmir ekki breytingarnar. Ef tillögurnar eru viðunandi og eiga að taka gildi, þ.e. setja á þær í töfluna **Söluverð** , má nota keyrsluna **Innleiða verðbreytingar** í flipanum **Aðgerðir**, flokknum **Aðgerðir** á síðunni **Vinnublað söluverðs**.

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)

Til að uppfæra verð fyrir margar vörur þarf að búa til nýjam verðlista og afrita síðan línurnar úr fyrirliggjandi verðlista. Þegar línur eru afritaðar er hægt að nota síur til að tilgreina hvað eigi að afrita og hægt er að tilgreina heiltölu eða tugabrot í reitnum **Leiðréttingarstuðull** til að hækka eða lækka verð. Verðlistinn verður að vera í stöðunni **Drög**. Ef þörf krefur er hægt að gera eldri verðlistann óvirkan.

> [!NOTE]
> Ekki er hægt að hafa tvær línur sem eru með sömu stillingarnar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  

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