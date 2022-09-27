---
title: Stjórnun birgða
description: Þessi grein lýsir því hvernig á að stjórna efnislegum vörum sem eru í viðskiptum í með því að stofna birgðavöruspjald.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.search.forms: 5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 568ccee7e01aacb429e6ed2e2b69daf91f67b488
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530028"
---
# <a name="manage-inventory"></a>Stjórna birgðum

Fyrir hverja efnislega vöru sem viðskipti eru gerð við þarf að stofna birgðaspjald af **Birgðagerð**. Vörur sem þú býður viðskiptavinum en halda ekki í birgðum er hægt að skrá sem vörulistavörur, sem hægt er að umbreyta í birgðavörur þegar þörf krefur. Hægt er að auka eða minnka magn vöru í birgðum með því að bóka beint í birgðafærslurnar, eins og eftir rauntalningu eða ef ekki eru skráð innkaup.

Birgðaaukning og minnkun er náttúrlega einnig skráð þegar innkaupa-og söluskjöl eru bókuð. Lærðu meira við skráningu innkaupa [,](purchasing-how-record-purchases.md) sölu á vörum [og](sales-how-sell-products.md) í [sölusölum](sales-how-invoice-sales.md). Færslur milli staða breyta birgðamagni yfir vöruhús fyrirtækisins.

Til að auka yfirlit yfir vörur og til að auðvelda þér að finna þær er hægt að flokka vörur og gefa þeim eigindir til að leita og raða eftir.

> [!NOTE]
> Raunmeðhöndlun birgða vísar til vöruhúsaaðgerða. Laern meira við [vöruhúsastjórnun](warehouse-manage-warehouse.md).

Áætlanagerð fyrir vörur til að uppfylla eftirspurn fellur undir virkni framboðsáætlanagerðar. Frekari upplýsingar í [Áætlanagerð](production-planning.md).  

## <a name="inventory-reconciliation"></a>Afstemming birgða

Þegar birgðafærslur, til dæmis söluafhending, innkaupareikningur eða birgðaleiðrétting eru bókaðar eru breytingar á kostnaði hinnar leiðréttu vöru skráðar í virðisfærslum birgða. Til að endurspegla þessa breytingu á birgðavirði í fjármálabókum er birgðakostnaður bókaður sjálfkrafa á tengda birgðareikninga í fjárhag. Fyrir hverja birgðafærslu sem er bókuð eru viðeigandi gildi bókuð á birgðareikninginn, leiðréttingarlykilinn og lykilinn KÓGS í fjárhag. Frekari upplýsingar um hvernig á [að stemma af birgðakostnað við fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Þó svo birgðakostnaður sé bókaður sjálfkrafa í fjárhag þarf samt að tryggja að kostnaður vara sé framsendur á viðeigandi sölufærslur á útleið, sérstaklega þar sem vörur eru seldar áður en reikningur er gefinn út fyrir kaupunum. Í kerfinu er þetta kallað kostnaðarleiðrétting. Vörukostnaður er sjálfkrafa leiðréttur þegar vörufærslur eru bókaðar en einnig er hægt að leiðrétta vörukostnað handvirkt. Larn meira at [Stilla vörukostnað](inventory-how-adjust-item-costs.md).  

## <a name="related-tasks"></a>Tengd verkefni

Eftirfarandi tafla sýnir tengd verk.

|Til |Sjá |
|---|----|
|Stofna birgðaspjöld fyrir birgðavörur sem boðið er upp á.|[Skrá nýjar vörur](inventory-how-register-new-items.md)|
|Uppbygging yfirliði vörur sem þú selur sem pökkum sem samanstanda af yfirþáttum eða sem þú kemur þér saman til að panta eða til á lager.|[Vinna með uppskriftir](inventory-how-work-BOMs.md)|
|Viðhalda yfirlit yfir vörur og hjálp þér að finna og flokka vörur með því að skipuleggja þær í flokkum.|[Flokka vörur](inventory-how-categorize-items.md)|
|Úthluta vörunum þínum vörueigindum mismunandi virðistegunda til að hjálpa þér að flokka og finna vörur.|[Vinna með vörueigindir](inventory-how-work-item-attributes.md)|
|Stofna Sérstök birgðaspjöld fyrir vörur sem boðið er upp á til viðskiptavina en ekki Viðhalda í birgðum.|[Vinna með vörulista](inventory-how-work-nonstock-items.md)|
|Framkvæma birgðatalningu með síðunum **Efnisleg birgðarpöntun** og **Efnisleg birgðarskráning**.|[Birgðatalning með skjölum](inventory-how-count-inventory-with-documents.md)|
|Framkvæma rauntalningu, gera neikvæðar eða jákvæðar leiðréttingar, og breyta upplýsingum, eins og t.d. staðsetningu eða lotunúmer, á birgðafærslum.|[Talning, breytingar og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md)|
|Skoða ráðstöfunarmagn vara, eftir tímabilum, sölu-eða innkaupaatburð, eða notkun þeirra við samsetningu eða framleiðslu uppskrifta (uppskrifta).|[Skoða tiltækileika vöru](inventory-how-availability-overview.md)|
|Flytja birgðavörur milli birgðageymslna sem nota flutningspantanir til að stjórna vöruhúsaaðgerðum eða með birgðaendurflokkunarbók.|[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)|
|Taka frá birgðir eða vörur á innleið fyrir sölupantanir, innkaupapantanir, þjónustupantanir, samsetningarpantanir, flutningspantanir eða framleiðslupantanir.|[Taka frá vörur](inventory-how-to-reserve-items.md)|
|Setjið upp vörurakningu svo hægt sé að rekja raðnúmer vöru, eins og þegar þörf er á að rekja vörur vegna afganga.|[Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer](inventory-how-setup-item-tracking.md)|
|Úthluta rað- eða lotunúmerum til sérhvers skjals á inn- eða útleið eða færslubókarlínu.|[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)|
|Finna hvar eitthvert rað-eða lotunúmer var notað í aðfangakeðjunni, eins og í mansalaðstæðum.|[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)|
|Settu upp eigin vörulýsingu lánardrottins eða viðskiptavinar á birgðaspjaldinu þínu svo fljótlegt sé að setja inn vörulýsingu þeirra á viðskiptakjör.|[Nota vörutilvísanir](inventory-how-use-item-cross-refs.md)|
|Loka á vörur svo þær verði ekki slegnar inn í sölu- eða innkaupalínur eða bókaðar í einhverri færslu.|[Loka vörum](inventory-how-block-items.md)|
|Umsjón með rekstri fyrirtækja í söluskrifstofum, innkaupadeildum eða verksmiðjuáætlunarstofum á mörgum stöðum.|[Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md)|
|Notið tilföng með sértækum aðgerðum fyrir ýmsa þjónustu og þjónustuvöru.|[Setja upp forðaúthlutun](service-how-setup-resource-allocation.md)|

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/paths/get-started-inventory-management/)

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
