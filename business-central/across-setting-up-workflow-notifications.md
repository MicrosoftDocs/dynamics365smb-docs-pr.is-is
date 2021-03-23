---
title: Tilkynningar verkflæðis
description: Mörg Verkflæðissvör snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu, og að svarið sé að tilkynning sé send til notanda 2, samþykkjanda. Í næsta verkflæðisskrefi getur tilvikið verið að Notandi 2 samþyki færsluna, og svarið að tilkynning sé send til notanda 3 til að hefja tengt ferli samþykktu færslunnar. Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: d11a391a7fd91f6a094dfae9f8908ba4314b357a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378949"
---
# <a name="workflow-notifications"></a>Tilkynningar verkflæðis

Setja upp verkflæðin til að láta notendur vita sjálfkrafa þegar þeir þurfa að skoða skref í því verkflæði. Mörg Verkflæðissvör snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu, og að svarið sé að tilkynning sé send til notanda 2, samþykkjanda. Í næsta verkflæðisskrefi getur tilvikið verið að Notandi 2 samþyki færsluna, og svarið að tilkynning sé send til notanda 3 til að hefja tengt ferli samþykktu færslunnar. Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
> Almenna útgáfan af [!INCLUDE[prod_short](includes/prod_short.md)] styður tilkynningar sem tölvupóst og innri athugasemdir.  

> [!IMPORTANT]  
> Allar verkflæðistilkynningar eru sendar um verkröð. Ganga skal úr skugga um að verkröð í uppsetningu sé sett upp þannig að hún meðhöndli verkflæðistilkynningar og að gátreiturinn **Byrja sjálfkrafa frá þjóni** sé valinn. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Setja upp tilkynningar

Sett eru upp mismunandi verkflæðistilkynningar á viðkomandi stöðum:  

* Tilkynning samþykktaraðila

    Fyrir samþykktarverkflæði eru settir upp viðtakendur verkflæðistilkynninga með því að fylla út línu á síðunni **Notandauppsetning samþykktar** fyrir hvern notanda sem tekur þátt í verkflæðinu.  

    Ef notandi 2 er t.d tilgreindur í **Kenni samþykktaraðila** reitnum á línu fyrir notanda 1 þá er tilkynning um samþykktarbeiðni send til notanda 1. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  
* Áætlanir tilkynninga

    Hægt er að stilla hvenær og hvernig notendur fá tilkynningar verkflæðis með því að fylla út **Áætlun tilkynninga** síðuna fyrir hvern notanda verkflæðis. Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Sérsníða tilkynningar í tölvupósti

    Ef þú vilt geturðu sérsniðið innihald á tilkynningu tölvupósts með því að breyta skýrslu 1320, Tilkynningapóstur. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).  
* Svarmöguleikar

    Sett er upp tiltekið efni og reglur um tilkynningar verkflæðis þegar verkflæðið er stofnað. Þetta er gert með því að velja valkosti á síðunni **Valkostir fyrir verkflæðissvar** fyrir verkflæðissvarið sem táknar tilkynninguna. Frekari upplýsingar eru í skrefi 9 í [Stofna verkflæði](across-how-to-create-workflows.md).  

* Tilkynna sendanda

    Fyrir samþykktarverkflæði skal bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni hefur verið samþykkt eða henni hafnað. Frekari upplýsingar eru í skrefi 9 í [Stofna verkflæði](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Sjá einnig

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Búa til verkflæði](across-how-to-create-workflows.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]