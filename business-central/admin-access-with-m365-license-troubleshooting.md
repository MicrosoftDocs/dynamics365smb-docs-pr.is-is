---
title: Úrræðaleita aðgang með Microsoft 365 leyfum
description: Kynntu þér hvernig þú getur lagað vandamál með því að opna Business Central með aðeins Microsoft 365 leyfi.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: 750a78eb32568bea07d6851ff69c0b2cfea3ab49
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745103"
---
# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Úrræðaleita aðgang með Microsoft 365 leyfum

## <a name="symptoms"></a>Einkenni

Þegar færsla í Teams er opnuð færðu villuboð í flipa eða spjaldaupplýsingum sem svipar til:

„Þessi síða notar gögn úr tengdum töflum sem þú hefur ekki aðgang að. Til að vinna með alla eiginleika þessarar síðu skal hafa samband við stjórnanda.“

## <a name="cause"></a>Stofnar

Þig vantar líklega heimildir hluta fyrir töflur sem núverandi síða eða færsla tengist við.

## <a name="symptoms"></a>Einkenni

Aðgangur hefur verið virkjaður en notendur fá heimildarvillu þegar þeir opna einhverja færslu.

## <a name="cause"></a>Stofnar

Ef þú virkjar aðgang í stjórnendamiðstöð Business Central, en úthlutar ekki heimildum á stillingarsíðu leyfis munu allir sem reyna að opna færslur Business Central í Teams fá notandafærslu sína úhlutaða án heimildar fyrir neina hluti. Öryggi er hannað inn í Business Central: stjórnendur verða fyrst að grunnstilla hvaða gögn er hægt að nálgast í Teams. 

## <a name="resolution"></a>Upplausn

Sérstilling heimilda á grunnstillingarsíðu leyfis mun aðeins hafa áhrif á nýlega stofnaða notendur. Þú verður einnig að úthluta heimildum sem vantar til notenda sem hafa þegar verið stofnaðir í gegnum listasíðu notenda. 

## <a name="symptoms"></a>Einkenni

Þegar ég deili tengli í Teams fá aðrir villuna „Þegar Business Central er opnað með Microsoft 365 leyfi er einungis hægt að skoða gögn í Microsoft Teams“.

## <a name="cause"></a>Stofnar

Þegar tengli Business Central er deilt í Teams-spjalli eða rásum mun tilfærsla í gegnum tengil alltaf fara úr Microsoft Teams þar sem gögnin verða ekki lengur aðgengileg einstaklingi sem er með Microsoft 365 leyfi.

## <a name="resolution"></a>Upplausn

Þegar síðum eða færslum er deilt skal annaðhvort hafa með forskoðun tengils sem spjald eða deila gögnum sem flipa í spjallinu eða rásinni.

## <a name="see-also"></a>Sjá einnig .

[Aðgangur að Business Central með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-setup.md)  
[Business Central og Microsoft Teams samþætting](across-teams-overview.md)
[Deila Business Central-gögnum og síðutenglum í Microsoft Teams](across-working-with-teams.md)  
[Úrræðaleit fyrir Teams-samþættingu](admin-teams-troubleshooting.md)  