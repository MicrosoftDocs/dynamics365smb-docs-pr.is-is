---
title: Uppsetning og reikningsfærsla fyrirframgreiðslna sölu
description: Fyrirframgreiðslur eru greiðslur sem eru reikningsfærðar og bókaðar á fyrirframgreiðslupöntun sölu- eða innkaupa áður en lokareikningsfærsla fer fram.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 01/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna sölu

Þessi kynning fer með þér í gegnum ferlið við að setja upp og nota fyrirframgreiðslur í [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Þú getur til dæmis sent fleiri fyrirframgreiðslureikninga ef fleiri vörum er bætt við pöntunina.  

## Um kynninguna  

Þessi kynning fer yfir eftirfarandi aðstæður:  

- Uppsetning fyrirframgreiðslna  
- Stofnun pöntunar sem þarf fyrirframgreiðslu  
- Stofnun fyrirframgreiðslureiknings  
- Leiðrétting fyrirframgreiðsluþarfa á pöntun  
- Notkun fyrirframgreiðslna á pöntun  
- Reikningsfærsla lokaupphæðar á pöntun með fyrirframgreiðslu  

### Hlutverk

Þessi kynning nær yfir verk fyrir eftirfarandi hlutverk:  

- Aðalbókari (Pála)  
- Pantanavinnsla (Súsanna)  
- Innheimtustjóri (Árni)  

## Ferill

 Pála er aðalbókari og tekur ákvarðanir um hvaða viðskiptamenn þurfa að greiða innborgun áður en vörur eru framleiddar eða afhentar. Pála stillir [!INCLUDE[prod_short](includes/prod_short.md)] á að reikna fyrirframgreiðslur sjálfvirkt.  

 Súsanna vinnur í sölupöntunarvinnslu. Þegar viðskiptamaður hringir til að panta færir Súsanna pöntunina inn í kerfið á meðan viðskiptamaðurinn er í símanum. Þannig getur Súsanna staðfest verð og greiðsluskilmála strax við viðskiptamanninn og breytt pöntuninni á meðan samið er við viðskiptamanninn.  

 Árni vinnur í deildinni Útistandandi reikningar og bókar reikninga og greiðslur.  

 Í þessu dæmi setur Phylllis upp kröfu um fyrirframgreiðslu fyrir viðskiptamanninn Selangorian, samkvæmt lánaferlinum hans. Phyllis gefur Susan fyrirmæli um hvernig eigi að afgreiða pantanirnar.  

 Þegar viðskiptamaðurinn hringir semur Súsanna við viðskiptamanninn þar til hann nær samkomulagi og velur að reikna fyrirframgreiðsluna á ýmsa vegu.  

 Eftir að Súsanna hefur sent fyrirframgreiðslureikninginn, pantar viðskiptamaðurinn aukavöru. Súsanna uppfærir pöntunina og býr til annan fyrirframgreiðslureikning.  

 Árni skráir greiðslu viðskiptamannsins, jafnar hana við reikninga og sendir að lokum lokareikninginn.  

## Setja upp fyrirframgreiðslur

Pála setur kerfið upp fyrir fyrirframgreiðslur frá viðskiptamönnum.  

- Hún ákveður að nota sömu númerröð fyrir fyrirframgreiðslu og er notuð fyrir sölureikningsfærslu.  
- Pála stillir forritið á að kanna hvort fyrirframgreiðslu er krafist fyrir lokareikningsfærslu á pöntun.  
- Hún tilgreinir sjálfgefin gildi hlutfalls fyrirframgreiðslu fyrir tilteknar vörur og viðskiptamenn.  

Eftirfarandi aðgerðir lýsa hvernig Pála framkvæmir þessi verk.  

### Uppsetning númeraraða fyrir fyrirframgreiðslur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.  
2. Á síðunni **Setja upp sölugrunn** skal stækka flýtiflipann **Númeraröð**.  
3. Ganga skal úr skugga um að númeraröðin fyrir bókaða fyrirframgreiðslureikninga í reitunum **Bókuð fyrirframgr.reikn.nr.** reiturinn er hinn sami og fyrir bókaða sölureikninga (**Bókuð reikningsnr.**) og númeraröðin fyrir bókaða fyrirframgreiðslu-kreditreikninga (**Bókuð kr.reikn.nr.röð fyrirframgr.**) er hin sama og fyrir bókaða kreditreikninga (**Nr.röð** bókaðra kreditreikninga).  

### Frysting afhendinga vegna ógreiddra fyrirframgreiðslna

1. Á síðunni **Sala & Útistandandi uppsetning**, á flýtiflipanum **Almennt**, er gátreiturinn **Kanna fyrirframgreiðslu við bókun** valinn.

Ekki er hægt að afhenda eða reikningsfæra pöntun sem er með ógreidda fyrirframgreiðslu.  

Sjálfgefið er að Pála vill að viðskiptamaður 20000 þurfi að greiða 30% af öllum pöntunum fyrirfram. Þess vegna færir Pála inn sjálfgefið prósentu fyrirframgreiðslu á viðskiptamannaspjaldið.  

Pála vill að allir viðskiptamenn þurfi að borga 20% fyrirfram fyrir vöru 1896-S. Viðskiptamaður 20000 er með lélegan greiðsluferil svo Pála þarf 40% fyrirframgreiðslu frá viðskiptamanni 20000 fyrir vöru 1896-S. Eftirfarandi dæmi sýnir hvernig á að setja upp sjálfgefið hlutfall fyrirframgreiðslu.  

### Úthlutun sjálfgefins hlutfalls fyrirframgreiðslu á viðskiptamenn og vörur

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

### Til að tilgreina lykil fyrir sölufyrirframgreiðslur í alm. bókunargrunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning almennrar bókunar** og velja síðan viðkomandi tengil.  
2. Veldu línuna þar sem reiturinn **Alm. viðsk.bókunarflokkur** er stilltur á **INNLENT** og reiturinn **Alm. vörubókunarflokkur** er stilltur á **SMÁSALA**.  
3. Í reitnum **Fyrirframgreiðslureikn. sölu** skal tilgreina viðeigandi reikning. Valið er vistað sjálfkrafa.  

> [!TIP]
> Ef þú getur ekki séð reit á síðunni **Uppsetning bókunargrunns** notaðu þá lárétta flettistiku neðst á síðunni til að fletta til hægri.  

## Stofna pöntun sem krefst fyrirframgreiðslu

 Í eftirfarandi dæmi stofnar Súsanna, pantanavinnslan, pöntun útfrá samtali við viðskiptamann. Vörurnar sem viðskiptamaðurinn pantar krefjast fyrirframgreiðslu. Auk þess hefur viðskiptamaðurinn greitt of seint nokkrum sinnum áður. Súsanna hefur fengið fyrirmæli um að krefjast föstu fyrirframgreiðsluupphæðarinnar **800** fyrir pöntunina.  

Viðskiptamaðurinn biður um að borga 35% sem Súsanna samþykkir og breytir pöntuninni.  

Hún stofnar fyrirframgreiðslureikning og sendir hann til viðskiptamannsins.  

### Stofnun sölupöntunar með fyrirframgreiðslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **Heiti viðskiptamanns** skal velja **Trey Research**.  
4. Loka skal viðvörun um vanskil sem birtist.  
5. Tvær sölulínur eru fylltar út með eftirfarandi upplýsingum.  

    |**Tegund**|**Nr.**|**Magn**|  
    |--------------|-------------|------------------|  
    |**Vara**|**1896-S**|**1**|  
    |**Vara**|**1900-S**|**1**|

    Fyrirframgreiðslureitirnir í sölulínunni eru sjálfgefið faldir. Ef birta á reitina verður að sérstilla síðuna. Nánari upplýsingar [eru í Til að byrja að sérstilla síðu með borðanum Sérstilling](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

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

## Stofna fyrirframgreiðslureikning

Þegar Súsanna hefur fært inn rétt fyrirframgreiðslugildi á pöntunina stofnar hún fyrirframgreiðslureikninga og sendir á viðskiptamanninn.  

### Stofnun fyrirframgreiðslureiknings

1. Á síðunni **Sölupöntun** skal velja **Aðgerðir**, síðan **Bókun**, síðan **Fyrirframgreiðsla** og velja **svo Bóka og prenta fyrirframgr. Reikning**
2. Veldu **Já** til að bóka reikninginn.  

> [!NOTE]  
> Susan myndi nú senda reikninginn til viðskiptamannsins.  

## Stofna annan fyrirframgreiðslureikning

Næsta dag hringir viðskiptamaðurinn í Súsönnu og gerir breytingar á pöntuninni. Viðskiptamaðurinn vill tvær vörur af 1896-S. Súsanna opnar pöntunina aftur, uppfærir hana og stofnar svo annan fyrirframgreiðslureikning fyrir pöntunina og sendir hana til viðskiptamannsins.  

### Stofnun annars fyrirframgreiðslureiknings

1. Á síðunni **Sölupöntun** skal velja aðgerðina **Losa** og síðan **Enduropna**.  
2. Á línunni fyrir vöruna **1896-S**, í reitnum **Magn** skal slá inn **2**.  

    Í aðgerðinni **Pöntun** skal velja **Upplýsingar**.  **Í reitnum Upphæð fyrirframgreiðslu án VSK er** nú 768,04 **og í reitnum** Upphæð fyrirframgr. án VSK **er** **417,76**. Þessi gildi sýna að önnur fyrirframgreiðsluuphæð er til staðar sem ekki er búið að reikningsfæra.  
3. Til að bóka reikning fyrir aukafyrirframgreiðsluupphæðina skal velja **Aðgerðir**, síðan **Bókun**, síðan **Fyrirframgreiðsla** og velja **svo Bóka og prenta fyrirframgreiðslu. Reikning**
4. Veldu **Já** til að bóka reikninginn.  

## Nota fyrirframgreiðslur

Viðskiptamaðurinn greiðir fyrirframgreiðsluupphæðina. Arnie, úr bókhaldsdeildinni, skráir greiðsluna og notar hana á fyrirframgreiðslureikninga.  

### Jöfnun greiðslu við fyrirframgreiðslureikninga

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

## Reikningsfæra eftirstandandi upphæð

Árna hefur verið tilkynnt að vörurnar á pöntuninni hafi verið afhentar og að pöntunin sé tilbúin til reikningsfærslu. Árni stofnar því reikning fyrir pöntunina.  

### Reikningsfærsla eftirstandandi upphæðar

1. Sölupöntunin er opnuð.
2. Veldu aðgerðina **Bókun** og svo **Bóka**.
3. Veljið **fhenda og reikningsfæra** og smellið á hnappinn **Í lagi**.
4. Ef forskoða á reikninginn skal velja hnappinn **Já**.

    > [!NOTE]  
    > Að öllu jöfnu væri afhendingardeildin búin að bóka afhendinguna.  

    Árni geta skoðað ferilinn til að staðfesta að sölureikningurinn var stofnaður eins og til var ætlast.

5. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.  

## Uppfæra stöðu fyrirframgreiddra pantana og reikninga sjálfkrafa

Þú getur flýtt fyrir pöntunar- og reikningsvinnslu með því að setja upp verkraðarfærslur sem uppfæra stöðu þessara skjala sjálfkrafa. Þegar fyrirframgreiðslureikningur er greiddur geta verkraðarfærslurnar sjálfkrafa breytt stöðu skjalsins úr **Bíður fyrirframgreiðslu** í **Útgefið**. Þegar þú setur upp verkraðarfærslurnar eru kóðaeiningarnar sem þú þarft að nota **383 Uppf. fyrirfgr. á sölu í bið** og **383 Uppf. fyrirfgr. á innkaupum í bið**. Mælt er með því að keyra færslurnar reglulega, t.d. á mínútu fresti. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## Næstu skref

Þessi kynning fór yfir eftirfarandi skref til að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að afgreiða fyrirframgreiðslur. 

- Settu upp sjálfgefnar fyrirframgreiðsluprósentur á viðskiptamenn og vörur.
- Notaðu mismunandi aðferðir til að reikna út fyrirframgreiðslurnar í pöntun.  
- Reiknaðu fyrirframgreiðsluupphæðina sem prósentu af samtölu pöntunarinnar.
- Úthlutaðu einni heildarupphæð fyrirframgreiðslunnar á pöntunina.  

Einnig var fyrirframgreiðslureikningur bókaður, annar reikningur stofnaður þegar pöntunin breyttist og lokareikningur fyrir eftirstandandi upphæð var bókaður.  

Möguleikar fyrirframgreiðslu gera þér auðvelt að setja upp og framfylgja reglum um fyrirframgreiðslu fyrir viðskiptamenn og vörur. Þeir gera þér einnig kleift að bóka allar greiðslur á móti reikningi.  

## Sjá einnig .

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
