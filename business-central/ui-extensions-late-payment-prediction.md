---
title: Spá fyrir um seinkun á greiðslu fyrir söluskjöl
description: Í þessu efnisatriði er útskýrt hvernig nota á fyrirspyrjandi líkanið til að spá fyrir um hvort reikningur verði greiddur á tíma.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.search.form: 1950, 1951,
ms.date: 12/20/2021
ms.author: bholtorf
ms.openlocfilehash: a2b6cc372846ec525c9f035aa98c5daafbf31913
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533765"
---
# <a name="the-late-payment-prediction-extension"></a>Viðbót greiðsludráttarspár

Árangursrík stjórnun viðskiptakrafna er mikilvæg fyrir heildar fjárhagslega heilsu fyrirtækis. Viðbót greiðsludráttarspár getur hjálpað þér að draga úr útistandandi kröfum og fínstilla stefnu sjóðsins með því að spá fyrir um hvort sölureikningar verði greiddar á réttum tíma. Til dæmis, ef spá telur greiðsla vera sein, gætir þú ákveðið að lagfæra skilmála greiðslu eða greiðslumáta fyrir viðskiptamanninn.

## <a name="getting-started"></a>Hafist handa

Þegar þú opnar bókað söluskjal birtist tilkynning efst á síðunni. Til að nota Viðbót greiðsludráttarspár geturðu tekið þátt með því að velja **Virkja** í tilkynningunni. Einnig er hægt að setja upp viðbótina handvirkt. Til dæmis, ef þú iðrast þess að hafna tilkynningunni.  

Til að virkja viðbótina handvirkt skaltu fylgja þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

> [!NOTE]
> Ef ákveðið er að virkja viðbótina handvirkt skal hafa í huga að [!INCLUDE[prod_short](includes/prod_short.md)] leyfir þér ekki að gera það ef gæði líkansins eru léleg. Gæði líkansins gefur til kynna hversu nákvæmar spár líkansins eru líklegar til að verða. Nokkrir þættir geta haft áhrif á gæði líkansins. Til dæmis getur verið að ekki hafi verið nægjanlega mikið af gögnum eða að þau voru ekki nógu fjölbreytt. Hægt er að skoða gæði líkansins sem þú ert að nota núna á síðunni **Uppsetning greiðsludráttaspár**. Þú getur einnig tilgreint lágmarksþröskuld fyrir gæði líkansins.   

## <a name="viewing-all-payment-predictions"></a>Skoða alla greiðsluspá

Ef þú virkjar viðbót verður **Greiðslur sem spáð er að munu dragast** flís tiltæk í **Viðskiptastjórnandi** í Mitt hlutverk. Flísin sýnir fjölda greiðslna sem spáð er að dragist, og gerir þér kleift að opna **viðskiptamannafærslur** síðuna þar sem þú getur grafið dýpra í bókaða reikninga. Það eru þrjár dálkar sem veita skal eftirtekt:  

* **Greiðsludráttur** - Gefur til kynna hvort dráttur verði á greiðslu reikningsins.
* **Áreiðanleiki spár** - Gefur til kynna hversu áreiðanlegt þú ættir að telja spánna vera. **Mikill** þýðir að spáin er að minnsta kosti 90% viss, **Miðlungs** er á milli 80 og 90% og **Lítill** er undir 80%.
* **Áreiðanleiki spár %** - Sýnir raunverulega prósentu á bak við áreiðanleikamatið. Sjálfgefið er að þessi dálkur er ekki sýndur, en þú getur bætt því við ef þú vilt. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

> [!TIP]
> Síðan Viðskiptamannafærslur sýnir einnig Upplýsingakassa til hægri. Á meðan þú ert að yfirfara spár, geta upplýsingarnar í **Upplýsingar um viðskiptamenn** hlutanum verið gagnlegar. Þegar þú velur reikninginn í listanum birtir hlutinn upplýsingar um viðskiptamanninn. Það gerir þér jafnframt kleift að hefja aðgerðir strax. Ef viðskiptamaður setur til dæmis oft veskið sitt á rangan stað getur þú opnað viðskiptamannakortið frá Upplýsingakassanum og útilokað viðskiptamanninn frá framtíðarsölu.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Greiðsluspá skoðuð fyrir tiltekið söluskjal

Þú getur einnig sagt fyrir um greiðsludrátt fyrirfram. Á síðunum **Sölutilboð**, **Sölupantanir** og **Sölureikningar** geturðu notað **Spá fyrir um greiðslu** aðgerðina til að búa til spá fyrir söluskjalið sem þú ert að skoða.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="design-details"></a>Hönnunarupplýsingar

Microsoft notar og rekur margar forspárþjónustur á netinu á öllu svæðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Aðgangur að þessum vefþjónustum er innifalinn í [!INCLUDE[prod_short](includes/prod_short.md)] áskriftinni. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Vefþjónustan starfar á þremur stillingum:

