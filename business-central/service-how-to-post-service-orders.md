---
title: Hvernig á að bóka þjónustupantanir
description: 'Þegar þjónustupöntun hefur verið búin til, allar upplýsingar færðar inn og breytingar gerðar er hægt að bóka þjónustupöntunina.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="post-service-orders-and-credit-memos"></a>Bóka þjónustupantanir og kreditreikninga
Þegar þjónustupöntun hefur verið búin til, allar upplýsingar færðar inn og breytingar gerðar er hægt að bóka þjónustupöntunina. Í pöntuninni þarf að vera að minnsta kosti ein þjónustuvörulína og ein þjónustulína áður en hægt er að bóka þjónustupöntunina. Ef pöntunin inniheldur meira en eina þjónustulínu mun forritið bóka allar línurnar í einu.  

Ef þú ert með margar þjónustupantanir kemur sér vel að bóka þær í fjöldabókun á sama tíma. Hægt er að keyra runuvinnsluna frá öllum þjónustupöntunum.

> [!Tip]
> Áður en þú bókar þjónustuskjal, er óvitlaust að nota **Prufuskýrsla** aðgerðina til að leita að villum eða upplýsingum sem vantar. Ef villur eru til staðar verður að leysa vandamálið. Hægt að prenta nýja prófunarskýrslu til að sannreyna lagfæringuna og bóka skjalið.

## <a name="to-post-a-service-order"></a>Þjónustupantanir bókaðar:
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Opna skal viðeigandi þjónustupöntun.  
3. Á síðunni **Þjónustupöntun** er ein af eftirfarandi aðgerðum er valin.  

    |**Aðgerð**|**Niðurstaða**|  
    |------------------|----------------|  
    |**Prófunarskýrsla** | Kannar alla hluta skjalsins og birtir niðurstöðuna í skýrslu. Ef í skýrslunni koma fram villur eða ef upplýsingar vantar verður að laga það. Síðan er hægt að prenta nýja prófunarskýrslu.|  
    |**Bóka** | Bókar pöntunina án þess að prenta afhendingu eða reikning.|  
    |**Bóka og prenta** | Bókar pöntunina og prentar afhendingu (ef pöntunin er afhent án þess að hún sé reikningsfærð) eða reikning (ef pöntunin er reikningsfærð).|  
    |**Fjöldabóka** | Bókar margar þjónustupantanir í einu í eitt skipti.|  

4. Þegar pöntunin er bókuð verður að tilgreina einn af eftirfarandi valkostum um hvernig skal bóka pöntunina.  

    |**Bókunarvalkostur**|**Niðurstaða**|  
    |------------------------|----------------|  
    |**Afhenda** | Bókar afhendingu varanna.|  
    |**Reikningur** | Reikningsfærir vörur sem þegar hafa verið afhentar.|  
    |**Afhenda og reikningsfæra** | Vörurnar eru afhentar og reikningsfærðar.|  
    |**Afhenda og nota** | Bókar afhendingu og notkun pöntunarinnar. Það uppfærir viðeigandi magn í þjónustulínum pöntunarinnar og í þjónustuafhendingarskjali sem þegar var bókað.|  

Hægt er að bóka notkun aðeins ef línan inniheldur magn sem hefur verið afhent en ekki reikningsfært eða notað.  

Þegar pöntun er bókuð býr forritið til samsvarandi fjárhagsfærslu og bókuð fylgiskjöl. Viðeigandi reitir eru uppfærðir í þjónustupöntunarskjalinu.  

## <a name="to-batch-post-service-orders"></a>Þjónustupantanir fjöldabókaðar:
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Veljið aðgerðina **Fjöldabókun**.  
3.  Hægt er að stilla afmörkun til að velja ákveðin pöntunarnúmer eða röð af pöntunarnúmerum fyrir keyrsluna.  
4.  Smellt er á **Í lagi** til að hefja keyrsluna.  

