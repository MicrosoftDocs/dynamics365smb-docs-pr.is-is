---
title: "Setja upp tilkynningar verkflæðis | Microsoft Docs"
description: "Mörg Verkflæðissvör snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu, og að svarið sé að tilkynning sé send til notanda 2, samþykkjanda. Í næsta verkflæðisskrefi getur tilvikið verið að Notandi 2 samþyki færsluna, og svarið að tilkynning sé send til notanda 3 til að hefja tengt ferli samþykktu færslunnar. Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 222056cc8b505d0ed027492d764ff4cde7f68795
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-workflow-notifications"></a>Setja upp tilkynningar verkflæðis
Mörg Verkflæðissvör snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu, og að svarið sé að tilkynning sé send til notanda 2, samþykkjanda. Í næsta verkflæðisskrefi getur tilvikið verið að Notandi 2 samþyki færsluna, og svarið að tilkynning sé send til notanda 3 til að hefja tengt ferli samþykktu færslunnar. Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
>  Almenna útgáfan af [!INCLUDE[d365fin](includes/d365fin_md.md)] styður tilkynningar sem tölvupóst og innri athugasemdir.  

> [!IMPORTANT]  
>  Allar verkflæðistilkynningar eru sendar um verkröð. Ganga skal úr skugga um að verkröð í þinni lausn. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

Sett eru upp mismunandi verkflæðistilkynningar á viðkomandi stöðum:  

1.  Fyrir samþykktarverkflæði eru settir upp viðtakendur verkflæðistilkynninga með því að fylla út línu í **Notandauppsetning** glugganum fyrir hvern notanda sem tekur þátt í verkflæðinu. Ef notandi 2 er t.d tilgreindur í **Kenni samþykktaraðila** reitnum á línu fyrir notanda 1 þá er tilkynning um samþykktarbeiðni send til notanda 1. Nánari upplýsingar eru í [Hvernig á að: Setja upp notendur sem samþykkjendur](across-how-to-set-up-approval-users.md)  
2.  Hægt er að stilla hvenær og hvernig notendur fá tilkynningar verkflæðis með því að fylla út **Áætlun tilkynninga** gluggann fyrir hvern notanda verkflæðis. Nánari upplýsingar er að finna í [Hvernig á að: Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)  
3.  Almennt efni og útlit tilkynninga, þ.m.t. tilkynningar um verkflæðissvör sem eru of sein, eru sett upp með því að setja upp tilkynningasniðmát í **Tilkynningasniðmát** glugganum. Hægt er að nota sjálfgefin sniðmát sem fylgja með [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4.  Sett er upp tiltekið efni og reglur um tilkynningar verkflæðis þegar verkflæðið er stofnað. Þetta er gert með því að velja valkosti í **Valkostir fyrir verkflæðissvar** glugganum fyrir verkflæðissvarið sem táknar tilkynninguna. Frekari upplýsingar eru að finna í 9 skrefi í [Hvernig skal: Stofna Verkflæði](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Sjá einnig  
 [Hvernig á að: Setja upp notendur sem samþykkjendur](across-how-to-set-up-approval-users.md)   
 [Hvernig á að: Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)   
 [Hvernig á að: Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Hvernig á að: Búa til verkflæði](across-how-to-create-workflows.md)   
 [Hvernig á að: Vinna með tilkynningasniðmát](across-how-to-manage-notification-templates.md)   
 [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)   
 [Hvernig á að: Setja upp tölvupóst](madeira-how-setup-email.md)   
 [Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Verkflæði](across-workflow.md)   

