---
title: Jafna og leiðrétta vistaðar stillingar í skýrslum | Microsoft Docs
description: Lýsir því hvernig not skal fyrirfram skilgreinda valmöguleika og afmarkanir til að sérstilla skýrslu, og ná fram réttum upplýsingum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 3e7b00d54a9c655a77b7b7f4854e59993866427e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251222"
---
# <a name="managing-saved-settings-on-reports"></a>Vinna með vistaðar stillingar á skýrslum
Þegar skýrslur eru keyrðar er notendum yfirleitt sýnd síða sem gerir þeim kleift að velja tiltekna valkosti og afmarkanir fyrir breytingar á gögnum sem eru í mynduðu skýrslunni. Þessi síða er kölluð beiðnisíða skýrslu. Skýrsla getur innihaldið eitt eða fleiri *vistaðar stillingar* sem notendur geta notað á skýrsluna úr beiðnisíðunni. *Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir. Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn. Nánari upplýsingar um það hvernig vistaðar stillingar eru notaðar eru í [Notkun vistaðra stillinga](ui-work-report.md#SavedSettings).

Ef rétta heimildir, hægt er að skoða, stofna og breyta vistuð stillingar fyrir allar skýrslur fyrir alla notendur í fyrirtækinu. Hægt er að úthluta vistuð stillingar skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.

<!--
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Stofna og breyta vistuðum stillingum fyrir alla notendur
Vistuðum stillingum er stjórna af síðu **1560 Stillingar skýrsla**. Tvær aðferðir til að opna þessa síða:
-   Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skýrslustillingar** og veldu síðan tengda tengilinn.
-   Opnaðu skýrslu, veldu uppflettinguna við hliðina á **Notuð sjálfgildi frá:** reitinn, veldu **Velja af öllum listanum**.

Síðan birtir allar fyrirliggjandi vistunarstillingafærslur fyrir alla notendur. Ef notandanafn er í **Úthlutað til** dálknum getur aðeins sá notandi notað vistuðu stillingarnar fyrir tengda skýrslu. Ef gátmerki er í **Deila með öllum notendum** dálknum geta allir notendur notað vistuðu stillingarnar fyrir skýrslu.

Á síðunni **Skýrslustillingar** er hægt að:
-   Veljið **Nýtt** til að stofna nýja færslu fyrir vistaðar stillingar frá grunni.
-   Veljið færslu fyrir vistaðar stillingar af listanum og veljið **Afrita** til að búa til afrit.
-   Veljið færslu fyrir vistaðar stillingar af listanum og veljið **Breyta** til að breyta færslu fyrir vistaðar stillingar.


> [!Important]
> Íhugaðu nafnið sem þú gefur færslu fyrir vistaðar stillingar. Ef þú býrð til færslu fyrir vistaðar stillingar fyrir alla notendur og þú gefur henni sama heiti og fyrirliggjandi færslu fyrir vistaðar stillingar sem er úthlutað á tiltekinn notanda, mun sá notandi ekki geta notað færsluna fyrir vistaðar stillingar sem er úthlutað á alla.  Undir **Vistaðar stillingar** á beiðnisíðu skýrslunnar mun notandinn sjá tvær vistaðar stillingar með sama heiti. Hins vegar, sama hvorn valmöguleikann hann velur, verður notandaskilgreinda færslan fyrir vistaðar stillingar notuð.

> [!NOTE]
> Aðgerð vistaðra stillinga á skýrslu er aðeins í boði þegar [eiginleikarnir SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) á beiðnisíðunni skýrslunnar er stilltur á `Yes`. **SaveValues** eiginleiki er sett í þróunarumhverfi.  

## <a name="see-also"></a>Sjá einnig
[Unnið með skýrslur og runuvinnslur](ui-work-report.md)  
