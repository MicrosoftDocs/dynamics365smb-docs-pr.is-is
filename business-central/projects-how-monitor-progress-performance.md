---
title: Fylgst með framvindu og afköstum
description: Lýsir því hvernig þú getur búið til verk í vinnslu (VÍV) aðferð og reiknað VÍV til að meta fjárhagslegt gildi verka meðan á þeim stendur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.search.form: 89, 92, 1010
ms.date: 08/04/2022
ms.author: edupont
ms.openlocfilehash: 9b4c511c0cdaa6be6147ab1df3672f07b58c2b81
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528922"
---
# <a name="monitor-job-progress-and-performance"></a>Fylgst með framvindu og afköstum

Með aðgerðinni verk í vinnslu (VÍV) er hægt að áætla fjárhagslegt virði áframhaldandi vinnslu í fjárhag.

Eftir því sem líður á vinnsluna er efni og tilföng notað og kostnaður sem stofnað er til við vinnsluna verður bókaður. Í mörgum tilfellum gæti verið hægt að bóka útgjöld fyrir vinnslu áður en reikningsfært er. En ef aðeins útgjöldin eru bókuð er fjárhagsuppgjörið þitt ónákvæmt. Til að rekja Raunverulegt gildi vinnslunnar skal reikna út VÍV og bóka hana í fjárhag. Lærðu meira á að [skilja VÍV-aðferðir](projects-understanding-wip.md).

VÍV má reikna út byggt á eftirfarandi:

* Kostnaðarvirði
* Söluandvirði
* Þekktra ocst
* Prósenta sem er lokið
* Samningi lokið

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-job-wip-method"></a>Stofna VÍV-aðferð fyrir verk

Stofnið VÍV-aðferð sem uppfyllir þarfir fyrirtækisins og Stillið það sem sjálfgildi.  

> [!NOTE]
> Þegar ný aðferð hefur verið notuð til að stofna VÍV-færslur er ekki hægt að breyta eða eyða þeirri aðferð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **verkvíg-aðferðir**, velja síðan tengda tengilinn.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Lokaðu síðunni.   
4. Til að gera þetta að sjálfgefinni aðferð velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **uppsetningaruppsetningu** og velja síðan tengda tengilinn.  
5. Í reitnum **Sjálfgefin vÍv-aðferð** veljið aðferðina af listanum.

## <a name="define-a-wip-method-for-a-job"></a>Skilgreina VÍV-aðferð fyrir vinnslu

Þegar ný vinnsla er stofnuð þarf að tilgreina hvaða vinnslu VÍV-aðferð á við. Í sumum tilvikum er VINNSLUVÍV-aðferðin sem er notuð er þegar stillt sem sjálfgildi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **vinnslur**, veldu síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt**. Frekari upplýsingar í [Stofna vinnslur](projects-how-create-jobs.md).  
3. Á síðunni **Verkspjald** skal velja VÍV-aðferð úr listanum í reitnum **VÍV-aðferð**. Ef sjálfgefin aðferð hefur verið skilgreind er hægt að velja annan valkost ef þess gerist þörf.  

### <a name="define-a-wip-method-for-a-job-task"></a>Skilgreina VÍV-aðferð fyrir vinnsluverk

Hægt er að tilgreina VÍV-aðferð fyrir verkhluta, útiloka nokkur vinnsluverk frá VÍV-reikniverki eða flokka verk sem skal kótað saman. 

Ef reikna á VÍV fyrir hvert vinnsluverk fyrir sig er VÍV-bókun skilgreindar víddir tiltekinna verka.

**VÍV-Samtala** Tilgreinir verkhluta verks sem á að flokka saman þegar VÍV og Viðurkenning er reiknað. Í hvaða flokk verkefna þarf að vera eitt verkefni sem fullnægir tveimur skilyrðum:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* **Er með VÍV-heildarstillt** á *samtölu*. (Ef ekki eru starfsverkefni með **VÍV-heildarstillt** á *samtölu*, *Samtala* er stillt sjálfkrafa á síðustu verkverklínu þegar VÍV er reiknað í fyrsta sinn.)

* **Hefur starf Verk nr.** númer sem er lokaorð í flokki eða bili verkhluta verks.

Eftirfarandi tafla lýsir valkostunum þremur:

| Svæði | Lýsing |
|--|--|
| **\<blank\>** | Skiljið eftir autt ef verkverkið er hluti af verki hóps. |
| **Samtals** | Skilgreinir afmörkun eða flokk verka sem eru innifalin í útreikningi VÍV og viðurkenningar. Innan flokksins eru allir verkhluta sem með **gerð** verkverkhluta settir á til **bókunar** teknir með í VÍV-samtölu, nema að VÍV-heildarreitur **verks** er stilltur að **undanskildum**. |
| **Útilokað** | Á aðeins við um verkefni við **gerð** starfsverkefnabókar **·**, í hvaða tilvikum er VERKIÐ ekki innifalið þegar VÍV og Viðurkenning er reiknað. |

