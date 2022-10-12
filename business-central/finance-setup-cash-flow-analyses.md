---
title: Uppsetning Sjóðstreymissgreiningar (inniheldur Video)
description: Notið Accountant-hlutverkamiðstöð ritara töflur til að greina flæði fjármuna í viðskiptunum, þ.m.t. útgjöld og tekjur, greiðslugetu og innhreyfingu að frádregnum peningagreiðslum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.search.form: 846, 847, 849, 851, 855, 862, 869, 1818
ms.date: 08/23/2022
ms.author: bholtorf
ms.openlocfilehash: 8074e7342740efa1466bc6fea3c4fd192ddbfd56
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605058"
---
# <a name="setting-up-cash-flow-analysis"></a>Setja upp sjóðstreymisgreiningu

Ef þú vilt fá aðstoð til að ákveða hvað þú átt að gera með féð þitt, skoðaðu töflurnar á Hlutverkamiðstöð bókhaldara:

* **ferill bundins reiðufés**  
* **Tekjur og útgjöld**  
* **Sjóðstreymi**  
* **Sjóðstreymispár**  

Í þessari grein er lýst hvaðan gögnin í kortunum koma og, ef nauðsyn krefur, hvað á að gera til að byrja að nota gröf.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Gröf ferils bundins reiðufés og tekjur og útgjöld

**Útboðsyfirlit** og **tekjur & útgjaldatöflur** eru tilbúnar til að fara á grundvelli bókhaldslykla og ársskýrslna. Reikningarnir eru þar sem gögnin koma og ársskýrslur reikna tengslin milli sölu og rekjanleika. Boðið er upp á nokkrar reikninga og ársskýrslur. Þú getur notað þau eins og-er, breytt þeim og bætt við nýjum. Ef þú bætir fjárhagsreikningum við bókhaldslykilinn þinn, til dæmis með því að flytja þá inn úr Fljótbókunum, þarftu að varpa á reikningana á **síðu fjárhagsskýrslna** fyrir eftirfarandi skýrslur:

| Heiti fjárhagsskýrslu | Þar sem það er notað |
| --- | --- |
| **I_CACYCLE** |Ferill bundins reiðufés |
| **I_CASHFLOW** |Sjóðstreymi |
| **I_INCEXP** |Tekjur og útgjöld |
| **I_MINTRIAL** |Sem rekstrarreikningur ef þú notar ekki bókhaldslykilinn |

> [!NOTE]
> Það er góð hugmynd að halda útreikningana sem eru veittir fyrir ársskýrslu.

Sláðu inn reikninga í reitinn **Samtals** fyrir **Heildartekjur**, **Samtala viðskiptakrafna**, **Samtala viðskiptaskulda** og **Samtals birgðir**. Til að varpa á svið reikninga skal færa reikningsnúmerin aðskilin með ".." eins og í **1111.. 4444**. Til að varpa á sérstaka lykla skal færa reikningsnúmerin aðskilin með lóðréttri stiku eins og í **2222 | 3333 | 5555**.  

> [!TIP] 
> Staðfestið vörpun með því að **velja Yfirlit** aðgerð.  

## <a name="set-up-the-cash-flow-chart"></a>Setja upp sjóðstreymirit

Sjóðstreymissrit er byggt á:  

* Myndrit sjóðstreymisreikninga.
* Eina eða fleiri uppsetningar í Uppsetning sjóðstreymis. Þessar uppsetningar tilgreina lykla sem nota á fyrir fjárhag, innkaup, sölu, þjónustu og eignir.  

Til að hjálpa þér að komast, eru nokkrar reikningar og sjóðstreymisstillingar veittar. Þú getur bætt við, breytt eða fjarlægt þau.  

Til að setja upp reikningana þarf að leita **að Sjóðsstreymisseikninga**, velja tengilinn og færa síðan inn í reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Endurtakið þessi skref fyrir **uppsetningu** sjóðstreymis.

## <a name="set-up-cash-flow-forecasts"></a>Uppsetning sjóðsstreymisspáa

**Sjóðstreymisspá** notar sjóðstreymisreikninga, sjóðstreymisskipulag og sjóðstreymisspár. Sumir eru til staðar, en þú getur sett upp þitt eigið með því að nota aðstoðarmaður uppsetningarleiðbeiningar. Leiðbeiningarnar hjálpar til við að tilgreina atriði hversu oft eigi að uppfæra spá, reikningar til að byggja á, upplýsingar um þegar greiða skatta og hvort kveikja eigi á [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Sjóðstreymisspá getur notað Azure AI til að stofna ítarlegri spá. Tengingin við Azure AI er þegar sett upp fyrir þig. Þú þarft bara að kveikja á því. Við innskráningu [!INCLUDE[prod_short](includes/prod_short.md)] birtist tilkynning í blárri stiku og er tengill á sjálfgefna uppsetningu sjóðstreymis. Tilkynningin birtist aðeins einu sinni. Ef þú lokar henni en ákveður síðan að kveikja Azure AI er hægt að nota leiðbeiningar með uppsetningarhandbók eða handvirkt ferli.  

> [!NOTE]
>
> Að öðrum kosti er hægt að nota eigin fyrirsjáanlega vefþjónustu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).  

