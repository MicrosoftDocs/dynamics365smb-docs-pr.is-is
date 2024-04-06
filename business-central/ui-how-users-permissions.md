---
title: Búa til notendur samkvæmt leyfum
description: Lýsir því hvernig skal bæta notendum við Business Central á netinu eða á staðnum samkvæmt leyfum.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 02/21/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-users-according-to-licenses"></a>Stofna notendur samkvæmt leyfum

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Í þessari grein er því lýst hvernig stjórnendur búa til notendur og skilgreina hverjir geta skráð sig inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú munt einnig læra hvernig á að úthluta mismunandi notendum heimildum samkvæmt vöruleyfunum.

Þegar notendur eru stofnaðir í [!INCLUDE[prod_short](includes/prod_short.md)] er þeim veitt heimildir með heimildarmengum. Einnig er hægt að skipuleggja notendur í notendaflokkum. Notendaflokkar auðvelda umsjón með heimildum og öðrum stillingum margra notenda samtímis. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

Frekari upplýsingar um mismunandi gerðir leyfa og hvernig leyfi virka í [!INCLUDE[prod_short](includes/prod_short.md)] fást með því að sækja [leyfishandbók Dynamics 365-](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Ferlið við að stjórna notendum og leyfum er mismunandi eftir því hvort [!INCLUDE[prod_short](includes/prod_short.md)] er sett upp á netinu eða innanhúss. Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu þarf að bæta við notendum úr Microsoft 365. Í uppsetningum á staðnum er hægt að búa til, breyta og eyða notendum beint.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Stjórna notendum og leyfum í leigjendum á netinu

Fyrst verður að stofna notendareikninga í [!INCLUDE[prod_short](includes/prod_short.md)]  Microsoft 365 stjórnunarstöðinni. Þessir notendareikningar eru ekki undanskildir [!INCLUDE [prod_short](includes/prod_short.md)]. Ef þú gerast áskrifandi að öðrum áætlunum er hægt að nota þær til að skrá þær inn í önnur forrit, t.d Power BI.. Upplýsingar um stofnun notenda í Microsoft 365 stjórnunarmiðstöðinni [fást í Bæta við notendum í stjórnunarmiðstöð Microsoft](/microsoft-365/admin/add-users/add-users).

Áskriftin þín til að [!INCLUDE[prod_short](includes/prod_short.md)] á netinu skilgreinir hversu mörg [!INCLUDE[prod_short](includes/prod_short.md)] notendaleyfi þú hefur leyfi. Notendum er bætt við leigjandann í miðstöð Microsoft-samstarfsaðila, yfirleitt af samstarfsaðila þínum hjá Microsoft. Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Notendum er úthlutað leyfi samkvæmt vinnunni sem hver notandi vinnur í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að úthluta leyfum á nokkra vegu:

- Microsoft 365 Stjórnandi fyrirtækisins þíns getur gert það í [Microsoft 365 Admin Center](https://admin.microsoft.com). Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Samstarfsaðili Microsoft getur úthlutað leyfum í stjórnendamiðstöð Microsoft 365 eða í Microsoft Partner Center. Frekari upplýsingar er að finna í [Stjórnunarverk notanda fyrir viðskiptamannalykla](/partner-center/assign-licenses-to-users) í hjálp Microsoft Partner Center.

Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp stjórnenda.

Þegar notendareikningar hafa verið stofnaðir í Microsoft 365 stjórnunarstöðinni eru tvær leiðir til að flytja þá inn í [!INCLUDE [prod_short](includes/prod_short.md)]:

- Notandareikningur er sjálfkrafa fluttur inn þegar notandi skráir sig inn í [!INCLUDE [prod_short](includes/prod_short.md)] fyrsta skipti.

   > [!NOTE]
   > Þegar notandi hefur skráð sig inn á netið er ekki hægt að [!INCLUDE [prod_short](includes/prod_short.md)] eyða notandanum.

- Stjórnandinn getur flutt inn notendur með því að **velja Uppfæra notendur úr Microsoft 365** aðgerð á síðunni **Notendur* .

Báðar aðferðir hafa sína eigin kosti og hægt er að nota þær samtímis. Hver nálgun gerir stjórnendum kleift að grunnstilla [!INCLUDE [prod_short](includes/prod_short.md)] á gagnvirkan hátt til að úthluta upphafsheimildum, notendaflokkum og notendaforstillingum.  **Með því að nota Uppfæra notendur úr Microsoft 365** aðgerð gefur stjórnendum meiri stjórntæki til að breyta heimildum, notendaflokkum og forstillingum. Það er tilvalin nálgun þegar verið er að setja upp [!INCLUDE [prod_short](includes/prod_short.md)] í fyrsta skipti, áður en einhverjir notendur skrá sig inn eða þegar nýju teymi notenda er bætt við.

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

Stjórnendur geta grunnstillt heimildasafn og notendaflokka fyrir hvert leyfi.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Til dæmis er leyfið sem almennt er notað, *Dynamics 365 Business Central  Teymismeðlimur* sjálfgefið:

- D365 UPPLÝSINGAR
- D365-TEYMISMEÐLIMUR
- BREYTA Í EXCEL – SKOÐA
- FLYTJA ÚT SKÝRSLU Í EXCEL.
- STAÐBUNDIÐ

Öðrum heimildasamstæðum er sjálfkrafa bætt við samkvæmt notendaflokkunum sem úthlutað hefur verið á leyfið. Þegar nýr notandi er stofnaður út frá þessu leyfi, [!INCLUDE[prod_short](includes/prod_short.md)]  úthlutar heimildarmengunum úr notendaflokkunum og heimildin setur úr leyfinu. Sömu upphafsheimildum er úthlutað á notandann ef notandareikningur þeirra var stofnaður sjálfvirkt eða [!INCLUDE[prod_short](includes/prod_short.md)] ef stjórnandinn notaði aðgerðina **Uppfæra notendur frá Microsoft 365** aðgerð á síðunni **Notendur** .

Ef þessi sjálfgefna grunnstilling er ekki rétt uppsetning fyrir tiltekið umhverfi getur stjórnandi breytt þeirri grunnstillingu. Hins vegar hafa sérsniðnar heimildir aðeins áhrif á nýja notendur sem fá það leyfi úthlutað. Þetta hefur ekki áhrif á heimildir fyrir núverandi notendur sem hafa fengið leyfið úthlutað.  

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Grunnstilling leyfis** og velja síðan viðkomandi tengil.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. Á síðunni **Grunnstilling leyfis** skaltu velja leyfið sem á að sérsníða og síðan velja aðgerðina **Grunnstilla**.  
4. Veldu reitinn **Sérsníða heimildir** til að kveikja á sérstillingu og gerðu síðan viðeigandi breytingar.  

    Í dæminu okkar vill stjórnandinn fjarlægja heimildina til að breyta í Excel, þannig að hann fjarlægir notendaflokkinn *Excel-útflutningsaðgerð* úr Team Member-leyfinu. Áfram munu nýir notendur sem fá úthlutað Team Member-leyfi ekki fá möguleika á að flytja gögn út í Excel. Ef fyrirtækið skiptir um skoðun um efnið getur það farið til baka á síðuna **Grunnstilling leyfis** og slökkt á sérstillingu fyrir þá leyfisgerð.  

> [!IMPORTANT]
> Þessi sérstilling heimilda tekur aðeins gildi fyrir nýja notendur sem úthlutað er viðeigandi leyfi. Núverandi notendur eru ekki uppfærðir. Mælt er með því að sérsníða heimildir áður en þú úthlutar notendum leyfum í Microsoft 365 stjórnendamiðstöðinni.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Að bæta við notendum eða uppfæra notandaupplýsingar og úthlutunum leyfa í Business Central

Þegar notendum er bætt við eða notandaupplýsingum er breytt í stjórnendamiðstöð Microsoft 365 er hægt að flytja notandaupplýsingarnar á fljótlegan hátt inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Innflutningurinn inniheldur leyfisúthlutanir.  

> [!TIP]
> Ef uppfæra þarf notandaupplýsingar og margir notendur eru til er hægt að nota afmörkunarsvæðið til að þrengja listann. Hægt er að afmarka eftir grunnupplýsingum eins og notandanafni eða setja fleiri tæknilegar afmarkanir, svo sem öryggiskenni notandans.

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.  
3. Veldu **Uppfæra notendur úr Microsoft 365**.

> [!IMPORTANT]  
> Þegar samstilling notenda er keyrð með Microsoft 365 því að nota **leiðbeiningarnar Uppfæra notendur úr Microsoft 365** leiðsagnarforritinu þarf SUPER-heimildarsafnið.

> [!NOTE]
> Uppfærir **notendur úr Microsoft 365** handbókinni uppfærir ekki notendur sem ekki hafa fengið leyfi, t.d. einhver sem er altækur stjórnandi og Dynamics 365 Admin. Þessir notendur uppfærast næst þegar þeir skrá sig inn í umhverfið.

Næsta skref fyrir nýstofnaða notendur er að úthluta notendaflokkum og heimildum. Farið í [Úthlutun heimilda til notenda og hópa](ui-define-granular-permissions.md) fyrir upplýsingar. Ef notandi er uppfærður og uppfærslan inniheldur leyfisbreytingu er notendum úthlutað til viðeigandi notendaflokks og heimildasafn þeirra eru uppfærð. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md).  

> [!NOTE]
> Öllum notendum í umhverfi þarf að fá sama leyfi, annaðhvort Grundvallaratriði eða Premium. Frekari upplýsingar um leyfisveitingar er að finna á [heimasíðu Business Central](https://dynamics.microsoft.com/business-central/overview/) .

Nánari upplýsingar um samstillingu notendaupplýsinga eru Microsoft 365 í hlutanum [Samstilling með Microsoft 365](#m365) kaflanum.

> [!NOTE]
> Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt [!INCLUDE[prod_short](includes/prod_short.md)] svo þeir geti unnið með þín fjárhagsgögn. Frekari upplýsingar eru í [Bjóða ytri endurskoðanda í þitt Business Central](finance-accounting.md#inviteaccountant).

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

Í báðum tilvikum eru nokkrar stillingar notaðar sjálfkrafa. Þessar stillingar eru taldar upp í öðrum og þriðja dálkinum í töflunni hér að neðan.

Ef notandaupplýsingum er breytt í Microsoft 365 er hægt að uppfæra [!INCLUDE[prod_short](includes/prod_short.md)] til að endurspegla breytinguna. Eftir því hvað á að uppfæra er hægt að velja eina af aðgerðunum á síðunni **Notendur**. Aðgerðunum er lýst í síðustu tveimur dálkunum í töflunni að neðan.

|Hvað gerist ef:|Fyrsti notandi, fyrsta innskráning|Uppfæra notendur úr Microsoft 365|Endurheimta sjálfgefna notendahópa notanda|
|-|-|-|-|
|Umfang:|Núverandi notandi|Margir notendur valdir|Einn notandi valinn  (fyrir utan núverandi)|
|Bættu við nýjum notanda og úthlutaðu SUPER heimildasamstæðu.<br /><br /><!--Platform-->|**X**|**X** | | 
|Uppfærðu notandann í samræmi við upplýsingar í Microsoft 365: Staða, fullt nafn, netfang tengiliðs, sannvottunarpóstur.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Samstilltu notendaáskriftir (leyfi) með leyfum og hlutverkum sem eru úthlutuð í Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Bættu notandanum við notendaflokka í samræmi við notendaáskriftir. Fjarlægja skal SUPER-heimildasamstæðuna fyrir alla notendur nema þann fyrsta sem skráir sig inn og [stjórnendur](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Velja þarf a.m.k. eitt SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Fjarlægir handvirkt úthlutuðum notendaflokkum og heimildum.|

Notendur geta fengið aðgang að [!INCLUDE[prod_short](includes/prod_short.md)] færslum í Teymum sem nota aðeins leyfi sitt Microsoft 365 . Þegar aðgangur er virkur fyrir umhverfi er samstillt með því að nota **Uppfæra notendur úr Microsoft 365** aðgerð ekki með notendum sem hafa Microsoft 365 aðeins leyfi. Til að taka þessa notendur með í samstillingu þarf fyrst að uppfæra umhverfisstillingar með því að úthluta öryggishópi sem inniheldur notendur með [!INCLUDE[prod_short](includes/prod_short.md)] leyfi og notendur sem hafa aðeins Microsoft 365 leyfi.

Fræðast um að tryggja aðgang að umhverfi með því að nota öryggishópa í [Manage með Microsoft Entra hópum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Fá yfirlit yfir aðgang [!INCLUDE[prod_short](includes/prod_short.md)] í Teymi með Microsoft 365 leyfi á [admin-aðgangi-með-m365-leyfi](admin-access-with-m365-license.md).

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Umsjón með notendum og leyfum í uppsetningu innanhúss

Fyrir virkjun innanhúss er fjöldi notendaleyfa tilgreindur í leyfisskránni (.bclicense eða .flf). Þegar stjórnandi eða Microsoft-samstarfsaðili hleður upp leyfisskránni geta þeir tilgreint hvaða notendur geta skráð sig inn á [!INCLUDE[prod_short](includes/prod_short.md)].

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
