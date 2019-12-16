---
title: Setja upp sjóðstreymisgreiningu | Microsoft Docs
description: Setja upp myndritin á Reikningar Mitt hlutverk til að hjálpa til við að greina sjóðstreymi í fyrirtækinu, þar á meðal útgjöld og tekjur, greiðslugetu og inngreiðslur mínus staðgreiðslur.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 88b84c13da3b443714bcfb7cb86a52ee49264c64
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879490"
---
# <a name="setting-up-cash-flow-analysis"></a>Setja upp sjóðstreymisgreiningu
Ef þú vilt fá aðstoð til að ákveða hvað þú átt að gera með féð þitt, skoðaðu töflurnar á Hlutverkamiðstöð bókhaldara:  

* **ferill bundins reiðufés**  
* **Tekjur og útgjöld**  
* **Sjóðstreymi**  
* **Sjóðstreymispár**  

Þetta efni lýsir hvar gögnin í töflunum koma frá og, ef nauðsyn krefur, hvað á að gera til að byrja að nota töflurnar.  

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

Sjóðstreymisspár geta notað Azure AI til að innihalda skjöl með gjalddaga í framtíðinni. Niðurstaðan er ítarlegri spá. Tengingin við Azure AI er þegar sett upp fyrir þig. Þú þarft bara að kveikja á því. Þegar þú skráir þig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)] birtist tilkynning á bláum reit og veitir hlekkur til sjálfgefna sjóðstreymisuppsetningar. Tilkynningin birtist aðeins einu sinni. Ef þú lokar því, en ákveður að kveikja á Azure AI, getur þú notað uppsetningu með hjálp eða handvirkt ferli.  

> [!NOTE]  
>   Að öðrum kosti er hægt að nota eigin fyrirsjáanlega vefþjónustu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).  

Uppsetning assisted leiðbeiningum nota til:  

1. Í Hlutverkamiðstöð bókhaldara undir **Sjóðstreymisspá** skal velja **Opna uppsetningu með hjálp** aðgerðina.  
2. Fylltu út reitina í hverju skrefi leiðarvísisins.  
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sjóðstreymisspá** og veldu síðan tengda tengilinn.
4. Á síðunni **Sjóðstreymisspá** skal velja aðgerðina **Endurreikna spá**.  

Nota handvirkt ferli:  

1. Í Hlutverkamiðstöð bókhaldara skaltu leita að **Uppsetning sjóðstreymis** og velja svo tengdan tengil.  
2. Stækkaðu **Azure AI** flýtiflipann og veldu gátreitinn **Kveikt á Azure AI**.  
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sjóðstreymisspá** eða Lánardrottinn og veldu síðan tengda tengilinn.
4. Á síðunni **Sjóðstreymisspá** skal velja aðgerðina **Endurreikna spá**.  

> [!TIP]  
>   Íhugaðu lengd tímabila sem þjónustan er notaður í útreikningum hennar. Frekari gögn sem veita verður því nákvæmari á predictions. Líka watch út fyrir mikið frávik í tímabil. Þeir eru einnig hefur predictions. Ef Azure AI finnur ekki næg gögn eða gögnin breytast við lotu mun þjónustan ekki framkvæma forspá.  

## <a name="AnchorText"> </a>Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár
Þú getur einnig búið til þína eigin fyrirsjáanlega vefþjónustu byggt á opinberu líkani sem heitir **Spárlíkan fyrir Microsoft Business Central**. Þetta líkan er aðgengilegt á netinu í Azure AI. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu á [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Leita að **Forspármódel fyrir Microsoft Business Central** og opna svo líkanið í Azure Machine Learning Studio.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sjóðstreymis** og veldu síðan tengda tengilinn.  
7. Stækkaðu **Azure AI** flýtiflipann, og fylltu síðan inn reitina.  

## <a name="see-also"></a>Sjá einnig
[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
