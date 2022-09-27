---
title: Aðfangakeðja
description: Undirbúa ítarlega og framkvæmanlega áætlun og loka-samsetningar framleiðslutímasetningu fyrir sölu og framleiðslueftirspurn.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.for: 291, 292, 293, 295, 517, 9010, 9038
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5fd4e6b1cf7e5f77c1273a58223f0c0b55db1ab0
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534832"
---
# <a name="planning"></a>Áætlun

Gera verður áætlun um framleiðsluaðgerðirnar sem þarf til að breyta ílagi í tilbúna vöru, daglega eða vikulega, eftir magni og eðli vörunnar. Í [!INCLUDE[prod_short](includes/prod_short.md)] er að finna aðgerðir til að anna áætlaðri og raunverulegri eftirspurn frá sölu og framleiðslu, auk aðgerða fyrir dreifingaráætlun með því að nota birgðahaldseiningar og birgðaflutninga.

> [!NOTE]
> Þetta efnisatriði lýsir fyrst og fremst áætlunum fyrir fyrirtæki sem eru í framleiðslu eða samsetningarstjórnun þar sem birgðapantanir geta verið framleiðsla, samsetning, flutningur eða innkaupapantanir. Aðalviðmótið fyrir þessa áætlunarvinnu er síðan **Áætlunarvinnublað**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] styður einnig framboðsáætlanir fyrir heildsölufyrirtæki þar sem framboðspantanir geta aðeins verið flutnings- eða innkaupapantanir. Aðalviðmótið fyrir þessa áætlunarvinnu er síðan **Innkaupatillaga**, sem er lýst óbeint í þessu efnisatriði þar sem flestar áætlunaraðgerðir má framkvæma í báðum vinnublöðum.

Líta má á áætlun sem undirbúning á nauðsynlegum birgðapöntunum í innkaupa-, samsetningar- eða framleiðsludeildunum til að uppfylla sölur eða eftirspurn á tilbúinni vöru. Nánari upplýsingar er að finna í [Innkaup](purchasing-manage-purchasing.md), [Stjórnun samsetningar](assembly-assemble-items.md) og [Framleiðsla](production-manage-manufacturing.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Fræðast snögglega um hvernig nota má áætlanakerfið til að finna og forgangsraða eftirspurn og leggja til framboðsáætlun með réttum hlutföllum.|[Um áætlunaraðgerðir](production-about-planning-functionality.md)|
|Lesið um hvernig áætlanakerfið virkar og hvernig á að leiðrétta reiknireglurnar til að uppfylla áætlunarþarfir í mismunandi umhverfi.|[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)|
|Fræðast um hvernig áætlanagrunnurinn greinir milli eftirspurnar í birgðageymslum samkvæmt uppsetningu birgðahaldseiningaspjalds og eftirspurnar án birgðageymslukóta.|[Áætlanagerð með eða án birgðageymslna](production-planning-with-without-locations.md)|
|Spá fyrir um eftirspurn sem kemur fram í væntanlegri sölu og framleiðsluhlutum.|[Búa til eftirspurnarspá](production-how-to-create-a-forecast.md)|  
|Stofna sérstakar eða verktengdar framleiðslupantanir sjálfkrafa úr sölupöntun til að anna nákvæmlega eftirspurn þeirrar sölupöntun.|[Búa til framleiðslupantanir úr sölupöntunum](production-how-to-create-production-orders-from-sales-orders.md)|
|Nota síðuna **Pantanaáætlun** fyrir handvirka áætlun sölu eða framleiðslueftirspurnar eina framleiðsluuppskrift í einu.|[Gera áætlanir um nýja eftirspurn pöntun fyrir pöntun](production-how-to-plan-for-new-demand.md)|
|Nota síðuna **Áætlunarvinnublað** til að keyra bæði MPS og MRP valmöguleika til að sjálfvirkt stofna framboðsáætlun, á háu stigi eða ítarlega, á öllum vörustigum.|[Keyra fulla áætlunargerð, MPS eða MRP](production-how-to-run-mps-and-mrp.md)|
|Notið síðuna **Innkaupatillögublað** til að búa sjálfkrafa til nákvæma framboðsáætlun til að anna eftirspurn eftir vörum sem aðeins er hægt að útvega með innkaupum eða millifærslu.|[Innkaupatillögublað](production-about-planning-functionality.md#requisition-worksheet)|  
|Ræsa eða uppfæra framleiðslupöntun sem gróflega áætlaðar aðgerðir í aðalframleiðsluáætluninni.|[Enduráætla eða uppfæra framleiðslupantanir beint](production-how-to-replan-refresh-production-orders.md)|
|Endurreikna dagatöl fyrir vinnu- eða vélastöðvar vegna breytinga á áætlun.|[Dagatal vinnustöðvar reiknað út](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Rekja pöntunareftirspurn (rakið magn), spá, standandi sölupöntun eða áætlunarfæribreytu (órakið magn) sem á við umrædda áætlunarlínu.|[Rekja tengsl milli eftirspurnar og framboðs](production-how-track-demand-supply.md)|
|Skoða áætlaða birgðastöðu vöru frá mismunandi sjónarhornum til að sjá hvaða brúttóþörf, reiknuð afhending og fleira hefur áhrif á hana eftir því sem tíminn líður.|[Skoða tiltækileika vöru](inventory-how-availability-overview.md)|  
<|Framkvæma valdar áætlunaraðgerðir, eins og að breyta eða bæta við áætlunarvinnublaðslínum, í myndrænu yfirliti yfir framboðsáætlun.|[Breyta áætlunartillögum í myndrænu yfirliti](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|-->

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/plan-items-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
