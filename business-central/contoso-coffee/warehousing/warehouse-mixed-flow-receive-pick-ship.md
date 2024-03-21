---
title: 'Móttaka, Frágangur, tiltekt og sendingar í Blönduðum vörugeymslum samskipa'
description: Á viðskipta-miðlægum er hægt að framkvæma inn-og úttaflana á mismunandi hátt eftir því hversu flókið það er í vöruhúsinu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a>Vasaljós á inn-og útrennsli í Blönduðum Vöruhúsaleiðingum

Þessi gönguleið sýnir hvernig á að fylla út inn-og út streymi í blandaðri skilgreiningu, þar sem fyrir vöruhús innstreymis er skilgreint sem grunnur: pöntun-eftir-pöntun og fyrir ítarlegri samskipan á útleið er notuð. Sjá  [Yfirlit yfir mismunandi skilgreiningarvalkosti fyrir frekari upplýsingar](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Frumskilyrði
Til að ljúka við þetta gönguleið þarftu að gera vöruhúsastarfsmann á  *gulum*  stað með því að fylgja þessum skrefum eftir:  
1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 1.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3.  **Í reitinn Kóti birgðageymslu**  er fært inn  *gult*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Innflæði: Móttaka og frágangur í grunnstillingum vöruhúss

Í  [!INCLUDE[prod_short](../../includes/prod_short.md)], er hægt að framkvæma ferli á innleið fyrir móttöku og frágang á fjóra vegu eftir mismunandi virkni í vöruhúsinu, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Móttökur|Frágangur|Flókið stig (sjá  [hönnunarupplýsingar: Uppsetning](../../design-details-warehouse-setup.md) vöruhúss)|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|X|||2|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali|||X|3|  
|C|Bóka móttöku og frágang frá vöruhúsamóttökuskjali||X||4/5/6|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali||X|X|4/5/6|  

Nánari upplýsingar má finna  [í hönnunarupplýsingum: flæði](../../design-details-inbound-warehouse-flow.md) á innleið í vöruhúsi.  

Eftirfarandi walkmeð sýndi aðferð C í fyrri töflunni.  

### <a name="scenario"></a>Aðstæður
Alicia, innkaupastjóri, stofnar innkaupapantanir fyrir ýmsar roasted-baunir eins og eftirspurn virðist. Þegar sameinuð afhending kemur í vöruhúsið, tekur John, starfsmaður vöruhússins, á móti og setur vörurnar í burtu. Þegar John bókar kvittunina eru vörurnar bókaðar sem mótteknar í birgðum og tiltækar til sölu eða annarrar eftirspurnar.  

### <a name="steps"></a>Skref
1. Setja upp  **Staðsetningarspjald**  á síðunni til að skilgreina innleiðarflæði fyrirtækisins.  

    1.  Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 2.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.   *Opnaðu gulu*  staðsetningarspjaldið.  
    3.   **Gera þarf skiptistað**  óvirkan.  

2. Losa innkaupapantanir í vöruhús.  

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 3.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
    2. Velja pantanir frá lánadrottnum 10000 fyrir GULA staðinn. Pantanir lánardrottins eru  *Y-1*  og  *Y-2*. Notaðu sérsniðsverkfærin ef  **Pöntunarnr.** Svæði ekki sýnilegt. Sjá  [Sérsníða vinnusvæðið](../../ui-personalization-user.md) til að fá frekari upplýsingar.
    3.  **Veljið úttektaraðgerð**  til að láta vöruhúsið vita að valdar innkaupapantanir séu tilbúnar fyrir vöruhúsameðhöndlun þegar sending berst.  

3. Vöruhúsamóttakan stofnuð til að taka á móti og senda afhendið vörur í burtu
    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 4.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **vöruhúsamóttökur**  og velja tengdan tengil.
    2.  **Velja nýju**  aðgerðina
    3. Á síðunni vöruhúsamóttaka er stutt á færslulykilinn til að hafa valið sjálfvirkt innhreyfingarnúmer vöruhúss
    4. Kóti  **birgðageymslu er**  færður inn sem  *gulur*.
    5.  **Veldu sækja upprunaskjöl...** aðgerð
    6. Velja áður útgefnar innkaupapantanir úr lánardr. 10000 og velja hnappinn í  **lagi** .
        Í línunum verður ný færsla fyrir hverja innkaupapöntunarlínu.

4. Leiðrétta magn til innhreyfingar á grundvelli móttekinna magns og bóka skjals
    1. Veldu línu með Item  *wrb-1000*.
    2. Veljið  *OVERRCPT10*  í  **reitnum yfir-móttökukóti**  og breyið  **gildinu í magninu sem á að taka á móti**  í reitnum  *100*  til  *110*.
    3. Velja línu með Item  *wrb-1001*  og 
    4. Í annarri línu skal breyta gildinu í  **magninu sem á að taka á móti**  reit frá  *200*  til  *190*.
    5.  **Veljið aðgerðina Bóka kvittun** .

### <a name="results"></a>Niðurstöður
 - roasted-baunirnar eru nú skrásettar sem frágangur
 -  **bókuð vöruhúsamóttaka**  er stofnuð
 -  **Bókuð innkaupamóttaka**  er stofnuð
 - Innkaupapöntunin er með magnið sem  **tekið**  var á móti uppfært fyrir línurnar sem fengu
 - Vörubirgða  **·**  eykst eftir því sem valið magn
    

## <a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a>Flæði á útleið: tiltekt og sendingu í ítarlegum Vöruhúsafbrigðum

Í  [!INCLUDE[prod_short](../../includes/prod_short.md)] er hægt að framkvæma úttaferlin fyrir tiltekt og sendingu á fjóra vegu með því að nota mismunandi vinnslueiginleika, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Tínsla|Afhendingar|Flókið stig (sjá  [hönnunarupplýsingar: Uppsetning](../../design-details-warehouse-setup.md) vöruhúss)|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka tínslu og afhendingu frá pöntunarlínunni|X|||2|  
|Á|Bóka tínslu og afhendingu frá birgðatínsluskjali||X||3|  
|C|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali|||X|4/5/6|  
|D|Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali||X|X|4/5/6|  

Nánari upplýsingar er að finna  [í hönnunarupplýsingum: flæði](../../design-details-outbound-warehouse-flow.md) á útleið vöruhúss.  

Eftirfarandi kynning sýnir aðferð D í fyrri töflu.

### <a name="scenario-1"></a>Aðstæður
Susan, pöntunarörgjörvinn, stofnar sölupantanir fyrir ýmsar roasted-baunir og sendir í vöruhús. Eftir því sem allar pantanir koma frá sama viðskiptavini, þá ákveður Ellen, vöruhússtjórinn að skipa þeim saman. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins.

### <a name="steps-1"></a>Skref
Þetta er framhald af  [innstreymissásinni: Móttaka og frágangur í Grunnvöruskilgreiningum](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Sleppa sölupöntunum í vöruhús.  

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 5.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Velja pantanir fyrir viðskiptavin 10000 fyrir GULA staðinn. Ytri pantanir nr eru  *y-3*,  *y-4*, og  *Y-5*.
    3.  **Veljið úttektaraðgerð**  til að láta vöruhúsið vita að valdar sölupantanir séu tilbúnar fyrir meðhöndlun vöruhúss.  

2. Til að senda vörur  
    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 6.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar** og velja síðan viðkomandi tengil.  
    2. Valið er aðgerðin **Nýtt**.  
    3.  **Í reitinn Kóti birgðageymslu**  er fært inn  *gult*.  
    4. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    5.  **Í reitnum kóti**  er fært inn  **CUST10000**.  
    6.  **Í reitinn Lýsing**  er færður inn  **Viðskiptamaður 10000**.  
    7. Velja aðgerðina **Breyta**.  
    8.  **Á flipanum sölufastinn**  í reitnum  **Selt-til viðskm. Afmörkun**  reits er færður  *10000*.  
    9. Velja skal aðgerðina **Keyra**. 
    
    Vöruhúsaafhendingin er fyllt með fjórum línum sem tákna sölupöntunarlínur fyrir tilgreindan viðskiptavin.  **Reiturinn Magn til sendingar**  er auður, sem vörur þarf að taka til fyrst.

3. Stofna Vöruhúsatínsluna úr vöruhúsaafhendingunni
    1. Á síðunni vöruhúsaafhending er valið  **aðgerðina stofna tínslu** .
    2. Staðfesta þarf allar tínslustillingarnar, til dæmis, velja  *atriði*  í  **röðunaraðferðinni fyrir aðgerðarlínustillingu**  til að flokka sömu vörur saman. Velja hnappinn **Í lagi**.
    3. Þú færð staðfestingarpóst með tínslunúmerinu. 

4. Vöruhús-tiltekt opnuð
    1. Notkun á ljósaperu  ![sem opnast Segðu mér lögun 7.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **Vöruhúsatínslur**  og veljið tengdan tengil.
    2. Finndu tínsluna sem þú stofnaðir og Opnaðu.
    3.  **Uppfærið magn til afgreiðslu**  ef þörf krefur.
    4. Velja aðgerðina **Skrá tínslu**.
    5. Vöruhúsatiltekt mun loka og vera fjarlægð ef allt magnið er afgreitt.

5. Bóka Vöruhúsaafhendinguna
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 8.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar** og velja síðan viðkomandi tengil.  
   2. Finndu sendinguna sem þú stofnaðir áður og Opnaðu hana.
    Takið eftir að  **Magn til sendingar**  er móttekið.
    3. Hægt er að uppfæra  **bókunardagsetningu**,  **númer utanaðkomandi skjals**,  **kóta** flutningsaðila og  **sendingarmáta**  ef þörf krefur. Gildi sem ekki eru tóm verða sett saman við upprunaskjöl.
    4.  **Veljið aðgerðina Bóka sending** .
    5.  **Staðfestu möguleika skipsins** .

### <a name="results-1"></a>Niðurstöður
 - roasted-baunirnar eru nú skráðar sem tíndar 
 -  **skráð Vöruhúsatínsla**  er stofnuð
 -  **bókuð vöruhúsaafhending**  er stofnuð
 - Búið er að stofna þrjár  **Bókaðar söluafhendingar** 
 - Sölupöntunin er með magnið  **sem**  hefur verið uppfært fyrir línurnar sem voru afhentar
 - Vörubirgðir  **·**  lækka um valið magn


## <a name="see-also"></a>Sjá einnig
[Receive Items](../../warehouse-how-receive-items.md)
[Set Up Basic Warehouses with Operations Areas](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Design Details: Inbound Warehouse Flow](../../design-details-inbound-warehouse-flow.md)
[Ship Items](../../warehouse-how-ship-items.md)
[Pick Items for Warehouse Shipment](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Design Details: Outbound Warehouse Flow](../../design-details-outbound-warehouse-flow.md)
[View the Availability of Items](../../inventory-how-availability-overview.md)
