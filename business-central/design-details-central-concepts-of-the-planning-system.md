---
title: Hönnunarupplýsingar Miðlæg hugtök áætlunarkerfisins
description: Áætlun leggur til aðgerðir sem notandinn á að grípa til samkvæmt eftirspurn/framboði og áætlunarfæribreytum vörunnar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis

Áætlunaraðgerðirnar eru í runuverki sem velur fyrst viðeigandi vörur og tímabil sem áætla á fyrir. Síðan kallar keyrslan á kótaeiningu sem reiknar út birgðaáætlun samkvæmt lágstigskóta hverrar vöru (uppskriftarstöðu) . Kótinn eining stemmir af framboðseftirspurn og leggur til aðgerðir sem notandinn á að grípa til. Ráðlagðar aðgerðir birtast sem línu á áætlunvinnublaðinu eða innkaupatillögunni.  

![Innihald síðu áætlunarvinnublaðs.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Innihald síðu áætlunarvinnublaðs")  

Skipuleggjandi fyrirtækis, t.d. innkaupaaðili eða framleiðslustjóri, er væntanlega notandi áætlunarkerfisins. Áætlanakerfið hjálpar notandanum með því að framkvæma víðtæka en fremur einfalda útreikninga fyrir áætlun. Notandinn getur þá einbeitt sér að því að leysa úr erfiðari vandamálunum, líkt og því sem er frábrugðið því sem eðlilegt er.  

Áætlanakerfið er knúið áfram af viðbúinni og raunverulegri eftirspurn viðskiptavina, svo sem spám og sölupöntunum. Áætlunarútreikningar leggja til aðgerðir sem hægt er að framkvæma varðandi framboð frá lánardrottnum, samsetningu eða framleiðslu eða flutninga frá öðrum vöruhúsum. Dæmi um aðgerð sem lögð er til gæti verið að stofna nýjar framboðspantanir, t.d. innkaupa- eða framleiðslupantanir. Ef framboðspantanir eru þegar til gætu aðgerðirnar sem lagðar eru til verið til að auka eða fyrna pantanir til að mæta breytingum á eftirspurn.  

Annað markmið áætlunarkerfisins er að tryggja það að birgðamagnið hækki ekki að óþörfu. Ef eftirspurnin minnkar leggur áætlunarkerfið til að notandinn fresti, minnki magn eða hættir við fyrirliggjandi framboðspantanir.  

Kóti eining inniheldur áætlunargrunninn og eftirfarandi aðgerðir:

* MRP og MPS
* Reikna áætlun hreyfingar
* Reikna áætlun endurgerðar

Hins vegar felur útreikningur framboðsáætlunar í sér mismunandi undirkerfi.  

Áætlunarkerfið inniheldur ekki sérstakt rökfræði fyrir stigskiptingu afkastagetu eða fína tímasetningu. Þessar gerðir tímasetningarvinnu fara fram sérstaklega. Skortur á beinni samþættingu milli svæðanna tveggja þýðir einnig að veruleg afkastageta eða tímasetningarbreytingar krefjast þess að áætlanagerð sé keyrð aftur.  

## <a name="planning-parameters"></a>Áætlunarfæribreytur

Áætlunarfæribreyturnar sem stilltar eru fyrir vöru eða vöruflokk stjórna því hvaða aðgerðir áætlunarkerfið leggur til í ýmsum aðstæðum. Skilgreina áætlunarfæribreytur fyrir hverja vöru til að stjórna því hvenær, hversu mikið og hvernig á að fylla á.  

Einnig er hægt að skilgreina áætlunarfæribreytur fyrir hverja samsetningu vöru, afbrigðis og birgðageymslu með því að setja upp birgðahaldseiningu (birgðahaldseiningu) fyrir hverja samsetningu og tilgreina síðan einstakar færibreytur. Nánari upplýsingar um [hönnun: Meðhöndlun endurpöntunarstefnu](design-details-handling-reordering-policies.md) og [hönnunarupplýsinga: Áætlunarfæribreytur](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Upphafsdagsetning áætlunar

Áætlunarkerfið auðveldar forðast að hafa opnar pantanir áður og tillögur um aðgerðir sem ekki eru mögulegar. Áætlun fer með allar dagsetningar fyrir upphafsdagsetninguna sem fryst svæði. Eftirfarandi regla gildir um fryst svæði:  

* Allar framboðs- og eftirspurn fyrir upphafsdagsetningu áætlunartímabilsins eru taldar hluti af birgðum eða afhentum. Með öðrum orðum, gert er ráð fyrir að áætlun fortíðarinnar keyri samkvæmt því sem gefin er áætlun. Nánari upplýsingar um vinnslupantanir fyrir [upphafsdagsetningu áætlunarinnar](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## <a name="dynamic-order-tracking-pegging"></a>Breytilegar pöntunarrakningar (vörpum)

Kvik rakning pöntunar og samtímis stofnun aðgerðaboða á áætlunarvinnublaðinu er ekki hluti af birgðaáætlunarkerfinu. Þegar eftirspurn eða framboð er stofnað eða því breytt tengir kvik rakning pöntunar eftirspurnarinnar og magnið til að ná yfir hana í rauntíma.  

Ef sölupöntun er til dæmis færð inn eða þeim breytt leitar kvik rakning pöntunar samstundis að framboði til að standa straum af eftirspurninni. Framboðið gæti verið úr birgðum eða úr væntanlegri framboðspöntun (t.d. innkaupapöntun eða framleiðslupöntun). Þegar hann finnur framboðsuppruna er [!INCLUDE [prod_short](includes/prod_short.md)]  eftirspurnin og framboðið tengt. Tengillinn er opnaður á skoðunarsíðum úr skjalalínunum. Þegar framboð finnst ekki stofnar kvika pöntunarrakningarkerfið aðgerðarboð á áætlunarvinnublaðinu með tillögum um framboðsáætlun.  

Kvik rakning pöntunar hjálpar til við að meta hvort samþykkja eigi tillögur um framboðspöntun. Frá framboðshliðinni sýnir hún eftirspurnina sem bjó til framboðið. Frá eftirspurnarhliðinni auðkennir það framboðið sem á að standa undir eftirspurninni.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Dæmi um kvika pöntunarrakningu.":::

Nánari upplýsingar um [hönnun: Frátekning, Rakning pöntunar og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).  

Í fyrirtækjum með lítið vöruflæði og minna háþróaða vörusamsetningu gæti dugað að nota kvika pöntunarrakningu fyrir framboðsáætlun. Hins vegar ætti skipulagskerfið að vera notað til að tryggja jafnað framboðsáætlun í verðmætasköpun.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Breytilegar pöntunarrakningar vs. áætlanakerfi

Það gæti verið erfitt að greina á milli áætlunarkerfisins og kvikrar rakningar pöntunar. Bæði sýna frálag í áætlanavinnublaði með því að leggja virkninni sem skipuleggjandi ætti að taka. Hins vegar er mismunandi hvernig þessi framleiðsla er framleidd.  

Áætlunarkerfið fjallar um allt framboð og eftirspurnarmynstur vöru. Það tekur tillit til allra stiga stigveldis uppskriftarinnar meðfram tímalínunni. Kvik rakning pöntunar fjallar aðeins um stöðu pöntunarinnar sem virkjaði hana. Þegar eftirspurn og framboð eru mótfærð býr áætlunarkerfið til tengla í notandavirkri keyrslustillingu. Kvik pöntunarrakning býr tengla sjálfkrafa til þegar færð er inn eftirspurn eða framboð. Til dæmis þegar stofnuð er sölu- eða innkaupapöntun.  

Kvik rakning pöntunar tenglar eftirspurn og framboð fyrstur kemur fyrstur fær þegar gögn eru færð inn. Þessi grundvöllur getur leitt til röskunar í forgangsröðun. Til dæmis gæti sölupöntun sem færð er inn fyrst með gjalddaga í næsta mánuði verið tengd við birgðir í birgðum. Næsta sölupöntun sem á að skila á morgun getur valdið því að aðgerðarboð um að stofna nýja innkaupapöntun nái yfir hana. Eftirfarandi mynd sýnir þetta dæmi.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Dæmi um pantanarakningu í framboðsáætlun 1.":::

Áætlunarkerfið fjallar um eftirspurn og framboð fyrir vörur í forgangsröð. Pöntuninni er forgangsraðað samkvæmt skiladagsetningum og pantanategundum. Það er, fyrst þarfnast fyrst þjónaðra grunna. Hann eyðir öllum pöntunarrakningartenglum sem voru búnir til á kvikan hátt og enduruppsetja þá samkvæmt forgangi skiladags. Þegar búið er að keyra áætlanakerfið hefur það leyst úr öllu ójafnvægi á milli eftirspurnar og framboðs, eins og sýnt er hér að neðan fyrir sömu gögn.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Dæmi um pantanarakningu í framboðsáætlun 2.":::  

Eftir að áætlun hefur verið keyrð inniheldur taflan Aðgerðaboðafærsla engin aðgerðaboð. Þessum skilaboðum er skipt út fyrir aðgerðirnar sem lagðar eru til á áætlunarvinnublaðinu. Fræðast meira um [Rakningartengla pantana við áætlun](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## <a name="sequence-and-priority-in-planning"></a>Röð og forgangur í áætlun

Röð útreikninganna í áætluninni skiptir miklu máli þegar verkið er gert á sanngjörnum tíma. Forgangur þarfa og forða gegnir einnig mikilvægu hlutverki við að ná sem bestum árangri.  

Áætlunarkerfið er eftirspurnardrifið. Áætla skal hástigsvörur fyrir lágstigsvörur vegna þess að þær gætu myndað eftirspurn eftir lægra-stigs vörum. Til dæmis má áætla smásölustaðsetningar fyrir dreifingarmiðstöðvar vegna þess að smásölustaðurinn getur innihaldið eftirspurn frá dreifingarmiðstöðinni. Ef útgefin framboðspöntun getur náð til sölupöntunar ætti kerfið ekki að stofna nýja framboðspöntun ef útgefin framboðspöntun nær yfir sölupöntun. Ekki ætti að úthluta framboði með tilteknu lotunúmeri til að standa undir almennri eftirspurn ef önnur eftirspurn krefst þessarar tilteknu lotu.  

### <a name="item-priority--low-level-code"></a>Vöruforgangur / Lægra stigs kóði

Í framleiðslu-umhverfi, eftirspurn fyrir lokið, seljanlega vöru mun leiða í unnum eftirspurn fyrir íhluti sem eru í tilbúna hlutnum. Uppbygging uppskriftar stjórnar íhlutauppbyggingunni og getur náð yfir nokkur stig hálfunninna vara. Áætlanagerð vöru á einu stigi veldur afleiddri eftirspurn eftir íhlutum á næsta stigi. Þetta stigveldi leiðir á endanum til afleiddrar eftirspurnar eftir keyptum vörum. Áætlunarkerfið áætlar vörur eftir flokkun þeirra í heildaruppskriftarstigveldinu. Kerfið byrjar á fullunnum seljanlegum vörum á efsta stigi og heldur áfram niður samsetningu framleiðslunnar í lægra-stigs vörur (samkvæmt lágstigskótanum).  

Eftirfarandi mynd sýnir þá röð sem [!INCLUDE [prod_short](includes/prod_short.md)] leggur til framboðspantanir á efsta stigi. Gert er ráð fyrir því að tillögurnar hafi verið samþykktar og einnig birtast lægri stigs vörur.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Áætlanir um uppskriftir.":::

Skoða má nánari upplýsingar um framleiðslu með því að [fara í Álagsbirgðaforstillingar](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### <a name="optimizing-performance-for-low-level-calculations"></a>Fínstilla afköst fyrir lágstigsútreikninga

Útreikningar á lágstigskóða geta haft áhrif á afköst kerfisins. Hægt er að draga úr áhrifunum **með því að slökkva á útreikningi** á kvikum lágstigskóta á **síðunni Uppsetning** framleiðslu. Þegar það er gert er [!INCLUDE[prod_short](includes/prod_short.md)]  lagt til að stofnuð sé ítrekuð verkraðarfærsla til að uppfæra lágstigskóta daglega. Hægt er að ganga úr skugga um að vinnslan keyri utan vinnutíma með því að tilgreina upphafstíma í reitnum **Fyrsti upphafsdagur/tími**.

Einnig er hægt að flýta útreikningum á lágstigskóta með því að kveikja á **vísbendingu um lágstigskóta** á **síðunni Uppsetning** framleiðslu.

> [!IMPORTANT]
> Ef valið er að fínstilla afköst notar [!INCLUDE[prod_short](includes/prod_short.md)] nýjar útreikningsaðferðir til að ákvarða lágstigskóða. Ef um er að ræða viðbót sem tengist atburðum sem gömlu útreikningarnir nota gæti framlengingin hætt að virka.

### <a name="locations--transfer-level-priority"></a>Birgðageymslur / Forgangur millifærslustigs

Fyrirtæki með fleiri en eina birgðageymslu gætu þurft að skipuleggja hverja birgðageymslu fyrir sig. Til dæmis gæti öryggisbirgðastig vöru og endurpöntunarstefnan verið frábrugðin einni birgðageymslu og annarri. Tilgreina verður áætlunarfæribreytur fyrir hverja vöru og birgðageymslu.  

Hægt er að nota birgðaeiningar til að tilgreina einstakar áætlunarfæribreytur. Hægt er að líta á BHE sem vöru í tiltekinni birgðageymslu. Ef birgðahaldseining hefur ekki verið skilgreind fyrir þá birgðageymslu [!INCLUDE [prod_short](includes/prod_short.md)]  notar kerfið færibreyturnar sem stilltar eru á birgðaspjaldinu. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar áætlun aðeins fyrir virkar birgðageymslur þar sem eftirspurn eða framboð er fyrir tiltekna vöru.  

Hægt er að meðhöndla allar vörur á hvaða stað sem er, en [!INCLUDE [prod_short](includes/prod_short.md)] það hefur strangt aðhald að hugmyndinni um birgðageymslur. Til dæmis er ekki hægt að uppfylla sölupöntun fyrir vöru í einni birgðageymslu með birgðir frá annarri birgðageymslu. Magn birgða þarf fyrst að flytja af þeirri staðsetningu sem tilgerind er á sölupöntun.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Áætlanir um birgðahaldseiningar.":::

Nánari upplýsingar um [hönnun: Millifærslur í áætlun](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Forgangur pöntunar

Innan tiltekinnar birgðahaldseiningar, táknar umbeðin eða tiltæk dagsetning hæsta forgang; eftirspurn í dag ætti að mæta áður en eftirspurn næstu viku er mætt. Fyrir utan þess háttar forgang er mismunandi eftirspurn og framboðstegundum raðað eftir mikilvægi viðskipta til að ákveða hvaða eftirspurn skuli vera ánægð fyrst. Í framboðshliðinni ákvarðar pöntunarforgangurinn uppruna framboðsins sem á að nota fyrst. Nánari upplýsingar um [forgangsröðun pantana](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Eftirspurnarspá og standandi pantanir

Spá og standandi pöntun endurspegla bæði vænta eftirspurn. Standandi pöntunin, sem nær yfir ætluð kaup viðskiptamanns á tilteknum tíma, er ætlað að minnka óvissu í heildarspá. Standandi pöntunin er spá fyrir viðskiptamann efst í ótilgreindri spá, eins og hún er mynduð í eftirfarandi mynd.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Áætlanir með spám.":::

Nánari upplýsingar um [spáreftirspurn eru dregnar úr sölupöntunum](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## <a name="planning-assignment"></a>Úthlutað á áætlun

Enduráætla skal allar vörur þegar mynstur eftirspurnar eða framboðs hefur breyst frá síðasta skipti sem áætlun var reiknuð. Ef t.d. ný sölupöntun er færð inn eða fyrirliggjandi sölupöntun er breytt þarf að endurreikna áætlunina. Aðrar ástæður fyrir enduráætlun fela í sér breytingu á spá eða magni í öryggisbirgðum. Ef uppskrift er breytt með því að bæta við eða fjarlægja íhlut er líklegast einnig breyting en aðeins fyrir íhlutarvöruna.  

Áætlanakerfið fylgist með slíkum tilvikum og úthlutar viðeigandi vörum til að gera áætlun.  

Í mörgum birgðageymslum gerist úthlutunin á vörustigi á hverja samsetningu birgðageymslu. Ef sölupöntun hefur verið stofnuð í aðeins einni birgðageymslu skal [!INCLUDE [prod_short](includes/prod_short.md)]  úthluta vörunni í þeirri birgðageymslu til áætlunar.  

Ástæðan fyrir að velja vörur fyrir áætlun grundvallast á afköstum kerfisins. Ef mynstur eftirspurnar-framboðs vöru hefur ekki breyst mun áætlunarkerfið ekki leggja til aðgerðir sem þarf. Án áætlunarúthlutunarinnar þyrfti kerfið að framkvæma útreikninga fyrir allar vörur til að finna út hvað á að áætla. Nánari upplýsingar um ástæður til að úthluta vörum vegna áætlunar er farið í [Upplýsingar um hönnun: Taflan](design-details-planning-assignment-table.md) Skipting áætlunar.  

Eftirfarandi eru tiltækir áætlunarkostir:  

* **Reikna áætlun endurgerðar** reiknar út allar valdar vörur, hvort sem það er nauðsynlegt eða ekki.  
* **Reikna áætlun hreyfingar** reiknar aðeins út vörurnar sem hafa breyst í eftirspurn og framboðsmynstri og hafa því verið tengdar við áætlun.  

Sumir telja að gera eigi áætlun hreyfingar á flugunni, til dæmis þegar sölupantanir eru færðar inn. Hins vegar gæti áætlanir á flugunni verið ruglingslegt vegna þess að kvik pöntunarrakning og aðgerðaboð eru einnig reiknuð á flugunni. [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á eftirlit með rauntíma til að lofa. Hann birtir sprettiviðvaranir þegar sölupantanir eru færðar inn og núgildandi birgðaáætlun uppfyllir ekki eftirspurnina.  

Áætlunarkerfið áætlar aðeins fyrir vörurnar sem búnar hafa verið til með viðeigandi áætlunarfæribreytum. Annars er gert ráð fyrir því að vörurnar verði áætlaðar handvirkt eða hálf-sjálfvirkt með aðgerðinni Pantanaáætlun. Nánari upplýsingar um sjálfvirkar áætlunaraðferðir eru í [Upplýsingar um hönnun: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Vöruvíddir

Eftirspurn og framboð geta haft afbrigðiskóða og staðsetningarkóða sem verður að virða þegar áætlanakerfið finnur jafnvægi framboðs og eftirspurnar.  

[!INCLUDE [prod_short](includes/prod_short.md)] fer með afbrigðis- og birgðageymslukóta sem vöruvíddir í sölupöntunarlínu, birgðafærslu og svo fram vegar. Í samræmi reiknar það áætlun fyrir hverja samsetningu afbrigðis og birgðageymslu eins og samsetningin væri aðskilið vörunúmer.  

Í stað þess að reikna fræðilegar samsetningar af afbrigði og birgðageymslu [!INCLUDE [prod_short](includes/prod_short.md)]  reiknar aðeins samsetningarnar sem eru til í gagnagrunninum. Nánari upplýsingar um hvernig áætlunarkerfið tekur við birgðageymslukótum eftirspurn er farið í [Upplýsingar um hönnun: Eftirspurn í auðri birgðageymslu](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Vörueigindir

Vörur eru oft með almennar eigindir, t.d. er vörunúmer, afbrigðiskóti, birgðageymslukóti og pöntunartegund. Þó getur hver eftirspurn og framboðsviðburður haft aðrar skilgreiningar, t.d. rað- eða lotunúmer. Áætlanakerfið skipuleggur þessar eigindir á ákveðinn hátt, allt eftir reglustigi.  

Tengill á milli pantana á milli eftirspurnar og framboðs er önnur gerð eigindar sem hefur áhrif á áætlunarkerfið. Fáðu nánari upplýsingar á [tenglum](#order-to-order-links) fyrir pöntun.

### <a name="specific-attributes"></a>Tilgreindir eiginleikar

Sumir eftirspurnareigindir eru sértækir og framboð verða að passa nákvæmlega við þau.

* Rað- eða lotunúmer sem krefjast sérstakrar forrits (Krafist er þessara eiginda ef kveikt er á **raðnr. raðnr., rað**  **- eða** lotunúmerum á síðunni **Vörurakningarkótaspjald** fyrir vörurakningarkótann sem varan notar.)  
* Tenglar í framboðspantanir stofnaðir handvirkt eða sjálfvirkt fyrir tiltekna eftirspurn (tenglar á milli pantana).  

Áætlunarkerfið beitir eftirfarandi reglum í þessum eigindum:  

* Eftirspurn með sérstaka eiginleika er aðeins hægt að uppfylla með framboði sem passa við eiginleika.  
* Framboð með sérstaka eiginleika getur einnig fullnægt eftirspurn sem krefst ekki sérstaklega þessara eiginda.  

Ef birgðir eða áætlaðar birgðir uppfylla ekki eftirspurn eftir sérstökum eigindum leggur áætlunarkerfið til nýja framboðspöntun án áætlunarfæribreyta.  

### <a name="non-specific-attributes"></a>Ótilgreindar eigindir

Rað- eða lotunúmeraðar vörur án tiltekinnar vörurakningaruppsetningar gætu verið með ósértæk rað- eða lotunúmer. Þessar tegundir númera er hægt að jafna við hvaða rað- eða lotunúmer sem er. Áætlunarkerfið hefur meira frelsi til að stemma, til dæmis raðaðri eftirspurn og raðað framboð, yfirleitt í birgðum.  

Eftirspurn-framboð með rað- eða lotunúmerum, tilteknum eða ósértækum, eru í miklum forgangi og eru undanþegin frysta svæðinu. Þeir verða hluti áætlunar jafnvel þótt þeir komi á gjalddaga fyrir upphafsdagsetningu áætlunarinnar. Nánari upplýsingar um [rað- og lotunúmer eru hlaðnar með lýsingarstigi](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Til að fræðast meira um hvernig eigindir áætlunarkerfisins stemma af eru farið á [Rað- og lotunúmer og tenglar fyrir pöntun eru undanþegnir fyrra tímabili](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## <a name="order-to-order-links"></a>Tenglar á milli pantana

Pöntun-eftir pöntun merkir að keypt er, sett saman eða framleitt vara fyrir tiltekna eftirspurn. Nokkrar ástæður eru fyrir vali á þessari stefnu:

* Eftirspurnin er óáreiðanleg.
* Afgreiðslutíminn er ótrúlegur.
* Nauðsynlegar eigindir eru breytilegar.  

Annað tilfelli sem notar tengla fyrir pöntun er þegar samsetningarpöntun er tengd sölupöntun í samsetningartilviki eftir pöntun.  

Tenglar á milli pantana eru jafnaðir milli eftirspurnar og framboðs á fjóra vegu:  

* Þegar áætluð vara notar **endurpöntunarstefnuna Pöntun**   
* Þegar framleiðslustefnan eftir pöntun er notuð til að stofna framleiðslupantanir af mörgum stigum eða framleiðslupantanir af verki (framleiðslu íhluta á sömu framleiðslupöntun)  
* Þegar framleiðslupantanir eru stofnaðar fyrir sölupantanir með aðgerðina áætlun sölupöntunar  
* Þegar vara er sett saman við sölupöntun (**Samsetningarstefna** er stillt á **Samsetning í pöntun**)  

Áætlunarkerfið leggur til að einungis sé pantað magn sem þarf. Innkaupa-, framleiðslu- eða samsetningarpöntunin heldur áfram að passa við eftirspurnina. Ef sölupöntun er til dæmis breytt með tíma eða magni leggur áætlunarkerfið til að framboðspöntuninni sé breytt í samræmi við það.  

Þegar pantanatenglar eru til staðar þá hefur áætlunarkerfið ekki tengt framboð eða birgðir í jöfnunarferlinu. Skipuleggjendur geta ákveðið hvort nota eigi tengda framboðið eða nýja eftirspurn. Í síðara tilfellinu er hægt að eyða framboðspöntuninni eða taka tengda framboðið frá handvirkt.  

Frátekningar og pöntunarrakningartenglar brjóta ef aðstæður verða ómögulegar. Til dæmis þegar eftirspurn er færð yfir á dagsetningu sem er fyrr en í framboðinu. Pantanatenglar laga sig að breytingum á eftirspurn eða framboði og brjóta aldrei.  

## <a name="reservations"></a>Bókanir

Áætlunarkerfið tekur ekki frátekið magn með í útreikningum. Ef magn í sölupöntun er til dæmis að fullu eða frátekið að hluta er ekki hægt að nota magnið til að standa undir annarri eftirspurn.

Áætlunarkerfið inniheldur frátekið magn í áætluðum birgðaforstillingum. Það verður að íhuga allt magn til að ákvarða hvenær endurpöntunarmarkið er liðið og hversu margir á að endurpanta til að ná hámarksbirgðastiginu. Óþarfar frátekningar geta aukið hættuna á að birgðastig keyri lítillega vegna þess að áætlunargrunnurinn finnur ekki frátekið magn.  

Eftirfarandi mynd sýnir hvernig frátekningar geta hindrað áætlun.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Áætlanir með frátekningu.":::

Nánari upplýsingar um [hönnun: Frátekning, Rakning pöntunar og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Viðvaranir

Fyrsti dálkur í áætlanagerðarvinnublaði er fyrir viðvörunarreiti. Viðvörunartákn sýnir þegar áætlunarlína er búin til fyrir óvenjulegar aðstæður.  

Framboð á áætlunarlínum með viðvaranir verður yfirleitt ekki breytt samkvæmt áætlunarfæribreytum. Þess í stað stingur áætlunarkerfið upp á framboði til að standa undir nákvæmu magni eftirspurnarinnar. Hins vegar er hægt að setja kerfið upp til að virða áætlunarfæribreytur fyrir áætlunarlínur með ákveðnar viðvaranir. Viðvörunarupplýsingarnar birtast á síðunni **Óraknar áætlunareiningar** sem einnig sýna rakningartengla pöntunar við neteiningar sem ekki eru pantaðar. Þrjár tegundir viðvarana eru:  

* Neyð  
* Frávik  
* Athugið  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Viðvaranir á áætlunarvinnublaðinu.":::

### <a name="emergency"></a>Neyð

Neyðarviðvörunin sýnir í tveimur aðstæðum:  

* Þegar birgðir eru neikvæðar á upphafsdagsetningu áætlunar  
* Þegar til eru aftur-dagsettir framboðs- eða eftirspurnartilvik  

Ef birgðir vöru eru neikvæðar á upphafsdegi áætlunarinnar stingur kerfið upp á neyðarbirgðum fyrir neikvæða magnið sem á að koma á upphafsdagsetningu áætlunarinnar. Upphafsdagsetningin og magn neyðarpöntunarinnar eru tiltekin í viðvörunartextanum. Nánari upplýsingar um meðhöndlun áætlaðra [birgða](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Fylgiskjalslínur með skiladagsetningar á undan upphafsdagsetningu áætlunarinnar eru sameinaðar í neyðarpöntun. Áætlað er að pöntunin berist á upphafsdagsetningu áætlunarinnar.  

### <a name="exception"></a>Frávik

Viðvörun um frávik birtist ef áætlaðar birgðir eru undir öryggismarki birgða. Áætlunarkerfið stingur upp á framboðspöntun til að uppfylla eftirspurnina á lokadagsetningunni. Viðvörunartextinn segir til um magn í öryggisbirgðum fyrir vöruna og dagsetninguna sem það magn varð of lítið.  

Það er undantekning að brjóta öryggisbirgðastig. Það ætti ekki að gerast ef endurpöntunarmarkið er rétt stillt. Nánari upplýsingar um [hlutverk endurpöntunarmarksins](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Hjálpa til við að tryggja að áætlaðar birgðir til ráðstöfunar séu aldrei lægri en öryggisbirgðastigið. Magnið sem lagt er til nær til öryggisbirgða, án þess að taka tillit til áætlunarfæribreyta. Í einhverjum aðstæðum verða hins vegar pöntunarbreytur teknar með.  

> [!NOTE]  
> Áætlanakerfið kann að hafa gleypt varabirgðirnar vísvitandi og mun svo endurnýja þær samstundis. Fræðast meira um [öryggisbirgðir](design-details-balancing-demand-and-supply.md#consume-safety-stock) neyta.

### <a name="attention"></a>Athugið

Viðvörunin Til athugunar birtist við þrennar aðstæður:  

* Upphafsdagsetning áætlunarinnar er á undan kerfisdagsetningunni.  
* Áætlunarlínan stingur upp á því að útgefinni innkaupa- eða framleiðslupöntun verði breytt.  
* Áætlaðar birgðir eru umfram yfirflæðisstig á gjalddaga. Fáðu frekari upplýsingar um [dvöl undir yfirflæði](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> Í áætlunarlínum með viðvaranir er reiturinn **Samþykkja aðgerðarboð** ekki valinn þar sem áætlað er að skipuleggjandi rannsaki línurnar áður en áætlunin er framkvæmd.  

## <a name="error-logs"></a>Villukladdar

Á beiðnisíðunni **Reikna áætlun** er hægt að velja reitinn **Stöðva og sýna fyrstu villu** til að láta stöðva áætlunarkeyrsluna þegar fyrsta villan finnst. Skilaboð birtast með upplýsingum um villuna. Ef villa er til staðar sýnir áætlunarvinnublaðið aðeins áætlunarlínurnar sem tókst að gera áður en villan gerðist.  

Ef reiturinn er ekki valinn **heldur keyrslan Reikna áætlun** áfram þar til henni er lokið. Villur ráfa ekki keyrsluna. Ef villur eru birtast skilaboð um hversu mörg atriði urðu fyrir áhrifum. Síðan **Villukladdi** áætlunar veitir nánari upplýsingar um villuna og tengla á viðkomandi skjöl eða uppsetningu.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Villuboð á áætlunarvinnublaðinu.":::

## <a name="planning-flexibility"></a>Sveigjanleiki áætlunar

Ekki er alltaf hagkvæmt að áætla fyrirliggjandi framboðspöntun. Þegar framleiðsla er til dæmis hafin eða viðbótarfólk er ráðið á tilteknum degi til að vinna verkefnið. Til að tilgreina hvort áætlunarkerfið geti breytt pöntun hafa **allar framboðspöntunarlínur reit með reitinn Sveigjanleiki** áætlunar með tvo valkosti: **Ótakmarkað** eða **Ekkert**. Ef reiturinn er stilltur á **Ekkert** reynir áætlunarkerfið ekki að breyta framboðspöntunarlínunni.  

Hægt er að velja valkost handvirkt í reitnum, þó í sumum tilfellum verði hann stilltur sjálfvirkt af [!INCLUDE [prod_short](includes/prod_short.md)]. Sú staðreynd að hægt er að stilla sveigjanleika áætlunar handvirkt er mikilvæg vegna þess að auðvelt er að aðlaga notkun eiginleikans að mismunandi verkflæðum og viðskiptamálum. Nánari upplýsingar um notkun reitsins fást [í Upplýsingar um hönnun: Millifærslur í Áætlun](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Áætlun pöntunar

Verkfæri grunnframboðsáætlanagerðar á síðunni **Pantanaáætlun** er hannað fyrir handvirka ákvarðanatöku. Hún telur engar áætlunarfæribreytur og er því ekki rætt frekar í þessari grein. Nánari upplýsingar við [Áætla nýja eftirspurnarpöntun eftir pöntun](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Mælt er með því að pantanaáætlun sé ekki notuð ef fyrirtækið notar þegar áætlunar- eða innkaupatillögublöð. Framboðspantanir sem stofnaðar eru á síðunni **Pantanaáætlun** geta breyst eða verið eytt á meðan sjálfvirk áætlanagerð er keyrð. Þessar breytingar gerast vegna þess að sjálfvirka áætlunarkeyrslan notar áætlunarfæribreytur sem hugsanlega hafa ekki verið teknar með þegar áætlunin er gerð handvirkt á síðunni Pantanaáætlun.  

## <a name="finite-loading"></a>Takmarkað álag

[!INCLUDE[prod_short](includes/prod_short.md)] veitir grófa áætlun til að áætla sanngjarna notkun forða. Hún býr ekki sjálfkrafa til og viðhalda nákvæmum áætlunum eftir forgangsröðun eða reglur um hagræðingu.  

Fyrirhuguð notkun eiginleikans með takmarkaða afkastagetu er sem hér segir:

* Til að forðast yfirálag forða
* Til að tryggja að afkastageta sé ekki skilin eftir óúthlutað ef hún gæti minnkað um tíma framleiðslupöntunar

Við áætlanir [!INCLUDE [prod_short](includes/prod_short.md)]  með forða með takmarkaða afkastagetu er tryggt að forðinn sé ekki hlaðinn yfir afkastagetu (bundin álag). Hún úthlutar hverri aðgerð næstu tímarauf. Ef tímaröðin er ekki nógu stór til að ljúka aðgerðinni skiptir hún aðgerðinni í tvo eða fleiri hluta í næstu tímaraufum.  

> [!NOTE]  
> Ef vinnsluaðgerðum er skipt er uppsetningartíma aðeins úthlutað einu sinni vegna þess að gert er ráð fyrir að einhver handvirk leiðrétting sé gerð til að fínstilla áætlunina.  

Hægt er að bæta hömlutíma við forða til að draga úr aðgerðaskiptingu. Í þetta sinn skulum við [!INCLUDE [prod_short](includes/prod_short.md)] tímasetja álagið á síðasta mögulega degi með því að fara örlítið yfir álagsprósentuna.  

## <a name="see-also"></a>Sjá einnig .

[Hönnunarupplýsingar: Flutningur í áætlun](design-details-transfers-in-planning.md)  
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)  
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)  
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
