---
title: Uppsetning Sjóðstreymissgreiningar (inniheldur Video)
description: Notaðu gröf reikninga í Mínu hlutverki til að greina sjóðstreymi í fyrirtækinu, þar á meðal útgjöld og tekjur, greiðslugetu og inngreiðslur mínus staðgreiðslur.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.search.form: 846, 847, 849, 855, 862, 869, 1818
ms.date: 06/16/2021
ms.author: bholtorf
ms.openlocfilehash: ca4f088156313ec9cf3796abab642b7d319327bb
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143505"
---
# <a name="setting-up-cash-flow-analysis"></a>Setja upp sjóðstreymisgreiningu
Ef þú vilt fá aðstoð til að ákveða hvað þú átt að gera með féð þitt, skoðaðu töflurnar á Hlutverkamiðstöð bókhaldara:  

* **ferill bundins reiðufés**  
* **Tekjur og útgjöld**  
* **Sjóðstreymi**  
* **Sjóðstreymispár**  

Þetta efni lýsir hvar gögnin í töflunum koma frá og, ef nauðsyn krefur, hvað á að gera til að byrja að nota töflurnar.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Gröf ferils bundins reiðufés og tekjur og útgjöld
Gröf **ferils bundins reiðufés** og **tekjur og útgjöld** eru tilbúin til notkunar, byggt á bókhaldslyklum og fjárhagsskema. Lyklarnir eru þar sem gögnin koma frá og fjárhagsskema reiknar út sambandið milli sölu og viðskiptakrafna. Sumir reikningar og fjárhagsskemu eru veitt. Þú getur notað þau eins og-er, breytt þeim og bætt við nýjum. Ef þú bætir fjárhagsreikningi við bókhaldslykil, til dæmis með því að flytja þær frá QuickBooks þarftu að varpa reikningunum á **Fjárhagsskema** síðuna fyrir eftirfarandi nöfn reikningsáætlunar:  

| Heiti fjárhagsskema | Þar sem það er notað |
| --- | --- |
| **I_CACYCLE** |Ferill bundins reiðufés |
| **I_CASHFLOW** |Sjóðstreymi |
| **I_INCEXP** |Tekjur og útgjöld |
| **I_MINTRIAL** |Sem rekstrarreikningur ef þú notar ekki bókhaldslykilinn |

**Athugaðu** Það er góð hugmynd að halda útreikningum sem eru veittar fyrir reikningsáætlunina.  

Sláðu inn reikninga í reitinn **Samtals** fyrir **Heildartekjur**, **Samtala viðskiptakrafna**, **Samtala viðskiptaskulda** og **Samtals birgðir**. Til að varpa á nokkra reikninga, eða fleiri en einn reikning, skaltu slá inn reikningsnúmer aðskilin með ".." eða með lóðrétt striki. Til dæmis **1111..4444** eða **2222|3333|5555**.  

**Ábending** Staðfestu kortlagninguna þína með því að velja **Yfirlit** aðgerðina.  

## <a name="set-up-the-cash-flow-chart"></a>Setja upp sjóðstreymirit
Sjóðstreymi er byggt á eftirfarandi:  

* Myndrit sjóðstreymisreikninga.
* Eina eða fleiri uppsetningar í Uppsetning sjóðstreymis. Þetta tilgreinir reikningana sem nota skal fyrir aðalbókina, kaupin, sölu, þjónustu og eignir.  

Til að hjálpa þér að komast, eru nokkrar reikningar og sjóðstreymisstillingar veittar. Þú getur bætt við, breytt eða fjarlægt þau.  

Til að setja þetta upp skaltu leita að **sjóðstreymisreikningum**, velja tengilinn og fylla síðan inn reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Endurtekur skrefin fyrir **Uppsetning sjóðstreymis**.  

## <a name="set-up-cash-flow-forecasts"></a>Uppsetning sjóðsstreymisspáa
**Sjóðstreymisspá** notar sjóðstreymisreikninga, sjóðstreymisskipulag og sjóðstreymisspár. Sumir eru til staðar, en þú getur sett upp þitt eigið með því að nota aðstoðarmaður uppsetningarleiðbeiningar. Leiðbeiningarnar hjálpar til við að tilgreina atriði hversu oft eigi að uppfæra spá, reikningar til að byggja á, upplýsingar um þegar greiða skatta og hvort kveikja eigi á [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Sjóðstreymisspár geta notað Azure AI til að spá fyrir um komandi skjöl. Niðurstaðan er ítarlegri spá. Tengingin við Azure AI er þegar sett upp fyrir þig. Þú þarft bara að kveikja á því. Þegar þú skráir þig inn á [!INCLUDE[prod_short](includes/prod_short.md)] birtist tilkynning á bláum reit og veitir hlekkur til sjálfgefna sjóðstreymisuppsetningar. Tilkynningin birtist aðeins einu sinni. Ef þú lokar því, en ákveður að kveikja á Azure AI, getur þú notað uppsetningu með hjálp eða handvirkt ferli.  

> [!NOTE]  
>   Að öðrum kosti er hægt að nota eigin fyrirsjáanlega vefþjónustu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).  

