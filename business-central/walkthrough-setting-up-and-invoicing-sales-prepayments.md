---
title: Kynning a uppsetningu og reikningsfærslu fyrirframgreiðslna fyrir sölu
description: Fyrirframgreiðslur eru greiðslur sem eru reikningsfærðar og bókaðar á fyrirframgreiðslupöntun sölu- eða innkaupa áður en lokareikningsfærsla fer fram. Hugsanlega er beðið um innborgun áður en vörur eru framleiddar upp í pöntun eða áður en vörur eru afhentar viðskiptamanni. Fyrirframgreiðslur í Business Central er hægt að nota til að reikningsfæra og innheimta innborganir frá viðskiptamönnum eða senda lánardrottnum innborganir. Þannig má tryggja að allar greiðslur séu bókaðar á móti reikningi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/25/2021
ms.author: edupont
ms.openlocfilehash: dacf9e5492f583513e69f2316a0440fce2597269
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216181"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Fyrirframgreiðslur eru greiðslur sem eru reikningsfærðar og bókaðar á fyrirframgreiðslupöntun sölu- eða innkaupa áður en lokareikningsfærsla fer fram. Hugsanlega er beðið um innborgun áður en vörur eru framleiddar upp í pöntun eða áður en vörur eru afhentar viðskiptamanni. Fyrirframgreiðslur í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að nota til að reikningsfæra og innheimta innborganir frá viðskiptamönnum eða senda lánardrottnum innborganir. Þannig má tryggja að allar greiðslur séu bókaðar á móti reikningi.  

Hægt er að skilgreina skilyrði fyrirframgreiðslu fyrir viðskiptamann eða lánardrottin fyrir allar vörur eða valdar vörur. Þegar uppsetningu er lokið er hægt að búa til fyrirframgreiðslureikninga úr sölu- og innkaupapöntunum fyrir útreiknuðu greiðsluupphæðina. Hægt er að breyta sjálfgefnu upphæðunum á reikningnum eins og þarf. T.d er hægt að senda viðbótarfyrirframgreiðslureikninga ef t.d. vörum er bætt við pöntunina.  

## <a name="about-this-walkthrough"></a>Um kynninguna  

Þessi kynning fer yfir eftirfarandi aðstæður:  

-  Uppsetning fyrirframgreiðslna  
-  Stofnun pöntunar sem þarf fyrirframgreiðslu  
-  Stofnun fyrirframgreiðslureiknings  
-  Leiðrétting fyrirframgreiðsluþarfa á pöntun  
-  Notkun fyrirframgreiðslna á pöntun  
-  Reikningsfærsla lokaupphæðar á pöntun með fyrirframgreiðslu  

### <a name="roles"></a>Hlutverk

Þessi kynning nær yfir verk fyrir eftirfarandi hlutverk:  

-  Aðalbókari (Pála)  
-  Pantanavinnsla (Súsanna)  
-  Innheimtustjóri (Árni)  

## <a name="story"></a>Ferill

 Pála er aðalbókari. Hún tekur ákvarðanir um hvaða viðskiptamenn þurfa að leggja fram innborgun áður en vörur eru framleiddar eða afhentar. Pála stillir [!INCLUDE[prod_short](includes/prod_short.md)] á að reikna fyrirframgreiðslur sjálfvirkt.  

 Súsanna vinnur í sölupöntunarvinnslu. Þegar viðskiptavinur hringir og pantar færir hann pöntunina inn í kerfið meðan viðskiptavinurinn er í símanum. Þannig getur hún staðfest verð og greiðsluskilmála við þann viðskiptamann strax og getur gert leiðréttingar á pöntun meðan hún semur við viðskiptamanninn.  

 Árni vinnur í innheimtudeildinni og sér um bókun reikninga og greiðslna.  

 Í þessu dæmi setur Pála upp fyrirframgreiðsluþarfir fyrir viðskiptamanninn Selangorian, samkvæmt kreditferli fyrirtækisins, og gefur Súsönnu leiðbeiningar um hvernig eigi að vinna pantanir þess.  

 Þegar viðskiptamaðurinn hringir semur Súsanna við hann þar til samkomulagi er náð. Hún getur þá valið að reikna fyrirframgreiðsluna á nokkra mismunandi vegu.  

 Eftir að Súsanna hefur sent fyrirframgreiðslureikninginn, pantar viðskiptamaðurinn aukavöru. Súsanna uppfærir pöntunina og býr til annan fyrirframgreiðslureikning.  

 Árni skráir greiðslu viðskiptamannsins, jafnar hana við reikninga og sendir að lokum lokareikninginn.  

## <a name="setting-up-prepayments"></a>Uppsetning fyrirframgreiðslna

