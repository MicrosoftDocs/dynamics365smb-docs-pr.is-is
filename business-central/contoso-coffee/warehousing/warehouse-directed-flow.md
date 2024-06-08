---
title: 'Móttaka, frágangur, flutningur, tínsla og afhending í ítarlegri grunnstillingu vöruhúss'
description: 'Hægt er að framkvæma ferli á inn- og útleið á mismunandi hátt, allt eftir flóknara stigi vöruhússins.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 12/07/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Kynning á flæði á inn- og útleið í ítarlegri vöruhúsaskilgreiningu

Þessi kynning sýnir hvernig ljúka á inn- og útleiðarflæði í ítarlegri: Beinn frágangur og tínsla. Nánari upplýsingar eru í [Yfirlit um mismunandi skilgreiningarvalkosti](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Frumskilyrði  
Til að ljúka þessari kynningu þarf að gera notanda að vöruhúsastarfsmanni í birgðageymslunni WHITE *með* eftirfarandi skrefum:  
1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3. Í reitnum **Birgðageymslu kóði** færið inn HVÍTT.  
4. Gera sjálfgefna **ví6** virka.


## Aðstæður  
Ellen, yfirmaður vöruhússins notar hjáskipun og áfyllingu hólfa til að flýta móttöku- og afhendingartíma.  

## Skref

1. Stofna vöruhúsaafhendingu.  

    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 2.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Velja pöntun fyrir viðskiptavin 10000 fyrir birgðageymsluna HVÍTT. Ytri pöntun nr. er *W-1*.
    3. Velja skal aðgerðina **Stofna vöruhúsaafhendingu** til að stofna vöruhúsaafhendingu fyrir valda sölupöntun.
    4. Velja skal aðgerðina **Gefa út** til að tilkynna vöruhúsinu að söluafhendingin sé tilbúin til vöruhúsastjórnunar.  

2. Skilgreina hólf fyrir vöruna til að stjórna hvar frágangur hennar er. 

    1.   ![Veldu Lightbulb sem opnar Tell Me eiginleika 3.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
    2.   *WRB-1000* er valið og aðgerðin Innihald hólfs **valin** .  
    3.  Valið er aðgerðin **Nýtt**. Bætt er við tveimur línum.
    
    |Atriði|Staðsetningarkóði|Hólfkóði|Lagað|Mælieining|
    |----------|----------|---------|---|------|  
    |WRB-1000|HVÍTUR|W-05-0001|Já|POKI|  
    |WRB-1000|HVÍTUR|W-05-0002|Já|POKI|

3. Stofna vöruhúsamóttöku.  

    1.  ![Veldu Lightbulb sem opnar Tell Me eiginleika 4.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
    2. Veljið pöntun frá lánardrottni 10000 fyrir birgðageymsluna HVÍTT. Pöntun lánardr. nr. er *V-2*. Sérstillingartólin eru notuð ef reiturinn **Pöntunarnr. lánardrottins er notaður.** Reiturinn sést ekki. Nánari upplýsingar eru í [Sérstilla vinnusvæðið](../../ui-personalization-user.md).
    3. Veljið aðgerðina **Stofna vöruhúsamóttöku** til að stofna vöruhúsamóttöku fyrir valda innkaupapöntun.


4. Kanna hvort það eru útleiðarpantanir sem þarfnast móttekinna vara og bóka móttöku
    1. Veldu aðgerðina **Reikna út Hjáskipun**. Í þessum reit er dálkur **Magn til hjáskipunar**.
    2. 0 er fært inn í reitinn **Magn til hjáskipunar** í línunni með vörunni *WRB-1000* þar sem ekki er ætlunin að endurgreiða á móttökusvæðinu.
    3. Velja skal aðgerðina **Bóka móttöku** .

5. Vöruhúsafrágangur skráður
    1.  ![Notkun Lightbulb sem opnar Tell Me aðgerð 5.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **vöruhúsafrágang** og velja viðeigandi tengil.
    2. Vöruhúsafrágangsskjalið sem stofnað er í vöruhúsamóttökunni er fundið og það opnað
    3. Á síðunni **Vöruhúsafrágangur** skal fara yfir hlutann **Línur** 

    Á þessu stigi birtist rökfræði hólfagetunnar. Frágangslínur vöruhússins eru með þrjár línur fyrir vöruna *WRB-1000*:
    - Taka-línu til að færa móttekið magn úr móttökuhólfinu (W-08-0001)
    - Setjalína sem flytur einn poka í eitt af skilgreindu föstu hólfunum (W-05-0001)
    - Setjalína sem flytur annan poka í önnur föst hólf (W-05-0002). Það er vegna þess að eitt fast hólf getur ekki innihaldið fullt móttökumagn.

    Þar sem þessi frágangur inniheldur hjáskipunarlínur sjást þrjár línur fyrir vöruna *WRB-1001*:
    -  Taka-línu til að færa móttekið magn úr móttökuhólfinu (W-08-0001)
    -  Setjalínu fyrir 2 í hjáskipunarhólfið
    -  Setja-lína fyrir það magn sem eftir er í geymsluhólfi

    4. Velja skal aðgerðina **Skrá frágang** .


6. Skilgreina tínsluhólf fyrir vöruna til að stjórna því hvaðan hún er tínd úr 

    1.   ![Veldu Lightbulb sem opnar Tell Me aðgerð 6.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.  BirgðageymsluspjaldIÐ HVÍTT *er* opnað.  
    3.  Velja aðgerðina **Hólf** á **birgðageymsluspjaldinu**
    4.  Veljið hólfið *V-02-0001* og veljið svo **innihaldsaðgerðina** .  
    5.  Valið er aðgerðin **Nýtt**.  
    6.  Gera fasta **víxl virka** .  
    7.  Í reitnum Vörunr **.** er fært inn *WRB-1000*. 
    8.  Í reitnum **Lágm.magn** 2 *er fært inn*. 
    9.  Í reitinn **Hámarksmagn er fært** inn *10*. 

    Sérstillingar verkfærin eru notuð ef reiturinn **Lágm.magn er notaður.** og **Hámarksmagn** reitir sjást ekki. Nánari upplýsingar eru í [Sérstilla vinnusvæðið](../../ui-personalization-user.md). 

7. Endurskipuleggja vöruhús með því að færa vörur úr magngeymslusvæði yfir í tínslusvæði til að fínstilla tínslutíma.

    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 7.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **vinnublöð hreyfingar** og velja viðeigandi tengil
    2. Velja skal aðgerðina **Reikna áfyllingu hólfs**. 

    Vöruhúsavinnublaðið með tillögu um flutning á vöru *WRB-1000* úr magngeymslu í tínslusvæði er stofnað.

    3. Veljið aðgerðina **Stofna hreyfingu** og staðfestið að stofna skjalið.
    4.   ![Veldu Lightbulb sem opnar Tell Me aðgerð 8.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **vöruhúsahreyfingar** og velja viðeigandi tengil
    5.  Opna vöruhúsahreyfinguna sem stofnuð var, fara yfir hlutann **Línur** 

     Aðgerðin einingaskipt kemur í ljós á þessu stigi. Línurnar verða fjórar:
    - Lína til að taka einn poka út fyrir magngeymsluhólf
    - Lína til að setja 48 stk. aftur í birgðir í sama hólfi. 
    - Lína til að taka 10 stk. út magngeymsluhólf
    - Lína til að setja 10 stk. í tínsluhólfið

    6.  Velja skal aðgerðina **Skrá hreyfingu** .

8. Stofna vöruhúsatínslur

    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 9.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **tínsluvinnublöð** og velja viðeigandi tengil
    2. Veljið aðgerðina **Sækja vöruhúsaskjöl**, veljið línuna fyrir sölupöntunina fyrir viðskiptamann 10000 og veljið **svo Í lagi** til að fylla út vinnublaðslínurnar í samræmi við það skjal sem var valið.

    3. Skoða reitinn **Magn í hjáskipunarhólfi** . 

    4. Veldu aðgerðina **Stofna tínslu**.
    5. Staðfesta þarf þær tínslustillingar sem þarf, til dæmis, gera vífæringu á svæði frá svæði **virka** . Velja hnappinn **Í lagi**.
    
    Staðfestingarboð berast með tínslunúmerum. Tvær tínslur eru þar sem sumar vörur eru staðsettar á hjáskipunarsvæðinu, nálægt afhendingarsvæði og skynsamlegt væri að vinna þær sérstaklega.

9.  Skráning vöruhúsatínslu
    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 10.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **vöruhúsatínslu** og velja viðeigandi tengil.
    2. Tínslurnar sem stofnaðar voru og opnaðar eru fundnar.
    3. Velja aðgerðina **Skrá tínslu**.
    4. Endurtaka fyrir seinni tínsluna

10. Vöruhúsaafhending bókuð
    
    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 11.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vöruhúsaafhendingu** og velja viðeigandi tengil.
    2. Á vöruhúsaafhendingarsíðunni er hlutinn Línur **skoðaður** . Þegar vöruhúsatínslan hefur verið skráð verður vöruhúsaafhendingin uppfærð með reitnum **Magn til afhendingar** útfyllt.
    3. Velja skal aðgerðina **Bóka afhendingu** .
    4. Valkosturinn Afhenda **er** staðfestur.


## Niðurstöður
- Bókuð vöruhúsamóttaka **er** stofnuð
- skráði **vöruhúsafrágangurinn** er stofnaður    
-  **bókuð innkaupamóttaka** er stofnuð    
- Innkaupapöntunin **er** með móttekið **magn** fyrir mótteknar línur
-  **skráða vöruhúsahreyfingin** er stofnuð
-  **skráða vöruhúsatínslan** er stofnuð
-  **Bókuð vöruhúsaafhending** er stofnuð
-  **bókuð söluafhending** er stofnuð
- sölupöntunin **er** með **afhent magn uppfært** fyrir afhentar línur
- vörubirgðir **hækka** um afgang sem ekki hefur verið afhent



## Sjá einnig .
[Taka á móti vörum](../../warehouse-how-receive-items.md) 
[Hönnunarupplýsingar:  vöruhúsaflæði inn](../../design-details-inbound-warehouse-flow.md) 
[Senda vörur](../../warehouse-how-ship-items.md) 
[Tína vörur fyrir vöruhúsaafhendingu](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Hönnunarupplýsingar: vöruhúsaflæði á innleið](../../design-details-outbound-warehouse-flow.md) 
[Skoða tiltækileika vöru](../../inventory-how-availability-overview.md) 
