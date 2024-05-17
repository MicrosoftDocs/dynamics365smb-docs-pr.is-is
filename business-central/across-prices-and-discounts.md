---
title: Setja upp verð og afslætti
description: Lýsir því hvernig á að skilgreina staðlað verð og sérverð og afsláttarsamninga fyrir sölu og innkaup.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: article
ms.search.keywords: 'price, pricing, discount, discounting, rebate, sale, purchase, invoice'
ms.search.form: '459, 460, 7001, 7011, 7015, 7016, 7017, 7018'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Setja upp verð og afslætti

> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út einfaldaðri ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður sem ert að nota þessa útgáfu þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** á síðunni **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Stjórnunarstefnur fyrir verð og afslætti fyrir innkaup og sölu á vörum og þjónustu eru mikilvæg verkfæri fyrir farsæl viðskipti. Þegar búið er að setja upp vörur og þjónustu sem fyrirtækið kaupir og selur er hægt að skilgreina hvað greitt eða rukkað er fyrir það og þessum upphæðum verður sjálfkrafa bætt við sölu- og innkaupaskjöl. 

## Uppsetning verðs og afsláttar

Áður en verðlistar eru stofnaðir verður að skilgreina stefnur verðlagningar og afslátta í síðunum **Uppsetning sölugrunns** og **Uppsetning innkaupagrunns**.

Hægt að setja upp og nota tvær tegundir afsláttar:

| Afsláttargerð | Description |
| --- | --- |
| **Línuafsláttur** |Afsláttarupphæð sem er gefin upp fyrir línur á sölu- og innkaupaskjölum. Yfirleitt eru línuafslættir byggðir á samsetningu viðskiptamanns, vöru, lágmarksmagni, mælieiningu eða tímabili sem skilgreint er fyrir sölu og innkaup á síðunum **Uppsetning sölugrunns** og **Uppsetning innkaupagrunns**.|
| **Reikningsafsláttur** |Afsláttarprósenta sem er dregin frá samtölu sölu- og innkaupaskjals ef summa allra lína í skjalinu fer yfir ákveðið lágmark. |

Af því að söluverð og afsláttur á sölulínur byggist á samsetningu vöru og viðskiptamanns þá má einnig framkvæma þessa grunnstillingu í birgðasíðu vörunnar þar sem reglurnar og gildin eiga við.

> [!TIP]  
> Ef aldrei á að selja vöru með afslætti skal skilja afsláttarreitinn á vörusíðunni eftir auðan og ekki hafa með vöruna í neinum uppsetningum línuafslátta.

## Um verðlista

Verðlistar eru sveigjanlegir og gera þér kleift að tilgreina viðskiptafélagann eða verkþáttinn sem hann á við um. Til dæmis er hægt að setja upp einn verðlista sem á við um alla lánardrottna og viðskiptamenn eða bjóða upp á sérverð eða afslætti fyrir hvern viðskiptafélaga sem byggir t.a.m. á lágmarksmagni í innkaupa- eða sölupöntunum eða ákveðinni samsetningu viðskiptamanns, vöru, lágmarksmagns, mælieiningu eða tímabila. Verð og afslættir sem eru skilgreind eru notuð sjálfkrafa í innkaupa- og söluskjölum. 

## Setja upp verð

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. 

#### [Núverandi reynsla](#tab/current-experience)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Velja skal viðskiptamanninn og síðan velja aðgerðina **Verð**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakt söluverð fyrir viðskiptamanninn.

#### [Ný reynsla](#tab/new-experience)  

Hægt er að bæta vörum og þjónustu handvirkt við hverja línu eða þú getur notað aðgerðina **Leggja til línur** til að búa til ný verð fyrir valdar vörur, vöruafsláttarflokka, tilföng og aðrar gerðir afurða. Ef þú velur **Leggja til línur** geturðu á síðunni **Verðlínur - Búa til nýjar** notað síur til að velja vörurnar eða þjónustuna sem á að hafa með í verðlistanum. Einnig er hægt að tilgreina hvort eigi að hafa með lágmarksmagn þegar verð eru reiknuð, leiðréttingarstuðulinn sem nota á fyrir nýjar verðlistalínur og sléttunaraðferðina til að nota fyrir verð. 

Sjálfgefið er að staða nýrra verðlista sé **Drög**. Þegar notandi er reiðubúinn að byrja að nota listann er hægt að breyta stöðunni í **Virkur**.

