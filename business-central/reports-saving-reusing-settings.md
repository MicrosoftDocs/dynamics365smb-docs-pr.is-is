---
title: Jafna og leiðrétta vistaðar stillingar í skýrslum | Microsoft Docs
description: Lýsir því hvernig not skal fyrirfram skilgreinda valmöguleika og afmarkanir til að sérstilla skýrslu, og ná fram réttum upplýsingum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d61e599b9e86f28de6edcf4ccff5b245503880fe
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784610"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur
Þegar skýrslur eru keyrðar er notendum yfirleitt sýnd síða sem gerir þeim kleift að velja valkosti og síur fyrir breytingar á gögnum sem eru í mynduðu skýrslunni. Þessi síða er kölluð beiðnisíða. Skýrsla getur innihaldið eitt eða fleiri *vistaðar stillingar* sem notendur geta notað á skýrsluna úr beiðnisíðunni. *Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir. Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn. Frekari upplýsingar eru í [Nota vistaðar stillingar](ui-work-report.md#SavedSettings).

> [!NOTE]
> Þetta efnisatriði á að mestu leyti við um „skýrslu“, en svipaðar upplýsingar eiga við um runuvinnslur.

Ef réttar heimildir eru til staðar er hægt að skoða, stofna og breyta vistuðum stillingum fyrir allar skýrslur fyrir alla notendur í fyrirtækinu. Hægt er að úthluta vistuðum stillingum fyrir skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Til að stofna og breyta vistuðum stillingum fyrir alla notendur
Þú hefur umsjón með vistuðum stillingum á síðunni **Stillingar skýrsla**. Tvær aðferðir til að opna þessa síða:
-   Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skýrslustillingar** og veldu síðan tengda tengilinn.
-   Opnaðu skýrslu, veldu uppflettingu í **Nota sjálfgildi úr** -svæði og veldu svo aðgerðina **Velja af öllum listanum**.

Síðan birtir allar fyrirliggjandi vistaðar stillingafærslur fyrir alla notendur. Ef notandanafn er í **Úthlutað til** reitnum getur aðeins sá notandi notað vistuðu stillingarnar fyrir tengda skýrslu. Ef gátmerki er í **Deila með öllum notendum** reitnum geta allir notendur notað vistuðu stillingarnar fyrir skýrslu.

Á síðunni **Skýrslustillingar** er hægt að:
-   Veljið aðgerðina **Nýtt** til að stofna nýja færslu fyrir vistaðar stillingar frá grunni.
-   Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Afrita** til að búa til afrit.
-   Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Breyta** til að breyta færslu fyrir vistaðar stillingar.

> [!Important]
> Íhugaðu nafnið sem þú gefur færslu fyrir vistaðar stillingar. Ef þú býrð til færslu fyrir vistaðar stillingar fyrir alla notendur og þú gefur henni sama heiti og fyrirliggjandi færslu fyrir vistaðar stillingar sem er úthlutað á tiltekinn notanda, mun sá notandi ekki geta notað færsluna fyrir vistaðar stillingar sem er úthlutað á alla.  Undir **Vistaðar stillingar** á beiðnisíðu skýrslunnar mun notandinn sjá tvær vistaðar stillingar með sama heiti. Notandaskilgreinda færslan fyrir vistaðar stillingar verður notuð, sama hvor valmöguleikinn er valinn.

> [!NOTE]
> Aðgerð vistaðra stillinga á skýrslu er aðeins í boði þegar [eiginleikarnir SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) á beiðnisíðunni skýrslunnar er stilltur á **Já**. **SaveValues** eiginleiki er sett í þróunarumhverfi.  

## <a name="see-also"></a>Sjá einnig
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
