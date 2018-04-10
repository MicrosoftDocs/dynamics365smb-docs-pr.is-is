---
title: "Uppsetning verkflæðis | Microsoft Docs"
description: "Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d2301b31308c1300961d78478ce1ada807eddeab
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-workflows"></a>Uppsetning verkflæðis
Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði. Frekari upplýsingar eru í [Nota verkflæði](across-use-workflows.md).  

 Áður en byrjað er að nota verkflæði verður að setja upp notendur verkflæðis og samþykktarnotendur, tilgreikna hvernig notendur fá tilkynningar um skref verkflæðis og stofna svo verkflæði, hugsanlega eftir að hafa sérsniðið kóða.  

 Í glugganum **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

 Ef viðskiptasviðsmynd kallar á verkflæðistilvik eða -viðbrögð sem ekki eru studd verður Microsoft-samstarfsaðili að virkja þau með því að sérstilla forritakóðann. Nánari upplýsingar er að finna í [Sýnikennsla: Innleiðing nýrra verkflæðistilvika og svara](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) í þróunar- og IT-pro hjálp.

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp notendur og notendahópa verkflæðis.|[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)|  
|Setja upp notendur verkflæðis sem taka þátt í samþykktarverkflæði.|[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)|  
|Tilgreinið hvernig notendum verkflæðis er tilkynnt um skref verkflæðis, þ.m.t. samþykktarbeiðnir.|[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)|  
|Tilgreinið hvenær notendur fá tilkynningar og hvort safna á saman tilkynningum innan tímabils til að lágmarka fjölda tilkynninga.|[Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Setja upp útlit og almennt efni nýrra tilkynningapóst verkflæðis, eða flytja út, breyta, og flytja aftur inn fyrirliggjandi útlit.|[Vinna með tilkynningasniðmát](across-how-to-manage-notification-templates.md)|  
|Uppsetning SMTP-netþjóns til að virkja tölvupóstssamskipti inn og út af [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Setja upp tölvupóst](admin-how-setup-email.md)|
|Tilgreinið ólík skref verkflæðis eftir tengdum verkflæðistilvikum með verkflæðisviðbrögðum.|[Búa til verkflæði](across-how-to-create-workflows.md)|  
|Nota verkflæðissniðmát til að stofna ný verkflæði.|[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)|  
|Deila verkflæði með öðrum [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunnum.|[Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md)|  
|Lærið að setja upp verkflæði fyrir söluskjöl sem eru til samþykktar með því að fylgja verkferli frá upphafi til enda.|[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Bæta við stuðningur fyrir sviðsmynd viðskipta sem þurfa ný verkflæðistilvik eða viðbrögð með því að sérsníða forritskóðann.|[Sýnikennsla: Innleiðing nýrra verkflæðistilvika og svörunar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Sjá einnig  
 [Nota verkflæði](across-use-workflows.md)   
 [Verkflæði](across-workflow.md)   
 [Kynning: Uppsetning og notkun verkflæðis innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Unnið með Financials](ui-work-product.md)
