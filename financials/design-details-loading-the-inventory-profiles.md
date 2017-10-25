---
title: "Hönnunarupplýsingar - Hleðsla birgðaforstillinga | Microsoft Docs"
description: "Til að raða út margar uppsprettur eftirspurn og framboð, áætlanagerð kerfi skipuleggur þá á tveggja tíma línur kallast skrá snið."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 449e6c23e345cddb7a8eacfe97a06174bca47e6e
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-loading-the-inventory-profiles"></a>Hönnunarupplýsingar: hleðsla birgðaforstillinga
Til að raða út margar uppsprettur eftirspurn og framboð, áætlanagerð kerfi skipuleggur þá á tveggja tíma línur kallast skrá snið.  
  
 Venjulegar gerðir eftirspurnar og framboðs ásamt gjalddögum á eða eftir ætlaða upphafsdagsetningu eru hlaðið inn í hverja birgðaforstillingu. Þegar hlaðið er mismunandi eftirspurn og framboð tegundir raðað í samræmi við heildarforgangsröðun, svo sem skiladaga, lágstigskóða, staðsetningu og afbrigði. Að auki er pantanaforgangsröðun beitt við mismunandi gerðir til þess að tryggja að mikilvægasta krafa er uppfyllt fyrst. Nánari upplýsingar eru í [Upplýsingar um hönnun: Forgangsröðun pantana](design-details-prioritizing-orders.md).  
  
 Eins og fyrr segir getur eftirspurn einnig verði neikvæð. Þetta þýðir að það ætti að meðhöndla sem framboð; Hins vegar, ólíkt eðlilegri gerðir af framboði, er neikvæð eftirspurn talin föst eftirspurn. Áætlanakerfið getur tekið það til greina en mun ekki leggja til neinar breytingar á því.  
  
 Almennt séð, áætlanagerðarkerfi telur allar framboðspantanir eftir áætlunarupphafsdegi sem breytingum háð í því skyni að anna eftirspurn. Hins vegar, um leið og magn er bókað frá birgðapöntun er ekki lengur hægt að breyta því úr áætlanakerfinu. Í samræmi er ekki hægt að enduráætla eftirfarandi mismunandi pantanir:  
  
-   Útgefnar framleiðslupantanir sem eru notkun og frálag er bókað á.  
  
-   Samsetningarpantanir þar sem búið er að bóka notkun eða frálag.  
  
-   Millifærslupantanir þar afhending hefur verið bókuð.  
  
-   Innkaupapantanir þar sem búið er að bóka móttöku.  
  
 Burtséð frá hleðslu eftirspurnar- og framboðsgerða er tilteknum gerðum hlaðið með sérstakri áherslu á sérstakar reglur og tengsl sem lýst er í eftirfarandi.  
  
## <a name="item-dimensions-are-separated"></a>Vöruvíddir eru aðskildar.  
 Reikna verður út birgðaáætlunina út frá samsetningu vöruvídda, s.s. afbrigðis og staðsetningu. Hins vegar er engin ástæða til að reikna út fræðilega samsetningu. Aðeins þarf að reikna þær samsetningar sem bera eftirspurn og/eða framboð.  
  
 Áætlanakerfið stjórnar þessu með því að fara yfir alla forstillingu birgða. Þegar ný samsetning er fundin skapar kerfið innra eftirlitsskrá sem geymir raunveruleg samsetningarupplýsingar. Forritið setur birgðahaldseininguna inn sem stjórnunarfærslu eða sem ytri snigil. Niðurstaðan er að réttar áætlunarfæribreytur samkvæmt samsetningu afbrigðis og birgðageymslu eru valdar og forritið getur haldið áfram að innri lykkju.  
  
> [!NOTE]  
>  Forritið krefst þess ekki að notandi færi inn birgðahaldseiningarfærslu þegar færð er inn eftirspurn og/eða framboð fyrir tiltekna samsetningu afbrigðis og staðsetningar. Því, ef birgðahaldseining er ekki til fyrir tiltekna samsetningu, stofnar forritið tímabundna birgðahaldseiningarfærslu byggða á gögnum birgðaspjaldsins. Ef Birgðageymsla áskilin er stillt á Já í glugganum Birgðagrunnur verður annaðhvort að stofna birgðahaldseiningu eða stilla Íhlutir á staðnum á Já. Frekari upplýsingar, sjá [Hönnunarupplýsingar: Eftirspurn í autt birgðageymsla](design-details-demand-at-blank-location.md).  
  
## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Raðnúmer-lotunúmer eru hlaðinn með lýsingarstigi  
 Eigindum í formi rað-/lotunúmers er hlaðið inn í birgðasnið ásamt eftirspurn og framboði sem þau eru úthlutuð á.  
  
 Eigindir eftirspurnar og framboðs er raðað skv. forgangi pantana sem og eftir forsktirtarstigi þeirra. Vegna niðurstöðu rað- / lotunúmera endurspegla forskriftarstig, nákvæmari eftirspurn, svo sem lotunúmer valið sérstaklega fyrir sölulínu, mun leita að samsvörun fyrir minna takmarkaða eftirspurn, svo sem sölu frá hvaða lotunúmer sem er valið.  
  
> [!NOTE]  
>  Engar forgangsreglur eru fyrir framboð og eftirspurn rað-/lotunúmera, annað en tilgreint stig sem er ákvarðað með samsetningu rað- og lotunúmer og uppsetningu vörurakningar fyrir viðkomandi vörur.  
  
 Við jöfnun les áætlanakerfið framboð með rað- og lotunúmerum sem fast og reynir ekki að auka eða enduráætla svoleiðis birgðapantanir (nema þær séu notaðar í vinnslur milli pantana). Sjá Pöntun fyrir pöntun tenglar eru aldrei rofnir). Þetta ver framboð frá móttöku margra, hugsanlega ósamhljóða aðgerðaboða þegar framboð ber mismunandi eiginleika - ss safn af mismunandi raðnúmerum.  
  
 Önnur ástæða fyrir því að rað-/lotunúmerað framboð er ósveigjanlegt er að rað-/lotunúmerum er alla jafna úthlutað það seint í ferlinu að það myndi valda ruglingi að stinga upp á breytingum.  
  
 Staða rað-/lotunúmera er ekki innan [frosna svæðisins](design-details-dealing-with-orders-before-the-planning-starting-date.md). Ef eftirspurn og framboð er ekki samstillt leggur áætlanakerfið til breytingar eða leggur til nýjar pantanir, óháð upphafsdegi áætlanagerðarinnar.  
  
## <a name="order-to-order-links-are-never-broken"></a>Tenglar á milli pantana eru aldrei rofnir  
 Við áætlun pöntun-í-pöntun vöru má ekki nota tengdu birgðirnar fyrir neina aðra eftirspurn nema þá sem þær voru upphaflega ætlaðar. Tengd eftirspurn ætti ekki að falla undir neitt annað tilviljanakennt framboð, jafnvel þótt það sé tiltækt í tíma og magni við núverandi kringumstæður. Til dæmis er ekki hægt að nota samsetningarpöntun sem tengd er við sölupöntun í aðstæðum þar sem vara er sett saman fyrir pöntun fyrir nokkra aðra eftirspurn.  
  
 Eftirspurn og framboð úr pöntun í pöntun þarf að vera í nákvæmu jafnvægi. Áætlanakerfið tryggir framboð undir öllum kringumstæðum, án þess að taka til greina færibreytur pantanastæðrar, breytingar og magn í birgðum (annað en magn sem varðar tengdar pantanir). Af sömu ástæðu stingur kerfið upp á að minnka umframframboð ef tengda eftirspurnin er minnkjuð.  
  
 Þessi jöfnun hefur einnig áhrif á tímann. Takmarkaði sjóndeildarhringurinn sem ákvarðast af tímarammanum er ekki virtur; framboð verður enduráætlað ef tímasetning eftirspurnar hefur breyst. Hins vegar verður hömlutími virtur og kemur í veg fyrir að pöntun-í-pöntun birgðir séu áætlaðar út, nema innri birgðir úr framleiðslupöntun á mörgum stigum (verkefnispöntun).  
  
> [!NOTE]  
>  Rað/lotunúmeri getur einnig tilgreint um pöntun fyrir pöntun eftirspurn. Í því tilfelli er framboð ekki talin ósveigjanleg sjálfgefið, eins og er venjulega erum að ræða fyrir raðnúmer / lotunúmeri. Í þessu tilviki, mun kerfið auka/minnka miðað við breytingu á eftirspurn. Enn fremur, ef einni eftirspurn fylgja breytileg raðnúmer/lotunúmer, svo sem fleiri en eitt lotunúmer, verður stungið upp á einni framboðspöntun fyrir hverja lotu.  
  