Til að yfirfara verðlista og verð sem gilda fyrir tiltekna viðskiptamenn eða lánardrottna á síðunum **Viðskiptamaður** eða **Lánardrottinn** skal velja annaðhvort aðgerðina **Söluverðlistar** eða **Innkaupsverðlistar**. Fyrir vörur og tilföng er hægt að skoða verðlistalínur með því að velja **Söluverð** eða **Innkaupaverð** á síðunum **Vara** og **Tilfang**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**. 
3. Veljið **Nýtt** til að stofna nýja söluverðslista.
4. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt** og **Skattur**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Til að bæta vörum við listann skal gera eitt af eftirfarandi:
   * Til að bæta við mörgum vörum skal velja **Leggja til línur** og síðan færa inn síuskilyrði til að tilgreina gerðir af vörum sem bæta á við. Einnig er hægt að færa inn nokkrar aðrar stillingar fyrir vörurnar sem eru tilgreindar sérstaklega í verðlistanum. Þú getur breytt þessu síðar ef þörf er á.
   * Til að afrita vörur úr öðrum verðlista skal velja **Afrita línur** og síðan velja verðlistann sem á að afrita.
   * Til að bæta vörum við handvirkt skal í reitnum **Gerð afurðar** velja gerð afurðar sem verðlistinn er fyrir. Fyllið inn í eftirstandandi reiti eftir þörfum, eftir vali. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Til að byrja að nota verðlistann skal í reitnum **Staða** velja **Virkur**.  

---

## Sölulínuafsláttur stofnaður fyrir viðskiptamann

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. 

#### [Núverandi reynsla](#tab/current-experience/)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið svo aðgerðina **Línuafslættir**.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakan sölulínuafslátt fyrir viðskiptamanninn.

