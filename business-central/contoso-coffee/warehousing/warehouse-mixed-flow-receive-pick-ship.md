---
title: 'Móttaka, Frágangur, Tínsla og Afhending í Blönduðum vöruhúsagrunnstillingu'
description: 'Í Business Central er hægt að framkvæma vinnslur á inn- og útleið á mismunandi hátt, allt eftir flækjustigi vöruhússins.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a>Kynning á flæði inn og út í blandað vöruhús grunnstillingar

Þessi kynning sýnir hvernig á að ljúka inn- og útleiðarflæði í blandaðri grunnstillingu þar sem vöruhús innleiðarflæðis er grunnstillt sem Grundvallaratriði: Pöntun-fyrir-pöntun og fyrir ítarlegt útflæði er notað. Nánari upplýsingar eru í [Yfirlit um mismunandi skilgreiningarvalkosti](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Frumskilyrði
Til að ljúka þessari kynningu þarf að gera notanda að vöruhúsastarfsmanni í *GULU* birgðageymslu með eftirfarandi skrefum:  
1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3.  **Gult er fært í** reitinn Kóti *birgðageymslu*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Innleiðarflæði: Móttaka og frágangur í einfaldri vöruhúsagrunnstillingu

Í [!INCLUDE[prod_short](../../includes/prod_short.md)] er hægt að framkvæma ferli á innleið fyrir móttöku og frágang á fjóra vegu með því að nota mismunandi aðgerðir eftir flóknara stigi vöruhúss.  

|Aðferð|Ferli á innleið|Hólf|Móttökur|Frágangur|Flækjustig (Sjá [Upplýsingar um hönnun: Vöruhúsauppsetning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|X|||2|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali|||X|3|  
|C|Bóka móttöku og frágang frá vöruhúsamóttökuskjali||X||4/5/6|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali||X|X|4/5/6|  

Nánari upplýsingar eru [í Hönnunarupplýsingar: Vöruhúsaflæði](../../design-details-inbound-warehouse-flow.md) á innleið.  

Eftirfarandi kynning sýnir aðferð C í fyrri töflu.  

### <a name="scenario"></a>Aðstæður
Alicia, innkaupaaðilinn, stofnar innkaupapantanir fyrir ýmsar steiktar baunir eins og eftirspurn birtist. Þegar sameinuð afhending kemur í vöruhúsið tekur Jón, starfsmaður vöruhússins, við og gengur frá vörunum. Þegar Jóhann bókar móttökuna eru vörurnar bókaðar sem mótteknar í birgðir og tiltækar til sölu eða annarrar eftirspurnar.  

### <a name="steps"></a>Skref
1. Setja upp síðuna **Birgðageymsluspjald** til að skilgreina vöruhúsaflæði inn í fyrirtækið.  

    1.   ![Veldu Lightbulb sem opnar Tell Me aðgerð 2.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.  Spjald gulu birgðageymslunnar *er* opnað.  
    3.  Gera þarf **frágangsáætlun** óvirka.  

2. Gefa út innkaupapantanir í vöruhús.  

    1.  ![Veldu Lightbulb sem opnar Tell Me eiginleika 3.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
    2. Velja pantanir frá lánardrottni 10000 fyrir gulu birgðageymsluna. Lánardrottnapantanir nr. eru *Y-1* og *Y-2*. Sérstillingartólin eru notuð ef reiturinn **Pöntunarnr. lánardrottins er notaður.** Reiturinn sést ekki. Nánari upplýsingar eru í [Sérstilla vinnusvæðið](../../ui-personalization-user.md).
    3. Veljið aðgerðina **Gefa út** til að tilkynna vöruhúsinu að valdar innkaupapantanir séu tilbúnar til afgreiðslu í vöruhúsi þegar afhendingin berst.  

3. Stofna vöruhúsamóttöku til móttöku og ganga frá afhentum vörum
    1.  ![Veldu Lightbulb sem opnar Tell Me eiginleika 4.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vöruhúsamóttökur** og velja viðeigandi tengil.
    2. Velja aðgerðina **Nýtt** 
    3. Á vöruhúsamóttökusíðunni er stutt á færslulykilinn til að velja vöruhúsamóttökunúmer sjálfkrafa
    4.  **Birgðageymslukótinn er** færður inn sem *GULUR*.
    5. Velja skal **Sækja upprunaskjöl...** Aðgerð
    6. Áður útgefnar innkaupapantanir frá lánardrottni 10000 eru valdar og hnappurinn **Í lagi** valinn.
        Í línunum verður ný færsla fyrir hverja innkaupapöntunarlínu.

4. Leiðrétta magn til móttöku samkvæmt mótteknu magni og bóka skjal
    1. Velja línu með vöru WRB-1000 *·*.
    2. Valið *er OVERRCPT10* í reitnum **Kóti** yfirmóttöku og gildi breytt í reitnum **Magn til móttöku** úr *100* í *110*.
    3. Velja línu með vöru *WRB-1001* og 
    4. Í annarri línu er gildi breytt í reitnum **Magn til móttöku** frá *200* til *190*.
    5. Velja skal aðgerðina **Bóka móttöku** .

### <a name="results"></a>Niðurstöður
 - Steiktar baunir eru nú skráðar sem frágengnar
 - Bókuð vöruhúsamóttaka **er** stofnuð
 -  **bókuð innkaupamóttaka** er stofnuð
 - Innkaupapöntunin er með móttekið **magn** fyrir mótteknar línur
 - vörubirgðir **hækka** um valið magn
    

## <a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a>Útleiðarflæði: Tínsla og afhending í ítarlegri vöruhúsagrunnstillingu

Í [!INCLUDE[prod_short](../../includes/prod_short.md)] er hægt að framkvæma ferla á útleið fyrir tínslu og afhendingu á fjóra vegu með mismunandi aðgerðum eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Tínsla|Afhendingar|Flækjustig (Sjá [Upplýsingar um hönnun: Vöruhúsauppsetning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka tínslu og afhendingu frá pöntunarlínunni|X|||2|  
|Á|Bóka tínslu og afhendingu frá birgðatínsluskjali||X||3|  
|C|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali|||X|4/5/6|  
|D|Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali||X|X|4/5/6|  

Nánari upplýsingar eru í [Hönnunarupplýsingar: Vöruhúsaflæði](../../design-details-outbound-warehouse-flow.md) á útleið.  

Eftirfarandi kynning sýnir aðferð D í fyrri töflu.

### <a name="scenario-1"></a>Aðstæður
Súsanna, pantanavinnslan, stofnar sölupantanir fyrir ýmsar steiktar baunir og sendir þær í vöruhúsið. Þegar allar pantanir koma frá sama viðskiptamanni ákveður Ellen, yfirmaður vöruhússins að senda þær saman. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins.

### <a name="steps-1"></a>Skref
Þetta er framhald af [flæði á innleið: Móttaka og frágangur í Grunnvöruhúsgrunnstillingum](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Gefa út sölupantanir í vöruhús.  

    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 5.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Velja pantanir fyrir viðskiptavin 10000 fyrir staðsetninguna GULUR. Ytri pantanir nr. eru *Y-3,Y-4* *og* *Y-5*.
    3. Veljið aðgerðina **Gefa út** til að tilkynna vöruhúsinu að valdar sölupantanir séu tilbúnar fyrir vöruhúsastjórnun.  

2. Vörur afhendar  
    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 6.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar** og velja síðan viðkomandi tengil.  
    2. Valið er aðgerðin **Nýtt**.  
    3.  **Gult er fært í** reitinn Kóti *birgðageymslu*.  
    4. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    5. CUST10000 er fært **í**  reitinn **Kóti**.  
    6. Í reitinn **Lýsing** er viðskiptamaður 10000 **færður** inn.  
    7. Velja aðgerðina **Breyta**.  
    8. Á flýtiflipanum **Sala** í reitnum **Selt-til viðskm.nr. Í reitinn Afmörkun** er fært inn *10000*.  
    9. Velja skal aðgerðina **Keyra**. 
    
    Vöruhúsaafhendingin er fyllt út með fjórum línum sem tákna sölupöntunarlínur fyrir tilgreindan viðskiptamann. Reiturinn **Magn til afhendingar** er auður því fyrst þarf að tína vörurnar.

3. Stofna vöruhúsatínslu úr vöruhúsaafhendingunni
    1. Á síðunni Vöruhúsaafhending er aðgerðin **Stofna tínslu** valin.
    2. Staðfesta þarf allar tínslustillingar sem þarf, til dæmis, velja *Vara* í reitnum **Röðunaraðferð fyrir aðgerðarlínu** til að flokka sömu vörur saman. Velja hnappinn **Í lagi**.
    3. Þú færð staðfestingarskilaboð með tínslunúmerinu. 

4. Vöruhúsatínsla er opnuð
    1.  ![Notkun Lightbulb sem opnar Tell Me aðgerð 7.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **vöruhúsatínslu** og velja viðeigandi tengil.
    2. Tínslan sem stofnuð var er fundin og hún opnuð.
    3. Uppfæra skal **Magn til afgreiðslu** ef þörf krefur.
    4. Velja aðgerðina **Skrá tínslu**.
    5. Vöruhúsatínslan lokast og verður fjarlægð ef allt magn er meðhöndlað.

5. Vöruhúsaafhending bókuð
   1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 8.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar** og velja síðan viðkomandi tengil.  
   2. Afhendingin sem stofnuð var er fundin og hún opnuð.
    Takið eftir að **útfyllt magn til afhendingar** .
    3. Hægt er að uppfæra **Bókunardags.**, **Númer utanaðk.** skjals,Flutningsaðilakóti,Flutningsmáti **·** **·**  ef þörf krefur. Gildi sem ekki eru tóm verða færð inn í upprunaskjöl.
    4. Velja skal aðgerðina **Bóka afhendingu** .
    5. Valkosturinn Afhenda **er** staðfestur.

### <a name="results-1"></a>Niðurstöður
 - Steiktar baunir eru nú skráðar sem tíndar 
 -  **skráða vöruhúsatínslan** er stofnuð
 -  **Bókuð vöruhúsaafhending** er stofnuð
 - Bókuðu söluafhendinguna **þrjár** eru stofnaðar
 - Sölupöntunin er með **afhent magn uppfært** fyrir afhentar línur
 - vörubirgðir **eru** minnkaðar um valið magn


## <a name="see-also"></a>Sjá einnig
[Receive Items](../../warehouse-how-receive-items.md)
[Set Up Basic Warehouses with Operations Areas](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Design Details: Inbound Warehouse Flow](../../design-details-inbound-warehouse-flow.md)
[Ship Items](../../warehouse-how-ship-items.md)
[Pick Items for Warehouse Shipment](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Design Details: Outbound Warehouse Flow](../../design-details-outbound-warehouse-flow.md)
[View the Availability of Items](../../inventory-how-availability-overview.md)