## <a name="to-post-a-service-credit-memo"></a>Þjónustukreditreikningar bókaðir:
Þegar búið er að búa til þjónustukreditreikning og fylla hann út er hægt að bóka kreditreikninginn. Ef einhverjar villur eða skortur á upplýsingum um kreditreikninginn kemur í ljós við bókun er ferlið rofið með villuboðum.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustukreditreikningar** og velja síðan viðkomandi tengil.  
2. Nýr þjónustukreditreikningur er stofnaður. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn í reitina eftir þörfum.  
4. Valið er **Bóka** aðgerðin. Ef prenta á út kreditreikninginn um leið og bókað er skal velja aðgerðina **Bóka og prenta** þess í stað.  
5. Til þess að prófa kreditreikninga áður en þeir eru bókaðir er **Prófunarskýrsla** valin. Þegar skýrslan er keyrð eru bókunardagsetningar sem tilgreindar eru í skjalinu staðfestar.  
6. Til þess að fjöldabóka nokkra kreditreikninga í einu. er hægt að nota keyrsluna **Fjöldabóka kreditreikninga þjónustu**. Hún getur verið gagnleg ef þarf að bóka marga kreditreikninga.  

> [!NOTE]  
>  Brýnt er að færa inn allar nauðsynlegar upplýsingar á kreditreikningana áður en þeir eru fjöldabókaðir. Annars er ekki víst að þær bókist. Þegar fjöldabókun er lokið birtast skilaboð um hve margir þjónustukreditreikningar voru bókaðir.  

## <a name="to-post-consumption-from-a-service-order"></a>Að bóka notkun úr þjónustupöntun:
Eftirfarandi ferli lýsir því hvernig á að bóka vörur, forðastundir og eða kostnað sem notaður er fyrir tiltekna þjónustuaðgerð sem ekki á að gjaldfæra á viðskiptamanninn. Aðeins er hægt að bóka notaðar vörur, stundir eða kostnað fyrir bókaða afhendingu sem hefur enga bókaða reikninga eða notkun.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Opna skal þjónustupöntunina sem bóka á notkun fyrir.  
3. Veljið þjónustuvöruna. Veljið aðgerðina **Þjónustulínur**.  
4. Nauðsynlegar færslur eru fundnar og magnið sem bóka á notkun í reitnum **Magn til notkunar** tilgreind fyrir. Magnið getur ekki verið meira en það magn sem þegar hefur verið afhent og eftirstandandi magn en ekki reikningsfært eftir hlutareikningsfærslu afhendingarinnar.  

    > [!NOTE]  
    >  Til að skrá notkun með tilliti til verks þarf að fylla út reitina **Verk nr.,** Verkhlutanr. **verks** og **Tegund** verklínu í þjónustulínunni.  

5. Veljið línunum sem á að bóka og og síðan valið **Bóka** aðgerð. Á síðunni sem opnast skal velja **Afhenda og nota**.  

Þjónustan er bókuð sem notuð ýmist að hluta eða að fulla, eftir gildinu í reitnum **Magn til notkunar**, og viðeigandi færslubókarfærslur eru búnar til. Þar að auki eru áður bókuð þjónustuafhendingarskjöl uppfærð í tímaröð með notuðu magni. Magnið sem við á er uppfært í þjónustulínum pöntunarinnar.  

## <a name="to-post-shipments-from-service-orders"></a>Bókun afhendinga úr þjónustupöntunum:
Þegar sundurliðun þjónustu hefur verið tilgreind er hægt að stilla og bóka magn notaðra vara, stunda sem eytt hefur verið kostnaðar sem fram er kominn. [!INCLUDE[prod_short](includes/prod_short.md)] Gerir í framhaldi af því nauðsynlegar breytingar sem gefa til kynna nýja birgðastöðu og gildandi stöðu þeirrar pöntunar sem er í vinnslu hverju sinni.  

