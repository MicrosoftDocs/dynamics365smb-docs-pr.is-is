---
title: Úrræðaleita aðgang með Microsoft 365 leyfum
description: Kynntu þér hvernig þú getur lagað vandamál með því að opna Business Central með aðeins Microsoft 365 leyfi.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.service: dynamics-365-business-central
---

# Úrræðaleita aðgang með Microsoft 365 leyfum

## "Þessi síða notar gögn úr tengdum töflum sem þú hefur ekki aðgang að" villuboðum

### Einkenni

Þegar farið er í færslu í Teymi birtast villuboð í flipa- eða kortaupplýsingum, svipað og:

"Þessi síða notar gögn úr tengdum töflum sem þú hefur ekki aðgang að. Til að vinna með alla eiginleika þessarar síðu skal hafa samband við stjórnanda.“

### Stofnar

Líklegast vantar heimildir hluta fyrir töflur sem núgildandi síða eða skrá tengla á.

## Microsoft 365 aðgangur hefur verið virkjaður en notendur fá heimildarvillu

### Einkenni

Aðgangur með Microsoft 365 hefur verið virkjaður í Stjórnunarmiðstöð Business Central en notendur fá heimildavillu þegar þeir fá aðgang að einhverri færslu.

### Stofnar

Ef þú virkjar aðgang í stjórnunarmiðstöð Business Central, en úthlutar ekki heimildum á síðunni **Leyfisskilgreining**, verður einhver sem reynir að fá aðgang að Business Central færslum í Teymum með heimild fyrir notandafærslu sinni án heimildar fyrir hlutum. Öryggi er hannað inn í Business Central: stjórnendur verða fyrst að grunnstilla hvaða gögn er hægt að nálgast í Teams. 

### Upplausn

Sérstilling heimilda á grunnstillingarsíðu leyfis mun aðeins hafa áhrif á nýlega stofnaða notendur. Þú verður einnig að úthluta heimildum sem vantar til notenda sem hafa þegar verið stofnaðir í gegnum listasíðu notenda. 

## Tengli var samnýtt í Teymi en notendur fá skilaboð um að þeir geti aðeins skoðað gögn

### Einkenni

Þegar þú deilir tengli í Teams sem Business Central notandi fá aðrir villuna "Þegar þú opnar Business Central með Microsoft 365 leyfi getur þú aðeins skoðað gögn í Microsoft Teams".

### Stofnar

Þegar tengli Business Central er deilt í Teams-spjalli eða rásum mun tilfærsla í gegnum tengil alltaf fara úr Microsoft Teams þar sem gögnin verða ekki lengur aðgengileg einstaklingi sem er með Microsoft 365 leyfi.

### Upplausn

Þegar síðum eða færslum er deilt skal annaðhvort hafa með forskoðun tengils sem spjald eða deila gögnum sem flipa í spjallinu eða rásinni.

## Kort úr samnýttum tengli er í lágmarki og inniheldur ekki hnappinn Upplýsingar

### Einkenni 

 Microsoft 365 Þegar leyfishafi án Business Central leyfis deilir Business Central tengli í Teams stækkar það sjálfkrafa í kort sem hefur engar gagnlegar upplýsingar og sýnir Aðeins Business Central án **upplýsingahnapps** .

### Stofnar

Notendur sem hafa Microsoft 365 leyfi en ekkert Business Central leyfi hafa ekki heimild til að deila tenglum sem kortum. Ef notandinn hefur Business Central forritið fyrir teymi uppsett og límir tengil inn í tónsmíðasvæðið þá birtist aðeins lágmarkskort. 

## Sjá einnig .

[Aðgangur að Business Central með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365-leyfum](admin-access-with-m365-license-setup.md)  
[Business Central og Microsoft Teams samþætting](across-teams-overview.md)
[Deila Business Central-gögnum og síðutenglum í Microsoft Teams](across-working-with-teams.md)  
[Úrræðaleit fyrir Teams-samþættingu](admin-teams-troubleshooting.md)  