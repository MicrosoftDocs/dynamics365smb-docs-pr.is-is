---
title: Skilgreina VÍV aðferð og fylgjast með framvindu verks| Microsoft Docs
description: Lýsir því hvernig þú getur búið til verk í vinnslu (VÍV) aðferð og reiknað VÍV til að meta fjárhagslegt gildi verka meðan á þeim stendur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fac1c041108cacfcabf18b04d128949d05e1d283
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938122"
---
# <a name="monitor-job-progress-and-performance"></a>Fylgst með framvindu og afköstum
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

> [!NOTE]
> Þegar búið er að nota nýju aðferðina til að stofna VÍV-færslur, er ekki hægt að eyða aðferðinni eða breyta henni.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **VÍV-aðferðir verks** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Lokaðu síðunni.   
4. Til að gera þetta að sjálfgefinni aðferð velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning verka** og veldu síðan tengda tengilinn.  
5. Í reitnum **Sjálfgefin vÍv-aðferð** veljið aðferðina af listanum.

## <a name="to-define-a-wip-method-for-a-job"></a>Til að skilgreina VÍV aðferð fyrir verk
Þegar nýtt verk er stofnað þarf að tilgreina hvaða VÍV-aðferð skuli eiga við. Í sumum tilfellum er þegar búið að stilla sjálfgefna VÍV-aðferð verka.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt**. Frekari upplýsingar eru í [Stofna verk](projects-how-create-jobs.md).  
3. Á síðunni **Verkspjald** skal velja VÍV-aðferð úr listanum í reitnum **VÍV-aðferð**. Ef sjálfgefin aðferð hefur verið skilgreind er hægt að velja annan valkost ef þess gerist þörf.  

## <a name="to-calculate-wip"></a>Útreikningur VÍV
Hægt er að ákvarða VÍV-upphæð sem bóka skal á efnahagsreikning fyrir árslokaskýrslu. Þetta má gera með því að nota keyrsluna **Verkreikna VÍV**.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkreikna VÍV** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Reikna VÍV**.
3. Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.
4. Velja hnappinn **Í lagi**.  

> [!NOTE]  
>   Keyrslan reiknar einungis út VÍV. Er ekki bókað í fjárhag. Til að gera það verður að keyra keyrsluna **Bóka VÍV á fjárhag** þegar VÍV hefur verið reiknað. Nánari upplýsingar má finna hér á eftir.

## <a name="to-post-wip"></a>Til að bóka VÍV
Þegar VÍV hefur verið reiknað er hægt að bóka það á efnahagsreikning fyrir árslokaskýrslu. Þetta má gera með því að nota keyrsluna **Bóka VÍV á fjárhag**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bóka VÍV í fjárhag** og veldu síðan tengda tengilinn.  
2. Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.

## <a name="to-calculate-and-post-job-completion-entries"></a>Að reikna út og bóka verklokafærslur
Þegar öllum aðgerðum verks hefur verið lokið, þar með talin bókun notkunar og reikningsfærsla, þarf að uppfæra verkið svo að **Staða** þess sé **Lokið**. Síðan þarf að bakfæra VÍV sem hefur verið bókað í fjárhag.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Veljið opið verk og veljið svo aðgerðina **Breyta**.
3. Í reitnum **Staða** skal velja **Lokið**.
4. Fylgið aðstoðarskrefunum til að reikna og bóka VÍV. Einnig er hægt að fylgja skrefum 5 og 6 til að gera það handvirkt.  
5. Veljið aðgerðina **Reikna VÍV**.
6. Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.  

     VÍV færslurnar sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær séu lokafærslur.  
7. Velja skal aðgerðina **Verk - Bóka VÍV í fjárhag**.
8. Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  

     VÍV-fjárlagsfærslur verks sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær eru lokafærslur.

## <a name="to-view-job-ledger-entries"></a>Verkdagbókarfærslur skoðaðar:
Allar færslur sem tengjast verki eru skráðar í verkdagbækur og tölusettar í réttri röð, byrjað á 1. Í verkdagbókinni er hægt að fá yfirlit um verkfærslurnar.    

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkdagbækur** og veldu síðan tengda tengilinn.
2. Valin er viðeigandi dagbók og síðan skal velja aðgerðina **Verklínur**.

Á síðunni **Verkfærslur** er hægt að fara yfir færslur sem tengjast verki.  

## <a name="see-also"></a>Sjá einnig
[Verkefnum stjórnað](projects-manage-projects.md)
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)   
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
