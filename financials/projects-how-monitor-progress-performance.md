---
title: "Skilgreina VÍV aðferð og fylgjast með framvindu verks| Microsoft Docs"
descrition: Describes how you can create a work in process (WIP) method and calculate WIP to estimate the financial value of jobs while they are ongoing.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b374c80a649a1e05c98fcbcea1ca447ec0b8d27
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-monitor-job-progress-and-performance"></a>Hvernig á að: Fylgjast með framvindu og afköstum
Þegar verk er unnið er efni, forði og annar kostnaður notuð og þetta þarf að bóka á verkið. Verk í vinnslu (VÍV) er eiginleiki þar sem hægt er að meta fjárhagslegt virði verka í fjárhag eftir því sem verkinu miðar áfram. Oft er kostnaður bókaður áður en verk er reikningsfært. Þegar aðeins kostnaður hefur verið bókaður verður fjárhagsyfirlitið ónákvæmt. Frekari upplýsingar eru í [Að skilja VÍV-aðferðir](projects-understanding-wip.md)

Til að rekja gildi í fjárhagnum er hægt að reikna út VÍV og bóka gildið í fjárhag.

VÍV má reikna út byggt á eftirfarandi:

* Kostnaðargildi
* Sölugildi
* Auðkennanlegur kostnaður
* Prósentum lokið
* Samningi lokið

Til að skoða niðurstöður með annarri aðferð er hægt að breyta aðferðinni og reikna Verk í vinnslu á nýjan leik. Engin takmörk eru á því hversu oft VÍV er reiknað. VÍV er aðeins reiknað en er ekki bókað í fjárhag. Þegar VÍV hefur verið reiknað út er hægt að bóka það í fjárhag.

## <a name="to-create-a-job-wip-method"></a>Til að búa til VÍV-aðferð fyrir verk
Hægt er að búa til VÍV-aðferð sem endurspeglar þarfir fyrirtækisins. Þegar búið er að stofna það, er hægt að velja það sem sjálfgefna VÍV-reikningsaðferð fyrir verk sem verða notuð í fyrirtækinu.  

**Athugasemd** Þegar búið er að nota nýju aðferðina til að stofna VÍV-færslur, er ekki hægt að eyða aðferðinni eða breyta henni.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk VÍV aðferðir** og velja svo viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Glugganum er lokað.   
4. Til að gera þessa nýju aðferð sjálfgefna, skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning verka** og velja svo viðeigandi tengil.  
5. Í reitnum **Sjálfgefin vÍv-aðferð** veljið aðferðina af listanum.

## <a name="to-define-a-wip-method-for-a-job"></a>Til að skilgreina VÍV aðferð fyrir verk
Þegar nýtt verk er stofnað þarf að tilgreina hvaða VÍV-aðferð skuli eiga við. Í sumum tilfellum er þegar búið að stilla sjálfgefna VÍV-aðferð verka.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð. Nánari upplýsingar eru í [Hvernig á að: Stofna verk](projects-how-create-jobs.md).  
3. Í glugganum **Verkspjald** skal velja VÍV-aðferð úr listanum í reitnum **VÍV-aðferð**. Ef sjálfgefin aðferð hefur verið skilgreind er hægt að velja annan valkost ef þess gerist þörf.  

## <a name="to-calculate-wip"></a>Útreikningur VÍV
Hægt er að ákvarða VÍV-upphæð sem bóka skal á efnahagsreikning fyrir árslokaskýrslu. Þetta má gera með því að nota keyrsluna **Verkreikna VÍV**.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk útreikningar VÍV** og velja svo viðeigandi tengil.  
2. Veljið aðgerðina **Reikna VÍV**.
3. Í glugganum **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.
4. Velja hnappinn **Í lagi**.  

> [!NOTE]  
>   Keyrslan reiknar einungis út VÍV. Er ekki bókað í fjárhag. Til að gera það verður að keyra keyrsluna **Bóka VÍV á fjárhag** þegar VÍV hefur verið reiknað. Nánari upplýsingar má finna hér á eftir.

## <a name="to-post-wip"></a>Til að bóka VÍV
Þegar VÍV hefur verið reiknað er hægt að bóka það á efnahagsreikning fyrir árslokaskýrslu. Þetta má gera með því að nota keyrsluna **Bóka VÍV á fjárhag**.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk bóka VÍV í fjárhag** og velja svo viðeigandi tengil.  
2. Í glugganum **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Til að skoða áætlanir um verknotkun og bóka uppfærslur
Skoða má verknotkun allt að lokum verkefnis í einu skrefi. Til þess er notuð keyrslan **Verk - Reikna eftirstandandi notkun** fyrir alla verkhluta allt að og með lokum verks.  

Á þennan hátt má rekja og bera saman upprunalega áætlun við raunverulegar niðurstöður og gera breytingar eða bæta við færslum eftir þörfum. Taka má dæmi af notanda sem hefur áætlað að verk taki 10 klukkustundir en það hefur þegar tekið 15 klukkustundir. Hann getur bætt klukkustundunum fimm við færslubókarlínu sem fyrir er eða búið til nýja færslubókarlínu til að skilgreina þessa fimm tíma sem yfirvinnu, sem er önnur tegund vinnu. Raunkostnaður og verð eru reiknuð út, sem svo er hægt að bóka í færslubókina.  

> [!NOTE]  
>   Birgðafærslur stofna færslur í birgðahöfuðbók og minnka birgðamagn. Keyrslan **Bóka birgðabreytingar** færir kostnaðinn úr birgðum í fjárhag. Forðafærslur stofna forðafærslur.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkbækur** og velja svo viðeigandi tengil.  
2. Veljið viðeigandi verkbók og veljið svo aðgerðina **Reikna eftirstandandi notkun**.  
3. Í glugganum **Verk - Reikna eftirstandandi notkun** skal slá inn númer skjalsins og bókunardagsetninguna sem færa skal í bókina og velja svo hnappinn **Í lagi**.  
4. Uppfærið bókina með þeim breytingum sem kann að vera þörf á.  
5. Veljið **Bókun**.

## <a name="to-view-job-ledger-entries"></a>Verkdagbókarfærslur skoðaðar:
Allar færslur sem tengjast verki eru skráðar í verkdagbækur og tölusettar í réttri röð, byrjað á 1. Í verkdagbókinni er hægt að fá yfirlit um verkfærslurnar.    

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **verkdagbók** og velja svo viðeigandi tengil.
2. Valin er viðeigandi dagbók og síðan skal velja aðgerðina **Verklínur**.

Í glugganum **Verkfærslur** er hægt að fara yfir færslur sem tengjast verki.  

## <a name="see-also"></a>Sjá einnig
[Stjórna verkefnum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

