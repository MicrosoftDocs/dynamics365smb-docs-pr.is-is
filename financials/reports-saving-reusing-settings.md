---
title: "Jafna og leiðrétta vistaðar stillingar í skýrslum | Microsoft Docs"
description: "Lýsir því hvernig not skal fyrirfram skilgreinda valmöguleika og afmarkanir til að sérstilla skýrslu, og ná fram réttum upplýsingum."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2783c3a80beed5de6b7f7a63ff6811648ef48df3
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="managing-saved-settings-on-reports"></a>Vinna með vistaðar stillingar á skýrslum
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

> [!NOTE]
> Aðgerð vistaðra stillinga á skýrslu er aðeins mikilvæg þegar eiginleikarnir SaveValues á beiðnisíðunni er stilltur á „Já“. SaveValues eiginleika eiginleika er sett í umhverfi þróun.  

> [!Important]
> Ef stofnað er vistað stillingaatriði fyrir alla notendur og það hefur sama heiti og fyrirliggjandi vistaðar stillingar fyrir tiltekinn notanda getur sá notandi ekki notað vistuðu stillingarnar sem er úthlutað til allra.  Í reitnum Vistaðar stillingar á beiðnisíðu skýrslunnar sér notandinn tvo valkosti fyrir vistaðar stillingar með sama heiti. Sama hvorn valkostinn hann velur verða vistuðu stillingarnar sem tilgreindar eru fyrir notandann notaðar.

## <a name="see-also"></a>Sjá einnig
[Unnið með Skýrslur](ui-work-report.md)  

