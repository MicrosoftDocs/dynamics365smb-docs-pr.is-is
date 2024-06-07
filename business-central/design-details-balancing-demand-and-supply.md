---
title: Upplýsingar um hönnun - jöfnun framboðs og eftirspurnar
description: Í þessari grein er því lýst hvernig á að forgangsraða markmiðum með því að jafna framboð við eftirspurn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# Upplýsingar um hönnun: Jöfnun framboðs og eftirspurnar

Til að skilja hvernig áætlunarkerfið virkar er mikilvægt að skilja markmiðin sem hafa forgangsraðað:  

* Allri eftirspurn verður sinnt með nægu framboði.  
* Allt framboð þjónar tilgangi.  

Almennt séð, er þessum markmiðum náð með því að jafna framboð við eftirspurn.  

## Framboð og eftirspurn

Hugtakið *framboð* vísar til hvers kyns jákvæðs eða innleiðarmagns, svo sem:

* Birgðir
* Innkaup
* Samsetning
* Framleiðsla
* Millifærslur á innleið
* Vöruskil sölu  

Hugtakið *eftirspurn* vísar til hvers kyns brúttóeftirspurnar, t.d.:

* Vara fyrir sölupöntun
* Íhlutur fyrir framleiðslupöntun

[!INCLUDE [prod_short](includes/prod_short.md)] Einnig er hægt að nota tæknilegar tegundir eftirspurnar, t.d. neikvæðar birgða- og innkaupaskila.

Til að raða uppruna framboðs og eftirspurnar skipuleggur áætlunarkerfið þær eftir tveimur tímalínum sem kallast birgðaforstillingar. Ein forstilling er fyrir eftirspurnarviðburði og önnur er fyrir samsvarandi framboðsviðburði. Hver framboðstilvik táknar eina einingu í pöntun, svo sem:

* Sölupöntunarlína
* Birgðafærsla
* Framleiðslupöntunarlína

Þegar birgðaforstillingar eru hlaðnar eru eftirspurnar-framboðsstillingar jafnaðar til að vinna framboðsáætlun sem uppfyllir skráð markmið.

Birgðastig og áætlunarfæribreytur eru aðrar gerðir framboðs og eftirspurnar. Þessar tegundir gangast undir samþætta mótun til að fylla á vörur í birgðum. Nánari upplýsingar um [hönnun: Meðhöndlun endurpöntunarstefnu](design-details-handling-reordering-policies.md).

## Hugtakið jöfnun, í stuttu máli

Eftirspurnin kemur frá viðskiptamönnum. Framboð er það sem stofnað er og fjarlægt til að koma á jafnvægi. Áætlunarkerfið hefst á eftirspurninni og rekur síðan afturábak að framboðinu.  

Í birgðaforstillingum eru upplýsingar um eftirspurn og birgðir, magn og tímasetningu. Þessar forstillingar mynda tvær hliðar á mótmælikvarðanum.  

Markmið áætlunarinnar er að jafna framboð og eftirspurn vöru til að tryggja að framboð samsvari eftirspurn eins og hún er skilgreind samkvæmt áætlunarfæribreytum og reglum.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Yfirlit yfir jöfnun framboðs og eftirspurnar.":::

## Vinna pantanir fyrir upphafsdagsetningu áætlunarinnar

Til að forðast að framboðsáætlun sýni óraunhæfar tillögur mun áætlunarkerfið ekki áætla neitt á tímabilinu fyrir upphafsdagsetningu áætlunarinnar. Eftirfarandi regla á við um það tímabil:

* Allar framboðs- og eftirspurn fyrir upphafsdagsetningu áætlunartímabilsins eru taldar hluti af birgðum eða afhentum.  

Með nokkrum undantekningum mun áætlunarkerfið ekki leggja til breytingar á framboðspöntunum á tímabilinu eða stofna rakningartengla pantana fyrir það tímabil. Eftirfarandi eru undantekningar frá þessari reglu:  

