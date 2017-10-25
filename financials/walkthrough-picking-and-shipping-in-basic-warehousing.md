---
title: "Kynning -Tínsla og Afhending í Einfaldar grunngerð vöruhúss | Microsoft Docs"
description: "Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 993d3f092db9f423aba9a67d58f53895df0d5c2f
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss
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
Í grunnvöruhúsi þar sem staðsetning er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota gluggann **Birgðatínsla** til að skrá og bóka tínslu og afhendingarupplýsingar fyrir upprunaskjöl á útleið. Upprunaskjalið á útleið getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið eða framleiðslupöntun með nauðsynlegum íhlutum.  

Þessi kynning fjallar um eftirfarandi verk:  

-   Stilli SILVER staðsetningu fyrir birgðatínslu.  
-   Stofna sölupöntun fyrir viðskiptamann 10000 fyrir 30 hátalara.  
-   Gefur út sölupöntunina fyrir afgreiðslu vöruhúss.  
-   Stofna birgðatínslu byggða á útgefnu upprunaskjali.  
-   Skráir vöruhúsahreyfinguna frá vöruhúsinu og bókar á sama tíma söluafhendinguna fyrir upprunaskjal sölupöntunarinnar.  

## <a name="roles"></a>Hlutverk  
Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

-   Yfirmaður vöruhúss  
-   Pantanavinnsla  
-   Starfsmaður í vöruhúsi  

## <a name="prerequisites"></a>Frumskilyrði  
Til að ljúka þessari kynningu þarf:  

-   CRONUS  International Ltd. er uppsett.  
-   Til að gera notanda að starfsmanni vöruhúss í SILVER staðsetningu á eftirfarandi hátt:  

    1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **starfsmenn vöruhúss** og velja svo viðeigandi tengil.  
    2.  Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda í glugganum **Notendur**.  
    3.  Í reitnum **Staðsetningarkóði** er fært inn SILVER.  
    4.  Veljið reitinn **Sjálfgefið**.  

-   Gerið vöru LS-81 tiltæka í SILFUR staðsetningu á eftirfarandi hátt:  

    1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðafærslubækur** og velja svo viðeigandi tengil.  
    2.  Opnið sjálfgefnu færslubókina og stofnið tvær birgðabókarlínur með eftirfarandi upplýsingum um vinnudagsetninguna (Janúar 23).  

        |Tegund færslu|Vörunúmer|Staðsetningarkóði|Hólfkóti|Magn|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Auking|LS-81|SILFRAÐ|S-01-0001 **Athugið:**  Sjálfgefið hólf vörunnar í CRONUS.|2.0|  
        |Auking|LS-81|SILFRAÐ|S-01-0002|2.0|  

    3.  Valið er **bóka** aðgerð og síðan hnappinn **Já**.  

## <a name="story"></a>Ferill  
Stjórnandi vöruhússins hjá CRONUS, Ellen, setur upp SILVER-vöruhúss fyrir grunntínslur þar sem starfsmenn vöruhússins meðhöndla pantanir á útleið hverja fyrir sig. Sá sem vinnur pantanir, býr til sölupöntun með 30 einingum af vöru LS-81 sem afgreiða á til viðskiptamanns 10000 úr SILVER vöruhúsinu. Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins. Öllum tengdum verkum er stjórnað af John í glugganum **Birgðatínsla** sem sjálfkrafa vísar í hólfin þar sem LS-81 er geymt.  

## <a name="setting-up-the-location"></a>Uppsetning staðsetningarinnar  
Uppsetning gluggans **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.  

### <a name="to-set-up-the-location"></a>Uppsetning staðsetningar  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.  
2.  SILVER-staðsetningarspjaldið er opnað.  
3.  Veljið gátreitinn **Taka til**.  

## <a name="creating-the-sales-order"></a>Stofna sölupöntunina  
Sölupantanir eru algengasta tegundin af upprunaskjali á útleið.  

### <a name="to-create-the-sales-order"></a>Stofna sölupöntun.  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3.  Stofna sölupöntun fyrir viðskiptamann 10000 á vinnudeginum (23. Janúar) með eftirfarandi sölupöntunarlínu.  

    |Vara|Kóti birgðageymslu |Magn|  
    |----------|-------------------|--------------|  
    |LS_81|SILVER|30|  

     Tilkynnið svo vöruhúsinu að sölupöntunin er tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.  

4.  Valið er **Losa** aðgerð.  

    Haldið er áfram að taka til og senda seldar vörur.  

## <a name="picking-and-shipping-items"></a>Tínsla og afhending vara  
Í glugganum **Birgðatínsla** er hægt að meðhöndla alla virkni vöruhúss á útleið fyrir tiltekið upprunaskjal, til dæmis sölupöntun.  

### <a name="to-pick-and-ship-items"></a>Til að tína og senda vörur  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatínsla** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3.  Veljið reitinn **Upprunaskjal** og svo **Sölupöntun**.  
4.  Veldu reitinn **Upprunanr.**, velja línuna fyrir sölu til viðskiptamanns 10000 og skal velja svo hnappinn **Í lagi**.  

    Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan sölupöntun.  
5.  Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

    Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 30 í birgðatínslulínurnar tvær, í þeirri röð.  
6.  Veldu aðgerðina **Bóka**, veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.  

    Tínsla hátalaranna 30 úr hólfum S-01-0001 og S-01-0002 er nú skráð og neikvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu söluafhendingu.  

## <a name="see-also"></a>Sjá einnig  
 [Hvernig á að tína Vörur með Birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)   
 [Hvernig á að tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Hvernig á að setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Hvernig á að: færa íhluti á aðgerðasvæði í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Hvernig skal: Taka til fyrir framleiðslu eða samsetningu.](warehouse-how-to-pick-for-production.md)   
 [Hvernig á að: færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Hönnunarupplýsingar: vöruhúsaflæði á innleið](design-details-outbound-warehouse-flow.md)   
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

