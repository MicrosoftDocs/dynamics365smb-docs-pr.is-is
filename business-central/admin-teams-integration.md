---
title: Stjórnun Microsoft Teams samþættingar við Business Central | Microsoft docs
description: Stjórna samþættingu Business Central við Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 2d86e96b1778df47f0ead9845e2585905087adae
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046481"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Að stjórna Microsoft Teams samþættingu við [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Í þessari grein er að finna yfirlit yfir það sem hægt er að gera sem stjórnandi til að stýra Microsoft Teams samþættingu við [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>Eftir Microsoft Teams

### <a name="minimum-requirements"></a>Lágmarkskröfur

Í þessum hluta er lýst lágmarkskröfum til að eiginleikar [!INCLUDE [prod_short](includes/prod_short.md)]-forritsins virki í Teams.

- Nauðsynleg leyfi

    Eftirfarandi tafla gefur yfirlit yfir leyfin sem þarf til að eiginleikar [!INCLUDE [prod_short](includes/prod_short.md)]-forritsins virki í Teams.

    |Hvað|Teams-leyfi|[!INCLUDE [prod_short](includes/prod_short.md)] leyfi|
    |----|---|---|
    |Límið tengil við [!INCLUDE [prod_short](includes/prod_short.md)]-færslu í samtal og sendið hann sem spjald.|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|
    |Skoðið spjald [!INCLUDE [prod_short](includes/prod_short.md)]-færslu í samtali.|![gátmerki](media/check.png "ávísun")||
    |Skoðið frekari upplýsingar um spjald fyrir [!INCLUDE [prod_short](includes/prod_short.md)]-færslu í samtali.|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|

- Leyfa forskoðanir vefslóða

    Það verður að vera kveikt á reglustillingunni **Leyfa forskoðanir vefslóða**. Annars verður ekki hægt að búa til spjald fyrir [!INCLUDE [prod_short](includes/prod_short.md)]-tengla sem límdir eru í samtal í Teams. Frekari upplýsingar um þessa stillingur er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Að stjórna [!INCLUDE [prod_short](includes/prod_short.md)]-forritinu (valfrjálst)

Sem stjórnandi í Teams er hægt að stjórna öllum forritum fyrir fyrirtækið, þ.m.t. [!INCLUDE [prod_short](includes/prod_short.md)]-forritinu. Hægt er að samþykkja eða setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir fyrirtækið þitt, útiloka notanda frá því að setja upp forritið og fleira.

Frekari upplýsingar er að finna í eftirfarandi greinum í fylgiskjölum Microsoft Teams:

