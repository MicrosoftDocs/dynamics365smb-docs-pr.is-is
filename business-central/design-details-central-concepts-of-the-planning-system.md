---
title: Hönnunarupplýsingar miðlægt hugtak Áætlanakerfisins
description: Áætlanir benda til aðgerða fyrir notandann til að byggja á aðstæðum eftirspurnar/framboðs og áætlunarfæribreytum varanna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis

Aðgerðir áætlanagerðar eru í runuvinnslu sem velur fyrst viðkomandi vöru og tímabil sem áætlun gildir um. Eftir lágstigskóða (UPPSKRIFTARSTÖÐU) kallar keyrslan á kóða sem reiknar út birgðaáætlun. Kóti birgðaeiningar kóða-eftirspurnar er og bendir á Aðgerðir sem notandinn tekur. Ráðlagðar aðgerðir birtast sem línu á áætlunvinnublaðinu eða innkaupatillögunni.  

![Innihald síðu áætlunarvinnublaðs.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Innihald síðu áætlunarvinnublaðs")  

Skipuleggjandi fyrirtækis, t.d. innkaupaaðili eða framleiðsluskipuleggjandi, er væntanlega notandi áætlanakerfisins. Áætlanakerfið hjálpar notandanum með því að framkvæma víðtæka en fremur einfalda útreikninga fyrir áætlun. Notandinn getur þá einbeitt sér að því að leysa úr erfiðari vandamálunum, líkt og því sem er frábrugðið því sem eðlilegt er.  

Áætlanakerfið er knúið áfram af viðbúinni og raunverulegri eftirspurn viðskiptavina, svo sem spám og sölupöntunum. Áætlunarútreikningar benda til aðgerða sem hægt er að taka varðandi framboð frá lánardrottnum, samsetningu eða framleiðslu eða flutning úr öðrum vöruhúsum. Dæmi um aðgerðina sem var lögð til gæti verið að stofna nýjar framboðspantanir, eins og innkaupa-eða framleiðslupöntunina. Ef framboðspantanir eru þegar til, gætu aðgerðirnar verið til þess að auka eða flýta pöntunum til að mæta breytingum á eftirspurn.  

Annað markmið áætlunarkerfisins er að tryggja það að birgðamagnið hækki ekki að óþörfu. Ef eftirspurn minnkar, stingur áætlunarkerfið upp á því að notandinn Frestar, minnkar magn eða hættir við tiltækar framboðspantanir.  

Í kóðakerfi eru skipulagsheildar og eftirfarandi aðgerðir:

* MRP og MPS
* Reikna áætlun hreyfingar
* Reikna áætlun endurgerðar

Hins vegar felst í útreikningi á framboði á áætlun um mismunandi undirkerfi.  

Áætlanakerfið felur ekki í sér tileinkaða rökfræði fyrir afkastajöfnun eða fínröðun. Þær tegundir röðunar starfa eru gerðar sérstaklega. Skortur á beinni samþættingu á milli þessara tveggja svæða þýðir einnig að veruleg afkastageta eða tímaáætlun breytingar krefjast þess að áætlun sé endurgerð.  

## Áætlunarfæribreytur

Áætlunarfæribreytur sem eru stilltar fyrir vöru eða hóp stjórna því hvaða aðgerðir áætlanakerfið leggur til við ýmsar aðstæður. Skilgreina áætlunarfæribreytur fyrir hverja vöru til að stjórna hvenær, hversu mikið, og hvernig á að fylla út.  

Einnig er hægt að skilgreina áætlunarfæribreytur fyrir hvaða samsetningu vöru, afbrigði og birgðageymslu með því að setja upp birgðahaldseiningu (be) fyrir hverja samsetningu og tilgreina síðan einstakar færibreytur. Frekari upplýsingar á  [hönnunarsíðu: afgreiðsla endurpöntunarstefnu](design-details-handling-reordering-policies.md)  og  [hönnunar nánar: skipulagsupprear](design-details-planning-parameters.md).  

## Upphafsdagsetning áætlunar

Áætlanakerfið hjálpar til við að forðast að hafa opnar pantanir í fortíðinni og tillögum um aðgerðir sem ekki er mögulegt. Áætlun meðhöndlar allar dagsetningar á undan upphafsdagsetningunni sem frost svæði. Eftirfarandi regla gildir um fryst svæði:  

* Öll framboð og eftirspurn áður en Upphafsdagur áætlunartímabilsins telst hluti af birgðum eða afhent. Með öðrum orðum er gert ráð fyrir því að áætlunin um fortíðina keyri í samræmi við gefna áætlun.  [Frekari upplýsingar um vinnupantanir eru á undan upphafsdegi áætlunar](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## Breytilegar pöntunarrakningar (vörpum)

Kvika pöntunarrakning og samtímis stofnun aðgerðaboðins í áætlunarvinnublaðinu eru ekki hluti af áætlunarkerfi framboðins. Þegar eftirspurn eða framboð er stofnað eða því breytt, skal kvika pöntun rekja eftirspurnina og magnið til að ná henni í rauntíma.  

Til dæmis ef sölupöntun er færð inn eða henni breytt, leitar dynamic pöntunarrakning samstundis að framboði til að ná eftirspurninni. Framboðið gæti verið úr birgðum eða úr væntanlegu framboðapöntun (til dæmis innkaupapöntun eða framleiðslupöntun). Þegar það finnur framboðsgjafa  [!INCLUDE [prod_short](includes/prod_short.md)]  tengir hann eftirspurnina og framboðið. Þú nálgast tengilinn á View-aðeins síður úr fylgiskjalslínunum. Þegar framboð finnst ekki, stofnar dynamic pöntunarrakningarkerfið aðgerðaboð á áætlunarvinnublaðinu með tillögum um framboðsáætlun.  

Kvika pöntunarrakning auðveldar notandanum að meta hvort samþykkja eigi tillögur um framboðapöntun. Frá framboðinu kemur fram sú krafa sem skapaði framboðið. Frá eftirspurnarhliðinni, þá greinir það framboðið sem á að ná eftirspurninni.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Dæmi um breytilega pöntunarrakningu.":::

Frekari upplýsingar í  [hönnunarlýsingu: frátekning, pöntun Rakning og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).  

Í fyrirtækjum með lágt vöruflæði og minni þróaðri vöruuppbyggingu gæti verið nóg að nota dynamic pöntunarrakningu fyrir framboðáætlanagerð. Í viðskipti-umhverfi er hins vegar ætlunin að nota áætlanakerfið til að tryggja rétt samhæfðu framboðsumhverfis.  

### Breytilegar pöntunarrakningar vs. áætlanakerfi

Það gæti verið erfitt að skilja á milli áætlanakerfisins og kviku pöntunarrakningar. Bæði sýna frálag í áætlanavinnublaði með því að leggja virkninni sem skipuleggjandi ætti að taka. Hins vegar er mismunandi hvernig þessi framleiðsla er framleidd.  

Í áætlanakerfinu er fjallað um allt framboðs-og eftirspurnarmynstur vöru. Hún telur öll stig UPPSKRIFTARSTIGVELDIS vera eftir tímalínu. Kvika pöntun Rakning aðeins aðsetur staða pöntunar sem virkjaði hana. Þegar mótkrafa og framboð er stofnuð, stofnar áætlanakerfið tengla í runustillingu notanda sem er óvirkur. Kvika pöntunarrakningar stofnar sjálfkrafa tengingar þegar eftirspurn eða framboð er skráð. Til dæmis þegar sölu-eða innkaupapöntun er stofnuð.  

Kvika pöntunarrakningartenglar eftirspurn og framboð á fyrsta flokks framreiddur Grunnur þegar gögn eru færð inn. Þessi grundvöllur getur leitt til röskun í forgangsröðun. Til dæmis gæti sölupöntun sem færð var inn fyrst með gjalddaga í næsta mánuði verið tengd framboði í birgðum. Næsta sölupöntun á morgun gæti valdið aðgerðaboð til að stofna nýja innkaupapöntun til að ná í hana. Eftirfarandi mynd sýnir þessa atburðarás.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Dæmi um pöntunarmælingar í framboðnum áætlunum 1.":::

Áætlanakerfið er fjallað um eftirspurn og framboð á vörum í forgangsröðinni. Pöntuninni er forgangsraðað eftir gjalddögum og pöntunargerðum. Sem er, á fyrstu sem hefur verið þörf-þjónað skv. Það eyðir öllum pöntunarrakningartenglum sem voru búnir að vera breytilegir og endurtengjast þeim í samræmi við forgang gjalddaga. Þegar búið er að keyra áætlanakerfið hefur það leyst úr öllu ójafnvægi á milli eftirspurnar og framboðs, eins og sýnt er hér að neðan fyrir sömu gögn.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Dæmi um pöntunarmælingar í viðauka skipulagslaga 2.":::  

Eftir að áætlun hefur verið keyrð, inniheldur taflan aðgerðaboðum ekki nein aðgerðaboð. Þeim skilaboðum er skipt út fyrir þær aðgerðir sem lagðar eru til á áætlunarblaðinu. Frekari upplýsingar um  [rakningartengla pöntunar á meðan á áætlanagerð](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level) stendur.  

## Röð og forgangur í áætlun

Röð útreikninganna í áætlun þinni er mikilvæg fyrir það að fá starfið afgreitt í hæfilegu magni. Forgangsröðun þarfa og fjármuna gegnir einnig mikilvægu hlutverki við að ná sem bestum árangri.  

Áætlanakerfið er kröfuknúið. Vörur á háu stigi ættu að vera áætlaðar áður en lágstig vara vegna þess að þau gætu myndað eftirspurn eftir minni vörum. Til dæmis, áætla smásölustaði fyrir dreifingarstöðvar þar sem smásölustaðurinn gæti innihaldið eftirspurn úr dreifingarstöð. Á nákvæmu jöfnunarstigi ef losuð framboðapöntun getur nær yfir sölupöntun kerfið ætti ekki að búa til nýja framboðstegundinni. Framboð með ákveðið lotunúmer ætti ekki að vera úthlutað til að ná almennri eftirspurn ef önnur eftirspurn krefst þessarar tilteknu lotu.  

### Vöruforgangur / Lægra stigs kóði

Í framleiðslu-umhverfi, eftirspurn fyrir lokið, seljanlega vöru mun leiða í unnum eftirspurn fyrir íhluti sem eru í tilbúna hlutnum. Uppbygging uppskriftar stjórnar íhlutauppbyggingunni og getur náð yfir nokkur stig hálfunninna vara. Áætlanagerð vöru á einu stigi mun valda afleiddri eftirspurn fyrir íhluti á næsta stigi. Þetta stigveldi mun á endanum leiða til afleiddrar eftirspurnar fyrir keyptar vörur. Áætlanakerfið fyrir vörur í röðun þeirra í heildarstigveldi UPPSKRIFTAR. Kerfið byrjar á að halda seljanlegum vörum á efsta stigi og heldur áfram niður framleiðsluskipulagið á neðra þrepi varanna (samkvæmt lágstigskótanum).  

Eftirfarandi mynd sýnir röðina sem  [!INCLUDE [prod_short](includes/prod_short.md)]  bendir á framboðspantanir í efsta þrepi. Hún tekur fram að tillögurnar hafi verið samþykktar og sýnir neðriliðum einnig.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Áætlun um efni uppskrifta.":::

Til að fræðast meira um framleiðsluatriði er farið í  [álagsprónsérsnið](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### Fínstilla afköst fyrir lágstigsútreikninga

Útreikningar fyrir lágstigs kóða geta haft áhrif á afköst kerfisins. Til að minnka áhrifin er hægt að slökkva á  **breytilegum útreikningi**  á lágmörkun kóða á  **uppsetningu**  framleiðslunnar. Þegar það er gert  [!INCLUDE[prod_short](includes/prod_short.md)]  leggur hann til að stofnuð sé ítrekunarfærsla vinnslu til að uppfæra lágstigskóta daglega. Hægt er að ganga úr skugga um að vinnslan keyri utan vinnutíma með því að tilgreina upphafstíma í reitnum **Fyrsti upphafsdagur/tími**.

Einnig er hægt að flýta útreikningum lágstigs kóða með því að  **kveikja á útreikningi**  á bestun lágstigs kóða á  **síðunni Uppsetning**  framleiðslu.

> [!IMPORTANT]
> Ef valið er að fínstilla afköst notar [!INCLUDE[prod_short](includes/prod_short.md)] nýjar útreikningsaðferðir til að ákvarða lágstigskóða. Ef þú átt framlengingu sem treystir á atburði sem notaðir eru við gamla útreikninga þá gæti framlengingunni hætt að virka.

### Birgðageymslur / Forgangur millifærslustigs

Fyrirtæki með fleiri en eina staðsetningu gætu þurft að áætla fyrir hverja staðsetningu fyrir sig. Til dæmis gæti öryggisbirgðastig vöru og Endurpöntunarstefna verið mismunandi frá einum stað til annars. Tilgreina verður áætlunarfæribreytur fyrir hverja vöru og staðsetningu.  

Hægt er að nota SKUs til að tilgreina einstakar áætlunarfæribreytur. Hægt er að líta á BHE sem vöru í tiltekinni birgðageymslu. Ef be hefur ekki verið skilgreint fyrir birgðageymsluna  [!INCLUDE [prod_short](includes/prod_short.md)]  mun hún nota færibreytur sem stilltar eru á birgðaspjaldinu. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar út áætlun aðeins fyrir virkar staðsetningar þar sem eftirspurn eða framboð er fyrir tiltekinn hlut.  

Hægt er að afgreiða öll atriði á hvaða stað sem er, en  [!INCLUDE [prod_short](includes/prod_short.md)]  hefur strangt aðhald haft í hugmyndavinnu staðsetningar. Til dæmis er ekki hægt að fullnægja sölupöntuninni fyrir vöru á einum stað með lager frá öðrum stað. Magn birgða þarf fyrst að flytja af þeirri staðsetningu sem tilgerind er á sölupöntun.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Áætlanir um birgðahaldseiningar.":::

Frekari upplýsingar hjá  [Hönnunarmiðstöð: flutningar í áætlanagerð](design-details-transfers-in-planning.md).  

### Forgangur pöntunar

Innan tiltekinnar birgðahaldseiningar, táknar umbeðin eða tiltæk dagsetning hæsta forgang; eftirspurn í dag ætti að mæta áður en eftirspurn næstu viku er mætt. En burtséð frá þessu forgangskröfum er mismunandi eftirspurnar-og framboðstegundum raðað eftir mikilvægi fyrirtækja til að ákveða hvaða eftirspurn eigi að vera fullnægt fyrst. Á framboðhliðinni ákvarðar Uppruni framboðs að nota fyrst. Frekari upplýsingar um  [forgangsröðun pantana](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## Eftirspurnarspá og standandi pantanir

Spá og standandi pöntun endurspegla bæði vænta eftirspurn. Standandi pöntunin, sem nær yfir ætluð kaup viðskiptamanns á tilteknum tíma, er ætlað að minnka óvissu í heildarspá. Standandi pöntun er viðskiptavinarbundin spá ofan á ótilgreinda spá, eins og sést í eftirfarandi mynd.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Áætlanagerð með spám.":::

Frekari upplýsingar í  [spáreftirspurn eru lækkaðar eftir sölupöntunum](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## Úthlutað á áætlun

Enduráætla þarf allar vörur fyrir þegar eftirspurnar-eða framboðsmynstrið hefur breyst frá því að áætlun var reiknuð síðast. Til dæmis, ef ný sölupöntun er sett inn eða hún breytt, skal endurreikna áætlunina. Aðrar ástæður endurákvörðunar fela í sér breytingu á spá eða öryggisbirgðamagn. Breyting á frumvarpi með því að bæta við eða fjarlægja íhlut myndu líklegast einnig gefa til kynna breytingu, en aðeins um hlutahlutinn.  

Áætlanakerfið fylgist með slíkum tilvikum og úthlutar viðeigandi vörum til að gera áætlun.  

Fyrir margar staðsetningar gerist úthlutunin á stigi vörunnar á birgðageymslusamsetningu. Ef sölupöntun hefur verið stofnuð á aðeins einni birgðageymslu  [!INCLUDE [prod_short](includes/prod_short.md)]  úthlutar hún vörunni í þeirri birgðageymslu til áætlanagerðar.  

Ástæðan fyrir að velja vörur fyrir áætlun grundvallast á afköstum kerfisins. Ef eftirspurnarteygni vöru hefur ekki breyst hefur áætlanakerfið ekki lagt til neinar aðgerðir til að grípa til. Án áætlunarúthlutuninni þyrfti kerfið að framkvæma útreikninga fyrir alla vöru til að finna út hvað ætti að áætla fyrir. Nánari upplýsingar um ástæðurnar til að úthluta vörum til áætlunar eru  [í Hönnunarupplýsingum: úthlutun töflu](design-details-planning-assignment-table.md).  

Eftirfarandi eru þeir áætlunarkostir sem eru í boði:  

* **Reikna áætlun**  endurgerðar reiknar allar valdar vörur hvort sem þær eru nauðsynlegar eða ekki.  
* **Reikna út nettó Breytingaáætlun**  reiknar eingöngu út þær vörur sem hafa fengið breytingu á eftirspurnar-og framboðsmynstri og hefur því verið falið að áætla.  

Sumir telja að Skipulagning nettó breytinga eigi að fara fram á Flúðum, til dæmis þegar sölupantanir eru færðar inn. Áætlun um flákann er hins vegar ruglingsleg þar sem kvikar pöntunarrakningar og aðgerðaboð eru einnig reiknuð á Flúðum. [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á rauntíma í boði-loforð stjórnar. Það gefur pop-up viðvaranir þegar sölupantanir eru færðar inn og núverandi framboðslátt getur ekki uppfyllt eftirspurnina.  

Áætlanakerfið aðeins áætlanir um vörurnar sem þú hefur undirbúið með viðeigandi áætlunarfæribreytum. Annars er gert ráð fyrir því að þú munt áætla vörurnar handvirkt eða hálfsjálfvirkt með því að nota Pantanáætlunaraðgerðina. Ef fræðast á um sjálfvirkar áætlanagerðar er farið í  [hönnunarupplýsingar: jöfnun eftirspurnar og framboð](design-details-balancing-demand-and-supply.md).  

## Vöruvíddir

Eftirspurn og framboð geta haft afbrigðiskóða og staðsetningarkóða sem verður að virða þegar áætlanakerfið finnur jafnvægi framboðs og eftirspurnar.  

[!INCLUDE [prod_short](includes/prod_short.md)] meðhöndlar afbrigði og birgðageymslukóta sem vöruvíddir í sölupöntunarlínu, birgðafærslu o. a. frv. Í samræmi reiknar það áætlun fyrir hverja samsetningu afbrigðis og birgðageymslu eins og samsetningin væri aðskilið vörunúmer.  

Í stað þess að reikna út fræðilegar samsetningar af afbrigði og birgðageymslu  [!INCLUDE [prod_short](includes/prod_short.md)]  reiknar aðeins út þær samsetningar sem eru í raun og veru í gagnagrunninum. Nánari upplýsingar um það hvernig áætlunarkerfið fæst með birgðageymslukótum í eftirspurn er að fá í  [Hönnunarupplýsingum: eftirspurn á auðum stað](design-details-balancing-demand-and-supply.md).  

## Vörueigindir

Vörur hafa oft almennar eigindir, eins og am vörunúmer, afbrigðiskóta, birgðageymslukóta og gerð pöntunar. Hver eftirspurnar-og framboðsatburður getur þó verið með öðrum lýsingum, t.d. rað-eða lotunúmerum. Áætlanakerfið skipuleggur þessar eigindir á ákveðinn hátt, allt eftir reglustigi.  

Tengill á milli pantana á milli eftirspurnar og framboðs er önnur gerð eigindar sem hefur áhrif á áætlunarkerfið. Frekari upplýsingar á  [pöntunartenglar](#order-to-order-links) til að fá nánari upplýsingar.

### Tilgreindir eiginleikar

Sumir eftirspurnareiginleikar eru sértækir og framboð verður að samsvara þeim nákvæmlega.

* Rað-eða lotunúmer sem þarfnast sérstakrar umsóknar (þessar eigindir eru nauðsynlegar ef kveikt er á þeim sn í  **tilteknum rakningu**  eða  **lotu rakningar**  **á vörurakningarkóta**  fyrir vörurakningu sem notuð er í vörunni.)  
* Tenglar í framboðspantanir stofnaðir handvirkt eða sjálfvirkt fyrir tiltekna eftirspurn (tenglar á milli pantana).  

Í áætlanakerfi gilda eftirfarandi reglur um þessar eigindir:  

* Eftirspurn með sérstaka eiginleika er aðeins hægt að uppfylla með framboði sem passa við eiginleika.  
* Framboð með sérstaka eiginleika getur einnig fullnægt eftirspurn sem ekki sérstaklega krefst þeirra eiginleika.  

Ef birgðir eða áætlaðar birgðir uppfylla ekki eftirspurn eftir tilteknum eiginleikum stingur áætlunarkerfið upp á nýrri framboðapöntun án þess að um skipulagsheilda sé að ræða.  

### Ótilgreindar eigindir

Raðnúmeraðar vörur til rað-eða lotu án sérstakrar raðnúmers og uppsetningar á vörurakningu gætu haft Óákveðin rað-eða lotunúmer. Hægt er að nota þessar gerðir af einhverju rað-eða lotunúmeri. Áætlanakerfið hefur meira frelsi til að stemma við, til dæmis, raðgerð eftirspurnar með raðstillt framboði, vanalega í birgðum.  

Eftirspurnarteygni með rað-eða lotunúmerum, sértækum eða ósértækum, er mikill Forgangur og eru þau undanþegin á frosksvæðinu. Þau verða hluti af áætlanagerð jafnvel þótt þau séu á gjalddaga áður en Upphafsdagsetningin er gerð.  [Frekari upplýsingar um rað-og lotunúmer eru sóttar eftir tilgreiningu stiga](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Til að fræðast nánar um stöðu Stöðueiginleika áætlanakerfisins er farið í  [rað-og lotunúmer og tenglar til pöntunarpöntunar eru undanþegnir fyrra tímabili](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## Tenglar á milli pantana

Pöntun-til-pöntun merkir að þú hafir keypt, sett saman eða framleitt vöru fyrir ákveðna eftirspurn. Ýmsar ástæður eru til að velja þessa stefnu:

* Eftirspurnin er ótíð.
* Afhendingartíminn er óverulegur.
* Nauðsynlegar eigindir eru breytilegar.  

Önnur tilfelli sem nota pöntunartengda tengla eru þegar samsetningarpöntun er tengd við sölupöntun í samsetningum sem settar eru saman í pöntun.  

Tenglar á milli pantana eru jafnaðir milli eftirspurnar og framboðs á fjóra vegu:  

* Þegar áætluð vara notar  **pöntunarendurpöntunarstefnuna**   
* Þegar notuð er framleiðslustefnu til pöntunar til að stofna Multi-stig eða framleiðslupantanir fyrir gerð verks (framleiða íhluti í sömu framleiðslupöntun)  
* Þegar stofnaðar eru framleiðslupantanir fyrir sölupantanir með aðgerðum áætlunarpantanirnar  
* Þegar vara er sett saman við sölupöntun (**Samsetningarregla**  er stillt á til að  **setja saman við pöntun**)  

Áætlanakerfið bendir til þess að aðeins sé pantað magn sem þarf. Innkaupa-, framleiðslu-eða samsetningarpöntun heldur áfram að samsvara eftirspurninni. Ef sölupöntun er til dæmis breytt í tíma eða magni, bendir áætlanakerfið á að framboðapöntuninni er breytt samkvæmt því.  

Þegar pöntunartenglar eru til staðar, felur áætlanakerfið ekki í sér tengt framboð eða birgðir í mótunarferlinu. Skipuleggjendur geta ákveðið hvort nota á tengda framboðið eða nýja eftirspurn. Í síðara tilfellinu geta þau eytt framboðinu eða fært handvirkt út tengda framleiðarpöntunina.  

Frátekningar og pöntun rakningartenglar brotna ef aðstæður verða ómögulegar. Til dæmis þegar verið er að færa eftirspurn í dagsetningu sem er á undan framboðinu. Pöntunartenglar til að aðlaga að breytingum á eftirspurn eða framboði og rjúfa aldrei.  

## Bókanir

Áætlanakerfið inniheldur ekki frátekið magn í útreikningum. Til dæmis, ef magn fyrir sölupöntun er að fullu eða að hluta frátekið, er ekki hægt að nota magnið til að ná yfir aðra eftirspurn.

Áætlunarkerfið inniheldur frátekið magn í áætlaðri birgðaforstillingu. Það verður að íhuga allt magn til að ákvarða hvenær endurpöntunarpunktur er liðinn og hversu margir á að endurskipuleggja til að ná hámarksbirgðastigi. Óþarfa frátekningar geta aukið hættuna á að birgðastig keyri lágt þar sem skipulagsheilarar greina ekki frátekið magn.  

Eftirfarandi mynd sýnir hvernig frátekningar geta hindrað áætlanagerð.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Áætlun með frátektum.":::

Frekari upplýsingar í  [hönnunarlýsingu: frátekning, pöntun Rakning og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).  

## Viðvaranir

Fyrsti dálkur í áætlanagerðarvinnublaði er fyrir viðvörunarreiti. VIÐVÖRUNARTEIKN birtast þegar áætlunarlína er stofnuð fyrir óvenjulegar aðstæður.  

Framboð á áætlunarlínum með viðvörunum er yfirleitt ekki breytt í samræmi við áætlunarfæribreytur. Þess í stað bendir áætlanakerfið á að framboð nái nákvæmlega því magni sem eftirspurn hefur verið. Hins vegar er hægt að setja kerfið upp þannig að það virðir áætlunarfæribreytur fyrir áætlunarlínur með ákveðnum viðvörunum. Upplýsingar um viðvörun eru sýndar á  **síðunni óraktar áætlunareiningar**  sem sýna einnig pöntunarrakningartengla sem ekki eru pöntunarnetseiningar. Til eru þrenns konar viðvaranir:  

* Neyð  
* Frávik  
* Athugið  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Viðvaranir á Áætlunarblað.":::

### Neyð

Neyðarviðvörunarbjöllur Sýna við tvenns konar aðstæður:  

* Þegar birgðir eru neikvæðar á upphafsdegi áætlunar  
* Þegar viðburðir á eftirdagnum framboðs-eða eftirspurnardagar eru til  

Ef birgðir vöru eru neikvæðar á upphafsdegi áætlunarinnar stingur kerfið upp á neyðarbirgðum fyrir neikvæða magnið sem á að koma á upphafsdagsetningu áætlunarinnar. Upphafsdagsetningin og magn neyðarpöntunarinnar eru tiltekin í viðvörunartextanum. Frekari upplýsingar við  [meðhöndlun áætlaðra neikvæðra birgða](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Fylgiskjalalínur með skiladagsetningum áður en upphafsdagsetning áætlunar eru sameinaðar í neyðarpöntunarpöntun. Pöntunin er áætluð til að koma á upphafsdegi áætlunar.  

### Frávik

Viðvörun um frávik birtist ef áætlaðar birgðir eru undir öryggismarki birgða. Áætlunarkerfið stingur upp á framboðspöntun til að uppfylla eftirspurnina á lokadagsetningunni. Viðvörunartextinn segir til um magn í öryggisbirgðum fyrir vöruna og dagsetninguna sem það magn varð of lítið.  

Brota á öryggisbirgðastigi er undantekning. Það ætti ekki að gerast ef endurpöntunarpunkturinn er rétt stilltur. Frekari upplýsingar í hlutverki [Endurpöntunarpunkta](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Tillögur um frábrigði hjálpa til við að tryggja að áætlaðar birgðir til ráðstöfunar eru aldrei lægri en öryggisbirgðastig. Lagt magn nær yfir öryggisbirgðir, án þess að miðað sé við áætlunarfæribreytur. Í einhverjum aðstæðum verða hins vegar pöntunarbreytur teknar með.  

> [!NOTE]  
> Áætlanakerfið kann að hafa gleypt varabirgðirnar vísvitandi og mun svo endurnýja þær samstundis. Lærðu meira á að  [neyta öryggisbirgðir](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### Athugið

Viðvörunin Til athugunar birtist við þrennar aðstæður:  

* Upphafsdagsetning áætlunarinnar er á undan kerfisdagsetningunni.  
* Áætlunarlínan stingur upp á því að útgefinni innkaupa- eða framleiðslupöntun verði breytt.  
* Áætlaðar birgðir eru umfram yfirflæðisstig á gjalddaga. Lærðu meira á  [að vera neðan við yfirstig](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> Í áætlunarlínum með viðvörunum  **er reiturinn Samþykkja aðgerðaboð**  ekki valinn vegna þess að búist er við því að áætlunin rannsaki línurnar áður en ætlunin er að framkvæma áætlunina.  

## Villulogs

 **Á beiðnasíðunni Reikna áætlun**  er hægt að velja  **reitinn stöðva og sýna fyrsta villureit**  til að láta stöðva áætlunarkeyrslu þegar fyrsta villan kemur upp. Skilaboð birtast með upplýsingum um villuna. Ef villa er til staðar sýnir áætlunarvinnublaðið aðeins áætlunarlínurnar sem hafa tekist áður en villan varð.  

Ef svæðið er ekki valið  **heldur keyrslan Reikna áætlun**  áfram þar til henni er lokið. Villur trufla ekki runuvinnsluna. Ef villur eru í boðum segir til um hversu margar vörur hafa áhrif. Á  **síðu villukladda**  áætlunar fást nánari upplýsingar um villuna og tengla við viðkomandi skjöl eða uppsetningar.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Villuskilaboð á áætlunarblaðinu.":::

## Sveigjanleiki áætlunar

Það er ekki alltaf hagkvæmt að áætla fyrirliggjandi framboðröð. Til dæmis þegar framleiðsla hefur hafist eða þú ræður aukavinnu á tilteknum degi til að vinna verkið. Til að tilgreina hvort áætlanakerfið getur breytt pöntun eru allar framboðslínur áætlunar með valkosti um  **sveigjanleika**  með tvo kosti:  **ótakmarkað**  eða  **ekkert**. Ef svæðið er stillt á  **ekkert** reynir áætlanakerfið ekki að breyta framboðslínu.  

Hægt er að velja valkost handvirkt í svæðinu, en í sumum tilfellum er það stillt sjálfkrafa með [!INCLUDE [prod_short](includes/prod_short.md)]. Sú staðreynd að hægt er að stilla sveigjanleika áætlunar handvirkt er mikilvægt þar sem það auðveldar að aðlaga notkun að lögun að mismunandi verkflæði og viðskiptatilfellum. Til að fræðast nánar um hvernig þetta svæði er notað er farið í  [hönnunarupplýsingar: flutningur í áætlanagerð](design-details-transfers-in-planning.md).  

## Áætlun pöntunar

Verkfæri grunnframboðsáætlanagerðar á síðunni **Pantanaáætlun** er hannað fyrir handvirka ákvarðanatöku. Hún telur engar skipulagsbreytingar og er því ekki fjallað frekar í þessari grein.  [Frekari upplýsingar er að áætla fyrir nýja eftirspurnarpöntun eftir pöntun](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Mælt er með að ekki sé notuð pantanáætlanagerð ef fyrirtækið notar þegar áætlunar-eða innkaupatillagnablöð. Framboðspantanir sem stofnaðar eru á síðunni **Pantanaáætlun** geta breyst eða verið eytt á meðan sjálfvirk áætlanagerð er keyrð. Þessar breytingar gerast vegna þess að sjálfvirk áætlunarkeyrsla notar áætlunarfæribreytur sem ekki er víst að hafi verið skráð þegar áætlunin var gerð handvirkt í síðunni Pöntunaráætlun.  

## Takmarkað álag

[!INCLUDE[prod_short](includes/prod_short.md)] leggur til grófa skorna tímaáætlun til að áætla sanngjarna nýtingu fjármuna. Það skapar ekki sjálfkrafa og viðhaldið ítarlegum áætlunum á grundvelli forgangsröðunar eða hagræðingarreglna.  

Fyrirhuguð notkun afkastagetan-takmarkaðra forðaeiginleika er eftirfarandi:

* Til að forðast ofhleðslu auðlinda
* Til að tryggja að afkastageta sé ekki eftir Óúthlutuð ef hún gæti lækkað tíma framleiðslupöntunar

Þegar áætlun með afkastagetu-takmörkuðum forða er  [!INCLUDE [prod_short](includes/prod_short.md)]  gerð tryggir það að tilföng eru ekki hlaðin fyrir ofan afkastagetu þeirra (alvarlegt álag). Hún úthlutar hverri aðgerð til næsta tiltæka tímarauta. Ef tímaraufa er ekki nógu stór til að ljúka aðgerðinni skiptir aðgerðin í tvo eða fleiri hluta í næsta tiltæka tímarauf.  

> [!NOTE]  
> Ef um aðgerðarskiptingu er að ræða er aðeins úthlutað einum tíma þar sem gert er ráð fyrir að einhver Handvirk leiðrétting sé gerð til að hámarka áætlunina.  

Hægt er að bæta við Hörpu tíma í tilföng til að lágmarka aðgerðarskiptingu. Í þetta sinn skulum  [!INCLUDE [prod_short](includes/prod_short.md)]  við áætla álagið á síðasta mögulega degi með því að lækka lítillega á álagsprósenta.  

## Sjá einnig .

[Hönnunarupplýsingar: Flutningur í áætlun](design-details-transfers-in-planning.md)  
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)  
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)  
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
