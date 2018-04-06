---
title: "Kynning - Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu | Microsoft Docs"
description: "Fyrirframgreiðslur eru greiðslur sem eru reikningsfærðar og bókaðar á fyrirframgreiðslupöntun sölu- eða innkaupa áður en lokareikningsfærsla fer fram. Hugsanlega er beðið um innborgun áður en vörur eru framleiddar upp í pöntun eða áður en vörur eru afhentar viðskiptamanni. Fyrirframgreiðslur í Finance and Operations, Business Edition er hægt að nota til að reikningsfæra og innheimta innborganir frá viðskiptamönnum eða senda lánardrottnum innborganir. Þannig má tryggja að allar greiðslur séu bókaðar á móti reikningi."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cd74d543168f1f96f55141aace571d6d701e3de1
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu
Fyrirframgreiðslur eru greiðslur sem eru reikningsfærðar og bókaðar á fyrirframgreiðslupöntun sölu- eða innkaupa áður en lokareikningsfærsla fer fram. Hugsanlega er beðið um innborgun áður en vörur eru framleiddar upp í pöntun eða áður en vörur eru afhentar viðskiptamanni. Fyrirframgreiðslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að nota til að reikningsfæra og innheimta innborganir frá viðskiptamönnum eða senda lánardrottnum innborganir. Þannig má tryggja að allar greiðslur séu bókaðar á móti reikningi.  

 Hægt er að skilgreina skilyrði fyrirframgreiðslu fyrir viðskiptamann eða lánardrottin fyrir allar vörur eða valdar vörur. Þegar uppsetningu er lokið er hægt að búa til fyrirframgreiðslureikninga úr sölu- og innkaupapöntunum fyrir útreiknuðu greiðsluupphæðina. Hægt er að breyta sjálfgefnu upphæðunum á reikningnum eins og þarf. T.d er hægt að senda viðbótarfyrirframgreiðslureikninga ef t.d. vörum er bætt við pöntunina.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
 Þessi kynning fer yfir eftirfarandi aðstæður:  

-   Uppsetning fyrirframgreiðslna  
-   Stofnun pöntunar sem þarf fyrirframgreiðslu  
-   Stofnun fyrirframgreiðslureiknings  
-   Leiðrétting fyrirframgreiðsluþarfa á pöntun  
-   Notkun fyrirframgreiðslna á pöntun  
-   Reikningsfærsla lokaupphæðar á pöntun með fyrirframgreiðslu  

### <a name="roles"></a>Hlutverk  
 Þessi kynning nær yfir verk fyrir eftirfarandi hlutverk:  

-   Aðalbókari (Pála)  
-   Pantanavinnsla (Súsanna)  
-   Innheimtustjóri (Árni)  

## <a name="story"></a>Ferill  
 Pála er aðalbókari. Hún tekur ákvarðanir um hvaða viðskiptamenn þurfa að leggja fram innborgun áður en vörur eru framleiddar eða afhentar. Pála stillir [!INCLUDE[d365fin](includes/d365fin_md.md)] á að reikna fyrirframgreiðslur sjálfvirkt.  

 Súsanna vinnur í sölupöntunarvinnslu. Þegar viðskiptavinur hringir og pantar færir hann pöntunina inn í kerfið meðan viðskiptavinurinn er í símanum. Þannig getur hún staðfest verð og greiðsluskilmála við þann viðskiptamann strax og getur gert leiðréttingar á pöntun meðan hún semur við viðskiptamanninn.  

 Árni vinnur í innheimtudeildinni og sér um bókun reikninga og greiðslna.  

 Í þessu dæmi setur Pála upp fyrirframgreiðsluþarfir fyrir viðskiptamanninn Selangorian, samkvæmt kreditferli fyrirtækisins, og gefur Súsönnu leiðbeiningar um hvernig eigi að vinna pantanir þess.  

 Þegar viðskiptamaðurinn hringir semur Súsanna við hann þar til samkomulagi er náð. Hún getur þá valið að reikna fyrirframgreiðsluna á nokkra mismunandi vegu.  

 Eftir að Súsanna hefur sent fyrirframgreiðslureikninginn, pantar viðskiptamaðurinn aukavöru. Súsanna uppfærir pöntunina og býr til annan fyrirframgreiðslureikning.  

 Árni skráir greiðslu viðskiptamannsins, jafnar hana við reikninga og sendir að lokum lokareikninginn.  

