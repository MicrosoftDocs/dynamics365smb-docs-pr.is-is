---
title: Samsetningarskýrslur og greiningar í Business Central
description: Finnið út hvaða samsetningarskýrslur eru í boði í staðlaðri útgáfu Business Central til að halda utan um reksturinn.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216370"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>Samsetningarskýrslur og greiningar í Business Central

Samsetningarskýrslugerð í [!INCLUDE [prod_short](includes/prod_short.md)] gerir starfsmönnum í framleiðslu og rekstri kleift að fá innsýn í og tölfræði um núverandi og fyrri samsetningaraðgerðir.  

## <a name="reports"></a>Skýrslur

Eftirfarandi tafla lýsir sumum helstu skýrslunum í samstingarskýrslugerð.

|Skýrsla |Kenni hlutar|Description  |
|---------|---------|---------|
|**Samsetningaruppskriftir**|801|Birtir lista yfir uppskriftir: heiti uppskrifta, númer uppskrifta, íhluti uppskrifta og þær uppskriftir aðrar sem eru íhlutir í uppskriftinni sem um ræðir. Uppskriftaíhlutirnir eru skilgreindir í töflunni BOM Component. Hér má einnig sjá mælieininguna og nauðsynlegt magn hvers íhlutar fyrir hverja grunnmælieiningu. |
|**Vara – Hægt að ná (tími)**|5871|Sýnir hvernig fimm mismunandi lykilráðstöfunartölur breytast með tímanum fyrir uppskriftarvöru. Þessar tölur breytast í samræmi við væntanlega framboðs- og eftirspurnaratburði og samkvæmt birgðum sem byggja á tiltækum íhlutum sem hægt er að setja saman eða útvega.<br>Hægt er að nota þessa skýrslu til að athuga hvort hægt sé að anna sölupöntun fyrir vöru á tiltekinni dagsetningu með því að skoða núverandi framboð ásamt mögulegu magni sem íhlutir hennar geta annað ef samsetningarpöntun yrði ræst. Skýrslan sýnir hvenær og hversu margar einingar af samsetningu og framleiðsluvöru er hægt að gera samkvæmt framboði íhluta og gildandi ráðstöfunarmagni vörunnar. Þetta birtist sem heildarmagn.<br>Upplýsingarnar koma fram í myndriti þar sem hver ráðstöfunartala er lína sem liggur eftir tímalínunni og færist upp og niður eftir því sem magn breytist. Magntölurnar koma úr sama kerfi sem veitir upplýsingum til gluggans **Vara til ráðstöfunar eftir uppskriftarstigi**. |
|**Dreifing á kostnaðarhlutdeild uppskriftar**|5872|Sýnir myndrænt hvernig kostnaður samsettrar eða framleiddrar vöru er dreift samkvæmt uppskrift.<br>Slíkar upplýsingar geta verið gagnlegar við að ákveða, til dæmis hvort eigi að skipta um íhlutabirgja, leysa af hólmi innri afköst með útvistuðu vinnuafli eða öfugt, eða þegar uppskrift vöru er endurskoðuð eða henni breytt.<br>Fyrsta línuritið í skýrslunni sýnir heildarkostnaðarverð íhluta yfirvörunnar og vinnuafl brotið niður í allt fimm mismunandi kostnaðarhlutdeildir, og birt myndrænt með mismunandi litum.<br>Kökuritið með yfirskriftinni *Eftir vinnu/efni* sýnir hlutfallslega dreifingu milli kostnaðar við efni og vinnu yfirvörunnar, sem og eigin sameiginlegs framleiðslukostnaðar. Hlutdeild efniskostnaðar felur í sér efniskostnað vörunnar. Kostnaðarhlutdeild vinnuafls felur í sér afkastagetu, kostnaðarhlutdeild afkastagetu og kostnað undirverktaka. Kostnaðarhlutdeild er birt með mismunandi hætti eftir því hvaða svæði er valið í **Sýna aðeins** reitnum.<br>Skífuritið með yfirskriftinni *Eftir beint/óbeint* sýnir hlutfallslega dreifingu á milli beins og óbeins kostnaðar yfirvörunnar. Í beinu kostnaðarhlutdeildinni felst efniskostnaður vöru, afkastageta og undirverktakakostnaður. Óbeina kostnaðarhlutfallið felur í sér fastan afkastakostnað og fastan framleiðslukostnað.<br>Taflan neðst í skýrslunni er höfð með þegar gátreiturinn Hafa upplýsingar með er valinn. Hún sýnir valin gildi úr glugganum Kostnaðarhlutdeild uppskriftar eftir einu stigi eða lögð saman, eftir valkostinum sem var valinn í reitnum Sýna kostnaðarhlutdeild sem.|
|**Hvar-notað, listi**|809|Birtir lista yfir uppskriftir sem vörurnar sem voru valdar tilheyra. Gagnlegt yfirlit ef breyta þarf íhlut í uppskrift sem er sett í samsetningaríhlut. Til dæmis ef lánardrottinn getur ekki lengur afhent tiltekinn hlut sem þú notaðir fyrir samsetninguna/framleiðsluna. Í slíkum tilvikum veitir þessi skýrsla auðvelda yfirsýn yfir hvaða uppskrift íhluturinn tilheyrir. Hægt er að setja afmörkun á fjölda íhlutanna.|
|**Uppskrift - Hráefni**|810|Í þessari skýrslu er hægt að fá yfirlit yfir nauðsynlega íhluti, bæði fyrir samsetningu og framleiðslu. Þú sérð birgðir, grunnmælieiningu, aðallánardrottinn ef lánardrottnanúmerið er skrifað á vörukortið sjálft og útreikninginn á afhendingartíma.|
|**Uppskrift - Millivörur**|811|Ef þú framleiðir og/eða setur saman undirsamsetningar skaltu nota þessa skýrslu til að fá yfirlit yfir þessa tegund íhluta. Í þessari skýrslu má sjá grunnmælieiningar, birgðir, einingarkostnað og annað vörunúmer. |
|**Samsetningaruppskrift - Endanlegar vörur**|812|Í þessari skýrslu er birtur listi yfir vörur eða uppskriftir sem ekki eru íhlutir í uppskriftum. **Athugið**: Þessi skýrsla er ekki eingöngu takmörkuð við uppskrift. Mundu því að setja síu í reitinn **Samsetningaruppskrift** eða reitina **Áfyllingarkerfi**|
|**Samsetning til pöntunar - Sala**|915|Sýnir lykiltölur fyrir samsetningaríhluti sem hægt er að selja bæði sem hluta af samsetningu í setja saman-í-pöntun sölu og sem aðskilda vöru beint úr birgðum.<br>Notið þessa skýrslu til að greina magn, kostnaðar-, sölu- og framlegðartölur samsetningaríhluta til að styðja ákvarðanir, t. d. hvort að verðleggja eigi sett öðruvísi eða hætta eða byrja eigi að nota tiltekna vöru í samsetningum.<br>Línan **Í samsetningu** sýnir sölutölur fyrir heildarmagnið sem er selt sem hluti af samsetningarvöru. Tilteknar samsetningaríhlutasölur sem lagðar eru saman í þessa samtölu eru sýndar ef reiturinn **Sýna upplýsingar um samsetningu** er valinn.<br>Áherslan er á samsetningaríhluti en tölurnar eru reiknaðar út frá hagnaðarhlutfalli yfirvöru, samsetningarvörunnar. Til samræmis er söluupphæð hvers íhlutar reiknuð út frá eigin kostnaði og framlegð yfirvörunnar með eftirfarandi formúlu.<br>Skýrslan sýnir upplýsingar fyrir vörur sem uppfylla eitt eða bæði af eftirfarandi skilyrðum:<br>- Til í samsetningaruppskrift af vöru sem notar samsetningarregluna Samsetning til pöntunar.<br>- Hefur verið seld sem hluti af samsetningarpöntun.|

## <a name="tasks"></a>Verk

Eftirfarandi greinar lýsa sumum lykilverkum til að greina stöðu fyrirtækisins:

* [Skoða tiltækileika vöru](inventory-how-availability-overview.md)

## <a name="see-also"></a>Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með uppskriftir](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
