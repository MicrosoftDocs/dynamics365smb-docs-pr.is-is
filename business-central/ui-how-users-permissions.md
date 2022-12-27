---
title: Búa til notendur samkvæmt leyfum
description: Lýsir því hvernig skal bæta notendum við Business Central á netinu eða á staðnum samkvæmt leyfum.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173
ms.date: 05/09/2022
ms.author: edupont
ms.openlocfilehash: 77a58c9e4cfc5e9a744d66d0f6b62c06cb430d6b
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/09/2022
ms.locfileid: "8729802"
---
# <a name="create-users-according-to-licenses"></a>Búa til notendur samkvæmt leyfum

Í þessari grein er því lýst hvernig stjórnendur búa til notendur og skilgreina hverjir geta skráð sig inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Í þessari grein er einnig fjallað um úthlutun heimilda til mismunandi tegunda notenda í samræmi við vöruleyfin þín.

Þegar notendur eru búnir til í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að úthluta þeim heimildum í gegnum heimildasamstæður og raða notendum í notendaflokka. Notendaflokkar auðvelda stjórnun heimilda fyrir marga notendur á sama tíma. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

Frekari upplýsingar um mismunandi gerðir leyfa og hvernig leyfi virka í [!INCLUDE[prod_short](includes/prod_short.md)] fást með því að sækja [leyfishandbók Dynamics 365-](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Ferlið við að stjórna notendum og leyfum er mismunandi eftir því hvort [!INCLUDE[prod_short](includes/prod_short.md)] er sett upp á netinu eða innanhúss. Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu þarf að bæta við notendum úr Microsoft 365. Í uppsetningum á staðnum er hægt að búa til, breyta og eyða notendum beint.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Stjórna notendum og leyfum í leigjendum á netinu

Áskrift þín að [!INCLUDE[prod_short](includes/prod_short.md)] á netinu skilgreinir þann fjölda notenda sem þú hefur leyfi fyrir. Notendum er bætt við leigjandann í miðstöð Microsoft-samstarfsaðila, yfirleitt af samstarfsaðila þínum hjá Microsoft. Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Þú úthlutar vöruleyfum til notenda samkvæmt vinnunni sem hver notandi gerir í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að úthluta leyfum á nokkra vegu:

- Microsoft 365 Stjórnandi fyrirtækisins þíns getur gert það í [Microsoft 365 Admin Center](https://admin.microsoft.com). Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Samstarfsaðili Microsoft getur úthlutað leyfum í stjórnendamiðstöð Microsoft 365 eða í Microsoft Partner Center. Frekari upplýsingar er að finna í [Stjórnunarverk notanda fyrir viðskiptamannalykla](/partner-center/assign-licenses-to-users) í hjálp Microsoft Partner Center.

Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp stjórnenda.

> [!NOTE]
> Eftir að þú hefur bætt við notendum í Microsoft 365 stjórnendamiðstöðinni er mælt með að uppfæra notandaupplýsingarnar í [!INCLUDE[prod_short](includes/prod_short.md)] sem fyrst. Það er auðvelt að halda núverandi upplýsingum um notendur uppfærðum og tryggir líka að fólk geti alltaf skráð sig inn. Frekari upplýsingar eru í [Að bæta við notendum eða uppfæra notandaupplýsingar og úthlutunum leyfa í Business Central](#adduser).<br>
>
> Það er sérstaklega mikilvægt að uppfæra notandaupplýsingar ef þú hefur sérstillt heimildasamstæður fyrir leyfið. Ef nýr notandi reynir að skrá sig inn í [!INCLUDE[prod_short](includes/prod_short.md)] áður en þú hefur bætt honum við er ekki víst að hann geti það. Sjá [Stilla uppruna miðað við heimildir](#licensespermissions) fyrir frekari upplýsingar.
>
> Notendur sem lenda í þessu vandamáli eru hins vegar ekki útilokaðir. Þeir geta annaðhvort notað aðgerðina **Fara aftur á upphafssíðu** eða einfaldlega skráð sig inn aftur til að leysa vandamálið.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Frekari upplýsingar eru í [Úthlutaður stjórnendaaðgangur að Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a>Grunnstilla heimildir út frá leyfum

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Stjórnendur geta grunnstillt heimildasamstæður og notendaflokka út frá mismunandi leyfisgerðum.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Til dæmis er algengasta leyfið, *Dynamics 365 Business Central teymismeðlimur*, með notendaflokkana *D365 teymismeðlimur* og *Excel-útflutningsaðgerð* auk eftirfarandi heimildasamstæða sjálfgefið:

- D365 UPPLÝSINGAR
- D365-TEYMISMEÐLIMUR
- BREYTA Í EXCEL – SKOÐA
- FLYTJA ÚT SKÝRSLU Í EXCEL.
- STAÐBUNDIÐ

Ef þessi sjálfgefna stilling er ekki rétt uppsetning fyrir tiltekinn leigjanda getur stjórnandi breytt þessari stillingu. Hins vegar hafa sérsniðnar heimildir aðeins áhrif á nýja notendur sem fá það leyfi úthlutað. Þetta hefur ekki áhrif á heimildir fyrir núverandi notendur sem hafa fengið leyfið úthlutað.  

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Grunnstilling leyfis** og velja síðan viðkomandi tengil.  

    Að öðrum kosti, ef þú ert þegar á síðunni **Notendur**, geturðu keyrt leiðsögnina **Uppfæra notendur úr Microsoft 365** og síðan á fyrstu síðu leiðsagnarinnar geturðu valið tengilinn **Grunnstilla heimildir fyrir hvert leyfi**.  
3. Á síðunni **Grunnstilling leyfis** skaltu velja leyfið sem á að sérsníða og síðan velja aðgerðina **Grunnstilla**.  
4. Veldu reitinn **Sérsníða heimildir** til að kveikja á sérstillingu og gerðu síðan viðeigandi breytingar.  

    Í dæminu okkar vill stjórnandinn fjarlægja heimildina til að breyta í Excel, þannig að hann fjarlægir notendaflokkinn *Excel-útflutningsaðgerð* úr Team Member-leyfinu. Áfram munu nýir notendur sem fá úthlutað Team Member-leyfi ekki fá möguleika á að flytja gögn út í Excel. Ef fyrirtækið skiptir um skoðun um efnið getur það farið til baka á síðuna **Grunnstilling leyfis** og slökkt á sérstillingu fyrir þá leyfisgerð.  

> [!IMPORTANT]
> Þessi sérstilling á heimildum tekur aðeins gildi fyrir nýja notendur sem þú úthlutar viðeigandi leyfi. Núverandi notendur eru ekki uppfærðir. Mælt er með því að sérsníða heimildir áður en þú úthlutar notendum leyfum í Microsoft 365 stjórnendamiðstöðinni.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Að bæta við notendum eða uppfæra notandaupplýsingar og úthlutunum leyfa í Business Central

Þegar notendum er bætt við eða notandaupplýsingum er breytt í stjórnendamiðstöð Microsoft 365 er hægt að flytja notandaupplýsingarnar á fljótlegan hátt inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Innflutningurinn inniheldur leyfisúthlutanir.  

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.  
3. Veldu **Uppfæra notendur úr Microsoft 365**.

Fyrir nýja notendur er næsta skref að úthluta notendaflokkum og heimildum. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md). Ef notandaupplýsingar eru uppfærðar og uppfærslan felur í sér breytingu á leyfi, verður notendum úthlutað á viðeigandi notendaflokk og heimildasamstæður þeirra verða uppfærðar. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md).  

> [!NOTE]
> Úthluta verður öllum notendum sama leyfi í umhverfi, annaðhvort Essential eða Premium. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Frekari upplýsingar um samstillingu notandaupplýsinga við Microsoft 365 er að finna í hlutanum [Samstilling við Microsoft 365](#m365).

> [!NOTE]
> Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt Business Central svo þeir geti unnið með þín fjárhagsgögn. Frekari upplýsingar eru í [Bjóða ytri endurskoðanda í þitt Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Til að fjarlægja aðgang notanda að kerfinu

Hægt er að fjarlægja aðgang notanda að [!INCLUDE[prod_short](includes/prod_short.md)]. Allar tilvísanir í notandann eru geymdar. Notandinn getur hins vegar ekki skráð sig inn og virkar lotur fyrir notandann eru stöðvaðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Opnaðu síðuna **Notandaspjald** fyrir viðkomandi notanda og síðan, í reitnum **Staða** skal velja **Óvirkt**.
3. Til að veita notandanum aðgang aftur skal stilla reitinn **Staða** á **Virkt**.

Auk þess er hægt að taka leyfið af notanda í Microsoft 365 stjórnendamiðstöðinni. Þá getur notandinn ekki skráð sig inn. Nánari upplýsingar er að finna í [Leyfi tekin af notendum](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Samstilling við Microsoft 365

Þegar notanda er úthlutað leyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Microsoft 365 eru tvær leiðir til að búa notandann til í [!INCLUDE[prod_short](includes/prod_short.md)].  

- Stjórnandi getur bætt notandanum við með því að velja **Uppfæra notendur úr Microsoft 365** aðgerðina á síðunni **Notendur** eins og lýst er í hlutanum [Að bæta við notanda eða uppfæra notandaupplýsingar í Business Central](#adduser).
- Leyfisupplýsingar uppfærast sjálfkrafa þegar notandinn skráir sig inn í fyrsta skipti.

Í báðum tilfellum eru nokkrar stillingar gerðar sjálfkrafa. Þessar stillingar eru taldar upp í öðrum og þriðja dálkinum í töflunni hér að neðan.

Ef notandaupplýsingum er breytt í Microsoft 365 er hægt að uppfæra [!INCLUDE[prod_short](includes/prod_short.md)] til að endurspegla breytinguna. Eftir því hvað á að uppfæra er hægt að velja eina af aðgerðunum á síðunni **Notendur**. Aðgerðunum er lýst í síðustu þremur dálkunum í töflunni hér að neðan.

> [!NOTE]
> Aðgerðunum sem lýst er í eftirfarandi töflu eru nákvæmar, en sú eina sem þú þarft er **Uppfæra notendur úr Microsoft 365** sem var bætt við til að einfalda ferlið. Hinar aðgerðirnar verða fjarlægðar í næstu útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)].

|Hvað gerist ef:|Fyrsti notandi, fyrsta innskráning|Fá notendur frá Microsoft 365|Uppfæra notendur úr Microsoft 365|Endurheimta sjálfgefna notendahópa notanda|Uppfæra notendahópa|Uppfæra notandaupplýsingar frá Microsoft 365|
|-|-|-|-|-|-|-|
|Umfang:|Núverandi notandi|Nýir notendur í Microsoft 365|Margir notendur valdir|Einn notandi valinn  (fyrir utan núverandi)|Margir notendur valdir|Margir notendur valdir|
|Bættu við nýjum notanda og úthlutaðu SUPER heimildasamstæðu.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Uppfærðu notandann í samræmi við upplýsingar í Microsoft 365: Staða, fullt nafn, netfang tengiliðs, sannvottunarpóstur.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Samstilltu notendaáskriftir (leyfi) með leyfum og hlutverkum sem eru úthlutuð í Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Bættu notandanum við notendaflokka í samræmi við notendaáskriftir. Fjarlægja skal SUPER-heimildasamstæðuna fyrir alla notendur nema þann fyrsta sem skráir sig inn og [stjórnendur](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Velja þarf a.m.k. eitt SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Fjarlægir handvirkt úthlutuðum notendaflokkum og heimildum.|**X**<br /><br />Uppfæra úthlutunum notendaflokks.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Umsjón með notendum og leyfum í uppsetningu innanhúss

Fyrir uppsetningu á staðnum er fjöldi notandaleyfa tilgreindur í leyfisskránni (.flf). Þegar stjórnandi eða Microsoft-samstarfsaðili hleður upp leyfisskránni geta þeir tilgreint hvaða notendur geta skráð sig inn á [!INCLUDE[prod_short](includes/prod_short.md)].

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
[Leyfisveitingar í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Bæta notendum við Microsoft 365 fyrir fyrirtæki](/microsoft-365/admin/add-users/add-users)  
[Öryggi og vernd í Business Central (efni stjórnenda)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Úthluta notendum auðkenni fyrir fjarmælingu](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]