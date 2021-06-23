---
title: Framleiðsluskýrslur og greiningar
description: Finndu út hvaða framleiðsluskýrslur og greiningar eru í boði í staðlaðri útgáfu Business Central til að halda utan um reksturinn.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216368"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Framleiðsluskýrslur og greiningar í Business Central

Framleiðsluskýrslugerð í [!INCLUDE [prod_short](includes/prod_short.md)] gerir starfsmönnum í framleiðslu og rekstri kleift að fá innsýn í og tölfræði um núverandi og fyrri framleiðsluaðgerðir.  

## <a name="reports"></a>Skýrslur

Eftirfarandi tafla lýsir sumum helstu skýrslunum í framleiðslu.

|Skýrsla |Kenni hlutar|Description  |
|---------|---------|---------|
|**Sundurliðað magn í uppskrift**|99000753|Í skýrslunni er prentaður inndreginn listi yfir vöruna eða vörurnar sem tilgreindar eru í afmörkununum. Framleiðsluuppskriftin er algerlega opnuð á öllum stigum.|
|**Vara – Hægt að ná (tími)**|5871|Sýnir hvernig fimm mismunandi lykilráðstöfunartölur breytast með tímanum fyrir uppskriftarvöru. Þessar tölur breytast í samræmi við væntanlega framboðs- og eftirspurnaratburði og samkvæmt birgðum sem byggja á tiltækum íhlutum sem hægt er að setja saman eða útvega.<br>Hægt er að nota þessa skýrslu til að athuga hvort hægt sé að anna sölupöntun fyrir vöru á tiltekinni dagsetningu með því að skoða núverandi framboð ásamt mögulegu magni sem íhlutir hennar geta annað ef samsetningarpöntun hefur verið. Skýrslan sýnir hvenær og hversu margar einingar af samsetningu og framleiðsluvöru er hægt að gera samkvæmt framboði íhluta og gildandi ráðstöfunarmagni vörunnar. Þetta birtist sem heildarmagn.<br>Upplýsingarnar koma fram í myndriti þar sem hver ráðstöfunartala er lína sem liggur eftir tímalínunni og færist upp og niður eftir því sem magn breytist. Magntölurnar koma úr sama kerfi sem veitir upplýsingum til gluggans **Vara til ráðstöfunar eftir uppskriftarstigi**. |
|**Dreifing á kostnaðarhlutdeild uppskriftar**|5872|Sýnir myndrænt hvernig kostnaður samsettrar eða framleiddrar vöru er dreift samkvæmt uppskrift.<br>Slíkar upplýsingar geta verið gagnlegar við að ákveða, til dæmis hvort eigi að skipta um íhlutabirgja, leysa af hólmi innri afköst með útvistuðu vinnuafli eða öfugt, eða þegar uppskrift vöru er endurskoðuð eða henni breytt.<br>Fyrsta línuritið í skýrslunni sýnir heildarkostnaðarverð íhluta yfirvörunnar og vinnuafl brotið niður í allt fimm mismunandi kostnaðarhlutdeildir, og birt myndrænt með mismunandi litum.<br>Kökuritið með yfirskriftinni *Eftir vinnu/efni* sýnir hlutfallslega dreifingu milli kostnaðar við efni og vinnu yfirvörunnar, sem og eigin sameiginlegs framleiðslukostnaðar. Hlutdeild efniskostnaðar felur í sér efniskostnað vörunnar. Kostnaðarhlutdeild vinnuafls felur í sér afkastagetu, kostnaðarhlutdeild afkastagetu og kostnað undirverktaka. Kostnaðarhlutdeild er birt með mismunandi hætti eftir því hvaða svæði er valið í **Sýna aðeins** reitnum.<br>Skífuritið með yfirskriftinni *Eftir beint/óbeint* sýnir hlutfallslega dreifingu á milli beins og óbeins kostnaðar yfirvörunnar. Í beinu kostnaðarhlutdeildinni felst efniskostnaður vöru, afkastageta og undirverktakakostnaður. Óbeina kostnaðarhlutfallið felur í sér fastan afkastakostnað og fastan framleiðslukostnað.<br>Taflan neðst í skýrslunni er höfð með þegar gátreiturinn **Hafa upplýsingar með** er valinn. Hún sýnir valin gildi úr glugganum Kostnaðarhlutdeild uppskriftar eftir einu stigi eða lögð saman, eftir því hvaða valkostur var valinn í reitnum **Sýna kostnaðarhlutdeild sem**.|
|**Sundurliðaður útreikningur**|99000756|Í þessari skýrslu verður til kostnaðarlisti á vöru þar sem tekið er tilliti til úrkasts.|
|**Þar sem notað (efsta stig)**|99000757|Sýnir hvar og í hvaða magni vörurnar eru notaðar í samsetningu framleiðslunnar.<br>Skýrslan sýnir aðeins notkunarstað vörunnar þegar grunnvaran er notuð sem efsta stigið. Ef t.d. vara „A“ er notuð til að framleiða vöru „B“ og vara „B“ er notuð til að framleiða vöru „C“ sýnir skýrslan vöru B ef hún er keyrð fyrir vöru A. Ef skýrslan er keyrð fyrir vöru B verður vara C birt sem notkunarstaður.<br>Einnig er hægt að opna síðuna **Notkunarstaðarlína** beint í kerfinu.|
|**Samanburðarlisti vöruuppskriftar**|99000758|Með skýrslunni fæst möguleiki á að bera saman svipaðar endanlegar vörur varðandi kostnað. Þá sérðu skráningu með öllum þáttum og kostnaði sem og nauðsynlegu magni. Útreikningardagsetningin er stillt á vinnudagsetninguna. |
|**Tölfræði framleiðslupantana**|99000791|Tilgreinir ýmsan uppsafnaðan kostnað valinnar framleiðslupöntunar.<br>Innihald skýrslunnar er mjög svipað síðunni **Upplýsingar um framl.pöntun**.<br>Fyrir framleiðslupantanir sem nota framleiðslustefnuna *Eftir pöntun* sýnir glugginn aðeins efnis- og afkastakostnað vara á efsta uppskriftarstigi.|
|**Verklisti afkastagetu**|99000780|Sýnir framleiðslupantanirnar sem bíða vinnslu á vinnustöðvum og vélastöðvum. Útprent eru gerð yfir afkastagetu vinnu- eða vélastöðvarinnar). Í skýrslunni eru birtar upplýsingar eins og upphafs- og lokatími, dagsetning fyrir hverja framleiðslupöntun og ílagsmagn.|
|**Álag á vinnustöð** eða **álag á vélastöð**|99000783 eða 99000784|Báðar skýrslur birta lista yfir álagið á vélastöð. Álagið á vinnu/vélastöð er samtalan af þeim fjölda stunda sem þarf vegna allra áætlaðra og raunverulegra pantana sem eru keyrðar í vinnustöðinni á tilteknu tímabili.|
|**Framl.pöntun Vöntunarlisti**|99000788|Skýrsluna má nota til að sjá alla íhluti sem ekki eru tiltækir vegna birgða sem vantar. Þannig er hægt að nota þetta yfirlit til að sjá tímanlega hvort tímalínan fyrir áætlaða eða útgefna framleiðslupöntun mun standast.|


## <a name="tasks"></a>Verk

Eftirfarandi greinar lýsa sumum lykilverkum til að greina stöðu fyrirtækisins:

* [Skoða álag á vinnu- og vélastöðvar](production-how-to-view-the-load-on-work-centers.md)  
* [Skoða tiltækileika vöru](inventory-how-availability-overview.md)

## <a name="see-also"></a>Sjá einnig .

[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
