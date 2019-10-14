---
title: Spá fyrir um seinkun á greiðslu fyrir söluskjöl | Microsoft Docs
description: Notaðu spálíkan okkar til að spá fyrir um hvort reikningur verði greiddur á réttum tíma.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 613d20e3b4132cdf797586441bff0688a2076692
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315503"
---
# <a name="the-late-payment-prediction-extension"></a>Viðbót greiðsludráttarspár  
Árangursrík stjórnun viðskiptakrafna er mikilvæg fyrir heildar fjárhagslega heilsu fyrirtækis. Viðbót greiðsludráttarspár getur hjálpað þér að draga úr útistandandi kröfum og fínstilla stefnu sjóðsins með því að spá fyrir um hvort sölureikningar verði greiddar á réttum tíma. Til dæmis, ef spá telur greiðsla vera sein, gætir þú ákveðið að lagfæra skilmála greiðslu eða greiðslumáta fyrir viðskiptamanninn.

## <a name="what-are-predictions-based-on"></a>Á hverju eru spár byggðar?  
Viðbót greiðsludráttarspár notar spálíkan sem við þróuðum í Azure-vélnámsstúdíói og þjálfuðum með því að nota gögn sem eru dæmigerð fyrir fjölda lítilla og meðalstórra fyrirtækja. Þó að við höfum nú þegar þjálfað og metið það, þá mun spálíkan okkar halda áfram að læra af gögnum þínum. Því meira sem þú notar líkanið og því fleiri gögn sem þú færir inn í það, því nákvæmari spár verða. Sjálfgefið er að viðbótin metur líkanið og uppfærir spárnar vikulega. Hins vegar er hægt að uppfæra spár þegar þú vilt með því að velja **Uppfæra spár** aðgerð á síðunni **Færslur í viðskiptamannabók**.  

> [!Note]
> Við notum smá af reikningstíma þinn í hverri viku þegar við metum líkanið og uppfærum spár þínar. Til viðbótar við handvirkt uppfærslu spár þínar eru aðrar aðgerðir sem neyta reikningstíma þegar þú þjálfar líkanið (sem þú gætir gert ef þú hefur nýlega bætt við gögnum) og þegar þú metur líkanið (sem lítur á gæði líkansins).

## <a name="getting-started"></a>Hafist handa
Viðbótin er ókeypis í [!INCLUDE[d365fin](includes/d365fin_md.md)] og við bjóðum áskrift á Azure-vélnámi. Áskriftin býður upp á 30 mínútur af reikningstíma á mánuði. Ef þú þarft meira en það geturðu búið til eigin fspálíkan og notað það í staðinn. Nánari upplýsingar er að finna í kaflanum sem heitir _Smíðaðu þitt eigið spálíkan_ síðar í þessu efnisatriði.  

Þegar þú opnar bókað söluskjal birtist tilkynning efst á síðunni. Til að nota Viðbót greiðsludráttarspár geturðu tekið þátt með því að velja **Virkja** í tilkynningunni. Einnig er hægt að setja upp viðbótina handvirkt. Til dæmis, ef þú iðrast þess að hafna tilkynningunni.  

Til að virkja viðbótina handvirkt skaltu fylgja þessum skrefum:

1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustutengingar** og veldu síðan tengda hlekkinn.  
2. Veldu **Uppsetning greiðsludráttarspár** valkostinn og síðan fylltu inn reitina eftir þörfum.

## <a name="viewing-all-payment-predictions"></a>Skoðar allar greiðsluspár
Ef þú virkjar viðbót verður **Greiðslur sem spáð er að munu dragast** flís tiltæk í **Viðskiptastjórnandi** í Mitt hlutverk. Flísin sýnir fjölda greiðslna sem spáð er að dragist, og gerir þér kleift að opna **viðskiptamannafærslur** síðuna þar sem þú getur grafið dýpra í bókaða reikninga. Það eru þrjár dálkar sem veita skal eftirtekt:  

* **Greiðsludráttur** - Gefur til kynna hvort dráttur verði á greiðslu reikningsins.
* **Áreiðanleiki spár** - Gefur til kynna hversu áreiðanlegt þú ættir að telja spánna vera. **Mikill** þýðir að spáin er að minnsta kosti 90% viss, **Miðlungs** er á milli 80 og 90% og **Lítill** er undir 80%.
* **Áreiðanleiki spár %** - Sýnir raunverulega prósentu á bak við áreiðanleikamatið. Sjálfgefið er að þessi dálkur er ekki sýndur, en þú getur bætt því við ef þú vilt. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

