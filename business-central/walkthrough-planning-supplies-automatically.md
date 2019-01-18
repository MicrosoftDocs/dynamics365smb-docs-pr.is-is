---
title: "Kynning - Sjálfvirk áætlun birgða | Microsoft Docs"
description: "Hugtök eins og \"keyra áætlun\" eða \"keyra MRP\" vísa í útreikninga á aðalframleiðsluáætluninni (MPS) og efnisþarfaáætluninni (MRP) útfrá raunverulegri eftirspurn og eftirspurn samkvæmt spá."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 778f182d12959e0332d538c0471a8c2e0d1613a1
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-planning-supplies-automatically"></a>Kynning: Sjálfvirk áætlun birgða
Hugtök eins og "keyra áætlun" eða "keyra MRP" vísa í útreikninga á aðalframleiðsluáætluninni (MPS) og efnisþarfaáætluninni (MRP) útfrá raunverulegri eftirspurn og eftirspurn samkvæmt spá.  

-   MPS er útreikningur á aðalframleiðsluáætlun byggt á raunverulegri eftirspurn og eftirspurnarspá. MPS-útreikningur er notaður fyrir lokavörur sem eru með spá eða sölupöntunarlínu. Þessar vörur eru kallaðar "MPS-vörur" og eru auðkenndar þegar útreikningur hefst.  
-   MRP er útreikningur á efnisþörfum sem byggjast á raunverulegri eftirspurn eftir hlutum og eftirspurnarspá á hlutastigi. MRP er eingöngu reiknað fyrir vörur sem eru ekki MPS-vörur. Megintilgangur MRP er bjóða upp á tímasettar áætlanir þannig að rétt vara er til á réttum tíma, á réttum stað og í réttu magni.  

 Áætlunaralgóritmarnir fyrir MPS og MRP eru eins. Áætlunarreiknireglurnar nota reikning nettóstöðu, endurnotkun birgðapantana og aðgerðarboð. Áætlunarkerfisvinnslan tekur mið af þörfum eða væntanlegum þörfum (eftirspurn) og hvað er til staðar (framboð). Þegar nettóstaða er reiknuð út frá þessum stærðum birtast aðgerðarboð á áætlunarvinnublaðinu. Aðgerðarboð eru tillögur um að stofna nýja birgðapöntun, breyta birgðapöntun (magn eða dagsetning) eða hætta við birgðapöntun. Birgðapantanir geta verið framleiðslupantanir, innkaupapantanir og millifærslupantanir. Nánari upplýsingar eru í [Upplýsingar um hönnun: áætlun birgða](design-details-supply-planning.md).  

 Niðurstöður áætlunargerðar eru reiknaðar að hluta til út frá framboð-eftirspurn gögnunum og að hluta til út frá uppsetningu birgðahaldseiningaspjalda eða birgðaspjalda, framleiðsluuppskrifta og leiða.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
 Þessi kynning sýnir hvernig nota skal birgðaáætlunarkerfið til að áætla sjálfkrafa allar innkaupa- og framleiðslupantanirnar sem þarf til að framleiða 15 kappakstursreiðhjól með eftirspurn á mismunandi sölupöntunum. Til að kynningin sé skýr og raunveruleg hefur fjölda áætlunarlína verið sett afmörkun með því að loka á öll önnur eftirspurn-framboð gögn í sýnifyrirtækinu CRONUS Íslandi hf. nema sölueftirspurnina í birgðageymslunni BLÁTT.  

 Þessi kynning fjallar um eftirfarandi verk:  

-   Stofna sölupöntunina og reikna út fullkomna birgðaáætlun.  
-   Skoða áætlunarfæribreytur og pantanarakningarfærslur fyrir aftan áætlunarlínurnar.  
-   Stofna sjálfkrafa þær birgðapantanir sem lagðar voru til.  
-   Stofna nýja sölueftirspurn og gera nýja áætlun eftir henni.  

## <a name="roles"></a>Hlutverk  

-   Framleiðslustjóri  
-   Innkaupaaðili  

## <a name="prerequisites"></a>Frumskilyrði  
 Til að ljúka þessari kynningu þarf:  

-   Sýnifyrirtækið CRONUS International Ltd.  
-   Að breyta ýmsum vörustillingargildum með því að fylgja leiðbeiningunum í hlutanum Undirbúa sýnigögn, síðar í kynningunni.  

