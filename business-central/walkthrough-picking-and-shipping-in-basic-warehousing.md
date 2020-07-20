---
title: Tínsla og Afhending í Einfaldar grunngerð vöruhúss | Microsoft Docs
description: Í Business Central, er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: 475f32dbaf9b4b80a61e1cad542fbf6db79cb029
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528311"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

Í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.  

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

- Stilli SILVER staðsetningu fyrir birgðatínslu.  
- Stofna sölupöntun fyrir viðskiptamann 10000 fyrir 30 hátalara.  
- Gefur út sölupöntunina fyrir afgreiðslu vöruhúss.  
- Stofna birgðatínslu byggða á útgefnu upprunaskjali.  
- Skráir vöruhúsahreyfinguna frá vöruhúsinu og bókar á sama tíma söluafhendinguna fyrir upprunaskjal sölupöntunarinnar.  

## <a name="roles"></a>Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Yfirmaður vöruhúss  
- Pantanavinnsla  
- Starfsmaður í vöruhúsi  

## <a name="prerequisites"></a>Frumskilyrði

Til að ljúka þessari kynningu þarf:  

- Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á netinu byggir fyrirtæki á **Ítarlegt mat - Heildarsýnigögn** valkostinn í sandkassaumhverfi. Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] innanhúss premises, CRONUS International Ltd. uppsett.  
- Til að gera þig að starfsmanni vöruhúss í SILVER staðsetningu skal fylgja eftirfarandi skrefum:  

  1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsmenn vöruhúss** og veldu síðan tengda tengilinn.  
  2. Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
  3. Í reitnum **Staðsetningarkóði** er fært inn SILVER.  
  4. Veljið reitinn **Sjálfgefið**.  

- Gerið vöru LS-81 tiltæka í SILFUR staðsetningu á eftirfarandi hátt:  

  1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðabækur** og veldu síðan tengda tengilinn.  
  2. Opnið sjálfgefnu færslubókina og stofnið tvær birgðabókarlínur með eftirfarandi upplýsingum um vinnudagsetninguna (Janúar 23).  

        |Tegund færslu|Vörunúmer|Kóti birgðageymslu |Hólfkóti|Magn|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Auking|LS-81|SILVER|S-01-0001|20|  
        |Auking|LS-81|SILVER|S-01-0002|20|  

  3. Valið er **bóka** aðgerð og síðan hnappinn **Já**.  

## <a name="story"></a>Ferill

Stjórnandi vöruhússins hjá CRONUS setur upp SILVER-vöruhúss fyrir grunntínslur þar sem starfsmenn vöruhússins meðhöndla pantanir á útleið hverja fyrir sig. Sá sem vinnur pantanir, býr til sölupöntun með 30 einingum af vöru LS-81 sem afgreiða á til viðskiptamanns 10000 úr SILVER vöruhúsinu. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins. Öllum tengdum verkum er stjórnað af John á síðunni **Birgðatínsla** sem sjálfkrafa vísar í hólfin þar sem LS-81 er geymt.  

## <a name="setting-up-the-location"></a>Uppsetning staðsetningarinnar

Uppsetning síðunnar **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.  

### <a name="to-set-up-the-location"></a>Uppsetning staðsetningar

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.  
2. SILVER-staðsetningarspjaldið er opnað.  
3. Á flipanum **Vöruhús** skal velja gátreitinn **Krefjast tínslu**.  

## <a name="creating-the-sales-order"></a>Stofna sölupöntunina

Sölupantanir eru algengasta tegundin af upprunaskjali á útleið.  

### <a name="to-create-the-sales-order"></a>Stofna sölupöntun

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.  
3. Stofna sölupöntun fyrir viðskiptamann 10000 á vinnudeginum (23. Janúar) með eftirfarandi sölupöntunarlínu.  

    |Vara|Kóti birgðageymslu |Magn|  
    |----|-------------|--------|  
    |LS_81|SILVER|30|  

     Tilkynnið svo vöruhúsinu að sölupöntunin er tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.  

4. Valið er **Losa** aðgerð.  

    Haldið er áfram að taka til og senda seldar vörur.  

## <a name="picking-and-shipping-items"></a>Tínsla og afhending vara

Á síðunni **Birgðatínsla** er hægt að meðhöndla alla virkni vöruhúss á útleið fyrir tiltekið upprunaskjal, til dæmis sölupöntun. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Til að tína og senda vörur

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðatínslur** og veldu síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.  

    Gakktu úr skugga um að **Nr.** reiturinn á flýtiflipanum **Almennt** er fylltur út.
3. Veljið reitinn **Upprunaskjal** og svo **Sölupöntun**.  
4. Veldu reitinn **Upprunanr.**, velja línuna fyrir sölu til viðskiptamanns 10000 og skal velja svo hnappinn **Í lagi**.  

    Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan sölupöntun.  
5. Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

    Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 20 í birgðatínslulínurnar tvær, í þeirri röð.  
6. Veldu aðgerðina **Bóka**, veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.  

    Tínsla hátalaranna 30 úr hólfum S-01-0001 og S-01-0002 er nú skráð og neikvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu söluafhendingu.  

## <a name="see-also"></a>Sjá einnig

[Vörur tíndar með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md)  
[Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Hönnunarupplýsingar: vöruhúsaflæði á innleið](design-details-outbound-warehouse-flow.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
