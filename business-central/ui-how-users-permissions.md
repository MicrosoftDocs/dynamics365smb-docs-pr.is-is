---
title: Búa til notendur samkvæmt leyfum
description: Lýsir því hvernig skal bæta notendum við Business Central á netinu eða á staðnum samkvæmt leyfum.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 03/24/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---
# Búa til notendur samkvæmt leyfum

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Í þessari grein er því lýst hvernig stjórnendur búa til notendur og skilgreina hverjir geta skráð sig inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú munt einnig læra hvernig á að úthluta heimildum til mismunandi notenda samkvæmt virkjunarleyfum.

Þegar notendur eru stofnaðir í  [!INCLUDE[prod_short](includes/prod_short.md)] eru Heimildir veittar í gegnum heimildasöfn. Einnig er hægt að skipuleggja notendur í notendahópum. Notendaflokkar gera það auðveldara að stjórna heimildum og öðrum stillingum fyrir marga notendur á sama tíma. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

Frekari upplýsingar um mismunandi gerðir leyfa og hvernig leyfi virka í [!INCLUDE[prod_short](includes/prod_short.md)] fást með því að sækja [leyfishandbók Dynamics 365-](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Ferlið við að stjórna notendum og leyfum er mismunandi eftir því hvort [!INCLUDE[prod_short](includes/prod_short.md)] er sett upp á netinu eða innanhúss. Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu þarf að bæta við notendum úr Microsoft 365. Í uppsetningum á staðnum er hægt að búa til, breyta og eyða notendum beint.  

## Stjórna notendum og leyfum í leigjendum á netinu

Notendareikningar í  [!INCLUDE[prod_short](includes/prod_short.md)]  verður fyrst að stofna í  Microsoft 365  admin Center. Þessir notendareikningar eru ekki einskorðnir [!INCLUDE [prod_short](includes/prod_short.md)]. Ef áskrifandi er að öðrum áætlunum geta þeir nýtt sér þær til innskráningar í aðrar umsóknir, svo sem Power BI. Frekari upplýsingar um stofnun notenda í  Microsoft 365  admin Center er að fara til að  [Bæta við notendum í admin Center](/microsoft-365/admin/add-users/add-users).

Áskrift þín að  [!INCLUDE[prod_short](includes/prod_short.md)]  netinu skilgreinir hversu mörg  [!INCLUDE[prod_short](includes/prod_short.md)]  notendaleyfi eru leyfð. Notendum er bætt við leigjandann í miðstöð Microsoft-samstarfsaðila, yfirleitt af samstarfsaðila þínum hjá Microsoft. Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Leyfum er úthlutað á notendur samkvæmt því starfi sem hver notandi gerir í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að úthluta leyfum á nokkra vegu:

- Microsoft 365 Stjórnandi fyrirtækisins þíns getur gert það í [Microsoft 365 Admin Center](https://admin.microsoft.com). Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Samstarfsaðili Microsoft getur úthlutað leyfum í stjórnendamiðstöð Microsoft 365 eða í Microsoft Partner Center. Frekari upplýsingar er að finna í [Stjórnunarverk notanda fyrir viðskiptamannalykla](/partner-center/assign-licenses-to-users) í hjálp Microsoft Partner Center.

Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp stjórnenda.

Þegar búið er að stofna notendareikninga í  Microsoft 365  admin Center eru tvær leiðir til að flytja þær  [!INCLUDE [prod_short](includes/prod_short.md)] inn:

- Notandareikning er sjálfkrafa fluttur inn þegar notandinn skráir sig inn í  [!INCLUDE [prod_short](includes/prod_short.md)]  fyrsta sinn.

   > [!NOTE]
   > Eftir að  [!INCLUDE [prod_short](includes/prod_short.md)]  notandi skráir sig inn á netið er ekki hægt að eyða notandanum.

- Stjórnandinn getur flutt inn notendur með því að  **Velja uppfæra notendur úr  Microsoft 365**  aðgerð á * *notendur*  síðu.

Báðar nálganir hafa sinn eigin kosti og hægt er að nota þær samtímis. Hver nálgun gerir stjórnendum kleift að samskipa  [!INCLUDE [prod_short](includes/prod_short.md)]  notendum til að úthluta upphafsheimildum, notendaflokkum og notendasniðmát. Með því  **að uppfæra notendur frá  Microsoft 365**  aðgerð gefa stjórnendur fleiri stjórntæki til að leiðrétta heimildir, notendaflokka og forstillingar. Það er tilvalin nálgun þegar verið er að setja upp  [!INCLUDE [prod_short](includes/prod_short.md)]  fyrsta tíma, áður en allir notendur skrá sig inn, eða þegar bætt er við nýjum hópi notenda.

> [!NOTE]
> Eftir að þú hefur bætt við notendum í Microsoft 365 stjórnendamiðstöðinni er mælt með að uppfæra notandaupplýsingarnar í [!INCLUDE[prod_short](includes/prod_short.md)] sem fyrst. Það er auðvelt að halda núverandi upplýsingum um notendur uppfærðum og tryggir líka að fólk geti alltaf skráð sig inn. Frekari upplýsingar eru í [Að bæta við notendum eða uppfæra notandaupplýsingar og úthlutunum leyfa í Business Central](#adduser).<br>
>
> Það er sérstaklega mikilvægt að uppfæra notandaupplýsingar ef þú hefur sérstillt heimildasamstæður fyrir leyfið. Ef nýr notandi reynir að skrá sig inn í [!INCLUDE[prod_short](includes/prod_short.md)] áður en þú hefur bætt honum við er ekki víst að hann geti það. Sjá [Stilla uppruna miðað við heimildir](#licensespermissions) fyrir frekari upplýsingar.
>
> Notendur sem lenda í þessu vandamáli eru hins vegar ekki útilokaðir. Þeir geta annaðhvort notað aðgerðina **Fara aftur á upphafssíðu** eða einfaldlega skráð sig inn aftur til að leysa vandamálið.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Frekari upplýsingar eru í [Úthlutaður stjórnendaaðgangur að Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="licensespermissions"></a>Grunnstilla heimildir út frá leyfum

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Admins er hægt að samskipa heimildastæðum og notendaflokkum fyrir hvert leyfi.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Sem dæmi má nefna að leyfilega,  *Dynamics 365 Business Central  teymisaðili* hefur eftirfarandi heimildir stillir sjálfgefið:

- D365 UPPLÝSINGAR
- D365-TEYMISMEÐLIMUR
- BREYTA Í EXCEL – SKOÐA
- FLYTJA ÚT SKÝRSLU Í EXCEL.
- STAÐBUNDIÐ

Öðrum leyfisstæðum er bætt við sjálfkrafa á grundvelli notendaflokka sem leyfið er úthlutað. Þegar nýr notandi er stofnaður samkvæmt þessu leyfi  [!INCLUDE[prod_short](includes/prod_short.md)]  úthlutar heimildin sér Uppruninn frá notendaflokkum og þeim sem leyfið setur frá leyfi. Sömu upphafsheimildir eru tengdar við notandann ef notandareikninginn þeirra var stofnaður sjálfvirkt í  [!INCLUDE[prod_short](includes/prod_short.md)]  eða ef Stjórnandinn notaði  **uppfærslunotendur úr  Microsoft 365**  aðgerðinni í  **síðunni notendur** .

Ef þessi sjálfgefna skilgreining er ekki rétt Uppsetning fyrir tiltekið umhverfi getur admin breytt þeirri skilgreiningu. Hins vegar hafa sérsniðnar heimildir aðeins áhrif á nýja notendur sem fá það leyfi úthlutað. Þetta hefur ekki áhrif á heimildir fyrir núverandi notendur sem hafa fengið leyfið úthlutað.  

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Grunnstilling leyfis** og velja síðan viðkomandi tengil.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. Á síðunni **Grunnstilling leyfis** skaltu velja leyfið sem á að sérsníða og síðan velja aðgerðina **Grunnstilla**.  
4. Veldu reitinn **Sérsníða heimildir** til að kveikja á sérstillingu og gerðu síðan viðeigandi breytingar.  

    Í dæminu okkar vill stjórnandinn fjarlægja heimildina til að breyta í Excel, þannig að hann fjarlægir notendaflokkinn *Excel-útflutningsaðgerð* úr Team Member-leyfinu. Áfram munu nýir notendur sem fá úthlutað Team Member-leyfi ekki fá möguleika á að flytja gögn út í Excel. Ef fyrirtækið skiptir um skoðun um efnið getur það farið til baka á síðuna **Grunnstilling leyfis** og slökkt á sérstillingu fyrir þá leyfisgerð.  

> [!IMPORTANT]
> Þetta sérsnið tekur aðeins gildi fyrir nýja notendur sem viðkomandi leyfi er úthlutað á. Núverandi notendur eru ekki uppfærðir. Mælt er með því að sérsníða heimildir áður en þú úthlutar notendum leyfum í Microsoft 365 stjórnendamiðstöðinni.

### <a name="adduser"></a>Að bæta við notendum eða uppfæra notandaupplýsingar og úthlutunum leyfa í Business Central

Þegar notendum er bætt við eða notandaupplýsingum er breytt í stjórnendamiðstöð Microsoft 365 er hægt að flytja notandaupplýsingarnar á fljótlegan hátt inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Innflutningurinn inniheldur leyfisúthlutanir.  

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með stjórnandareikningi.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.  
3. Veldu **Uppfæra notendur úr Microsoft 365**.

> [!IMPORTANT]  
> Ef samstilling notenda  Microsoft 365  **Microsoft 365**  er keyrð út frá Guide þarf Super heimildasettið að vera uppsett.

> [!NOTE]
> Að  **Uppfæra notendur úr  Microsoft 365**  leiðbeiningum er ekki uppfært notendum sem ekki fær úthlutað leyfi, eins og einhver sem er alþjóðlegt admin og Dynamics 365 admin. Þeir notendur munu uppfæra næst þegar þeir skrá sig inn í appinu.

Næsta skref fyrir nýstofnaða notendur er að úthluta notendaflokkum og heimildum. Fara í að  [úthluta heimildum til notenda og hópa](ui-define-granular-permissions.md)  til upplýsinga. Ef notandi er að uppfæra notanda og uppfærslan felur í sér breytingar á leyfi, er notendum úthlutað til viðeigandi notendaflokks og heimildir þeirra eru uppfærðar. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md).  

> [!NOTE]
> Öllum notendum í umhverfi verður að vera úthlutað sama leyfi, annaðhvort í meginatriðum eða Premium. Nánari upplýsingar um leyfisveitingar er að fara á  [vefsíðu Viðskiptaráðs](https://dynamics.microsoft.com/business-central/overview/) .

Nánari upplýsingar um samstillingu notendaupplýsinga með  Microsoft 365 er að fara í  [samstillingarhlutann Microsoft 365](#m365) .

> [!NOTE]
> Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt [!INCLUDE[prod_short](includes/prod_short.md)] svo þeir geti unnið með þín fjárhagsgögn. Frekari upplýsingar eru í [Bjóða ytri endurskoðanda í þitt Business Central](finance-accounting.md#inviteaccountant).

### Til að fjarlægja aðgang notanda að kerfinu

Hægt er að fjarlægja aðgang notanda að [!INCLUDE[prod_short](includes/prod_short.md)]. Allar tilvísanir í notandann eru geymdar. Notandinn getur hins vegar ekki skráð sig inn og virkar lotur fyrir notandann eru stöðvaðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Opnaðu síðuna **Notandaspjald** fyrir viðkomandi notanda og síðan, í reitnum **Staða** skal velja **Óvirkt**.
3. Til að veita notandanum aðgang aftur skal stilla reitinn **Staða** á **Virkt**.

Auk þess er hægt að taka leyfið af notanda í Microsoft 365 stjórnendamiðstöðinni. Þá getur notandinn ekki skráð sig inn. Nánari upplýsingar er að finna í [Leyfi tekin af notendum](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="m365"></a>Samstilling við Microsoft 365

Þegar notanda er úthlutað leyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Microsoft 365 eru tvær leiðir til að búa notandann til í [!INCLUDE[prod_short](includes/prod_short.md)].  

- Stjórnandi getur bætt notandanum við með því að velja **Uppfæra notendur úr Microsoft 365** aðgerðina á síðunni **Notendur** eins og lýst er í hlutanum [Að bæta við notanda eða uppfæra notandaupplýsingar í Business Central](#adduser).
- Leyfisupplýsingar uppfærast sjálfkrafa þegar notandinn skráir sig inn í fyrsta skipti.

Í báðum tilvikum eru nokkrar stillingar notaðar sjálfvirkt. Þessar stillingar eru taldar upp í öðrum og þriðja dálkinum í töflunni hér að neðan.

Ef notandaupplýsingum er breytt í Microsoft 365 er hægt að uppfæra [!INCLUDE[prod_short](includes/prod_short.md)] til að endurspegla breytinguna. Eftir því hvað á að uppfæra er hægt að velja eina af aðgerðunum á síðunni **Notendur**. Aðgerðunum er lýst í síðustu tveimur dálkunum í töflunni hér á eftir.

|Hvað gerist ef:|Fyrsti notandi, fyrsta innskráning|Uppfæra notendur úr Microsoft 365|Endurheimta sjálfgefna notendahópa notanda|
|-|-|-|-|
|Umfang:|Núverandi notandi|Margir notendur valdir|Einn notandi valinn  (fyrir utan núverandi)|
|Bættu við nýjum notanda og úthlutaðu SUPER heimildasamstæðu.<br /><br /><!--Platform-->|**X**|**X** | | 
|Uppfærðu notandann í samræmi við upplýsingar í Microsoft 365: Staða, fullt nafn, netfang tengiliðs, sannvottunarpóstur.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Samstilltu notendaáskriftir (leyfi) með leyfum og hlutverkum sem eru úthlutuð í Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Bættu notandanum við notendaflokka í samræmi við notendaáskriftir. Fjarlægja skal SUPER-heimildasamstæðuna fyrir alla notendur nema þann fyrsta sem skráir sig inn og [stjórnendur](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Velja þarf a.m.k. eitt SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Fjarlægir handvirkt úthlutuðum notendaflokkum og heimildum.|

Notendur geta opnað  [!INCLUDE[prod_short](includes/prod_short.md)]  færslur í teymum með því að nota aðeins sitt  Microsoft 365  leyfi. Þegar aðgangur er virkjaður fyrir umhverfi, samstilling með því að  **Uppfæra notendur úr  Microsoft 365**  aðgerð, taka notendur ekki einungis  Microsoft 365  með leyfi. Til að taka þessa notendur með í samstillingu þarf fyrst að uppfæra umhverfisstillingar með því að úthluta öryggisflokki sem inniheldur notendur með  [!INCLUDE[prod_short](includes/prod_short.md)]  leyfi og notendur með aðeins  Microsoft 365  leyfi.

Upplýsingar um tryggja aðgang að umhverfi með því að nota öryggishópa  [með því að stjórna  Microsoft Entra  hópum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Fáðu yfirsýn yfir aðgang  [!INCLUDE[prod_short](includes/prod_short.md)]  í teymum með  Microsoft 365  leyfum at  [admin-aðgangur-með-m365-leyfi](admin-access-with-m365-license.md).

## Umsjón með notendum og leyfum í uppsetningu innanhúss

Fyrir virkjanir innanhúss er fjöldi notendaleyfis tilgreindur í leyfisskránni (. bcleyfi or. flf). Þegar stjórnandi eða Microsoft-samstarfsaðili hleður upp leyfisskránni geta þeir tilgreint hvaða notendur geta skráð sig inn á [!INCLUDE[prod_short](includes/prod_short.md)].

Fyrir uppsetningar innanhúss býr stjórnandinn til, breytir og eyðir notendum beint af síðunni **Notendur**.

### Til að breyta eða eyða notanda í uppsetningu á staðnum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Velja skal notandann sem á að breyta og velja síðan aðgerðina **Breyta**.
3. Á síðunni **Notandaspjald** skal breyta upplýsingunum eftir þörfum.  
4. Til að eyða notanda, skal velja notandann sem á að eyða og velja síðna aðgerðina **Eyða**.

> [!NOTE]
> Fyrir uppsetningar á staðnum getur stjórnandi tilgreint hvernig á að sannvotta innskráningarupplýsingar notanda í [!INCLUDE[server](includes/server.md)] tilvikinu. Þegar notandi er búinn til er gefin upp gerð innskráningarupplýsinga sem er notuð.
>
> Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í hjálparefni stjórnenda fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

## Sjá einnig

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