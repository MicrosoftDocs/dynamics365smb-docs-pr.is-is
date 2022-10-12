---
title: Ctrl-hugmyndir í hönnunarupplýsingum áætlanakerfis
description: Virkni áætlanagerðar leggur til mögulegar aðgerðir sem notandi getur framkvæmt út frá eftirspurn/framboði og áætlunarfæribreytum vöru.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: a9218bf8d8fa2c7f84b08380742df17bd7be7afe
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605165"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis

Aðgerðir áætlanagerðar eru í runuvinnslu sem velur fyrst viðkomandi vöru og tímabil sem áætlun gildir um. Síðan, í samræmi við lágstigs kóða (UPPSKRIFTARSTÖÐU), kallar keyrslan kótaeiningu, sem reiknar út framboðstegundin eftir að mótframboð-krafa er sett upp og stingur upp á hugsanlegum aðgerðum sem notandinn á að taka. Ráðlagðar aðgerðir birtast sem línu á áætlunvinnublaðinu eða innkaupatillögunni.  

![Innihald síðu áætlunarvinnublaðs.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Innihald síðu áætlunarvinnublaðs")  

Reiknað er með að sá sem annast áætlanagerð í fyrirtæki, svo sem innkaupsaðili eða framleiðslustjóri, sé notandi áætlanakerfis. Áætlanakerfið hjálpar notandanum með því að framkvæma víðtæka en fremur einfalda útreikninga fyrir áætlun. Notandinn getur þá einbeitt sér að því að leysa úr erfiðari vandamálunum, líkt og því sem er frábrugðið því sem eðlilegt er.  

Áætlanakerfið er knúið áfram af viðbúinni og raunverulegri eftirspurn viðskiptavina, svo sem spám og sölupöntunum. Ef áætlunarútreikningurinn er keyrður mun það leiða til þess að forritið leggi til sérstakar aðgerðir fyrir notandann til að framkvæma varðandi mögulegt framboð frá lánardrottnum, samsetningar- eða framleiðsludeildum, eða millifærslur frá öðrum vöruhúsum. Þessar aðgerðir sem lagt er til kunna að vera til að stofna nýjar birgðapantanir, líkt og innkaupa eða framleiðslupöntun. Ef birgðapöntun eru þegar til gætu tillögurnar verið þess efnis að auka við pantanirnar eða flýta þeim til að koma til móts við eftirspurnarbreytingarnar.  

Annað markmið áætlunarkerfisins er að tryggja það að birgðamagnið hækki ekki að óþörfu. Í tilfelli minnkandi eftirspurnar mun áætlunarkerfið leggja til að annað hvort verði þeim birgðapöntunum sem eru fyrir hendi frestað, þær minnkaðar eða afpantaðar.  

MRP og MPS, Reikna nettóbreytingaráætlun og Reikna endurgerðaráætlun eru allt aðgerðir innan einnar kóðaeiningar sem inniheldur áætlunargrunninn. Hins vegar felur útreikningur framboðsáætlunarinnar í sér mismunandi undirkerfi.  

Hafið í huga að áætlanakerfið inniheldur ekki sérstakan grunn fyrir afkastaveitujöfnun eða fínstillingu. Því er slík áætluð vinna framkvæmd sem aðskilinn þáttur. Skortur á beinni samþættingu á milli þessara tveggja svæða merkir einnig að veruleg geta eða breytingar á áætlun munu útheimnta endurkeyrslu á áætlanagerð.  

## <a name="planning-parameters"></a>Færibreytur áætlana

Áætlunarfæribreytur sem notandi velur fyrir vöru eða vöruflokk stjórnar því hvaða aðgerðum áætlunarkerfið stingur upp á við ýmsar aðstæður. Áætlunarfæribreyturnar eru skilgreindar á hverju birgðaspjaldi til að stýra því hvenær, hversu mikið og hvernig er fyllt á.  

Áætlunarfæribreytur er einnig hægt að tilgreina fyrir allar samsetningar vöru, afbrigðis og birgðageymslu með uppsetningu birgðahaldseiningar (BHE) fyrir hverja samsetningu og skilgreiningu einstakra færibreyta.  

Nánari upplýsingar eru í [Upplýsingar um hönnun: Afgreiðsla endurpöntunarstefna](design-details-handling-reordering-policies.md) og [Upplýsingar um hönnun: Áætlunarfæribreytur](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Upphafsdagsetning áætlunar

Til að forðast framboðsáætlun sem notar opnar pöntunum í fortíðinni og stingur upp á hugsanlega ómögulegt aðgerðir, áætlanakerfi fer með allar dagsetningar fyrir upphafsdag áætlunargerðar sem frosið svæði þar sem eftirfarandi regla gildir:  

Allt framboð og eftirspurn fyrir upphafsdagsetningu áætlunartímabilsins verður talin hluti af birgðum eða afhent.  

Með öðrum orðum, það er gert ráð fyrir að áætlun fyrir fortíðina er framkvæmd í samræmi við uppgefna áætlun.  

Frekari upplýsingar eru í [Takast á við pantanir fyrir upphafsdag áætlanagerðar](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Kvika pöntun Rakning (pegging)

Breytilegar pöntunarrakningar, með samtímis stofnun aðgerðaskilaboða í áætlanavinnublaði, er ekki hluti af framboðsáætlanakerfi í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi eiginleiki tengir, í rauntíma, eftirspurnina og magnið sem uppfyllir hana, í hvert skipti sem framboð er stofnað eða því breytt.  

Til dæmis ef notandi slær inn eða breytir sölupöntun, mun kvika pöntunarrakningarkerfið um leið leita að viðeigandi framboði til að uppfylla eftirspurnina. Þetta getur verið úr birgðum eða fyrirsjáanlegri birgðapöntun (líkt og innkaupapöntun eða framleiðslupöntun). Þegar framboðsuppruni finnst, kerfið skapar tengsl milli eftirspurnar og framboðs, og sýnir það í skrifvörðum síðum sem eru nálgast á skjalalínum. Þegar nægt framboð er ekki hægt að finna, er kvik pöntunarrakningarkerfi býr til aðgerðaboð í áætlanavinnublaðinu með framboðsáætlunartillögum sem endurspegla kvika jöfnun. Í samræmi býður kvikt pöntunarrakningarkerfi upp á mjög einfalt áætlanakerfi sem getur bæði gagnast notanda sem áætlar og öðrum hlutverkum í framboðskeðjunni.  

Í samræmi er hægt að horfa á kvika pöntunarrakningu sem verkfæri fyrir notanda til að meta hvort samþykkja eigi pöntunartillögur fyrir framboð. Frá framboðshliðinni getur notandi séð hvaða eftirspurn hefur búið framboðið til og frá eftirspurnarhliðinni hvaða framboð á að sinna eftirspurninni.  

![Dæmi um gagnvirka rakningu pöntunar.](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Dæmi um gagnvirka rakningu pöntunar")  

Nánari upplýsingar eru í [Upplýsingar um hönnun: Frátekning, Vörurakning og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).  

Í fyrirtækjum með lítið vöruflæði og minna þróaða vöruuppbyggingu getur verið fullnægjandi til að nota kvika pöntunarrakningu sem helstu leiðir til framboðsáætlanagerðar. Hins vegar, í umhverfi þar sem meira er um að vera ætti alltaf að nota áætlanakerfið til að tryggja rétt jafnaða framboðsáætlun.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynamic pöntunarmælingar á móti í áætlanakerfi

Fljótt á litið kann það að virðast erfitt að greina á milli áætlunarkerfis og kvikrar pöntunarrakningar. Bæði sýna frálag í áætlanavinnublaði með því að leggja virkninni sem skipuleggjandi ætti að taka. Hins vegar er mismunandi hvernig þessi framleiðsla er framleidd.  

Áætlanakerfið tekur á öllu mynstri  framboðs og eftirspurnar varðandi tiltekna vöru á öllum stigum uppskriftarstigveldisins með fram tímalínunni, en kvik pöntunarrakning tekur á stöðu pöntunarinnar sem virkjaði það. Þegar eftirspurn og framboð er jafnað býr áætlanakerfið til tengla í notandavirkjuðu runustillingu, en kvik pöntunarrakning skapar tengla sjálfkrafa og samstundis, hvenær sem notandi slær inn eftirspurn eða framboð í forritinu, svosem sölupöntun eða innkaupapöntun.  

Breytilegar pantanir setja tengil milli eftirspurnar og framboðs þegar gögn eru slegin inn, á fyrstu kemur fyrstur fær reglu. Þetta getur leitt til röskun í forgangsröðun. Til dæmis er hægt að tengja sölupöntun sem færð er inn fyrst, með skiladegi í næsta mánuði, við framboð í birgðum, en næsta sölupöntun með skiladegi á morgun getur kallað fram aðgerðaboð um að stofna nýja innkaupapöntun til að sinna henni, eins og sýnt er hér fyrir neðan.  

![Dæmi um pöntunarrakningu í aðfangakeðju 1.](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Dæmi um pöntunarrakningu í aðfangakeðju 1")  

Hins vegar snýst áætlanakerfið um alla eftirspurn og framboð fyrir ákveðna vöru, í forgangsröð samkvæmt gjalddögum og pantanagerðum, það er, á þarf fyrst/fær fyrst grundvelli. Það eyðir pöntunarrakningartenglum sem voru búnir til kvikt og enduruppsetur þá í samræmi við skiladagsforgang. Þegar búið er að keyra áætlanakerfið hefur það leyst úr öllu ójafnvægi á milli eftirspurnar og framboðs, eins og sýnt er hér að neðan fyrir sömu gögn.  

![Dæmi um pöntunarrakningu í aðfangakeðju 2.](media/NAV_APP_supply_planning_1_planning_graph.png "Dæmi um pöntunarrakningu í aðfangakeðju 2")  

Eftir áætlunarkeyrslu eru engin aðgerðaboð eftir í töflunni Aðgerðarboðafærsla þar sem þeim hefur verið skipt út fyrir áætlaðar aðgerðir í áætlanavinnublaðinu.  

Frekari upplýsingar eru í [Pantanarakningartenglar við áætlunargerð](design-details-balancing-demand-and-supply.md#seriallot-numbers-are-loaded-by-specification-level).  

## <a name="sequence-and-priority-in-planning"></a>Röð og forgangur í áætlanagerð

Þegar koma á á áætlun skiptir  röð útreikninga máli til að ljúka megi verkinu innan hæfilegs tíma. Að auki, forgangsröðun krafna og tilfanga gegna mikilvægu hlutverki við að afla sem bestum árangri.  

Áætlanakerfið í [!INCLUDE[prod_short](includes/prod_short.md)] er knúið áfram af eftirspurn. Vörur á háu stigi skulu áætlaðar á undan lágstigsvörum því áætlunin fyrir hástigsvörur gæti myndað viðbótareftirspurn fyrir vörur á lægra stigi. Þetta þýðir til dæmis að smásölustaðsetningar skulu áætlaðar áður en dreifingarmiðstöðvar eru áætlapðar, vegna þess að áætlun fyrir smásala staðsetning getur falið frekari eftirspurn frá dreifingarmiðstöð. Í sundurliðuðum jöfnunarstigum þýðir þetta einnig að sölupöntun skuli ekki kveikja á nýrri framboðstekju ef hægt er að ná sölupöntuninni. Eins ætti ekki að úthluta framboð með tilteknu lotunúmeri til að uppfylla almenna eftirspurn ef önnur eftirspurn krefst þessara tilteknu lotu.  

### <a name="item-priority--low-level-code"></a>Forgangur/Lágstigskóti vöru

Í framleiðslu-umhverfi, eftirspurn fyrir lokið, seljanlega vöru mun leiða í unnum eftirspurn fyrir íhluti sem eru í tilbúna hlutnum. Uppbygging uppskriftar stjórnar íhlutauppbyggingunni og getur náð yfir nokkur stig hálfunninna vara. Áætlun vöru á einu stigi veldur afleiddri eftirspurn fyrir íhluti á næsta stigi, og svo koll af kolli. Þetta leiðir á endanum til afleiddrar eftirspurnar fyrir keyptar vörur. Þar af leiðandi áætlar áætlanakerfi vörur í flokkunarröð þeirra í stigveldi uppskrifa og byrjar á loknum seljanlegum vörum á efsta stigi og heldur áfram niður eftir vörustigveldinu að lægra skipuðum vörum (samkvæmt lágstigskóða)  

![Áætlanagerð fyrir uppskriftir.](media/NAV_APP_supply_planning_1_BOM_planning.png "Áætlanagerð fyrir uppskriftir")  

Tölurnar sýnir í hvaða röð kerfið gerir tillögur um framboðspantanir á efsta stigi og, að því gefnu að notandi vilja samþykkja þessar tillögur, fyrir hvaða lægra stigi sem er líka.  

Frekari upplýsingar um hluti tengda framleiðslu eru í [Hleðsla birgðaforstillinga](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

#### <a name="optimizing-performance-for-low-level-calculations"></a>Hagræðing vegna lágmörkun útreikninga

Útreikningar á lágstigskóða geta haft áhrif á afköst kerfis. Til að draga úr áhrifunum er hægt að gera **Útreikning á breytilegum lágstigskóða** óvirkan á síðunni **Framleiðsluuppsetning**. Þegar það er gert leggur [!INCLUDE[prod_short](includes/prod_short.md)] til að stofnuð sé endurtekin verkraðarfærsla sem mun uppfæra lágstigskóða daglega. Hægt er að ganga úr skugga um að vinnslan keyri utan vinnutíma með því að tilgreina upphafstíma í reitnum **Fyrsti upphafsdagur/tími**.

Einnig er hægt að virkja reiknireglu sem hraðar útreikningi á lágstigskóða með því að velja **Fínstilla útreikning fyrir lágstigskóða** á síðunni **Framleiðsluuppsetning**. 

> [!IMPORTANT]
> Ef valið er að fínstilla afköst notar [!INCLUDE[prod_short](includes/prod_short.md)] nýjar útreikningsaðferðir til að ákvarða lágstigskóða. Ef um er að ræða viðbót sem treystir á þau tilvik sem notast er við í gamla útreikningunum, getur viðbótin hætt að virka.   

### <a name="locations--transfer-level-priority"></a>Forgangur staðsetningar/flutnings-stigs

Fyrirtæki sem starfa á fleiri en einum stað getur þurft að áætla fyrir hverja staðsetningu fyrir sig. Til dæmis getur öryggisbirgðastig vöru og Endurpöntunarstefna verið mismunandi frá einum stað til annars. Í þessu tilviki, verða að vera tilgreind áætlunarfæribreyta fyrir hverja vöru og einnig á stað.  

Þetta er stutt við notkun birgðahaldseiningar, þar sem einstaka áætlunarfæribreytur geta verið tilgreindar á birgðahaldseiningarstigi. Hægt er að líta á BHE sem vöru í tiltekinni birgðageymslu. Ef notandi hefur ekki skilgreint birgðahaldseiningu fyrir þessa staðsetningu notar forritið sjálfgefið þær færibreytur sem voru stilltar á birgðaspjaldinu. Forritið reiknar út áætlun fyrir aðeins virkar staðsetningar, sem eru staðsetningar þar sem er fyrirliggjandi eftirspurn eða framboð á viðkomandi vöru.  

Í grundvallaratriðum er hægt að afgreiða öll atriði á hvaða stað sem er, en nálgun umsóknar á staðsetningarhugtakinu er nokkuð ströng. Til dæmis er ekki hægt að uppfylla sölupöntun á einum stað með magni í birgðum af öðrum stað. Magn birgða þarf fyrst að flytja af þeirri staðsetningu sem tilgerind er á sölupöntun.  

![Áætlanagerð fyrir birgðahaldseiningar.](media/NAV_APP_supply_planning_1_SKU_planning.png "Áætlanagerð fyrir birgðahaldseiningar")  

Nánari upplýsingar eru í [Hönnunarupplýsingar: Flutningur í áætlun](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Forgangsröðun pöntunar

Innan tiltekinnar birgðahaldseiningar, táknar umbeðin eða tiltæk dagsetning hæsta forgang; eftirspurn í dag ætti að mæta áður en eftirspurn næstu viku er mætt. En burtséð frá þessu forgangskröfum er mismunandi eftirspurnar-og framboðstegundum raðað eftir viðskiptamikilvægi til að ákveða hvaða eftirspurn eigi að vera fullnægjandi áður en til annarrar eftirspurnar kemur. Á framboðshlið segir pöntunarforgangur til um hvaða uppsprettu framboðs á að jafna áður en aðrar uppsprettur framboðs eru jafnaðar.  

Frekari upplýsingar eru í [Forgangsröðun pantana](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Eftirspurnarspár og standandi pantanir

Spá og standandi pöntun endurspegla bæði vænta eftirspurn. Standandi pöntunin sem fjallar um fyrirhugaða innkaup viðskiptavinar yfir ákveðinn tíma, virkar til að minnka óvissu um heildarspána. Standandi pöntunin er spá fyrir tiltekinn viðskiptamann ofan á ótilgreindri spá sem útskýrð er hér að neðan.  

![Áætlanagerð með spám.](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Áætlanagerð með spám")  

Frekari upplýsingar eru í [Spá um eftirspurn er minnkuð eftir sölupöntunum](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## <a name="planning-assignment"></a>Skipulagning úthlutunar

Allar vörur ættu að vera áætlaðar en aftur á móti er engin ástæða til að reikna áætlun fyrir vöru nema eftirspurnar- eða framboðsmynstur hafi breyst síðan áætlun var síðast reiknuð.  

Ef notandi hefur slegið inn nýja sölupöntun eða breytt pöntun sem fyrir er er ástæða til að endurreikna áætlunina. Aðrar ástæður eru m.a. breytingar á spá eða viðeigandi magn í öryggisbirgðum. Breyting uppskrift með því að bæta við eða fjarlægja íhlut myndi líklega gefa til kynna breytingu, en aðeins fyrir íhlut vöru.  

Áætlanakerfið fylgist með slíkum tilvikum og úthlutar viðeigandi vörum til að gera áætlun.  

Fyrir margar staðsetningar fer úthlutunin fram á vörustigi hverrar samsetningar staðsetningar. Ef, til dæmis, sölupöntun hefur verið búin til á aðeins einum stað, úthlutar forritið vörunni á þeim tiltekna stað fyrir áætlanagerð.  

Ástæðan fyrir að velja vörur fyrir áætlun grundvallast á afköstum kerfisins. Ef engin breyting á eftirspurnarmynstri vöru hefur átt sér stað mun áætlanakerfið ekki benda til þess að grípa þurfi til aðgerða. Ef áætlun væri ekki úthlutað yrði kerfið að gera útreikninga fyrir allar vörur til að finna út hvernig á að áætla og það myndi ganga um of á kerfið.  

Tæmandi skrá yfir ástæður fyrir úthlutun vöru í áætlanagerð er að finna í [Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md).  

Áætlunarvalkostir í [!INCLUDE[prod_short](includes/prod_short.md)] eru:  

-   Reikna endurgerðaráætlun reiknar öll valin atriði, hvort sem það er nauðsynlegt eða ekki.  
-   Reikna áætlun hreyfingar - reiknar aðeins þær völdu vörur sem eru með breytingu í eftirspurn-framboðmynstri og  hafa því verið úthltað í áætlun.  

Sumir notendur telja að nettóbreytingaáætlunargerð skuli framkvæma hratt, til dæmis, þegar sölupantanir eru færðar inn. Hins vegar gæti þetta verið misvísandi því kvik pöntunarrakning og aðgerðarboð eru einnig reiknuð út hvenær sem er. Að auki býður [!INCLUDE[prod_short](includes/prod_short.md)] upp á rauntíma tiltæki, sem veitir sprettiviðvaranir þegar þú slærð inn sölupöntun ef eftirspurnin er ekki hægt að uppfylla samkvæmt framboðsáætlun.  

Auk þessara sjónarmiða, er áætlanagerðarkerfi aðeins áætlanir fyrir þær vörur sem notandinn hefur undirbúið með viðeigandi breytur áætlanagerð. Annars er gert ráð fyrir að notandi vilja áætla vörurnar handvirkt eða hálf-sjálfvirkt með eiginleikanum Pantanaáætlun.  

Nánari upplýsingar um ferli sjálfvirkrar áætlunargerðar eru í [Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Vöruvíddir

Eftirspurn og framboð geta haft afbrigðiskóða og staðsetningarkóða sem verður að virða þegar áætlanakerfið finnur jafnvægi framboðs og eftirspurnar.  

Kerfið meðhöndlar afbrigði og staðsetningarkóða sem vöruvídd á sölupöntunarlínu, birgðafærslu o.s.frv. Í samræmi reiknar það áætlun fyrir hverja samsetningu afbrigðis og birgðageymslu eins og samsetningin væri aðskilið vörunúmer.  

Í stað þess að reikna hvaða fræðilega samsetningu af afbrigði og staðsetningu sem er reiknar forritið aðeins þær samsetningar sem í raun fyrir hendi í gagnagrunninum.  

Frekari upplýsingar um hvernig áætlanakerfi vinna með staðsetningarkóða eftir pöntun eru í [Hönnunarupplýsingar: Eftirspurn í autt birgðageymslu](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Eigindir vöru

Fyrir utan almennar vöruvíddir, eins og vörunúmer, afbrigðiskóða, birgðageymslukóða og pöntunarger, geta eftirspurnar- og framboðstilvik haft í för með sér frekari skilgreiningar í rað-/lotunúmerum. Áætlanakerfið skipuleggur þessar eigindir á ákveðinn hátt, allt eftir reglustigi.  

Tengill á milli pantana á milli eftirspurnar og framboðs er önnur gerð eigindar sem hefur áhrif á áætlunarkerfið.  

### <a name="specific-attributes"></a>Tilteknar eigindir

Ákveðin eigindir á eftirspurn eru sérstakar og verður að passa nákvæmlega við samsvarandi framboð. Eftirfarandi tvær sérstakar eigindir eru til:  

-   Krefjast raðnúmer/lotunúmer sem krefjast sérstaks forrits (**SN sértæk rakning** eða **lotusértæk rakning** gátreitur er valinn á síðunni **vörurakningarkóðaspjald** fyrir vörurakningarkóða sem er notað af hlutnum.)  
-   Tenglar í framboðspantanir stofnaðir handvirkt eða sjálfvirkt fyrir tiltekna eftirspurn (tenglar á milli pantana).  

Fyrir þessar eigindir beitir áætlanakerfið eftirfarandi reglum:  

-   Eftirspurn með sérstaka eiginleika er aðeins hægt að uppfylla með framboði sem passa við eiginleika.  
-   Framboð með sérstaka eiginleika geta einnig fullnægja eftirspurn sem er ekki að biðja sérstaklega umframboðþá eiginleika.  

Í samræmi, ef eftirspurn eftir sérstökum eigindum er ekki hægt að uppfylla með birgðum eða áætluðum framboði mun áætlunarkerfið stinga upp á nýrri framboðspöntun til að dekka þessa sérstöku eftirspurn án tillits til áætlunarfæribreyta.  

### <a name="non-specific-attributes"></a>Óákveðnar eigindir

Rað/Lotunúmeraðar vöru án ákveðinna vörurakningaruppsetningar kunna að bera raðnúmer / lotunúmeri sem þurfa ekki að beita á nákvæmlega sama raðnúmer / lotunúmer, en hægt er að beita á allir raðnúmer / lotunúmer. Þetta gefur áætlanakerfinu meira frelsi til að para saman, t.d. raðaðri eftirspurn með röðuðu framboði, vanalega í birgðum.  

Eftirspurn- framboð með raðnúmer / lotunúmeri, tiltekið eða ótiltekið, teljast forgangsmál og eru því undanþegin frystu svæði, sem þýðir að þau eru  áætlanagerð, jafnvel þótt það séu á tíma fyrir upphafsdag skipulagningar.  

Frekari upplýsingar eru í [Raðnúmer/lotunúmer eru hlaðin eftir lýsingarstigi](design-details-balancing-demand-and-supply.md#seriallot-numbers-are-loaded-by-specification-level).

Frekari upplýsingar um hvernig áætlanakerfi jafnar eigindir eru í [Tenglar vöru-/raðnúmers og pöntun-í-pöntun eru undanskildir frosna svæðinu](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Pöntunartenglar til að panta

Vinnsla á milli pantana merkir að vara er keypt, samsett eða framleidd til að uppfylla sérstaka eftirspurn. Venjulega tekur hún til A-vara og ástæða fyrir að velja þessa stefnu getur verið að eftirspurn er hverfandi, sem afhendingartími er óveruleg, eða nauðsynlegar eigindir mismunandi.  

Annað sérstak tilfelli sem notara tengil á milli pantana er þegar samsetningarpöntun er tengd við sölupöntun í samsetningu fyrir pöntun.  

Tenglar á milli pantana eru jafnaðir milli eftirspurnar og framboðs á fjóra vegu:  

-   Þegar áætlaða varan notar endurpöntunarstefnuna Pöntun.  
-   Þegar framleiðslureglan framleiðsla eftir pöntun er notuð til að stofna margþrepa framleiðslupöntun eða framleiðslupöntun af gerðinni verk (nauðsynlegir íhlutir framleiddir samkv. sömu framleiðslupöntun).  
-   Þegar þú býrð til framleiðslupantanir fyrir sölupantanir með sölupantanaáætlun eiginleikanum.  
-   Þegar vara er sett saman við sölupöntun. (Samsetningarregla er stillt á Samsetning til pöntunar.  

Í þessum tilvikum er áætlanakerfi mun aðeins benda til þess þarf magn. Þegar framleiðslu eru lokið halda innkaup, framleiðsla eða samsetningarpöntun áfram að passa við viðkomandi eftirspurn. Til dæmis ef tíma eða magni sölupöntunar er breytt stingur áætlunarkerfið upp á að samsvarandi birgðapöntun sé breytt til samræmis.  

Þegar pöntun fyrir pöntun tenglar eru til felur áætlanakerfið ekki í sér tengt framboð eða birgðir í jöfnunarferlinu. Það er undir notanda komið að meta hvort tengda framboðið ætti að nota til að mæta annarri eða nýrri eftirspurn og, ef svo er, eyða birgðapöntuninni eða taka tengdu birgðirnar frá handvirkt.  

Frátekningar og pöntunarrakningartenglar mun brotna ef ástandið verður ómögulegt, svo sem ef reynt er að færa eftirspurn að dagsetningu fyrr en framboð. Hins vegar lagar pöntun-í-pöntun tengillinn sig að breytingum í viðkomandi eftirspurn eða framboði og þar með er tengillinn aldrei rofinn.  

## <a name="reservations"></a>Bókanir

Áætlanakerfið tekur ekki frátekið magn með í útreikningana. Til dæmis ef sölupöntun hefur verið frátekin að hluta eða heild gagnvart magni í birgðum er ekki hægt að nota frátekna magnið í birgðum fyrir neina aðra eftirspurn. Áætlanakerfið tekur þetta eftispurn-framboð magn ekki með í útreikningana.  

Hins vegar tekur áætlanakerfið frátekið magn áfram með í forstillingu fyrir áætlaðar birgðir vegna þess að gera verður ráð fyrir öllu magni þegar ákvarðað er bæði hvenær endurpöntunarmarkinu hefur verið náð og hversu mikið þarf að endurpanta til að ná en fara ekki yfir hámarksbirgðastigið. Þar af leiðandi leiða óþarfa bókanir til aukinnar áhættu um að birgðastig verði lág vegna þess að áætlanagerð greinir ekki frátekið magn.  

Eftirfarandi mynd sýnir hvernig pöntun getur komið í veg heppilegasta áætlun.  

![Áætlanagerð með frátekningum.](media/NAV_APP_supply_planning_1_reservations.png "Áætlanagerð með frátekningum")  

Nánari upplýsingar eru í [Upplýsingar um hönnun: Frátekning, Vörurakning og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Viðvaranir

Fyrsti dálkur í áætlanagerðarvinnublaði er fyrir viðvörunarreiti. Hver áætlunarlína sem er búin til fyrir óvenjulegar aðstæður birtir viðvörunartákn í þessum reit, sem notandinn getur smellt á til að fá frekari upplýsingar.  

Framboði fyrir áætlunarlínur með viðvörunum er yfirleitt ekki breytt samkvæmt áætlunarfæribreytum. Þess í stað stingur áætlunarkerfið einungis upp á framboði til að anna nákvæmu eftirspurnarmagni. Hins vegar er hægt að stilla kerfið þannig að hún virði tilteknar áætlunarfæribreytur fyrir áætlunarlínur með viðvörunum. Frekari upplýsingar eru í lýsingunni á þessum valkostum fyrir **Reikna áætlun - Áætl.vinnubl.** runuvinnsla og **reikna áætlun - Innk.tillaga** runuvinnsla, í þeirri röð.  

Viðvörunarupplýsingar eru sýndar á síðunni **Óraktar áætlunareiningar** sem er einnig notaður til að sýna aðra pöntunarrakningarlista í einingar sem ekki eru af gerðinni pöntunarnet. Eftirfarandi tegundir viðvarana eru til:  

-   Neyð  
-   Frávik  
-   Athugið  

![Viðvaranir í áætlanavinnublaðinu.](media/NAV_APP_supply_planning_1_warnings.png "Viðvaranir í áætlanavinnublaðinu")  

### <a name="emergency"></a>Neyð

Neyðarviðvörun birtist í tveimur aðstæðum:  

-   Þegar birgðir eru neikvæðar á upphafsdagsetningu áætlunar.  
-   Þegar framboðs- eða eftirspurnaratvik eru til aftur í tíma.  

Ef birgðir vöru eru neikvæðar á upphafsdegi áætlunar stingur áætlunarkerfið upp á neyðarbirgðum fyrir neikvætt magn til að koma á upphafsdegi áætlunar. Upphafsdagsetningin og magn neyðarpöntunarinnar eru tiltekin í viðvörunartextanum. Frekari upplýsingar er að finna í [Að takast á við áætlaða neikvæða birgðastöðu](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Allar skjalalínur með skiladagsetningar á undan upphafsdagsetningu áætlunarinnar eru settar í eina neyðarpöntun til að varan berist á áætlaðri upphafsdagsetningu.  

### <a name="exception"></a>Frávik

Viðvörun um frávik birtist ef áætlaðar birgðir eru undir öryggismarki birgða. Áætlunarkerfið stingur upp á framboðspöntun til að uppfylla eftirspurnina á lokadagsetningunni. Viðvörunartextinn segir til um magn í öryggisbirgðum fyrir vöruna og dagsetninguna sem það magn varð of lítið.  

Þegar farið er undir öryggismagn í birgðum er það talið frávik þar sem það ætti ekki að gerast ef endurpöntunarmark hefur verið stillt rétt. Frekari upplýsingar eru í [Hlutverk endurpöntunarmarks](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Yfirleitt sjá sérstakar pöntunartillögur til þess að áætlaðar tiltækar birgðir séu aldrei undir öryggismarki birgða. Þetta þýðir að magnið sem var lagt til er rétt svo nóg til að anna öryggisbirgðum, án tillits til áætlunarfærslubreytum. Í einhverjum aðstæðum verða hins vegar pöntunarbreytur teknar með.  

> [!NOTE]  
>  Áætlanakerfið kann að hafa gleypt varabirgðirnar vísvitandi og mun svo endurnýja þær samstundis. Nánari upplýsingar er að finna í [Öryggisbirgðir má nota](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Athugið

Viðvörunin Til athugunar birtist við þrennar aðstæður:  

-   Upphafsdagsetning áætlunarinnar er á undan kerfisdagsetningunni.  
-   Áætlunarlínan stingur upp á því að útgefinni innkaupa- eða framleiðslupöntun verði breytt.  
-   Áætlaðar birgðir eru umfram yfirflæðisstig á gjalddaga. Frekari upplýsingar eru í [Að vera undir yfirflæðisstigi](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  Í áætlunarlínum með viðvaranir er reiturinn **Samþykkja aðgerðarboð** ekki valinn þar sem sá sem gerir áætlunina á að kanna þessar línur nánar áður en lokið er við áætlunina.  

## <a name="error-logs"></a>Villuskrár

Á beiðnisíðunni Reikna áætlun getur notandinn valið **Stöðva og sýna fyrstu villu** reitinn til að láta áætlunarkeyrslu hætta þegar það rekst fyrsta villa. Um leið birtast skilaboð með upplýsingum um villuna. Ef villa er til staðar eru aðeins áætlunarlínur sem lokið var við fyrir villuna í áætlunarvinnublaðinu.  

Ef reiturinn er ekki valinn heldur runuvinnslan Reikna áætlun áfram þangað til henni er lokið. Villur munu ekki trufla runuvinnsluna. Ef ein eða fleiri villur eru til staðar birtir forritið skilaboð um hvaða vörur villurnar höfðu áhrif á. Síðan **Villukladdi áætlunar** opnast og birtir upplýsingar um villuna og tengla í þau skjöl eða birgðaspjöld sem hún hafði áhrif á.  

![Villuboð í áætlanavinnublaðinu.](media/NAV_APP_supply_planning_1_error_log.png "Villuboð í áætlanavinnublaðinu")  

## <a name="planning-flexibility"></a>Sveigjanleiki áætlunar

Ekki er alltaf hentugt að áætla fyrirliggjandi framboðspöntun, til dæmis þegar framleiðsla er hafin eða viðbótarstarfsmenn hafa verið ráðnir á tilteknum degi til að framkvæma verkið. Til kynna hvort núverandi pöntun er hægt að breyta af áætlanakerfi, hafa allar framboðspantanalínur áætlanasveigjanleikareit með tveimur valkostum: Ótakmarkað eða ekkert. Ef reiturinn er stilltur á Ekkert reynir áætlanakerfið ekki að breyta birgðapöntunarlínunni.  

Reitinn má handvirkt stilla af notanda, þó í sumum tilfellum verður að vera stillt sjálfkrafa af kerfinu. Sú staðreynd að sveigjanleika skipulagningu má handvirkt stilla af notanda er mikilvægt, vegna þess að það gerir það auðvelt að laga notkun á eiginleikanum að mismunandi verkflæði og viðskiptatilvikum.  

Nánari upplýsingar um það hvernig þessi reitur er notaður eru í [Hönnunarupplýsingar: Flutningur í áætlun](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Pantanáætlun

Verkfæri grunnframboðsáætlanagerðar á síðunni **Pantanaáætlun** er hannað fyrir handvirka ákvarðanatöku. Það tekur ekki tillit til áætlanagerðarfæribreytur og er því ekki rætt frekar í þessu skjali. Frekari upplýsingar eru í [Gera áætlanir um nýja eftirspurn pöntun fyrir pöntun](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Ekki er ráðlegt er að nota pantanaáætlun ef fyrirtækið notar þegar áætlunarvinnublöð eða innkaupatillagnablöð. Framboðspantanir sem stofnaðar eru á síðunni **Pantanaáætlun** geta breyst eða verið eytt á meðan sjálfvirk áætlanagerð er keyrð. Það er vegna þess að sjálfvirk áætlanagerð er keyrð með áætlunarfæribreytum og hugsanlega tekur notandinn sem gerir handvirka áætlun á síðunni Pantanaáætlun ekki tillit til þeirra.  

## <a name="finite-loading"></a>Takmörkuð hleðsla

[!INCLUDE[prod_short](includes/prod_short.md)] er staðlað ERP kerfi, ekki stjórnkerfi afgreiðslu eða verslunar. Hún áætlar gerlega nýtingu tilfanga með því að leggja fram grófa áætlun en stofnar ekki og viðheldur sjálfkrafa ítarlegum áætlunum, byggðum á reglum um forgangsröðun eða bestun.  

Fyrirhuguð notkun á tilföngum með takmarkaða getu er 1): að forðast yfirálag á tilgreind tilföng og 2): að tryggja að engin afkastageta sé án úthlutunar ef úthlutun á henni gæti aukið viðdvalartíma framleiðslupöntunar. Eiginleikinn fela í sér enga aðstöðu eða möguleika til að forgangsraða eða hagræða starfsemi eins og búast má við að finna í sendingakerfi. Hins vegar getur það veitt gróflega áætlaðar upplýsingar um afkastagetu sem eru gagnlegar til að greina flöskuhálsa og forðast yfirálag á auðlindir.  

Við áætlum á tilföngum með takmarkaða getu tryggir kerfið að engin tilföng séu hlaðin yfir skilgreina getu (hættumörk) Þetta er gert með því að úthluta hverri virkni á næsta tiltekna tímabil. Ef tímabilið er ekki nógu langt til að hægt sé að ljúka allri aðgerðinni verður aðgerðinni skipt í tvo eða fleiri hluta á næstu tiltæku tímabilum.  

> [!NOTE]  
> Í tilviki uppskiptingar starfssemi er uppsetningartíma aðeins  úthlutað einu sinni vegna þess að það er gert ráð fyrir að sumir handvirk jöfnun sé gerð til að hámarka áætlun.  

Hömlutíma má bæta við tilföng til að draga úr skiptingu reksturs Þetta gerir kerfinu kleift að áætla hleðslu á síðasta mögulega dag með því auka álagsprósentuna lítillega ef það er hægt að minnka fjölda virkni sem er skipt.  

Þetta lýkur grind miðlægra hugmynda sem tengjast framboðsáætlunargerð í [!INCLUDE[prod_short](includes/prod_short.md)]. Í eftirfarandi köflum er dýpra kafað í þessar hugmyndir og þær settar í samhengi við áætlanagerðarverklag, jöfnun eftirspurnar og framboðs, sem og notkun á endurpöntunarstefna.  

## <a name="see-also"></a>Sjá einnig .

[Hönnunarupplýsingar: Flutningur í áætlun](design-details-transfers-in-planning.md)  
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)  
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)  
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