## <a name="story"></a>Ferill  
 Viðskiptamaðurinn, Cannon Group PLC, pantar fimm kappakstursreiðhjól fyrir sendingu þann 02-05-2014 (5. febrúar).  

 Framleiðslustjórinn, Einar, framkvæmir reglubundna birgðaáætlun fyrir fyrstu vikuna í febrúar 2014. Hann afmarkar við sína eigin birgðageymslu, BLÁTT, og færir inn áætlunarbilið 01-23-2014 til 02-07-2014 áður en hann reiknar út fyrstu framboðsáætlun.  

 Eina eftirspurnin þá vikuna er sölupöntunin frá Cannon Group. Einar sér að engar áætlanalínur innihalda viðvaranir, og býr síðan til án breytinga birgðapantanir fyrir þær áætlunarlínur sem lagðar voru til.  

 Daginn eftir, áður en byrjað er á fyrstu birgðapöntununum eða þær bókaðar, fær Einar tilkynningu um að annar viðskiptamaður hafi pantað tíu kappakstursreiðhjól sem senda skal 02-12-2014. Hann endurreiknar til að laga birgðaáætlunina að breyttri eftirspurn. Endurreikningur skilar áætlun hreyfingar sem leggur til breytingar á bæði tíma og magni fyrir sumar af birgðapöntununum sem stofnaðar voru í fyrstu keyrslunni.  

 Í hinum ýmsu þrepum áætlunar getur Einar flett upp viðeigandi pöntunum og notað eiginleikann Rakning pöntunar til að sjá hvaða framboð sinnir hvaða eftirspurn.  

## <a name="preparing-sample-data"></a>Undirbúa sýnigögn  
 Stofna birgðahaldseiningar (SKU) fyrir keppnishjólið og úrval af íhlutum þess, vörunúmer 1001 til 1300. (Sumir íhlutir eru útilokaðir til þess að einfalda ferlið.) Laga áætlunarfæribreytur valinna íhluta til að fá gagnsærri áætlunarniðurstöður.  

### <a name="to-create-stockkeeping-units"></a>Stofna birgðahaldseiningu  

1.  Opna birgðaspjaldið fyrir vöru 1001, kappakstursreiðhjól.  
2.  Valið er **Stofna birgðahaldseining** aðgerð.  
3.  Á síðunni **Stofna birgðahaldseining** skal skilja alla valkosti og afmarkanir eftir óbreyttar og smella svo á **Í lagi**.  
4.  Skref 1 til 3 eru endurtekin fyrir allar vörur á númerabilinu 1100 til 1300.  

### <a name="to-change-selected-planning-parameters"></a>Til að breyta völdum áætlunarfæribreytum  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðahaldseiningar** og veldu síðan tengda tengilinn.  
2.  Opna BLUE birgðahaldseininguna fyrir vöru 1100, framhjól.  
3.  Á flýtiflipanum **Áætlun** eru reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

    |Endurpöntunarstefna|Magn í öryggisbirgðum|Lotusöfnunartímabil|Enduráætlunartímabil|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Lotu-fyrir-lotu|Autt|2V|2V|  

4.  Skref 2 til 3 eru endurtekin fyrir allar birgðarhaldseiningar á númerabilinu 1100 til 1300.  

 Svona lýkur undirbúningi sýndargagna fyrir kynninguna.  

## <a name="creating-a-regenerative-supply-plan"></a>Stofna birgðaáætlun með endurgerð  
 Við meðhöndlun á nýrri sölupöntun á fimm kappakstursreiðhjólum, byrjar notandinn skipulagsferlið með því að stilla valmöguleika, afmarkanir og áætlunarbil til að útiloka alla aðra eftirspurn nema þá sem er í fyrstu viku mars í staðsetningunni BLÁTT. Hann byrjar á að reikna út aðalframleiðsluáætlun (MPS) , og reiknar síðan út fullkomna birgðaáætlun fyrir alla lægra-stigs eftirspurn (MRP).  

### <a name="to-create-the-sales-order"></a>Stofna sölupöntun  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2.  Valið er **Nýtt** aðgerð.  
3.  Á síðunni **Sölupöntun** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Nafn selt-til-viðskiptavinar|Afh.dags|Vörunr.|Birgðageymsla|Magn|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Cannon Group|02-05-2014|1001|BLÁTT|5|  

