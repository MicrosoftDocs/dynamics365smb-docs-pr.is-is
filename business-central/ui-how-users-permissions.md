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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/09/2022
ms.locfileid: "8729802"
---
# <a name="create-users-according-to-licenses"></a>Búa til notendur samkvæmt leyfum

Í þessari grein er lýst hvernig kerfisstjórar stofna notendur og skilgreina hverjir geta skráð sig inn [!INCLUDE[prod_short](includes/prod_short.md)]. Í greininni er einnig fjallað um hvernig staðið skuli að úthlutun heimilda til mismunandi notenda samkvæmt virkjunarleyfum.

Þegar notendur eru stofnaðir í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að úthluta heimildum til þeirra með heimildastæðum og skipuleggja notendur í notendaflokkum. Notendaflokkar auðvelda stjórnun heimilda fyrir marga notendur á sama tíma. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

Frekari upplýsingar um mismunandi gerðir leyfa og hvernig leyfi virka í [!INCLUDE[prod_short](includes/prod_short.md)] fást með því að sækja [leyfishandbók Dynamics 365-](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Ferlið við að stjórna notendum og leyfum er mismunandi eftir því hvort [!INCLUDE[prod_short](includes/prod_short.md)] er sett upp á netinu eða innanhúss. Það þarf að bæta notendum við [!INCLUDE [prod_short](includes/prod_short.md)] á netinu Microsoft 365. Í uppsetningum á staðnum er hægt að búa til, breyta og eyða notendum beint.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Umsjón með notendum og leyfum í netverslunum

Áskriftin þín að [!INCLUDE[prod_short](includes/prod_short.md)] netinu skilgreinir fjölda notenda sem er leyfilegt. Notendum er bætt við þinn leigjanda í Microsoft Partner Center, yfirleitt af Microsoft samstarfsaðila. Nánari upplýsingar er að finna [í stjórn Viðskiptasviðs Seðlabanka Íslands](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Notendum er úthlutað leyfum til notenda samkvæmt því starfi sem hver notandi gerir í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að úthluta leyfum með nokkrum hætti:

- Kerfisstjóri fyrirtækisins Microsoft 365 getur gert það í [Microsoft 365 stjórnendamiðstöð](https://admin.microsoft.com). Nánari upplýsingar eru [í bæta við notendum sérstaklega eða að magni til Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Microsoft-félagi getur úthlutað leyfum í Microsoft 365 admin Center eða í Microsoft samstarfsmiðstöðinni. Frekari upplýsingar er að finna í [Stjórnunarverk notanda fyrir viðskiptamannalykla](/partner-center/assign-licenses-to-users) í hjálp Microsoft Partner Center.

Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp stjórnenda.

> [!NOTE]
> Eftir að notendum hefur verið bætt í Microsoft 365 admin Center er mælt með því að uppfæra notendaupplýsingarnar í [!INCLUDE[prod_short](includes/prod_short.md)] eins fljótt og auðið er. Að halda utan um Notandaupplýsingar þetta er auðvelt að gera og hjálpar til við að tryggja að fólk geti alltaf skráð sig inn. Frekari upplýsingar er að finna [í til að bæta við notendum eða uppfæra notendaupplýsingar og leyfisúthlutanir í Viðskiptamiðnum](#adduser).<br>
>
> Uppfærsla á notandaupplýsingum er sérstaklega mikilvæg ef þú hefur sérsniðið heimildasöfn að leyfinu. Ef nýr notandi reynir að skrá sig inn [!INCLUDE[prod_short](includes/prod_short.md)] áður en þeim er bætt við þá er það hugsanlega ekki hægt. Nánari upplýsingar eru [í Configure aðgangsheimildir byggðar á leyfum](#licensespermissions).
>
> Notendur sem upplifa vandann eru hins vegar í raun ekki lokaðir. Þeir geta annað hvort notað **aðgerðina fara aftur heim**, eða einfaldlega skrá sig inn aftur til að leysa málið.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Nánari upplýsingar [fást hjá fulltrúa kerfisstjóra á netinu](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a> Skilgreina heimildir samkvæmt leyfum

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Admins er hægt að samskipa heimildastæðum og notendaflokkum á grundvelli mismunandi leyfistegundum.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Til dæmis er mest notaða leyfið, *Dynamics 365 Business Central teymisaðili*, er með notendaflokka *D365 Team meðlim* og *Excel-útflutningsaðgerð* plús eftirfarandi heimildir stillir sjálfgefið:

- D365 UPPLÝSINGAR
- D365
- BREYTA Í EXCEL-SKOÐA
- ÚTFLUTNINGSSKÝRSLA EXCEL
- SVEITARFÉLAGA

Ef þessi sjálfgefna skilgreining er ekki rétt Uppsetning tiltekins leigjanda getur admin breytt þeirri skilgreiningu. Sérsniðnar heimildir hafa hins vegar aðeins áhrif á nýja notendur sem fá úthlutað því leyfi. Heimildir fyrir þá notendur sem eru tengdar leyfinu verða ekki óbreyttar.  

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Leyfistelling** og veljið síðan tengda tengilinn.  

    Ef þú ert þegar á **síðunni notendur** er hægt að keyra **uppfærslunotendur úr Microsoft 365** leiðbeiningum og svo á fyrstu blaðsíðu leiðbeininganna með því að velja **tengilinn skilgreina heimildir fyrir hvern leyfistengil**.  
3. **Á síðunni um Leyfisskilgreiningar** er valið það leyfi sem á að sérsníða og síðan er **valið aðgerðin skilgreina**.  
4. **Reiturinn sérsníða heimildir** er valinn til að skipta á sérsnið og gera síðan viðeigandi breytingar.  

    Í okkar dæmi vill admin að fjarlægja heimildina til að breyta í Excel, þannig að þau fjarlægi *notendaflokk Excel-útflutnings* úr Team-félagi leyfishafa. Fara fram, nýir notendur sem eru tengdir Team-meðlimurinn leyfi fær ekki möguleika á að flytja út gögn í Excel. Ef skipulagið breytir hugarfari sínu um efni geta þeir svo farið aftur **á síðuna leyfisveiting** og slökkt á sérkennslunum fyrir þá leyfisgerð.  

> [!IMPORTANT]
> Þessi heimild tekur aðeins til gilda fyrir nýja notendur sem viðkomandi leyfi er úthlutað á sérsnið. Fyrirliggjandi notendur eru ekki uppfærðir. Mælt er með að sérsníða heimildir áður en byrjað er að úthluta notendaleyfum í Microsoft 365 admin Center.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Að bæta við notendum eða uppfæra notandaupplýsingar og úthlutunum leyfa í Business Central

Eftir að þú hefur bætt við notendum eða breytt upplýsingum um notanda í Microsoft 365 admin Center er fljótlegt að flytja inn notendaupplýsingar inn á [!INCLUDE[prod_short](includes/prod_short.md)]. Innflutningurinn felur í sér leyfisverkefni.  

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.  
3. Valið **er uppfæra notendur úr Microsoft 365**.

Fyrir nýja notendur er næsta skref að úthluta notendaflokkum og heimildum. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md). Ef Notandaupplýsingar eru uppfærðar og uppfærslan felur í sér breytingu á leyfi, er notendum úthlutað til viðeigandi notendaflokks og heimildir þeirra eru uppfærðar. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md).  

> [!NOTE]
> Öllum notendum í umhverfi verður að vera úthlutað sama leyfi, annað hvort nauðsynlegt eða Premium. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Nánari upplýsingar um samstillingu notendaupplýsinga með Microsoft 365 er að finna í [samstillingarhlutanum Microsoft 365](#m365).

> [!NOTE]
> Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt Business Central svo þeir geti unnið með þín fjárhagsgögn. Frekari upplýsingar eru í [Bjóða ytri endurskoðanda í þitt Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Til að fjarlægja aðgang notanda að kerfinu

Hægt er að fjarlægja aðgang notanda að [!INCLUDE[prod_short](includes/prod_short.md)] netinu. Öllum tilvísunum til notandans er haldið leyndum. Notandinn getur hins vegar ekki skráð sig inn og virkar lotur fyrir notandann.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Opnaðu síðuna **Notandaspjald** fyrir viðkomandi notanda og síðan, í reitnum **Staða** skal velja **Óvirkt**.
3. Til að veita notandanum aðgang aftur skal stilla reitinn **Staða** á **Virkt**.

Einnig er hægt að fjarlægja leyfið frá notanda í Microsoft 365 admin Center. Þá getur notandinn ekki skráð sig inn. Nánari upplýsingar er að finna í [Leyfi tekin af notendum](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a> Samstilling við Microsoft 365

Þegar leyfi [!INCLUDE[prod_short](includes/prod_short.md)] er úthlutað til notanda í Microsoft 365 eru tvær leiðir til að stofna notandann í [!INCLUDE[prod_short](includes/prod_short.md)].  

- Kerfisstjórinn getur bætt notandanum við með því að velja að **Uppfæra notendur úr Microsoft 365** aðgerð á **síðunni notendur** eins og lýst er [í til að bæta við notanda eða uppfæra notendaupplýsingar í miðlægum](#adduser) kafla viðskipta.
- Leyfisupplýsingar uppfærast sjálfkrafa þegar notandinn skráir sig inn í fyrsta skipti.

Í báðum tilvikum eru nokkrar stillingar gerðar sjálfvirkt. Þessar stillingar eru taldar upp í öðrum og þriðja dálkunum í töflunni hér að neðan.

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

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Umsjón með notendum og leyfum í innanhússvirkjanir

Fyrir uppsetningu á staðnum er fjöldi notandaleyfa tilgreindur í leyfisskránni (.flf). Þegar kerfisstjóri eða Microsoft eru að hlaða niður [!INCLUDE[prod_short](includes/prod_short.md)] leyfisskránni geta þeir tilgreint hvaða notendur geta skráð sig inn.

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
[Úthluta notendum telemetrakenni](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]