---
title: Nota viðbót fyrir sölu- og birgðaforspá til að stjórna birðgum | Microsoft Docs
description: Þessi viðbót aðstoðar þig við að spá fyrir um sölu, að fá skýrara yfirlit yfir líkur á birgðaskorti og jafnvel að fá aðstoð við að stofna áfyllingarbeiðnir til lánardrottna.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f55bad5c26e1f1fbb336090ff862e0e931ff9c39
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784741"
---
# <a name="the-sales-and-inventory-forecast-extension"></a>Spá um sölu og birgðir viðbótina
Birgðastjórnun er málamiðlun á milli notendaþjónustu og stjónun kostnaðar. Ein hliðin er sú að lágar birgðir krefjast minna veltufés, en, á hinn bóginn getur birgðaskortur hugsanlega leitt til tapaðrar sölu. Viðbótin fyrir sölu- og birgðaspá sér fyrir hugsanlegar sölur með því að nota söguleg gögn og veitir skýrt yfirlit yfir viðbúinn birgðaskort. Samkvæmt spá, aðstoðar viðbótin að stofna áfyllingarbeiðnir til lánardrottna þinna og sparar þér tíma.  

## <a name="setting-up-forecasting"></a>Spáruppsetning
Í [!INCLUDE[prod_short](includes/prod_short.md)] er tengingin við [Azure AI](https://azure.microsoft.com/overview/ai-platform/) þegar sett upp fyrir þig. En hægt er að grunnstilla spá til að nota aðra tímabilsgerð til að gefa skýrslur samkvæmt, eins og að breyta úr spám samkvæmt mánuðum í spám samkvæmt ársfjórðungum. Einnig er hægt að velja fjölda tímabila sem á að reikna spá eftir, eftir því hversu grófgerð spáin á að vera. Við að leggja til að spá eftir mánuðum og með 12 mánaða sjóndeildarhring fyrir spána. 

> [!TIP]  
>   Íhugaðu lengd tímabila sem þjónustan er notaður í útreikningum hennar. Frekari gögn sem veita verður því nákvæmari á predictions. Líka watch út fyrir mikið frávik í tímabil. Þeir eru einnig hefur predictions. Ef Azure AI finnur ekki næg gögn eða gögnin breytast við lotu mun þjónustan ekki framkvæma forspá.

## <a name="using-the-forecasts"></a>Notkun spáa
Þessi viðbót notar Azure AI til að spá fyrir um framtíðarsölu byggt á söluferli þínum til að hjálpa þér að komast hjá birgðaskorti. Til dæmis þegar valið er vöru á síðunni **Vörur** , í sýnir grafið á **vöruspá** svæðinu áætlaða sölu vörunnar á komandi tímabili. Þannig má sjá ef líklegt er að varan klárist fljótlega hjá þér.  

Einnig má nota viðbótina til að leggja til þegar þarf að fylla á birgðir. T.d. ef þú stofnar innkaupapöntun Fabrikam af því þú vilt kaupa nýja skrifstofustólinn þeirra, mun sölu- og birgðaspárviðbótin leggja til að þú bætir einnig á birgðir LONDON-snúningsstólsins sem þú kaupir yfirleitt frá þessum lánardrottni. Það er vegna þess viðbótin spáir að þú munir klára úr birgðum þennan London-snúningsstól á næstu tveimur mánuðum, svo þú gætir viljað panta fleiri stóla nú þegar.  

## <a name="design-details"></a>Hönnunarupplýsingar
Áskriftum að [!INCLUDE[prod_short](includes/prod_short.md)] fylgir aðgangur að nokkrum forspárþjónustum á netinu á öllum stöðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þær vita ekki gögn.

> [!NOTE]  
>   Einnig er hægt að nota eigin forspárþjónustu á netinu í stað okkar. Nánari upplýsingar er að finna í [Búa til og nota eigin forspárþjónustu á netinu fyrir sölu- og birgðaspá](#AnchorText). 

### <a name="data-required-for-forecast"></a>Gögn eru nauðsynleg fyrir forspá
Til að spá fyrir um sölu í framtíðinni þarf vefþjónustan magnbundin gögn um fyrri sölur. Þessi gögn koma úr reitunum **Bókunardagsetning**, **Vörunr.** og **Magn** á síðunni **Birgðabókafærslur**, þar sem:
-    Færslugerðin er „Sala“.
- Bókunardagsetningin er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sölu- og birgðaspár** og vinnudagsetningarinnar.

Áður en vefþjónustan er notuð þjappar [!INCLUDE[prod_short](includes/prod_short.md)] færslum eftir **Vörunr.** og **Bókunardagsetning** samkvæmt gildinu í reitnum **Tímabilsgerð** á síðunni **Uppsetning sölu- og birgðaspár**.

## <a name="create-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Búa til og nota eigin forspárþjónustu á netinu fyrir sölu- og birgðaspá
Þú getur einnig búið til þína eigin fyrirsjáanlega vefþjónustu byggt á opinberu líkani sem heitir **Spárlíkan fyrir Microsoft Business Central**. Þetta líkan er aðgengilegt á netinu í Azure AI. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu á [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Leita að **Forspármódel fyrir Microsoft Business Central** og opna svo líkanið í Azure Machine Learning Studio.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sölu- og birgðaspár** og veldu síðan tengda tengilinn.  
7. Stækkaðu flýtiflipann **Almennt** og fylltu síðan út reiti fyrir API-vefslóð og API-lykil.  


## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]