Uppsetning assisted leiðbeiningum nota til:  

1. Í Hlutverkamiðstöð bókhaldara undir **Sjóðstreymisspá** skal velja **Opna uppsetningu með hjálp** aðgerðina.
2. Fylltu út reitina í hverju skrefi leiðarvísisins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til baka í hlutverkamiðstöð endurskoðanda skal velja endurreikna spáraðgerðina **í** **línuritinu Sjóðstreymisspá**.

Nota handvirkt ferli:  

1. Í hlutverkamiðstöð endurskoðanda skaltu velja þá ![ljósaperu sem opnar aðgerðina segja mér upp.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Sjóðstreymissuppsetningu** og velja síðan tengda tengilinn.
2. **Stækkaðu AZURE AI** fastflipann og veldu **svo Azure AI virkt** svæðið.
3. Til baka í hlutverkamiðstöð endurskoðanda skal velja endurreikna spáraðgerðina **í** **línuritinu Sjóðstreymisspá**.

> [!TIP]  
> Íhugaðu lengd tímabila sem þjónustan er notaður í útreikningum hennar. Frekari gögn sem veita verður því nákvæmari á predictions. Líka watch út fyrir mikið frávik í tímabil. Þeir eru einnig hefur predictions. Ef Azure AI finnur ekki næg gögn eða gögnin breytast við lotu mun þjónustan ekki framkvæma forspá.  

## <a name="design-details"></a>Hönnunarupplýsingar

Áskriftum að [!INCLUDE[prod_short](includes/prod_short.md)] fylgir aðgangur að nokkrum forspárþjónustum á netinu á öllum stöðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Frekari upplýsingar í Microsoft Dynamics 365 Business Central leyfisleiðbeiningum. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þær vita ekki gögn.

> [!NOTE]
>
> Einnig er hægt að nota eigin forspárþjónustu á netinu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).

### <a name="data-required-for-forecast"></a>Gögn eru nauðsynleg fyrir forspá

Til að spá fyrir um tekjur og útgjöld í framtíðinni þurfa vefþjónustur á eldri gögnum að halda frá útistandandi, viðskiptaskuldum og sköttum.

#### <a name="receivables"></a>Viðskiptakröfur

Reitirnir **Gjalddagi**, **Upphæð (SGM)** síðunnar **Færslur í viðskiptamannabók**, þar sem:

* Skjalgerðin er *Reikningur* eða *kreditreikningur*.
* Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildunum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en spá vefþjónustu er notuð skal [!INCLUDE[prod_short](includes/prod_short.md)] þjappa færslum eftir **gjalddaga** samkvæmt gildinu í **reitnum Tegund** tímabils á **uppsetningarsíðu** sjóðstreymis.

#### <a name="payables"></a>Viðskiptaskuldir

Reitirnir **Gjalddagi**, **Upphæð (SGM)** á síðunni **Lánardrottnafærslur**, þar sem:

* Skjalgerðin er *Reikningur* eða *kreditreikningur*.
* Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en spá vefþjónustu er notuð skal [!INCLUDE[prod_short](includes/prod_short.md)] þjappa færslum eftir **gjalddaga** samkvæmt gildinu í **reitnum Tegund** tímabils á **uppsetningarsíðu** sjóðstreymis.

#### <a name="tax"></a>Skattur

Reitirnir **Dagsetning skjals**, **Upphæð** á síðunni **Fjárhagsfærslur VSK (skatts)**, þar sem:

* Skjalgerðin er *Sala*.
* Dagsetning skjals er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en spá vefþjónustu er notuð skal [!INCLUDE[prod_short](includes/prod_short.md)] þjappa færslum eftir **dagsetningu** fylgiskjals á grundvelli virðis í **reitnum Tegund** tímabils í **uppsetningarsíðu** sjóðstreymis.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a> Stofna og nota eigin spá vefþjónustu fyrir sjóðstreymisspár

Þú getur einnig búið til þína eigin fyrirsjáanlega vefþjónustu byggt á opinberu líkani sem heitir **Spárlíkan fyrir Microsoft Business Central**. Þetta líkan er aðgengilegt á netinu í Azure AI. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu á [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Leita að **spárlíkani fyrir Microsoft Business Central** og opna síðan líkanið í Microsoft Azure véla-námsvinnustofan.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sjóðstreymis** og velja síðan viðkomandi tengil.  
7. **Útvíkkið AZURE AI** fastflipann og fyllið síðan inn í reitina, þar á meðal API-URL og API-lykil úr Azure vél Learning Studio. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. Í hlutverkamiðstöð endurskoðanda skal velja **Endurreikna spáaðgerðina** **í sjóðstreymisspár**.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/forecast-cash-flow-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
