---
title: Vinna með birgðir| Microsoft Docs
description: Lýsir því hvernig skal vinna með efnislegar vörur sem þú átt viðskipti með, til dæmis að meðhöndla birgðir í vöruhúsinu.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a4c4788f7f262dee32f489095bf1ee303ea712c5
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2019
ms.locfileid: "939417"
---
# <a name="inventory"></a>Birgðir
Fyrir hverja vöru sem þú ert að eiga viðskipti með þarftu að búa til hlutakort af tegundinni **Birgðir**. Vörur sem þú býður viðskiptamönnum en geymir ekki í birgðum er hægt að skrá sem vörulistaatriði sem hægt er að breyta í birgðavara þegar þörf krefur. Hægt að auka eða minnka magn vöru í birgðum með því að bóka beint í birgðafærslur, til dæmis þegar eftir raunbirgðatalningu eða ef þú skráir ekki innkaup.

Birgðaaukning og minnkun eru auðvitað líka skráðar þegar þú bókar innkaupaskjöl og söluskjöl. Nánari upplýsingar eru í [Skrá innkaup](purchasing-how-record-purchases.md), [Selja vörur](sales-how-sell-products.md) og [Reikningsfæra sölur](sales-how-invoice-sales.md). Flutningur milli staða breytir birgðamagni yfir vörugeymslur fyrirtækisins.   

Til að auka yfirlit yfir vörur og til að hjálpa þér að finna þær, geturðu flokka vörur og gefa þeim eigindir til að leita að og raða eftir.

> [!NOTE]
> Raunmeðhöndlun birgða vísar til vöruhúsaaðgerða. Frekari upplýsingar eru í [Vöruhúsastjórnun](warehouse-manage-warehouse.md)

## <a name="inventory-reconciliation"></a>Afstemming birgða
Þegar birgðafærslur, til dæmis söluafhending, innkaupareikningur eða birgðaleiðrétting eru bókaðar eru breytingar á kostnaði hinnar leiðréttu vöru skráðar í virðisfærslum birgða. Til að endurspegla þessar breytingar á birgðavirði í ársreikningum, er birgðakostnaður bókaður sjálfkrafa á tengda birgðareikninga í fjárhag. Fyrir hverja birgðafærslu sem er bókuð er viðeigandi gildi bókað í birgðareikninginn, leiðréttingarreikninginn og KSV-reikninginn í fjárhagnum. Frekari upplýsingar eru í [Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Þó svo birgðakostnaður sé bókaður sjálfkrafa í fjárhag þarf samt að tryggja að kostnaður vara sé framsendur á viðeigandi sölufærslur á útleið, sérstaklega þar sem vörur eru seldar áður en reikningur er gefinn út fyrir kaupunum. Í kerfinu er þetta kallað kostnaðarleiðrétting. Vörukostnaður er sjálfkrafa leiðréttur þegar vörufærslur eru bókaðar en einnig er hægt að leiðrétta vörukostnað handvirkt. Nánari upplýsingar eru í [Leiðrétta kostnað](inventory-how-adjust-item-costs.md).

|Til |Sjá |
|---|----|
|Stofna birgðaspjöld fyrir birgðavörur sem boðið er upp á.|[Skrá nýjar vörur](inventory-how-register-new-items.md)|
|Byggðu upp yfireiningu sem þú selur sem undireiningar sem samanstanda af yfiríhlutnum eða sem þú setja saman í pöntun eða í birgðir.|[Vinna með uppskriftir](inventory-how-work-BOMs.md)|
|Viðhalda yfirlit yfir vörur og hjálp þér að finna og flokka vörur með því að skipuleggja þær í flokkum.|[Flokka vörur](inventory-how-categorize-items.md)|
|Úthluta vörunum þínum vörueigindum mismunandi virðistegunda til að hjálpa þér að flokka og finna vörur.|[Vinna með vörueigindir](inventory-how-work-item-attributes.md)|
|Stofna sérstaka birgðaspjald fyrir vörur sem boðnar eru viðskiptamönnum en viðheldur ekki birgðum fyrir.|[Vinna með vörulista](inventory-how-work-nonstock-items.md)|
|Framkvæma birgðatalningu með síðunum **Efnisleg birgðarpöntun** og **Efnisleg birgðarskráning**.|[Birgðatalning með skjölum](inventory-how-count-inventory-with-documents.md)|
|Framkvæma rauntalningu, gera neikvæðar eða jákvæðar leiðréttingar, og breyta upplýsingum, eins og t.d. staðsetningu eða lotunúmer, á birgðafærslum.|[Talning, breytingar og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md)|
|Skoðaðu framboð á hlutum eftir staðsetningu, eftir tímabili, eftir sölu eða innkaupatilviki, eða eftir notkun á samsetningar- eða framleiðsluuppskrift.|[Skoða tiltækileika vöru](inventory-how-availability-overview.md)|
|Flytja birgðavörur á milli staða með flutningspöntun, til að stjórna vöruhúsaaðgerðum eða með vöruendurflokkunarbók.|[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)|
|Hægt er að taka frá birgðavörur eða vörur á innleið fyrir sölu-, innkaupa-, þjónustu, samsetningar- og framleiðslupantanir.|[Taka frá vörur](inventory-how-to-reserve-items.md)|
|Setja upp eigin lýsingu lánardrottins eða viðskiptavinar fyrir vöru, þannig að þú getur auðveldlega fært vörulýsingu þeirra inn á viðskiptaskjöl.|[Nota millivísanir vöru](inventory-how-use-item-cross-refs.md)|
|Úthluta rað- eða lotunúmerum til sérhvers skjals á inn- eða útleið eða færslubókarlínu, til dæmis til að rekja vörur í tilviki innköllunar.|[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)|
|Setja upp eigin lýsingu lánardrottins eða viðskiptavinar á vöruspjald, þannig að þú getur fært vörulýsingu þeirra inn á viðskiptaskjöl.|[Nota millivísanir vöru](inventory-how-use-item-cross-refs.md)|
|Komast að því hvar rað- eða lotunúmer var notað í aðfangakeðju, til dæmis í innköllunaraðstæðum.|[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)|
|Loka á vörur svo þær verði ekki slegnar inn í sölu- eða innkaupalínur eða bókaðar í einhverri færslu.|[Loka vörum](inventory-how-block-items.md)|
|Stjórna viðskiptaaðgerðum á söluskrifstofum, innkaupadeildum, eða komið fyrir áætlunarskrifstofum í mörgum birgðageymslum.|[Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
