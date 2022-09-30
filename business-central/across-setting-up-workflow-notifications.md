---
title: Uppsetning tilkynninga um samþykktarverkflæði
description: Í þessari grein er sagt til um hvernig eigi að setja upp verkflæðistilkynningar til að viðvörun notanda um að tilvik hafi orðið til þess að þau geti brugðist við; verkflæðissvar er nauðsynlegt.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 65dad3ffcb91415b13683f20a5e91274c3841c87
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585469"
---
# <a name="approval-workflow-notifications"></a>Tilkynningar um samþykktarverkflæði

Setja upp verkflæði til að tilkynna sjálfkrafa notendum þegar þörf er á athygli þeirra í skrefi í verkflæði. Mörg viðbrögð við verkflæði Tilkynna notanda um tilvik sem þeir verða að bregðast við hefur átt sér stað.

Til dæmis er hægt að stilla það þannig að notandi 2, notandi samþykkjanda, fái tilkynningu í hvert sinn sem notandi 1 biður um samþykki fyrir nýrri færslu. Í næsta verkflæðisskrefi eftir að notandi 2 samþykkir færsluna er notandinn 3 látinn vita og hægt að hefja tengda vinnslu færslunnar. Með verkflæðisskrefum er hver tilkynning bundin við samþykktarfærslu. Frekari upplýsingar á [verkflæði](across-workflow.md).  

> [!NOTE]  
> Sjálfgefin útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] styður tilkynningar í tölvupósti eða sem innri athugasemdir.  

> [!IMPORTANT]  
> Allar verkflæðistilkynningar eru sendar um verkröð. Ganga skal úr skugga um að vinnsluröðin í uppsetningunni sé sett upp til að annast verkflæðistilkynningar og að gátreiturinn ræsa sjálfkrafa frá þjóni **hafi verið valinn**. [Frekari upplýsingar um notkun Vinnubiðraða á að áætla verk](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Setja upp tilkynningar

Hægt er að setja upp mismunandi þætti verkflæðistilkynninga á eftirfarandi stöðum:  

* Tilkynning samþykktaraðila

  Fyrir samþykktarverkflæði eru settir upp viðtakendur verkflæðistilkynninga með því að fylla út línu á **uppsetningarsíðu** samþykktarinnar fyrir hvern notanda sem tekur þátt í verkflæðinu.  

  Ef notandi 2 er t.d tilgreindur í **Kenni samþykktaraðila** reitnum á línu fyrir notanda 1 þá er tilkynning um samþykktarbeiðni send til notanda 2. Frekari upplýsingar um [uppsetningu Samþykktarnotenda](across-how-to-set-up-approval-users.md). 
  
* Áætlanir tilkynninga

  Setja upp hvenær og hvernig notendur fá verkflæðistilkynningar með því að **fylla út tilkynningasíðu tilkynningarinnar** fyrir hvern notanda verkflæðis. Frekari upplýsingar eru tilgreindar í [Tilgreinið hvenær og hvernig á að taka á móti tilkynningum](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Sérsníða tilkynningar í tölvupósti

  Sé þess óskað er hægt að aðlaga efni tilkynningar í tölvupósti með því að breyta skýrslu 1320, netfang tilkynningar. Frekari upplýsingar er að [Stofna og breyta skipan](ui-how-create-custom-report-layout.md) sérsniðinnar skýrslu.  

  > [!NOTE]
  > Eigi að nota tölvupóst sem tilkynningamáta þarf að setja upp tölvupóst bæði fyrir sendanda og móttakanda í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar er að setja upp í [tölvupósti](admin-how-setup-email.md).
  
* Svarmöguleikar

  Setja upp sérstakt efni fyrir og reglur um verkflæðistilkynningu þegar notandi stofnar verkflæðið sem um ræðir. Veljið valkosti sérsniðsvalkosta á **síðunni viðbrögð** við verkflæði fyrir verkflæðissvarið sem stendur fyrir tilkynninguna. Frekari upplýsingar úr skrefi 9 í [hlutanum Stofna verkflæði](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Tilkynna sendanda

  Fyrir samþykktarverkflæði skal bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni hefur verið samþykkt eða henni hafnað. Frekari upplýsingar úr skrefi 9 í [hlutanum Stofna verkflæði](across-how-to-create-workflows.md#to-create-a-workflow).   

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Stofna samþykktarverkflæði](across-how-to-create-workflows.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
