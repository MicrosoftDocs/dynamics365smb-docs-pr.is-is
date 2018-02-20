---
title: "Bestu venjur fyrir uppsetningu altækra áætlana | Microsoft Docs"
description: "Flýtiflipinn **Áætlun** í glugganum **Framleiðslugrunnur** inniheldur nokkra reiti sem skilgreina altækar reglur fyrir framboðsáætlun."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f1a4e3a30d4d665a83ab599ad19dfd3760d744b2
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="setup-best-practices-global-planning-setup"></a>Uppsetning bestu venjur: Uppsetning altækra áætlanna
Flýtiflipinn **Áætlun** í glugganum **Framleiðslugrunnur** inniheldur nokkra reiti sem skilgreina altækar reglur fyrir framboðsáætlun.  

 Eftirfarandi tafla gefur upp bestu venjur um uppsetningu valinna altækra áætlunarfæribreytareita. Nánari upplýsingar um reit fást með því að velja tengilinn í dálkinum **Uppsetningarreitur**.  

|Uppsetning reits|Bestu starfsvenjur|Athugasemd|  
|-----------------|-------------------|-------------|  
|Nota spá á staðsetningum|Valið ef spár eru gerðar fyrir tilteknar birgðageymslur.||  
|Íhlutir í birgðageymslu|Ef vörur eru ekki eru skilgreindar sem birgðahaldseiningar skal velja birgðageymslukóta aðalvöruhúss.|Þetta á einnig við ef aðeins er notuð innkaupatillögubók.|  
|Autt yfirflæðisstig|Velja skal **Leyfa sjálfgefinn útreikning** ef þú kemur frá Microsoft Dynamics NAV 5.0 eða eldri.|Notist eingöngu ef leyfa á öllum eða nokkrum af vörunum að flæða yfir endurpöntunarmarkið.|  
|Sjálfgefið hömlutímabil|Stilla á milli 1D og 5D.<br /><br /> Ef þú hefur ekki gert áætlanir áður í [!INCLUDE[d365fin](includes/d365fin_md.md)] skaltu stilla lengra tímabil.|Þegar notendur þekkja ólíkar ástæður aðgerðaboða betur skal stytta hömlutímabilið til að leyfa fleiri tillögur um breytingar.|  
|Sjálfgefið hömlu magn|Stilla á milli 5 og 20 prósent af lotustærð vörunnar.||  

## <a name="see-also"></a>Sjá einnig  
 [Uppsetning bestu venjur: Framboðsáætlun](setup-best-practices-supply-planning.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
 [Setja upp flókin notkunarsviðum með því að nota bestu venjur](set-up-complex-application-areas-using-best-practices.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

