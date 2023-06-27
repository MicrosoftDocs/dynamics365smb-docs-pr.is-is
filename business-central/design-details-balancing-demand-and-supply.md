---
title: Hönnun lýsingar-Jafnvægisframboð og eftirspurn
description: Í greininni er því lýst hvernig eigi að forgangsraða markmiðum með því að mótframboð með eftirspurn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand"></a>Hönnun lýsingar: Jafnvægisframboð og eftirspurn

Til að skilja hvernig áætlanakerfið virkar er mikilvægt að skilja það forgangsröðuðu markmiðum:  

* Allri eftirspurn verður sinnt með nægu framboði.  
* Allt framboð þjónar tilgangi.  

Almennt séð, er þessum markmiðum náð með því að jafna framboð við eftirspurn.  

## <a name="supply-and-demand"></a>Framboð og eftirspurn

Með hugtakinu  *framboð*  er átt við hvers konar jákvætt eða magn í magni, svo sem:

* Birgðir
* Innkaup
* Samsetning
* Framleiðsla
* Flutningar á innleið
* Söluskil  

Með hugtakinu  *eftirspurn*  er átt við hvers konar brúttó eftirspurn, svo sem:

* Vara fyrir sölupöntun
* Íhlutur fyrir framleiðslupöntun

[!INCLUDE [prod_short](includes/prod_short.md)] Einnig er hægt að nota tæknilegar tegundir eftirspurnar, t.d. neikvæðar birgðir og innkaupaskil.

Til að flokka uppruna framboðs og eftirspurnar skipuleggur áætlanakerfið þær á tveimur tímalínum sem kallast birgðaforstillingar. Ein regla er eftir atvikum eftirspurn og hin er fyrir tilsvarandi framboðsatburði. Hvert framboðstilvik stendur fyrir eina einingu í pöntun, til dæmis:

* Sölupöntunarlínu
* Birgðafærslu
* Í framleiðslupöntunarlínu

Þegar birgðaforstillingar eru sóttar er eftirspurnarteygni dreift til að úttaksáætlun sem uppfylla neðantalin markmið sé sett upp.

