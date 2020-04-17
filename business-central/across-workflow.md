---
title: Verkflæði | Microsoft Docs
description: Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: fb5fce62bddbb4739ef14851464a973262569815
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187533"
---
# <a name="workflow"></a>Verkflæði
Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

 Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

 Almenna útgáfan af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur fjölda forstilltra verkflæða sem birtast í sniðmáti verkflæðis og þau er hægt að afrita til að stofna verkflæði. Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“. Sjá nánari upplýsingar í lista yfir verkflæðissniðmát á síðunni Verkflæðissniðmát.  

 Ef viðskiptasviðsmynd kallar á verkflæðistilvik eða -viðbrögð sem ekki eru studd verður Microsoft-samstarfsaðili að virkja þau með því að sérstilla forritakóðann. Nánari upplýsingar er að finna í [Sýnikennsla: Innleiðing nýrra verkflæðistilvika og svara](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) í þróunar- og IT-pro hjálp.

 > [!NOTE]
 > Til viðbótar við Workflow-virknina innan [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að sameina við Microsoft Flow til að skilgreina verkflæði fyrir tilvik í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðiskerfi, þá eru öll Flow-sniðmát sem búin eru til með Microsoft Flow bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Notkun Business Central í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp notendum verkflæðis, skilgreina hvernig notendur fá tilkynningu, og búa til ný verkflæði. Til að skapa ný verkflæði fyrir óstuddar sviðsmyndir skal framkvæma umbeðnar verkflæðiseiningar með því að sérsníða kóða forrits.|[Uppsetning verkflæðis](across-set-up-workflows.md)|  
|Virkja verkflæði, bregðast við tilkynningar verkflæðis, þ.m.t samþykktarbeiðnum og samþykkja beiðnir til að framkvæma skref í verkflæði. Setja verkflæði í skjalasafn eða eyða.|[Nota verkflæði](across-use-workflows.md)|  

## <a name="see-also"></a>Sjá einnig  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórna verkum](projects-manage-projects.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