* Birgðir sem áætlað er að séu tiltækar, þar á meðal samtala framboðs og eftirspurnar á tímabilinu, er undir núlli.  
* Bakfærðar pantanir þurfa rað- eða lotunúmer.  
* Framboðseftirspurnarsafnið er tengt við stefnu pöntunar eftir pöntun. 

Ef fyrstu tiltæku birgðir eru undir núlli leggur áætlanakerfið til neyðarbirgðapöntun daginn fyrir áætlunartímabilið til að ná yfir magnið sem vantar. Áætlaðar og tiltækar birgðir verða því alltaf að minnsta kosti núll þegar áætlanir um framtíðartímabilið hefjast. Áætlunarlínan fyrir þessa framboðspöntun birtir viðvörunartákn neyðarviðvörunar og veitir viðbótarupplýsingar.

### Rað- og lotunúmer og tenglar í pöntun eru undanþegnir fyrra tímabili  

Ef rað- eða lotunúmera er krafist eða tengill fyrir pöntun er til hunsar áætlunarkerfið regluna um fyrra tímabil. Í honum er bakdagsett magn frá upphafsdagsetningu og gæti lagt til leiðréttingaraðgerðir ef framboð og eftirspurn eru ekki samstillt. Þessi eftirspurnar-framboðssett verða að passa til að tryggja að tiltekinni eftirspurn sé uppfyllt.

## Álag birgðaforstillingar

Til að raða uppruna framboðs og eftirspurnar skipuleggur áætlunarkerfið þær eftir tveimur tímalínum sem kallast birgðaforstillingar.  

Framboð og eftirspurn með gjalddaga á eða eftir upphafsdagsetningu áætlunarinnar er hlaðið inn í hverja birgðaforstillingu. Þegar hlaðið er inn er framboðinu og eftirspurnartegundunum raðað eftir forgangsröðun í heild, svo sem:

* Eindagi
* Lágstigskótar
* Staðsetningu
* Afbrigði