- [Stjórna forritunum í Microsoft Teams stjórnendamiðstöðinni](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Stjórna uppsetningarreglum forrits í Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>Eftir [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Lágmarkskröfur

- útgáfa [!INCLUDE [prod_short](includes/prod_short.md)]:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2020 útgáfutímabil 2, uppfærsla 17.3 eða nýrri. Samþætting Teams er aðeins studd fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu; ekki á staðnum.

- Codeunit: **2718 Þjónustuaðili síðusamantektar** er gefin út sem vefþjónusta:

    Þetta codeunit er gefið út sem vefþjónusta að sjálfgefnu. Codeunit er hluti af kerfisforriti [!INCLUDE [prod_short](includes/prod_short.md)]. Það er notað til að sækja reitargögn fyrir [!INCLUDE [prod_short](includes/prod_short.md)]-síðu sem er bætt við samtal í Teams. Upplýsingar um birtingu vefþjónustu er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).

- <a name="permissions"></a>Aðgangsheimildir notanda:

    Að mestu leyti eru síður og gögn sem notendur geta skoðað og breytt í samtali í Teams stjórnað af heimildum þeirra í [!INCLUDE [prod_short](includes/prod_short.md)].
    
    - Til að líma [!INCLUDE [prod_short](includes/prod_short.md)]-tengil í samtal í Teams og fá hann til að stækka í spjald, verða notendur að minnsta kosti að hafa lesheimild á síðunni og gögnum hennar.
    - Þegar spjald er sent inn í samtal, getur hvaða notandi sem er í því samtali skoðað spjaldið án leyfis frá [!INCLUDE [prod_short](includes/prod_short.md)].
    - Til að skoða frekari upplýsingar um spjald eða opna færsluna í [!INCLUDE [prod_short](includes/prod_short.md)], verða notendur að hafa lesheimild á síðunni og gögnum hennar.
    - Til að breyta gögnum þarf notandi að breyta heimildum.
    
    Frekari upplýsingar um heimildir er að finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Umsjón með persónuvernd og reglufylgni 

Microsoft Teams býður upp á víðtæka stjórnun fyrir reglufylgni og umsjón með viðkvæmum eða persónugreinanlegum gögnum&mdash;þar á meðal gögnum sem bætt er við spjall og rásir af [!INCLUDE [prod_short](includes/prod_short.md)]-forritinu.

### <a name="understanding-where-prod_short-cards-are-stored"></a>Að skilja hvar [!INCLUDE [prod_short](includes/prod_short.md)]-spjöld eru geymd 

Eftir að kort hefur verið sent á spjall er kortið og reitirnir á kortinu afritaðir í Teams. Þessar upplýsingar heyra undir reglur Teams fyrir fyrirtækið þitt, svo sem reglur um gagnavarðveislu. Þegar upplýsingar spjalds birtast eru engin gögn í uppplýsingaglugganum geymd í Teams. Gögnin eru áfram geymd í [!INCLUDE [prod_short](includes/prod_short.md)] og verða aðeins sótt af Teams þegar notandinn velur að skoða upplýsingarnar. 

- Frekari upplýsingar um hvar Teams geymir þessi gögn er að finna í [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Frekari upplýsingar um varðveislureglur í Teams er að finna í [Varðveislureglur í Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Takmörkun á deilingu spjalda 

Þú kemur í veg fyrir að ákveðnir notendur eða hópar sendi spjöld á spjall eða rásir með því að setja upp reglu um skilaboð sem slekkur á stillingunni **Forskoðun vefslóða**. Frekari upplýsingar um þessa stillingur er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams). 

Einnig er hægt að nota upplýsingatálma til að koma í veg fyrir að einstaklingar eða hópar séu í samskiptum. Frekari upplýsingar er að finna í [Upplýsingatálmar í Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Eiginleika gagnatapsvarnar í öryggis- og reglufylgnimiðstöð Microsoft 365 er ekki hægt að nota sérstaklega fyrir spjöld. En hægt er að nota þau í spjallskilaboðunum sem innihalda kortin. Til að rekja væntanlega ítarlega eiginleika sem fela í sér að virkja gagnatapsvörn fyrir spjöld er að finna í [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).

### <a name="responding-to-data-requests"></a>Bregðast við gagnabeiðnum

Hægt er að leyfa teymismeðlimum og eigendum hópa að eyða skilaboðum sem innihalda viðkvæm spjöld með því að setja upp skilaboðareglur eins og: **Eigendur geta eytt sendum skilaboðum** og **Notendur geta eytt sendum skilaboð**. Frekari upplýsingar er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams).

Eftirlitseiginleika efnisleitar og eDiscovery í öryggis- og reglufylgnimiðstöð Microsoft 365 er ekki hægt að nota sérstaklega á spjöld. En hægt er að nota þau í spjallskilaboðunum sem innihalda kort. Til að rekja væntanlega eftirlitseiginleika fyrir spjöld skal skoða [https://www.microsoft.com/microsoft-365/roadmap?featureid=68875](https://www.microsoft.com/microsoft-365/roadmap?featureid=68875).

Þar sem gögn spjalds í Teams er afrit af gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] er einnig hægt að nota [!INCLUDE [prod_short](includes/prod_short.md)]-eiginleika til að flytja út gögn viðskiptamanna ef þess er óskað. Frekari upplýsingar um persónuvernd í [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Algengar spurningar um persónuvernd fyrir viðskiptamenn Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Sjá einnig
[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Teams - Algengar spurningar](teams-faq.md)  
[Úrræðaleit Teams](admin-teams-troubleshooting.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
