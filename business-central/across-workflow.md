---
title: Verkflæði í Dynamics365 Business Central
description: Nota innbyggða verkflæðistilvik til að setja upp samþykktarverkflæði fyrir viðbót við sjálfvirk verkflæði Byggt á Power Automate. Hægt er að setja upp skref til að úthluta verkum á mismunandi einstaklinga sem hluta af mismunandi verkum í viðskiptaferli.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: ab7d131e965b0698c6e33a0b1a43c8f408a7b1b2
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129903"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Verkflæði í Dynamics 365 Business Central

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Sjálfgefin útgáfa [!INCLUDE [prod_short](includes/prod_short.md)] styður þrjár gerðir verkflæða:

* Sjálfvirk samþykktarverkflæði út frá innbyggðu verkflæðissniðmátum  

  **Á síðunni verkflæðissniðmát** er hægt að sjá öll tiltæk verkflæði. Prufuútgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur mörg forskilgreind verkflæði með verkflæðissniðmátum sem hægt er að afrita til að stofna verkflæði. Þegar verkflæðissniðmát er opnað af **síðunni verkflæði sniðmátsins** og heiti verkflæðisins byrjar *á MS-* þá er sniðmáti verkflæðis bætt við Microsoft.  
* Sjálfvirkt streymi sem þú setur upp sjálfur  

  Öll verkflæðissniðmát sem eru stofnuð með Power Automate er bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna [í notkun Viðskiptamiðis í Power Automate streymi](across-how-use-financials-data-source-flow.md).  
* Ræstar rennur úr **sjálfvirkri** aðgerð ([!INCLUDE [prod_short](includes/prod_short.md)] aðeins nettenginu). Frekari upplýsingar er að finna [í handvirku skyndilausnum](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate streymir

Með því að nota [!INCLUDE [prod_short](includes/prod_short.md)] online getur þú skráð þig fyrir Power Automate og byggja síðan upp öfluga sjálfvirka streymdi sem þú getur keyrt að innan [!INCLUDE [prod_short](includes/prod_short.md)] frá. Nánari upplýsingar eru í notkun í flæðisjá [[!INCLUDE[prod_short](includes/prod_short.md)] . Power Automate](across-how-use-financials-data-source-flow.md)  

## <a name="automated-approval-workflows"></a>Sjálfvirk samþykktarverkflæði

Samþykktarverkflæði er stofnað með því að skrá þátt skrefanna í línunum. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

[!INCLUDE[workflow](includes/workflow.md)]

Til að setja upp og nota verkflæði sem ekki eru skilgreind í Power Automate, Athugið eftirfarandi greinar:  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp notendum verkflæðis, skilgreina hvernig notendur fá tilkynningu, og búa til ný verkflæði. Til að skapa ný verkflæði fyrir óstuddar sviðsmyndir skal framkvæma umbeðnar verkflæðiseiningar með því að sérsníða kóða forrits.|[Setja upp verkflæði](across-set-up-workflows.md)|  
|Virkja verkflæði, bregðast við tilkynningar verkflæðis, þ.m.t samþykktarbeiðnum og samþykkja beiðnir til að framkvæma skref í verkflæði. Setja verkflæði í skjalasafn eða eyða.|[Nota verkflæði](across-use-workflows.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórna verkum](projects-manage-projects.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Notkun [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate flæðigryfjur](across-how-use-financials-data-source-flow.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]