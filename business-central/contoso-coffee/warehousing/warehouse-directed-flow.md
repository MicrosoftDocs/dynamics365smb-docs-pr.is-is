---
title: 'Móttaka, Frágangur, flutningur, tiltekt og sendingu í Ítarleg Vöruhúsakerfi með beinar tínslur og frágang'
description: Á viðskipta-miðlægum er hægt að framkvæma inn-og úttaflana á mismunandi hátt eftir því hversu flókið það er í vöruhúsinu.
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-advanced-warehouse-configuration-with-directed-put-away-and-pick"></a><a name="walkthrough-of-inbound-and-outbound-flow-in-advanced-warehouse-configuration-with-directed-put-away-and-pick"></a>Ganga frá inn-og útstreymissútflæði í ítarlegri samskipan vöruhúss með beinan frágang og tínslu

Þessi gönguleið sýnir hvernig á að fylla út inn-og út streymi í ítarlegu: beinn frágangur og Tínsluafbrigði. Sjá  [Yfirlit yfir mismunandi skilgreiningarvalkosti fyrir frekari upplýsingar](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a><a name="prerequisites"></a>Frumskilyrði
Ef þú vilt ljúka við þetta gönguleið þarftu að gera vöruhúsastarfsmann á  *hvítum*  stað með því að fylgja þessum skrefum:  
1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 1.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3. Í reitnum **Birgðageymslu kóði** færið inn HVÍTT.  
4.  **Virkja sjálfgefna**  skipta.


## <a name="scenario"></a><a name="scenario"></a>Aðstæður
Ellen, vöruhúsastjórinn nýtir sér hjáskipunaraðgerðir og hólfaáfyllingaraðgerð til að flýta móttöku og sendingartíma.  

## <a name="steps"></a><a name="steps"></a>Skref

1. Stofna vöruhúsaafhendingu.  

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 2.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Velja pöntun fyrir viðskiptavin 10000 fyrir HVÍTAN stað. Ytra Pöntunarnr er  *W-1*. Notaðu sérsniðsverkfærin ef  **ytri Pöntunarnr**. Svæði ekki sýnilegt. Sjá  [Sérsníða vinnusvæðið](../../ui-personalization-user.md) til að fá frekari upplýsingar.
    3.  **Veldu vöruhúsaafhendingaraðgerðina**  til að stofna vöruhúsaafhendingu fyrir völdu sölupöntunina.
    4.   **Aðgerðin úttektaraðgerð**  er valin til að láta vöruhúsið vita að Söluafhendingin sé tilbúin fyrir meðhöndlun vöruhúss.  

2. Skilgreina hólf fyrir vöruna sem á að stjórna þar sem hún er fráleit 

    1.  Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 3.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
    2.  Velja skal  *wrb-1000*  og velja  **síðan innihald**  hólfs.  
    3.  Valið er aðgerðin **Nýtt**. Bæta við tveimur línum. Notaðu sérsniðsverkfærin ef  **reiturinn Kóti hólfs**  er ekki sýnilegur. Sjá  [Sérsníða vinnusvæðið](../../ui-personalization-user.md) til að fá frekari upplýsingar. 
    
    |Vara|Staðsetningarkóði|Hólfkóti|Fast|Mælieining|
    |----------|----------|---------|---|------|  
    |WRB-1000|HVÍTT|W-05-0001|Já|POKI|  
    |WRB-1000|HVÍTT|W-05-0002|Já|POKI|

3. Stofna vöruhúsamóttöku.  

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 4.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
    2. Velja pöntun frá lánardrottni 10000 fyrir HVÍTAN stað. Pöntunarnr lánardrottins er  *W-2*. Notaðu sérsniðsverkfærin ef  **Pöntunarnr**. Svæði ekki sýnilegt. Sjá  [Sérsníða vinnusvæðið](../../ui-personalization-user.md) til að fá frekari upplýsingar.
    3.  **Veljið móttökuaðgerðina Móttaka**  vöruhúss til að stofna vöruhúsamóttöku fyrir völdu innkaupapöntunina.


4. Athugaðu hvort það eru útsend pantanir sem þurfa mótteknar vörur og Bóka móttöku
    1. Veldu aðgerðina **Reikna út Hjáskipun**. Þetta mun fylla út dálkamagn  **til að Hjábrytja**.
    2. Fært er inn 0 í  **reitinn Magn til að fara úr bryggju**  í línunni með Item  *wrb-1000*  og ekki er ætlunin að endurpakka á móttökusvæðinu.
    3.  **Veljið aðgerðina Bóka kvittun** .

5. Skrá frágang vöruhúsafrágangs
    1.  ![Notkun ljósapera sem opnast Segðu mér lögun 5](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Teikn, færa inn  **vöruhúsafrágang**  og velja tengdan tengil.
    2. Staðsetja vöruhúsafrágang skjals sem búið var til úr vöruhúsamóttöku og opna hana
    3.  **Í frágangssíðu vöruhúsafrágangs**  er farið yfir  **kaflann línur** 

    Á þessu stigi er hólfageturökin ljós. Frágangslínur vöruhúss verða þrjár línur fyrir vöruwrb  *-1000*:
    - Take Line til að færa móttekið magn úr móttökuhólfinu (W-08-0001)
    - Stað lína sem mun flytja eina TÖSKU inn á eitt af skilgreindum föstum hólfum (W-05-0001)
    - Stað lína sem mun flytja annan POKANN í önnur föst hólf (W-05-0002). Þetta er vegna þess að eitt fast hólf inniheldur ekki fullt innhreyfingarmagn.

    Þar sem þessi frágangur inniheldur hjáskipunarlínur sjást þrjár línur um vöruwrb  *-1001*:
    -  Take Line til að færa móttekið magn úr móttökuhólfinu (W-08-0001)
    -  Í stað línu fyrir 2 inn í hjáskipunarhólfi
    -  Í stað línu fyrir eftirstöðvar magns í geymsluhólfi

    4.  **Veljið aðgerðina frágangur**  skráningar.


6. Skilgreinið tínsluhólf fyrir vöruna sem á að stjórna þar sem hún er tekin frá 

    1.  Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 6.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.  Hvítt  *staðsetningarspjald er*  opnað.  
    3.  Velja skal  **aðgerðina hólf**  á  **birgðageymsluspjaldinu**
    4.  Velja hólf  *W-02-0001* og velja  **·**  síðan efnisaðgerðina.  
    5.  Valið er aðgerðin **Nýtt**.  
    6.   **Virkja fasta**  skipta.  
    7.  Í reitnum  **Vörunr.**  reit skal færa inn  *wrb-1000*. 
    8.   **Í mýrin magn**  - reit skal færa  *í 2*. 
    9.   **Í reitnum Hámarksmagn**  er fært inn  *10*. 

    Notaðu sérsniðsverkfærin ef  **Lágmótímagn**  og  **Hámarksmagn**  svæði eru ekki sýnileg. Sjá  [Sérsníða vinnusvæðið](../../ui-personalization-user.md) til að fá frekari upplýsingar. 

7. Endurskipuleggja vöruhús með því að færa vörur frá fjöldageymslusvæði yfir í tiltektarsvæði, til að hagræða tiltektartíma.

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 7.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn  **vinnublöð**  hreyfinga og veldu tengdan tengil
    2. Velja skal aðgerðina **Reikna áfyllingu hólfs**. 

    Vöruhúsavinnublaðið með tillögu um að flytja vöru  *wrb-1000*  frá magngeymslu til tínslusvæðis er stofnað.

    3.  **Veldu stofna hreyfingaraðgerð**  og staðfestu til að stofna skjalið.
    4.  Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 8](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Táknið, færa inn  **vöruhúsahreyfingar**  og velja tengdan tengil
    5.  Opna vöruhúsahreyfinguna sem þú stofnaðir, skoða  **kaflann línur** 

     Á þessu stigi er Break-magnvirknin ljós. Það verða fjórar línur:
    - Lína til að taka eina POKANN úr fjöldageymslumhólfi
    - Línu til að setja 48 PCS aftur í birgðir í sama hólfi. 
    - Línu til að taka 10 PCS út magngeymsluhólfi
    - Lína til að setja 10 PCS inn í tiltektarhólfið

    6.  Velja skal  **hreyfingaraðgerðina**  skrá.

8. Stofna vöruhúsatínslur

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 9](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Táknið, færa inn  **tínsluvinnublöð**  og velja tengdan tengil
    2. Velja skal  **aðgerðina Sækja vöruhúsaskjöl**, velja línuna fyrir sölupöntunina fyrir viðskiptavin 10000, og velja  **síðan OK**  hnappinn til að fylla vinnublaðslínurnar samkvæmt völdu skjali.

    3. Skoðið magn í  **reitnum hjáskipunarhólf** . 

    4. Veldu aðgerðina **Stofna tínslu**.
    5. Staðfesta þarf allar tínslustillingarnar, til dæmis virkja  **á milli skipta á svæði** . Velja hnappinn **Í lagi**.
    
    Þú færð staðfestingarpóst með tínslunúmerunum. Tvær hirslur eru til staðar eins og sumar vörur eru staðsettar á hjáskipunarsvæðinu, nálægt sendingarsvæði og það væri skynsamlegt að vinna þær sérstaklega.

9.  Skrá vöruhúsatínslur
    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 10](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Teiknið, Færið inn  **Vöruhúsatínslur**  og veljið tengdan tengil.
    2. Finndu tínslur sem þú stofnaðir og Opnaðu.
    3. Velja aðgerðina **Skrá tínslu**.
    4. Endurtakið seinni tínsluna

10. Bóka Vöruhúsaafhendinguna
    
    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 11](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Táknið, færa inn  **vöruhúsaafhendingu**  og velja tengdan tengil.
    2. Farið  **er eftir línunum**  á síðunni vöruhúsaafhending. Eftir að Vöruhúsatínsla er skráð verður vöruhúsaafhendingin uppfærð með  **magni til afhendingar** .
    3.  **Veljið aðgerðina Bóka sending** .
    4.  **Staðfestu möguleika skipsins** .


## <a name="results"></a><a name="results"></a>Niðurstöður
-  **bókuð vöruhúsamóttaka**  er stofnuð
- Búið er að  **Stofna skráðan vöruhúsafrágang**     
-  **Bókuð innkaupamóttaka**  er stofnuð    
-  **innkaupapöntunin**  er með magnið sem  **tekið**  var á móti uppfært fyrir línurnar sem fengu
-  **skráð vöruhúsahreyfing**  er stofnuð
-  **skráð Vöruhúsatínsla**  er stofnuð
-  **bókuð vöruhúsaafhending**  er stofnuð
-  **Bókuð söluafhending**  er stofnuð
-  **sölupöntunin**  er með magnið  **sem**  hefur verið uppfært fyrir línurnar sem voru afhentar
- Vörubirgðum  **·**  er fjölgað með hvaða afganga sem er ekki sendur út



## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Taka á móti vörum](../../warehouse-how-receive-items.md) 
[hönnun upplýsingar: vörur vöruflutningsvörur](../../design-details-inbound-warehouse-flow.md) 
[...](../../warehouse-how-ship-items.md) 
[á innleið tínsla vörur fyrir vöruhúsaafhendingshönnun](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[upplýsingar: flæði](../../design-details-outbound-warehouse-flow.md) 
[vöruhúss á útleið Skoða framboð vara](../../inventory-how-availability-overview.md) 
