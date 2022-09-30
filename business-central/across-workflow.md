---
title: Verkflæði í Dynamics 365 Business Central
description: Nota innbyggða verkflæðistilvik til að setja upp samþykktarverkflæði fyrir viðbót við sjálfvirk verkflæði Byggt á Power Automate. Hægt er að setja upp skref til að úthluta verkum á ólíka einstaklinga sem hluta af mismunandi verkum í viðskiptaferli.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585622"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Verkflæði í Dynamics 365 Business Central

Hægt er að setja upp og nota verkflæði til að tengja verk-ferliverkin sem eru unnin af mismunandi notendum. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.

Sjálfgefin útgáfa [!INCLUDE [prod_short](includes/prod_short.md)] styður þrjár gerðir verkflæða:

* Samþykktarverkflæði samkvæmt sniðmátum sem hafa verið byggð á verkflæði

  **Á síðunni verkflæðissniðmát** er hægt að sjá öll tiltæk verkflæði. Prufuútgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur mörg forskilgreind verkflæði fyrir sniðmát verkflæðis sem hægt er að afrita til að stofna ný. Þegar sniðmát er opnað á **síðunni verkflæðissniðmát** og verkflæðisheitið byrjar *MS-* síðan var sniðmátinu bætt við af Microsoft.
  
* Power Automate flæðir sem þú setur upp sjálfur

  Eitthvert verkflæðissniðmát sem er stofnað með Microsoft Power Automate er bætt við listann yfir sniðmát verkflæðis innan [!INCLUDE[prod_short](includes/prod_short.md)]. [Frekari upplýsingar um notkun [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate flæðigryfjur](across-how-use-financials-data-source-flow.md). 
  
* Skyndihjálpar er **sjálfkrafa hrundið af stað með automate** aðgerðinni ([!INCLUDE [prod_short](includes/prod_short.md)] eingöngu á netinu).

  Virkja og kveikja Power Automate handvirkt á flæði á [!INCLUDE[prod_short](includes/prod_short.md)] færslu, eins og viðskiptavin, vöru eða sölupöntun, með valkostum til að vinna úr upplýsingum bæði innan og utan (með samþættum verkfærum). Frekari upplýsingar í kaflanum um [skyndifriðun](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Power Automate streymir

Með því að nota [!INCLUDE [prod_short](includes/prod_short.md)] Online er hægt að skrá sig Power Automate til að smíða öflug sjálfvirk verkflæði. Hægt er að keyra þau verkflæði innan [!INCLUDE [prod_short](includes/prod_short.md)] frá, tengja innri og ytri uppsprettu gagna og verkfæra án þess að kóðun þekkingar.

Power Automate Hægt er að kveikja flæði eftir atburðum (eins og færslu-eða skjalastofnun, breytingar eða eyðingu) og keyra á notandaskilgreinda áætlun eða í þörf (sem **kallast Skyndiflæði**).

## <a name="approval-workflows"></a>Samþykktarverkflæði

Samþykktarverkflæði er stofnað með því að skrá þátt skrefanna í línunum. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Verkflæðisskrefum er skilgreint með því að fylla út reiti í verkflæðislínum með því að nota fasta lista yfir tilvik og svargildi sem tákna áætlanir sem styðja með forritskóta.<!--What are the "values"? Can we give an example?-->

Dæmi um tilvik samþykktarverkflæða eru, meðal annars, stofnun sölu-eða innkaupapantana/tilboða/reikninga, Verðbreytingar og breytingar á lánardrottni eða viðskiptavini.

[!INCLUDE[workflow](includes/workflow.md)]

| **Til að** | **Sjá** |
|--|--|
| Setja upp notendur samþykktarverkflæðis, tilgreina hvernig notendur fá tilkynningu og stofna nýtt verkflæði. (Ef stofna á nýtt verkflæði fyrir Óstudd aðstæður þarf að innleiða verkflæðiatriðin sem þarf með því að sérsníða forritskóða.) | [Setja upp samþykktarverkflæði](across-set-up-workflows.md) |
| Virkja samþykktarverkflæði, vinna með verkflæðistilkynningar, þar sem beðið er um og samþykkt verkflæðisskref. Setja verkflæði í skjalasafn eða eyða. | [Nota samþykktarverkflæði](across-use-workflows.md) |
| Samþætta gögn fyrirtækisins með Power Automate verkflæði, nota bæði innri og ytri heimildir og tilvik til að stofna og gera verk eða verkflæði. | [Nota Power Automate rennur í[!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórna verkum](projects-manage-projects.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