4.  Ráðstöfunarviðvörunin er samþykkt og svo er hnappurinn **Já** valinn til að skrá nýtt eftirspurnarmagn.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-blue"></a>stofna endurgerðaráætlun til að uppfylla eftirspurn í birgðageymslunni BLÁTT.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlunarvinnublöð** og veldu síðan tengda tengilinn.  
2.  Velja **Reikna áætlun endurgerðar** aðgerðina.  
3.  Á **Reikna áætlun - Áætl.tillaga** síðuna, fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Reikna áætlun|Upphafsdagsetning|Lokadagsetning|Sýna niðurstöður:|Takmarka samtölur við|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Já<br /><br /> **MRP** = Nei|01-23-2014<br /><br /> (vinnudagsetning)|02-07-2014|1001..1300|Vöruhúsasía = BLÁTT|  

4.  Velja hnappinn **Í lagi** til að ræsa áætlunarkeyrsluna.  

     Ein áætlunarlína er stofnuð sem leggur til að áætluð framleiðslupöntun sé gefin út til að framleiða kappakstursreiðhjólin tíu, vöru 1001, fyrir 02-05-2014, afhendingardagsetningu sölupöntunarinnar.  

     Næst skal gengið úr skugga um að þessi áætlunarlína vísi í sölupöntun Cannon Group með því að nota aðgerðina **Rakning pöntunar** sem tengir eftirspurn áætluðu framboði.  

5.  Veljið nýju áætlunarlínuna og veljið því næst **Rakning pöntunar** aðgerðina.  
6.  Á síðunni **Rakning pöntunar** er smellt á **Sýna**.  

     Sölupöntunin fyrir fimm kappakstursreiðhjól sem afhenda á viðskiptamanni með númerið 10000 þann 02-05-2014 er birt.  

7.  Lokið síðunum **Sölupöntun** og **Pöntunarrakning**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Til að reikna MRP svo það taki undirliggjandi íhlutaþarfir með  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlunarvinnublöð** og veldu síðan tengda tengilinn.  
2.  Velja **Reikna áætlun endurgerðar** aðgerðina.  
3.  Á **Reikna áætlun - Áætl.tillaga** síðuna, fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Reikna|Upphafsdagsetning|Lokadagsetning|Sýna niðurstöður:|Takmarka heildartölur við:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Já<br /><br /> **MRP** = Já|01-23-2014|02-07-2014|1001..1300|Vöruhúsasía = BLÁTT|  

4.  Velja hnappinn **Í lagi** til að ræsa áætlunarkeyrsluna.  

     Stofnaðar eru 14 áætlunarlínur sem leggja til birgðapantanir fyrir alla eftirspurnina sem sölupöntunin fyrir kappakstursreiðhjól í vörugeymslunni BLÁTT stendur fyrir.  

## <a name="analyzing-the-planning-result"></a>Greining á áætlunarniðurstöðunum  
 Til að greina magnið sem lagt var til kafar Einar í valdar áætlunarlínur til að skoða pantanarakningarfærslur og áætlunarfæribreytur.  

 Á síðunni **Áætlunarvinnublað** skal athuga að í dálknum **Gjalddagi** eru birgðapantanirnar sem lagðar eru til skipulagðar aftur á bak frá gjalddaga sölupöntunarinnar, 02-05-2014. Tímalínan byrjar á efstu áætlunarlínunni með framleiðslupöntuninni til að framleiða fullgerð keppnisreiðhjól. Tímalínan endar á neðstu áætlunarlínu á innkaupabeiðninni fyrir eina af lægsta-stigs vörunum, 1255, afturtengi, sem skila á 01-30-2014. Eins og áætlunarlínan fyrir vöru 1251, öxull afturhjóls, sýnir þessi lína innkaupapöntun fyrir íhluti sem eiga að vera til reiðu á upphafsdagsetningu yfirvörunnar, millivara 1250, en skiladagur hennar er aftur á móti 02-03-2014. Á öllu vinnublaðinu má sjá að undirliggjandi vörur eru með skiladag á upphafsdagsetningu yfirvöru þeirra.  

 Áætlunarlínan fyrir vöru 1300, keðju, leggur til tíu stykki. Þetta er frávik frá þeim fimm stykkjum sem áætlað er að uppfylli sölupöntunina. Skoðið svo pantanarakningarfærslurnar.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>Til að skoða pöntunarrakningarfærslur fyrir vöru 1300  

