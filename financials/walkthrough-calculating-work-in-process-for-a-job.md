---
title: "Kynning - Útreikningur á VÍV fyrir verk | Microsoft Docs"
description: "Með verkum er hægt að áætla notkun á forða fyrirtækisins og rakningu á ýmsum kostnaði sem fylgir notkun forða í tilteknu verkefni. Verk ná yfir notkun á vinnutíma starfsmanna, vélastundir, birgðahluti og aðrar gerðir notkunar sem þarf að fylgjast með í verkferlum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2c043a33e02d197281877a8287df7008377d52e4
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-calculating-work-in-process-for-a-job"></a>Kynning: Útreikningur á VÍV fyrir verk
Með verkum er hægt að áætla notkun á forða fyrirtækisins og rakningu á ýmsum kostnaði sem fylgir notkun forða í tilteknu verkefni. Verk ná yfir notkun á vinnutíma starfsmanna, vélastundir, birgðahluti og aðrar gerðir notkunar sem þarf að fylgjast með í verkferlum. Ef verk stendur yfir í langan tíma verður hugsanlega að flytja þennan kostnað á VÍV-reikning (verk í vinnslu) á efnahagsreikningi á meðan verkinu er lokið. Þannig er hægt að samþykkja kostnaðinn og söluna á rekstrarreikningnum þegar það á við.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
 Þessi kynning fjallar um eftirfarandi verk:  

-   Útreikning á VÍV.  
-   Val á VÍV-útreikningsaðferð.  
-   Undanskil á verkhluta frá VÍV.  
-   Bókun VÍV í fjárhag.  
-   Bakfærslu á VÍV-bókun.  

 Hvert skref í ferlinu virðisreiknar og færir verkfærslurnar í fjárhaginn. Útreikningur og bókun eru aðskilin svo hægt sé að fara yfir gögn og gera breytingar áður en bókað er í fjárhaginn. Þess vegna þarf að ganga úr skugga um að allar upplýsingar séu réttar eftir að útreikningskeyrslur eru keyrðar og áður en bókunarkeyrslur eru keyrðar.  

## <a name="roles"></a>Hlutverk  
 Þessi kynning notar Tinnu sem meðlim verkefnateymisins.  

## <a name="prerequisites"></a>Frumskilyrði  
 Áður en hægt er að framkvæma verk hér í kynningunni þarf að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)] í tölvunni.  

## <a name="story"></a>Ferill  
 Þessi kynning einblínir á fyrirtækið CRONUS International Ltd., hönnunar- og ráðgjafafyrirtæki sem hannar og setur upp nýja innviði á borð við ráðstefnusali og skrifstofur, með húsgögn, aukahluti og geymslueiningar. Mest vinnan í Cronus er verkefnatengd og Tinna, meðlimur í verkefnateymi, notar verk til að geta haft yfirlit yfir hvert verk í vinnslu sem Cronus hefur verið ræst en einnig þau verk sem lokið er. Sum verkin geta verið mjög löng og tekið marga mánuði. Tinna getur notað VÍV reikninginn til að skrá yfirstandandi vinnu og rekja kostnað í verkinu.  

## <a name="calculating-wip"></a>Útreikningur á VÍV  
 Cronus hefur tekið að sér langt verk sem nær yfir nokkur skýrslutímabil. Tinna, sem er teymismeðlimur í verkefninu, reiknar út verk í vinnslu (VÍV) til að tryggja að ársreikningur fyrirtækisins verði réttur.  

 Tinna mun velja tiltekinn hóp verkhluta sem tekin verða með í VÍV-útreikninginn. Í glugganum **Verkhlutalínur verks** getur hún tilgreint þessar línur í dálkinum **VÍV-samtala**.  

 Eftirfarandi tafla lýsir valkostunum þremur.  

|Svæði|Description|  
|-------------------------------------|---------------------------------------|  
|**<blank>**|Haft autt ef verkhlutinn er hluti af hópi verkhluta.|  
|**Samtals**|Skilgreinir svið eða hóp verkhluta sem eru innifaldir í VÍV og samþykkisútreikningi. Innan flokksins mun hver verkhluti með **Tegund verkhluta** stillta á **Bókun** tekinn með í VÍV-samtölunni, nema að reiturinn **VÍV-samtala** er stilltur á **Útilokað**.|  
|**Útilokað**|Á aðeins við verk með **Verkhlutategund verks** sem **Bókun**. Verkið er ekki haft með þegar í verk í vinnslu og samþykktir eru reiknaðar.|  

 Í eftirfarandi kynningu beitir Trausti Kostnaðarvirðisaðferðinni, sem er stöðluð aðferð í fyrirtæki hans, til að reikna VÍV. Hún tilgreinir hvaða hluti af verkinu verður með í VÍV-útreikningnum með því að úthluta VÍV-Heildargildum til ýmissa verkhlutalína.  