Birgðastig og áætlunarfæribreytur eru annars konar framboð og eftirspurn. Þessar gerðir gangast undir samþætt jafnvægi að uppfylltum verðbréfamörkuðum. Nánari upplýsingar á  [Hönnunarsíðu: afgreiðsla endurpöntunarstefnu](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Hugtakið jafnvægislíkan, í stuttu máli

Eftirspurn kemur frá viðskiptavinum. Framboð er það sem búið er til og fjarlægt til að koma á jafnvægi. Áætlanakerfið byrjar með eftirspurninni og rekur síðan afturábak til útframboðs.  

Birgðaforstillingar innihalda upplýsingar um kröfur og birgðir, magn og tímasetningu. Þessar forstillingar mynda tvær hliðar á jöfnunarkvarðanum.  

Markmið áætlunar er að jafna framboð og eftirspurn vöru til að tryggja að framboð muni samræmast eftirspurn eins og hún er skilgreind með áætlunarfæribreytum og reglum.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Yfirlit um jöfnunarframboð og eftirspurn.":::

## <a name="process-orders-before-the-planning-start-date"></a>Vinna pantanir á undan upphafsdegi áætlunar

Til að komast hjá því að framboðsáætlun sýnir órökstuddar tillögur ætlar áætlanakerfið ekki að áætla neitt á tímabilinu áður en Upphafsdagsetningin áætlunar hefst. Eftirfarandi regla gildir um það tímabil:

* Öll framboð og eftirspurn á undan upphafsdegi áætlunartímabilsins telst hluti af birgðum eða afhent.  

Með örfáum undantekningum stingur áætlanakerfið ekki í neinar breytingar á framboðspantanir á tímabilinu eða stofnar pöntunarrakningartengla fyrir það tímabil. Eftirfarandi eru undantekningar frá þessari reglu:  

* Birgðir sem varpað er til ráðstöfunar, þ.m.t. Samtala framboðs og eftirspurnar á tímabilinu, er undir núlli.  
* Baksettar pantanir þurfa rað-eða lotunúmer.  
* Framboðstilkrafa er tengd við pöntunarstefnu. 

Ef fyrstu tiltæku birgðir eru undir núlli leggur áætlanakerfið til neyðarbirgðapöntun daginn fyrir áætlunartímabilið til að ná yfir magnið sem vantar. Þannig að áætlaðar og tiltækar birgðir eru alltaf að minnsta kosti núll þegar áætlun fyrir komandi tímabil hefst. Áætlunarlínan fyrir þessa framboðpöntun birtir neyðarviðvörunarteikn og veitir frekari upplýsingar.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a>Rað-og lotunúmer og röð tengla sem undanþegnir eru frá fyrra tímabili

Ef þörf er á rað-eða lotunúmerum eða að pöntunartenging sé til staðar, hunsar kerfið regluna um fyrra tímabil. Það mun fela í sér aftur dagsettar magn frá upphafsdagsetningunni og gæti stungið upp á leiðréttingum ef framboð og eftirspurn eru ekki samstillt. Þessir eftirspurnarflokkar verða að passa upp á að tryggja að ákveðinni eftirspurn sé fullnægt.

## <a name="load-inventory-profiles"></a>Sækja birgðaforstillingar

Til að flokka uppruna framboðs og eftirspurnar skipuleggur áætlanakerfið þær á tveimur tímalínum sem kallast birgðaforstillingar.  

Framboð og eftirspurn með gjalddögum á eða eftir upphafsdag áætlunar eru sóttar í hverja birgðasniðs. Við hleðslu er tegundum framboðs og eftirspurnar raðað eftir heildarforgangsröðun, svo sem:

* Gjalddagi
* Lágstigskóta
* Staðsetningu
* Afbrigði

Forgangsröðun pöntunar er notuð við mismunandi gerðir til að uppfylla mikilvægustu eftirspurnina fyrst. Frekari upplýsingar um  [forgangsröðun pantana](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Eftirspurn getur einnig verið neikvæð. Meðhöndla neikvæða eftirspurn sem framboð. Ólíkt Dæmigerðu framboði, er neikvæð eftirspurn talin vera föst framboð. Áætlanakerfið getur tekið það mið af þeim en mun ekki leggja til breytingar á því.  

Almennt séð, áætlanagerðarkerfi telur allar framboðspantanir eftir áætlunarupphafsdegi sem breytingum háð í því skyni að anna eftirspurn. Hins vegar, eftir að magn er bókað úr framboðskerfinu, getur áætlanakerfið ekki breytt því. Ekki er hægt að enduráætla eftirtaldar pantanir:  

* Útgefnar framleiðslupantanir sem eru notkun og frálag er bókað á.  
* Samsetningarpantanir þar sem búið er að bóka notkun eða frálag.  
* Millifærslupantanir þar afhending hefur verið bókuð.  
* Innkaupapantanir þar sem búið er að bóka móttöku.  

Fyrir utan að hlaða upp framboðs-og eftirspurnargerðum eru vissar tegundir hlaðnar með athygli eftir sérstökum reglum og vegtengingar. Í eftirfarandi köflum í þessari grein er lýst þessum reglum og meðfylgjandi.  

### <a name="item-dimensions-are-separated"></a>Vöruvíddir eru aðskildar

Reikna verður út framkomin áætlun fyrir hverja samsetningu vöruvídda, svo sem afbrigði og staðsetningu. Aðeins þarf að reikna út samsetningar sem bera með sér eftirspurn og/eða framboð.  

Áætlunarkerfið leitar að samsetningum í birgðasniðaforstillingunni. Þegar hann finnur sér nýja samsetningu stofnar hún innra eftirlitsskrá sem geymir upplýsingar um samsetninguna. Áætlunarkerfið setur síðan inn be-ið sem stýrifærsluna eða ytri lykkjan. Þar af leiðandi eru skipulagsheilur stilltar eftir samsettri vöruvíddasamsetningu og staðsetningu og kerfið kemst áfram í innri lykkjuna. 

> [!NOTE]  
> Ekki þarf að slá inn skr færslu þegar eftirspurn og/eða framboð er skráð fyrir tiltekna samsetningu vöruvíddasamsetningar og staðsetningar. Því ef BIRGÐAHALDSEINING er ekki til fyrir gefna samsetningu  [!INCLUDE [prod_short](includes/prod_short.md)]  stofnar tímabundin be-færslu sem er byggð á gögnum úr vörunni. Ef Staðsetningin sem  **er áskilin**  er á  **er kveikt á síðunni** Birgðagrunnur verður annað hvort að búa til be eða kveikja á  **íhlutunum á skiptistað** . Frekari upplýsingar eru í  [áætlun með eða án staðsetningar](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a>Raf-og lotunúmer eru hlaðin eftir tilgreiningu stiga

Raf-og lotunúmer eru hlaðin inn í birgðaforstillingarnar ásamt framboði og eftirspurn sem þeim er úthlutað.  

Eiginleikum framboðs og eftirspurnar er raðað eftir forgangi pöntunar og Skilgreining þeirra. Þar sem raðnúmer og lotunúmer samsvara því sem er í tilgreiningu, mun nákvæmari eftirspurn stemma áður en minna ákveðinnar eftirspurnar er þörf. Til dæmis gæti ákveðin eftirspurn verið lotunúmer fyrir sölulínu. Minni ákveðin eftirspurn gæti verið við sölu frá hvaða lotunúmeri sem er.

> [!NOTE]  
> Einu tilefnislausar forgangsreglur fyrir raðnúmer og lotu-númeraða framboð og eftirspurn eru stig tilgreiningar sem skilgreindar eru í samsetningum þeirra og hvernig Vörurakning er sett upp fyrir vörurnar.  

Við jöfnun, litið á áætlanakerfið sem hefur rað-og lotunúmer sem Ósveigjanlegt. Kerfið hækkar ekki eða endurtímasetja slíkar framboðspantanir. Ein undantekning á þessu er ef þær eru notaðar í venslum pöntunarpöntunar. Frekari upplýsingar á  [pöntunartenglar til að panta tengla eru aldrei brotnir](#order-to-order-links-are-never-broken). Þessi undantekning verndar framboðið frá móttöku margra, hugsanlega árekstrum, aðgerðabota þegar það er með misjöfnum eiginleikum. Til dæmis gæti mismikill eiginleiki verið þegar framboðið hefur safn af mismunandi raðnúmerum.  

Önnur ástæða þess að rað-og lotunúmer eru ónúmeruð er því að rað-og lotunúmerum er oft úthlutað seint í ferlinu. Það gæti verið ruglingslegt ef breytingar eru lagðar fram á þeim tímapunkti.  

Jöfnun á rað-og lotunúmeri virðir ekki regluna um að skipuleggja neitt fyrir upphafsdag áætlunar. Ef framboð og eftirspurn eru ekki samstillt munu áætlanakerfið leggja til breytingar eða nýjar pantanir, burtséð frá upphafsdagsetningu áætlunar.  

### <a name="order-to-order-links-are-never-broken"></a>Pöntunartenglar til að panta eru aldrei brotnir

Þegar áætlun er gerð til pöntunar verður aðeins að nota tengda framleiðarlínu fyrir það sem upphaflega var ætlað. Tengda eftirspurnin ætti ekki að falla undir önnur framboð, jafnvel þó að framboðið sé tiltækt í tíma og magni. Til dæmis er ekki hægt að nota samsetningarpöntun sem tengist sölupöntun í þeirri röð sem er sett saman til að ná annarri eftirspurn.  

Það þarf að hafa stöðuna nákvæmar til að geta krafist framboðs. Áætlanakerfið mun tryggja framboðið án þess að um sé að ræða færibreytur pöntunar, breytistykki og magn í birgðum (annað en magn sem tengist tengdum pöntunum). Af sömu ástæðu stingur kerfið upp á að minnka umframframboð ef tengda eftirspurnin er minnkjuð.  

Þessi jöfnun hefur einnig áhrif á tímann. Takmarkaði sjóndeildarhringurinn sem ákvarðast af tímarammanum er ekki virtur; framboð verður enduráætlað ef tímasetning eftirspurnar hefur breyst. Hins vegar verður hömlutími virtur og kemur í veg fyrir að pöntun-í-pöntun birgðir séu áætlaðar út, nema innri birgðir úr framleiðslupöntun á mörgum stigum (verkefnispöntun).  

> [!NOTE]  
> Einnig er hægt að tilgreina rað-og lotunúmer fyrir eftirspurn eftir pöntun. Í því tilfelli er framboðið ekki Ósveigjanlegt, sem venjulega er fyrir rað-og lotunúmerum. Í þessu tilfelli mun kerfið hækka eða lækka í samræmi við breytingar á eftirspurn. Ef ein eftirspurn er með misjöfnum rað-og lotunúmerum, eins og fleiri en eitt lotunúmer, verður ein framboðapöntun lögð til fyrir hverja lotu.  

> [!NOTE]  
> Spár ættu ekki að leiða til þess að stofnaðar séu nýjar birgðapantanir sem eru bundnar af pöntun-í-pöntun tengslum. Ef spáin er notuð ætti aðeins að nota hana til að mynda háða eftirspurn í framleiðsluumhverfi.

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Íhlutaþörf er hlaðin í samræmi við breytingar á framleiðslupöntun

Við meðhöndlun framleiðslupantana verður  áætlanakerfið að fylgjast með nauðsynlegum íhlutum áður en þeim er hlaðið í eftirspurnarforstillinguna. Íhlutalínur sem verða til við breytta framleiðslupöntun skipta línunum í upprunalegu pöntuninni. Breytingin tryggir að áætlanakerfið tvítekningar beri ekki áætlunarlínur fyrir íhlutaþörf.  

### <a name="consume-safety-stock"></a>Nota öryggisbirgðir

Magn öryggisbirgða er krafa sem er hlaðin inn í birgðasniðinni á upphafsdegi áætlunar.  

Öryggisbirgðir eru magn birgða sem eru settar til hliðar til að mæta óvissu í eftirspurn við áfyllingu. Hins vegar getur verið að það sé neytt til að fullnægja eftirspurn. Í því tilviki skal áætlanakerfið tryggja að öryggisbirgðir komi snögglega í staðinn. Kerfið leggur til birgðapöntun til að fylla út öryggisbirgðamagn á þeim degi sem þess er neytt. Áætlunarlínan birtir frávísunarviðvörunarteikn sem útskýrir að öryggisbirgðir hafi verið að hluta til eða að fullu verið notaðar með undantekningarpöntun fyrir það magn sem vantar.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Spáreftirspurn er minnkuð með sölupöntunum

Eftirspurnarspár tjá áætlaða framtíðareftirspurn. Þegar rauneftirspurn er slegin inn, yfirleitt sem sölupantanir fyrir framleiddar vörur, notar hún spána.

Spáin sjálf er ekki minnkuð með sölupöntunum. Spámagnið sem er notað í áætlunarútreikningi er hins vegar dregið frá magni söltunarinnar áður en eftirstandandi magn fer inn í eftirspurnarforstillinguna. Í sölu á tímabili er áætlanagerð inniheldur bæði opnar sölupantanir og birgðafærslur frá afhendingum sölu. Undantekningin frá þessari reglu eru þegar þær koma úr standandi pöntun.  

Skilgreina þarf gilt spártímabil. Dagsetningin á áætlaðrar magni skilgreinir upphaf tímabilsins, og dagurinn í næstu spá skilgreinir lok tímabilsins.  

Spá fyrir tímabil fyrir áætlunartímabilið er ekki notuð, óháð því hvort hennar var neytt. Fyrsta spátalan með vöxtum er annaðhvort upphafsdagsetningin í áætlun eða skásta dagsetningin á hana.  

Spáin getur verið fyrir mismunandi tegundir af eftirspurn:

* Sjálfstæða eftirspurn, svo sem sölupantana
* Háð eftirspurn, til dæmis framleiðslupöntunaríhlutir.

Vara getur haft báðar gerðir spár. Við áætlanagerð gerist notkun þeirra sérstaklega, fyrst fyrir sjálfstæða eftirspurn og síðan fyrir háð eftirspurn.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Eftirspurn eftir standandi pöntun er minnkuð í sölupöntunum

Spár eru eftir standandi sölupöntunum um leið og tilgreina þarf framtíðareftirspurn frá tilteknum viðskiptamanni. Eins og í (ótilgreindri) spá ætti raunveruleg sala að nota áætlaða eftirspurn og eftirstandandi magn ætti að færa inn birgðaforstillingu eftirspurnar. Notkun minnkar ekki magnið í standandi pöntun.

Í áætlunarútreikningi eru opnar sölupantanir sem tengjast tiltekinni línu standandi pöntunar, en hún felur ekki í sér gilt tímabil. Það felur einnig í sér bókaðar pantanir þar sem bókunarferlið hefur þegar dregið úr magni eftirstöðva standandi pöntunar.

## <a name="prioritize-orders"></a>Forgangsraða pöntunum

Innan ákveðins be táknar að Umbeðin dagsetning eða tiltæk sé Mesti forgangur. Nú ætti að brugðist við eftirspurn í dag en áður með eftirspurn næstu vikurnar. En, til viðbótar við þennan heildarforgang, gerir áætlanakerfið eftirfarandi tillögur í samræmi við forgangsröðun verkefna:

* Hvaða tegund af kröfu þú ættir að uppfylla fyrst.
* Hvaða heimild framboð skal gilda áður en beitt er öðrum heimildum um framboð.  

Hlaðið upp framboði og eftirspurn leggja til snið fyrir áætlaðar birgðir samkvæmt forgangsröðun.  

### <a name="priorities-on-the-demand-side"></a>Forgangskröfur á kröfuhlið

1. Þegar afhent: birgðafærsla  
2. Vöruskilapöntun innkaupa  
3. Sölupöntun  
4. Þjónustupöntun  
5. Framleiðsluþáttinn þarf  
6. Lína samsetningar tillögu  
7. Flutningspantanir á útleið.  
8. Standandi pöntun (sem hefur ekki þegar verið notuð af tengdum sölupöntunum)  
9. Spá (sem hefur ekki þegar verið notuð í annarri sölupöntun)  

> [!NOTE]  
> Innkaupaskil eru yfirleitt ekki í áætlunargerð framboðs; Þeir ættu alltaf að vera teknir úr lotu sem verður að skila. Ef ekki frátekið, skilar innkaupaskil hlutverki í framboði og er mjög forgangsraðað til að komast hjá því að áætlanakerfið leggur til framboðapöntun bara til að þjóna innkaupaskilum.  

### <a name="priorities-on-the-supply-side"></a>Forgangur á framboðsmegin

1. Þegar í birgðum: birgðafærsla (sveigjanleiki áætlunar = enginn)  
2. Vöruskilapöntun sölu (sveigjanleiki í áætlanagerð = enginn)  
3. Flutningspöntun á innleið  
4. Framleiðslupöntun  
5. Tillaga um skipun  
6. Innkaupapöntun  

### <a name="priority-related-to-the-state-of-supply-and-demand"></a>Forgangsröðun tengd ástandi framboðs og eftirspurnar

Auk forgangsröðunar út frá gerð framboðs og eftirspurnar, þá eru önnur atriði sem hafa áhrif á sveigjanleika skipulags. Til dæmis vöruhúsaaðgerðir og stöðu eftirfarandi pantana:

* Sölur
* Innkaup
* Millifærsla
* Samsetning
* Framleiðsla

Staða þessara pantana hefur eftirfarandi áhrif: 

1. Að hluta meðhöndlað (Sveigjanleiki áætlunar = Enginn)  
2. Þegar í vinnslu í vöruhúsi (sveigjanleiki áætlunar = enginn)  
3. Útgefið - allar pantanategundir (áætlunarsveigjanleiki = ótakmarkað)  
4. Fastáætluð framleiðslupöntun (sveigjanleiki áætlunar = ótakmarkaður)  
5. Áætlað/opið – allar pantanagerðir (Sveigjanleiki áætlunar = Ótakmarkaður)

## <a name="balancing-supply-with-demand"></a>Jafnvægisframboð með eftirspurn

Staða og eftirspurn áætlanakerfis með því að leggja til aðgerðir til að endurskoða framboðspantanir sem eru ekki samhæfar. Þetta jafnvægi gerist fyrir hverja samsetningu vöruvíddasamsetningar og staðsetningar.  

Ímyndaðu þér að hver birgðasniðs innihaldi tvo strengi:

* Strengi um eftirspurnartilvik, raðað eftir dagsetningu og forgangi
* Samsvarandi streng framboðs atvika

Með hverju tilviki er átt við upprunagerð hans og auðkenni. Reglurnar um jöfnun á vörunni eru til einföldunar. Samsvörun framboðs og eftirspurnar getur komið fram á hvaða tímapunkti sem er í ferlinu, sem hér segir:  

1. Ekker framboð eða eftirspurn fyrir vöruna => áætluninni er lokið (eða hún á ekki að hefjast).  
2. Eftirspurn er fyrir hendi en það er ekkert framboð = > framboð skal lagt til.  
3. Framboð er til en það er engin eftirspurn eftir því = > framboði skal aflýst.  
4. Bæði framboð og eftirspurn eru til = > spurt verður um og svarað áður en  [!INCLUDE [prod_short](includes/prod_short.md)]  hægt er að tryggja að framboð geti mætt eftirspurninni.

    Ef tímasetning framboðs hentar ekki, kannski er hægt að endurreisa framboðið, eins og hér er komið:  

    1. Ef framboðið er sett á undan eftirspurn, kannski er hægt að áætla framboðið út þannig að birgðir séu eins lágar og mögulegt er.  
    2. Ef framboðið er sett seinna en eftirspurnin, kannski er hægt að áætla framboðið áfram. Annars leggur kerfið til nýtt framboð.  
    3. Ef frambirgðin uppfyllir kröfuna á þeim degi, getur áætlanakerfi kannað hvort magn framboðs geti forað eftirspurninni.  

    Þegar Tímataka er í stað er hægt að reikna út magn til framboðs á eftirfarandi hátt:  

    1. Ef framboðsmagnið er lægra en eftirspurnin gæti framboðið hækkað (eða ekki, ef um Hámarksmagn er að ræða).  
    2. Ef framboðsmagnið er hærra en eftirspurnin er hægt að lækka birgðamagn (eða ekki, ef um er að ræða lágmarks magnstefnu).  

    Á þessu stigi er ein þessara tveggja aðstæðna fyrir hendi:  

    1. Núverandi eftirspurn er hægt að ná yfir, og þar af leiðandi hægt að loka og áætlanagerð fyrir næsta eftirspurn getur byrjað.  
    2. Birgðir hafa náð hámarksgildi svo eitthvert eftirspurnarmagn er óvarið. Í þessu tilviki er áætlanakerfi getur lokað núverandi framboð og halda áfram í næsta.  

 Aðferðin byrjar allt saman með næstu kröfunum og núverandi framboði, eða öfugt. Núverandi framboð gæti náð yfir þessa eftirspurn líka eða núverandi eftirspurn hefur ekki enn verið að fullu tryggðir.  

### <a name="rules-for-actions-for-supply-events"></a>Reglur um aðgerðir vegna framboðsatvika

Fyrir ofan útreikningana þar sem framboð verður að uppfylla eftirspurn er tekin sú krafa sem gefin er upp. Það er fyrir utan eftirlit með áætlanakerfinu. Hins vegar hefur áætlanakerfið umsjón með framboðskerfinu og mun gera eftirfarandi tillögur:

* Stofna nýjar framboðspantanir
* Endurtímasetja fyrirliggjandi pantanir eða breyta magni þeirra
* Hætta við framboðspantanir sem ekki er lengur þörf fyrir  

Til að útiloka framboðstilskipun úr skipulagstillögur er hægt að ríkið hafi engan sveigjanleika fyrir áætlanagerð (Sveigjanleiki áætlunar = enginn). Þá er umframframboð úr þeirri pöntun notað fyrir eftirspurn, án þess að stungið sé upp á neinni aðgerð. 

Almennt er lagt til að öll framboð hafi skipulagssveigjanleika sem takmarkist af skilyrðum hvers og eins af þeim aðgerðum sem lagðar eru til.  

* **Endurtímasetja út**: Dagsetning núverandi framboðspöntunar er hægt að Endurtímasetja út til að mæta skiladegi, nema

  * Taflan táknar birgðir (alltaf á degi núll).  
  * Það er með pöntun fyrir pöntun tengda við aðra eftirspurn.  
  * Það er fyrir utan gluggann til endurröðunar í tímarammanum.
  * Þar er nánari framboð sem hægt væri að nota.  
  * Á hinn bóginn kann notandinn að ákveða að enduráætla ekki vegna þess að:
  * Framboðröðin er bundin við aðra kröfuhafa á fyrri dagsetningu.  
  * Þarfnaðist endurröðunar er svo að lágmarki það er hverfandi.  

* **Endurrit í** : dagsetningu fyrirliggjandi framboðapöntun er hægt að áætla í, nema undir eftirfarandi skilyrðum:

  * Það tengist beint einhverri annarri eftirspurn.  
  * Það er fyrir utan gluggann fyrir endurröðun sem skilgreindur er í tímarammanum.

> [!NOTE]  
> Þegar vöru er raðað með pöntunarpunkti er hægt að endurtímasetja framboðapöntunina. Þetta gerist oft í framsettum framboðspantanir sem birtast af endurpöntunarpunkti.

* **Auka magn**: Magn núverandi framboðspöntunar má auka til að mæta eftirspurn nema framboð þess er tengt beint við eftirspurn með Pöntun fyrir pöntun tengil.  

> [!NOTE]  
> Þó að hægt sé að auka framboðsuppröð gæti aukningin verið takmörkuð vegna skilgreinds hámarksmagns.  

* **Minnka Magn**: Núverandi birgðapöntun með afgang miðað við núverandi eftirspurn getur lækkað til að mæta eftirspurn.  

> [!NOTE]  
> Þó að hægt sé að minnka magnið gæti umframmagn borið saman við eftirspurnina eftir skilgreindu Lágmarkspöntunarmagni eða pantað margfeldi. 

* **Hætta** við: þar sem Sérstök tilviljun er aðgerðin minnkun magns getur hætt við birgðapöntunina ef hún hefur verið minnkuð í núll. 
* **Nýtt** : Ef það eru ekki framboðspantanir eða ekki hægt að breyta fyrirliggjandi pöntun til að mæta magninu sem þarf á gjalddögum kröfunnar, er ný framboðapöntun lögð til.  

### <a name="determine-the-supply-quantity"></a>Ákvarðað framboðsmagn

Áætlunarfæribreyturnar sem eru með leiðbeinandi magni í hverri framboðapöntun eru skilgreindar.  

Þegar áætlanakerfið reiknar út magn nýrrar framboðapöntun eða magnið sem á að breyta í fyrirliggjandi pöntun gæti magnið sem er lagt til annað en raunveruleg eftirspurn.  

Ef hámarks birgðir eða fast pöntunarmagn er valið gæti magnið sem lagt er til aukist til að mæta föstu magni eða hámarksbirgðum. Ef endurpöntunarstefna notar endurpöntunarmark er hægt að auka magnið að minnsta kosti til að ná endurpöntunarmarkinu. 

Ráðlagt magn gæti verið breytt í þessari röð:  

1. Niður í hámarksmagn pöntunar.  
2. Upp að lágmarksmagni pöntunar.  
3. Upp til að mæta næsta margfeldi pöntunar.

### <a name="order-tracking-links-during-planning"></a>Panta rakningartengla við áætlanagerð

Til að panta rakningu við áætlanagerð endurraðar áætlunarkerfið pöntunarrakningartengla fyrir samsetningar vara, afbrigða og birgðageymslna. Kerfið endurraðar rakningartenglum af eftirfarandi ástæðum:

* Að sannreyna tillögur hennar um nær alla eftirspurn og tryggja að öllum framboðstilskipunum sé þörf.  
* Reglulega þarf að endurræsa pantanakrakki.  

Með tímanum verða rakningar pöntunartengla úr jafnvægi. Tenglarnir verða úr jafnvægi þar sem pöntunin rakningar-net er ekki endurraðað þar til eftirspurnar-eða framboðsatburður er lokaður.

Áður en mótframboð eftir eftirspurn eyðir áætlanakerfið öllum rakningartenglum pöntunar. Meðan á mótferlinu stendur, þegar kröfu um eða framboðsatburði er lokað, býr til nýja pöntunarrakningartengla milli framboðs og eftirspurnar.  

> [!NOTE]  
> Þó að varan sé ekki uppsett fyrir breytilega pöntunarrakningu mun áætlanakerfið búa til hollari pöntunarrakningartengla.

## <a name="close-balanced-supply-and-demand"></a>Náið jafnvægi framboðs og eftirspurnar

Mótframboð hefur þrjár mögulegar Útkomur:

* Nauðsynlegt magn og dagsetning eftirspurnaratburðar er uppfyllt og áætlun um þau er hægt að loka. Framboðsatburðurinn haldist opinn og gæti mögulega náð yfir næstu eftirspurn. Að halda framboðstilvikinu opnu leyfir jöfnunarferli að byrja á með núverandi atburði og næstu eftirspurn.  
* Ekki er hægt að breyta framboðinu til að ná öllum eftirspurninni. Eftirspurnaratburðurinn er enn opinn með óteygið magn sem gæti hugsanlega þakið næsta afgreiðsluatburð. Því er núverandi framboðstegundunum lokað og jöfnun getur hafist aftur við gildandi eftirspurn og næsta framboðsatburð.  
* Öll eftirspurnin er þakin og það er ekki næg eftirspurn (eða það var engin eftirspurn á öllum). Umframframboð gæti lækkað (eða hætt við) og því síðan lokað. Einnig ætti að hætta við önnur framboðstilvik.  

Að lokum býr áætlanakerfið til pöntunarrakningartengil milli framboðs og eftirspurnar.  

### <a name="create-the-planning-line-suggested-action"></a>Stofna áætlunarlínuna (leiðbeinandi aðgerð)

 **Ef nýtt**,  **breytt magn**,  **endurröðun**,  **endurröðun og breytt magn** eða  **Hætta**  við aðgerð er lögð til til að endurskoða framboðpöntunina, stofnar áætlanakerfið áætlunarlínu á áætlunarblaðinu. Til að panta rakningu er áætlunarlínan stofnuð ekki aðeins þegar framboðtilvikinu er lokað, heldur einnig ef eftirspurnaratburðurinn er lokaður. Þetta gildir jafnvel þó að framboðsatburðurinn sé enn opinn og gæti breyst þegar Næsti eftirspurnaratburður er unninn. Hugsanlega er hægt að breyta áætlunarlínunni aftur þegar hún er stofnuð.

Til að minnka álagið á gagnagrunninum við meðhöndlun framleiðslupantana er hægt að viðhalda áætlunarlínunni í þremur þrepum:

* Stofna aðeins áætlanagerðarlínu með núverandi gjalddagadagsetningu og magni en án vegvísun og íhlutum.  
* Taka með leið: Áætluð leið felur í sér útreikning upphafs-og lokadagsetningar og tímasetningar. Hafa leiðbeiningu með kröfu hvað varðar gagnagrunnsaðgang. Til að ákvarða endapunkta og gjalddaga gæti verið nauðsynlegt að reikna leiðina jafnvel þótt framboðtilvikinu hafi ekki verið lokað. Til dæmis ef þú ert að gera áfram röðun.  
* Niðurbrot UPPSKRIFTAR tekið með: getur gerst rétt áður en framboðshamnum er lokað.

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)  
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
