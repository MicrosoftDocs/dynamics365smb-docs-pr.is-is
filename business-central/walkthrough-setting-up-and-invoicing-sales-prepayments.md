---
title: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu
description: Fyrirframgreiðslur eru greiðslur sem eru reikningsfærðar og bókaðar á fyrirframgreiðslupöntun sölu- eða innkaupa áður en lokareikningsfærsla fer fram.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu

Þessi kynning fer með þér í gegnum ferlið við að setja upp og nota fyrirframgreiðslur í [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Þú getur til dæmis sent fleiri fyrirframgreiðslureikninga ef fleiri vörum er bætt við pöntunina.  

## <a name="about-this-walkthrough"></a>Um kynninguna

Þessi kynning fer yfir eftirfarandi aðstæður:  

- Uppsetning fyrirframgreiðslna  
- Stofnun pöntunar sem þarf fyrirframgreiðslu  
- Stofnun fyrirframgreiðslureiknings  
- Leiðrétting fyrirframgreiðsluþarfa á pöntun  
- Notkun fyrirframgreiðslna á pöntun  
- Reikningsfærsla lokaupphæðar á pöntun með fyrirframgreiðslu  

### <a name="roles"></a>Hlutverk

Þessi kynning nær yfir verk fyrir eftirfarandi hlutverk:  

- Aðalbókari (Pála)  
- Pantanavinnsla (Súsanna)  
- Innheimtustjóri (Árni)  

## <a name="story"></a>Ferill

 Phyllis er bókhaldsstjóri og tekur ákvarðanir um hvaða Viðskiptavinir eru nauðsynlegir til að greiða innborgun áður en vörur eru framleiddar eða afhentar. Pála stillir [!INCLUDE[prod_short](includes/prod_short.md)] á að reikna fyrirframgreiðslur sjálfvirkt.  

 Súsanna vinnur í sölupöntunarvinnslu. Þegar viðskiptavinur hringir til að leggja inn pöntun slær Susan inn pöntun í kerfið á meðan viðskiptavinurinn er í símanum. Þannig getur Susan staðfest verð og greiðsluskilmála með viðskiptavininum strax og gert breytingar á pöntuninni á meðan verið er að semja við viðskiptavininn.  

 Arnie starfar á viðskiptadeild og bókar reikninga og greiðslur.  

 Í þessu dæmi setur Phylllis upp kröfu um fyrirframgreiðslu fyrir viðskiptamanninn Selangorian, samkvæmt lánaferlinum hans. Phyllis gefur Susan fyrirmæli um hvernig eigi að afgreiða pantanirnar.  

 Þegar viðskiptavinurinn hringir er Susan að semja við viðskiptavininn þar til þeir ná samkomulagi og velja síðan að reikna fyrirframgreiðsluna á nokkra mismunandi vegu.  

 Eftir að Súsanna hefur sent fyrirframgreiðslureikninginn, pantar viðskiptamaðurinn aukavöru. Súsanna uppfærir pöntunina og býr til annan fyrirframgreiðslureikning.  

 Árni skráir greiðslu viðskiptamannsins, jafnar hana við reikninga og sendir að lokum lokareikninginn.  

## <a name="set-up-prepayments"></a>Uppsetning fyrirframgreiðslu

Pála setur kerfið upp fyrir fyrirframgreiðslur frá viðskiptamönnum.  

- Hún ákveður að nota sömu númerröð fyrir fyrirframgreiðslu og er notuð fyrir sölureikningsfærslu.  
- Pála stillir forritið á að kanna hvort fyrirframgreiðslu er krafist fyrir lokareikningsfærslu á pöntun.  
- Hún tilgreinir sjálfgefin gildi hlutfalls fyrirframgreiðslu fyrir tilteknar vörur og viðskiptamenn.  

Eftirfarandi aðgerðir lýsa hvernig Pála framkvæmir þessi verk.  

### <a name="to-set-up-number-series-for-prepayments"></a>Uppsetning númeraraða fyrir fyrirframgreiðslur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.  
2. Á síðunni **Setja upp sölugrunn** skal stækka flýtiflipann **Númeraröð**.  
3. Ganga þarf úr skugga um að númeraraðirnar fyrir bókaða fyrirframgreiðslureikninga (í reitnum **Bókuð fyrirframgr.reikn.nr.**) séu þær sömu og fyrir bókaða sölureikninga (**Nr.röð bókaðra reikninga**) og númeraraðirnar fyrir bókaða kreditreikninga fyrirframgreiðslu (**Bókuð kr.reikn.nr. fyrirframgr.**) séu þær sömu og fyrir bókaða kreditreikninga (**Nr.röð bókaðra kreditreikninga**).  

### <a name="to-block-shipments-for-unpaid-prepayment"></a>Frysting afhendinga vegna ógreiddra fyrirframgreiðslna

1. Á síðunni **Sala & Útistandandi uppsetning**, á flýtiflipanum **Almennt**, er gátreiturinn **Kanna fyrirframgreiðslu við bókun** valinn.

Ekki er hægt að afhenda eða reikningsfæra pöntun sem er með ógreidda fyrirframgreiðslu.  

Sjálfgefið er að Pála vill að viðskiptamaður 20000 þurfi að greiða 30% af öllum pöntunum fyrirfram. Því mun Phyllis færa inn sjálfgefið fyrirframgreiðsluhlutfall á viðskiptamannaspjaldinu.  

Pála vill að allir viðskiptamenn þurfi að borga 20% fyrirfram fyrir vöru 1896-S. Viðskiptavinur 20000 er með lélega greiðslusögu, þannig að Phyllis krefst 40% fyrirframgreiðslu frá viðskiptavini 20000 fyrir vöru 1896-S. Eftirfarandi dæmi sýnir hvernig á að setja upp sjálfgefið hlutfall fyrirframgreiðslu.  

### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Úthlutun sjálfgefins hlutfalls fyrirframgreiðslu á viðskiptamenn og vörur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.  
2. Opnaðu spjaldið fyrir viðskiptamann 20000 (Trey Research).
3. Í flýtiflipann **Greiðslur**, í reitinn **Fyrirframgreiðsla %**, skal færa inn **30**.  
4. Veldu aðgerðina **Tengt**, veldu valmyndaratriðið **Sala** og veldu síðan valmyndaratriðið **Fyrirframgreiðsluprósentur**.  
5. Tvær línur á síðunni **Prósentur fyrirframgreiðslu sölu** eru fylltar út á eftirfarandi hátt.  

    |**Tegund sölu**|**Kóti sölu**|**Vörunr.**|**Fyrirframgreiðsla %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Viðskiptamaður**|**20000**|**1896-S**|**40**|
    |**Viðskiptamaður**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > Einnig þarf að tilgreina skattflokkskóða samkvæmt landinu/svæðinu þínu í flýtiflipanum **Kostnaður og bókun** fyrir vöru 1896-S. Þegar sýnifyrirtækið er notað er þegar búið að stilla þennan reit.

6. Loka öllum síðum.  

### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Til að tilgreina lykil fyrir sölufyrirframgreiðslur í alm. bókunargrunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning almennrar bókunar** og velja síðan viðkomandi tengil.  
2. Veldu línuna þar sem reiturinn **Alm. viðsk.bókunarflokkur** er stilltur á **INNLENT** og reiturinn **Alm. vörubókunarflokkur** er stilltur á **SMÁSALA**.  
3. Í reitnum **Fyrirframgreiðslureikn. sölu** skal tilgreina viðeigandi reikning. Valið er vistað sjálfkrafa.  

> [!TIP]
> Ef þú getur ekki séð reit á síðunni **Uppsetning bókunargrunns** notaðu þá lárétta flettistiku neðst á síðunni til að fletta til hægri.  

## <a name="create-an-order-that-requires-a-prepayment"></a>Stofna pöntun sem þarf fyrirframgreiðslu

 Í eftirfarandi dæmi stofnar Súsanna, pantanavinnslan, pöntun útfrá samtali við viðskiptamann. Vörurnar sem viðskiptamaðurinn pantar krefjast fyrirframgreiðslu. Auk þess hefur viðskiptamaðurinn greitt of seint nokkrum sinnum áður. Súsanna hefur fengið fyrirmæli um að krefjast föstu fyrirframgreiðsluupphæðarinnar **800** fyrir pöntunina.  

Viðskiptavinurinn biður um að borga 35%, sem Susan samþykkir og breytir pöntuninni.  

Hún stofnar fyrirframgreiðslureikning og sendir hann til viðskiptamannsins.  

### <a name="to-create-a-sales-order-with-a-prepayment"></a>Stofnun sölupöntunar með fyrirframgreiðslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **Heiti viðskiptamanns** skal velja **Trey Research**.  
4. Loka skal viðvörun um vanskil sem birtist.  
5. Tvær sölulínur eru fylltar út með eftirfarandi upplýsingum.  

    |**Tegund**|**Nr.**|**Magn**|  
    |--------------|-------------|------------------|  
    |**Vara**|**1896-S**|**1**|  
    |**Vara**|**1900-S**|**1**|

    Fyrirframgreiðslureitirnir í sölulínunni eru sjálfgefið faldir. Til að birta reitina verður þú að sérsníða síðuna. Frekari upplýsingar eru í [Hefja sérstillingu á síðu með borðanum Sérstilla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6. Ganga þarf úr skugga um að í reitnum **Fyrirframgreiðsla %** á línunni með vöru **1900-S** standi **30**. Sjálfgefið gildi er tekið úr söluhausnum sem var fylltur út með viðskiptamannsspjaldinu.  

    Í reitnum **Fyrirframgreiðsla %** á línunni með vörunni **1896-S** stendur **40**. 40 er prósentan sem var færð inn á síðunni **Prósentur fyrirframgreiðslu sölu** fyrir vöru **1896-S** og viðskiptamann **20000**.  

    Nánari upplýsingar um það eru í [Setja upp fyrirframgreiðslur](finance-set-up-prepayments.md).  
7. Í aðgerðinni **Pöntun** skal velja **Upplýsingar**.  
8. Í flýtiflipanum **Fyrirframgreiðsla** inniheldur reiturinn **Upphæð fyrirframgreiðslu án VSK** **458,16**. Ef fyrirframgreiðslureikningur er stofnaður fyrir pöntunina núna er 458,16 upphæðin á reikningnum.  

    Í þessu dæmi hefur Súsanna fyrirmæli um að nota fyrirframgreiðslu upp á **800** á pöntunina.  

    > [!IMPORTANT]  
    >  Eftirfarandi skref gætu ekki átt við, allt eftir landi/svæði.  
9. Upphæðinni í reitnum **Upphæð fyrirframgr. án skatts** er breytt í **800** og síðunni því næst lokað.  
10. Þegar reiturinn **Fyrirframgreiðsla %** á sölulínunni er skoðaður sést að hann hefur verið endurreiknaður í **67,02438** og **67,02282**.  

     Endurreikningurinn nær yfir allar línur sem eru með fyrirframgreiðsluprósentu sem er hærri en 0.  

     Nú spyr viðskiptamaðurinn hvort hægt sé að hafa fyrirframgreiðsluna 35%. Yfirmaður Súsönnu samþykkir breytinguna.
11. Á síðunni **Sölupöntun** á reitnum **Fyrirframgreiðsla** í **Fyrirframgreiðsla %** er fært inn **35**.  
12. Í viðvörunarglugganum sem birtist velurðu **Já** hnappinn. 35% gjald verður notaður sem fyrirframgreiðsluprósenta fyrir alla pöntunina.  
13. Staðfestu að línurnar hafi verið rétt uppfærðar.  

## <a name="create-a-prepayment-invoice"></a>Stofna fyrirframgreiðslureikning

Þegar Súsanna hefur fært inn rétt fyrirframgreiðslugildi á pöntunina stofnar hún fyrirframgreiðslureikninga og sendir á viðskiptamanninn.  

### <a name="to-create-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings

1. Á síðunni **Sölupöntun** skal velja **Aðgerðir**, síðan **Bókun**, síðan **Fyrirframgreiðsla** og síðan er valin **Bóka og prenta fyrirframgreiðslureikning**
2. Veldu **Já** til að bóka reikninginn.  

> [!NOTE]  
> Susan myndi nú senda reikninginn til viðskiptamannsins.  

## <a name="create-an-additional-prepayment-invoice"></a>Stofna annan fyrirframgreiðslureikning

Næsta dag hringir viðskiptamaðurinn í Súsönnu og gerir breytingar á pöntuninni. Viðskiptamaðurinn vill tvær vörur af 1896-S. Susan Enduropnar pöntunina, uppfærir hana og stofnar síðan annan fyrirframgreiðslureikning fyrir pöntunina og sendir til viðskiptavinarins.  

### <a name="to-create-an-additional-prepayment-invoice"></a>Stofnun annars fyrirframgreiðslureiknings

1. Á síðunni **Sölupöntun** skal velja aðgerðina **Losa** og síðan **Enduropna**.  
2. Á línunni fyrir vöruna **1896-S**, í reitnum **Magn** skal slá inn **2**.  

    Í aðgerðinni **Pöntun** skal velja **Upplýsingar**. Reiturinn **Upphæð fyrirframgreiðslu án VSK** inniheldur nú **768,04** og reiturinn **Reikn. fyrirfr.gr.upphæð. án VSK** inniheldur **417,76**. Þessi gildi sýna að önnur fyrirframgreiðsluuphæð er til staðar sem ekki er búið að reikningsfæra.  
3. Til að bóka reikning fyrir aðra fyrirframgreiðslu er valin **Aðgerðir**, síðan **Bókun**, síðan **Fyrirframgreiðsla** og síðan er valin **Bóka og prenta fyrirframgreiðslureikning**
4. Veldu **Já** til að bóka reikninginn.  

## <a name="apply-the-prepayments"></a>Jafna fyrirframgreiðslu

Viðskiptamaðurinn greiðir fyrirframgreiðsluupphæðina. Arnie, úr bókhaldsdeildinni, skráir greiðsluna og notar hana á fyrirframgreiðslureikninga.  

### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Jöfnun greiðslu við fyrirframgreiðslureikninga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Inngreiðslubækur** og velja síðan viðkomandi tengil.  
2. Færslubókarlínan er fyllt út með eftirfarandi upplýsingum.  

    |Heiti reits|Innfært|  
    |----------------|-----------|  
    |**Tegund fylgiskjals**|**Greiðsla**|  
    |**Tegund reiknings**|**Viðskiptamaður**|  
    |**Reikningur nr.**|**20000**|  
3. Veldu aðgerðina **Ferli** og síðan **Jafna færslur**.  
4. Á síðunni **Jafna viðskm.færslur** er fyrsti fyrirframgreiðslureikningurinn valinn og svo aðgerðin **Ferli** og **Setja kenni jöfnunar** aðgerðin.  
5. Endurtaka skal fyrri skref fyrir seinni fyrirframgreiðsluna.  
6. Velja hnappinn **Í lagi**.  

    Reitirnir **Upphæð** hafa nú verið fylltir út með samtölu fyrirframgreiðslureikninganna tveggja.  

7. Til að bóka færslubókina velurðu **Bóka/Prenta** og síðan **Bóka**.
8. Velja hnappinn **Já**.

## <a name="invoice-the-remaining-amount"></a>Reikningsfæra eftirstandandi upphæð

Árna hefur verið tilkynnt að vörurnar á pöntuninni hafi verið afhentar og að pöntunin sé tilbúin til reikningsfærslu. Árni stofnar því reikning fyrir pöntunina.  

### <a name="to-invoice-the-remaining-amount"></a>Reikningsfærsla eftirstandandi upphæðar

1. Sölupöntunin er opnuð.
2. Veldu aðgerðina **Bókun** og svo **Bóka**.
3. Veljið **fhenda og reikningsfæra** og smellið á hnappinn **Í lagi**.
4. Ef forskoða á reikninginn skal velja hnappinn **Já**.

    > [!NOTE]  
    > Að öllu jöfnu væri afhendingardeildin búin að bóka afhendinguna.  

    Árni geta skoðað ferilinn til að staðfesta að sölureikningurinn var stofnaður eins og til var ætlast.

5. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Uppfæra stöðu fyrirframgreiddra pantana og reikninga sjálfkrafa

Þú getur flýtt fyrir pöntunar- og reikningsvinnslu með því að setja upp verkraðarfærslur sem uppfæra stöðu þessara skjala sjálfkrafa. Þegar fyrirframgreiðslureikningur er greiddur geta verkraðarfærslurnar sjálfkrafa breytt stöðu skjalsins úr **Bíður fyrirframgreiðslu** í **Útgefið**. Þegar þú setur upp verkraðarfærslurnar eru kóðaeiningarnar sem þú þarft að nota **383 Uppf. fyrirfgr. á sölu í bið** og **383 Uppf. fyrirfgr. á innkaupum í bið**. Mælt er með því að keyra færslurnar reglulega, t.d. á mínútu fresti. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="next-steps"></a>Næstu þrep

Þessi kynning fór yfir eftirfarandi skref til að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að afgreiða fyrirframgreiðslur. 

- Settu upp sjálfgefnar fyrirframgreiðsluprósentur á viðskiptamenn og vörur.
- Notaðu mismunandi aðferðir til að reikna út fyrirframgreiðslurnar í pöntun.  
- Reiknaðu fyrirframgreiðsluupphæðina sem prósentu af samtölu pöntunarinnar.
- Úthlutaðu einni heildarupphæð fyrirframgreiðslunnar á pöntunina.  

Einnig var fyrirframgreiðslureikningur bókaður, annar reikningur stofnaður þegar pöntunin breyttist og lokareikningur fyrir eftirstandandi upphæð var bókaður.  

Möguleikar fyrirframgreiðslu gera þér auðvelt að setja upp og framfylgja reglum um fyrirframgreiðslu fyrir viðskiptamenn og vörur. Þeir gera þér einnig kleift að bóka allar greiðslur á móti reikningi.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
