---
title: "Jafna og leiðrétta vistaðar stillingar í skýrslum | Microsoft Docs"
description: "Lýsir því hvernig not skal fyrirfram skilgreinda valmöguleika og afmarkanir til að sérstilla skýrslu, og ná fram réttum upplýsingum."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="saved-settings-on-reports"></a>Vistuð Stillingar á Skýrslur
Í skýrslunni sem fer eftir að kann að birta með page sem gerir kleift að tilteknum valkosti og afmarkanir fyrir breytingar gögnin sem er tekið með í skýrslunni generated. Þessa síðu er heitir síðuna beiðni skýrslu. Með skýrslunni getur innihaldið eitt eða fleiri *vistuð stillingar* sem hægt er að jafna við skýrsluna úr síðuna beiðni. *Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir. Með því að nota vistaðar stillingar er er fljótleg og reliable leið til að haldbærar búa til skýrslur sem eru rétt gögn.

Hægt er að skoða vistuð stillingar sem völ er á með í skýrslunni í **Vistuð Stillingar** hluta af síðu skýrslunnar beiðni.  

## <a name="to-apply-saved-settings-to-a-report"></a>Jafna vistuð stillingar í skýrslu
1. Viðeigandi skýrsla er opnuð.

   Skýrslunni beiðni page birtist.    
2. Í sem **Vistuð Stillingar** hluta af síðu, setja á **Heiti** á vistuðu stillingar sem á að nota.

   Hlutinn **Vistaðar stillingar** birtist eingöngu ef skýrslan hefur verið keyrð áður eða ef fyrir eru vistaðar stillingafærslur. Vistaða stillingafærslan sem kallast **Síðast notaðir valkostir og afmarkanir** er alltaf tiltæk. Þessar stillingar eru kostur og afmörkun gildin sem voru notaðar í síðasta sinn sem keyrslan er í skýrslunni.

## <a name="administer-saved-report-settings-for-users"></a>Séð um vistuðu skýrslu stillingar fyrir notendur
Ef rétta heimildir, hægt er að skoða, stofna og breyta vistuð stillingar fyrir allar skýrslur fyrir alla notendur í fyrirtækinu. Hægt er að úthluta vistuð stillingar skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.

Stjórna er vistuð stillingar úr page 1506 **Skýrslum Stillingar**. Til að opna þessa síðu, skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Skýrslustillingar** og velja svo viðeigandi tengil.

Úr á **Skýrslu Stillingar** er hægt að búa til nýja stillingar í scratch eða er hægt að afrita og breyta þeim stillingar. Til að breyta valkostum og síum fyrir stillingar skal velja aðgerðina **Breyta**.

**Athugasemdir:**

* Aðgerð vistaðra stillinga á skýrslu er aðeins mikilvæg þegar eiginleikarnir SaveValues á beiðnisíðunni er stilltur á „Já“. SaveValues eiginleika eiginleika er sett í umhverfi þróun.
* Ef stofnað er vistað stillingaatriði fyrir alla notendur og það hefur sama heiti og fyrirliggjandi vistaðar stillingar fyrir tiltekinn notanda getur sá notandi ekki notað vistuðu stillingarnar sem er úthlutað til allra.  Í reitnum Vistaðar stillingar á beiðnisíðu skýrslunnar sér notandinn tvo valkosti fyrir vistaðar stillingar með sama heiti. Sama hvorn valkostinn hann velur verða vistuðu stillingarnar sem tilgreindar eru fyrir notandann notaðar.

## <a name="see-also"></a>Sjá einnig
[Tímasetja keyrslu skýrslu](ui-schedule-report.md)  

