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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989359"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Stjórnun Microsoft Teams samþættingar við Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Í þessari grein er að finna yfirlit yfir það sem hægt er að gera sem stjórnandi til að stýra Microsoft Teams samþættingu við [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="in-microsoft-teams"></a>Eftir Microsoft Teams

### <a name="minimum-requirements"></a>Lágmarkskröfur

Í þessum hluta er lýst lágmarkskröfum til að eiginleikar [!INCLUDE [prodshort](includes/prodshort.md)]-forritsins virki í Teams.

- Nauðsynleg leyfi

    Eftirfarandi tafla gefur yfirlit yfir leyfin sem þarf til að eiginleikar [!INCLUDE [prodshort](includes/prodshort.md)]-forritsins virki í Teams.

    |Hvað|Teams-leyfi|Business Central-leyfi|
    |----|---|---|
    |Límið tengil við [!INCLUDE [prodshort](includes/prodshort.md)]-færslu í samtal og sendið hann sem spjald.|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|
    |Skoðið spjald [!INCLUDE [prodshort](includes/prodshort.md)]-færslu í samtali.|![gátmerki](media/check.png "ávísun")||
    |Skoðið frekari upplýsingar um spjald fyrir [!INCLUDE [prodshort](includes/prodshort.md)]-færslu í samtali.|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|

- Leyfa forskoðanir vefslóða

    Það verður að vera kveikt á reglustillingunni **Leyfa forskoðanir vefslóða** . Annars verður ekki hægt að búa til spjald fyrir tengla Business Central sem límdir eru í samtal í Teams. Frekari upplýsingar um þessa stillingur er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Stjórnun Business Central (valfrjálst)

Sem stjórnandi í Teams er hægt að stjórna öllum forritum fyrir fyrirtækið, þ.m.t. [!INCLUDE [prodshort](includes/prodshort.md)]-forritinu. Hægt er að samþykkja eða setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir fyrirtækið þitt, útiloka notanda frá því að setja upp forritið og fleira.

Frekari upplýsingar er að finna í eftirfarandi greinum í fylgiskjölum Microsoft Teams:

- [Stjórna forritunum í Microsoft Teams stjórnendamiðstöðinni](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Stjórna uppsetningarreglum forrits í Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>Eftir [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Lágmarkskröfur

- útgáfa [!INCLUDE [prodshort](includes/prodshort.md)]:

    [!INCLUDE [prodshort](includes/prodshort.md)] 2020 útgáfutímabil 2 (útgáfa 17) eða nýrra. Samþætting Teams er aðeins studd fyrir [!INCLUDE [prodshort](includes/prodshort.md)] á netinu; ekki á staðnum.

- Codeunit: **2718 Þjónustuaðili síðusamantektar** er gefin út sem vefþjónusta:

    Þetta codeunit er gefið út sem vefþjónusta að sjálfgefnu. Codeunit er hluti af kerfisforriti [!INCLUDE [prodshort](includes/prodshort.md)]. Það er notað til að sækja reitargögn fyrir [!INCLUDE [prodshort](includes/prodshort.md)]-síðu sem er bætt við samtal í Teams. 

- Aðgangsheimildir notanda:

    Að mestu leyti eru síður og gögn sem notendur geta skoðað og breytt í samtali í Teams stjórnað af heimildum þeirra í [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - Til að líma [!INCLUDE [prodshort](includes/prodshort.md)]-tengil í samtal í Teams og fá hann til að stækka í spjald, verða notendur að minnsta kosti að hafa lesheimild á síðunni og gögnum hennar.
    - Þegar spjald er sent inn í samtal, getur hvaða notandi sem er í því samtali skoðað spjaldið án leyfis frá Business Central.
    - Til að skoða frekari upplýsingar um spjald eða opna færsluna í [!INCLUDE [prodshort](includes/prodshort.md)], verða notendur að hafa lesheimild á síðunni og gögnum hennar.
    - Til að breyta gögnum þarf notandi að breyta heimildum.
    
    Frekari upplýsingar um heimildir er að finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

## <a name="see-also"></a>Sjá einnig
[Business Central og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Hafist handa](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