1.  Velja skal áætlunarlínuna fyrir vöru 1300 og smella svo á **Rakning pöntunar** aðgerðina.  

     Línurnar tvær á síðunni **Rakning pöntunar** sýna að fimm stykki eru rakin frá áætlunarlínunni (fyrsta pantanarakningarlína) til sölupöntunar 1001 (önnur pantanarakningarlína). Síðustu fimm stykkin sem lögð eru til á áætlunarlínunni tengjast engum skjalalínum, heldur einungis færibreytu áætlunar, spáfærslu eða standandi pöntunarfærslu. Þetta órakta magn er tekið saman í reitnum **Órakið magn** í haus síðunnar **Rakning pöntunar**.  

2.  Veljði reitinn **órakið magnið**.  

     Síðan **Órakin áætlunareining** sýnir að vara 1300 notar áætlunarfæribreytu, Lágmarksmagn pöntunar, tíu stykki. Áætlunarlínan hljóðar því upp á tíu stykki í heildina, en aðeins fimm þeirra er hægt að rekja til eftirspurnar. Síðustu fimm stykkin eru órakið magn til að uppfylla áætlunarfæribreytuna. Næsta þarf að yfirfara áætlunarfæribreyturnar.  

### <a name="to-check-the-planning-parameter"></a>Til að athuga áætlunarfæribreytuna  

1.  Á síðunni **Óraktar áætlunareingar** er viðeigandi pantanarakningarlína valin fyrir vöru 1300.  
2.  Velja reitinn **Vörunr.** og svo **Ítarlegt** aðgerðina.  
3.  Á síðunni **Vörulisti** skal velja aðgerðina **Birgðahaldseiningar**.  
4.  Á síðunni **Birgðaeiningalisti** skal opna birgðaeiningarspjaldið BLÁTT.  
5.  Á flýtiflipanum **Áætlun** skal athuga að reiturinn **Minnsta pöntunarmagn** inniheldur 10.  
6.  Öllum síðum nema **Áætlunarvinnublað** er lokað.  

### <a name="to-view-more-order-tracking-entries"></a>Til að skoða fleiri pantanarakningarfærslur  

1.  Velja skal áætlunarlínuna fyrir vöru 1110 og smella svo á **Rakning pöntunar** aðgerðina.  

     Síðan **Rakning pöntunar** sýnir að fimm felgur þarf fyrir hverja framleiðslupöntun, fyrir fram- og afturhjól.  

     Sama pöntunarrakningin gildir fyrir áætlunarlínur varanna 1120, 1160 og 1170. Fyrir vöru 1120 er reiturinn **Magn per** á framleiðsluuppskriftinni fyrir hverja hjólavöru 50 STK, sem verður til þess að heildarþörfin er 100.  

     Áætlunarlínan fyrir vöru 1150, fyrir sex stykki, virðist óvenjuleg. Haldið áfram til að greina.  

2.  Velja skal áætlunarlínuna fyrir vöru 1150 og smella svo á **Rakning pöntunar** aðgerðina.  

     Síðan **Rakning pöntunar** sýnir að fimm einingar eru raktar til framhjólsins og að ein eining er órakin. Skoðið svo órakta magnið.  

3.  Veljði reitinn **órakið magnið**.  

     Síðan **óraktar áætlunareiningar** sýnir að varan 1150 notar áætlunarfæribreytuna, Margföld pöntun, með 2.00, sem tilgreinir að þegar varan er pöntuð verður að vera hægt að deila magninu með 2. Sú tala næst 5 sem hægt er að deila í með 2 er 6.  

     Sama pöntunarrakningin gildir fyrir áætlunarlínur íhluta Framnafar, vörur 1151 og 1155, nema að hver þörf margfaldast af rýrnunarprósentu sem er skilgreind fyrir vöru 1150 í reitnum **Úrkastsprósenta** á birgðaspjaldinu.  

 Svona lýkur greiningu fyrstu birgðaáætlunar. Takið eftir að gátreiturinn **Samþykkja aðgerðaboð** er valinn í öllum áætlunarlínum sem gefur til kynna að þær séu nú tilbúnar til umbreytingar í birgðapantanir.  

