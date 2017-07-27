---
title: "Vinna með birgðir| Microsoft Docs"
description: "Lýsir því hvernig skal vinna með efnislegar vörur sem þú átt viðskipti með, til dæmis að meðhöndla birgðir í vöruhúsinu."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 920df314dc8b671d4e2d99d8449ee02a74cb9078
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017

---

# <a name="inventory"></a>Birgðir
Fyrir hverja vöru sem þú ert að eiga viðskipti með þarftu að búa til hlutakort af tegundinni **Birgðir**. Vörur sem þú býður viðskiptavinum en geymir ekki í birgðum er hægt að skrá sem utanbirgðavörur sem hægt er að breyta í birgðavara þegar þörf krefur. Hægt að auka eða minnka magn vöru í birgðum með því að bóka beint í birgðafærslur, til dæmis þegar eftir raunbirgðatalningu eða ef þú skráir ekki innkaup.

Birgðaaukning og minnkun eru auðvitað líka skráðar þegar þú bókar innkaupaskjöl og söluskjöl. Nánari upplýsingar eru í [Hvernig á að skrá innkaup](purchasing-how-record-purchases.md) eða [hvernig á að: selja vörur.](sales-how-sell-products.md) og [hvernig á að: reikningsfæra sölur](sales-how-invoice-sales.md). Flutningur milli staða breytir birgðamagni yfir vörugeymslur fyrirtækisins.   

Til að auka yfirlit yfir vörur og til að hjálpa þér að finna þær, geturðu flokka vörur og gefa þeim eigindir til að leita að og raða eftir.

Þú verður að tryggja að kostnaður vara sé framsendur á viðeigandi sölufærslur á útleið, sérstaklega þar sem vörur eru seldar áður en reikningur er gefinn út fyrir kaupunum. Þetta er kallað kostnaðarleiðrétting, hægt er að framkvæma hana handvirkt eða stilla þannig að hún eigi sér stað sjálfkrafa þegar vörufærsla er bókuð.

## <a name="inventory-reconciliation"></a>Afstemming birgða
Þegar birgðafærslur, til dæmis söluafhending, innkaupareikningur eða birgðaleiðrétting eru bókaðar eru breytingar á kostnaði hinnar leiðréttu vöru skráðar í virðisfærslum birgða. Til að endurspegla þessar breytingar á birgðavirði í ársreikningum, er birgðakostnaður bókaður sjálfkrafa á tengda birgðareikninga í fjárhag. Fyrir hverja birgðafærslu sem er bókuð er viðeigandi gildi bókað í birgðareikninginn, leiðréttingarreikninginn og KSV-reikninginn í fjárhagnum.

Þó svo birgðakostnaður sé bókaður sjálfkrafa í fjárhag þarf samt að tryggja að kostnaður vara sé framsendur á viðeigandi sölufærslur á útleið, sérstaklega þar sem vörur eru seldar áður en reikningur er gefinn út fyrir kaupunum. Í kerfinu er þetta kallað kostnaðarleiðrétting. Vörukostnaður er sjálfkrafa leiðréttur þegar vörufærslur eru bókaðar en einnig er hægt að leiðrétta vörukostnað handvirkt. Nánari upplýsingar eru í Hvernig á að: leiðrétta kostnað.

|Til |Sjá |
|---|----|
|Stofna birgðaspjöld fyrir birgðavörur sem boðið er upp á.|[Hvernig á að Skrá nýjar vörur](inventory-how-register-new-items.md)|
|Byggðu upp yfireiningu sem þú selur sem undireiningar sem samanstanda af yfiríhlutnum eða sem þú setja saman í pöntun eða í birgðir.|[Hvernig á að: Vinna með uppskriftir](inventory-how-work-BOMs.md)|
|Viðhalda yfirlit yfir vörur og hjálp þér að finna og flokka vörur með því að skipuleggja þær í flokkum.|[Hvernig á að: Flokka vörur](inventory-how-categorize-items.md)|
|Úthluta vörunum þínum vörueigindum mismunandi virðistegunda til að hjálpa þér að flokka og finna vörur.|[Hvernig á að: Vinna með vörueigindir](inventory-how-work-item-attributes.md)|
|Stofna sérstaka birgðaspjald fyrir vörur sem boðnar eru viðskiptamönnum en viðheldur ekki birgðum fyrir.|[Hvernig á að: Vinna með Utanbirgðavörur](inventory-how-work-nonstock-items.md)|
|Framkvæma rauntalningu, gera neikvæðar eða jákvæðar leiðréttingar, og breyta upplýsingum, eins og t.d. staðsetningu eða lotunúmer, á birgðafærslum.|[Hvernig skal: Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md)|
|Skoðaðu framboð á hlutum eftir hverri staðsetningu, eftir sölu eða innkaupatilviki, eða eftir notkun á samsetningaruppskrift.|[Hvernig skal: Skoða tiltækileika vöru](inventory-how-availability-overview.md)|
|Flytja birgðavörur á milli staða með flutningspöntun, til að stjórna vöruhúsaaðgerðum eða með vöruendurflokkunarbók.|[Hvernig á að: Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)|
|Hækka eða lækka virði einnar eða fleiri vara í birgðaskrá með því að bóka núverandi, útreiknað virði þeirra.|[Hvernig á að: Endurmeta birgðir](inventory-how-revalue-inventory.md)|
|Leiðrétta kostnað vöru, annaðhvort sjálfvirkt eða handvirkt til að áframsenda kostnaðarbreytingar úr færslum á innleið í tengdar færslur á útleið.|[Hvernig á að: Leiðrétta birgðakostnað](inventory-how-adjust-item-costs.md)|

## <a name="see-also"></a>Sjá einnig  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)    
[Aðfangakeðja](madeira-supply-chain.md)  
[Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