> [!Note]
> Þegar síðurnar **Söluverð** og **Sölulínuafslættir** frá tilteknum viðskiptamanni eru til staðar eru reitirnir **Sölugerðarafmörkun** og **Sölukóðaafmörkun** stillt fyrir viðskiptamanninn og ekki er hægt að breyta eða fjarlægja þær.
>
> Til að setja upp verð eða línuafslætti fyrir alla viðskiptamenn, verðflokk viðskiptamanns eða herferð verður að opna síðurnar af birgðaspjaldi. Einnig er hægt að nota síðuna **Vinnublað söluverðs** fyrir söluverð. Frekari upplýsingar eru í [Til að magnuppfæra vöruverð](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Ný reynsla](#tab/new-experience/)  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Veldu viðskiptamann og veldu svo aðgerðina **Söluverðlistar**.
3. Opnið verðlistann þar sem tilgreina á línuafsláttinn.
4. Kveikið á **Leyfa línuafsl.**.
5. Stofnið nýja línu eða veljið fyrirliggjandi línu og fyllið svo út í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Í reitnum **Skilgreinir** skal velja annaðhvort **Verð og afsláttur** eða aðeins **Afsláttur**. 
7. Í reitnum **Línuafsláttur %** skal tilgreina afsláttarprósentuna.

   > [!TIP]
   > Ef verið er að breyta fyrirliggjandi línu er hægt að sía línurnar með því að velja viðeigandi valkost í reitnum **Skoða dálka fyrir**.

---

## Vinna með reikningsafslátt og þjónustugjöld

Þegar reikningsafslættir eru notaðir fer afslátturinn sem er veittur eftir því hve reikningsupphæðin er há. Á síðunni **Reikningsafsláttur** er einnig hægt að leggja þjónustugjald á reikninga sem eru yfir tiltekinni upphæð.  <!--The Invoice Discounts page is hard to find.-->

Áður en hægt er að veita reikningsafslátt af sölu þarf að færa tilteknar upplýsingar í forritið. Þú verður að ákveða hvaða viðskiptamenn fá þessa gerð afsláttar og afsláttarprósenturnar sem þú munt nota.  

Ef þú reikningsfærir afslætti til að verða reiknaðir sjálfvirkt, geturðu tilgreint þetta á síðunni **Uppsetning Sala & Útistandandi**.  

Við hvern viðskiptamann er hægt að tilgreina hvort veita eigi reikningsafslátt ef skilyrðum er fullnægt (það er, ef reikningurinn nær ákveðinni upphæð). Skilmála um reikningsafslátt innlendra viðskiptamanna má tilgreina í staðbundinn gjaldmiðill og í erlendum gjaldmiðli hjá erlendum viðskiptamönnum.  

Afsláttarprósentur eru tengdar við ákveðnar reikningsupphæðir á síðunni **Reikningsafsláttur**. Hægt er að færa inn eins margar prósetnur og nauðsynlegt er. Hver viðskiptamaður getur haft sína eigin síðu, eða þá að hægt er að tengja nokkra viðskiptamenn saman á síðu.  

Til viðbótar við (eða í staðinn fyrir) afsláttarprósentu er hægt að tengja ákveðið þjónustugjald við ákveðna reikningsupphæð.  

> [!TIP]  
> Áður en þessar upplýsingar eru færðar inn er góð hugmynd að undirbúa afsláttarformið fyrst þannig að það sé auðveldara að sjá hvaða viðskiptamenn á að tengja við sömu reikningsafsláttarsíðuna. Frekari upplýsingar um afslætti á sölum er að finna í [Setja upp afslætti fyrir viðskiptamenn þína](/training/modules/customer-discounts-dynamics-365-business-central/index).

### Að setja upp reikningsafslátt fyrir viðskiptamann

Eftir að ákveðið hefur verið hvaða viðskiptamenn geti fengið reikningsafslátt er færður inn reikningsafsláttarkóði á viðskiptamannaspjöldin og sett upp skilyrði fyrir hvern kóða.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
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

Reikningsafsláttur er nú settur upp og úthlutað á umræddan viðskiptamann. Þegar valinn er kóði viðskiptamannsins í reitnum **Reikningsafsl.kóði** á öðrum viðskiptamannaspjöldum er sama reikningsafslætti úthlutað þeim viðskiptamönnum.

## Til að afrita söluverð

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. 

#### [Núverandi reynsla](#tab/current-experience/)  

Ef afrita á söluverð, svo sem söluverð tiltekins viðskiptamanns, og nota í verðflokki viðskiptamanna þarf að keyra **Leggja til söluverð á vinnublaði.** runuvinnslan á síðunni **Vinnublað söluverðs**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað söluverðs** og velja síðan viðkomandi tengil.  
2. Velja skal **Leggja til söluverð á vinnublaði** Aðgerð  
3. Á flýtiflipanum **Söluverð** skal færa þá **tegund sölu** og **kóta sölu** sem gilda í söluverðinu sem á að afrita inn í reitina.  
4. Efst á beiðnisíðunni er fyllt út í reitunum **Tegund sölu** og **Kóta sölu** með gerðinni og heitinu sem afrita á söluverðið í.  
5. Ef stofna á nýtt verð í keyrslunni er gátreiturinn **Stofna nýtt verð** valinn.  
6. Veldu hnappinn **Í lagi** til að setja nýtt verð í línurnar á síðunni **Vinnublað söluverðs** með nýju verðtillögunum og gefður til kynna að það gildi fyrir þá tegund sölu sem var valin.  

   > [!NOTE]  
   > Keyrslan gerir aðeins tillögur, hún framkvæmir ekki breytingarnar. Ef tillögurnar eru viðunandi og eiga að taka gildi, þ.e. setja þær á síðuna **Söluverð** skal velja aðgerðina **Innleiða verðbreytingar** á síðunni **Vinnublað söluverðs**.

#### [Ný reynsla](#tab/new-experience/)  

Staða verðlistans verður að vera **Drög**. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Söluverðlistar** og veldu síðan tengda tengilinn. 
2. Velja skal verðlistann sem á að afrita og velja síðan **Afrita línur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Ekki er hægt að hafa tvær línur sem eru með sömu stillingarnar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  
  
---

## Til að magnuppfæra vöruverð

Þessi skref eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**. 

#### [Núverandi reynsla](#tab/current-experience/)

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

#### [Ný reynsla](#tab/new-experience/)

Til að uppfæra verð fyrir margar vörur þarf að búa til nýjam verðlista og afrita síðan línurnar úr fyrirliggjandi verðlista. Þegar línur eru afritaðar er hægt að nota síur til að tilgreina hvað eigi að afrita og hægt er að tilgreina heiltölu eða tugabrot í reitnum **Leiðréttingarstuðull** til að hækka eða lækka verð. Verðlistinn verður að vera í stöðunni **Drög**. Ef þörf krefur er hægt að gera eldri verðlistann óvirkan.

> [!NOTE]
> Ekki er hægt að hafa tvær línur sem eru með sömu stillingarnar en mismunandi verð. Ef það gerist birtast skilaboð þegar verðlisti er virkjaður. Hægt er að velja verðið sem á að nota með því að opna listann og eyða röngu verði.  

---

## Útreikningur á besta verðinu

Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[d365fin](includes/d365fin_md.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur. Frekari upplýsingar er að finna í [Útreikningur besta verðs](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## Sjá einnig .

[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
