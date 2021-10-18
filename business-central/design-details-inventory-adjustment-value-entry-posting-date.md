---
title: Bókunardagsetning á virðisfærslum
description: Lærðu hvernig runuvinnslan Leiðréttur kostnaður - birgðafærslur ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/17/2021
ms.author: edupont
ms.openlocfilehash: 49b840f91ca4177e046b986acbeb38b0ce3d4abb
ms.sourcegitcommit: 772af6954539c65743d1a2f59e8a37d30bd30278
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2021
ms.locfileid: "7557216"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslu

Þessi grein veitir leiðbeiningar fyrir notendur birgðakostnaðarvirkni í [!INCLUDE[prod_short](includes/prod_short.md)] og þá sérstaklega hvernig runuvinnslan **Leiðréttur kostnaður - birgðafærslur** ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.

## <a name="how-posting-dates-are-assigned"></a>Hvernig bókunardagsetningum er úthlutað

Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** úthlutar bókunardagsetningu fyrir virðisfærsluna sem hún kemur til með að búa til í eftirfarandi skrefum:  

1. Upphaflega er bókunardagsetning færslunnar sem á að búa til sú sama og dagsetning færslunnar sem hún leiðréttir.  

2. Bókunardagsetningin er sannprófuð gagnvart birgðatímabili og/eða fjárhagsgrunni.  

3. Úthlutun bókunardagsetningu; Ef upphafleg bókunardagsetning er ekki innan leyfilegs dagsetningabils bókunar, þá mun runuvinnslan úthluta leyfilegri bókunardagsetningu frá annað hvort fjárhagsgrunni eða birgðatímabili. Ef bæði birgðatímabil og leyfileg bókunardagsetning í fjárhagsgrunni eru skilgreind, verður síðari dagsetning þessara tveggja úthlutað til leiðréttingarvirðisfærslu.  

Við skulum yfirfara þetta ferli betur með dæmi. Gerum ráð fyrir að við séum með birgðafærslu fyrir sölu. Þessi hlutur var sendur 5. september 2020 og reikningsfærður daginn eftir.  

#### <a name="item-ledger-entry"></a>Birgðafærsla

|Færslunr.  |Vörunr.  |Bókunardagsetning  |Tegund færslu  | Nr. fylgiskjals |Kóti birgðageymslu   |Magn  |Kostnaðarupphæð (raunverul.)  |Reikningsfært magn  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Sala       |102033     |  Blátt       | -1    |    -11     |-1     |    0     |

Hér fyrir neðan eru tengdar virðisfærslur:

- **Færslunr. 379** táknar sendinguna og ber sömu bókunardagsetningu og fjárhagsfærsla yfirvörunnar.  
- **Færslunr. 381** táknar reikninginn.  
- **Færslunr. 391** er leiðrétting á virði reikningsfærslu (færslunr. 381 hér að ofan).  

|Færslunr.  |Vörunr.  |Bókunardagsetning  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  |Birgðafærsla nr.  |Kóti birgðageymslu   |Magn birgðafærslu  |Reikningsfært magn  |Kostnaðarupphæð (raunverul.)  |Kostnaðarupphæð (væntanl.)  |LEIÐRÉTT  |Jafna færslu  |Upprunakóði  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Sala     | Beinn kostnaður   | 102033        |319     | Blátt        | -1       |0         |  0       |     -10   |Nr   |0    |Sölur          |
|381     |  A       |    2020-09-06     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |-1        |-10       |    10     | Nr  |0      |       Sölur   |
|391     |  A       |    2020-09-10     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |0         |-1        |    0     |Já   |    181   | BIRGLEIÐR   |

Til að úthluta bókunardagsetningu fyrir **Færslunr. 391** voru eftirfarandi skref gerð:

1. **Virðisfærsla leiðréttingar** sem á að búa til (**Færslunr. 391**) er úthlutað sömu **Bókunardagsetningu** og færslunni sem hún leiðréttir.

2. Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** ákvarðar hvort upphafleg bókunardagsetning fyrir leiðréttingarvirðisfærslu er innan leyfilegs dagsetningabils bókunar byggt á birgðatímabili og/eða fjárhagsgrunni.  