Uppsetning assisted leiðbeiningum nota til:  

1. Í Hlutverkamiðstöð bókhaldara undir **Sjóðstreymisspá** skal velja **Opna uppsetningu með hjálp** aðgerðina.  
2. Fylltu út reitina í hverju skrefi leiðarvísisins.  
3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sjóðstreymisspá** og velja síðan viðkomandi tengil.
4. Á síðunni **Sjóðstreymisspá** skal velja aðgerðina **Endurreikna spá**.  

Nota handvirkt ferli:  

1. Í Hlutverkamiðstöð bókhaldara skaltu leita að **Uppsetning sjóðstreymis** og velja svo tengdan tengil.  
2. Stækkaðu **Azure AI** flýtiflipann og veldu gátreitinn **Kveikt á Azure AI**.  
3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sjóðstreymisspá** og velja síðan viðkomandi tengil.
4. Á síðunni **Sjóðstreymisspá** skal velja aðgerðina **Endurreikna spá**.  

> [!TIP]  
>   Íhugaðu lengd tímabila sem þjónustan er notaður í útreikningum hennar. Frekari gögn sem veita verður því nákvæmari á predictions. Líka watch út fyrir mikið frávik í tímabil. Þeir eru einnig hefur predictions. Ef Azure AI finnur ekki næg gögn eða gögnin breytast við lotu mun þjónustan ekki framkvæma forspá.  

## <a name="design-details"></a>Hönnunarupplýsingar
Áskriftum að [!INCLUDE[prod_short](includes/prod_short.md)] fylgir aðgangur að nokkrum forspárþjónustum á netinu á öllum stöðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þær vita ekki gögn.

> [!NOTE]  
>   Einnig er hægt að nota eigin forspárþjónustu á netinu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText). 

### <a name="data-required-for-forecast"></a>Gögn eru nauðsynleg fyrir forspá
Til að spá fyrir um tekjur og útgjöld í framtíðinni þurfa vefþjónustur á eldri gögnum að halda frá útistandandi, viðskiptaskuldum og sköttum.

#### <a name="receivables"></a>Útistandandi:
Reitirnir **Gjalddagi**, **Upphæð (SGM)** síðunnar **Færslur í viðskiptamannabók**, þar sem:
- Tegund skjals er reikningur eða kreditreikningur.
- Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildunum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en forspárþjónusta á netinu er notuð þjappar [!INCLUDE[prod_short](includes/prod_short.md)] færslum eftir **Gjalddaga** út frá gildinu í reitnum **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis**.

#### <a name="payables"></a>Viðskiptaskuldir:
Reitirnir **Gjalddagi**, **Upphæð (SGM)** á síðunni **Lánardrottnafærslur**, þar sem:
- Tegund skjals er „Reikningur“ eða „Kreditreikningur“.
- Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en forspárþjónusta á netinu er notuð þjappar [!INCLUDE[prod_short](includes/prod_short.md)] færslum eftir **Gjalddaga** út frá gildinu í reitnum **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis**.

#### <a name="tax"></a>Skattur:
Reitirnir **Dagsetning skjals**, **Upphæð** á síðunni **Fjárhagsfærslur VSK (skatts)**, þar sem:
- Tegund skjals er „sala“.
- Dagsetning skjals er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en forspárþjónusta á netinu er notuð þjappar [!INCLUDE[prod_short](includes/prod_short.md)] færslum eftir **Dagsetning skjals** út frá gildinu í reitnum **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"> </a>Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár
Þú getur einnig búið til þína eigin fyrirsjáanlega vefþjónustu byggt á opinberu líkani sem heitir **Spárlíkan fyrir Microsoft Business Central**. Þetta líkan er aðgengilegt á netinu í Azure AI. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu á [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Leita að **Forspármódel fyrir Microsoft Business Central** og opna svo líkanið í Azure Machine Learning Studio.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sjóðstreymis** og velja síðan viðkomandi tengil.  
7. Stækkaðu **Azure AI** flýtiflipann, og fylltu síðan inn reitina.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]