> [!Tip]
> Síðan Viðskiptamannafærslur sýnir einnig Upplýsingakassa til hægri. Á meðan þú ert að yfirfara spár, geta upplýsingarnar í **Upplýsingar um viðskiptamenn** hlutanum verið gagnlegar. Þegar þú velur reikninginn í listanum birtir hlutinn upplýsingar um viðskiptamanninn. Það gerir þér jafnframt kleift að hefja aðgerðir strax. Ef viðskiptamaður setur til dæmis oft veskið sitt á rangan stað getur þú opnað viðskiptamannakortið frá Upplýsingakassanum og útilokað viðskiptamanninn frá framtíðarsölu.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Skoðar greiðsluspá fyrir tiltekið söluskjal
Þú getur einnig sagt fyrir um greiðsludrátt fyrirfram. Á síðunum **Sölutilboð**, **Sölupantanir** og **Sölureikningar** geturðu notað **Spá fyrir um greiðslu** aðgerðina til að búa til spá fyrir söluskjalið sem þú ert að skoða.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Búðu til eigin spálíkan
Hefurðu áhuga á að byggja upp eigin spálíkan? Þú getur notað Azure-vélnámsstúdíó til að byggja upp eigin spálíkan og nota það í [!INCLUDE[d365fin](includes/d365fin_md.md)] . Til að nota eigin líkan þarftu að gerast áskrifandi að Azure-vélnám. Nánari upplýsingar er að finna í [Fylgiskjöl fyrir Azure-vélnámsstúdíó](https://go.microsoft.com/fwlink/?linkid=861765).  

Við bjóðum hins vegar auðveldara leið fyrir þig til að búa til og nota eigin spálíkan. Þú getur deilt gögnum úr reikningum þínum með [Forspártilraun okkar fyrir Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?linkid=2086310) í Azure-vélnámi og látið tilraun okkar búa til og þjálfa spálíkan byggt á gögnum þínum. Til að deila gögnum, á síðunni **Uppsetning greiðsludráttarspár** skal velja **Búa til mitt líkan** aðgerð. Eftir það mun spár byggjast á líkaninu og gögnunum þínum, ekki okkar.  

> [!Note]
>   Gæði líkansins er mikilvægt. Þegar forspártilraunin okkar notar gögnin þín til að þjálfa líkan ákvarðar það gæðagildi fyrir líkanið í prósentum. Gæði líkansins gefur til kynna hversu nákvæmar spár líkansins séu líklegar að vera. Nokkrir þættir geta haft áhrif á gæði líkansins. Til dæmis, þessar þættir gætu verið að ekki voru næg gögn eða að gögnin innihéldu ekki nógu mikinn breytileika. Hægt er að skoða gæði líkansins sem þú ert að nota núna á síðunni **Uppsetning greiðsludráttaspár**. Þú getur einnig tilgreint lágmarksþröskuld fyrir gæði líkansins. Líkön með gæðagildi fyrir neðan þröskuldinn munu ekki framleiða spár.  

### <a name="to-use-your-model-instead-of-ours"></a>Að nota líkanið þitt í stað okkar  
Ef þú býrð til eigin líkan í Azure-vélnámsstúdíói, án þess að nota verkfæri í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að gefa upp innskráningarupplýsingar þína svo að [!INCLUDE[d365fin](includes/d365fin_md.md)] hafi aðgang að líkaninu. Það eru nokkrar skref til að gera þetta:

1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning greiðsludráttaspár**, og veldu síðan tengda hlekkinn.  
2. Veldu **Nota Azure-áskriftina mína** gátreitinn.  
3. Í **Valið líkan** reitinn, veldu **Mitt líkan**.  
4. Í **Innskráningarupplýsingar fyrir líkanið mitt** flýtiflipanum, sláðu inn API slóðina og API lykil fyrir líkanið.  

## <a name="see-also"></a>Sjá einnig  
[Fylgiskjöl fyrir Azure-vélnámsstúdíó](https://go.microsoft.com/fwlink/?linkid=861765)  
[Sérstilling Business Central með viðbótum](ui-extensions.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
