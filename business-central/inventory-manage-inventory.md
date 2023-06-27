---
title: Stjórnun birgða
description: Í þessari grein er lýst hvernig eigi að stjórna efnislegum vörum þú verslar með með því að búa til birgðavöruspjald.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.forms: '5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782'
ms.date: 06/16/2021
ms.author: edupont
---

# <a name="manage-inventory"></a>Stjórna birgðum

Fyrir hverja efnislega vöru sem þú átt í viðskiptum með þarftu að búa til birgðaspjald af gerðinni **Birgðir**. Vörur sem þú býður viðskiptamönnum en geymir ekki í birgðum er hægt að skrá sem vörulistaatriði sem hægt er að breyta í birgðavara þegar þörf krefur. Hægt að auka eða minnka magn vöru í birgðum með því að bóka beint í birgðafærslur, til dæmis þegar eftir raunbirgðatalningu eða ef þú skráir ekki innkaup.

Birgðaaukning og minnkun eru auðvitað líka skráðar þegar þú bókar innkaupaskjöl og söluskjöl. Fáðu frekari upplýsingar á [Skrá innkaup](purchasing-how-record-purchases.md), [Selja vörur](sales-how-sell-products.md) og [Reikningsfæra sölur](sales-how-invoice-sales.md). Flutningur milli staða breytir birgðamagni yfir vörugeymslur fyrirtækisins.

Til að auka yfirlit yfir vörur og til að hjálpa þér að finna þær, geturðu flokka vörur og gefa þeim eigindir til að leita að og raða eftir.

> [!NOTE]
> Raunmeðhöndlun birgða vísar til vöruhúsaaðgerða. Frekari upplýsingar á  [Yfirlit Vöruhúsakerstjórnunar](design-details-warehouse-management.md).

Áætlanagerð fyrir vörur til að uppfylla eftirspurn fellur undir virkni framboðsáætlanagerðar. Frekari upplýsingar eru í [Áætlanagerð](production-planning.md).  

## <a name="inventory-reconciliation"></a>Afstemming birgða

Þegar birgðafærslur, til dæmis söluafhending, innkaupareikningur eða birgðaleiðrétting eru bókaðar eru breytingar á kostnaði hinnar leiðréttu vöru skráðar í virðisfærslum birgða. Til að endurspegla þessar breytingar á birgðavirði í ársreikningum, er birgðakostnaður bókaður sjálfkrafa á tengda birgðareikninga í fjárhag. Fyrir hverja birgðafærslu sem er bókuð er viðeigandi gildi bókað í birgðareikninginn, leiðréttingarreikninginn og KSV-reikninginn í fjárhagnum. Frekari upplýsingar eru í [Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Þó svo birgðakostnaður sé bókaður sjálfkrafa í fjárhag þarf samt að tryggja að kostnaður vara sé framsendur á viðeigandi sölufærslur á útleið, sérstaklega þar sem vörur eru seldar áður en reikningur er gefinn út fyrir kaupunum. Í kerfinu er þetta kallað kostnaðarleiðrétting. Vörukostnaður er sjálfkrafa leiðréttur þegar vörufærslur eru bókaðar en einnig er hægt að leiðrétta vörukostnað handvirkt. Frekari upplýsingar um  [leiðréttan vörukostnað](inventory-how-adjust-item-costs.md).  

## <a name="related-tasks"></a>Tengd verkefni

Eftirfarandi tafla sýnir tengd verk.

|Til |Sjá |
|---|----|
|Stofna birgðaspjöld fyrir birgðavörur sem boðið er upp á.|[Skrá nýjar vörur](inventory-how-register-new-items.md)|
|Byggðu upp yfireiningu sem þú selur sem undireiningar sem samanstanda af yfiríhlutnum eða sem þú setja saman í pöntun eða í birgðir.|[Vinna með uppskriftir](inventory-how-work-BOMs.md)|
|Viðhalda yfirlit yfir vörur og hjálp þér að finna og flokka vörur með því að skipuleggja þær í flokkum.|[Flokka vörur](inventory-how-categorize-items.md)|
|Úthluta vörunum þínum vörueigindum mismunandi virðistegunda til að hjálpa þér að flokka og finna vörur.|[Vinna með vörueigindir](inventory-how-work-item-attributes.md)|
|Búðu til sérstök birgðaspjöld fyrir vörur sem þú býður viðskiptamönnum en heldur ekki við í birgðum.|[Vinna með vörulista](inventory-how-work-nonstock-items.md)|
|Framkvæma birgðatalningu með síðunum **Efnisleg birgðarpöntun** og **Efnisleg birgðarskráning**.|[Birgðatalning með skjölum](inventory-how-count-inventory-with-documents.md)|
|Framkvæma rauntalningu, gera neikvæðar eða jákvæðar leiðréttingar, og breyta upplýsingum, eins og t.d. staðsetningu eða lotunúmer, á birgðafærslum.|[Talning, breytingar og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md)|
|Skoðaðu framboð á hlutum eftir staðsetningu, eftir tímabili, eftir sölu eða innkaupatilviki, eða eftir notkun á samsetningar- eða framleiðsluuppskrift.|[Skoða tiltækileika vöru](inventory-how-availability-overview.md)|
|Flyttu birgðavörur á milli staða með flutningspöntun, til að stjórna vöruhúsaaðgerðum eða með vöruendurflokkunarbók.|[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)|
|Hægt er að taka frá birgðavörur eða vörur á innleið fyrir sölu-, innkaupa-, þjónustu, samsetningar-, flutnings- og framleiðslupantanir.|[Taka frá vörur](inventory-how-to-reserve-items.md)|
|Settu upp vörurakningu svo þú getir rakið raðnúmer vöru, t.d. þegar þú þarft að rekja vörur vegna innköllunar.|[Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer](inventory-how-setup-item-tracking.md)|
|Úthluta rað- eða lotunúmerum til sérhvers skjals á inn- eða útleið eða færslubókarlínu.|[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)|
|Finndu út hvar rað- eða lotunúmer var notað í aðfangakeðju, til dæmis í innköllunaraðstæðum.|[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)|
|Setja upp eigin lýsingu lánardrottins eða viðskiptavinar á vöruspjald, þannig að þú getur fært vörulýsingu þeirra inn á viðskiptaskjöl.|[Nota vörutilvísanir](inventory-how-use-item-cross-refs.md)|
|Loka á vörur svo þær verði ekki slegnar inn í sölu- eða innkaupalínur eða bókaðar í einhverri færslu.|[Loka vörum](inventory-how-block-items.md)|
|Stjórna viðskiptaaðgerðum á söluskrifstofum, innkaupadeildum, eða komið fyrir áætlunarskrifstofum í mörgum birgðageymslum.|[Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md)|
|Notaðu tilföng með sérstökum aðgerðum fyrir ýmsa þjónustu og þjónustuvörur.|[Setja upp forðaúthlutun](service-how-setup-resource-allocation.md)|

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/get-started-inventory-management/)

## <a name="see-also"></a>Sjá einnig .

[Yfirlýsing](design-details-warehouse-management.md)
[um Vöruhúsakerfi kaupfélag](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