## <a name="setting-up-prepayments"></a>Uppsetning fyrirframgreiðslna  
 Pála setur kerfið upp fyrir fyrirframgreiðslur frá viðskiptamönnum.  

-   Hún ákveður að nota sömu númerröð fyrir fyrirframgreiðslu og er notuð fyrir sölureikningsfærslu.  
-   Pála stillir kerfið á að kanna hvort fyrirframgreiðslu er krafist fyrir lokareikningsfærslu á pöntun.  
-   Hún tilgreinir sjálfgefin gildi hlutfalls fyrirframgreiðslu fyrir tilteknar vörur og viðskiptamenn.  

Eftirfarandi aðgerðir lýsa hvernig Pála framkvæmir þessi verk.  

#### <a name="to-set-up-number-series-for-prepayments"></a>Uppsetning númeraraða fyrir fyrirframgreiðslur  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning Sala & útistandandi** og velja svo viðeigandi tengil.  
2.  Í glugganum **Sölugrunnur** þarf að stækka flýtiflipann **Númeraröð**.  
3.  Ganga þarf úr skugga um að númeraraðirnar fyrir bókaða fyrirframgreiðslureikninga (í reitnum **Bókuð fyrirframgr.reikn.nr.**) séu þær sömu og fyrir bókaða sölureikninga (**Nr.röð bókaðra reikninga**) og númeraraðirnar fyrir bókaða kreditreikninga fyrirframgreiðslu (**Bókuð kr.reikn.nr. fyrirframgr.**) séu þær sömu og fyrir bókaða kreditreikninga (**Nr.röð bókaðra kreditreikninga**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Frysting afhendinga vegna ógreiddra fyrirframgreiðslna  
1.  Í glugganum **Sala & Útistandandi uppsetning**, á flýtiflipanum **Almennt**, er gátreiturinn **Kanna fyrirframgreiðslu við bókun** valinn.

    Ekki er hægt að afhenda eða reikningsfæra pöntun sem er með ógreidda fyrirframgreiðslu.  

Sjálfgefið er að Pála vill að viðskiptamaður 20000 þurfi að greiða 30% af öllum pöntunum fyrirfram. Þar af leiðandi færir hún sjálfgefið hlutfall fyrirframgreiðslu á spjald viðskiptamannsins.  

Pála vill að allir viðskiptamenn þurfi að borga 20% fyrirfram fyrir vöru 1100. Viðskiptamaður 20000 er með lélegan ferill. Þar af leiðandi hún krefst fyrirframgreiðslu 40% af viðskiptamaður 20000 fyrir vöru 1100. Eftirfarandi dæmi sýnir hvernig á að setja upp sjálfgefið hlutfall fyrirframgreiðslu.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Úthlutun sjálfgefins hlutfalls fyrirframgreiðslu á viðskiptamenn og vörur  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamenn** og velja svo viðeigandi tengil.  
2.  Opna spjaldið fyrir viðskiptamann 20000 (Selangorian).
3.  **30** er slegið inn í reitinn **Fyrirframgreiðsla %**.  
4.  Velja hnappinn **Í lagi** til að loka viðskiptamannaspjaldinu.  
5.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.  
6.  Opna spjaldið fyrir viðskiptamann 1100.
7.  Veljið aðgerðina **Fyrirframgreiðsluprósenta**.  
8.  Tvær línur í glugganum **Prósentur fyrirframgreiðslu sölu** eru fylltar út á eftirfarandi hátt.  

    |**Tegund sölu**|**Kóti sölu**|**Vörunr.**|**Fyrirframgreiðsla %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Viðskiptamaður**|**20000**|**1100**|**40**|  
    |**Allir viðskiptamenn**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Einnig þarf að tilgreina skattflokkskóta á flýtiflipanum **Reikningsfærsla** fyrir vörur 1000 og 1100, allt eftir landi/svæði.  

9. Öllum gluggum er lokað.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Til að tilgreina lykil fyrir sölufyrirframgreiðslur í alm. bókunargrunni  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **almennur bókunargrunnur** og velja svo viðeigandi tengil.  
2.  Veljið línuna þar sem reiturinn **Alm. viðsk.bókunarflokkur** er stilltur á **ÚTFL** og reiturinn **Alm. vörubókunarflokkur** er stilltur á **SMÁSALA** og veljið síðan aðgerðina **Breyta**.  
3.  Í glugganum **Alm. bókunargrunnsspjald** í reitnum **Fyrirframgreiðslureikn. sölu** skal tilgreina viðeigandi reikning.  
4.  Velja hnappinn **Í lagi**.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Stofnun pöntunar sem þarf fyrirframgreiðslu  
 Í eftirfarandi dæmi stofnar Súsanna, pantanavinnslan, pöntun útfrá samtali við viðskiptamann. Þær vörur sem viðskiptavinurinn pantar krefjast fyrirframgreiðslu og viðskiptavinurinn hefur áður greitt eftir gjalddaga. Súsanna hefur því fengið fyrirmæli um að krefjast föstu fyrirframgreiðsluupphæðarinnar 2000 fyrir pöntunina.  

Viðskiptamaðurinn biður um að fá að borga 35%, sem Súsanna getur samþykkt. Hún breytir því pöntuninni.  

Hún stofnar fyrirframgreiðslureikning og sendir hann til viðskiptamannsins.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Stofnun sölupöntunar með fyrirframgreiðslu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3.  Í reitnum **Selt til Viðskm.nr.**. skal velja **20000**.  
5.  Samþykkja skal viðvörun um vanskil sem birtist.  
6.  Tvær sölulínur eru fylltar út með eftirfarandi upplýsingum.  

    |**Tegund**|**Nr.**|**Magn**|  
    |--------------|-------------|------------------|  
    |**Vara**|**1000**|**1**|  
    |**Vara**|**1100**|**1**|

    Fyrirframgreiðslureitirnir á sölulínunni eru sjálfgefið faldir. Þá þarf að kalla fram.  

7. Ganga þarf úr skugga um að í reitnum **Fyrirframgreiðsla %** á línunni með vöru **1000** standi **30**. Sjálfgefið gildi er tekið úr söluhausnum sem var fylltur út með viðskiptamannsspjaldinu.  

    Í reitnum **Fyrirframgreiðsla %** á línunni með vörunni **1100** stendur **40**. Þetta er prósentan sem var færð inn í gluggann **Prósentur fyrirframgreiðslu sölu** fyrir vöru **1100** og viðskiptamann **20000**.  

    Nánari upplýsingar um það eru í [Setja upp fyrirframgreiðslur](finance-set-up-prepayments.md).  
8. Veldu **Upplýsingar** aðgerðina.  
9. Á flýtiflipanum **Fyrirframgreiðsla**, inniheldur reiturinn **Línuupphæð fyrirframgr. án VSK** **1,560**. Ef fyrirframgreiðslureikningur er stofnaður fyrir pöntunina núna er þetta upphæðin sem er birt á reikningnum.  

    Í þessu dæmi hefur Súsanna fyrirmæli um að nota fyrirframgreiðslu upp á 2000 á pöntunina.  

    > [!IMPORTANT]  
    >  Eftirfarandi skref gætu ekki átt við, allt eftir landi/svæði.  
10. Upphæðinni í reitnum **Línuupphæð fyrirframgr. án VSK** er breytt í **2000** og glugganum því næst lokað.  
11. Þegar reiturinn **Fyrirframgreiðsla %** á sölulínunni er skoðaður sést að hann hefur verið endurreiknaður í **40.81625**.  

    Endurreikningurinn nær yfir allar línur sem eru með fyrirframgreiðsluprósentu sem er hærri en 0.  

    Nú spyr viðskiptamaðurinn hvort hægt sé að hafa fyrirframgreiðsluna 35%. Yfirmaður Súsönnu samþykkir breytinguna.  

12. Í gluggann **Sölupöntun** á reitnum **Fyrirframgreiðsla %** er fært inn **35**.  
13. Í viðvörunarglugganum sem birtist velurðu **Já** hnappinn. 35% gjald verður notaður sem fyrirframgreiðsluprósenta fyrir alla pöntunina.  
14. Staðfesta að línurnar hafi verið uppfærðar í samræmi við þetta.  

## <a name="creating-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings  
Þegar Súsanna hefur fært inn rétt fyrirframgreiðslugildi á pöntunina stofnar hún fyrirframgreiðslureikninga og sendir á viðskiptamanninn.  

#### <a name="to-create-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings  

1.  Í glugganum **sölupöntun** skal velja aðgerðina **bóka fyrirframgreiðslureikningur**.  

> [!NOTE]  
>  Súsanna myndi velja **Bóka og prenta fyrirframgr.reikning** og senda reikninginn til viðskiptamannsins.  

## <a name="creating-an-additional-prepayment-invoice"></a>Stofnun annars fyrirframgreiðslureiknings  
Næsta dag hringir viðskiptamaðurinn í Súsönnu og gerir breytingar á pöntuninni. Hann vill tvennt af vöru 1100. Súsanna opnar pöntunina og uppfærir hana, stofnar annan fyrirframgreiðslureikning á pöntuninni og sendir hann til viðskiptavinarins.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Stofnun annars fyrirframgreiðslureiknings  

1.  Í glugganum **sölupöntun** skal velja aðgerðina **enduropna**.  
2.  Á línunni fyrir vöruna **1100** er **2** fært inn í reitinn **Magn**.  

    Flett er til að skoða fyrirframgreiðslureiti. Reiturinn **Línuupphæð fyrirframgreiðslu án VSK** inniheldur nú **630** og reiturinn **Reikn. fyrirfr.gr.upphæð. án VSK** inniheldur **315**. Þetta sýnir að til er önnur fyrirframgreiðsluupphæð sem hefur ekki verið reikningsfærð ennþá.  
3.  Til að bóka reikning fyrir aðra fyrirframgreiðslu er farið í flipann **Aðgerðir** , flokkinn **Bókun** , **Fyrirframgreiðsla**valin og síðan **Bóka fyrirframgreiðslureikning**.  

## <a name="applying-the-prepayments"></a>Jöfnun fyrirframgreiðslu  
Viðskiptamaðurinn borgar fyrirframgreiðsluna og Árni, í innheimtudeildinni, skráir greiðsluna og jafnar hana við fyrirframgreiðslureikningana.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Jöfnun greiðslu við fyrirframgreiðslureikninga  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **inngreiðslubók** og velja svo viðeigandi tengil.  
2.  Færslubókarlínan er fyllt út með eftirfarandi upplýsingum.  

    |Heiti reits|Innfært|  
    |----------------|-----------|  
    |**Tegund fylgiskjals**|**Greiðsla**|  
    |**Tegund reiknings**|**Viðskiptamaður**|  
    |**Reikningur nr.**|**20000**|  
3. Valið er **Jafna Færslur** aðgerð.  
4.  Í glugganum **Jafna viðskm.færslur** er fyrsti fyrirframgreiðslureikningurinn valinn og svo er aðgerðin **Setja kenni jöfnunar** valin.  
5.  Endurtaka skal fyrri skref fyrir seinni fyrirframgreiðsluna.  
6.  Velja hnappinn **Í lagi**.  

    Upphæðarreiturinn inniheldur núna samtölu fyrirframgreiðslureikninganna tveggja.  

7.  Bóka skal færslubókina.  

## <a name="invoicing-the-remaining-amount"></a>Reikningsfærsla eftirstandandi upphæðar  
Árna hefur verið tilkynnt að vörurnar á pöntuninni hafi verið afhentar og að pöntunin sé tilbúin til reikningsfærslu. Árni stofnar því reikning fyrir pöntunina.  

#### <a name="to-invoice-the-remaining-amount"></a>Reikningsfærsla eftirstandandi upphæðar  
1. Sölupöntunin er opnuð.  
2. Veldu aðgerðina **Afgreiða og reikningsfæra** og veldu síðan **Í lagi** hnappinn.  

> [!NOTE]  
>  Að öllu jöfnu væri afhendingardeildin búin að bóka afhendinguna.  

Árni geta skoðað ferilinn til að staðfesta að sölureikningurinn var stofnaður eins og til var ætlast.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bókaðir sölureikningar** og velja svo viðeigandi tengil.  

## <a name="next-steps"></a>Næstu þrep  
Í þessari kynningu var farið í gegnum uppsetningu á vinnslu fyrirframgreiðslna í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Sett var upp sjálfgefin fyrirframgreiðsluprósentu á viðskiptamenn og vörur, auk þess sem notaðar voru mismunandi aðferðir til að reikna fyrirframgreiðslur á pöntun. Einni heildarupphæð fyrirframgreiðslu var úthlutað á pöntun og upphæð fyrirframgreiðslu var reiknuð sem hlutfall af pöntuninni í heild sinni.  

Einnig var fyrirframgreiðslureikningur bókaður, annar reikningur stofnaður þegar pöntunin breyttist og lokareikningur fyrir eftirstandandi upphæð var bókaður.  

Fyrirframgreiðslueiginleikinn í [!INCLUDE[d365fin](includes/d365fin_md.md)] einfaldar uppsetningu og innleiðingu fyrirframgreiðslureglna fyrir viðskiptamenn og vörur, auk þess sem hann býður upp á bókun allra greiðslna gegn reikningi.  

## <a name="see-also"></a>Sjá einnig  
[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)

