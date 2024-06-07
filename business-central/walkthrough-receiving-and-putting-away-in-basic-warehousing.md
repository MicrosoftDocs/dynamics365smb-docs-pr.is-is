---
title: Kynning – Móttaka og frágangur í grunnstillingum vöruhúss
description: Fræðast um mismunandi leiðir til að meðhöndla ferla á innleið til móttöku og frágangs.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru mótteknar og gengið frá þeim með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast móttöku|Krefjast frágangs|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Nánari upplýsingar í Vöruhúsaflæði á [innleið](design-details-inbound-warehouse-flow.md).

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.  

## <a name="about-this-walkthrough"></a>Um kynninguna

Í einfaldri vöruhúsagrunnstillingu þar sem birgðageymsla er sett upp þannig að krafist sé frágangsvinnslu en ekki móttökuvinnslu skal nota **síðuna Birgðafrágangur** til að skrá og bóka frágang og móttökuupplýsingar fyrir upprunaskjöl á innleið. Eftirfarandi skjöl eru upprunaskjöl á innleið:

* Innkaupapöntun
* Vöruskilapöntun sölu
* Flutningspöntun á innleið
* Framleiðslupöntun með frálagi sem er tilbúið til frágangs

> [!NOTE]
> Jafnvel þó stillingarnar séu kallaðar **Krefjast tínslu** og **Krefjast frágangs** er samt hægt að bóka móttökur og afhendingar beint úr upprunaviðskiptaskjölum í birgðageymslum þar sem þessir gátreitir eru valdir.  

Þessi kynning fjallar um eftirfarandi verk:  

* Setja upp staðsetningu SILVER fyrir birgðafrágang.  
* Setja upp birgðageymsluna SILVER fyrir meðhöndlun hólfa.  
* Skilgreina sjálfgefið hólf fyrir vöruna LS-81. (LS-75 er þegar uppsett í CRONUS.)  
* Stofna innkaupapöntun fyrir lánardrottin 10000 fyrir 40 hástafi.  
* Ganga þarf úr skugga um að frágangshólfin séu forstillt eftir uppsetningu.  
* Innkaupapöntunin er gefin út fyrir vöruhúsastjórnun.  
* Stofna birgðafrágang sem byggist á útgefnu upprunaskjali.  
* Ganga þarf úr skugga um að frágangshólfin séu fengin úr innkaupapöntuninni.  
* Skrá vöruhúsahreyfinguna í vöruhúsið og bóka innkaupamóttökuna fyrir upprunainnkaupapöntunina.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Hlutverk

Eftirfarandi notendahlutverk framkvæma verkin sem þessi kynning sýnir:  

* Yfirmaður vöruhúss  
* Innkaupaaðili  
* Starfsmaður í vöruhúsi  

## <a name="prerequisites"></a>Frumskilyrði

Til að ljúka þessari kynningu þarf:  

* CRONUS Gögn um Ísland hf.  
* Að vera starfsmaður í vöruhúsi á SILVER- stað. Til að setja sig upp skal fylgja eftirfarandi skrefum:  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
    2. Reiturinn **Notandakenni** er valinn og notandareikningur valinn á síðunni **Notendur** .  
    3. Í reitnum **Kóti** birgðageymslu skal velja **SILVER**.  
    4. Gátreiturinn **Sjálfgefinn** er valinn.  

## <a name="story"></a>Ferill

Ellen, stjórnandi vöruhúss hjá CRONUS International Ltd. stofnar innkaupapöntun fyrir 10 einingar af vöru LS-75 og 30 einingar af vöru LS-81 frá lánardrottni 10000 sem afhenda á til SILVER vöruhúss. Þegar afhending berst í vöruhúsið setur Jón starfsmaður vöruhússins frá vörunum í sjálfgefin hólf sem skilgreind eru fyrir vörurnar. Frágangurinn er bókaður, vörurnar eru bókaðar sem mótteknar í birgðir og tiltækar til sölu eða aðra eftirspurn.  

## <a name="setting-up-the-location"></a>Uppsetning birgðageymslu

Stillingar á síðunni **Birgðageymsluspjald** skilgreina vöruhúsaflæði fyrirtækisins.  

### <a name="to-set-up-the-location"></a>Uppsetning staðsetningar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2. SILVER-staðsetningarspjaldið er opnað.  
3. Kveikja á krefjast **frágangsvíkkunar** .  

    Setja upp sjálfgefið hólf fyrir vörunúmerin tvö til að stjórna því hvar gengið er frá þeim.  

4. Veldu aðgerðina **Hólf**.  
5. Fyrsta línan er valin fyrir hólfið **R-01-0001** og síðan aðgerðin **Innihald** valið.  

    Tilkynning á síðunni **Innihald** hólfs um að varan **LS-75** er þegar uppsett sem innihald í hólfi S-01-0001.  

6. Valið er **Nýtt** aðgerð.  
7. Veljið **Fast** og svo **Sjálfgefið**.  
8. Í reitnum Vörunr **.** LS-81 **er fært inn**.  

## <a name="create-the-purchase-order"></a>Innkaupapöntunin búin til

Innkaupapantanir eru algengustu tegundir af upprunaskjölum á innleið.  

### <a name="to-create-the-purchase-order"></a>Innkaupapöntunin stofnuð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Stofna innkaupapöntun fyrir lánardrottinn 10000 á vinnudeginum (23. Janúar) með eftirfarandi innkaupapöntunarlínum.  

    |Vara|Staðsetningarkóði|Hólfkóði|Magn|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SILVER|S-01-0001|10|  
    |LS-81|SILVER|S-01-0001|30|  

    > [!NOTE]  
    > Hólfakótinn er færður inn sjálfvirkt samkvæmt uppsetningunni sem stofnuð var í hlutanum [Uppsetning birgðageymslu](#setting-up-the-location) .  

    Næst skal tilkynna vöruhúsinu að innkaupapöntunin sé tilbúin til meðhöndlunar á vöruhúsi þegar afhending berst.  

4. Valið er **Losa** aðgerð.  

    Afhending hátalara frá lánardrottni 10000 hefur borist til SILVER vöruhússins og starfsmaður gengur svo frá þeim.  

## <a name="receive-and-put-the-items-away"></a>Móttaka og ganga frá vörunum

Nota síðuna **Birgðafrágangur** til að stjórna öllum vöruhúsaaðgerðum á innleið fyrir tiltekið upprunaskjal, t.d. innkaupapöntun.  

### <a name="to-receive-and-put-the-items-away"></a>Tekið á móti og gengið frá vörunum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðafrágangur** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Veljið reitinn **Upprunaskjal** og svo **Innkaupapöntun**.  
4. Veldu reitinn **Upprunanr.**, velja línuna fyrir innkaup frá viðskiptamanni 10000 og skal velja svo hnappinn **Í lagi**.  

    Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan innkaupapöntunina.  

5. Velja aðgerðina **Færa sjálfkr. magn til afgr.**.  

    Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 30 í birgðafrágangslínurnar tvær, í þeirri röð.  

6. Veldu aðgerðina **Bóka**, veldu **Móttaka** aðgerðina og veldu síðan **Í lagi** hnappinn.  

    Frágangur hátalaranna 40 í hólf S-01-0001 er nú skráður og jákvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu innkaupamóttöku.  

## <a name="see-also"></a>Sjá einnig

[Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md)  
[Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
