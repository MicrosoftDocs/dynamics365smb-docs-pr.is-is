---
title: Tínsla og Afhending í einfaldar grunngerðir vöruhúss
description: Í Business Central, er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214654"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

Í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Tínsla|Afhendingar|Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka tínslu og afhendingu frá pöntunarlínunni|X|||2|  
|Á|Bóka tínslu og afhendingu frá birgðatínsluskjali||X||3|  
|C|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali|||X|4/5/6|  
|D|Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali||X|X|4/5/6|  

Nánari upplýsingar má nálgast á [Hönnunarupplýsingar: vöruhúsaflæði á útleið](design-details-outbound-warehouse-flow.md)  

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.  

## <a name="about-this-walkthrough"></a>Um kynninguna

Í grunnvöruhúsi þar sem staðsetning er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota síðuna **Birgðatínsla** til að skrá og bóka tínslu og afhendingarupplýsingar fyrir upprunaskjöl á útleið. Upprunaskjalið á útleið getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið eða framleiðslupöntun með nauðsynlegum íhlutum.  

Þessi kynning fjallar um eftirfarandi verk:  

- Stilli staðsetningu SUÐUR fyrir birgðatínslu.  
- Stofna sölupöntun fyrir viðskiptamann 10000 fyrir 30 Amsterdam Lamps.  
- Gefur út sölupöntunina fyrir afgreiðslu vöruhúss.  
- Stofna birgðatínslu byggða á útgefnu upprunaskjali.  
- Skráir vöruhúsahreyfinguna frá vöruhúsinu og bókar á sama tíma söluafhendinguna fyrir upprunaskjal sölupöntunarinnar.  

## <a name="roles"></a>Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Yfirmaður vöruhúss  
- Pantanavinnsla  
- Starfsmaður í vöruhúsi  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a>Ferill

Stjórnandi vöruhússins hjá CRONUS setur upp SUÐUR-vöruhús fyrir grunntínslur þar sem starfsmenn vöruhússins meðhöndla pantanir á útleið hverja fyrir sig. Sá sem vinnur pantanir, býr til sölupöntun með 30 einingum af vöru 1928-S sem afgreiða á til viðskiptamanns 10000 úr SUÐUR vöruhúsinu. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins. Öllum tengdum verkum er stjórnað af John á síðunni **Birgðatínsla** sem sjálfkrafa vísar í hólfin þar sem 1928-S er geymt.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a>Uppsetning hólfakóða
Þegar staðsetningin hefur verið sett upp verður að bæta tveimur hólfum við.

#### <a name="to-setup-the-bin-codes"></a>Til að setja upp hólfakóðana

1. Veldu aðgerðina **Hólf**.
2. Búðu til tvö hólf, með kóðunum *S-01-0001* og *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a>Að gera sig að vöruhúsastarfsmanni á staðsetningunni SUÐUR

Til að nota þessa aðgerð verður þú að bæta við þig staðsetningu sem starfskraftur í vöruhúsi. 

#### <a name="to-make-yourself-a-warehouse-employee"></a>Til að gera þig að starfsmanni vöruhúss

  1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar fyrsta](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsmenn vöruhúss** og veldu síðan tengda tengilinn.  
  2. Veldu reitinn **Notandakenni** og síðan eigin notandareikning á síðunni **Starfsmaður vöruhúss**.
  3. Í reitnum **Staðsetningarkóði** velur þú SUÐUR.  
  4. Veldu reitinn **Sjálfgefið** og síðan hnappinn **Já**.  

### <a name="making-item-1928-s-available"></a>Gera hlut 1928-S tiltækan

Til að gera hlut 1928-S aðgengilegan á SUÐUR staðsetningunni skal fylgja þessum skrefum:  

  1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar annað](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðabækur** og veldu síðan tengda tengilinn.  
  2. Opnið sjálfgefnu færslubókina og stofnið tvær birgðabókarlínur með eftirfarandi upplýsingum um vinnudagsetninguna (Janúar 23).  

        |Tegund færslu|Vörunúmer|Kóti birgðageymslu |Hólfkóti|Magn|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Auking|1928-S|SUÐUR|S-01-0001|20|  
        |Auking|1928-S|SUÐUR|S-01-0002|20|  

        Sjálfgefið er að **Hólfakóði** á sölulínunni sé falinn og því þarf að kalla hann fram. Til að gera þetta þarftu að sérstilla síðuna. Frekari upplýsingar eru í [Hefja sérstillingu á síðu með borðanum Sérstilla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Veldu **Aðgerðir**, smelltu síðan á **Bókun** og smella síðan á **Bóka**.  
  4. Velja hnappinn **Já**.  

## <a name="creating-the-sales-order"></a>Stofna sölupöntunina

Sölupantanir eru algengasta tegundin af upprunaskjali á útleið.  

### <a name="to-create-the-sales-order"></a>Stofna sölupöntun

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar þriðja](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.  
3. Stofna sölupöntun fyrir viðskiptamann 10000 á vinnudeginum (23. Janúar) með eftirfarandi sölupöntunarlínu.  

    |Vara|Kóti birgðageymslu |Magn|  
    |----|-------------|--------|  
    |1928-S|SUÐUR|30|  

     Tilkynnið svo vöruhúsinu að sölupöntunin er tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.  

4. Valið er **Losa** aðgerð.  

    Haldið er áfram að taka til og senda seldar vörur.  

## <a name="picking-and-shipping-items"></a>Tínsla og afhending vara

Á síðunni **Birgðatínsla** er hægt að meðhöndla alla virkni vöruhúss á útleið fyrir tiltekið upprunaskjal, til dæmis sölupöntun. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Til að tína og senda vörur

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar fjórða](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðatínslur** og veldu síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.  

    Gakktu úr skugga um að **Nr.** reiturinn á flýtiflipanum **Almennt** er fylltur út.
3. Veljið reitinn **Upprunaskjal** og svo **Sölupöntun**.  
4. Veldu reitinn **Upprunanr.**, velja línuna fyrir sölu til viðskiptamanns 10000 og skal velja svo hnappinn **Í lagi**.  

    Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan sölupöntun.  
5. Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

    Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 20 í birgðatínslulínurnar tvær, í þeirri röð.  
6. Veldu aðgerðina **Bóka**, veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.  

    30 Amsterdam Lamps eru nú skráðir sem teknir til úr hólfum S-01-0001 og S-01-0002 er nú skráð og neikvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu söluafhendingu.  

## <a name="see-also"></a>Sjá einnig

[Vörur tíndar með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md)  
[Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Hönnunarupplýsingar: vöruhúsaflæði á innleið](design-details-outbound-warehouse-flow.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
