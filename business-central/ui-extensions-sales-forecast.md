---
title: Notkun viðbóta við sölu- og birgðaspá til að stjórna birgðum
description: 'Þessi viðbót aðstoðar þig við að spá fyrir um sölu, að fá skýrara yfirlit yfir líkur á birgðaskorti og jafnvel að fá aðstoð við að stofna áfyllingarbeiðnir til lánardrottna.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 07/01/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-sales-and-inventory-forecast-extension"></a>Viðbót við sölu- og birgðaspá

Birgðastjórnun er málamiðlun á milli notendaþjónustu og stjónun kostnaðar. Ein hliðin er sú að lágar birgðir krefjast minna veltufés, en, á hinn bóginn getur birgðaskortur hugsanlega leitt til tapaðrar sölu. Viðbótin fyrir sölu- og birgðaspá sér fyrir hugsanlegar sölur með því að nota söguleg gögn og veitir skýrt yfirlit yfir viðbúinn birgðaskort. Samkvæmt spá, aðstoðar viðbótin að stofna áfyllingarbeiðnir til lánardrottna þinna og sparar þér tíma.  

## <a name="setting-up-forecasting"></a>Spáruppsetning

Í [!INCLUDE[prod_short](includes/prod_short.md)] er tengingin við [Azure AI](https://azure.microsoft.com/overview/ai-platform/) þegar sett upp fyrir þig. En hægt er að grunnstilla spá til að nota aðra tímabilsgerð til að gefa skýrslur samkvæmt, eins og að breyta úr spám samkvæmt mánuðum í spám samkvæmt ársfjórðungum. Einnig er hægt að velja fjölda tímabila sem á að reikna spá eftir, eftir því hversu grófgerð spáin á að vera. Við að leggja til að spá eftir mánuðum og með 12 mánaða sjóndeildarhring fyrir spána.

> [!TIP]  
> Íhugaðu lengd tímabila sem þjónustan er notaður í útreikningum hennar. Frekari gögn sem veita verður því nákvæmari á predictions. Líka watch út fyrir mikið frávik í tímabil. Þeir eru einnig hefur predictions. Ef Azure AI finnur ekki næg gögn eða gögnin breytast við lotu mun þjónustan ekki framkvæma forspá.

## <a name="use-the-forecasts"></a>Nota spár

Þessi viðbót notar Azure AI til að spá fyrir um framtíðarsölu byggt á söluferli þínum til að hjálpa þér að komast hjá birgðaskorti. Til dæmis þegar valið er vöru á síðunni **Vörur** , í sýnir grafið á **vöruspá** svæðinu áætlaða sölu vörunnar á komandi tímabili. Þannig er hægt að sjá hvort líklegt sé að birgðir af vörunni fari fljótlega af stað.  

Einnig má nota viðbótina til að leggja til þegar þarf að fylla á birgðir. Til dæmis væri hægt að búa til innkaupapöntun fyrir Fabrikam til að kaupa nýja skrifborðsstólinn þeirra. Viðauki sölu- og birgðaspárinnar gæti lagt til að einnig sé settur aftur á sundstólINN í LONDON sem venjulega er keyptur frá þessum lánardrottni. Viðbótin getur spáð því að þú munir brátt keyra út af lager af LONDON swivel stólnum, þannig að þú gætir pantað fleiri stóla nú þegar.  

## <a name="design-details"></a>Hönnunarupplýsingar

Áskriftum að [!INCLUDE[prod_short](includes/prod_short.md)] fylgir aðgangur að nokkrum forspárþjónustum á netinu á öllum stöðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þau geyma ekki gögn.

> [!NOTE]  
>   Einnig er hægt að nota eigin forspárþjónustu á netinu í stað okkar. Nánari upplýsingar er að finna í [Búa til og nota eigin forspárþjónustu á netinu fyrir sölu- og birgðaspá](#AnchorText). 

### <a name="data-required-for-forecast"></a>Gögn eru nauðsynleg fyrir forspá

Til að spá fyrir um sölu í framtíðinni þarf vefþjónustan magnbundin gögn um fyrri sölur. Þessi gögn koma úr reitunum **Bókunardagsetning**, **Vörunr.** og **Magn** á síðunni **Birgðabókafærslur**, þar sem:

- Færslugerðin er „Sala“.
- Bókunardagsetningin er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sölu- og birgðaspár** og vinnudagsetningarinnar.

Áður en vefþjónustan er notuð,þjappar [!INCLUDE[prod_short](includes/prod_short.md)]  færslum eftir **vörunr.** og **Bókunardagsetning** byggð á gildinu í reitnum **Tegund** tímabils á síðunni **Söluspá og Uppsetning** birgðaspár.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Búa til og nota eigin forspárþjónustu á netinu fyrir sölu- og birgðaspá

Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] netið er líkanið gefið út af Microsoft og tengt við Microsoft-áskriftina. Fyrir aðra virkjunarkosti þarf að búa til vélarnámsforða í eigin Azure-áskrift. Hægt er að finna sýniskref í [sýnishorninu](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Tilgangur þessa verks er að fá API-URI og API-lykil.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu- og birgðaspár** og velja síðan viðkomandi tengil.  
2. Stækkaðu flýtiflipann **Almennt** og fylltu síðan út reiti fyrir API-vefslóð og API-lykil.  

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Nota gervigreind í Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  
[Yfirlit yfir API spár](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
