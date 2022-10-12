---
title: Nota Power Automate flæði í Viðskiptamiðinu
description: Setja upp og nota Power Automate flæði til að stofna eða breyta aðalgögnum viðskipta.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 5fe089c0330a8d2b7a71f4907212665722d27d38
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606522"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Nota Power Automate rennur í [!INCLUDE[prod_short](includes/prod_short.md)]

Notandi getur notað [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín sem hluta af verkflæði í Microsoft Power Automate. Búðu til þitt eigið flæði og tengdu saman gögn frá innri og ytri aðilum með [!INCLUDE [prod_short](includes/prod_short.md)] tengivirkinu.

> [!NOTE]
> Þú verður að hafa gildan reikning við báða [!INCLUDE[prod_short](includes/prod_short.md)] og Power Automate.  

> [!TIP]
> Auk þess er hægt að Power Automate nota sniðmát samþykktarverkflæðis í [!INCLUDE[prod_short](includes/prod_short.md)]. Þó að þau séu tvö aðskilin verkflæðiskerfi er einhverju samþykktarverksniðmáti sem stofnað Power Automate er til bætt við listann yfir verkflæði að innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar um [verkflæði](across-workflow.md).

Power Automate flæði er ræst eftir atburðum eins og stofnun skráningar og skjalavistunar, breytingar eða eyðing (sjálfvirk streymi). Flæðin geta einnig keyrt á notandaskilgreinda áætlun (tímaflæði) eða eftirspurn (augnablik).

## <a name="power-automate-features-in-prod_short"></a>Power Automate aðgerðir í [!INCLUDE[prod_short](includes/prod_short.md)]

Streymi stækkar með innbyggðum tiltækum verkflæðisaðgerðum sem eru tiltækar í [!INCLUDE[prod_short](includes/prod_short.md)] án þess að krefjast kóðunar þekkingar og geta tengst margs konar atburðum og viðbrögðum, svo sem færslubreytingum, uppfærslum ytri skráa, bókað skjöl, auk ólíkra þjónustu Microsoft og þriðja aðila, svo sem Microsoft Outlook, Microsoft Excel Microsoft Dataverse Microsoft Teams,, Microsoft SharePoint, Microsoft Power Apps og fleira.

Þannig að til dæmis getur nýr sölureikningur kallað fram verkflæði fyrir samþykktarbeiðni, sem getur haft mismunandi tilvik eftir því hver er svari samþykkjanda. Neikvætt svar sendir tilkynningu og tölvupóst til samþykktarumsækjanda. Jákvætt svar uppfærir samtímis Excel-töflu sem er SharePoint staðsett í möppu og sendir uppfærslu á teymum spjalla.

Verk á augabragði eru notuð á sama hátt og í runustúðum, framkvæmd mörgum skrefum með nokkrum hnappabrennum og hleypt er frá tilteknum síðum eða töflum. Til dæmis getur áklæði bætt við hnapp í aðgerðavalmyndinni á **síðunni Lánardrottnar** til að loka fyrir greiðslur til lánardrottins og á sama tíma er hægt að senda sérhannaðan tölvupóst til tengiliðs lánardrottins og kaupanda fyrirtækisins sem og uppfæra tengilið í Outlook.

## <a name="automated-workflows"></a>Sjálfvirk verkflæði

Með Power Automate er hægt að búa til viðskiptastreymi beint í hús og treysta á eldri hönnuði. Hægt er að ræsa sjálfvirk verkflæði með því að hafa bæði innri og ytri viðburði í [!INCLUDE[prod_short](includes/prod_short.md)] og einnig að vera stilltur til að keyra reglulega. Lærðu meira og fáðu leiðbeiningar um það [hvernig á að stofna verkflæði í setja upp sjálfvirka verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) gr. um stjórnunarinnihald.

## <a name="instant-flows"></a>Augnablik streyma

[!INCLUDE [prod_short](includes/prod_short.md)] hægt að Power Automate keyra áklæði frá flestum lista, spjaldtölvu og skjalsíðum. Þegar admin hefur tengst [!INCLUDE [prod_short](includes/prod_short.md)] við Power Automate er hægt að sjá hvaða streymi fyrirtækið hefur bætt við þegar aðgerðin automate **er valin** á viðkomandi síðum. Skyndilausnir eru keyrðar án þess að fara [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar í reitnum [Setja upp sjálfvirka verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) gr. um stjórnunarinnihald.

Þessi augnablik opnast á síðu inni [!INCLUDE [prod_short](includes/prod_short.md)] á netinu þannig að þú getur haldið áfram innan samhengis viðskiptaferlisins sem þú varst í miðri. Aðgerðin automate **er** valin — í sumum síðum sem eru hreifður undir **valmyndinni fleiri Valkostir** — Veljið **Power Automate** valmyndaratriðið og veljið síðan viðeigandi tengil til að ræsa verkflæðið. Tengingin Power Automate sem þegar er uppsett fyrir þig.

Flest flæði gera kröfu um að fyllt sé út í reit eða tvö áður en keyrsluflæðiaðgerðin **er valin**.

> [!TIP]
> Ef þú sérð **ekki automate** aðgerð þá [!INCLUDE [prod_short](includes/prod_short.md)] hefur líklega ekki enn verið sett upp notkun Power Automate. Frekari upplýsingar frá admin.

## <a name="add-more-automated-flows-and-instant-flows"></a>Bæta við fleiri sjálfvirkum flæðum og skyndilausnum

Hægt er að búa til streymi í gegnum [vefsíðuna powerautomate.microsoft.com](https://powerautomate.microsoft.com). Hins vegar ef admin hefur kveikt á getu til að keyra flæði frá innu Power Automate á netinu er hægt að hefja vinnslu á flæði úr [!INCLUDE [prod_short](includes/prod_short.md)]**sjálfkeyrandi** aðgerðinni á viðeigandi síðum sem er hægt að finna undir **valmyndinni fleiri Valkostir** eftir síðunni. Þá er valmyndaratriðið valið **Power Automate** og síðan er valið að **gera flæðiaðgerð**. Power Automate Þá opnast í nýjum vafraflipa og þá skráir notandi sig inn sjálfkrafa.

Sýnishorn af sniðmátum má finna til að laga fyrirtækið og öll tiltæk kveikja á þeim og nota bæði [!INCLUDE [prod_short](includes/prod_short.md)] ytri verkfæri með því að velja **tengingarvalmyndina** á Power Automate vefsvæðinu. Frekari upplýsingar um tiltæk sniðmát og kveikir í reitnum setja upp sjálfvirka verkflæði [eru](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) sett upp í innihaldi stjórnunar.

## <a name="manage-automated-workflows"></a>Stjórna sjálfvirkum verkflæði

Hægt er að búa til nýjar rennur eða stjórna tiltækum Power Automate flæði í [!INCLUDE [prod_short](includes/prod_short.md)] á **síðunni stjórna Power Automate streymi**. Frekari upplýsingar í [Umsjón Power Automate með sjóðstreymi](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) í stjórnunarinnihaldi.

Einnig er hægt að stjórna tiltækum Power Automate verkflæði á **síðunni verkflæði** í [!INCLUDE[prod_short](includes/prod_short.md)]. Síðan er listi yfir innbyggð samþykkt og Power Automate verkflæði, með valkostum fyrir Hið síðarnefnda til að gera/óvirka, eyða og skoða verkflæðið á Power Automate vefsvæðinu.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/use-power-automate/)

## <a name="see-also"></a>Sjá einnig .

[[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða](across-flow-troubleshoot.md)  
[Vertu klár í rekstur fyrirtækja](ui-get-ready-business.md)  
[Verkflæði](across-workflow.md)  
[Flytja inn viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Setja upp[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  
[Stjórna Power Automate streymi](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Setja upp sjálfvirk verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Rofi á Skyndistreymi](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
