---
title: Villuskilaboðin „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga“
description: Leystu úr villunni á bak við skilaboðin „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga“ þegar runuvinnslan Leiðrétta kostnað - Birgðafærslur er keyrð.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/17/2021
ms.author: edupont
ms.openlocfilehash: 68d0fc68b799306fafa4e4fc0fb5f6cb146faca9
ms.sourcegitcommit: 772af6954539c65743d1a2f59e8a37d30bd30278
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2021
ms.locfileid: "7557299"
---
# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Villuskilaboð: „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga ...“

Þegar runuvinnslan **Leiðrétta kostnað - Birgðafærslur** er notuð gætu eftirfarandi villuboð komið upp:

**Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga.**

Þessi villuboð gefa til kynna að notandinn megi ekki bóka færslur fyrir umrædda dagsetningu og hægt er að bæta úr því með því að breyta uppsetningu notandans.

## <a name="change-the-user-setup"></a>Breyta uppsetningu notanda  

|Notandakenni  |Bókun leyfð frá  | Bókun leyfð til  |
|---------|---------|--------|
|Í EVRÓPU  |  2020-09-11      |2020-09-30      |

Notandinn í þessu tilfelli hefur leyfilegt dagsetningabil bókunar frá 11. september til 30. september og er því ekki heimilt að bóka leiðréttingarvirðisfærsluna með bókunardagsetninguna 10. september.  

### <a name="overview-of-involved-posting-date-setup"></a>Yfirlit yfir virka uppsetningu bókunardagsetningar

#### <a name="inventory-periods"></a>Birgðatímabil

|Lokadagsetning  |Name  |Lokað  |
|---------|---------|---------|
|2020-01-31     |2020. janúar      |  Já    |
|2020-02-28     |2020. febrúar     |  Já    |
|2020-03-31     |Mars 2020        |  Já    |
|2020-04-30     |Apríl 2020        |  Já    |
|2020-05-31     |Maí 2020        |  Já    |
|2020-06-30     |Júní 2020       |  Já    |
|2020-07-31     |Júlí 2020        |   Já   |
|2020-08-31     |Ágúst 2020     |   Já   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Október 2020    |         |
|2020-11-30     |Nóvember 2020   |         |
|2020-12-31     |Desember 2020   |         |  

#### <a name="general-ledger-setup"></a>Uppsetning fjárhags

|Svæði|Gildi:|
|---------|---------|
|Bókun leyfð frá:  |  2020-09-10      |
|Bókun leyfð til:    |  2020-09-30      |
|Skrá tíma:       |         |
|Snið staðbundins aðseturs:|   Póstnúmer      |  

#### <a name="user-setup"></a>Notandaupplýsingar

|Notandakenni  |Bókun leyfð frá  | Bókun leyfð til  |
|---------|---------|--------|
|NOTANDANAFN |  2020-09-10      |2020-09-30      |

Með því að úthluta víðara leyfilegu dagsetningabili bókunar, eins og í birgðahaldstíma eða fjárhagsuppsetningu, verður hægt að koma í veg fyrir árekstra sem valda því að villuboðin koma upp. Færsla leiðréttingargildis með bókunardagsetningu 10. september verður bókuð með þessari uppsetningu.
  
## <a name="see-also"></a>Sjá einnig  

[Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslum](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
