---
title: Búa til notendur samkvæmt leyfum
description: Lýsir því hvernig skal bæta notendum við Business Central á netinu eða á staðnum samkvæmt leyfum.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9173
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f39067f990c80fad751d251ab4dd7ff038ac0cb2
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148253"
---
# <a name="create-users-according-to-licenses"></a>Búa til notendur samkvæmt leyfum

Í þessari grein er því lýst hvernig stjórnendur búa til notendur og skilgreina hverjir geta skráð sig inn í [!INCLUDE[prod_short](includes/prod_short.md)] og hvaða heimildir eru gefnar mismunandi gerðum notenda samkvæmt leyfunum.

Þegar notendur eru búnir til í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að úthluta þeim ákveðnum heimildum í gegnum heimildasamstæður og raða notendum í notendaflokka. Notendaflokkar auðvelda stjórnun heimilda fyrir marga notendur á sama tíma. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

Frekari upplýsingar um mismunandi gerðir leyfa og hvernig leyfi virka í [!INCLUDE[prod_short](includes/prod_short.md)] fást með því að sækja [leyfishandbók Dynamics 365-](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Ferlið við að stjórna notendum og leyfum er mismunandi eftir því hvort [!INCLUDE[prod_short](includes/prod_short.md)] er sett upp á netinu eða innanhúss. Það þarf að bæta notendum við [!INCLUDE [prod_short](includes/prod_short.md)] á netinu Microsoft 365. Í uppsetningum á staðnum er hægt að búa til, breyta og eyða notendum beint.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Umsjón með notendum og leyfum uppsetningum á netinu

Í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er fjöldi notenda skilgreindur eftir áskriftinni og bætt við leigjandann þinn í Microsoft Partner Center, yfirleitt af Microsoft-samstarfsaðila þínum. Frekari upplýsingar er að finna í [Bæta nýjum viðskiptavin við](/partner-center/add-a-new-customer) og [Stofna, setja í bið eða segja upp áskriftum viðskiptamanna](/partner-center/create-a-new-subscription) í hjálp Microsoft Partner Center.

Til að skilgreina hverjir geta skráð sig inn á [!INCLUDE[prod_short](includes/prod_short.md)] þarf að úthluta vöruleyfum til notenda í samræmi við þau hlutverk sem þeir munu framkvæma í [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta er hægt að gera á eftirfarandi hátt:

- Kerfisstjóri fyrirtækisins Microsoft 365 getur gert það í [Microsoft 365 stjórnendamiðstöð](https://admin.microsoft.com). Nánari upplýsingar eru [í bæta við notendum sérstaklega eða að magni til Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Microsoft-félagi getur úthlutað leyfum í Microsoft 365 admin Center eða í Microsoft samstarfsmiðstöðinni. Frekari upplýsingar er að finna í [Stjórnunarverk notanda fyrir viðskiptamannalykla](/partner-center/assign-licenses-to-users) í hjálp Microsoft Partner Center.

Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp stjórnenda.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Að bæta við notendum eða uppfæra notandaupplýsingar og úthlutunum leyfa í Business Central
Eftir að þú hefur bætt við notendum eða breytt upplýsingum um notanda í Microsoft 365 admin Center er fljótlegt að flytja inn notendaupplýsingar inn á [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta felur í sér leyfisúthlutanir. 

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.  
3. Valið **er uppfæra notendur úr Microsoft 365**.

Ef verið er að bæta við nýjum notendum er næsta skref að úthluta notendaflokkum og heimildum. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md). Ef notandaupplýsingar eru uppfærðar og uppfærslan felur í sér breytingu á leyfi, verður notendum úthlutað til viðeigandi notandaflokks og heimildasamstæður þeirra verða uppfærðar. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md).  

> [!NOTE]
> Úthluta verður öllum notendum sama leyfið, annaðhvort Essential eða Premium. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Nánari upplýsingar um samstillingu notendaupplýsinga með Microsoft 365 er að finna í [samstillingarhlutanum Microsoft 365](#m365).

> [!NOTE]
> Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt Business Central svo þeir geti unnið með þín fjárhagsgögn. Frekari upplýsingar eru í [Bjóða ytri endurskoðanda í þitt Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Til að fjarlægja aðgang notanda að kerfinu

Í uppsetningu á netinu er hægt að fjarlægja aðgang notanda að [!INCLUDE[prod_short](includes/prod_short.md)]. Allar tilvísanir til notandans verða varðveittar, en notandinn getur ekki lengur skráð sig inn í virkar lotur fyrir notandann verða stöðvaðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Opnaðu síðuna **Notandaspjald** fyrir viðkomandi notanda og síðan, í reitnum **Staða** skal velja **Óvirkt**.
3. Til að veita notandanum aðgang aftur skal stilla reitinn **Staða** á **Virkt**.

Einnig er hægt að fjarlægja leyfið frá notanda í Microsoft 365 admin Center. Þá getur notandinn ekki skráð sig inn. Nánari upplýsingar er að finna í [Leyfi tekin af notendum](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a> Samstilling við Microsoft 365

Þegar leyfi [!INCLUDE[prod_short](includes/prod_short.md)] er úthlutað til notanda í Microsoft 365 eru tvær leiðir til að stofna notandann í [!INCLUDE[prod_short](includes/prod_short.md)].  

- Kerfisstjórinn getur bætt notandanum við með því að velja að **Uppfæra notendur úr Microsoft 365** aðgerð á **síðunni notendur** eins og lýst er [í til að bæta við notanda eða uppfæra notendaupplýsingar í miðlægum](#adduser) kafla viðskipta.
- Leyfisupplýsingar uppfærast sjálfkrafa þegar notandinn skráir sig inn í fyrsta skipti.

Í báðum tilvikum er fjöldi stillinga valinn sjálfkrafa. Þessi atriði eru talin upp í öðrum og þriðja dálkinum í töflunni hér að neðan.

Ef notendaupplýsingum er breytt í Microsoft 365 er hægt að uppfæra [!INCLUDE[prod_short](includes/prod_short.md)] til samræmis við breytinguna. Eftir því hvað á að uppfæra er hægt að velja eina af aðgerðunum á síðunni **Notendur**. Aðgerðunum er lýst í síðustu þremur dálkunum í töflunni hér að neðan.

> [!NOTE]
> Þær aðgerðir sem lýst er í eftirfarandi töflu eru þó nákvæmar en það eina sem þarf er **að uppfæra notendur úr Microsoft 365**, sem var bætt við til að einfalda ferlið. Hinar aðgerðirnar verða fjarlægðar í næstu útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)].

|Hvað gerist ef:|Fyrsti notandi, fyrsta innskráning|Fá notendur frá Microsoft 365|Uppfæra notendur úr Microsoft 365|Endurheimta sjálfgefna notendahópa notanda|Uppfæra notendahópa|Uppfæra Notandaupplýsingar frá Microsoft 365|
|-|-|-|-|-|-|-|
|Umfang:|Núverandi notandi|Nýir notendur í Microsoft 365|Margir notendur valdir|Einn notandi valinn  (fyrir utan núverandi)|Margir notendur valdir|Margir notendur valdir|
|Bættu við nýjum notanda og úthlutaðu SUPER heimildasamstæðu.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Uppfærðu notandann á grundvelli upplýsinga í Microsoft 365 : staða, fullt nafn, Netfang tengiliðar, netfang.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Samstilla notendáætlanir (leyfi) með leyfum og hlutverkum sem Microsoft 365 þeim er úthlutað.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Bættu notandanum við notendaflokka í samræmi við notendaáskriftir. Fjarlægja skal SUPER-heimildasamstæðuna fyrir alla notendur nema þann fyrsta sem skráir sig inn og [stjórnendur](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Velja þarf a.m.k. eitt SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Fjarlægir handvirkt úthlutuðum notendaflokkum og heimildum.|**X**<br /><br />Uppfæra úthlutunum notendaflokks.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Umsjón með notendum og leyfum í uppsetningu innanhúss

Fyrir uppsetningu á staðnum er fjöldi notandaleyfa tilgreindur í leyfisskránni (.flf). Þegar stjórnandi eða Microsoft-samstarfsaðili hleður upp leyfisskránni getur stjórnandinn tilgreint hvaða notendur geta skráð sig inn á [!INCLUDE[prod_short](includes/prod_short.md)].

Fyrir uppsetningar innanhúss býr stjórnandinn til, breytir og eyðir notendum beint af síðunni **Notendur**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Til að breyta eða eyða notanda í uppsetningu á staðnum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Velja skal notandann sem á að breyta og velja síðan aðgerðina **Breyta**.
3. Á síðunni **Notandaspjald** skal breyta upplýsingunum eftir þörfum.  
4. Til að eyða notanda, skal velja notandann sem á að eyða og velja síðna aðgerðina **Eyða**.

> [!NOTE]
> Fyrir uppsetningar á staðnum getur stjórnandi tilgreint hvernig á að sannvotta innskráningarupplýsingar notanda í [!INCLUDE[server](includes/server.md)] tilvikinu. Þegar notandi er búinn til er gefin upp gerð innskráningarupplýsinga sem er notuð.
>
> Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í hjálparefni stjórnenda fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Sjá einnig

[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Sérstillir [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Leyfi í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Bæta notendum við Microsoft 365 fyrir viðskipti](/microsoft-365/admin/add-users/add-users)  
[Öryggi og vernd í Business Central (efni stjórnenda)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]