## <a name="carrying-out-action-messages"></a>Framkvæmd aðgerðarboða  
 Næst breytir Einar áætlunarlínunum sem lagðar voru til í birgðapantanir með því að nota aðgerðina **Framfylgja aðgerðarboðum**.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>Til að stofna sjálfkrafa þær birgðapantanir sem lagðar voru til  

1.  Veljið gátreitinn **Samþykkja aðgerðaboð** á öllum áætlunarlínum með viðvörun af gerðinni Frávik.  
2.  Veljið aðgerðina **Framkvæma aðgerðaboð**.  
3.  Á síðunni **Framkvæma aðgerðaboð - áætlun** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Framleiðslupöntun|Innkaupapöntun|Millifærslupöntun|  
    |----------------------|--------------------|--------------------|  
    |Fastáætluð|Gera innkaupapantanir|Gera millifærslupantanir|  

4.  Veldu hnappinn **Í lagi** til að stofna sjálfkrafa allar birgðapantanir sem lagðar voru til.  
5.  Lokið tómu síðunni **Áætlunarvinnublað**.  

 Svona lýkur fyrstu útreikningum, greiningu og stofnun fyrir eftirspurn í staðsetningunni BLÁTT í fyrstu viku febrúar. Í hlutanum sem á eftir kemur pantar annar viðskiptamaður tíu kappakstursreiðhjól, og Einar þarf að enduráætla.  

## <a name="creating-a-net-change-plan"></a>Stofnun áætlunar hreyfingar  
 Daginn eftir, áður en byrjað er á birgðapöntunum eða þær bókaðar, berst ný sölupöntun frá Libros S.A. á tíu kappakstursreiðhjólum sem á að afhenda 02-12-2014. Einar er látinn vita af þessari nýju eftirspurn, og hann enduráætlar til að aðlaga birgðaáætlunina. Einar notar aðgerðina Áætlun hreyfingar til að reikna aðeins þær breytingar sem orðið hafa á framboði eða eftirspurn frá síðustu áætlunarkeyrslu. Auk þess stækkar hann áætlunartímabilið í 02-14-2014 svo nýja sölueftirspurnin fallin innan 02-12-2014.  

 Áætlunarkerfið reiknar út bestu leiðina til að uppfylla eftirspurnina eftir þessum tveimur eins vörum, svo sem að sameina sumar innkaupa- og framleiðslupantanir, endurtímasetja aðrar pantanir og stofna nýjar pantanir ef með þarf.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>Til að stofna nýja sölueftirspurn og enduráætla eftir því  

1.  Valið er **Nýtt** aðgerð.  
2.  Á síðunni **Sölupöntun** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Nafn selt-til-viðskiptavinar|Afh.dags|Vörunr.|Birgðageymsla|Magn|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A.|02-12-2014|1001|BLÁTT|10|  

3.  Ráðstöfunarviðvörunin er samþykkt og svo er hnappurinn **Já** valinn til að skrá eftirspurnarmagnið.  
4.  Næst þarf að enduráætla til að aðlaga birgðaáætlunina.  
5.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlunarvinnublöð** og veldu síðan tengda tengilinn.  
6.  Velja **Reikna áætlun nettóbreytingar** aðgerðina.  
7.  Á **Reikna áætlun - Áætl.tillaga** síðuna, fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Reikna áætlun|Upphafsdagsetning|Lokadagsetning|Sýna niðurstöður:|Takmarka samtölur við|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Já<br /><br /> **MRP** = Já|01-23-2014|02-14-2014|1001..1300|Vöruhúsasía = BLÁTT|  

