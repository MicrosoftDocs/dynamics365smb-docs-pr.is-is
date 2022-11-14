---
title: Úrræðaleit vegna aðgangs með Microsoft 365 leyfi
description: Lærðu hvernig hægt er að leysa vandamál með aðgang að Microsoft 365 miðborg með leyfi eingöngu.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745103"
---
# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Úrræðaleit vegna aðgangs með Microsoft 365 leyfi

## <a name="symptoms"></a>Einkenni

Þegar verið er að fá færslu í teymum birtast villuboð í flipa eða upplýsingum um kort sem svipar til:

"Þessi síða notar gögn úr tengdum töflum sem þú hefur ekki aðgang að. Til að vinna með alla eiginleika þessarar síðu skal hafa samband við kerfisstjóra. "

## <a name="cause"></a>Stofnar

Líklega vantar Hlutaheimildir fyrir töflur sem þessi síða á að tengjast eða skrá tengla á.

## <a name="symptoms"></a>Einkenni

Aðgangur hefur verið virkjaður en notendur fá heimildarvillu þegar verið er að fá aðgang að einhverri færslu.

## <a name="cause"></a>Stofnar

Ef aðgangur er gerður í stjórnstöðinni aðalmiðstöð en úthluta ekki heimildum á síðuna Leyfistilrasíðan, verður einhver sem reynir að fá aðgang að aðalfærslum í teymi. Rekstur Aðalmiðstöðvar er öruggur með hönnun: stjórnendur verða fyrst að skilgreina hvaða gögn er hægt að nálgast í teymum. 

## <a name="resolution"></a>Upplausn

Heimildir í Skilgreiningarsíðu leyfis geta aðeins haft áhrif á nýstofnaða notendur. Einnig verður að úthluta þeim heimildum sem vantar fyrir notendur sem þegar hafa verið stofnaðir í gegnum listasíðuna notendur. 

## <a name="symptoms"></a>Einkenni

Þegar ég deili hlekknum í teymum, aðrir fá villuna "þegar aðgangur að Viðskiptamiðinu er með Microsoft 365 leyfi er einungis hægt að skoða gögn í Microsoft Teams ".

## <a name="cause"></a>Stofnar

Þegar samnýtt er Viðskiptamiðlæg tenging við teymum spjall eða rásir, vafra Microsoft Teams um tengil fer alltaf eftir því hvar gögnin verða ekki lengur aðgengileg fyrir einstakling sem hefur Microsoft 365 leyfi.

## <a name="resolution"></a>Upplausn

Þegar samnýtt er með síðum eða færslum er annað hvort að hafa tengilinn Forskoðun sem spjald eða deila gögnum sem flipa á spjallinu eða rás.

## <a name="see-also"></a>Sjá einnig .

[Aðgangur að miðborg með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-setup.md)  
[Miðlæg samnýting og Microsoft Teams sameining](across-teams-overview.md)
[fyrirtækja miðlæg færslur og síðutenglar í Microsoft Teams](across-working-with-teams.md)  
[Samþætting úrræðaleyteta](admin-teams-troubleshooting.md)  