---
title: Aðgangstreymi notanda fyrir Microsoft 365 leyfi
description: Fá yfirlit yfir það sem gerist þegar notandi nálgast aðalgögn miðlægt með leyfi sínu Microsoft 365 í fyrsta sinn.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: d20384149854161588df50af9e8d92af78e16fa1
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745105"
---
# <a name="user-access-flow-for-microsoft-365-licenses"></a>Aðgangstreymi notanda fyrir Microsoft 365 leyfi

Í greininni er fjallað um það sem gerist þegar notandi hefur aðgang að miðlægum gögnum með leyfi sínu Microsoft 365 í fyrsta sinn. Skilningur á þessu flæði gerir stjórnendum kleift að áætla nálgun þeirra og skilgreina Viðskiptamiðmið til að stemma við þarfir fyrirtækja.

1. Í fyrsta lagi eru auðkenni notandans sannvottaður 
2. Viðskiptamiðlæg staðfestir að allar [lágmarkskröfur](admin-access-with-m365-license.md#minimum-requirements) séu uppfylltar.
3. Aðalleyfishafi staðfestir að þessi notandi hafi ekki hærra leyfi eins og Aðalleyfi fyrirtækja eða stjórnunarhlutverk eins og úthlutað hlutverk kerfisstjóra. 
4. Viðskiptamiðlæg staðfestir hvort notandinn sé að fá aðgang að gögnum sem tilheyra umhverfi sem hefur virkjað aðgang með Microsoft 365 leyfum. 
5. Notendaskrá er úthlutaður í Business Central, með því að úthluta notendaflokki, forstillingum og Heimildaveningum sem eru skilgreindar í Microsoft 365 síðunni leyfisstillingar. Sjálfgefið er að teymum notendaflokksins er úthlutað, Starfsmannaforstillingunni er úthlutað og aðeins innskráningarheimildinni er úthlutað. Öllum öðrum sjálfgildi notendastillingum er einnig beitt, eins og með leyfi Aðalnotanda Business. 
6. Aðalöryggislíkani fyrir Full viðskipti er beitt, til að ákvarða hvort notandinn eigi að geta komist í færsluna, síðan í tilgreindu fyrirtæki og í tilgreindu umhverfi. 

Ef öll skref heppnast getur notandinn nú skoðað þessi viðskipti miðlægt í teymum. Miðlæg þjónusta Business tryggir sjálfkrafa lesaðgang og einfaldar í HÍ. 

Notandareikninginn er nú skráður í Business Central og hægt er að stjórna honum eins og öllum notendum viðskipta.

> [!NOTE]
> Skref geta verið mismunandi eftir því hvaða viðbótaröryggissjónarmið sem tilgreind eru í Microsoft 365 eða Viðskiptamiðinu.

## <a name="see-also"></a>Sjá einnig .

[Aðgangur að miðborg með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-setup.md)  