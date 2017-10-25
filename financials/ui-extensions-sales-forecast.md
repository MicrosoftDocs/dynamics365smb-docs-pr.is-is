---
title: "Nota viðbót fyrir sölu- og birgðaforspá til að stjórna birðgum | Microsoft Docs"
description: "Þessi viðbót aðstoðar þig við að spá fyrir um sölu, að fá skýrara yfirlit yfir líkur á birgðaskorti og jafnvel að fá aðstoð við að stofna áfyllingarbeiðnir til lánardrottna."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a0cac0236611c90d3d1fdf1bae9deaaeb235b540
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="sales-and-inventory-forecast-for-dynamics-365-for-financials"></a>Sölu- og birgðaáætlun fyrir Dynamics 365 for Financials
Birgðastjórnun er málamiðlun á milli notendaþjónustu og stjónun kostnaðar. Ein hliðin er sú að lágar birgðir krefjast minna veltufés, en, á hinn bóginn getur birgðaskortur hugsanlega leitt til tapaðrar sölu. Viðbótin fyrir sölu- og birgðaspá sér fyrir hugsanlegar sölur með því að nota söguleg gögn og veitir skýrt yfirlit yfir viðbúinn birgðaskort. Samkvæmt spá, aðstoðar viðbótin að stofna áfyllingarbeiðnir til lánardrottna þinna og sparar þér tíma.  

## <a name="setting-up-forecasting"></a>Spáruppsetning
Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er tengingin við [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) þegar sett upp fyrir þig. En hægt er að grunnstilla spá til að nota aðra tímabilsgerð til að gefa skýrslur samkvæmt, eins og að breyta úr spám samkvæmt mánuðum í spám samkvæmt ársfjórðungum. Einnig er hægt að velja fjölda tímabila sem á að reikna spá eftir, eftir því hversu grófgerð spáin á að vera. Við að leggja til að spá eftir mánuðum og með 12 mánaða sjóndeildarhring fyrir spána.  

## <a name="using-the-forecasts"></a>Notkun spáa
Þessi viðbót notar Cortana Intelligence til að spá fyrir um framtíðar sölu byggt á söluferli þínum til að hjálpa þér að komast hjá birgðaskorti. Til dæmis þegar valið er vöru í glugganum **Vörur** , í sýnir grafið á **vöruspá** svæðinu áætlaða sölu vörunnar á komandi tímabili. Þannig má sjá ef líklegt er að varan klárist fljótlega hjá þér.  

Einnig má nota viðbótina til að leggja til þegar þarf að fylla á birgðir. T.d. ef þú stofnar innkaupapöntun Fabrikam af því þú vilt kaupa nýja skrifstofustólinn þeirra, mun sölu- og birgðaspárviðbótin leggja til að þú bætir einnig á birgðir LONDON-snúningsstólsins sem þú kaupir yfirleitt frá þessum lánardrottni. Það er vegna þess viðbótin spáir að þú munir klára úr birgðum þennan London-snúningsstól á næstu tveimur mánuðum, svo þú gætir viljað panta fleiri stóla nú þegar.  

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  

