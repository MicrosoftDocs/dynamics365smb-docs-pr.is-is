---
title: Verkflæði í Dynamics 365 Business Central
description: Nota innbyggða verkflæðistilvik til að setja upp samþykktarverkflæði fyrir viðbót við sjálfvirk verkflæði Byggt á Power Automate. Hægt er að setja upp skref til að úthluta verkum á ólíka einstaklinga sem hluta af mismunandi verkum í viðskiptaferli.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
ms.openlocfilehash: c8cd251a2e82cd1a721f070f14986dd78c6f1730
ms.sourcegitcommit: 902834e76460d751a345485c66fd2831066b396b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716533"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Verkflæði í Dynamics 365 Business Central

Hægt er að setja upp og nota verkflæði til að tengja verk-ferliverkin sem eru unnin af mismunandi notendum. Kerfisverk, svo sem Sjálfvirk bókun, er hægt að taka með sem þrep í verkflæði. Kerfisverk geta verið á undan eða eftir notendaverkefnum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.

Sjálfgefin útgáfa [!INCLUDE [prod_short](includes/prod_short.md)] styður þrjár gerðir verkflæða:
  
* Power Automate streymir

  * Sjálfvirk streymi sem eru ræst upp eftir atvikum (eins og færsla eða skjalastofnun, breyting eða eyðing) í [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig innifalið eru samþykkisflæði sem er stofnað í Power Automate þeirri kveikju þegar beðið er um samþykki í [!INCLUDE[prod_short](includes/prod_short.md)].
  * Skyndiflæði sem er sjálfvirkt ræst af **lista**, spjöld og fylgiskjalssíðum. 

    Virkja og kveikja Power Automate handvirkt á flæði á [!INCLUDE[prod_short](includes/prod_short.md)] færslu, eins og viðskiptavin, vöru eða sölupöntun, með valkostum til að vinna úr upplýsingum bæði innan og utan (með samþættum verkfærum).

* Samþykktarverkflæði samkvæmt sniðmátum sem hafa verið byggð á verkflæði

  **Á síðunni verkflæðissniðmát** er hægt að sjá öll tiltæk verkflæði. Prufuútgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur mörg forskilgreind verkflæði fyrir sniðmát verkflæðis sem hægt er að afrita til að stofna ný. Þegar sniðmát er opnað á **síðunni verkflæðissniðmát** og verkflæðisheitið byrjar *MS-* síðan var sniðmátinu bætt við af Microsoft.

## <a name="power-automate-flows"></a>Power Automate streymir

Með [!INCLUDE [prod_short](includes/prod_short.md)] netinu er hægt að skrá sig Power Automate til að smíða öflug sjálfvirk verkflæði. Þú keyrir verkflæðið innan [!INCLUDE [prod_short](includes/prod_short.md)] frá. Flæðin geta tengst innri og ytri gagnagjöfum og verkfærum, án þess að kóðun þekkingar.

|**Til að** |**Sjá**|
|-------|-------|
|Byrja með Power Automate og búa til flæði, keyra augnablik streyma|[Nota Power Automate rennur í[!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Frekari upplýsingar um hvernig á að stofna, breyta og stjórna streymi|[Setja upp sjálfvirka Flæðistreyta](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) og [Setja upp skyndilausnir](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Setja upp Power Automate samþættingu við [!INCLUDE[prod_short](includes/prod_short.md)] fyrir notendur sem admin|[Setja upp Power Automate samþættingu](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## <a name="approval-workflows"></a>Samþykktarverkflæði

Samþykktarverkflæði er stofnað með því að skrá þátt skrefanna í línunum. Hvert skref samanstendur af:
- Verkflæðistilvik, sem er stjórnað eftir atvikum skilyrðum
- Svar við verkflæði, sem er stjórnað af svarmöguleikum.

Til að skilgreina verkflæðisskref er fyllt út í reiti í verkflæðislínum með föstum lista yfir tilvik og svargildi sem tákna aðstæður sem styðja með forritskóta.<!--What are the "values"? Can we give an example?-->

Dæmi um tilvik samþykktarverkfallsins eru meðal annars stofnun sölu-eða innkaupapantana/tilboða/reikninga, Verðbreytingar, lánardrottna-eða viðskiptamannabókanir og fleira.

[!INCLUDE[workflow](includes/workflow.md)]

| **Til að** | **Sjá** |
|--|--|
| Setja upp notendur samþykktarverkflæðis, tilgreina hvernig notendur fá tilkynningu og stofna nýtt verkflæði. (Ef stofna á nýtt verkflæði fyrir Óstudd aðstæður þarf að innleiða verkflæðiatriðin sem þarf með því að sérsníða forritskóða.) | [Setja upp samþykktarverkflæði](across-set-up-workflows.md) |
| Virkja samþykktarverkflæði, vinna með verkflæðistilkynningar, þar sem beðið er um og samþykkt verkflæðisskref. Setja verkflæði í skjalasafn eða eyða. | [Nota samþykktarverkflæði](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórna verkum](projects-manage-projects.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
