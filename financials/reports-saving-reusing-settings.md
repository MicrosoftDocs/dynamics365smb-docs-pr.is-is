---
title: "Vistuð Stillingar á Skýrslur"
description: "Lýsir hvernig á að nota vistunarstillingar á skýrslu."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 12/12/2016
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7afbd31e77a4f53ee99fbb192dd8a32a660f87eb
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


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

Stjórna er vistuð stillingar úr page 1506 **Skýrslum Stillingar**. Til að opna þessa síðu, efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Skýrslustillingar**, og velja síðan viðeigandi tengil.

Úr á **Skýrslu Stillingar** er hægt að búa til nýja stillingar í scratch eða er hægt að afrita og breyta þeim stillingar. Til að breyta valkostum og síum fyrir stillingar skal velja aðgerðina **Breyta**.

**Athugasemdir:**

* Aðgerð vistaðra stillinga á skýrslu er aðeins mikilvæg þegar eiginleikarnir SaveValues á beiðnisíðunni er stilltur á „Já“. SaveValues eiginleika eiginleika er sett í umhverfi þróun.
* Ef stofnað er vistað stillingaatriði fyrir alla notendur og það hefur sama heiti og fyrirliggjandi vistaðar stillingar fyrir tiltekinn notanda getur sá notandi ekki notað vistuðu stillingarnar sem er úthlutað til allra.  Í reitnum Vistaðar stillingar á beiðnisíðu skýrslunnar sér notandinn tvo valkosti fyrir vistaðar stillingar með sama heiti. Sama hvorn valkostinn hann velur verða vistuðu stillingarnar sem tilgreindar eru fyrir notandann notaðar.

## <a name="see-also"></a>Sjá einnig
[Tímasetja keyrslu skýrslu](ui-schedule-report.md)  

