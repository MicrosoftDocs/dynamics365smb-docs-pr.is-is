---
title: 'Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss | Microsoft Docs'
description: Í Business Central er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 597f14f07f7e8ac690dce8a5473d01ec68d1669a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314744"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss

**Athugið**: Framkvæma verður þessa kynningu í sýnifyrirtæki með valkostinum **Fullt mat - öll sýnigögn** sem er í boði í sandkassaumhverfinu. Nánari upplýsingar eru í [Sandkassaumhverfi stofnað](across-how-create-sandbox-environment.md).

Í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Móttökur|Frágangur|Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|X|||2|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali|||X|3|  
|C|Bóka móttöku og frágang frá vöruhúsamóttökuskjali||X||4/5/6|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali||X|X|4/5/6|  

Nánari upplýsingar er að finna í [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md).  

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
Í grunnstillungum vöruhúss þar sem staðsetning er sett upp þannig að krafist sé frágangs en ekki móttökuvinnslu skal nota síðuna **Birgðafrágangur** til að skrá og bóka frágang og afhendingarupplýsingar fyrir upprunaskjöl á innleið. Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun þar sem úttakið er tilbúið til frágangs.

> [!NOTE]
> Jafnvel þótt stillingarnar séu kallaðar **Krefjast tínslu** og **Krefjast frágangs**, geturðu samt sem áður bókað móttöku og afhendingu beint frá uppruna viðskiptaskjala í birgðageymslum þar sem þú velur þessa gátreiti.  

Þessi kynning fjallar um eftirfarandi verk.  

-   Stilli SILVER staðsetningu fyrir birgðafrágang.  
-   Stilli SILVER staðsetningu fyrir meðhöndlun hólfa.  
-   Skilgreinir sjálgefið hólf fyrir vöru LS-81. (LS-75 er þegar uppsett í CRONUS.)  
-   Stofna innkaupapöntun fyrir lánardrottinn 10000 fyrir 40 hátalara.  
-   Staðfesti að frágangshólfin er forstillt samkvæmt uppsetningu.  
-   Gefur út innkaupapöntunina fyrir afgreiðslu vöruhúss.  
-   Stofna birgðafrágang byggðan á útgefnu upprunaskjali.  
-   Staðfesti að frágangshólfin erfast úr innkaupapöntuninni.  
-   Skráir vöruhúsahreyfinguna í vöruhúsið og bókar á sama tíma innkaupamóttökuna fyrir upprunaskjal innkaupapöntunarinnar.  

## <a name="roles"></a>Hlutverk  
Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

-   Yfirmaður vöruhúss  
-   Innkaupaaðili  
-   Starfsmaður í vöruhúsi  

## <a name="prerequisites"></a>Frumskilyrði  
Til að ljúka þessari kynningu þarf:  

-   CRONUS International Ltd. er uppsett.  
-   Til að gera notanda að starfsmanni vöruhúss í SILVER staðsetningu á eftirfarandi hátt:  

    1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsfólk vöruhúss** og veldu síðan tengda tengilinn.  
    2.  Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
    3.  Í reitnum **Staðsetningarkóði** er fært inn SILVER.  
    4.  Veljið reitinn **Sjálfgefið**.  

## <a name="story"></a>Ferill  
Ellen, stjórnandi vöruhúss hjá CRONUS International Ltd. stofnar innkaupapöntun fyrir 10 einingar af vöru LS-75 og 30 einingar af vöru LS-81 frá lánardrottni 10000 sem afhenda á til SILVER vöruhúss. Þegar sending berst í vöruhúsið, gengur starfsmaður vöruhússins frá vörunum í sjálfgefin hólf sem eru skilgreind fyrir vörurnar. Frágangurinn er bókaður, vörurnar eru bókaðar sem mótteknar í birgðir og tiltækar til sölu eða aðra eftirspurn.  

## <a name="setting-up-the-location"></a>Uppsetning staðsetningarinnar  
 Uppsetning síðunnar **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.  

### <a name="to-set-up-the-location"></a>Uppsetning staðsetningar  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.  
2.  SILVER-staðsetningarspjaldið er opnað.  
3.  Veljið gátreitinn **Þarf að ganga frá**.  

    Setjið svo upp sjálfgefið hólf fyrir vörunúmerin tvö til að stjórna hvar gengið sé frá þeim.  

4.  Veldu aðgerðina **Hólf**.  
5.  Veljið fyrstu röð fyrir hólf S-01-0001 og svo aðgerðina **Innihald**.  

    Takið eftir að á síðunni **Innihald hólfs** er vara LS-75 þegar sett upp sem efni í hólfi S-01-0001.  

6.  Valið er **Nýtt** aðgerð.  
7.  Veljið **Fast** og svo **Sjálfgefið**.  
8.  Á **Vörunúmer** reitnum skaltu slá inn LS-81.  

## <a name="creating-the-purchase-order"></a>Stofna innkaupapöntunina  
Innkaupapantanir eru algengustu tegundir af upprunaskjölum á innleið.  

### <a name="to-create-the-purchase-order"></a>Innkaupapöntunin stofnuð  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda hlekkinn.  
2.  Valið er **Nýtt** aðgerð.  
3.  Stofna innkaupapöntun fyrir lánardrottinn 10000 á vinnudeginum (23. Janúar) með eftirfarandi innkaupapöntunarlínum.  

    |Vara|Staðsetningarkóði|Hólfkóði|Magn|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SILVER|S-01-0001|10|  
    |LS-81|SILVER|S-01-0001|30|  

    > [!NOTE]  
    >  Hólfkóðinn færist sjálfvirkt inn samkvæmt uppsetningunni sem gerð var í hlutanum „Staðsetning sett upp.“  

    Tilkynnið svo vöruhúsinu að innkaupapöntunin sé tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.  

4.  Valið er **Losa** aðgerð.  

    Afhending hátalara frá lánardrottni 10000 hefur borist til SILVER vöruhússins og starfsmaður gengur svo frá þeim.  

## <a name="receiving-and-putting-the-items-away"></a>Móttaka og frágangur varanna  
Á síðunni **Birgðafrágangur** er hægt að meðhöndla alla virkni vöruhúss á innleið fyrir tiltekið upprunaskjal, til dæmis innkaupapöntun.  

### <a name="to-receive-and-put-the-items-away"></a>Tekið á móti og gengið frá vörunum  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **birgðafrágangur** og veldu síðan tengda tengilinn.  
2.  Valið er **Nýtt** aðgerð.  
3.  Veljið reitinn **Upprunaskjal** og svo **Innkaupapöntun**.  
4.  Veldu reitinn **Upprunanr.**, velja línuna fyrir innkaup frá viðskiptamanni 10000 og skal velja svo hnappinn **Í lagi**.  

    Að öðrum kosti, á flipanum **Aðgerðir** í flokknum **Eiginleikar** skal velja **Sækja upprunaskjal**og síðan innkaupapöntunina.  

5.  Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

    Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 30 í birgðafrágangslínurnar tvær, í þeirri röð.  

6.  Veldu aðgerðina **Bóka**, veldu **Móttaka** aðgerðina og veldu síðan **Í lagi** hnappinn.  

    Frágangur hátalaranna 40 í hólf S-01-0001 er nú skráður og jákvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu innkaupamóttöku.  

## <a name="see-also"></a>Sjá einnig  
 [Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md)   
 [Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md)   
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