Pála setur kerfið upp fyrir fyrirframgreiðslur frá viðskiptamönnum.  

-  Hún ákveður að nota sömu númerröð fyrir fyrirframgreiðslu og er notuð fyrir sölureikningsfærslu.  
-  Pála stillir forritið á að kanna hvort fyrirframgreiðslu er krafist fyrir lokareikningsfærslu á pöntun.  
-  Hún tilgreinir sjálfgefin gildi hlutfalls fyrirframgreiðslu fyrir tilteknar vörur og viðskiptamenn.  

Eftirfarandi aðgerðir lýsa hvernig Pála framkvæmir þessi verk.  

#### <a name="to-set-up-number-series-for-prepayments"></a>Uppsetning númeraraða fyrir fyrirframgreiðslur

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölugrunnur** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Setja upp sölugrunn** skal stækka flýtiflipann **Númeraröð**.  
3.  Ganga þarf úr skugga um að númeraraðirnar fyrir bókaða fyrirframgreiðslureikninga (í reitnum **Bókuð fyrirframgr.reikn.nr.**) séu þær sömu og fyrir bókaða sölureikninga (**Nr.röð bókaðra reikninga**) og númeraraðirnar fyrir bókaða kreditreikninga fyrirframgreiðslu (**Bókuð kr.reikn.nr. fyrirframgr.**) séu þær sömu og fyrir bókaða kreditreikninga (**Nr.röð bókaðra kreditreikninga**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Frysting afhendinga vegna ógreiddra fyrirframgreiðslna

1.  Á síðunni **Sala & Útistandandi uppsetning**, á flýtiflipanum **Almennt**, er gátreiturinn **Kanna fyrirframgreiðslu við bókun** valinn.

Ekki er hægt að afhenda eða reikningsfæra pöntun sem er með ógreidda fyrirframgreiðslu.  

Sjálfgefið er að Pála vill að viðskiptamaður 20000 þurfi að greiða 30% af öllum pöntunum fyrirfram. Þar af leiðandi færir hún sjálfgefið hlutfall fyrirframgreiðslu á spjald viðskiptamannsins.  

Pála vill að allir viðskiptamenn þurfi að borga 20% fyrirfram fyrir vöru 1896-S. Viðskiptamaður 20000 er með lélegan ferill. Þess vegna krefst hún 40% fyrirframgreiðslu frá viðskiptavini 20000 fyrir vöru 1896-S. Eftirfarandi dæmi sýnir hvernig á að setja upp sjálfgefið hlutfall fyrirframgreiðslu.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Úthlutun sjálfgefins hlutfalls fyrirframgreiðslu á viðskiptamenn og vörur

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.  
2.  Opnaðu spjaldið fyrir viðskiptamann 20000 (Trey Research).
3.  Í reitinn **Fyrirframgreiðsla %** skal slá inn **30**.  
4.  Veldu **Tengd** og síðan **SaLA** og **fyrirframgreiðsluprósenta**
5.  Tvær línur á síðunni **Prósentur fyrirframgreiðslu sölu** eru fylltar út á eftirfarandi hátt.  

    |**Tegund sölu**|**Kóti sölu**|**Vörunr.**|**Fyrirframgreiðsla %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Viðskiptamaður**|**20000**|**1896-S**|**40**|  
    |**Allir viðskiptamenn**| |**1896-S**|**20**|  

    > [!IMPORTANT]  
    >  Einnig þarf að tilgreina skattflokkskóða á flýtiflipanum **Reikningsfærsla** fyrir vöru 1896-S.  

6.  Loka öllum síðum.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Til að tilgreina lykil fyrir sölufyrirframgreiðslur í alm. bókunargrunni

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Almennur bókunargrunnur** og veldu síðan tengda tengilinn.  
2.  Veldu línuna þar sem reiturinn **Alm. viðsk.bókunarflokkur** er stilltur á **INNLENT** og reiturinn **Alm. vörubókunarflokkur** er stilltur á **SMÁSALA**.  
3.  Í reitnum **Fyrirframgreiðslureikn. sölu** skal tilgreina viðeigandi reikning. Valið er vistað sjálfkrafa.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Stofnun pöntunar sem þarf fyrirframgreiðslu

 Í eftirfarandi dæmi stofnar Súsanna, pantanavinnslan, pöntun útfrá samtali við viðskiptamann. Þær vörur sem viðskiptavinurinn pantar krefjast fyrirframgreiðslu og viðskiptavinurinn hefur áður greitt eftir gjalddaga. Súsanna hefur því fengið fyrirmæli um að krefjast föstu fyrirframgreiðsluupphæðarinnar **800** fyrir pöntunina.  

Viðskiptamaðurinn biður um að fá að borga 35%, sem Súsanna getur samþykkt. Hún breytir því pöntuninni.  

Hún stofnar fyrirframgreiðslureikning og sendir hann til viðskiptamannsins.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Stofnun sölupöntunar með fyrirframgreiðslu

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2.  Valið er aðgerðin **Nýtt**.  
3.  Fyrir **Númer viðskiptamanns** skal velja **20000**.  
4.  Loka skal viðvörun um vanskil sem birtist.  
5.  Tvær sölulínur eru fylltar út með eftirfarandi upplýsingum.  

    |**Tegund**|**Nr.**|**Magn**|  
    |--------------|-------------|------------------|  
    |**Vara**|**1896-S**|**1**|  
    |**Vara**|**1900-S**|**1**|

    Fyrirframgreiðslureitirnir á sölulínunni eru sjálfgefið faldir. Þá þarf að kalla fram. Til að gera þetta þarftu að sérstilla síðuna. Frekari upplýsingar eru í [Hefja sérstillingu á síðu með borðanum Sérstilla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6.  Ganga þarf úr skugga um að í reitnum **Fyrirframgreiðsla %** á línunni með vöru **1900-S** standi **30**. Sjálfgefið gildi er tekið úr söluhausnum sem var fylltur út með viðskiptamannsspjaldinu.  

    Í reitnum **Fyrirframgreiðsla %** á línunni með vörunni **1896-S** stendur **40**. Þetta er prósentan sem var færð inn á síðunni **Prósentur fyrirframgreiðslu sölu** fyrir vöru **1896-S** og viðskiptamann **20000**.  

    Nánari upplýsingar um það eru í [Setja upp fyrirframgreiðslur](finance-set-up-prepayments.md).  
7.  Í aðgerðinni **Pöntun** skal velja **Upplýsingar**.  
8.  Á flýtiflipanum **Fyrirframgreiðsla**, inniheldur reiturinn **Línuupphæð fyrirframgr. án VSK** **458.16**. Ef fyrirframgreiðslureikningur er stofnaður fyrir pöntunina núna er þetta upphæðin sem er birt á reikningnum.  

    Í þessu dæmi hefur Súsanna fyrirmæli um að nota fyrirframgreiðslu upp á **800** á pöntunina.  

    > [!IMPORTANT]  
    >  Eftirfarandi skref gætu ekki átt við, allt eftir landi/svæði.  
9.  Upphæðinni í reitnum **Línuupphæð fyrirframgr. án skatts** er breytt í **800** og síðunni því næst lokað.  
10.  Þegar reiturinn **Fyrirframgreiðsla %** á sölulínunni er skoðaður sést að hann hefur verið endurreiknaður í **67,02438** og **67,02282**.  

     Endurreikningurinn nær yfir allar línur sem eru með fyrirframgreiðsluprósentu sem er hærri en 0.  

     Nú spyr viðskiptamaðurinn hvort hægt sé að hafa fyrirframgreiðsluna 35%. Yfirmaður Súsönnu samþykkir breytinguna.
11.  Á síðunni **Sölupöntun** á reitnum **Fyrirframgreiðsla** í **Fyrirframgreiðsla %** er fært inn **35**.  
12.  Í viðvörunarglugganum sem birtist velurðu **Já** hnappinn. 35% gjald verður notaður sem fyrirframgreiðsluprósenta fyrir alla pöntunina.  
13.  Staðfesta að línurnar hafi verið uppfærðar í samræmi við þetta.  

## <a name="creating-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings  
Þegar Súsanna hefur fært inn rétt fyrirframgreiðslugildi á pöntunina stofnar hún fyrirframgreiðslureikninga og sendir á viðskiptamanninn.  

#### <a name="to-create-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings

1.  Á síðunni **Sölupöntun** skal velja **Aðgerðir**, síðan **Bókun**, síðan **Fyrirframgreiðsla** og síðan er valin **Bóka og prenta fyrirframgreiðslureikning**
2.  Veldu **Já** til að bóka reikninginn.  

> [!NOTE]  
>  Súsanna myndi velja **Bóka og prenta fyrirframgr.reikning** og senda reikninginn til viðskiptamannsins.  

## <a name="creating-an-additional-prepayment-invoice"></a>Stofnun annars fyrirframgreiðslureiknings

Næsta dag hringir viðskiptamaðurinn í Súsönnu og gerir breytingar á pöntuninni. Hann vill tvennt af vöru 1100. Súsanna opnar pöntunina og uppfærir hana, stofnar annan fyrirframgreiðslureikning á pöntuninni og sendir hann til viðskiptavinarins.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Stofnun annars fyrirframgreiðslureiknings

1.  Á síðunni **Sölupöntun** skal velja aðgerðina **Losa** og síðan **Enduropna**.  
2.  Á línunni fyrir vöruna **1896-S**, í reitnum **Magn** skal slá inn **2**.  

    Í aðgerðinni **Pöntun** skal velja **Upplýsingar**. Reiturinn **Línuupphæð fyrirframgreiðslu án VSK** inniheldur nú **768.04** og reiturinn **Reikn. fyrirfr.gr.upphæð. án VSK** inniheldur **417.76**. Þetta sýnir að til er önnur fyrirframgreiðsluupphæð sem hefur ekki verið reikningsfærð ennþá.  
3.  Til að bóka reikning fyrir aðra fyrirframgreiðslu er valin **Aðgerðir**, síðan **Bókun**, síðan **Fyrirframgreiðsla** og síðan er valin **Bóka og prenta fyrirframgreiðslureikning**
4.  Veldu **Já** til að bóka reikninginn.  

## <a name="applying-the-prepayments"></a>Jöfnun fyrirframgreiðslu  
Viðskiptamaðurinn borgar fyrirframgreiðsluna og Árni, í innheimtudeildinni, skráir greiðsluna og jafnar hana við fyrirframgreiðslureikningana.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Jöfnun greiðslu við fyrirframgreiðslureikninga

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Inngreiðslubækur** og veldu síðan tengda tengilinn.  
2.  Færslubókarlínan er fyllt út með eftirfarandi upplýsingum.  

    |Heiti reits|Innfært|  
    |----------------|-----------|  
    |**Tegund fylgiskjals**|**Greiðsla**|  
    |**Tegund reiknings**|**Viðskiptamaður**|  
    |**Reikningur nr.**|**20000**|  
3.  Veldu aðgerðina **Ferli** og síðan **Jafna færslur**.  
4.  Á síðunni **Jafna viðskm.færslur** er fyrsti fyrirframgreiðslureikningurinn valinn og svo aðgerðin **Ferli** og **Setja kenni jöfnunar**.  
5.  Endurtaka skal fyrri skref fyrir seinni fyrirframgreiðsluna.  
6.  Velja hnappinn **Í lagi**.  

    Upphæðarreiturinn inniheldur núna samtölu fyrirframgreiðslureikninganna tveggja.  

7.  Til að bóka færslubókina velurðu **Bóka/Prenta** og síðan **Bóka**.
8.  Velja hnappinn **Já**.

## <a name="invoicing-the-remaining-amount"></a>Reikningsfærsla eftirstandandi upphæðar

Árna hefur verið tilkynnt að vörurnar á pöntuninni hafi verið afhentar og að pöntunin sé tilbúin til reikningsfærslu. Árni stofnar því reikning fyrir pöntunina.  

#### <a name="to-invoice-the-remaining-amount"></a>Reikningsfærsla eftirstandandi upphæðar

1.  Sölupöntunin er opnuð.
2.  Veldu aðgerðina **Bókun** og svo **Bóka**.
3.  Veljið **fhenda og reikningsfæra** og smellið á hnappinn **Í lagi**.
4.  Ef forskoða á reikninginn skal velja hnappinn **Já**.

> [!NOTE]  
>  Að öllu jöfnu væri afhendingardeildin búin að bóka afhendinguna.  

Árni geta skoðað ferilinn til að staðfesta að sölureikningurinn var stofnaður eins og til var ætlast.

1.  Veldu táknið ![Ljósapera sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), sláðu inn **Bókaðir sölureikningar** og veldu síðan tengda tengilinn.  

## <a name="next-steps"></a>Næstu þrep

Í þessari kynningu var farið í gegnum uppsetningu á vinnslu fyrirframgreiðslna í [!INCLUDE[prod_short](includes/prod_short.md)]. Sett var upp sjálfgefin fyrirframgreiðsluprósentu á viðskiptamenn og vörur, auk þess sem notaðar voru mismunandi aðferðir til að reikna fyrirframgreiðslur á pöntun. Einni heildarupphæð fyrirframgreiðslu var úthlutað á pöntun og upphæð fyrirframgreiðslu var reiknuð sem hlutfall af pöntuninni í heild sinni.  

Einnig var fyrirframgreiðslureikningur bókaður, annar reikningur stofnaður þegar pöntunin breyttist og lokareikningur fyrir eftirstandandi upphæð var bókaður.  

Fyrirframgreiðslueiginleikinn í [!INCLUDE[prod_short](includes/prod_short.md)] einfaldar uppsetningu og innleiðingu fyrirframgreiðslureglna fyrir viðskiptamenn og vörur, auk þess sem hann býður upp á bókun allra greiðslna gegn reikningi.  

## <a name="see-also"></a>Sjá einnig  
[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
