---
title: "Setja upp sjóðstreymisgreiningu | Microsoft Docs"
description: "Setja upp myndritin á Reikningar Mitt hlutverk til að hjálpa til við að greina sjóðstreymi í fyrirtækinu, þar á meðal útgjöld og tekjur, greiðslugetu og inngreiðslur mínus staðgreiðslur."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7fd5d5885439a34ca18ae4ed8d7c0bfb577c0174
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

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
**Sjóðstreymisspá** notar sjóðstreymisreikninga, sjóðstreymisskipulag og sjóðstreymisspár. Sumir eru til staðar, en þú getur sett upp þitt eigið með því að nota aðstoðarmaður uppsetningarleiðbeiningar. Leiðbeiningarnar hjálpar til við að tilgreina atriði hversu oft eigi að uppfæra spá, reikningar til að byggja á, upplýsingar um þegar greiða skatta og hvort kveikja eigi á [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite).  

Sjóðstreymisspár geta notað Cortana Intelligence til að innihalda skjöl með gjalddaga í framtíðinni. Niðurstaðan er ítarlegri spá. Tengingin við Cortana Intelligence er þegar sett upp fyrir þig. Þú þarft bara að kveikja á því. Þegar þú skráir þig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)] birtist tilkynning á bláum reit og veitir hlekkur til sjálfgefna sjóðstreymisuppsetningar. Tilkynningin birtist aðeins einu sinni. Ef þú lokar því, en ákveður að kveikja á Cortana Intelligence, getur þú notað uppsetningu með hjálp eða handvirkt ferli.  

> [!NOTE]  
>   Að öðrum kosti er hægt að nota eigin fyrirsjáanlega vefþjónustu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).  

Uppsetning assisted leiðbeiningum nota til:  

1. Í Hlutverkamiðstöð bókhaldara undir **Sjóðstreymisspá** skal velja **Opna uppsetningu með hjálp** aðgerðina.  
2. Fylltu út reitina í hverju skrefi leiðarvísisins.  
3. Á heimasíðunni velurðu **Sjóðstreymisspá** fyrir ofan töfluna og síðan **Endurreikna spá**..  

Nota handvirkt ferli:  

1. Í Hlutverkamiðstöð bókhaldara skaltu leita að **Uppsetning sjóðstreymis** og velja svo tengdan tengil.  
2. Stækkaðu **Cortana Intelligence** flýtiflipann, og veldu **Cortana Intelligence virkjað** gátreitinn.  
3. Á heimasíðunni velurðu **Sjóðstreymisspá** fyrir ofan töfluna og síðan **Endurreikna spá**..  

> [!TIP]  
>   Íhugaðu lengd tímabila sem þjónustan er notaður í útreikningum hennar. Frekari gögn sem veita verður því nákvæmari á predictions. Líka watch út fyrir mikið frávik í tímabil. Þeir eru einnig hefur predictions. Ef Cortana Intelligence finnur ekki nægt gögnum eða gögnin breytist við lotu, gera á ekki við prediction.  

## <a name="AnchorText"> </a>Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár
Þú getur einnig búið til þína eigin fyrirsjáanlega vefþjónustu byggt á opinberu fyrirmynd sem heitir **Forspármódel fyrir Microsoft Finance and Operations, Business Edition**. Þetta líkan er aðgengilegt á netinu í Cortana Intelligence Gallery. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu í [Cortana Intelligence Gallery](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Leitið að **Spárlíkan fyrir Microsoft Finance and Operations, Business Edition** og opnið svo líkanið Azure Machine Learning Studio.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning sjóðstreymis** og velja svo viðeigandi tengil.  
7. Stækkaðu **Cortana Intelligence** flýtiflipann, og fylltu síðan inn reitina.  

## <a name="see-also"></a>Sjá einnig
[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

