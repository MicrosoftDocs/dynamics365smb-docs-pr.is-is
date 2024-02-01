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

# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Úrræðaleita aðgang með Microsoft 365 leyfum

## <a name="this-page-uses-data-from-related-tables-that-you-do-not-have-access-to-error-message"></a>"Þessi síða notar gögn úr tengdum töflum sem hafa ekki aðgang að" villuboðum

### <a name="symptoms"></a>Einkenni

Þegar verið er að fá færslu í teymum birtast villuboð í flipa eða upplýsingum um kort sem svipar til:

"Þessi síða notar gögn úr tengdum töflum sem þú hefur ekki aðgang að. Til að vinna með alla eiginleika þessarar síðu skal hafa samband við stjórnanda.“

### <a name="cause"></a>Stofnar

Líklega vantar Hlutaheimildir fyrir töflur sem þessi síða á að tengjast eða skrá tengla á.

## <a name="microsoft-365-access-has-been-enabled-but-users-get-a-permission-error"></a>Microsoft 365 aðgangur hefur verið virkjaður en notendur fá heimildarvillu

### <a name="symptoms-1"></a>Einkenni

Aðgangur með  Microsoft 365  hefur verið virkjaður í Aðalmiðstöð fyrirtækja en notendur fá heimildarvillu þegar verið er að fá aðgang að einhverri færslu.

### <a name="cause-1"></a>Stofnar

Ef aðgangur er gerður í stjórnstöðinni aðalmiðstöð, en úthluta ekki heimildum á  **síðuna leyfistilrasíðan**, mun einhver sem reynir að fá aðgang að aðalfærslum í teymi. Öryggi er hannað inn í Business Central: stjórnendur verða fyrst að grunnstilla hvaða gögn er hægt að nálgast í Teams. 

### <a name="resolution"></a>Upplausn

Sérstilling heimilda á grunnstillingarsíðu leyfis mun aðeins hafa áhrif á nýlega stofnaða notendur. Þú verður einnig að úthluta heimildum sem vantar til notenda sem hafa þegar verið stofnaðir í gegnum listasíðu notenda. 

## <a name="you-shared-a-link-in-teams-but-users-get-a-message-that-they-can-only-view-data"></a>Þú samnýttir tengil í teymum en notendur fá skilaboð um að þeir geti aðeins skoðað gögn

### <a name="symptoms-2"></a>Einkenni

Þegar þú deilir tengli í lið sem aðalnotandi viðskipta, aðrir fá villuna "þegar aðgangur að viðskiptamiðinu er með  Microsoft 365  leyfi er aðeins hægt að skoða gögn í  Microsoft Teams ".

### <a name="cause-2"></a>Stofnar

Þegar tengli Business Central er deilt í Teams-spjalli eða rásum mun tilfærsla í gegnum tengil alltaf fara úr Microsoft Teams þar sem gögnin verða ekki lengur aðgengileg einstaklingi sem er með Microsoft 365 leyfi.

### <a name="resolution-1"></a>Upplausn

Þegar síðum eða færslum er deilt skal annaðhvort hafa með forskoðun tengils sem spjald eða deila gögnum sem flipa í spjallinu eða rásinni.

## <a name="card-from-shared-link-is-minimal-and-doesnt-include-details-button"></a>Spjald frá samnýttum tengli er lágmarks og inniheldur ekki upplýsingar um hnappinn

### <a name="symptoms-3"></a>Einkenni

 Microsoft 365 Þegar leyfishafi hefur hluta af aðalleyfishafi í starfsemi sem hefur aðaltengigjald í teymum, stækkar það sjálfkrafa í spjald sem hefur engar gagnlegar upplýsingar og sýnir aðeins Viðskiptaseðla  **án upplýsingahnappi** .

### <a name="cause-3"></a>Stofnar

Notendur sem eru með  Microsoft 365  leyfi en engin fyrirtæki miðlægt leyfi mega ekki samnýta tengla sem spjöld. Ef notandinn er með Business Central App fyrir hópa uppsetta og límum tengil inn á tónsvæðið þá birtist aðeins lágmarks kort. 

## <a name="see-also"></a>Sjá einnig .

[Aðgangur að Business Central með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-setup.md)  
[Business Central og Microsoft Teams samþætting](across-teams-overview.md)
[Deila Business Central-gögnum og síðutenglum í Microsoft Teams](across-working-with-teams.md)  
[Úrræðaleit fyrir Teams-samþættingu](admin-teams-troubleshooting.md)  
