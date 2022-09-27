---
title: Setja upp tilkynningar verkflæðis
description: Í þessari grein er sagt til um hvernig eigi að setja upp verkflæðistilkynningar til að viðvörun notanda um að tilvik hafi orðið til þess að þau geti brugðist við; verkflæðissvar er nauðsynlegt.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9405af9c52b17ab34fded263692e3294ed8aaf11
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533968"
---
# <a name="workflow-notifications"></a>Tilkynningar verkflæðis

Setja upp verkflæðin til að láta notendur vita sjálfkrafa þegar þeir þurfa að skoða skref í því verkflæði. Mörg Verkflæðissvör snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því.

Til dæmis er hægt að stilla þann notanda 2, notandi samþykkjanda, fær tilkynningu í hvert sinn sem notandi 1 biður um samþykki fyrir nýrri færslu. Í næsta verkflæðisskrefi er notandi 3 látinn vita eftir að notandi 2 samþykkir færsluna til að hefja tengda vinnslu færslunnar. Með verkflæðisskrefum er hver tilkynning bundin við samþykktarfærslu. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
> Sjálfgefin útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] styður tilkynningar sem tölvupóstur og sem innri athugasemdir.  

> [!IMPORTANT]  
> Allar verkflæðistilkynningar eru sendar um verkröð. Ganga skal úr skugga um að verkröð í uppsetningu sé sett upp þannig að hún meðhöndli verkflæðistilkynningar og að gátreiturinn **Byrja sjálfkrafa frá þjóni** sé valinn. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Setja upp tilkynningar

Hægt er að setja upp mismunandi þætti verkflæðistilkynninga á eftirfarandi stöðum:  

* Tilkynning samþykktaraðila

    Fyrir samþykktarverkflæði eru settir upp viðtakendur verkflæðistilkynninga með því að fylla út línu á síðunni **Notandauppsetning samþykktar** fyrir hvern notanda sem tekur þátt í verkflæðinu.  

    Ef notandi 2 er t.d tilgreindur í **Kenni samþykktaraðila** reitnum á línu fyrir notanda 1 þá er tilkynning um samþykktarbeiðni send til notanda 2. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  
* Áætlanir tilkynninga

    Hægt er að stilla hvenær og hvernig notendur fá tilkynningar verkflæðis með því að fylla út **Áætlun tilkynninga** síðuna fyrir hvern notanda verkflæðis. Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Sérsníða tilkynningar í tölvupósti

    Sé þess óskað, er hægt að aðlaga efni tilkynningar í tölvupósti með því að breyta skýrslu 1320, netfang tilkynningar. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Eigi að nota tölvupóst sem tilkynningamáta þarf að setja upp tölvupóst bæði fyrir sendanda og móttakanda í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

* Svarmöguleikar

    Sett er upp tiltekið efni og reglur um tilkynningar verkflæðis þegar verkflæðið er stofnað. Veljið valkosti sérsniðsvalkosta á **síðunni viðbrögð** við verkflæði fyrir verkflæðissvarið sem stendur fyrir tilkynninguna. Sjá skref 9 í [Create verkflæði til að fá frekari upplýsingar](across-how-to-create-workflows.md#to-create-a-workflow).  

* Tilkynna sendanda

    Fyrir samþykktarverkflæði skal bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni hefur verið samþykkt eða henni hafnað. Sjá skref 9 í [Create verkflæði til að fá frekari upplýsingar](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

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