> [!NOTE]  
>  Spár ættu ekki að leiða til þess að stofnaðar séu nýjar birgðapantanir sem eru bundnar af pöntun-í-pöntun tengslum. Ef spáin er notuð ætti aðeins að nota hana til að mynda háða eftirspurn í framleiðsluumhverfi.  
  
## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Íhlutaþörf er hlaðið samkvæmt breytingum á framleiðslupöntun  
 Við meðhöndlun framleiðslupantana verður  áætlanakerfið að fylgjast með nauðsynlegum íhlutum áður en þeim er hlaðið í eftirspurnarforstillinguna. Íhlutalínur sem leiða af breyttri framleiðslupöntun koma í stað upprunalegu pöntunarinnar. Þetta tryggir að áætlanakerfið tvítaki aldrei áætlunarlínurnar fyrir íhluti.  
  
##  <a name="BKMK_SafetyStockMayBeConsumed"></a> Öryggisbirgðir má nota  
 Öryggisbirgðamagn er aðallega eftirspurnargerð og þess vegna hlaðið inn í birgðaforstillinguna í upphafsdagsetningu áætlanagerðar.  
  
 Öryggisbirgðir er birgðamagn sett til hliðar til að bæta upp fyrir óvissu í eftirspurn á áfyllingearafhendingartíma. Hins vegar má nota það ef það er nauðsynlegt að taka af því til að svara eftirspurn. Í þessu tilfelli tryggir áætlunarkerfið að öryggisbirgðir séu endurnýjaðar með því að leggja til afhendingarpöntun til þess að fylla á magn öryggisbirgða á þeim degi er þær verða notaðar. Þessi áætlunarlína mun sýna  fráviksviðvöruntákn sem skýrir að öryggisbirgðir hafi verið notaðar að hluta eða að fullu vegna frávikspöntunar fyrir magn sem vantaði.  
  
## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Spá um eftirspurn er minnkuð eftir sölupöntunum  
 Framleiðsluspáin gefur upp ætlaða verðandi eftirspurn. Þegar rauneftirspurn er slegin inn, yfirleitt sem sölupantanir fyrir framleiddar vörur, notar hún spána.  
  
 Spáin sjálf er í raun ekki minnkuð af sölupöntunum, hún er enn sú sama. Hins vegar er spármagnið sem notað er í útreikningi á áætluninni minnkað (með magni sölupöntunarinnar) áður en magnið sem eftir er, ef eitthvað er, fer í birgðaforstillingu eftirspurnar. Þegar áætlanakerfið kannar raunverulega sölu á einhverju tímabili eru teknar með bæði opnar sölupantanir og birgðahöfuðbókarfærslur úr sendum pöntunum, nema þær séu úr standandi pöntun.  
  
 Notandi þarf að tilgreina gilt spártímabil. Dagsetningin á áætlaðrar magni skilgreinir upphaf tímabilsins, og dagurinn í næstu spá skilgreinir lok tímabilsins.  
  
 Spáin fyrir tímabil fyrir áætlanagerðartímabilið er ekki notuð, án tillits til þess hvort hún var notuð eða ekki. Fyrsta áhugaverða spátala er annaðhvort sá dagur eða næsta dagsetning fyrir upphafsdag áætlunar.  
  
 Spáin getur verið fyrir sjálfstæða eftirspurn, svo sem sölupantanir, eða háð eftirspurn, eins og efnisþætti framleiðslupöntunar (einingaspá). Vara getur haft báðar gerðir spár. Á áætlanagerð, fer neyslu fram fyrir sig, fyrst fyrir sjálfstæða eftirspurn og þá fyrir háða eftirspurn.  
  
## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Eftirspurn standandi pöntunar er minnkuð eftir sölupöntunum  
 Spá er bætt við af standandi sölupöntun í því skyni að tilgreina framtíðareftirspurn frá tilteknum viðskiptamanni. Eins og í (ótilgreindri) spá ætti raunveruleg sala að nota áætlaða eftirspurn og eftirstandandi magn ætti að færa inn birgðaforstillingu eftirspurnar. Eins og áður minnkar notkun ekki raunverulega standandi pöntun.  
  
 Útreikningar áætlanagerðar taka til greina opnar sölupantanir tengdar tilgreindum standandi pöntunum, en tekur ekki til greina nein gild tímabil. Né tekur það tillit til bókaðra pantana þar sem bókunarferlið hefur þegar minnkað útistandandi magn standandi pöntunar.  
  
## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
 [Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
 [Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)