Við skulum endurskoða ofangreinda sölu með því að bæta við uppsetningu á leyfilegu dagsetningabili bókunar.  
  
#### <a name="inventory-periods"></a>Birgðatímabil

|Lokadagsetning  |Name  |Lokað  |
|---------|---------|---------|
|2020-01-31     |2020. janúar      |  Já    |
|2020-02-28     |2020. febrúar     |  Já    |
|2020-03-31     |Mars 2020        |  Já    |
|2020-04-30     |Apríl 2020        |  Já    |
|2020-05-31     |Maí 2020        |  Já    |
|2020-06-30     |Júní 2020       |  Já    |
|2020-07-31     |Júlí 2020        |  Já    |
|2020-08-31     |Ágúst 2020     |  Já    |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Október 2020    |         |
|2020-11-30     |Nóvember 2020   |         |
|2020-12-31     |Desember 2020   |         |

Fyrsta leyfilega bókunardagsetningin er fyrsti dagurinn á fyrsta opna tímabilinu, sem er 1. september 2020.  

#### <a name="general-ledger-setup"></a>Uppsetning fjárhags

|Svæði|Gildi:  |
|---------|---------|
|Bókun leyfð frá:  |  2020-09-10      |
|Bókun leyfð til:    |  2020-09-30      |
|Skrá tíma:       |         |
|Snið staðbundins aðseturs:|   Póstnúmer      |  

Fyrsta leyfilega bókunardagsetning er dagsetningin sem tilgreind er í reitnum **Leyfa bókanir frá**: 10. september 2020. Ef bæði birgðatímabil og leyfilegar bókunardagsetningar í **fjárhagsgrunni** eru skilgreind mun síðari dagsetning þessara tveggja skilgreina leyfilegt dagsetningabil bókunar.  

**Úthlutun á leyfilegri bókunardagsetningu**  

Upphaflega úthlutaða bókunardagsetningin var 6. september eins og sýnt er í skrefi 1. Í öðru skrefi ber runuvinnslan Leiðrétta kostnað - Birgðafærslur kennsl 10. september sem fyrstu leyfilegu bókunardagsetninguna og úthlutar þess vegna 10. september á leiðréttingarvirðisfærsluna (**Færsla nr. 391**) fyrir neðan.  


|Færslunr.  |Vörunr.  |Bókunardagsetning  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  |Birgðafærsla nr.  |Kóti birgðageymslu   |Magn birgðafærslu  |Reikningsfært magn  |Kostnaðarupphæð (raunverul.)  |Kostnaðarupphæð (væntanl.)  |LEIÐRÉTT  |Jafna færslu  |Upprunakóði  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Sala     | Beinn kostnaður   | 102033        |319     | Blátt        | -1       |0         |  0       |     -10   |Nr   |0    |Sölur          |
|381     |  A       |    2020-09-06     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |-1        |-10       |    10     | Nr  |0      |       Sölur   |
|391     |  A       |    **10-09-2020**     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |0         |-1        |    0     |Já   |    181   | BIRGLEIÐR   |

## <a name="common-problems-with-the-adjust-cost---item-entries-batch-job"></a>Algeng vandamál með runuvinnsluna „Leiðrétta kostnað - Birgðafærslur“

Tvær aðstæður eru fyrir hendi sem þjónustudeildin lendir nógu oft í til að skrifa eigin greinar um lausn á vandamálinu.

### <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Villuskilaboð: „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga ...“

Ef þú færð upp þessa villu þarftu að leiðrétta dagsetningarnar þar sem notandinn má bóka færslur. Frekari upplýsingar má finna í [Villuskilaboð: „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga“](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### <a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Bókunardagsetning á leiðréttingarvirðisfærslum á móti bókunardagsetningu við innfærslu sem veldur leiðréttingu, eins og endurmati eða kostnaðarauka

Frekari upplýsingar er að finna í [Bókunardagsetning fyrir virðisfærslu leiðréttingar í samanburði við upprunafærsluna](design-details-inventory-adjustment-value-entry-source-entry.md).

## <a name="see-also"></a>Sjá einnig  

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
