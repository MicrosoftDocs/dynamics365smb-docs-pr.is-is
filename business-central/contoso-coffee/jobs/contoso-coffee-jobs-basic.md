---
title: Vasaljós í Grunnvinnslu
description: Þessi grein leiðbeinir þér í gegnum nokkra kjarnaferla í verkefnastjórnun.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-of-basic-jobs"></a>Vasaljós í Grunnvinnslu

Þessi gönguleið sýnir fram á nokkra kjarnaferla:

- Bæta vinnsluverkum við vinnslur
- Skrá tíma-og efniskostnað við vinnu
- Reikningsfæra verk

## <a name="adding-a-job-task-to-a-job"></a>Bætt verklag við vinnu

### <a name="scenario"></a>Aðstæður

Símon, Verkstjóri, vill vera að skrá tíma eyða menntun viðskiptavinur í espresso vél nota skal sérstakt verk í vinnsluna til að setja upp vél á staðnum.

### <a name="steps"></a>Skref

1. Stofna Vinnsluverkefnið  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
    2. Veljið vinnsluna  *J00010*.
    3.  **Í verksvæðinu**  skal velja  **nýju línuaðgerðina** .  Sláðu inn eftirfarandi gildi:
 
    |Verkhlutanúmer verks|Heimildasamstæða|Tegund verkhluta|
    |------------|-----------|-------------|  
    |220|Þjálfun viðskiptavina|Bóka|

2. Inntaka þeirra verkhluta sem vinna
   1. Í verksvæðinu skal staðsetja  **aðgerðina Inndráttur verkhluta**  vinnu
   2. Staðfesta þarf inndrátt verkefna með því að velja  **Já**.

### <a name="results"></a>Niðurstöður

 - Nú er hægt að skrá tíma og útgjöld í nýtt vinnsluverk

## <a name="record-time-and-material-expenses-to-a-job"></a>Skrá tíma-og efniskostnað við vinnslu

### <a name="scenario-1"></a>Aðstæður

Edgin, tæknimaður að setja upp vélina, þarf að skrá tíma hans og þau efni sem notuð eru við uppsetningu á vinnslunni fyrir innheimtuaðila.  Hann hefur þegar bætt við ferðum og efnum og þarf nú að bæta við tímann fyrir að kenna starfsfólki hvernig á að nota vélina.

### <a name="steps-1"></a>Skref

1. Stofna fleiri færslubókarlínur vinnslu

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
    2. Veljið *runcontoso*.  Hér birtast nokkrar línur um forða og vörutegundir, sem endurspegla tímann (fyrir tæknimann og ökutækið) og efni (sem vél og vistir) notuðu.
    3. Stofnið nýja línu. Sláðu inn eftirfarandi gildi:
 
    |Verknúmer|Verkhlutanúmer verks|Gerð|Nr.|Heimildasamstæða|Magn|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Forði|EDGIN|Þjálfun viðskiptavina|1|

2. Bóka tíma-og kostnað
   1.  **Velja aðgerðina Bóka** 
   2. Staðfesta skal að bóka eigi línurnar með því að velja  **Já**.

### <a name="results-1"></a>Niðurstöður

 - Verkfærslur og forðafærslur af gerðinni  *notkun*  verða stofnaðar
 - Birgðafærslur verða stofnaðar til að breyta birgðum
 - Á verkspjaldinu er kostnaður og verð á verksvæðinu sem endurspeglar nýja stöðu sem bíður eftir reikningsfærslu
 - Upplýsingakassi í Vinnsluspjaldinu endurspeglar samtölur verðanna

## <a name="creating-a-sales-invoice-for-a-job"></a>Sölureikningur stofnaður fyrir verk

### <a name="scenario-2"></a>Aðstæður
Símon þarf að stofna og bóka reikning til að geta sent viðskiptavininum þann tíma og kostnað frá vinnslunni.

### <a name="steps-2"></a>Skref
1. Stofna sölureikning

    1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
    2. Í listanum yfir vinnslur skal velja  **aðgerðina Sölureikningsaðgerðin**  Stofna vinnslu.
    3.  **Sett Verk nr.** sía til  *J00010*.
    4. Velja  **skal í lagi**  til að mynda sölureikninginn.  Þú munt fá staðfestingu á því hversu margir reikningar eru myndaðir

2. Bóka tíma-og kostnaðarreikning
   1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  
   2. Veljið Síðasta reikning til að opna hana til yfirferðar.
   3. Valið er **Bóka** aðgerðin.

### <a name="results-2"></a>Niðurstöður

 - Verkfærslur og forðafærslur af tegundinni  *Sala*  verða stofnaðar
 - Á verkspjaldinu endurspeglar kostnaðurinn og verðið á verksvæðinu endurspegli nýju reikningsfærðu stöðurnar
 - Upplýsingakassi í Vinnsluspjaldinu endurspeglar samtölur verðs í kaflanum Reikningsfært verð til að færa inn á verkspjaldið.
