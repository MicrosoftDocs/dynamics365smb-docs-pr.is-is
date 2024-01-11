---
title: 'Móttaka, leggja í burtu, flytja, tína og senda í háþróaðri vöruhúsastillingu'
description: Innleiðandi og útleið ferli er hægt að framkvæma á mismunandi hátt eftir því hversu flókið vöruhús er.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 12/07/2023
ms.author: bholtorf
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-advanced-warehouse-configuration"></a>Farið yfir inn- og útstreymi í háþróaðri vöruhúsastillingu

Þessi leið sýnir hvernig á að klára inn- og útstreymi í Advanced: Directed Put-away and Pick stillingunum. Fyrir frekari upplýsingar, sjá [Yfirlit yfir mismunandi stillingarvalkosti](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Frumskilyrði
Til að ljúka þessari leiðsögn þarftu að gera þig að vöruhússtarfsmanni á *WHITE* stað með því að fylgja þessum skrefum:  
1. Veldu ![peruna sem opnar Segðu mér eiginleikann 1.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3. Í reitnum **Birgðageymslu kóði** færið inn HVÍTT.  
4. Virkjaðu **Sjálfgefið** rofa.


## <a name="scenario"></a>Aðstæður
Ellen, vöruhússtjórinn notar virkni á milli bryggju og bakka til að flýta fyrir móttöku- og sendingartíma.  

## <a name="steps"></a>Skref

1. Búa til vöruhúsasendingu.  

    1. Veldu ![peruna sem opnar Segðu mér eiginleikann 2.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Veldu pöntun fyrir viðskiptavin 10000 fyrir HVÍTA staðsetninguna. Ytra pöntunarnúmer er *W-1*.
    3. Veldu  **Búa til vöruhúsasendingu** aðgerðina til að búa til vöruhúsasendingu fyrir valda sölupöntun.
    4. Veldu aðgerðina **Sleppa** til að tilkynna vöruhúsinu að sölusendingin sé tilbúin til vöruhúsameðferðar.  

2. Skilgreindu hólf fyrir hlutinn til að stjórna því hvar hún er sett í burtu 

    1.  Veldu ![peruna sem opnar Segðu mér eiginleikann 3.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
    2.  Veldu *WRB-1000* og veldu síðan **Hassainnihald** aðgerðina.  
    3.  Valið er aðgerðin **Nýtt**. Bættu við tveimur línum.
    
    |Atriði|Staðsetningarkóði|Hólfkóði|Lagað|Mælieining|
    |----------|----------|---------|---|------|  
    |WRB-1000|HVÍTUR|W-05-0001|Já|POKI|  
    |WRB-1000|HVÍTUR|W-05-0002|Já|POKI|

3. Búðu til vöruhúsakvittun.  

    1. Veldu ![peruna sem opnar Segðu mér eiginleikann 4.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
    2. Veldu pöntun frá seljanda 10000 fyrir HVÍTA staðsetninguna. Pöntunarnúmer seljanda er *W-2*. Notaðu sérstillingartækin ef **pöntunarnr.** Reiturinn sést ekki. Fyrir frekari upplýsingar, sjá [Sérsníða vinnusvæðið þitt](../../ui-personalization-user.md).
    3. Veldu aðgerðina **Búa til vöruhúsakvittun** til að búa til vöruhússkvittun fyrir valda innkaupapöntun.


4. Athugaðu hvort það séu pantanir á útleið sem þarfnast móttekinna vara og sendu inn móttöku
    1. Veldu aðgerðina **Reikna út Hjáskipun**. Þetta fyllir dálk **Magn. í Cross-Dock**.
    2. Sláðu inn 0 í **Magn. til Cross Dock** reitinn í línunni með hlut *WRB-1000* þar sem þú ætlar ekki að pakka aftur á móttökusvæðið.
    3. Veldu aðgerðina **Posta kvittun** .

5. Skráðu vörugeymsluna
    1. Notkun ![perunnar sem opnar Segðu mér eiginleikann 5.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Warehouse Put-Away** og veldu tengda hlekkinn.
    2. Finndu vöruhúsaflátsskjalið sem búið var til úr vöruhúsakvittun þinni og opnaðu það
    3. Farðu yfir **Línur** hlutann á **Warehouse Put-Away** síðunni

    Á þessu stigi er rökfræði geymslurýmisins ljós. Vöruhús frágangslínurnar hafa þrjár línur fyrir vöru *WRB-1000*:
    - A Taktu línu til að færa móttekið magn úr móttökutunnunni (W-08-0001)
    - Place lína sem færir einn BAG inn í einn af stilltum föstum hólfum (W-05-0001)
    - Place lína sem færir aðra BAG í aðra fasta bakka (W-05-0002). Þetta er vegna þess að ein föst bakka getur ekki innihaldið fullt innhreyfingarmagn.

    Vegna þess að þessi frágangur inniheldur krosslínur, sérðu þrjár línur fyrir hlut *WRB-1001*:
    -  A Taktu línu til að færa móttekið magn úr móttökutunnunni (W-08-0001)
    -  A Settu línu fyrir 2 í krossbryggjutunnuna
    -  A Settu línu fyrir það magn sem eftir er í geymsluhólf

    4. Veldu aðgerðina **Skrá frágang** .


6. Skilgreindu tínsluhólf fyrir vöruna til að stjórna hvaðan hún er tínd 

    1.  Veldu ![peruna sem opnar Segðu mér eiginleikann 6.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.  Opnaðu *HVÍTA* staðsetningarkortið.  
    3.  Veldu **Hassa** aðgerðina á **staðsetningarspjaldinu**
    4.  Veldu bin *W-02-0001* og veldu síðan **Content** aðgerðina.  
    5.  Valið er aðgerðin **Nýtt**.  
    6.  Virkjaðu **Föst** rofi.  
    7.  Í  **Vörunúmer** reitinn skaltu slá inn *WRB-1000*. 
    8.  Í reitnum **Min Magn.**, sláðu inn *2*. 
    9.  Í reitnum **Hámarksmagn**  skaltu slá inn *10*. 

    Notaðu sérstillingarverkfærin ef reitirnir **Lágmarksmagni** og **Hámarksmagni**  eru ekki sýnilegir. Fyrir frekari upplýsingar, sjá [Sérsníða vinnusvæðið þitt](../../ui-personalization-user.md). 

7. Endurskipuleggja vöruhús með því að færa hluti frá magngeymslusvæði yfir á tínslusvæði, til að hámarka tínslutíma.

    1. Veldu ![peruna sem opnar Segðu mér eiginleikann 7.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Hreyfingarvinnublöð** og veldu tengda hlekkinn
    2. Velja skal aðgerðina **Reikna áfyllingu hólfs**. 

    Vöruhúsablaðið með tillögu um að flytja hlut *WRB-1000* úr magngeymslu yfir á tínslusvæði er búið til.

    3. Veldu **Create Movement** aðgerðina og staðfestu til að búa til skjalið.
    4.  Veldu ![peruna sem opnar Segðu mér eiginleikann 8.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Vöruhúsahreyfingar** og veldu tengda hlekkinn
    5.  Opnaðu vöruhúsahreyfinguna sem þú bjóst til, skoðaðu **Línur** hlutann

     Á þessu stigi kemur í ljós brotavirknin. Það verða fjórar línur:
    - Lína til að taka eina BAG út lausageymslutunnuna
    - Lína til að setja 48 PCS aftur á lager í sömu tunnu. 
    - Lína til að taka 10 PCS úr lausageymslunni
    - Lína til að setja 10 PCS í tínslutunnuna

    6.  Veldu aðgerðina **Skráðu hreyfingu** .

8. Búðu til vöruhúsval

    1. Veldu ![peruna sem opnar Segðu mér eiginleikann 9.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Veldu vinnublöð** og veldu tengda hlekkinn
    2. Veldu aðgerðina **Fá vöruhúsaskjöl**, veldu línuna fyrir sölupöntun fyrir viðskiptavin 10000 og veldu síðan **Í lagi** hnappur til að fylla vinnublaðslínurnar í samræmi við valið skjal.

    3. Skoðaðu **Magn. á Cross-Dock Bin** vellinum. 

    4. Veldu aðgerðina **Stofna tínslu**.
    5. Staðfestu hvaða valstillingu sem þarf, til dæmis, virkjaðu **Per From Zone** skipta. Velja hnappinn **Í lagi**.
    
    Þú færð staðfestingarskilaboð með valnúmerunum. Það eru tveir valir þar sem sumir hlutir eru staðsettir á bryggjusvæðinu, nálægt sendingarsvæðinu, og það væri skynsamlegt að vinna þá sérstaklega.

9.  Skráðu vöruhúsvalið
    1. Veldu ![peruna sem opnar Segðu mér eiginleikann 10.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Vöruhúsval** og veldu tengda hlekkinn.
    2. Finndu valið sem þú bjóst til og opnaðu það.
    3. Velja aðgerðina **Skrá tínslu**.
    4. Endurtaktu fyrir seinni valið

10. Bókaðu vöruhúsasendinguna
    
    1. Veldu ![peruna sem opnar Segðu mér eiginleikann 11.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Vöruhúsasending** og veldu tengda hlekkinn.
    2. Farðu yfir **Línur** hlutann á vöruhúsafhendingarsíðunni. Eftir að vöruhúsvalið hefur verið skráð verður vöruhúsasendingin uppfærð með **Magn. til að skipa** fjölmennt.
    3. Veldu aðgerðina **Send sending** .
    4. Staðfestu **Send** valkostinn.


## <a name="results"></a>Niðurstöður
-  **Bókuð vöruhússkvittun** er búin til
-  **Skráð vöruhús frágangur** er búinn til    
-  **bókuð innkaupakvittun** er búin til    
-  **innkaupapöntunin** er með **magn móttekið** uppfært fyrir mótteknar línur
-  **Skráð vöruhúsahreyfing** er búin til
-  **Vöruhúsvalið** er búið til
-  **Bókuð vöruhúsasending** er búin til
-  **Bókuð sölusending** er búin til
-  **Sölupöntunin** er með **magn sent** uppfært fyrir sendar línur
- hluturinn **Birgð** hækkar um afgang sem ekki er sendur út



## <a name="see-also"></a>Sjá einnig .
[Fáðu hluti](../../warehouse-how-receive-items.md) 
[Hönnunarupplýsingar: Innleið vöruhúsaflæði](../../design-details-inbound-warehouse-flow.md) 
[Sendunarvörur](../../warehouse-how-ship-items.md) 
[Veldu vörur fyrir vöruhússendingu](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Hönnunarupplýsingar: Outbound Warehouse Flow](../../design-details-outbound-warehouse-flow.md) 
[Skoða framboð á hlutum](../../inventory-how-availability-overview.md) 