Í dæminu hér á eftir er vinnsluverkefnum skipt í tvær VÍV-heildarsamtölu, þar sem **sýnt er hvernig svæðið VÍV-Samtals** virkar:

|Verklag nr.|Lýsing|Gerð verks|**VÍV-Samtals** svæði|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Undirbúningur|Byrja-Samtals|\<blank\>|
|1010|.    Þrif|Bóka|**Útilokað**|
|1099|Undirbúningur í heild|Enda-Samtals|\<blank\>|
|1100|Teppalagning|Byrja-Samtals|\<blank\>|
|1110|.    Límbera gólf|Bóka|**Útilokað**|
|1120|.    Leggja teppi|Bóka|\<blank\>|
|1199|Teppalagning í heild|Enda-Samtals|\<blank\>|
|1200|Ljúka|Byrja-Samtals|\<blank\>|
|1210|.    Ryksuga teppi|Bóka|\<blank\>|
|1299|Frágangur í heild|Enda-Samtals|**Samtals**|
|1300|Villuleiðrétting|Byrja-Samtals|\<blank\>|
|1310|.    Villuleiðrétting|Bóka|\<blank\>|
|1399|Alger leiðrétting á villu|Enda-Samtals|**Samtals**|

Þú munt taka eftir:

* *1000* í gegnum *1299* : vís reiknar sérstaklega fyrir þennan flokk atvinnuverkefna. Athugið þó að tvö verkefnanna, 1010 og 1110, eru undanskilin í útreikningi á VÍV því vinnsluverkgerðin er **bókuð**.

* *1300* í gegnum *1399* : vís reiknar sérstaklega fyrir þennan flokk atvinnuverkefna.

## <a name="calculate-wip"></a>Reikna VÍV

Hægt er að ákvarða VÍV-upphæð til að bóka á efnahagslykla fyrir lokskýrslugerð fyrir tímabilið. Keyrslan Reikna VÍV **verk er** notuð til að gera þetta.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **vinnsluna reikna VÍV** og velja síðan tengda tengilinn.  
2. Veljið aðgerðina **Reikna VÍV**.
3. Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.
4. Velja hnappinn **Í lagi**.  

> [!NOTE]  
>   Keyrslan reiknar aðeins út VÍV, hún bókar hana ekki í fjárhag. Ef bóka á það skal keyra **keyrsluna Bóka VÍV í fjárhag** eftir að VÍV hefur verið reiknað. Frekari upplýsingar á eftirfarandi hátt.

## <a name="post-wip"></a>Bóka VÍV

Þegar VÍV hefur verið reiknað er hægt að bóka það á efnahagslykla fyrir lokskýrslugerð fyrir tímabilið. Þetta má gera með því að nota keyrsluna **Bóka VÍV á fjárhag**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **verkbókun VÍV í fjárhag** og velja síðan tengdan tengil.  
2. Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.

## <a name="calculate-and-post-job-completion-entries"></a>Reikna og bóka verklokafærslur

Þegar lokið hefur verið við alla verkþætti fyrir vinnslu, þar á meðal notkun bókunar og reikningsfærslu, verður að uppfæra vinnsluna **í** **lokið**. Síðan þarf að bakfæra VÍV sem hefur verið bókað í fjárhag.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **vinnslur**, veldu síðan tengda tengilinn.  
2. Veljið opið verk og veljið svo aðgerðina **Breyta**.
3. Í reitnum **Staða** skal velja **Lokið**.
4. Fylgdu leiðbeiningum um aðstoð til að reikna út og bóka VÍV. Eða fylgja skrefum 5 og 6 þannig að það sé gert handvirkt.  
5. Veljið aðgerðina **Reikna VÍV**.
6. Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.  

     VÍV færslurnar sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær séu lokafærslur.  
7. Velja skal aðgerðina **Verk - Bóka VÍV í fjárhag**.
8. Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.  

     VÍV-fjárlagsfærslur verks sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær eru lokafærslur.

## <a name="view-job-ledger-entries"></a>Skoða verkfærslur

Allar starfstengda færslur eru skráðar í verkdagbækur og raðar tölusettar, sem hefjast 1. Í verkdagbókinni er hægt að fá yfirlit um verkfærslurnar.    

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **verkdagbækur** og velja tengdan tengil.
2. Valin er viðeigandi dagbók og síðan skal velja aðgerðina **Verklínur**.

Á síðunni **Verkfærslur** er hægt að fara yfir færslur sem tengjast verki.  

## <a name="find-related-microsoft-training"></a>Finna tengt [Microsoft þjálfun](/training/paths/calculate-post-job-wip/)

## <a name="see-also"></a>Sjá einnig .

[Walkthrough-útreikningur á vinnu í gangi vegna vinnu](walkthrough-calculating-work-in-process-for-a-job.md)
[Umsjón verkefna](projects-manage-projects.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
