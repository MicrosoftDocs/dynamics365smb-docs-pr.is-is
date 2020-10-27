---
title: Hönnunarupplýsingar - Afstemming eftirspurnar og framboðs | Microsoft Docs
description: Til að skilja hvernig áætlanakerfi virkar, það er nauðsynlegt að skilja forgangsraðað markmið áætlanakerfisins, mikilvægasta sem eru að tryggja að allri eftirspurn verðið svarað með nægu framboði og að allt framboð þjóni tilgangi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 30c78ba04d58a2e2c2227ec638724c85cb1236c7
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917552"
---
# <a name="design-details-balancing-demand-and-supply"></a>Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs
Til að skilja hvernig áætlanakerfi virkar, það er nauðsynlegt að skilja forgangsraðað markmið áætlanakerfisins, mikilvægasta sem eru að tryggja að:  

- Allri eftirspurn verður sinnt með nægu framboði.  
- Allt framboð þjónar tilgangi.  

 Almennt séð, er þessum markmiðum náð með því að jafna framboð við eftirspurn.  

## <a name="demand-and-supply"></a>Eftirspurn og Framboð
 Eftirspurn er algeng orð notuð fyrir hvers konar vergri eftirspurn, svo sem sölupöntun og íhluti þarft frá framleiðslu röð. Að auki leyfir forritið tæknilegri tegundir af eftirspurn, svo sem neikvæðar birgðir og innkaupaskil.  

  Framboð er það orð sem er mest notað fyrir hvaða tegund af jákvæðu eða innleiðarmagni sem er, eins og birgðir, innkaup, samsetning, framleiðsla eða millifærslu á innleið. Að auki geta söluvöruskil aftur getur einnig táknað framboð.  

  Til að raða út margar uppsprettur eftirspurn og framboð, áætlanakerfi skipuleggur þær á tvær tíma línur sem kallast birgðaforstillingar. Ein forstilling inniheldur eftirspurnartilvik og önnur inniheldur samsvarandi framboðstilvik. Hver atburður táknar eina pöntunarnetsfærslu, t.d. sölulínu, birgðafærslu, eða framleiðslupöntunarlínu.  

  Þegar birgðaforstillingar eru sóttar eru mismunandi eftirspurn-framboð söfn jöfnuð til að skila framboðsáætlun sem uppfyllir listuð markmið.  

  Áætlunarfæribreytur og birgðastig eru aðrar gerðir eftirspurnar og framboðs, sem fara í gegnum samþætta jöfnun til að fylla á birgðavörur. Nánari upplýsingar eru í [Upplýsingar um hönnun: Afgreiðsla endurpöntunarstefna](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Hugmyndin um Jafnvægi í hnotskurn
  Eftirspurn er gefin af viðskiptavinum fyrirtækisins. Framboð er það sem fyrirtækið getur búið til og fjarlægy til að koma á jafnvægi. Áætlanakerfið byrjar á óháðri eftirspurn og rekur sig svo aftur að framboðinu.  

   Forstillingar birgða eru notaðar til að taka upplýsingar um eftirspurn og búnað, magn og tímastillingu. Þessar forstillingar mynda tvær hliðar afstemmingarskalans.  

   Markmiðið með tihögun áætlanagerðarinnar er að mynda andvægi í eftirspurn og framboði vöru til að tryggja að eftirspurnin samsvari framboðinu á gerlegan hátt, eins og skilgreind er með áætlunarfæribreytum og -reglum.  

   ![Yfirlit yfir framboð og eftirspurn jafnvægi](media/nav_app_supply_planning_2_balancing.png "Yfirlit yfir framboð og eftirspurn jafnvægi")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Takast á við pantanir fyrir upphafsdag áætlanagerðar
Til að forðast að framboðsáætlun sýnir ómögulegt og því gagnslaus tillögur, vinnur áætlanakerfið tímabilið allt til áætlanagerðarupphafsdags sem fryst svæði þar sem ekkert er áætlað fyrir. Eftirfarandi regla gildir um fryst svæði:  

Allt framboð og eftirspurn fyrir upphafsdagsetningu áætlunartímabilsins verður talin hluti af birgðum eða afhent.  

Í samræmi mun áætlanakerfið ekki, með nokkrum undantekningum, stinga upp á breytingum á framboðspöntunum á frystu svæði og engir pöntunarrakningartenglar eru stofnaðir eða viðhaldið fyrir það tímabil.  

Undantekningar frá þessari reglu eru sem hér segir:  

   * Ef áætlaðar tiltækar birgðir, þar með talin summa framboðs og eftirspurnar á frysta svæðinu, eru undir núlli.  
   * Ef raðnúmer/lotunúmer þarf á bakfærða pöntun/pantanir.  
   * Ef samstæðan framboð-eftirspurn er tengd með pöntun-fyrir-pöntun stefnu.  

Ef fyrstu tiltæku birgðir eru undir núlli leggur áætlanakerfið til neyðarbirgðapöntun daginn fyrir áætlunartímabilið til að ná yfir magnið sem vantar. Þar af leiðandi verða áætlaðar og tiltækar birgðir alltaf minnst núll þegar áætlun fyrir komandi tímabil hefst. Áætlunarlína fyrir þessa birgðapöntun birtir viðvörunartákn og viðbótarupplýsingar birtast við uppflettingu.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Rað/Lotunúmer og pöntun fyrir pöntun tenglar eru undanþegin frosna reiturum  
   Ef raðnúmer/lotunúmer þarf eða pöntun-í-pöntun tengill er til staðar hunsar áætlanakerfið frysta svæðið og skráir magn sem er bakfært frá upphafsdegi og leggur mögulega til aðgerðir til úrbóta ef framboð og eftirspurn eru ekki samstillt. Viðskiptaástæðan fyrir þessari stefnu er að slík sérstök pör eftirspurnar og framboðs verða að passa til að tryggja að þessi tiltekna eftirspurn sé uppfyllt.

## <a name="loading-the-inventory-profiles"></a>Hleðsla birgðaforstillinga
Til að raða út margar uppsprettur eftirspurn og framboð, áætlanagerð kerfi skipuleggur þá á tveggja tíma línur kallast skrá snið.  

Venjulegar gerðir eftirspurnar og framboðs ásamt gjalddögum á eða eftir ætlaða upphafsdagsetningu eru hlaðið inn í hverja birgðaforstillingu. Þegar hlaðið er mismunandi eftirspurn og framboð tegundir raðað í samræmi við heildarforgangsröðun, svo sem skiladaga, lágstigskóða, staðsetningu og afbrigði. Að auki er pantanaforgangsröðun beitt við mismunandi gerðir til þess að tryggja að mikilvægasta krafa er uppfyllt fyrst. Frekari upplýsingar eru í [Forgangsröðun pantana](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Eins og fyrr segir getur eftirspurn einnig verði neikvæð. Þetta þýðir að það ætti að meðhöndla sem framboð; Hins vegar, ólíkt eðlilegri gerðir af framboði, er neikvæð eftirspurn talin föst eftirspurn. Áætlanakerfið getur tekið það til greina en mun ekki leggja til neinar breytingar á því.  

Almennt séð, áætlanagerðarkerfi telur allar framboðspantanir eftir áætlunarupphafsdegi sem breytingum háð í því skyni að anna eftirspurn. Hins vegar, um leið og magn er bókað frá birgðapöntun er ekki lengur hægt að breyta því úr áætlanakerfinu. Í samræmi er ekki hægt að enduráætla eftirfarandi mismunandi pantanir:  

- Útgefnar framleiðslupantanir sem eru notkun og frálag er bókað á.  
- Samsetningarpantanir þar sem búið er að bóka notkun eða frálag.  
- Millifærslupantanir þar afhending hefur verið bókuð.  
- Innkaupapantanir þar sem búið er að bóka móttöku.  

Burtséð frá hleðslu eftirspurnar- og framboðsgerða er tilteknum gerðum hlaðið með sérstakri áherslu á sérstakar reglur og tengsl sem lýst er í eftirfarandi.  

### <a name="item-dimensions-are-separated"></a>Vöruvíddir eru aðskildar.  
Reikna verður út birgðaáætlunina út frá samsetningu vöruvídda, s.s. afbrigðis og staðsetningu. Hins vegar er engin ástæða til að reikna út fræðilega samsetningu. Aðeins þarf að reikna þær samsetningar sem bera eftirspurn og/eða framboð.  

Áætlanakerfið stjórnar þessu með því að fara yfir alla forstillingu birgða. Þegar ný samsetning er fundin skapar forritið innra eftirlitsskrá sem geymir raunveruleg samsetningarupplýsingar. Forritið setur birgðahaldseininguna inn sem stjórnunarfærslu eða sem ytri snigil. Niðurstaðan er að réttar áætlunarfæribreytur samkvæmt samsetningu afbrigðis og birgðageymslu eru valdar og forritið getur haldið áfram að innri lykkju.  

> [!NOTE]  
>  Forritið krefst þess ekki að notandi færi inn birgðahaldseiningarfærslu þegar færð er inn eftirspurn og/eða framboð fyrir tiltekna samsetningu afbrigðis og staðsetningar. Ef birgðahaldseining er ekki til fyrir tiltekna samsetningu stofnar forritið því tímabundna birgðahaldseiningarfærslu byggða á gögnum birgðaspjaldsins. Ef Birgðageymsla áskilin er stillt á Já á síðunni Birgðagrunnur verður annaðhvort að stofna birgðahaldseiningu eða stilla Íhlutir á staðnum á Já. Frekari upplýsingar, sjá [Hönnunarupplýsingar: Eftirspurn í autt birgðageymsla](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Raðnúmer-lotunúmer eru hlaðinn með lýsingarstigi  
Eigindum í formi rað-/lotunúmers er hlaðið inn í birgðasnið ásamt eftirspurn og framboði sem þau eru úthlutuð á.  

Eigindir eftirspurnar og framboðs er raðað skv. forgangi pantana sem og eftir forsktirtarstigi þeirra. Vegna niðurstöðu rað- / lotunúmera endurspegla forskriftarstig, nákvæmari eftirspurn, svo sem lotunúmer valið sérstaklega fyrir sölulínu, mun leita að samsvörun fyrir minna takmarkaða eftirspurn, svo sem sölu frá hvaða lotunúmer sem er valið.  

> [!NOTE]  
>  Engar forgangsreglur eru fyrir framboð og eftirspurn rað-/lotunúmera, annað en tilgreint stig sem er ákvarðað með samsetningu rað- og lotunúmer og uppsetningu vörurakningar fyrir viðkomandi vörur.  

Við jöfnun les áætlanakerfið framboð með rað- og lotunúmerum sem fast og reynir ekki að auka eða enduráætla svoleiðis birgðapantanir (nema þær séu notaðar í vinnslur milli pantana). Sjá Pöntun fyrir pöntun tenglar eru aldrei rofnir). Þetta ver framboð frá móttöku margra, hugsanlega ósamhljóða aðgerðaboða þegar framboð ber mismunandi eiginleika - ss safn af mismunandi raðnúmerum.  

Önnur ástæða fyrir því að rað-/lotunúmerað framboð er ósveigjanlegt er að rað-/lotunúmerum er alla jafna úthlutað það seint í ferlinu að það myndi valda ruglingi að stinga upp á breytingum.  

Staða rað-/lotunúmera er ekki innan *frosna svæðisins* . Ef eftirspurn og framboð er ekki samstillt leggur áætlanakerfið til breytingar eða leggur til nýjar pantanir, óháð upphafsdegi áætlanagerðarinnar.  

### <a name="order-to-order-links-are-never-broken"></a>Tenglar á milli pantana eru aldrei rofnir  
Við áætlun pöntun-í-pöntun vöru má ekki nota tengdu birgðirnar fyrir neina aðra eftirspurn nema þá sem þær voru upphaflega ætlaðar. Tengd eftirspurn ætti ekki að falla undir neitt annað tilviljanakennt framboð, jafnvel þótt það sé tiltækt í tíma og magni við núverandi kringumstæður. Til dæmis er ekki hægt að nota samsetningarpöntun sem tengd er við sölupöntun í aðstæðum þar sem vara er sett saman fyrir pöntun fyrir nokkra aðra eftirspurn.  

Eftirspurn og framboð úr pöntun í pöntun þarf að vera í nákvæmu jafnvægi. Áætlanakerfið tryggir framboð undir öllum kringumstæðum, án þess að taka til greina færibreytur pantanastæðrar, breytingar og magn í birgðum (annað en magn sem varðar tengdar pantanir). Af sömu ástæðu stingur kerfið upp á að minnka umframframboð ef tengda eftirspurnin er minnkjuð.  

Þessi jöfnun hefur einnig áhrif á tímann. Takmarkaði sjóndeildarhringurinn sem ákvarðast af tímarammanum er ekki virtur; framboð verður enduráætlað ef tímasetning eftirspurnar hefur breyst. Hins vegar verður hömlutími virtur og kemur í veg fyrir að pöntun-í-pöntun birgðir séu áætlaðar út, nema innri birgðir úr framleiðslupöntun á mörgum stigum (verkefnispöntun).  

> [!NOTE]  
>  Rað/lotunúmeri getur einnig tilgreint um pöntun fyrir pöntun eftirspurn. Í því tilfelli er framboð ekki talin ósveigjanleg sjálfgefið, eins og er venjulega erum að ræða fyrir raðnúmer / lotunúmeri. Í þessu tilviki, mun kerfið auka/minnka miðað við breytingu á eftirspurn. Enn fremur, ef einni eftirspurn fylgja breytileg raðnúmer/lotunúmer, svo sem fleiri en eitt lotunúmer, verður stungið upp á einni framboðspöntun fyrir hverja lotu.  

> [!NOTE]  
>  Spár ættu ekki að leiða til þess að stofnaðar séu nýjar birgðapantanir sem eru bundnar af pöntun-í-pöntun tengslum. Ef spáin er notuð ætti aðeins að nota hana til að mynda háða eftirspurn í framleiðsluumhverfi.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Íhlutaþörf er hlaðið samkvæmt breytingum á framleiðslupöntun  
Við meðhöndlun framleiðslupantana verður  áætlanakerfið að fylgjast með nauðsynlegum íhlutum áður en þeim er hlaðið í eftirspurnarforstillinguna. Íhlutalínur sem leiða af breyttri framleiðslupöntun koma í stað upprunalegu pöntunarinnar. Þetta tryggir að áætlanakerfið tvítaki aldrei áætlunarlínurnar fyrir íhluti.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Öryggisbirgðir má nota  
Öryggisbirgðamagn er aðallega eftirspurnargerð og þess vegna hlaðið inn í birgðaforstillinguna í upphafsdagsetningu áætlanagerðar.  

Öryggisbirgðir er birgðamagn sett til hliðar til að bæta upp fyrir óvissu í eftirspurn á áfyllingearafhendingartíma. Hins vegar má nota það ef það er nauðsynlegt að taka af því til að svara eftirspurn. Í þessu tilfelli tryggir áætlunarkerfið að öryggisbirgðir séu endurnýjaðar með því að leggja til afhendingarpöntun til þess að fylla á magn öryggisbirgða á þeim degi er þær verða notaðar. Þessi áætlunarlína mun sýna  fráviksviðvöruntákn sem skýrir að öryggisbirgðir hafi verið notaðar að hluta eða að fullu vegna frávikspöntunar fyrir magn sem vantaði.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Spá um eftirspurn er minnkuð eftir sölupöntunum  
Eftirspárspáin lýsir væntanlegri eftirspurn eftir framtíðinni. Þegar rauneftirspurn er slegin inn, yfirleitt sem sölupantanir fyrir framleiddar vörur, notar hún spána.  

Spáin sjálf er í raun ekki minnkuð af sölupöntunum, hún er enn sú sama. Hins vegar er spármagnið sem notað er í útreikningi á áætluninni minnkað (með magni sölupöntunarinnar) áður en magnið sem eftir er, ef eitthvað er, fer í birgðaforstillingu eftirspurnar. Þegar áætlanakerfið kannar raunverulega sölu á einhverju tímabili eru teknar með bæði opnar sölupantanir og birgðahöfuðbókarfærslur úr sendum pöntunum, nema þær séu úr standandi pöntun.  

Notandi þarf að tilgreina gilt spártímabil. Dagsetningin á áætlaðrar magni skilgreinir upphaf tímabilsins, og dagurinn í næstu spá skilgreinir lok tímabilsins.  

Spáin fyrir tímabil fyrir áætlanagerðartímabilið er ekki notuð, án tillits til þess hvort hún var notuð eða ekki. Fyrsta áhugaverða spátala er annaðhvort sá dagur eða næsta dagsetning fyrir upphafsdag áætlunar.  

Spáin getur verið fyrir sjálfstæða eftirspurn, svo sem sölupantanir, eða háð eftirspurn, eins og efnisþætti framleiðslupöntunar (einingaspá). Vara getur haft báðar gerðir spár. Á áætlanagerð, fer neyslu fram fyrir sig, fyrst fyrir sjálfstæða eftirspurn og þá fyrir háða eftirspurn.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Eftirspurn standandi pöntunar er minnkuð eftir sölupöntunum  
Spá er bætt við af standandi sölupöntun í því skyni að tilgreina framtíðareftirspurn frá tilteknum viðskiptamanni. Eins og í (ótilgreindri) spá ætti raunveruleg sala að nota áætlaða eftirspurn og eftirstandandi magn ætti að færa inn birgðaforstillingu eftirspurnar. Eins og áður minnkar notkun ekki raunverulega standandi pöntun.  

Útreikningar áætlanagerðar taka til greina opnar sölupantanir tengdar tilgreindum standandi pöntunum, en tekur ekki til greina nein gild tímabil. Né tekur það tillit til bókaðra pantana þar sem bókunarferlið hefur þegar minnkað útistandandi magn standandi pöntunar.

## <a name="prioritizing-orders"></a>Forgangsröðun pantana
Innan tiltekinnar birgðahaldseiningar, táknar umbeðin eða tiltæk dagsetning hæsta forgang; eftirspurn í dag ætti að mæta áður en eftirspurn næstu viku er mætt. En auk þessarar heildarforgangs, mun áætlanakerfi einnig benda hvaða tegund af eftirspurn ætti að vera uppfyllt áður en önnur er uppfyllt. Eins mun það stinga upp á hvaða uppruna framboðs ætti að jafna áður en aðrar framboðsuppsprettur eru jafnaðar. Þetta er gert í samræmi við forgang pöntunar.  

Hlaðin eftirspurn og framboð hafa áhrif á forstillingu fyrir áætlaðar birgðir samkvæmt eftirfarandi forgangi:  

### <a name="priorities-on-the-demand-side"></a>Forgangur eftirspurnarmegin  
1. Þegar afhent: birgðafærsla  
2. Vöruskilapöntun innkaupa  
3. Sölupöntun  
4. Þjónustupöntun  
5. Framleiðsluíhlutaþörf  
6. Samsetningarpöntunarlína  
7. Flutningspantanir á útleið.  
8. Standandi pöntun (sem hefur ekki þegar verið notuð í annarri sölupöntun)  
9. Spá (sem hefur ekki þegar verið notuð í annarri sölupöntun)  

> [!NOTE]  
>  Innkaupaskil eru yfirleitt ekki notuð í framboðsáætlun. Þau ætti að alltaf að taka úr lotunni sem á að skila. Ef ekki er tekið frá gegna innkaupaskil hlutverki í framboðinu og eru fremst í forgangsröðinni til að komast hjá því að áætlanakerfið leggi til birgðapöntun bara til að þjóna innkaupaskilum.  

### <a name="priorities-on-the-supply-side"></a>Forgangur framboðsmegin  
1. Þegar í birgðum: birgðafærsla (sveigjanleiki áætlunar = enginn)  
2. Söluskilapöntun (sveigjanleiki í áætlun = enginn)  
3. Flutningspöntun á innleið  
4. Framleiðslupöntun  
5. Samsetningarpöntun  
6. Innkaupapöntun  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Forgangur sem tengist stöðu eftirspurnar og framboðs  
Burtséð frá forgangi sem fylgir gerð eftirspurnar og framboðs skilgreinir núverandi staða pantana í vinnsluferlinu einnig forgang. Til dæmis hafa vöruhúsaaðgerðir áhrif og staða sölu, innkaupa, flutnings, samsetningar og framleiðslupantana er tekin með í reikninginn:  

1. Að hluta meðhöndlað (Sveigjanleiki áætlunar = Enginn)  
2. Þegar í vinnslu í vöruhúsi (sveigjanleiki áætlunar = enginn)  
3. Útgefið - allar pantanategundir (áætlunarsveigjanleiki = ótakmarkað)  
4. Fastáætluð framleiðslupöntun (sveigjanleiki áætlunar = ótakmarkaður)  
5. Áætlað/opið – allar pantanagerðir (Sveigjanleiki áætlunar = Ótakmarkaður)

## <a name="balancing-supply-with-demand"></a>Jöfnun framboðs við eftirspurn
Kjarni áætlanakerfisins felst í jafnvægi á milli eftirspurn og framboð með því að leggja til notandaaðgerðir til að endurskoða framboðspantanir við ójafnvægi. Þetta á sér stað á blöndu af afbrigði og staðsetningu.  

Ímyndaðu þér að hver birgðaforstilling inniheldur eftirspurnartilvika (raðað eftir dagsetningu og forgangi) og samsvarandi streng á framboðstilvikum. Hver atburður vísar aftur til upphaflega gerðar þeirra og auðkennis. Reglur um mótjöfnun vörunnar eru einfaldar. Fjögur tilvik af samsvörun framboðs og eftirspurnar getur komið fram hvenær sem er í ferlinu.  

1. Ekker framboð eða eftirspurn fyrir vöruna => áætluninni er lokið (eða hún á ekki að hefjast).  
2. Eftirspurn er til en ekkert framboð => framboð skal leggja til.  
3. Framboð er til en engin eftirspurn => hætta skal við framboð.  
4. Hvort tveggja eftirspurn og framboð er til => Spurningar skal spyrja og svara áður en hægt er að tryggja að eftirspurn sé mætt og að framboð sé nægt.  

    Ef tímasetning framboðs hentar ekki er kannski hægt að enduráætla framboðið eins og hér segir:  

    1.  Ef framboð er sett á undan eftirspurn er kannski hægt að enduráætla framboðið út svo að birgðirnar séu eins litlar og hægt er.  
    2.  Ef framboð er sett á eftir eftirspurn er kannski hægt að enduráætla framboðið inn. Annars leggur kerfið til nýtt framboð.  
    3.  Ef framboð svarar eftirspurn á þeim degi getur áætlanakerfið haldið áfram að kanna hvort framboðsmagnið svarar eftirspurn.  

    Þegar tímasetning er rétt er hægt að reikna viðeigandi magn sem leggja á til sem hér segir:  

    1.  Ef framboðsmagnið er minna en eftirspurn er mögulegt að hægt sé að auka framboðsmagnið (eða ekki, ef takmarkað af stefnu um hámarksmagn).  
    2.  Ef framboðsmagnið er meira en eftirspurn er mögulegt að hægt sé að minnka framboðsmagnið (eða ekki, ef takmarkað af stefnu um lágmarksmagn).  

    Á þessum tímapunkti er annað hvor af þessum tveimur aðstæðum til:  

    1.  Núverandi eftirspurn er hægt að ná yfir, og þar af leiðandi hægt að loka og áætlanagerð fyrir næsta eftirspurn getur byrjað.  
    2.  Birgðir hafa náð hámarksgildi svo eitthvert eftirspurnarmagn er óvarið. Í þessu tilviki er áætlanakerfi getur lokað núverandi framboð og halda áfram í næsta.  

 Ferlið byrjar upp á nýtt með næstu eftirspurn og núverandi framboði, eða öfugt. Núverandi framboð gæti náð yfir þessa eftirspurn líka eða núverandi eftirspurn hefur ekki enn verið að fullu tryggðir.  

### <a name="rules-concerning-actions-for-supply-events"></a>Reglur um aðgerðir fyrir framboðstilvik  
Þegar áætlanakerfið framkvæmir ofansækinn útreikninga þar sem birgðir verða að mæta eftirspurn er eftirspurnin tekin sem sjálfgefin, þ.e. er ekki undir stjórn áætlanakerfis. Hins vegar er hægt að stjórna framboðshliðinni. Því mun áætlanakerfið stinga upp á að búnar séu til nýjar birgðapantanir, þær sem fyrir liggja séu enduráætlaðar og/eða pöntunarmagni sé breytt. Ef núverandi birgðapöntun verður óþörf leggur áætlanakerfið til að notandinn hætti við hana.  

Ef notandinn vill útiloka núverandi birgðapöntun frá tillögum áætlanagerðar getur hann tekið fram að hún hafi engan sveigjanleika áætlunar (Sveigjanleiki áætlunar = Enginn). Þá er umframframboð úr þeirri pöntun notað fyrir eftirspurn, án þess að stungið sé upp á neinni aðgerð.  

Almennt gildir að allt framboð hefur áætlunarsveigjanleika sem takmarkast af skilyrðum hverrar af leiðbeinandi aðgerðum.  

-   **Endurtímasetja út** : Dagsetning núverandi framboðspöntunar er hægt að Endurtímasetja út til að mæta skiladegi, nema  

    -   Taflan táknar birgðir (alltaf á degi núll).  
    -   Það er með pöntun fyrir pöntun tengda við aðra eftirspurn.  
    -   Hún liggur utan enduráætlunarsíðunnar sem skilgreind er með tímarammanum.  
    -   Hægt er að nota birgðir sem eru nær.  
    -   Á hinn bóginn kann notandinn að ákveða að enduráætla ekki vegna þess að:  
    -   Birgðapöntunin hefur þegar verið tengd við aðra eftirspurn á fyrri dagsetningu  
    -   Nauðsynleg enduráætlunagerð er svo minniháttar að notanda finnst hún óþörf.  

-   **Endurtímasetja inn** : Dagsetning núverandi framboðspöntunar sem er hægt að gera tímaáætlun á, nema í eftirfarandi skilyrðum:  

    -   Það er beintengt við einhverja aðra eftirspurn.  
    -   Hún liggur utan enduráætlunarsíðunnar sem skilgreind er með tímarammanum.  

> [!NOTE]  
>  Við áætlun vöru með endurpöntunarmarki, er alltaf hægt að áætla birgðapöntunina ef nauðsynlegt er. Þetta er algengt í birgðapöntun sem er dagsett í framtíðinni sem eru ræstar af endurpöntunarmarki.  

-   **Auka magn** : Magn núverandi framboðspöntunar má auka til að mæta eftirspurn nema framboð þess er tengt beint við eftirspurn með Pöntun fyrir pöntun tengil.  

> [!NOTE]  
>  Jafnvel þótt hægt sé að auka við birgðapöntunina getur það verið takmarkað vegna skilgreinds hámarks pöntunarmagns.  

-   **Minnka Magn** : Núverandi birgðapöntun með afgang miðað við núverandi eftirspurn getur lækkað til að mæta eftirspurn.  

> [!NOTE]  
>  Jafnvel þótt hægt væri að minnka magnið getur samt verið afgangur miðað við eftirspurnina vegna skilgreinds lágmarks pöntunarmagns við fjöldapantanir.  

-   **Hætta** : Sem sérstök atvik af lækkun magnsaðgerð, er hægt að hætta við birgðapöntun ef það hefur verið lækkað niður í núll.  
-   **Nýtt** : Ef engin framboðspöntun er til staðar eða fyrirliggjandi pöntun er ekki hægt að breyta til að uppfylla nauðsynlegt magn á settum skiladegi er stungið upp á nýrri framboðspöntun.  

### <a name="determining-the-supply-quantity"></a>Ákvarða framboðsmagn  
Áætlunarfæribreytur sem tilgreindar voru af notanda stjórna áætluðu magni fyrir hverja framboðspöntun.  

Þegar áætlanakerfið reiknar út magn fyrir nýja birgðapöntun eða breytingu á magni í fyrirliggjandi pöntun getur magn sem lagt er til verið annað en raunverulegt eftirspurn segir til um.  

Ef hámarksbirgðir eða fast pöntunarmagn er valið er hægt að auka magnið sem lagt er til til að ná þessu fasta magni eða hámarksbirgðum. Ef endurpöntunarstefna notar endurpöntunarmark er hægt að auka magnið að minnsta kosti til að ná endurpöntunarmarkinu.  

 Hægt er að breyta ráðlögðu magni í þessari röð:  

1. Niður að hámarki pöntunarmagns (ef einhverjar).  
2. Upp að lágmarksmagni pöntunar.  
3. Upp til að mæta næsta margfeldi pöntunar. (Ef rangar stillingar eru notaðar er mögulega farið yfir hámarkspöntunarmagn.)  

### <a name="order-tracking-links-during-planning"></a>Pöntunarrakningatenglar í áætlun  
Varðandi pöntunarrakningu við áætlanagerð, það er mikilvægt að nefna að áætlanakerfi endurraðar kvikt stofnuðum pöntunarrakningartenglum fyrir samsetningarnar hlutur/afbrigði / Staðsetningu.  

Það eru tvær ástæður fyrir þessu:  

-   Áætlanakerfið verður að geta réttlætt tillögur sínar, að allri eftirspurn hafi verið svarað og að engar birgðapantanir séu umfram þörf.  
-   Breytilegir pöntunarrakningartengla þarf að endurjafna reglulega.  

Með tímanum myndast ójafnvægi í pöntunarrakningartenglum þar sem pöntunarrakningarnetinu er ekki endurraðað fyrr en eftirspurnar- eða framboðstilvikum er lokað í raun og veru.  

Áður en framboð og eftirspurn er jafnað eyðir forritið öllum pöntunarrakningartenglum. Við afstemmingu, þegar eftirspurn eða framboð er lokað, er nýjum pöntunarrakningartenglum komið á milli framboðs og eftirspurnar.  

> [!NOTE]  
>  Jafnvel þótt vara sé ekki sett upp fyrir kvika pöntunarrakningi býr áætlunarkerfið til jafnaða pöntunarrakningartengla eins og útskýrt er hér að ofan.
## <a name="closing-demand-and-supply"></a>Lokun eftirspurnar og framboðs
Þegar jafnvægisstillingarferli hafa verið framkvæmd eru þrjár hugsanlegar lokaaðstæður:  

* Nauðsynlegt magn og dagsetning eftirspurnartilvika hafa verið uppfyllt þeim er hægt að loka. Birgðatilvikið er enn opið og gæti uppfyllt næstu eftirspurn, svo hægt er að hefja afstemmingu að nýju með núverandi birgðatilviki og næstu eftirspurn.  
* Ekki er hægt að breyta birgðapöntuninni svo hún nái yfir alla eftirspurn. Eftirspurnartilvik er enn opinn, með nokkru óuppfylltu magni sem hugsanlega er uppfyllt í næsta framboðstilviki. Þannig er núverandi framboðstilvik lokað, þannig að jöfnunaraðgerð getur byrjað aftur með núverandi eftirspurn og næsta framboðstilviki.  
* Öll eftirspurn hefur verið uppfyllt, engin eftirspurn stendur eftir (eða eftirspurn var ekki til staðar). Ef það er eitthvert afgangsframboð er hægt að minnka það (eða hætta við) og loka síðan. Hugsanlega eru fleiri framboðstilvik til staðar innar í keðjunni og einnig ætti að hætta við þau.  

Að lokum mun áætlanakerfið stofna pöntunarrakningartengil milli framboðs og eftirspurnar.  

### <a name="creating-the-planning-line-suggested-action"></a>Stiofna áætlunarlínu (Tillögu um aðgerð)  
Ef einhver aðgerð – Ný, Breyta magni, Enduráætla, Enduráætla og breyta magni eða Hætta við – er lögð til til að endurskoða birgðapöntunina býr áætlanakerfið til áætlunarlínu í áætlanavinnublaðinu. Vegna pöntunarrakningar, er áætlunarlína ekki aðeins búin til þegar framboðsatburður er lokaður, en einnig ef eftirspurnaratburði er lokað, jafnvel þótt framboðsatburður er enn opinn og getur verið háð frekari breytingum þegar næsta eftirspurnaratburður er afgreiddur. Þetta þýðir að þegar fyrst búið til er hægt að breyta áætlunarlínu aftur.  

Til að lágmarka gagnagrunnsaðgang við meðhöndlun framleiðslu pantanir, áætlunarlína getur verið haldið í þrjú stig, en stefnt að framkvæma einfaldasta viðhald stig:  

* Stofna aðeins áætlanagerðarlínu með núverandi gjalddagadagsetningu og magni en án vegvísun og íhlutum.  
* Taka með leið: fyrirhuguð leið er sett fram með útreikningur á upphaf og endir dagsetningar og tíma. Þetta fer eftir aðgangi að gagnagrunni. Til að ákvarða endi og skiladag, kann að vera nauðsynlegt að reikna þetta jafnvel ef framboðstilvik hefur ekki verið lokað (ef um er að ræða framvirk tímasetningu).  
* Taka með uppskriftarsprengingu: Þetta getur bíða þangað til rétt áður en framboðstilvik er lokað.  

Þetta lýkur lýsingu á því hvernig eftirspurn og framboð er hlaðið, gefið forgang og jafnað í áætlanakerfinu. Í samþættingu við þessa framboðsáætlunarstarfsemi verður kerfið að tryggja að nauðsynlegt birgðastig hverrar áætlunarvöru sé haldið í samræmi við pöntunarstefnu hennar.

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
 [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
