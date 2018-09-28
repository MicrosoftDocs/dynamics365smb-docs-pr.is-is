---
title: "Hönnunarupplýsingar - Jöfnun framboðs og eftirspurnar | Microsoft Docs"
description: "Kjarni áætlanakerfisins felst í jafnvægi á milli eftirspurn og framboð með því að leggja til notandaaðgerðir til að endurskoða framboðspantanir við ójafnvægi. Þetta á sér stað á blöndu af afbrigði og staðsetningu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 51555bbfbd7fec6ca46bc1b2e6b02382288a41bc
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-balancing-supply-with-demand"></a>Hönnunarupplýsingar: jöfnun framboðs og eftirspurnar
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
  
## <a name="rules-concerning-actions-for-supply-events"></a>Reglur um aðgerðir fyrir framboðstilvik  
Þegar áætlanakerfið framkvæmir ofansækinn útreikninga þar sem birgðir verða að mæta eftirspurn er eftirspurnin tekin sem sjálfgefin, þ.e. er ekki undir stjórn áætlanakerfis. Hins vegar er hægt að stjórna framboðshliðinni. Því mun áætlanakerfið stinga upp á að búnar séu til nýjar birgðapantanir, þær sem fyrir liggja séu enduráætlaðar og/eða pöntunarmagni sé breytt. Ef núverandi birgðapöntun verður óþörf leggur áætlanakerfið til að notandinn hætti við hana.  
  
Ef notandinn vill útiloka núverandi birgðapöntun frá tillögum áætlanagerðar getur hann tekið fram að hún hafi engan sveigjanleika áætlunar (Sveigjanleiki áætlunar = Enginn). Þá er umframframboð úr þeirri pöntun notað fyrir eftirspurn, án þess að stungið sé upp á neinni aðgerð.  
  
Almennt gildir að allt framboð hefur áætlunarsveigjanleika sem takmarkast af skilyrðum hverrar af leiðbeinandi aðgerðum.  
  
-   **Endurtímasetja út**: Dagsetning núverandi framboðspöntunar er hægt að Endurtímasetja út til að mæta skiladegi, nema  
  
    -   Taflan táknar birgðir (alltaf á degi núll).  
    -   Það er með pöntun fyrir pöntun tengda við aðra eftirspurn.  
    -   Hún liggur utan enduráætlunargluggans sem skilgreindur er með tímarammanum.  
    -   Hægt er að nota birgðir sem eru nær.  
    -   Á hinn bóginn kann notandinn að ákveða að enduráætla ekki vegna þess að:  
    -   Birgðapöntunin hefur þegar verið tengd við aðra eftirspurn á fyrri dagsetningu  
    -   Nauðsynleg enduráætlunagerð er svo minniháttar að notanda finnst hún óþörf.  
  
-   **Endurtímasetja inn**: Dagsetning núverandi framboðspöntunar sem er hægt að gera tímaáætlun á, nema í eftirfarandi skilyrðum:  
  
    -   Það er beintengt við einhverja aðra eftirspurn.  
    -   Hún liggur utan enduráætlunargluggans sem skilgreindur er með tímarammanum.  
  
> [!NOTE]  
>  Við áætlun vöru með endurpöntunarmarki, er alltaf hægt að áætla birgðapöntunina ef nauðsynlegt er. Þetta er algengt í birgðapöntun sem er dagsett í framtíðinni sem eru ræstar af endurpöntunarmarki.  
  
-   **Auka magn**: Magn núverandi framboðspöntunar má auka til að mæta eftirspurn nema framboð þess er tengt beint við eftirspurn með Pöntun fyrir pöntun tengil.  
  
> [!NOTE]  
>  Jafnvel þótt hægt sé að auka við birgðapöntunina getur það verið takmarkað vegna skilgreinds hámarks pöntunarmagns.  
  
-   **Minnka Magn**: Núverandi birgðapöntun með afgang miðað við núverandi eftirspurn getur lækkað til að mæta eftirspurn.  
  
> [!NOTE]  
>  Jafnvel þótt hægt væri að minnka magnið getur samt verið afgangur miðað við eftirspurnina vegna skilgreinds lágmarks pöntunarmagns við fjöldapantanir.  
  
-   **Hætta**: Sem sérstök atvik af lækkun magnsaðgerð, er hægt að hætta við birgðapöntun ef það hefur verið lækkað niður í núll.  
-   **Nýtt**: Ef engin framboðspöntun er til staðar eða fyrirliggjandi pöntun er ekki hægt að breyta til að uppfylla nauðsynlegt magn á settum skiladegi er stungið upp á nýrri framboðspöntun.  
  
## <a name="determining-the-supply-quantity"></a>Ákvarða framboðsmagn  
Áætlunarfæribreytur sem tilgreindar voru af notanda stjórna áætluðu magni fyrir hverja framboðspöntun.  
  
Þegar áætlanakerfið reiknar út magn fyrir nýja birgðapöntun eða breytingu á magni í fyrirliggjandi pöntun getur magn sem lagt er til verið annað en raunverulegt eftirspurn segir til um.  
  
Ef hámarksbirgðir eða fast pöntunarmagn er valið er hægt að auka magnið sem lagt er til til að ná þessu fasta magni eða hámarksbirgðum. Ef endurpöntunarstefna notar endurpöntunarmark er hægt að auka magnið að minnsta kosti til að ná endurpöntunarmarkinu.  
  
 Hægt er að breyta ráðlögðu magni í þessari röð:  
  
1. Niður að hámarki pöntunarmagns (ef einhverjar).  
2. Upp að lágmarksmagni pöntunar.  
3. Upp til að mæta næsta margfeldi pöntunar. (Ef rangar stillingar eru notaðar er mögulega farið yfir hámarkspöntunarmagn.)  
  
## <a name="order-tracking-links-during-planning"></a>Pöntunarrakningatenglar í áætlun  
Varðandi pöntunarrakningu við áætlanagerð, það er mikilvægt að nefna að áætlanakerfi endurraðar kvikt stofnuðum pöntunarrakningartenglum fyrir samsetningarnar hlutur/afbrigði / Staðsetningu.  
  
Það eru tvær ástæður fyrir þessu:  
  
-   Áætlanakerfið verður að geta réttlætt tillögur sínar, að allri eftirspurn hafi verið svarað og að engar birgðapantanir séu umfram þörf.  
-   Breytilegir pöntunarrakningartengla þarf að endurjafna reglulega.  
  
Með tímanum myndast ójafnvægi í pöntunarrakningartenglum þar sem pöntunarrakningarnetinu er ekki endurraðað fyrr en eftirspurnar- eða framboðstilvikum er lokað í raun og veru.  
  
Áður framboðs og eftirspurn er jafnað eyðir forritið öllum pöntunarrakningartenglum. Við afstemmingu, þegar eftirspurn eða framboð er lokað, er nýjum pöntunarrakningartenglum komið á milli framboðs og eftirspurnar.  
  
> [!NOTE]  
>  Jafnvel þótt vara sé ekki sett upp fyrir kvika pöntunarrakningi býr áætlunarkerfið til jafnaða pöntunarrakningartengla eins og útskýrt er hér að ofan.  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