Pöntunarforgangur er notaður fyrir mismunandi tegundir til að uppfylla mikilvægustu eftirspurnina fyrst. Nánari upplýsingar um [Forgangsröðun pantana](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Eftirspurn getur einnig verið neikvæð. Meðhöndla neikvæða eftirspurn sem framboð. Hins vegar, ólíkt dæmigerðu framboði er neikvæð eftirspurn talin föst framboð. Áætlunarkerfið getur tekið það með í reikninginn en leggur ekki til breytingar á því.  

Almennt séð, áætlanagerðarkerfi telur allar framboðspantanir eftir áætlunarupphafsdegi sem breytingum háð í því skyni að anna eftirspurn. Eftir að magn hefur verið bókað úr framboðspöntun getur áætlunarkerfið ekki breytt því. Ekki er hægt að enduráætla eftirfarandi pantanir:  

* Útgefnar framleiðslupantanir sem eru notkun og frálag er bókað á.  
* Samsetningarpantanir þar sem búið er að bóka notkun eða frálag.  
* Millifærslupantanir þar afhending hefur verið bókuð.  
* Innkaupapantanir þar sem búið er að bóka móttöku.  

Auk þess að hlaða inn framboðs- og eftirspurnartegundum eru ákveðnar tegundir hlaðnar með athygli að sérstökum reglum og tengslum. Eftirfarandi kaflar í þessari grein lýsa þessum reglum og tengslum.  

### Vöruvíddir eru aðgreindar  

Reikna þarf birgðaáætlun fyrir hverja samsetningu af vöruvíddum, eins og afbrigði og birgðageymslu. Aðeins þarf að reikna samsetningar sem hafa eftirspurn og/eða framboð.  

Áætlunarkerfið leitar að samsetningum í birgðaforstillingunni. Þegar hún finnur nýja samsetningu stofnar hún innri eftirlitsfærslu með upplýsingunum um samsetninguna. Áætlunarkerfið setur birgðahaldseininguna inn sem eftirlitsfærslu eða ytri lykkju. Þar af leiðandi eru áætlunarfæribreyturnar stilltar eftir samsetningu afbrigðis og birgðageymslu og kerfið getur haldið áfram að innri lykkjunni. 

> [!NOTE]  
> Ekki þarf að færa inn birgðahaldseiningarfærslu þegar færð er inn eftirspurn og/eða framboð fyrir tiltekna samsetningu afbrigðis og birgðageymslu. Ef birgðahaldseining er ekki til fyrir tiltekna samsetningu [!INCLUDE [prod_short](includes/prod_short.md)]  stofnar bráðabirgða birgðahaldseiningarfærsla sem byggð er á gögnum úr vörunni. Ef kveikt er á Birgðageymslunni áskilin **á síðunni**  **Birgðagrunnur verður annað hvort að stofna birgðahaldseiningu eða kveikja á** vífæringu á Íhlutum á staðnum **.**  Fræðast meira um áætlun [með eða án birgðageymslna](production-planning-with-without-locations.md).  

### Rað- og lotunúmer eru hlaðin inn með lýsingarstigi  

Rað- og lotunúmer eru hlaðin inn í birgðaforstillingarnar ásamt framboðinu og eftirspurninni sem þeim er úthlutað til.  

Framboðs- og eftirspurnareigindum er raðað eftir forgangi pöntunar og skilgreiningarstigi þeirra. Þar sem rað- og lotunúmer samsvarar lýsingarstiginu samsvarar nákvæmari eftirspurn á undan minni tiltekinni eftirspurn. Tiltekin eftirspurn gæti til dæmis verið lotunúmer sem tilgreint er fyrir sölulínu. Minni eftirspurn getur verið sala frá hvaða lotunúmeri sem er.

> [!NOTE]  
> Einu sérstakar forgangsreglur fyrir rað- og lotunúmeruð framboð og eftirspurn eru sú lýsing sem skilgreind er af samsetningum þeirra og hvernig vörurakning er sett upp fyrir vörurnar.  

Á móti kemur áætlunarkerfið tillit til framboðs sem er með rað- og lotunúmer sem ósveigjanlegt. Kerfið eykur ekki eða endurtímasetur slíkar framboðspantanir. Undantekningin frá þessu er ef þau eru notuð í tengslum við pöntun eftir pöntun. Nánari upplýsingar um [pöntunartengla eru aldrei rofnar](#order-to-order-links-are-never-broken). Þessi undantekning ver að birgðir berist fyrir nokkrum, hugsanlega árekstrum, aðgerðaboðum þegar það er með misjöfn eigindir. Til dæmis gætu mismunandi eigindir verið þegar framboðið er með safn mismunandi raðnúmera.  

Önnur ástæða fyrir því að rað- og lotunúmeruð framboð eru ósveigjanleg er vegna þess að rað- og lotunúmerum er oft úthlutað seint í ferlinu. Það gæti verið ruglingslegt ef breytingar eru lagðar til á þeim tímapunkti.  

Mótjöfnun rað- og lotunúmers virðir ekki regluna um að áætla ekki neitt fyrir upphafsdagsetningu áætlunarinnar. Ef framboð og eftirspurn eru ekki samstillt mun áætlunarkerfið leggja til breytingar eða nýjar pantanir, óháð upphafsdagsetningu áætlunarinnar.  

### Tenglar fyrir pöntun eru aldrei rofnir

Þegar vara sem er áætluð eftir pöntun er áætluð má aðeins nota tengda framboðið fyrir það sem hún var upphaflega ætluð. Tengda eftirspurnin ætti ekki að ná yfir annað framboð, jafnvel þó að birgðir séu tiltækar í tíma og magni. Til dæmis er ekki hægt að nota samsetningarpöntun sem er tengd sölupöntun í samsetningartilviki til að ná yfir aðra eftirspurn.  

Framboð og eftirspurn eftir pöntunum þarf að jafna nákvæmlega. Áætlunarkerfið tryggir birgðir án þess að breyta pöntunum, breytum og magni í birgðum (öðru en magni sem tengist tengdum pöntunum). Af sömu ástæðu stingur kerfið upp á að minnka umframframboð ef tengda eftirspurnin er minnkjuð.  

Þessi jöfnun hefur einnig áhrif á tímann. Takmarkaði sjóndeildarhringurinn sem ákvarðast af tímarammanum er ekki virtur; framboð verður enduráætlað ef tímasetning eftirspurnar hefur breyst. Hins vegar verður hömlutími virtur og kemur í veg fyrir að pöntun-í-pöntun birgðir séu áætlaðar út, nema innri birgðir úr framleiðslupöntun á mörgum stigum (verkefnispöntun).  

> [!NOTE]  
> Einnig er hægt að tilgreina rað- og lotunúmer á eftirspurn eftir pöntun. Í því tilviki er framboðið ekki ósveigjanlegt, sem er venjulega fyrir rað- og lotunúmer. Í þessu tilfelli hækkar kerfið eða minnkar í samræmi við breytingar á eftirspurn. Ef ein eftirspurn er með misjöfn rað- og lotunúmer, t.d. fleiri en eitt lotunúmer, verður ein framboðspöntun lögð til fyrir hverja lotu.  

> [!NOTE]  
> Spár ættu ekki að leiða til þess að stofnaðar séu nýjar birgðapantanir sem eru bundnar af pöntun-í-pöntun tengslum. Ef spáin er notuð ætti aðeins að nota hana til að mynda háða eftirspurn í framleiðsluumhverfi.

### Íhlutaþörf er hlaðin samkvæmt breytingum á framleiðslupöntunum

Við meðhöndlun framleiðslupantana verður  áætlanakerfið að fylgjast með nauðsynlegum íhlutum áður en þeim er hlaðið í eftirspurnarforstillinguna. Íhlutalínur sem verða til vegna breyttrar framleiðslupöntunar koma í stað lína upphaflegu pöntunarinnar. Breytingin tryggir að áætlunarkerfið tvítekur ekki áætlunarlínur fyrir íhlutaþörf.  

### Nota öryggisbirgðir

Magn í öryggisbirgðum er eftirspurn sem er hlaðin inn í birgðaforstillinguna á upphafsdagsetningu áætlunarinnar.  

Öryggisbirgðir er magn birgða sem er til hliðsjónar til að mæta óvissu í eftirspurn meðan á áfyllingu stendur. Hins vegar er hægt að nota hana til að uppfylla eftirspurn. Í því tilviki tryggir áætlunarkerfið að skipt sé um öryggisbirgðir á fljótlegan hátt. Kerfið leggur til framboðspöntun til að fylla á magn öryggisbirgða á þeim degi sem það er notað. Áætlunarlínan birtir viðvörunartákn fyrir frávik sem útskýrir að öryggisbirgðir hafi verið notaðar að hluta eða að fullu í frávikspöntun fyrir magn sem vantar.  

### Dregið er úr eftirspurn spár með sölupöntunum

Eftirspurnarspá tjáir áætlaða framtíðareftirspurn. Þegar rauneftirspurn er slegin inn, yfirleitt sem sölupantanir fyrir framleiddar vörur, notar hún spána.

Ekki er dregið úr spánni sjálfri með sölupöntunum. Hins vegar er dregið úr magni spár sem notaðar eru við áætlunarútreikninga sem dregið er úr magni sölupöntunar áður en eftirstöðvarnar eru færðar inn í eftirspurnarforstillinguna. Í sölu á tímabili felst áætlun bæði í opnum sölupöntunum og birgðafærslum úr afhentri sölu. Undantekningin frá þessari reglu er þegar hún kemur úr standandi pöntun.  

Tilgreina verður gilda spártímabilið. Dagsetningin á áætlaðrar magni skilgreinir upphaf tímabilsins, og dagurinn í næstu spá skilgreinir lok tímabilsins.  

Spáin fyrir tímabil þar til áætlunartímabilið er ekki notað, óháð því hvort það var notað. Fyrsta spáin með vöxtum er annaðhvort upphafsdagsetning áætlunarinnar eða lokadagsetningin.  

Spáin getur verið fyrir mismunandi eftirspurnartegundir:

* Sjálfstæð eftirspurn, t.d. sölupantanir
* Ósjálfstæð eftirspurn, t.d. framleiðslupöntunaríhlutir.

Vara getur haft báðar gerðir spár. Notkun gerist sérstaklega við áætlun, fyrst fyrir sjálfstæða eftirspurn og síðan fyrir ósjálfstæða eftirspurn.  

### Dregið er úr eftirspurn standandi pöntunar í sölupöntunum

Spá er viðbót við standandi sölupantanir sem leið til að tilgreina framtíðareftirspurn frá tilteknum viðskiptamanni. Eins og í (ótilgreindri) spá ætti raunveruleg sala að nota áætlaða eftirspurn og eftirstandandi magn ætti að færa inn birgðaforstillingu eftirspurnar. Notkun dregur ekki úr magni standandi pöntunar.

Áætlunarútreikningurinn felur í sér opnar sölupantanir sem tengjast tiltekinni línu standandi pöntunar, en hann er ekki með neinu gildu tímabili. Einnig eru ekki bókaðar pantanir þar sem bókunarferlið hefur þegar dregið úr útistandandi magni standandi pöntunar.

## Forgangsraða pöntunum

Innan tiltekinnar birgðahaldseiningar sýnir umbeðin dagsetning eða tiltæk dagsetning mestan forgang. Eftirspurnin í dag ætti að lúta fyrir eftirspurn næstu viku. En til viðbótar þessum heildarforgangi gerir áætlunarkerfið eftirfarandi tillögur í samræmi við forgangsröðun pöntuna:

* Hvaða tegund eftirspurnar á að uppfylla fyrst.
* Hvaða uppruna framboðs á að nota áður en aðrir aðilar framboðs eru notaðir.  

Hlaðið framboð og eftirspurn stuðla að forstillingu á áætluðum birgðum samkvæmt forgangsröðun.  

### Forgangur eftirspurnarhliðarinnar  

1. Þegar afhent: birgðafærsla  
2. Vöruskilapöntun innkaupa  
3. Sölupöntun  
4. Þjónustupöntun  
5. Þarfir framleiðsluíhlutar  
6. Samsetningarpöntunarlína  
7. Flutningspantanir á útleið.  
8. Standandi pöntun (sem ekki hefur þegar verið notuð af tengdum sölupöntunum)  
9. Spá (sem hefur ekki þegar verið notuð í annarri sölupöntun)  

> [!NOTE]  
> Innkaupaskil koma yfirleitt ekki við í framboðsáætlun; Þær ætti alltaf að taka frá úr lotunni sem verður skilað. Ef ekki er tekið frá gegna innkaupaskil hlutverki í framboði og þeim er mjög forgangsraðað til að forðast það að áætlunarkerfið leggi til framboðspöntun eingöngu til að þjónusta innkaupaskil.  

### Forgangur framboðs  

1. Þegar í birgðum: birgðafærsla (sveigjanleiki áætlunar = enginn)  
2. Vöruskilapöntun sölu (Sveigjanleiki áætlunar = Ekkert)  
3. Flutningspöntun á innleið  
4. Framleiðslupöntun  
5. Samsetningarpöntun  
6. Innkaupapöntun  

### Forgangur tengdur framboði og eftirspurn  

Auk forgangsraðar frá gerð framboðs og eftirspurnar eru aðrir hlutir sem hafa áhrif á sveigjanleika áætlunar. Til dæmis vöruhúsaaðgerðir og staða eftirfarandi pantana:

* Sölur
* Innkaup
* Flutningur
* Samsetning
* Framleiðsla

Staða þessara pantana hefur eftirfarandi áhrif: 

1. Að hluta meðhöndlað (Sveigjanleiki áætlunar = Enginn)  
2. Þegar í vinnslu í vöruhúsi (sveigjanleiki áætlunar = enginn)  
3. Útgefið - allar pantanategundir (áætlunarsveigjanleiki = ótakmarkað)  
4. Fastáætluð framleiðslupöntun (sveigjanleiki áætlunar = ótakmarkaður)  
5. Áætlað/opið – allar pantanagerðir (Sveigjanleiki áætlunar = Ótakmarkaður)

## Jöfnun framboðs og eftirspurnar

Áætlunarkerfið stemmir af framboð og eftirspurn með því að leggja til aðgerðir til að endurskoða framboðspantanir sem ekki eru jafnaðar. Þessi staða gerist fyrir hverja samsetningu afbrigðis og birgðageymslu.  

Ímyndið ykkur að hver birgðaregla innihaldi tvo strengi:

* Strengur eftirspurnarviðburða, raðað eftir dagsetningu og forgangi
* Samsvarandi strengur birgðaviðburða

Hver atburður vísar til upprunagerðar og kennis. Reglurnar um mótun vörunnar eru einfaldar. Samsvörun framboðs og eftirspurnar getur komið fram hvenær sem er í ferlinu, á eftirfarandi hátt:  

1. Ekker framboð eða eftirspurn fyrir vöruna => áætluninni er lokið (eða hún á ekki að hefjast).  
2. Eftirspurn er til en ekkert framboð => framboð ætti að leggja til.  
3. Framboð er til en engin eftirspurn er eftir því =hætt ætti við framboð >.  
4. Bæði framboð og eftirspurn er til => spurningum ætti að spyrja og svara áður en [!INCLUDE [prod_short](includes/prod_short.md)] hægt er að tryggja að framboðið geti uppfyllt eftirspurnina.

    Ef tímasetning framboðsins hentar ekki er hægt að enduráætla framboðið, eins og hér segir:  

    1. Ef framboðið er sett fyrr en eftirspurnin er hægt að áætla framboðið þannig að birgðir séu eins lágar og mögulegt er.  
    2. Ef framboðið er seinna en eftirspurnin er hægt að tímasetja framboðið. Annars leggur kerfið til nýtt framboð.  
    3. Ef framboðið uppfyllir eftirspurnina á dagsetningunni getur áætlunarkerfið kannað hvort magn framboðsins nær yfir eftirspurnina.  

    Þegar tímasetningin er til staðar er hægt að reikna magn til framboðs á eftirfarandi hátt:  

    1. Ef framboðsmagnið er lægra en eftirspurnin er hægt að auka framboðsmagnið (eða ekki, ef til er regla um hámarksmagn).  
    2. Ef framboðsmagnið er meira en eftirspurnin er hægt að minnka framboðsmagnið (eða ekki, ef um lágmarksmagnsreglu er að ræða).  

    Á þessum tímapunkti er önnur af þessum tveimur aðstæðum til:  

    1. Núverandi eftirspurn er hægt að ná yfir, og þar af leiðandi hægt að loka og áætlanagerð fyrir næsta eftirspurn getur byrjað.  
    2. Birgðir hafa náð hámarksgildi svo eitthvert eftirspurnarmagn er óvarið. Í þessu tilviki er áætlanakerfi getur lokað núverandi framboð og halda áfram í næsta.  

 Ferlið byrjar allt á næstu eftirspurn og núverandi framboði eða öfugt. Núverandi framboð gæti náð yfir þessa eftirspurn líka eða núverandi eftirspurn hefur ekki enn verið að fullu tryggðir.  

### Reglur um aðgerðir fyrir framboðsviðburði

Efst-niður útreikningar þar sem framboð verður að uppfylla eftirspurn er eftirspurnin tekin sem gefin. Hún er utan stjórnunar áætlunarkerfisins. Hins vegar getur áætlunarkerfið stjórnað framboðshliðinni og gert eftirfarandi tillögur:

* Stofna nýjar framboðspantanir
* Endurtímasetja fyrirliggjandi pantanir eða breyta magni þeirra
* Afturkalla framboðspantanir sem ekki er lengur þörf á  

Til að útiloka framboðspöntun frá áætlunartillögunum er hægt að taka fram að hún hafi engan sveigjanleika í áætlun (Sveigjanleiki áætlunar = Enginn). Þá er umframframboð úr þeirri pöntun notað fyrir eftirspurn, án þess að stungið sé upp á neinni aðgerð. 

Almennt hefur öll framboð áætlunarsveigjanleika sem takmarkast af skilyrðum hverrar aðgerðar sem lögð er til.  

* **Endurtímasetja út**: Dagsetning núverandi framboðspöntunar er hægt að Endurtímasetja út til að mæta skiladegi, nema

  * Taflan táknar birgðir (alltaf á degi núll).  
  * Það er með pöntun fyrir pöntun tengda við aðra eftirspurn.  
  * Það er fyrir utan gluggann til að endurtímasetja í tímarammann.
  * Það er nær framboð sem hægt er að nota.  
  * Á hinn bóginn kann notandinn að ákveða að enduráætla ekki vegna þess að:
  * Framboðspöntunin er bundin við aðra eftirspurn á fyrri degi.  
  * Nauðsynleg endurtímasetning er svo í lágmarki hún er hverfandi.  

* **Endurtímasetja í**: Hægt er að áætla dagsetningu fyrirliggjandi framboðspöntunar, nema samkvæmt eftirfarandi skilyrðum:

  * Hún er tengd beint við aðra eftirspurn.  
  * Hann er fyrir utan gluggann fyrir endurtímasetningu sem skilgreind er af tímarammanni.

> [!NOTE]  
> Þegar vara er áætluð með endurpöntunarmarki er hægt að endurtímasetja framboðspöntunina. Þetta gerist oft í framvirkum framboðspöntunum sem settar eru af stað með endurpöntunarmarki.

* **Auka magn**: Magn núverandi framboðspöntunar má auka til að mæta eftirspurn nema framboð þess er tengt beint við eftirspurn með Pöntun fyrir pöntun tengil.  

> [!NOTE]  
> Þótt hægt sé að auka framboðspöntunina gæti aukningin verið takmörkuð vegna skilgreinds hámarksmagns pöntunar.  

* **Minnka Magn**: Núverandi birgðapöntun með afgang miðað við núverandi eftirspurn getur lækkað til að mæta eftirspurn.  

> [!NOTE]  
> Þó svo að hægt sé að minnka magnið gæti verið umframmagn borið saman við eftirspurnina vegna skilgreinds lágmarksmagns pöntunar eða fjöldapanta. 

* **Hætta við**: Sem sérstakt tilvik af aðgerðinni minnka magn er hægt að hætta við framboðspöntun ef hún hefur verið minnkuð í núll. 
* **Nýtt: Ef engar** framboðspantanir eru til staðar eða fyrirliggjandi pöntun er ekki hægt að breyta til að uppfylla það magn sem þarf á skiladegi eftirspurnarinnar er lögð til ný framboðspöntun.  

### Ákvarða framboðsmagn  

Áætlunarfæribreyturnar sem stýra magninu sem lagt er til í hverri framboðspöntun eru skilgreindar.  

Þegar áætlunarkerfið reiknar magn nýrrar framboðspöntunar eða magn til að breytast á fyrirliggjandi pöntun gæti magnið sem lagt er til verið annað en raunveruleg eftirspurn.  

Ef hámarksbirgðir eða fast pöntunarmagn eru valin er hægt að hækka magnið sem lagt er til að uppfylla fasta magnið eða hámarksbirgðirnar. Ef endurpöntunarstefna notar endurpöntunarmark er hægt að auka magnið að minnsta kosti til að ná endurpöntunarmarkinu. 

Magninu sem lagt er til gæti verið breytt í þessari röð:  

1. Niður að hámarksmagni pöntunar.  
2. Upp að lágmarksmagni pöntunar.  
3. Upp til að mæta næsta margfeldi pöntunar.

### Rakningartenglar pantana við áætlun  

Fyrir pöntunarrakningu við áætlun endurraða áætlunarkerfið pöntunarrakningartenglum fyrir samsetningar á vörum, afbrigðum og birgðageymslum. Kerfið endurraðar rakningartenglum af eftirfarandi ástæðum:

* Til að staðfesta tillögur sínar um alla eftirspurn og tryggja að þörf sé á öllum framboðspöntunum.  
* Endurjafna þarf pöntunarrakningartenglana reglulega.  

Með tímanum verða pöntunarrakningartenglar úr jafnvægi. Tenglarnir verða óstöðugir vegna þess að pöntunarrakningarnetið er ekki endurraðað fyrr en eftirspurn eða framboðstilviki er lokað.

Áður en framboð er jafnað eftir eftirspurn eyðir áætlunarkerfið öllum pantanarakningartenglum. Þegar eftirspurn eða framboðstilviki er lokað stofnar það nýjar rakningartengingar pöntunar milli framboðs og eftirspurnar þegar eftirspurn eða framboðstilviki er lokað.  

> [!NOTE]  
> Jafnvel þótt varan sé ekki sett upp fyrir kvika rakningu pöntunar býr áætlunarkerfið til samhæfða rakningartengla pöntunar.

## Loka jafnað framboði og eftirspurn

Jöfnun framboðs hefur þrjár mögulegar niðurstöður:

* Tilskildu magni og dagsetningu eftirspurnarviðburða er mætt og hægt er að loka áætlun fyrir þá. Framboðsviðburðurinn verður opinn og gæti náð yfir næstu eftirspurn. Ef framboðsviðburðurinn er opinn hefst jöfnunarferlið með núverandi framboðsviðburði og næstu eftirspurn.  
* Ekki er hægt að breyta framboðspöntuninni til að standa undir allri eftirspurninni. Eftirspurnarvikið er enn opið með ósjálfstætt magn sem gæti fjallað um næsta framboðsviðburð. Þess vegna er núverandi framboðsviðburði lokað og jöfnun getur hafist upp á nýtt með núverandi eftirspurn og næsta framboðsviki.  
* Fjallað er um alla eftirspurnina og ekki er um næstu eftirspurn að ræða (eða engin eftirspurn var nein). Umframmagn gæti verið minnkað (eða hætt við) og svo lokað. Einnig ætti að hætta við aðra framboðsviðburði.  

Að lokum stofnar áætlunarkerfið rakningartengil pöntunar milli framboðs og eftirspurnar.  

### Stofna áætlunarlínuna (Aðgerð tillaga)  

 **Ef ný,Breyta** **magni**, **Endurtímasetja**, **Endurtímasetja og Breyta magni** eða **Hætta við** er lögð til að endurskoða framboðspöntunina stofnar áætlunarlína á áætlunarvinnublaðinu. Fyrir pöntunarrakningu er áætlunarlínan ekki aðeins stofnuð þegar birgðatilvikinu er lokað heldur einnig ef eftirspurnartilvikinu er lokað. Þetta á við jafnvel þótt framboðsviðburðurinn sé enn opinn og gæti breyst þegar næsta eftirspurnarvik er unnið. Áætlunarlínunni kann að breytast aftur þegar hún er stofnuð.

Til að minnka álagið á gagnagrunninum þegar unnið er með framleiðslupantanir er hægt að viðhalda áætlunarlínunni á þremur stigum:

* Stofna aðeins áætlanagerðarlínu með núverandi gjalddagadagsetningu og magni en án vegvísun og íhlutum.  
* Taka leið með: áætluðu leiðina felur í sér útreikning á upphafs- og lokadagsetningum og tímasetningum. Taka leið með er eftirspurn eftir aðgangi að gagnagrunni. Ef ákvarða á loka- og skiladagsetningar getur verið nauðsynlegt að reikna leiðina jafnvel þótt birgðavikinu hafi ekki verið lokað. Ef til dæmis er verið að gera framvirka tímasetningu.  
* Taka með niðurbrot uppskriftar: það getur gerst rétt áður en birgðatilvikinu er lokað.

## Sjá einnig  

[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)  
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]