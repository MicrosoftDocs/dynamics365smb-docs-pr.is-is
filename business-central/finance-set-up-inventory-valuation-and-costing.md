---
title: Uppsetning birgðaverðmats og kostnaðar | Microsoft Docs
description: Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: edcaaaedde3bb42c0c0d69c3e71dd659f5475712
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750456"
---
# <a name="setting-up-inventory-valuation-and-costing"></a>Uppsetning birgðaverðmats og kostnaðar

Til að ganga úr skugga um að birgðakostnaður sé skráður rétt, er nauðsynlegt að setja upp ýmsa reiti og síður áður en þú byrjar að framkvæma vörufærslur. Yfirleitt velja fyrirtæki tiltekna aðferð við útreikning kostnaðar og nota hana birgðavörur, til dæmis til að fylgjast með virði á vörum og birgðum.  

> [!TIP]
> Til að sjá kynningu á kostnaðarútreikningi í [!INCLUDE [prod_short](includes/prod_short.md)] skal skoða [Um birgðakostnað](finance-learn-about-costing.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|
|Tilgreinið sjálfgefna aðferð kostnaðarútreiknings fyrir fyrirtækið til að stýra því hvernig upphaflegur kostnaður er notaður til að meta birgðavirði og kostnað seldra vara.|[Setja upp almennar birgðaupplýsingar](inventory-how-setup-general.md)|  
|Tilgreinið aðferð kostnaðarútreiknings á einstökum vörum ef hún krefst annars konar aðferðar við kostnaðarútreikning.|[Skrá nýjar vörur](inventory-how-register-new-items.md)|  
|Tryggja að kostnaður sé sjálfkrafa bókaður á fjárhag hvenær sem birgðafærsla er bókuð.|Reiturinn **Sjálfvirk kostnaðarbókun** á síðunni **Uppsetning birgða**|  
|Tryggja að áætlaður kostnaður sé bókaður á fjárhag til að geta séð af bráðabirgðafjárhagsreikningum áætlaðar upphæðir sem eru fallnar í gjalddaga og kostnað seldra vara áður en þær eru reikningsfærðar í raun.|Reiturinn **Áætluð kostnaðarbókun í fjárhag** á síðunni **Uppsetning birgða**|  
|Setja kerfið þannig upp að leiðrétt sé sjálfvirkt vegna allra kostnaðarbreytinga í hvert sinn sem birgðafærslur eru bókaðar.|[Leiðr. kostnað vara](inventory-how-adjust-item-costs.md)|  
|Skilgreina hvort reikna skuli meðalkostnaður aðeins á hverja vöru eða á hverja vöru og hverja birgðahaldseiningu og afbrigði vörunnar.|Reiturinn **Útreikningsgerð meðalkostnaðar** á síðunni **Uppsetning birgða**|  
|Velja tímabilið sem forritið á að nota til að reikna út vegið meðalinnkaupsverð vara sem nota meðalverðsaðferðina.|Reiturinn **Meðalkostnaðartímabil** á síðunni **Uppsetning birgða**|  
|Skilgreina birgðatímabil til að stýra birgðavirði yfir tiltekinn tíma með því að banna bókun færslna á lokuð birgðatímabil.|[Vinna við birgðatímabil](finance-how-to-work-with-inventory-periods.md)|  
|Tryggja að söluvöruskilum sé jafnað á upphaflegu færsluna á útleið til að varðveita birgðavirð.|Reiturinn **Nákvæmar kostnaðarbakfærslur áskildar** á síðunni **Sala & útistandandi**|  
|Tryggja að innkaupaskil sé jafnað á upphaflegu færsluna á innleið til að varðveita birgðavirði.|Reiturinn **Nákvæmar kostnaðarbakfærslur áskildar** á síðunni **Innkaup & viðskiptaskuldir**|
|Setja upp sléttunarreglur sem á að nota þegar vöruverð er leiðrétt eða lagt til eða þegar staðlaður kostnaður er leiðréttur eða lagður til.|**Sléttunaraðferð** síða|  

## <a name="see-also"></a>Sjá einnig

[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Setja upp almennar birgðaupplýsingar](inventory-how-setup-general.md)  
[Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Uppsetning bestu venjur: Aðferð kostnaðarútreiknings](setup-best-practices-costing-method.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Breyta kostnaðarútreikningi fyrir vörur](design-details-changing-costing-methods.md)  
[Unnið með Business Central](ui-work-product.md)  
[Fjármál](finance.md)  