* Þjálfa líkan. Vefþjónustan þjálfar líkanið á grunni gagnamengis sem er útvegað.
* Leggja mat á líkan. Vefþjónustan athugar hvort líkanið skili áreiðanlegum gögnum fyrir uppgefið gagnamengi.
* Spá Vefþjónustan notar líkanið á uppgefið gagnamengi til að spá fyrir.

Þessar vefþjónustur eru stöðulausar, sem þýðir að þær nota gögn aðeins til að reikna út spár samkvæmt eftirspurn. Þær vita ekki gögn. 

> [!NOTE]  
> Einnig er hægt að nota eigin forspárþjónustu á netinu. Nánari upplýsingar er að finna í [Búa til og nota eigin forspárþjónustu á netinu fyrir spá um greiðsludrátt](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a>Gögn sem þarf til að þjálfa og meta líkanið

Fyrir hverja **Viðskiptamannafærslu** sem er með tengdan **Bókaðan sölureikning**:

* Upphæð (SGM) með sköttum
* Greiðsluskilmálar í dögum eru reiknaðir út sem **Gjalddagi** mínus **Bókunardagsetning**.
* Hvort um jafnaðan kreditreikning er að ræða. 

Þar að auki er uppsöfnuðum gögnum bætt við færsluna úr öðrum reikningum sem eru tengdir sama viðskiptamanninum. Þetta felur í sér eftirfarandi:

- Heildarfjöldi og upphæð greiddra reikninga
- Heildarfjöldi og upphæð reikninga sem voru greiddir seint
- Heildarfjöldi og upphæð útistandandi reikninga
- Heildarfjöldi og upphæð útistandandi reikninga sem eru þegar komnir á tíma
- Hversu mörgum dögum of seint að meðaltali
- Hlutfall: Fjöldi greiddur of seint/Greiddir reikningar
- Hlutfall: Upphæð greidd of seint/Greiddir reikningar
- Hlutfall: Fjöldi útistandandi komnir á tíma/Útistandandi reikningar
- Hlutfall: Upphæð útistandandi komnir á tíma/Útistandandi reikningar

> [!NOTE]
> Upplýsingar um viðskiptamanninn eru ekki í gagnamenginu.

### <a name="standard-model-and-my-model"></a>Staðlað líkan og Líkanið mitt

Viðbót greiðsludráttarspár inniheldur spálíkan sem er þjálfað í að nota gögn sem eru dæmigerð fyrir lítil og upp í meðalstór fyrirtæki. Þegar byrjað er á því að bóka reikninga og taka við greiðslum, mun [!INCLUDE[prod_short](includes/prod_short.md)] meta hvort staðlaða líkanið passi við viðskiptaflæðið. 

Ef svo virðist sem ferli notanda stemmi ekki við staðlaða líkanið er samt hægt að nota viðbótina en nauðsynlegt er að fá fleiri gögn. Haltu bara áfram að nota [!INCLUDE[prod_short](includes/prod_short.md)].
> [!NOTE]
> Við notum smá af reikningstíma þínum í hverri viku þegar við metum og endurþjálfum líkanið. 

[!INCLUDE[prod_short](includes/prod_short.md)] keyrir þjálfun og mat sjálfkrafa þegar nógu margir greiddir reikningar og seinir reikningar eru í boði, en þú getur hins vegar keyrt þetta handvirkt hvenær sem þú vilt.

#### <a name="to-train-and-use-your-model"></a>Að þjálfa og nota líkanið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
2. Í **Valið líkan** reitinn, veldu **Mitt líkan**.
3. Veldu aðgerðina **Búa til líkanið mitt** til að þjálfa líkan í gögnunum þínum.  

## <a name="create-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Búa til og nota eigin greiðsludráttarspá á netinu til að spá fyrir um greiðsludrátt

Þú getur einnig búið til þína eigin spáþjónustu á netinu sem byggir á almennu líkani sem heitir **Forspártilraun fyrir Dynamics 365 Business Central**. Þetta líkan er aðgengilegt á netinu í Azure AI. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu á [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=2086310).  
2. Leita að **Forspártilraun fyrir Dynamics 365 Business Central**, og opna svo líkanið í Azure Machine Learning Studio.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
7. Veldu **Nota Azure-áskriftina mína** gátreitinn.
8. Í **Innskráningarupplýsingar fyrir líkanið mitt** flýtiflipanum, sláðu inn API slóðina og API lykil fyrir líkanið.  .  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/predict-late-payments-sales-documents/)

## <a name="see-also"></a>Sjá einnig .

[Fylgiskjöl fyrir Azure-vélnámsstúdíó](/azure/machine-learning/classic/)  
[Sérstilling Business Central með viðbótum](ui-extensions.md)  
[Velkomin(n) í [!INCLUDE[prod_long](includes/prod_long.md)]](index.md)  
[Nota gervigreind í Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
