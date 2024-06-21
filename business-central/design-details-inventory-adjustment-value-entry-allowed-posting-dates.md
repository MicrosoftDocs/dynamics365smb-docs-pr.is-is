---
title: Villuskilaboðin „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga“
description: Leystu úr villunni á bak við skilaboðin „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga“ þegar runuvinnslan Leiðrétta kostnað - Birgðafærslur er keyrð.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# Villuskilaboð: „Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga ...“

 **Þegar keyrslan** Leiðr. kostnað - Birgðafærslur er notuð er hægt að keyra eftirfarandi villuboð:

**Bókunardagsetning er ekki á leyfilegu bili bókunardagsetninga.**

Þessi skilaboð gefa til kynna að ekki sé heimilt að bóka færslur fyrir dagsetninguna sem færð var inn. Hægt er að komast utan um þetta mál með því að breyta notandauppsetningunni.

## Breyta uppsetningu notanda  

|Auðkenni notanda  |Bókun leyfð frá  | Bókun leyfð til  |
|---------|---------|--------|
|Í EVRÓPU  |  2020-09-11      |2020-09-30      |

Í þessu tilviki er heimilt að bóka á tímabilinu frá 11. september til 30. september. Hins vegar er ekki heimilt að bóka leiðréttingarvirðisfærsluna með 10. september bókunardagsetningu.  

### Yfirlit yfir uppsetningu bókunardagsetninga

#### Birgðatímabil

|Lokadagur  |Nafn  |Lokað  |
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

#### Uppsetning fjárhags

|Svæði|Gildi:|
|---------|---------|
|Bókun leyfð frá:  |  2020-09-10      |
|Bókun leyfð til:    |  2020-09-30      |
|Skrá tíma:       |         |
|Snið staðbundins aðseturs:|   Póstnúmer      |  

#### Notandaupplýsingar

|Notandakenni  |Bókun leyfð frá  | Bókun leyfð til  |
|---------|---------|--------|
|NOTANDANAFN |  2020-09-10      |2020-09-30      |

Með því að úthluta breiðari dagsetningasviði þar sem hægt er að bóka á síðurnar **Birgðatímabil** eða **Fjárhagsgrunnur** er hægt að koma í veg fyrir áreksturinn sem veldur villuboðunum. Til dæmis er hægt að bóka leiðréttingarvirðisfærsluna með 10. september bókunardagsetningu.
  
## Sjá einnig .  

[Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslum](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