### <a name="to-calculate-wip"></a>Útreikningur VÍV  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.  
2.  Á listanum **Verk** er verkinu **Deerfield** valin og svo er valin aðgerðin **Breyta**. Þetta opnar verkspjaldið í breytingastillingu.  

     Hægt er að reikna VÍV eftir Kostnaðarvirði, Söluvirði, Sölukostnaði, Prósentum lokið eða Samningi lokið. Í þessu dæmi, notar Cronus aðferðina kostnaðarvirði.  

3.  Á flýtiflipanum **Bókun** í reitnum **VÍV-aðferð** og síðan valið **Kostnaðarvirði**.  
4.  Veldu aðgerðina **Verkhlutalínur** og stilltu eftirfarandi gildi í **VÍV-samtals** reitnum.  

     Eftirfarandi tafla lýsir gildunum.  

    |Verkhlutanr. verks|VÍV-samtala|  
    |------------------|----------------------|  
    |1130|Útilokað|  
    |1190|Samtals|  
    |1210|Útilokað|  
    |1310|Útilokað|  

5.  Veljið aðgerðina **VÍV** og svo aðgerðina **Reikna VÍV**.  
6.  Í glugganum **Reikna út VÍG** er hægt að velja verk sem á að reikna VÍV fyrir. Á flýtiflipanum **Verk** skal velja **Deerfield** í reitnum **Nr.**. .  
7.  Í reitnum **Bókunardags.** færið inn dagsetningu sem er síðar en vinnudagsetningu.
8.  Fært er inn **1** í reitinn **Númer fylgiskjals**. Þetta stofnar skjal sem síðar er hægt að vísa í fyrir rekjanleika.  
9. Veldu hnappinn **Í lagi** til að ræsa keyrsluna. Skilaboð birtast. Velja hnappinn **Í lagi** til að halda áfram. Glugganum **Verkhlutalínur** er lokað.  

    > [!NOTE]  
    >  Skilaboðin tilgreina að um viðvaranir sé að ræða sem tengjast VÍV-útreikningnum. Fara þarf yfir viðvaranirnar í næsta ferli.  

10. Á spjaldinu **Verk** er stækkaður flýtiflipinn **VÍV og samþykki** til að sjá reiknuð gildi. Einnig er hægt að sjá **Bókunardagsetning VÍV** og gildin sem hafa verið bókuð í fjárhag, ef einhver eru.  

 Athugið að gildið fyrir **Samþ. kostnaðarupphæð** er 215.60 í dálknum **Til að bóka**. Þetta speglar heildarkostnað tveggja af vörunum í flokki verkhluta 1110-1130.  Þriðja varan var stillt á **Útilokað** og er því ekki talin með í VÍV-útreikningnum.  

### <a name="to-review-wip-warnings"></a>Til að fara yfir viðvaranir VÍV  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk VÍV Stjórnklefi** og velja svo viðeigandi tengil.  
2.  Veljið verkið **Deerfield** og svo er valin aðgerðin **Sýna**.  
3.  Í glugganum **VÍV-viðvaranir verks** skal fara yfir viðvörunina sem tengist verkinu.  

 Eftir bókhaldstímabilið þarf Tinna að endurreikna VÍV til að taka með þá vinnu sem unnin hefur verið.  

### <a name="to-recalculate-wip"></a>VÍV endurreiknað  

1.  Á spjaldinu **Verk**, skal velja**VÍV-færslur** til að skoða VÍV-útreikningur.  

     Glugginn **VÍV-færslur verks** sýnir VÍV-færslur sem síðast voru reiknaðar fyrir verkið, jafnvel þótt VÍV hafi ekki verið bókað í fjárhaginn.  

2.  Hægt er að fylgja skrefunum í leiðbeiningunum sem útskýrir hvernig reikna á VÍV til að endurreikna VÍV. Í hvert skipti sem VÍV er reiknað er færsla stofnuð í glugganum **VÍV-færslur verks**.  
3.  Glugganum er lokað.  

> [!NOTE]  
>  Verk í vinnslu og samþykki eru bara reiknuð. Er ekki bókað í fjárhag. Til þess þarf að keyra keyrsluna **Bóka VÍV í fjárhag** þegar búið er að reikna VÍV og samþykki.

## <a name="posting-wip-to-general-ledger"></a>VÍV bókað í fjárhag  
 Þegar Tinna hefur reiknað VÍV fyrir þetta verk getur hún bókað það í fjárhaginn.  

### <a name="to-post-wip-to-general-ledger"></a>VÍV bókað í fjárhag  

