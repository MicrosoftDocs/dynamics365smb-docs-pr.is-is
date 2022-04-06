---
title: Verkflæði í Dynamics365 Business Central
description: Notaðu verkflæði sem tengja viðskiptaferlisverk sem aðrir notendur framkvæma. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa með sem verkflæðisskref.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9cfdcc9bbf8e24675c6894b8ca2efbf10129d990
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511182"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Verkflæði í Dynamics 365 Business Central

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

 Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

 Almenna útgáfan af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur fjölda forstilltra verkflæða sem birtast í sniðmáti verkflæðis og þau er hægt að afrita til að stofna verkflæði. Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“. Sjá nánari upplýsingar í lista yfir verkflæðissniðmát á síðunni Verkflæðissniðmát.  

 Ef viðskiptaaðstæður krefjast verkflæðistilviks eða svars sem ekki er stutt er annað hvort hægt að nota Power Automate eða vinna með Microsoft-samstarfsaðila til að sérsníða forritskóða. Nánari upplýsingar eru [í notkun [!INCLUDE[prod_short](includes/prod_short.md)] í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).

Öll verkflæðissniðmát sem eru stofnuð með Power Automate er bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna [í notkun Viðskiptamiðis í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp notendum verkflæðis, skilgreina hvernig notendur fá tilkynningu, og búa til ný verkflæði. Til að skapa ný verkflæði fyrir óstuddar sviðsmyndir skal framkvæma umbeðnar verkflæðiseiningar með því að sérsníða kóða forrits.|[Uppsetning verkflæðis](across-set-up-workflows.md)|  
|Virkja verkflæði, bregðast við tilkynningar verkflæðis, þ.m.t samþykktarbeiðnum og samþykkja beiðnir til að framkvæma skref í verkflæði. Setja verkflæði í skjalasafn eða eyða.|[Nota verkflæði](across-use-workflows.md)|  

## <a name="see-also"></a>Sjá einnig

[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórna verkum](projects-manage-projects.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]