Eftirfarandi ferli sýnir hvernig á að bóka afhendingu þjónustulínuvara í birgðageymslum sem ekki eru settar upp þannig að krafist sé vöruhúsastjórnunar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupöntun** og svo velja viðeigandi tengil. 2. á síðunni fyrir völdu þjónustupöntunina er smellt á **Aðgerðir**, **Pöntun**, **Þjónustulínur**.  
3. Á síðunni **Þjónustulínur** er leitað að færslunum sem þörf er á og þvínæst er magn til bókunar í reitnum **Magn til afhendingar**.  

   > [!NOTE]  
   >  Gildið fyrir magn til afhendingar veltur á því hvort ætlunin er að bóka afhendingu að hluta til eða til fulls. Ef afhending til fulls er valin verður gildið í reitnum **Magn til afhendingar** að vera hið sama og gildið í reitnum **Magn**. Ef afhending að hluta er bókuð verður að tilgreina magnið sem ætlunin var að afhenda í byrjun. Hafi hluti þjónustunnar þegar verið afhentur verður að skrá gildið í reitnum **Afhent magn**. Hámarksmagn sem hægt er að færa inn í reitinn **Magn til afhendingar** er fjöldi eininga sem á eftir að afhenda.  

4. Valið er **Bóka** aðgerðin. á síðunni sem birtist velurðu **Afgreiða** hnappinn.

[!INCLUDE[prod_short](includes/prod_short.md)] stofnar fjárhagsfærslur (í ábyrgðahöfuðbók, birgðahöfuðbók, þjónustuhöfuðbók eða fjárhag), framleiðir bókað þjónustuafhendingarfylgiskjal og uppfærir viðkomandi reiti í þjónustulínum þjónustupöntunarinnar.  

Ef birgðageymslan er sett upp þannig að hún krefjist vöruhúsaafgreiðslu virka afhending og færsla þjónustulínuvara á sama hátt og í öðrum upprunaskjölum. Eini munurinn er sá að hægt er að nota þjónustulínuvörurnar við ytri eða innri vinnslu og þær krefjast því tvenns konar mismunandi afhendingarvirkni.  

Til að fræðast meira um afhendingu þjónustulínuvara í ítarlegri grunnstillingu vöruhúss er farið í að tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

## <a name="to-undo-posted-consumption"></a>Afturkalla bókaða notkun
Þú getur hætt við notkun á þjónustupöntununum. Til dæmis vegna þess að hún var bókuð fyrir mistök.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðar þjónustuafhendingar** og velja síðan viðkomandi tengil.  
2. Opna skal bókuðu þjónustuafhendinguna sem ranga notkunin var bókuð fyrir.  
3. Veldu aðgerðina **Þjónustuafhendingarlínur**.  
4. Veldu línur sem innihalda ranga notkun, og veldu svo aðgerðina **Afturkalla notkun**.  

 Þjónustuafhendingarlína er færð inn með neikvæðu virði í magnreitum fyrir valdar línur.  
  
> [!NOTE]  
>  Ekki er hægt að afturkalla þjónustunotkun ef:  

>    * Þjónustupöntuninni hefur verið lokað.  
>    * Hún hefur verið bókuð á verksvæðið og því eru verkfærslur tengdar því.  

## <a name="to-post-service-lines"></a>Þjónustulínur bókaðar:
Ef nauðsynlegt er að vinna með þjónustupöntun í umtalsverðan tíma án þess að bóka hana gæti þurft að bóka sumar af þjónustulínunum sem tengdar eru henni á þann hátt, til dæmis að uppfæra birgðir. Hægt er að bóka með því að tiltaka viðeigandi magn á línum sem á að bóka. Hægt er að bóka eina og eina línu fyrir sig eða með því að velja nokkrar línur í einu.  

Eftirfarandi ferli lýsir bókun afhendingar beint úr þjónustupöntun í birgðageymslum án þess að meðhöndlun vöruhúss hafi verið sett upp. Ef birgðageymslan er sett upp þannig að hún krefjist vöruhúsaafgreiðslu fer bókun afhendingar fram í öðru vöruhúsaskjali, eftir birgðageymsluuppsetningu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Veljið þjónustupöntunina og velja svo aðgerðina **þjónustulína**.  
4. Fyllt er út í reitina **Magn til afhendingar**, **Magn til reikningsf. og** Magn til nota **eftir því hvernig línurnar eru bókaðar** .  
5. Valið er **Bóka** aðgerðin.

## <a name="see-also"></a>Sjá einnig .
[Bókun í þjónustukerfi](service-service-posting.md)  
[Stofnun þjónustupöntunar](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
