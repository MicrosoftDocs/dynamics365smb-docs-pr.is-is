---
title: Úthluta eða breyta notendaheimild | Microsoft Docs
description: Lýsir því hvernig skal bæta Office 365 notendum við Business Central, og svo úthluta heimildum, aðgangsréttindum og öryggisstillingum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 11/07/2019
ms.author: sgroespe
ms.openlocfilehash: c64a14ed66668f8c3cbe09e8db3430a7dc25db5c
ms.sourcegitcommit: 2a6d629cf290645606356b714a77ef2872bdec64
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2019
ms.locfileid: "2774820"
---
# <a name="create-users-according-to-licenses"></a>Búa til notendur samkvæmt leyfum
Hér á eftir er lýst hvernig þú sem stjórnandi býrð til notendur og skilgreinir hverjir geta skráð sig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)] og hvaða grundvallarréttindi mismunandi notendagerðir eru með samkvæmt leyfum.

Þegar notendur eru búnir til í [!INCLUDE[d365fin](includes/d365fin_md.md)] geturðu haldið áfram að úthluta ákveðnum heimildum til notenda í gegnum heimildasamstæður og til að raða notendum í notendaflokka til að auðvelda heimildastjórnun. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

> [!NOTE]
> Ferlið við að stjórna notendum og leyfum er mismunandi eftir því hvort lausnin er sett upp á netinu eða innanhúss. Í uppsetningum á staðnum er til dæmis aðeins hægt að slökkva og kveikja á notanda þegar honum hefur verið bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í uppsetningum á staðnum er hægt að búa til, breyta og eyða notendum.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Umsjón með notendum og leyfum uppsetningum á netinu
Í [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu er fjöldi notenda skilgreindur eftir áskriftinni og bætt við leigjandann þinn í Microsoft Partner Center, yfirleitt af Microsoft-samstarfsaðila þínum. Frekari upplýsingar er að finna í [Bæta nýjum viðskiptavin við](https://docs.microsoft.com/partner-center/add-a-new-customer) og [Stofna, setja í bið eða segja upp áskriftum viðskiptamanna](https://docs.microsoft.com/partner-center/create-a-new-subscription) í hjálp Microsoft Partner Center.

Til að skilgreina hverjir geta skráð sig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)]verður að úthluta vöruleyfum til notenda í samræmi við þau hlutverk sem þeir munu framkvæma í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta er hægt að gera á eftirfarandi hátt:
- Office 365 Stjórnandi fyrirtækisins þíns getur gert það í [Microsoft 365 Admin Center](https://admin.microsoft.com). Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Office 365](https://aka.ms/CreateOffice365Users).  
- Samstarfsaðili Microsoft getur úthlutað leyfum í stjórnendamiðstöð Microsoft 365 eða í Microsoft Partner Center. Frekari upplýsingar er að finna í [Stjórnunarverk notanda fyrir viðskiptamannalykla](https://docs.microsoft.com/partner-center/assign-licenses-to-users) í hjálp Microsoft Partner Center.

Frekari upplýsingar er að finna í [Stjórnun Business Central á netinu](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp Developer og ITPro.

Þegar notendur með [!INCLUDE[d365fin](includes/d365fin_md.md)] leyfi hafa verið stofnaðir í Office 365 er hægt að flytja þá inn á **Notendur** síðuna í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því velja aðgerðina **Sækja notendur úr Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Að bæta við notanda í Business Central
Til að bæta notendum frá Microsoft 365 Admin Center við [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu notarðu sérstaka innflutningsaðgerð.  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Veldu **Fá notendur frá Office 365** aðgerð.

Sérhver nýr notandi sem hefur verið búinn til fyrir Office 365 áskriftina þína verður honum bætt við á síðunni **Notendur**. Notendum er úthlutað heimildasamstæðum samkvæmt leyfi sem úthlutað er til notanda í Office 365. Síðan geturðu haldið áfram að úthluta notendum ítarlegri heimildum og flokka þá í notendahópa til að einfalda þér að úthluta heimildum. Nánari upplýsingar er að finna í [Til að úthluta heimildasamstæðu á notendur](ui-define-granular-permissions.md#to-assign-permission-sets-to-users)

### <a name="to-remove-a-users-access-to-the-system"></a>Til að fjarlægja aðgang notanda að kerfinu
Í uppsetningu á netinu er hægt að fjarlægja aðgang notanda að kerfinu með því að stilla reitinn **Staða** á **Óvirkt**. Allar tilvísanir til notandans verða varðveittar, en notandinn getur ekki lengur skráð sig inn í kerfið og virkar lotur fyrir notandann verða stöðvaðar.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Opnaðu síðuna **Notandaspjald** fyrir viðkomandi notanda og síðan, í reitnum **Staða**, skal velja **Óvirkt**.
3. Til að veita notandanum aðgang aftur skal stilla **Ástand** reitinn á **Virkt**.

Auk þess að óvirkja notanda geturðu tekið leyfið af notanda í Office 365 stjórnendamiðstöðinni. Þá getur notandinn ekki skráð sig inn. Nánari upplýsingar er að finna í [Leyfi tekin af notendum](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Til að breyta úthlutuðu leyfi notanda
Stundum gætirðu þurft að breyta leyfi sem er úthlutað til notanda. Ef þú ákveður til dæmis að nota þjónustukerfiseininguna og þarft því að uppfæra allar grunnáskriftir í úrvalsáskriftir. Eða ef ábyrgð notanda hefur breyst og nauðsynlegt er að skipta út Team Members-leyfi fyrir grunnáskrift.

1. Breyttu leyfinu í stjórnendamiðstöð Office 365. Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Office 365](https://aka.ms/CreateOffice365Users).
2. Skráðu þig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)] sem stjórnandi.
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
4. Á síðunni **Notendur** skaltu velja aðgerðina **Endurhlaða alla notendaflokka**.
Notendurnir verða færðir yfir í viðeigandi notendahóp og heimildasamstæðurnar verða uppfærðar. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Öllum venjulegum notendum í lausn verður að vera veitt sama leyfi, grunn eða úrvals.
> Fyrir upplýsingar um leyfisveitingu, sjá [Microsoft Dynamics 365 Business Central leyfishandbók](https://aka.ms/BusinessCentralLicensing).

## <a name="managing-users-and-licenses-in-online-deployments"></a>Umsjón með notendum og leyfum uppsetningum á netinu
Fyrir uppsetningu á staðnum er fjöldi notenda með leyfi tilgreindur í leyfisskránni (.flf). Þegar stjórnandi eða Microsoft-samstarfsaðili hleður upp leyfisskránni getur stjórnandinn tilgreint hvaða notendur geta skráð sig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)].

Fyrir uppsetningar innanhúss býr stjórnandinn til, breytir og eyðir notendum beint af síðunni **Notendur**.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Til að breyta eða eyða on-premises notanda
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Velja skal notandann sem á að breyta og velja síðan aðgerðina **Breyta**.
3. Á síðunni **Notandaspjald** skal breyta upplýsingunum eftir þörfum.    
4. Til að eyða notanda, skal velja notandann sem á að eyða og veljið síðna aðgerðina **Eyða**.

> [!NOTE]
> Fyrir uppsetningu á staðnum fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] getur stjórnandi valið á milli mismunandi auðkenningarbúnaðs skilríkja fyrir notendur. Þegar þú býrð til notanda gefur þú síðan mismunandi upplýsingar eftir því hvaða skilríki þú notar í tilteknu [!INCLUDE[server](includes/server.md)] tilviki.<br /><br />
> Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í stjórnunarhluta þróunaraðila og ITPro efni fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Sjá einnig
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Sérstillir [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Bæta notendum við Office 365 fyrir fyrirtæki](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central Leyfishandbók](https://aka.ms/BusinessCentralLicensing)  
[Öryggi og vernd í Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) í Developer og ITPro hjálp
