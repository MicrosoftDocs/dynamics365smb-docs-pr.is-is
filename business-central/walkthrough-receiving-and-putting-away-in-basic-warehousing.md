---
title: Kynning – Móttaka og frágangur í grunnstillingum vöruhúss
description: Lærðu um mismunandi leiðir til að sjá um innferli fyrir móttöku og frágang.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru vörur afhentar og þær síðan notaðar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast kvittana|Krefjandi frágangur|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|B|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: pöntun-eftir pöntun.|  
|N|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar um vöruflæði á  [innleið](design-details-inbound-warehouse-flow.md).

Eftirfarandi kynning sýnir aðferð B í fyrri töflu.  

## <a name="about-this-walkthrough"></a>Um kynninguna

Í grunnvöruhúsaleiðunum þar sem birgðageymslan er sett upp þannig að krafist sé frágangsvinnslu en ekki móttöku vinnslu skal nota  **síðuna birgðafrágangsfærslu**  til að skrá og bóka frágangs-og móttökuupplýsingar fyrir upprunaskjöl á innleið. Eftirfarandi skjöl eru upprunaskjöl á innleið:

* Innkaupapöntun
* Vöruskilapöntun sölu
* Flutningspöntun á innleið
* Framleiðslupöntun með úttak sem tilbúið er að ganga frá

> [!NOTE]
> Þó svo að stillingarnar kalli  **á tiltekt**  og  **frágangssendingar** er samt hægt að bóka móttökur og afhendingar beint úr upprunaviðskiptaskjölum á birgðageymslum þar sem gátreitirnir eru valdir.  

Þessi kynning fjallar um eftirfarandi verk:  

* Setja upp staðsetningu SILFURS til frágangs birgða.  
* Setja upp staðsetningu SILUNGS fyrir hólfaafgreiðslu.  
* Skilgreinið sjálfgefið hólf fyrir vöru LS-81. (LS-75 er þegar uppsett í CRONUS.)  
* Stofna innkaupapöntun fyrir lánardrottin 10000 fyrir 40 hátalara.  
* Staðfestið að frágangshólfin séu forstillt af uppsetningunni.  
* Sleppið innkaupapöntuninni fyrir vöruhúsameðhöndlun.  
* Stofna birgðafrágang út frá útgefnu upprunaskjali.  
* Staðfestið að frágangshólf séu fengin úr innkaupapöntuninni.  
* Skrá vöruhúsahreyfinguna inn í vöruhúsið og bóka innkaupamóttöku fyrir upprunapöntunina.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Hlutverk

Eftirtalin hlutverk notenda framkvæma verkefnin sem þessi gönguleið sýnir:  

* Yfirmaður vöruhúss  
* Innkaupaaðili  
* Starfsmaður í vöruhúsi  

## <a name="prerequisites"></a>Frumskilyrði

Til að ljúka þessu gönguleið þarftu:  

* CRONUS Alþt hf. gögn  
* Að vera starfsmaður vöruhúss á SILUNGSVEIÐI á staðnum. Ef þú vilt stilla þig upp skaltu fylgja þessum skrefum:  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
    2.  **REITURINN kenni**  notanda er valinn og notandareikninginn á  **síðunni notendur** .  
    3.  **Í reitnum Kóti birgðageymslu**  er valið  **silfur**.  
    4.  **Veljið sjálfgefna**  gátreitinn.  

## <a name="story"></a>Ferill

Ellen, stjórnandi vöruhúss hjá CRONUS International Ltd. stofnar innkaupapöntun fyrir 10 einingar af vöru LS-75 og 30 einingar af vöru LS-81 frá lánardrottni 10000 sem afhenda á til SILVER vöruhúss. Þegar sendingin kemur til vöruhúss, er John, starfsmaður vöruhússins, setur vörurnar í sjálfgefnu hólfin sem tilgreind eru fyrir vörurnar. Frágangurinn er bókaður, vörurnar eru bókaðar sem mótteknar í birgðir og tiltækar til sölu eða aðra eftirspurn.  

## <a name="setting-up-the-location"></a>Staðsetningin sett upp

Stillingar á  **birgðageymsluspjaldinu**  Skilgreina vöruhúsaflæði fyrirtækisins.  

### <a name="to-set-up-the-location"></a>Uppsetning staðsetningar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2. SILVER-staðsetningarspjaldið er opnað.  
3. Kveikja á  **kröfu um frágang á skiptistað** .  

    Setja upp sjálfgefið hólf fyrir þau tvö vörunúmer sem á að stjórna þar sem gengið er frá.  

4. Veldu aðgerðina **Hólf**.  
5. Valin er fyrsta röðin, fyrir hólf  **S-01-0001** og síðan valið  **·**  efnisaðgerðin.  

    Tilkynning um  **innihald**  hólfs sem vara  **ls-75**  er þegar uppsett sem efni á hólmsheiði S-01-0001.  

6. Valið er **Nýtt** aðgerð.  
7. Veljið **Fast** og svo **Sjálfgefið**.  
8. Í reitnum  **Vörunr.**  reit skal færa  **ls-81**.  

## <a name="create-the-purchase-order"></a>Stofna innkaupapöntunina

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
    > Hólfakótinn er sjálfkrafa færður inn samkvæmt uppsetningunni sem var stofnuð í  [uppsetningu kaflans Birgðageymsla](#setting-up-the-location) .  

    Næsta skal tilkynna vöruhúsið að innkaupapöntunin er tilbúin fyrir vöruhúsameðhöndlun þegar sending berst.  

4. Valið er **Losa** aðgerð.  

    Afhending hátalara frá lánardrottni 10000 hefur borist til SILVER vöruhússins og starfsmaður gengur svo frá þeim.  

## <a name="receive-and-put-the-items-away"></a>Taka við og setja vörurnar í burtu

 **Notið síðuna birgðafrágangssíða**  til að hafa umsjón með öllum vöruhúsaaðgerðum á innleið fyrir tiltekið upprunaskjal, til dæmis innkaupapöntun.  

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
