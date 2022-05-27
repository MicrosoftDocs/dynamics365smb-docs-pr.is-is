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
ms.openlocfilehash: 84d4a87a0edab18be342b9ed5732de0350a31645
ms.sourcegitcommit: bc645e7ecb1940a85b2c433aa894d3494c9b10df
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743672"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Verkflæði í Dynamics 365 Business Central

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Sjálfgefin útgáfa [!INCLUDE [prod_short](includes/prod_short.md)] styður þrjár gerðir verkflæða:

* Sjálfvirk samþykktarverkflæði út frá innbyggðu verkflæðissniðmátum  

  **Á síðunni verkflæðissniðmát** er hægt að sjá öll tiltæk verkflæði. Prufuútgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur fjölda forskilgreindra verkflæða sem sniðmát verkflæðis sem hægt er að afrita til að stofna verkflæði. Þegar verkflæðissniðmát er opnað af **síðunni verkflæði sniðmátsins** og heiti verkflæðisins byrjar *á MS-* þá er sniðmáti verkflæðis bætt við Microsoft.  
* Sjálfvirkt streymi sem þú setur upp sjálfur  

  Öll verkflæðissniðmát sem eru stofnuð með Power Automate er bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna [í notkun Viðskiptamiðis í Power Automate streymi](across-how-use-financials-data-source-flow.md).  
* Ræstar rennur úr **sjálfvirkri** aðgerð ([!INCLUDE [prod_short](includes/prod_short.md)] aðeins nettenginu). Frekari upplýsingar er að finna [í handvirku skyndilausnum](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate streymir

Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] Online er hægt að skrá sig fyrir Power Automate og byggja svo upp öfluga sjálfvirka streymi sem þú getur keyrt að innan [!INCLUDE [prod_short](includes/prod_short.md)] frá. Nánari upplýsingar eru í notkun í flæðisjá [[!INCLUDE[prod_short](includes/prod_short.md)] . Power Automate](across-how-use-financials-data-source-flow.md)  

## <a name="automated-approval-workflows"></a>Sjálfvirk samþykktarverkflæði

Samþykktarverkflæði er stofnað með því að skrá þátt skrefanna í línunum. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

Ef viðskiptaaðstæður krefjast verkflæðistilviddar eða viðbragða sem ekki er stutt í sjálfgefnu útgáfuna skal skrá sig í Power Automate. Nánari upplýsingar eru í notkun í flæðisjá [[!INCLUDE[prod_short](includes/prod_short.md)] . Power Automate](across-how-use-financials-data-source-flow.md) Einnig er hægt að sækja app eða vinna með Microsoft samstarfsaðila til að sérsníða forritskóða.  

Til að setja upp og nota verkflæði sem ekki eru skilgreind í Power Automate skal athuga eftirfarandi greinar:  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp notendum verkflæðis, skilgreina hvernig notendur fá tilkynningu, og búa til ný verkflæði. Til að skapa ný verkflæði fyrir óstuddar sviðsmyndir skal framkvæma umbeðnar verkflæðiseiningar með því að sérsníða kóða forrits.|[Setja upp verkflæði](across-set-up-workflows.md)|  
|Virkja verkflæði, bregðast við tilkynningar verkflæðis, þ.m.t samþykktarbeiðnum og samþykkja beiðnir til að framkvæma skref í verkflæði. Setja verkflæði í skjalasafn eða eyða.|[Nota verkflæði](across-use-workflows.md)|  

## <a name="see-also"></a>Sjá einnig

[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórna verkum](projects-manage-projects.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Notkun [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate flæðigryfjur](across-how-use-financials-data-source-flow.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða](across-flow-troubleshoot.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]