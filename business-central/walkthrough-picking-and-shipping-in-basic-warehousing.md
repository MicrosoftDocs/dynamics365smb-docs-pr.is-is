---
title: Tínsla og Afhending í einfaldar grunngerðir vöruhúss
description: Í þessari grein er lýst ýmsum stigum margbreytileika í tínslu-og skipaferlum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
ms.service: dynamics-365-business-central
---
# Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru tínsla og sendingarvara notuð með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínslu og sendingu úr pöntunarlínu|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: pöntun-eftir pöntun.|  
|U|Bóka tínslu og sendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bókið tínsluna úr vöruhúsatínsluskjali og bókið sendinguna úr afhendingarskjali vöruhúss|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar á útdragandi [Vöruhúsaklæðum](design-details-outbound-warehouse-flow.md).

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.  

## Um kynninguna

Í grunnvöruhúsi þar sem staðsetning er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota síðuna **Birgðatínsla** til að skrá og bóka tínslu og afhendingarupplýsingar fyrir upprunaskjöl á útleið. Upprunaskjalið á útleið getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið eða framleiðslupöntun með nauðsynlegum íhlutum.  

Þessi kynning fjallar um eftirfarandi verk:  

- Stilli staðsetningu SUÐUR fyrir birgðatínslu.  
- Stofna sölupöntun fyrir viðskiptamann 10000 fyrir 30 Amsterdam Lamps.  
- Gefur út sölupöntunina fyrir afgreiðslu vöruhúss.  
- Stofna birgðatínslu byggða á útgefnu upprunaskjali.  
- Skráir vöruhúsahreyfinguna frá vöruhúsinu og bókar á sama tíma söluafhendinguna fyrir upprunaskjal sölupöntunarinnar.  

## Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Yfirmaður vöruhúss  
- Pantanavinnsla  
- Starfsmaður í vöruhúsi  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## Ferill

Stjórnandi vöruhússins hjá CRONUS setur upp SUÐUR-vöruhús fyrir grunntínslur þar sem starfsmenn vöruhússins meðhöndla pantanir á útleið hverja fyrir sig. Sá sem vinnur pantanir, býr til sölupöntun með 30 einingum af vöru 1928-S sem afgreiða á til viðskiptamanns 10000 úr SUÐUR vöruhúsinu. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins. Öllum tengdum verkum er stjórnað af John á síðunni **Birgðatínsla** sem sjálfkrafa vísar í hólfin þar sem 1928-S er geymt.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### Uppsetning hólfakóða

Þegar staðsetningin hefur verið sett upp verður að bæta tveimur hólfum við.

#### Til að setja upp hólfakóðana

1. Veldu aðgerðina **Hólf**.
2. Búðu til tvö hólf, með kóðunum *S-01-0001* og *S-01-0002*.

### Að gera sig að vöruhúsastarfsmanni á staðsetningunni SUÐUR

Til að nota þessa aðgerð verður þú að bæta við þig staðsetningu sem starfskraftur í vöruhúsi. 

#### Til að gera þig að starfsmanni vöruhúss

  1. Veldu táknið ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
  2. Veldu reitinn **Notandakenni** og síðan eigin notandareikning á síðunni **Starfsmaður vöruhúss**.
  3. Í reitnum **Staðsetningarkóði** velur þú SUÐUR.  
  4. Veldu reitinn **Sjálfgefið** og síðan hnappinn **Já**.  

### Gera hlut 1928-S tiltækan

Til að gera hlut 1928-S aðgengilegan á SUÐUR staðsetningunni skal fylgja þessum skrefum:  

  1. Veldu ![Ljósapera sem opnar annan eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.  
  2. Opnið sjálfgefnu færslubókina og stofnið tvær birgðabókarlínur með eftirfarandi upplýsingum um vinnudagsetninguna (Janúar 23).  

        |Tegund færslu|Vörunúmer|Kóti birgðageymslu |Hólfkóti|Magn|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Auking|1928-S|SUÐUR|S-01-0001|20|  
        |Auking|1928-S|SUÐUR|S-01-0002|20|  

        Sjálfgefið er að **Hólfakóði** á sölulínunni sé falinn og því þarf að kalla hann fram. Til að gera þetta þarftu að sérstilla síðuna. Nánari upplýsingar er að finna  [í til að ræsa sérsníða síðu í gegnum fylgiritið](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

  3. Veldu **Aðgerðir**, smelltu síðan á **Bókun** og smella síðan á **Bóka**.  
  4. Velja hnappinn **Já**.  

## Stofna sölupöntunina

Sölupantanir eru algengasta tegundin af upprunaskjali á útleið.  

### Stofna sölupöntun

1. Veldu ![Ljósapera sem opnar þriðja eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Stofna sölupöntun fyrir viðskiptamann 10000 á vinnudeginum (23. Janúar) með eftirfarandi sölupöntunarlínu.  

    |Vara|Kóti birgðageymslu |Magn|  
    |----|-------------|--------|  
    |1928-S|SUÐUR|30|  

     Tilkynnið svo vöruhúsinu að sölupöntunin er tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.  

4. Valið er **Losa** aðgerð.  

    Haldið er áfram að taka til og senda seldar vörur.  

## Tínsla og afhending vara

Á síðunni **Birgðatínsla** er hægt að meðhöndla alla virkni vöruhúss á útleið fyrir tiltekið upprunaskjal, til dæmis sölupöntun. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### Til að tína og senda vörur

1. Veldu ![Ljósapera sem opnar fjórða eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  

    Gakktu úr skugga um að **Nr.** reiturinn á flýtiflipanum **Almennt** er fylltur út.
3. Veljið reitinn **Upprunaskjal** og svo **Sölupöntun**.  
4. Veldu reitinn **Upprunanr.**, velja línuna fyrir sölu til viðskiptamanns 10000 og skal velja svo hnappinn **Í lagi**.  

    Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan sölupöntun.  
5. Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

    Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 20 í birgðatínslulínurnar tvær, í þeirri röð.  
6. Veldu aðgerðina **Bóka**, veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.  

    30 Amsterdam Lamps eru nú skráðir sem teknir til úr hólfum S-01-0001 og S-01-0002 er nú skráð og neikvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu söluafhendingu.  

## Sjá einnig .

[Vörur tíndar með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md)  
[Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Hönnunarupplýsingar: vöruhúsaflæði á innleið](design-details-outbound-warehouse-flow.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