1.  Í listanum **Verk** er línan með verkinu **Deerfield** valin.  
2.  Veljið aðgerðina **VÍV** og svo aðgerðina **Bóka VÍV í fjárhag**.  
3.  Í glugganum **Verk Bóka VÍV í fjárhag** á flýtiflipanum **Verk** er **Deerfield** valið í reitnum **Nr.**. .  
4.  Á flýtiflipanum **Valkostir** í reitnum **Fylgiskjalsnr. bakfærslu** er **1** fært inn.  
5.  Velja hnappinn **Í lagi** til að bóka VÍV í fjárhag.  
6.  Velja hnappinn **Í lagi** til að loka staðfestingarglugganum.  

     Eftir að gengið hefur verið frá bókun er hægt að skoða upplýsingar um bókun í glugganum **Fjárhagsfærslur VÍV**.  

7.  Á listanum **Verk** er verkinu **Deerfield** valin og svo er valin aðgerðin **VÍV fjárhagsfærslur**.  

     Í glugganum **VÍV-fjárhagsfærslur verks** er hægt að staðfesta að VÍV hafi verið bókað í fjárhag.  

8.  Glugganum er lokað.  
9. Spjaldið **Verk** fyrir verkið **Deerfield** er opnað.  
10. Á flýtiflipanum **VÍV og samþykki** skal athuga að í dálkinum **Bókað** er reiturinn **Samþ. fjárhagsupph. kostnaðar** nú útfylltur, sem þýðir að það tókst að bóka VÍV í fjárhag.  
11. Velja hnappinn **Í lagi** til að loka spjaldinu.  

## <a name="reversing-a-wip-posting"></a>Bakfærsla VÍV-bókunar  
 Tinna ákveður að reikna hefði átt þá verkhluta verks sem ekki voru hafðir með í VÍV í VÍV. Hún getur bakfært rangar bókanir án þess að bóka nýjar VÍV-bókanir.  

### <a name="to-reverse-a-wip-posting"></a>Bakfærsla VÍV-bókunar  

1.  Í listanum **Verk** er línan með verkinu **Deerfield** valin.  
2.  Veljið aðgerðina **VÍV** og svo aðgerðina **Bóka VÍV í fjárhag**.  
3.  Í glugganum **Verk Bóka í VÍV í fjárhag** á flýtiflipanum **Verk** er **Deerfield** valið í reitnum **Nr.**. .  
4.  Á flýtiflipanum **Valkostir** í reitnum **Fylgiskjalsnr. bakfærslu** er **1** fært inn.  
5.  Í reitnum **Bókunardags. bakfærslu** er færð inn upprunaleg bókunardagsetningu. Það ætti að vera sama dagsetning og notuð var til að reikna VÍV í fyrsta sinn.  
6.  Gátreiturinn **Eingöngu bakfæra**. Þetta bakfærir bókað VÍV, en bókar ekki nýtt VÍV í fjárhaginn.  
7.  Velja hnappinn **Í lagi** til að keyra runuvinnsluna og velja svo **Í lagi** til að loka staðfestingarglugganum.  
8.  Spjaldið **Verk** fyrir **Deerfield** er opnað.  
9. Á flýtiflipanum **VÍV og samþykki** skal staðfesta að engar bókaðar VÍV-færslur séu til staðar.  
10. Glugganum er lokað.  
11. Á listanum **Verk** er verkinu **Deerfield** valin og svo aðgerðin **VÍV** og síðan valin aðgerðin **VÍV fjárhagsfærslur**. VÍV-færslur hafa gátreitinn **Bakfært** valinn.  
12. Glugganum er lokað.  
13. Opna skal **Verkhlutalínur verks**, taka þá hluta með sem eiga að vera með í VÍV-útreikningnum og endurreikna og bóka nýja virðið í fjárhaginn.  

    > [!NOTE]  
    >  Gefum okkur að Tricia hafi reiknað út og bókað WIP fyrir verk með röngum dagsetningum. Í kjölfar aðferðarinnar sem var rædd hér á undan, getur hún bakfært rangar bókanir, leiðrétt dagsetningarnar og endurbókað í fjárhag.  

## <a name="next-steps"></a>Næstu þrep  
 Í þessari kynningu var farið yfir skrefin í útreikningi á VÍV í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í stærri verkum kann að vera gagnlegt að flytja kostnaðinn í VÍV-reikning reglulega á meðan verkið er unnið. Í kynningunni var sýnt hvernig á að undanskilja verkhlutalínur frá útreikningi. Sýnir einnig hvenær þörf er á endurreikningi. Og að lokum, þessi kynning sýnir hvernig á að bóka VÍV í fjárhag. Dæmi um bakfærslu VÍV-bókunar í fjárhag er einnig tekin með.  

## <a name="see-also"></a>Sjá einnig  
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Kynning: Stýring verkefna með verkum](walkthrough-managing-projects-with-jobs.md)   
 [Að skila VÍV aðferðir](projects-understanding-wip.md)   
 [Fylgst með framvindu og afköstum](projects-how-monitor-progress-performance.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

