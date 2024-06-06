---
title: 'Móttaka, Frágangur, Tínsla og Afhending í Grunngrunnstilling vöruhúss'
description: 'Í Business Central er hægt að framkvæma vinnslur á inn- og útleið á mismunandi hátt, allt eftir flækjustigi vöruhússins.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 02/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a>Kynning á flæði á inn- og útleið í Grunngrunnstilling vöruhúss

Þessi kynning sýnir hvernig ljúka á inn- og útleiðarflæði í grunnstillingunni: Pöntun-fyrir-pöntun. Nánari upplýsingar eru í [Yfirlit um mismunandi skilgreiningarvalkosti](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Frumskilyrði
Til að ljúka þessari kynningu þarf að gera notanda að vöruhúsastarfsmanni í birgðageymslunni *SILVER* með eftirfarandi skrefum:  
1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3. Í reitinn **Kóti** birgðageymslu er SILVER *slegið inn*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Innleiðarflæði: Móttaka og frágangur í einfaldri vöruhúsagrunnstillingu

Í [!INCLUDE[prod_short](../../includes/prod_short.md)] er hægt að framkvæma ferli á innleið fyrir móttöku og frágang á fjóra vegu með því að nota mismunandi aðgerðir eftir flóknara stigi vöruhúss.  

|Aðferð|Ferli á innleið|Hólf|Móttökur|Frágangur|Flækjustig (Sjá [Upplýsingar um hönnun: Vöruhúsauppsetning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|X|||2|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali|||X|3|  
|C|Bóka móttöku og frágang frá vöruhúsamóttökuskjali||X||4/5/6|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali||X|X|4/5/6|  

Nánari upplýsingar eru [í Hönnunarupplýsingar: Vöruhúsaflæði](../../design-details-inbound-warehouse-flow.md) á innleið.  

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.  

### <a name="scenario"></a>Aðstæður
Alicia, innkaupaaðilinn, stofnar innkaupapöntun fyrir ýmsar steiktar baunir. Þegar afhending berst í vöruhúsið gengur Jón, starfsmaður vöruhússins frá vörunum í hentug hólf. Þegar Jóhann bókar fráganginn eru vörurnar bókaðar sem mótteknar í birgðir og tiltækar til sölu eða annarrar eftirspurnar.  

### <a name="steps"></a>Skref
1. Setja upp síðuna **Birgðageymsluspjald** til að skilgreina vöruhúsaflæði inn í fyrirtækið.  

    1.   ![Veldu Lightbulb sem opnar Tell Me aðgerð 2.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.  Opna skal *birgðageymsluspjaldið SILVER* .  
    3.  Veljið gátreitinn **Þarf að ganga frá**.  

2. Skilgreina sjálfgefið hólf fyrir vöruna til að stjórna hvar hún er frágangur

    1.  Velja aðgerðina **Hólf** á **birgðageymsluspjaldinu**
    2.  Fyrsta línan er valin fyrir hólfið *R-1-01* og svo aðgerðin **Innihald** valið.  
    3.  Valið er aðgerðin **Nýtt**.  
    4.  Veljið **Fast** og svo **Sjálfgefið**.  
    5.  Í reitnum Vörunr **.** er fært inn *WRB-1000*.  

3. Innkaupapöntun, sem er algengasta tegund upprunaskjals á innleið.  

    1.   ![Veldu Lightbulb sem opnar Tell Me eiginleika 3.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
    2.  Valið er aðgerðin **Nýtt**.  
    3.  Stofna innkaupapöntun fyrir lánardrottin 10000 með eftirfarandi innkaupapöntunarlínum. Sérstillingarverkfærin eru notuð ef reiturinn **Hólfkóti** er ekki sýnilegur. Nánari upplýsingar eru í [Sérstilla vinnusvæðið](../../ui-personalization-user.md). 

    |Atriði|Staðsetningarkóði|Hólfkóði|Magn|  
    |----------|----------|---------|--------------|  
    |WRB-1000|SILFUR|S-1-01|20|  
    |WRB-1001|SILFUR||30|

    Hólfakótinn í fyrstu er fylltur út í samræmi við uppsetningu. Hólfakóti seinni vörunnar er auður þar sem hann hefur ekki sjálfgefin gildi. Hafðu það svona.  

    4.  Veljið aðgerðina **Gefa út** til að tilkynna vöruhúsinu að innkaupapöntunin sé tilbúin til afgreiðslu í vöruhúsi þegar afhending berst.  

4. Stofna **birgðafrágang** til móttöku og ganga frá afhentum vörum  

    1.  ![Veldu Lightbulb sem opnar Tell Me eiginleika 4.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðafrágangur** og velja síðan viðkomandi tengil.  
    2. Valið er aðgerðin **Nýtt**. 
    3. SILVER er valið *í reitnum* Birgðageymslukóti **.** 
    4. Veljið reitinn **Upprunaskjal** og svo **Innkaupapöntun**.  
    5. Reiturinn Upprunanúmer er valinn **.** er valin lína fyrir innkaup frá lánardrottni 10000 og síðan er hnappurinn **Í lagi** valinn til að fylla út frágangslínurnar í samræmi við það upprunaskjal sem valið var.

        Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan innkaupapöntunina.  

5. Breyta birgðafrágangi út frá raunverulegri setningu á vörum og bóka fylgiskjal

    Þegar vörur eru settar í hólf tekur Jóhann eftir sjálfgefnu hólfi sem þegar er búið að taka eftir nokkrum vörum og ákvað því að nota annað hólf. Jóhann setur einnig aðrar vörur í næstu hólf þar sem móttekið magn passar ekki við afkastagetuna.

    1. Í fyrstu línunni breytist **Hólfkóti úr** R-1-01 *·*, sem var afritaður úr innkaupapöntuninni, *í R-1-02*. 
    2.  20 er fært inn í reitinn **Magn til afgreiðslu** á birgðafrágangslínunni með vörunni WRB-1000.  
    3. Í annarri línu er 20 fært inn í reitinn **Magn til afgreiðslu** og aðgerðin Skipta línu **valin** . Ný lína birtist, eins og sú upphaflega, nema að reiturinn **Magn til afgreiðslu** er með magninu sem var fjarlægt úr upphaflegu línunni. 
    4. Hólfakótar eru fylltir út fyrir vöruna WRB-1001:

    |Atriði|Hólfkóði|Magn|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Veldu aðgerðina **Bóka**, veldu **Móttaka** aðgerðina og veldu síðan **Í lagi** hnappinn.  

### <a name="results"></a>Niðurstöður
 - Steiktar baunir eru nú skráðar sem frágengnar í tilgreindum hólfum
 - reiturinn **Bókaður birgðah. Frágangur** er stofnaður
 -  **bókuð innkaupamóttaka** er stofnuð
 - Innkaupapöntunin er með móttekið **magn** fyrir mótteknar línur
 - vörubirgðir **hækka** um valið magn
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a>Útleiðarflæði: Tínsla og afhending í Grunnvöruhúsgrunnstilling

Í [!INCLUDE[prod_short](../../includes/prod_short.md)] er hægt að framkvæma ferla á útleið fyrir tínslu og afhendingu á fjóra vegu með mismunandi aðgerðum eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Tínsla|Afhendingar|Flækjustig (Sjá [Upplýsingar um hönnun: Vöruhúsauppsetning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka tínslu og afhendingu frá pöntunarlínunni|X|||2|  
|Á|Bóka tínslu og afhendingu frá birgðatínsluskjali||X||3|  
|C|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali|||X|4/5/6|  
|D|Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali||X|X|4/5/6|  

Nánari upplýsingar eru í [Hönnunarupplýsingar: Vöruhúsaflæði](../../design-details-outbound-warehouse-flow.md) á útleið.  

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.

### <a name="scenario-1"></a>Aðstæður
Súsanna, pantanavinnslan, stofnar sölupöntun fyrir ýmsar steiktar baunir og sendir þær í vöruhús. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins. John hefur umsjón með öllum verkum á síðunni **Birgðatínsla** sem vísar sjálfkrafa á hólfin þar sem steiktar baunir eru geymdar.

### <a name="steps-1"></a>Skref
Þetta er framhald af [flæði á innleið: Móttaka og frágangur í Grunnvöruhúsgrunnstillingum](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Setja upp síðuna **Birgðageymsluspjald** til að skilgreina vöruhúsaflæði inn í fyrirtækið.  

    1.   ![Veldu Lightbulb sem opnar Tell Me aðgerð 5.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.  Opna skal *birgðageymsluspjaldið SILVER* .  
    3.  Veljið gátreitinn **Taka til**.  

2. Sölupöntunin er stofnuð, sem er algengasta tegund upprunaskjals á útleið.  

    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 6.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Valið er aðgerðin **Nýtt**.  
    3. Stofna sölupöntun fyrir viðskiptamann 10000 með eftirfarandi sölupöntunarlínu.  

    |Atriði|Kóði birgðageymslu|Magn|  
    |----|-------------|--------|  
    |WRB-1000|SILFUR|20|  
    |WRB-1001|SILFUR|30|  

    Hólfakótarnir eru fylltir sjálfkrafa með sjálfgefnum hólfum.

    4. Velja skal aðgerðina **Stofna birgðafrágang/tínslu** .
    5. Veljið gátreitinn **Stofna birgðatínslu**.  
    6. Velja hnappinn **Í lagi**. Ný birgðatínsla verður stofnuð.

3. Tína og senda vörur

    1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 7.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
    2. Velja birgðatínslu fyrir sölu til viðskiptamanns 10000
    
    Stofnaða birgðatínsluhólfið sem skilgreint var fyrir vöruna *WRB-1000* þar sem það er ekki með birgðum og notað annað hólf. Seinni línunum með vörunni *WRB-1001* var sjálfkrafa skipt í tínslu úr nokkrum hólfum.
    
4. Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

5. Veldu aðgerðina **Bóka**, veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.  

### <a name="results-1"></a>Niðurstöður
 - Steiktar baunir eru nú skráðar sem tíndar úr tilteknum hólfum
 - reiturinn **Bókaður birgðah. Tínsla** er stofnuð
 -  **bókuð söluafhending** er stofnuð
 - Sölupöntunin er með **afhent magn uppfært** fyrir afhentar línur
 - vörubirgðir **eru** minnkaðar um valið magn


## <a name="see-also"></a>Sjá einnig
[Frágangsvörur með birgðafráganga](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Setja upp grunnvöruhús með aðgerðasvæðum](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Hönnunarupplýsingar: Vöruhúsaflæði á innleið](../../design-details-inbound-warehouse-flow.md) 
[Tína vörur með birgðatínslu](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Hönnunarupplýsingar: Vöruhúsaflæði á útleið](../../design-details-outbound-warehouse-flow.md) 
[Skoða ráðstöfunarmagn vara](../../inventory-how-availability-overview.md) 
