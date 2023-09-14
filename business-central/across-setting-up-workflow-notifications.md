---
title: Setja upp tilkynningar samþykktarverkflæðis
description: Í þessari grein er sagt hvernig á að setja upp tilkynningar verkflæðis til að láta notanda vita að tilvik hafi komið upp sem þarf að bregðast við; verkflæðissvar er nauðsynlegt.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# Tilkynning samþykktarverkflæðis

Setja upp verkflæðin til að láta notendur vita sjálfkrafa þegar þeir þurfa að skoða skref í því verkflæði. Mörg verkflæðisviðbrögð fela í sér að láta notanda vita um tilvik sem hefur komið upp og hann verður að bregðast við.

Til dæmis er hægt að stilla þau á notanda 2, samþykktarnotandinn sem fær tilkynningu þegar notandi 1 biður um samþykki fyrir nýja færslu. Í næsta verkflæðisskrefi, eftir að notandi 2 samþykkir færsluna, er notandi 3 látinn vita og getur hafið tengda úrvinnslu á færslunni. Með verkflæðisskrefum samþykktar er hver tilkynning bundin við samþykktarfærslu. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
> Sjálfgefin útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] styður tilkynningar í tölvupósti eða er með innri athugasemdir.  

> [!IMPORTANT]  
> Allar verkflæðistilkynningar eru sendar um verkröð. Gakktu úr skugga um að verkröð í uppsetningu sé sett upp þannig að hún meðhöndli verkflæðistilkynningar og að gátreiturinn **Byrja sjálfkrafa frá þjóni** sé valinn. Frekari upplýsingar eru í [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## Setja upp tilkynningar

Hægt er að setja upp mismunandi verkflæðistilkynningar á viðkomandi stöðum:  

* Tilkynning samþykktaraðila

  Fyrir samþykktarverkflæði eru settir upp viðtakendur verkflæðistilkynninga með því að fylla út línu á síðunni **Notandauppsetning samþykktar** fyrir hvern notanda sem tekur þátt í verkflæðinu.  

  Ef notandi 2 er t.d tilgreindur í **Kenni samþykktaraðila** reitnum á línu fyrir notanda 1 þá er tilkynning um samþykktarbeiðni send til notanda 2. Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md). 
  
* Áætlanir tilkynninga

  Stilla hvenær og hvernig notendur fá tilkynningar verkflæðis með því að fylla út **Áætlun tilkynninga** síðuna fyrir hvern notanda verkflæðis. Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Sérsníða tilkynningar í tölvupósti

  Ef þú vilt geturðu sérsniðið innihald á tilkynningu tölvupósts með því að breyta skýrslu 1320, Tilkynningapóstur. Frekari upplýsingar eru í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Eigi að nota tölvupóst sem tilkynningamáta þarf að setja upp tölvupóst bæði fyrir sendanda og móttakanda í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar má finna á [Setja upp tölvupóst](admin-how-setup-email.md).
  
* Svarmöguleikar

  Sett er upp tiltekið efni og reglur um tilkynningar verkflæðis þegar verkflæðið er stofnað. Veldu valkosti sérstillingar á síðunni **Verkflæðisviðbrögð** fyrir verkflæðisviðbrögðin sem standa fyrir tilkynninguna. Frekari upplýsingar er að finna í skrefi 9 í hlutanum [Stofna verkflæði](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Tilkynna sendanda

  Fyrir samþykktarverkflæði skal bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni hefur verið samþykkt eða henni hafnað. Frekari upplýsingar er að finna í skrefi 9 í hlutanum [Stofna verkflæði](across-how-to-create-workflows.md#to-create-a-workflow).   

## Sjá tengda [Microsoft þjálfun](/training/modules/create-workflows/)

## Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
