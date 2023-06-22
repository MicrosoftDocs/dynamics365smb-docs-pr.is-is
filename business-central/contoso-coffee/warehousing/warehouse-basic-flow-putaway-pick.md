---
title: 'Móttaka, Frágangur, tiltekt og sendingu í grunnstillingu vöruhúss'
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

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations" />Ganga frá innflæði á innleið og útleið í grunnstillingum vöruhúss

Þessi gönguleið sýnir hvernig á að fylla út inn-og út streymi á Grunnunum: Skilgreining pöntunar eftir pöntun. Sjá  [Yfirlit yfir mismunandi skilgreiningarvalkosti fyrir frekari upplýsingar](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites" />Frumskilyrði
Til að ljúka þessu gönguleið þarftu að gera þig að vöruhúsastarfsmanni á  *silfurfati*  með því að fylgja þessum skrefum:  
1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 1.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3.  **Í reitinn Kóti birgðageymslu**  er fært inn  *silfur*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations" />Innflæði: Móttaka og frágangur í grunnstillingum vöruhúss

Í  [!INCLUDE[prod_short](../../includes/prod_short.md)], er hægt að framkvæma ferli á innleið fyrir móttöku og frágang á fjóra vegu eftir mismunandi virkni í vöruhúsinu, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Móttökur|Frágangur|Flókið stig (sjá  [hönnunarupplýsingar: Uppsetning](../../design-details-warehouse-setup.md) vöruhúss)|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|X|||2|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali|||X|3|  
|C|Bóka móttöku og frágang frá vöruhúsamóttökuskjali||X||4/5/6|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali||X|X|4/5/6|  

Nánari upplýsingar má finna  [í hönnunarupplýsingum: flæði](../../design-details-inbound-warehouse-flow.md) á innleið í vöruhúsi.  

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.  

### <a name="scenario" />Aðstæður
Alicia, innkaupastjóri, stofnar til innkaupapöntunar fyrir ýmsar roasted-baunir. Þegar sendingin kemur til vöruhúss hefur John, starfsmaður vöruhússins, gengið frá vörunum í svífandi hólfum. Þegar John bókar fráganginn eru vörurnar bókaðar sem mótteknar í birgðum og tiltækar til sölu eða annarrar eftirspurnar.  

### <a name="steps" />Skref
1. Setja upp  **Staðsetningarspjald**  á síðunni til að skilgreina innleiðarflæði fyrirtækisins.  

    1.  Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 2.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.   *Opna staðsetningarkort Silver* .  
    3.  Veljið gátreitinn **Þarf að ganga frá**.  

2. Skilgreinið sjálfgefið hólf fyrir vöruna sem á að stjórna þar sem hún er frágangð

    1.  Velja skal  **aðgerðina hólf**  á  **birgðageymsluspjaldinu**
    2.  Valin er fyrsta röðin, fyrir hólf  *S-1-01* og síðan valið  **·**  efnisaðgerðin.  
    3.  Valið er aðgerðin **Nýtt**.  
    4.  Veljið **Fast** og svo **Sjálfgefið**.  
    5.  Í reitnum  **Vörunr.**  reit skal færa inn  *wrb-1000*.  

3. Stofnið innkaupapöntunina sem er algengasta tegund upprunaskjals á innleið.  

    1.  Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 3.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
    2.  Valið er aðgerðin **Nýtt**.  
    3.  Stofnið innkaupapöntun fyrir lánardrottin 10000 með eftirfarandi innkaupapöntunarlínum. Notaðu sérsniðsverkfærin ef  **reiturinn Kóti hólfs**  er ekki sýnilegur. Sjá  [Sérsníða vinnusvæðið](../../ui-personalization-user.md) til að fá frekari upplýsingar. 

    |Vara|Staðsetningarkóði|Hólfkóti|Magn|  
    |----------|----------|---------|--------------|  
    |WRB-1000|SILVER|S-1-01|20|  
    |WRB-1001|SILVER||30|

    Hólfakótinn sem fyrstur er fylltur út er til samræmis við uppsetningu. Hólfkóti fyrir seinni vöru er auður þar sem hún hefur ekki sjálfgefin gildi. Haltu þessu áfram.  

    4.   **Veljið úttektaraðgerð**  til að láta vöruhúsið vita að innkaupapöntunin er tilbúin fyrir vöruhúsameðhöndlun þegar sending berst.  

4. Stofna  **birgðafrágang**  til að taka á móti og setja afhent atriði í burtu  

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 4.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðafrágangur** og velja síðan viðkomandi tengil.  
    2. Valið er aðgerðin **Nýtt**. 
    3. Valið  *er*  silfur  **í reitnum Kóti birgðageymslu** .
    4. Veljið reitinn **Upprunaskjal** og svo **Innkaupapöntun**.  
    5.  **Veljið Upprunnr.**  er valin línan fyrir innkaupin frá lánardrottni 10000 og síðan er  **hnappurinn í lagi**  valinn til að fylla frágangslínur samkvæmt völdu upprunaskjali.

        Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan innkaupapöntunina.  

5. Breyta frágangi byggða á raunverulegri vöru og bóka skjali

    Þegar vörur eru settar í hólf tekur John eftir sjálfgefnu hólfi þegar nokkur atriði hafa verið notuð svo hann ákvað að nota annað hólf. Jón setur einnig aðrar vörur í næsta hólf, þar sem móttekið magn fellur ekki að getu.

    1. Í fyrsta línukóta breyta  **hólfakóta**  úr  *s-1-01*, sem var afritaður úr innkaupapöntun, yfir í  *s-1-02*. 
    2.  Færið inn 20 í  **reitinn Magn til afgreiðslu**  í birgðafrágangslínunni með vöru wbr-1000.  
    3. Í annarri línunni skal slá inn 20 í  **reitinn Magn til afgreiðslu**  og velja  **skipta Línuaðgerð** . Ný lína birtist, eins og sú upphaflega, nema að reiturinn **Magn til afgreiðslu** er með magninu sem var fjarlægt úr upphaflegu línunni. 
    4. Kótar hólfa eru fylltir út fyrir vöru WBR-1001:

    |Vara|Hólfkóði|Magn|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Veldu aðgerðina **Bóka**, veldu **Móttaka** aðgerðina og veldu síðan **Í lagi** hnappinn.  

### <a name="results" />Niðurstöður
 - roasted-baunirnar eru nú skráðar sem frágangur í tilgreindum hólfum
 -  **bókaður Ívt.** Frágangur er búinn
 -  **Bókuð innkaupamóttaka**  er stofnuð
 - Innkaupapöntunin er með magnið sem  **tekið**  var á móti uppfært fyrir línurnar sem fengu
 - Vörubirgða  **·**  eykst eftir því sem valið magn
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations" />Flæði á útleið: tiltekt og sendingu í Grunnafbrigðum vöruhúsa

Í  [!INCLUDE[prod_short](../../includes/prod_short.md)] er hægt að framkvæma úttaferlin fyrir tiltekt og sendingu á fjóra vegu með því að nota mismunandi vinnslueiginleika, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Tínsla|Afhendingar|Flókið stig (sjá  [hönnunarupplýsingar: Uppsetning](../../design-details-warehouse-setup.md) vöruhúss)|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka tínslu og afhendingu frá pöntunarlínunni|X|||2|  
|Á|Bóka tínslu og afhendingu frá birgðatínsluskjali||X||3|  
|C|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali|||X|4/5/6|  
|D|Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali||X|X|4/5/6|  

Nánari upplýsingar er að finna  [í hönnunarupplýsingum: flæði](../../design-details-outbound-warehouse-flow.md) á útleið vöruhúss.  

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.

### <a name="scenario" />Aðstæður
Susan, pöntunarörgjörvinn, stofnar sölupöntun fyrir ýmsar roasted-baunir og sendir hana til vöruhúss. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins. John hefur umsjón með öllum þátt verka á  **síðunni Birgðatínsla**  sem bendir sjálfkrafa á hólfin þar sem roasted Beans eru geymdar.

### <a name="steps" />Skref
Þetta er framhald af  [innstreymissásinni: Móttaka og frágangur í Grunnvöruskilgreiningum](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Setja upp  **Staðsetningarspjald**  á síðunni til að skilgreina innleiðarflæði fyrirtækisins.  

    1.  Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 5.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
    2.   *Opna staðsetningarkort Silver* .  
    3.  Veljið gátreitinn **Taka til**.  

2. Stofnið sölupöntunina sem er algengasta tegund upprunaskjals á útleið.  

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 6.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
    2. Valið er aðgerðin **Nýtt**.  
    3. Stofnið sölupöntun fyrir viðskiptavin 10000 með eftirfarandi sölupöntunarlínu.  

    |Vara|Kóti birgðageymslu |Magn|  
    |----|-------------|--------|  
    |WRB-1000|SILVER|20|  
    |WRB-1001|SILVER|30|  

    Hólfakótarnir eru sjálfkrafa fylltir út með sjálfgefnum hólfum.

    4.  **Veljið aðgerðina stofna birgðafrágang/tínslu** .
    5. Veljið gátreitinn **Stofna birgðatínslu**.  
    6. Velja hnappinn **Í lagi**. Ný birgðatínsla verður stofnuð.

3. Taka til og senda vörur

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 7.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
    2. Velja birgðatínslu fyrir sölu til viðskiptavinar 10000
    
    Hólf fyrir stofnaða birgðatínslu var skilgreint fyrir vöruna  *wrb-1000*, þar sem hún inniheldur ekki birgðir og notar annað hólf. Seinni línunum, með Item  *wrb-1001*, var skipt sjálfkrafa til að velja úr nokkrum hólfum.
    
4. Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

5. Veldu aðgerðina **Bóka**, veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.  

### <a name="results" />Niðurstöður
 - roasted-baunirnar eru nú skrásettar sem tíndar úr tilgreindum hólfum
 -  **bókaður Ívt. Tínsla**  er stofnuð
 -  **Bókuð söluafhending**  er stofnuð
 - Sölupöntunin er með magnið  **sem**  hefur verið uppfært fyrir línurnar sem voru afhentar
 - Vörubirgðir  **·**  lækka um valið magn


## <a name="see-also" />Sjá einnig
[Frágangsatriði með birgðafrágangi](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Setja upp grunnvöruhús með aðgerðarsvæðum](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[hönnun upplýsingar: vörufráflæðisvörunarvörur](../../design-details-inbound-warehouse-flow.md) 
[á innleið í birgðahaldi](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[hönnunar upplýsingar: Skoða vöruhúsaflæði](../../design-details-outbound-warehouse-flow.md) 
[...](../../inventory-how-availability-overview.md) 