8.  Velja hnappinn **Í lagi** til að ræsa áætlunarkeyrsluna.  

 14 áætlunarlínur eru stofnaðar. Takið eftir að í fyrstu áætlunarlínunni að í reitnum **Aðgerðaboð** stendur **Ný**, í reitnum **Magn** stendur 10 og í reitnum **Skiladagur** stendur 02-12-14. Þessi nýja lína fyrir yfireiningu 1001, kappakstursreiðhjól, er stofnuð vegna þess að varan notar endurpöntunarstefnuna **Panta**, sem þýðir að það verður að birgja hana í einn-fyrir-einn sambandi við eftirspurnina, sölupöntun upp á tíu stykki.  

 Næstu tvær áætlunarlínur eru framleiðslupantanirnar fyrir hjól kappakstursreiðhjóla. Allar pantanir sem til voru fyrir upp á fimm stykki í reiturinn **Upprunalegt magn**, eru stækkað upp í 15 í reiturinn **Magn**. Báðar framleiðslupantanir hafa óbreyttar skiladagsetningar, eins og sjá má í reitnum **Aðgerðarboð** þar sem stendur **Breyta magni**. Þetta gildir einnig um áætlunarlínuna fyrir vöru 1300, fyrir utan pöntun þessi sinnum 10.00 námundar rakta eftirspurn fyrir 15 stykki upp í 20.  

 Allar aðrar áætlunarlínur eru með aðgerðarboðin **Endurtímas. og br. magni**. Það þýðir að fyrir utan að hafa aukið magn eru skiladagsetningarnar færðar til samræmis við birgðaáætlunina svo þær innihaldi aukamagnið í tiltækum framleiðslutíma (geta). Keyptir íhlutir eru enduráætlaðir og auknir til að mæta framleiðslupöntununum. Haldið áfram til að greina nýju áætlunina.  

## <a name="analyzing-the-changed-planning-result"></a>Greining á hreyfingaáætlunarniðurstöðunum  
 Þar sem allar lota-fyrir lotu vörur innan afmörkunarinnar, 1100 til 1300, hafa tveggja vikna enduráætlunartímabil, er öllum fyrirliggjandi birgðapöntunum breytt til að uppfylla nýju skilyrðin sem eiga sér stað innan þeirra tveggja vikna sem voru tilgreindar.  

 Margar áætlunarlínur eru einfaldlega margfaldaðar með þremur til veita 15 kappakstursreiðhjól í stað 5, og skiladagsetningarnar eru færðar aftur í tíma til að veita aukna magninu fyrir afhendingardagsetningu sölupöntunarinnar til Cannon Group. Fyrir þessar áætlunarlínu er hægt að rekja allt magn. Hinar eftirstandandi áætlunarlínur eru auknar um tíu stykki ásamt því að gjalddagar þeirra eru færðir. Fyrir þessar áætlunarlínur, eru hluti magnsins órakið vegna mismunandi áætlunarfæribreyta. Skoðið svo eitthvað af þessum pantanarakningarfærslum.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>Til að skoða pöntunarrakningarfærslur fyrir vöru 1250  

1.  Velja skal áætlunarlínuna fyrir vöru 1250 og smella svo á **Rakning pöntunar** aðgerðina.  

     Línurnar sjö á síðunni **Rakning pöntunar** sýna að fimm og tíu stykki eru rakin í gegn um afturhjólið að kappakstursreiðhjólinu á sölupöntununum tveim.  

     Fimm síðustu stykkin eru órakin. Haldið áfram til að greina.  

2.  Veljði reitinn **órakið magnið**.  

     Síðan **Óraktar áætlunareiningar** sýnir að vara 1250 notar áætlunarfæribreytu, Margföld pöntun, með 10.00. Þess vegna er áætlunarlínan fyrir 20 stykki samtals til að námunda raunþörfina að næstu tölu sem er deilanleg með 10. Síðustu fimm stykkin eru órakið magn til að uppfylla áætlunarfæribreytuna.  

3.  Öllum síðum nema **Áætlunarvinnublað** er lokað.  

### <a name="to-view-an-existing-order"></a>Fyrirliggjandi pöntun skoðuð  

1.  Í áætlunarlínunni fyrir vöru 1250 er reiturinn **Tilv. Pöntunarnúmer** valinn. .  
2.  Á síðunni **Fastáætluð framleiðslupöntun** fyrir Afturnafið. Hin fyrirliggjandi pöntun fyrir tíu stykki, sem búin var til í fyrstu áætlunarkeyrslunni, opnast.  
3.  Loka fastáætlaðri framleiðslupöntun.  

 Svona lýkur kynningunni á því hvernig áætlunarkerfið er notað til að nema sjálfkrafa eftirspurn, reikna út viðeigandi birgðapantanir út frá eftirspurn og áætlunarfæribreytum, og stofna síðan sjálfkrafa mismunandi gerðir birgðapantana með viðeigandi dagsetningar og magn.  

## <a name="see-also"></a>Sjá einnig  
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)   
 [Kynning: Handvirk áætlun birgða](walkthrough-planning-supplies-manually.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

