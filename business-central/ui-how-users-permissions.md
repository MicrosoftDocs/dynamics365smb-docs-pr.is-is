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
ms.date: 01/06/2020
ms.author: sgroespe
ms.openlocfilehash: b9fbf0b2793c6239f3a1a416230d4afb17bdb5c6
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943234"
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

Þegar notendur með [!INCLUDE[d365fin](includes/d365fin_md.md)] leyfi hafa verið stofnaðir í Office 365 er hægt að flytja þá inn á **Notendur** síðuna í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því velja aðgerðina **Sækja nýja notendur úr Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Að bæta við notanda í Business Central
Til að bæta notendum frá Microsoft 365 Admin Center við [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu notarðu sérstaka innflutningsaðgerð.  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Veldu **Fá nýja notendur úr Office 365** aðgerðina.

Sérhver nýr notandi sem hefur verið búinn til fyrir Office 365 áskriftina þína verður honum bætt við á síðunni **Notendur**. Notendum er úthlutað heimildasamstæðum samkvæmt leyfi sem úthlutað er til notanda í Office 365. Síðan geturðu haldið áfram að úthluta notendum ítarlegri heimildum og flokka þá í notendahópa til að einfalda þér að úthluta heimildum. Nánari upplýsingar er að finna í [Til að úthluta heimildasamstæðu á notendur](ui-define-granular-permissions.md#to-assign-permission-sets-to-users)

> [!NOTE]
> Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt Business Central svo þeir geti unnið með þín fjárhagsgögn. Frekari upplýsingar eru í [Bjóða ytri endurskoðanda í þitt Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Til að fjarlægja aðgang notanda að kerfinu
Í uppsetningu á netinu er hægt að fjarlægja aðgang notanda að kerfinu með því að stilla reitinn **Staða** á **Óvirkt**. Allar tilvísanir til notandans verða varðveittar, en notandinn getur ekki lengur skráð sig inn í kerfið og virkar lotur fyrir notandann verða stöðvaðar.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Opnaðu síðuna **Notandaspjald** fyrir viðkomandi notanda og síðan, í reitnum **Staða**, skal velja **Óvirkt**.
3. Til að veita notandanum aðgang aftur skal stilla **Ástand** reitinn á **Virkt**.

Auk þess að óvirkja notanda geturðu tekið leyfið af notanda í Microsoft 365 stjórnendamiðstöðinni. Þá getur notandinn ekki skráð sig inn. Nánari upplýsingar er að finna í [Leyfi tekin af notendum](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Til að breyta úthlutuðu leyfi notanda
Stundum gætirðu þurft að breyta leyfi sem er úthlutað til notanda. Ef þú ákveður til dæmis að nota þjónustukerfiseininguna og þarft því að uppfæra allar grunnáskriftir í úrvalsáskriftir. Eða ef ábyrgð notanda hefur breyst og nauðsynlegt er að skipta út Team Members-leyfi fyrir grunnáskrift.

1. Breyttu leyfinu í Microsoft 365 stjórnendamiðstöð. Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Office 365](https://aka.ms/CreateOffice365Users).
2. Skráðu þig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)] sem stjórnandi.
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
4. Á síðunni **Notendur** skaltu velja aðgerðina **Endurhlaða alla notendaflokka**.

Notendurnir verða færðir yfir í viðeigandi notendahóp og heimildasamstæðurnar verða uppfærðar. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Öllum venjulegum notendum í lausn verður að vera veitt sama leyfi, grunn eða úrvals.
> Fyrir upplýsingar um leyfisveitingu, sjá [Microsoft Dynamics 365 Business Central leyfishandbók](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Samstilling við Office 365
Þegar leyfi er úthlutað til notanda í Office 365 eru tvær leiðir til að búa notandann til í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kerfið gerir það sjálfkrafa þegar notandinn skráir sig inn í fyrsta sinn en einnig getur stjórnandi bætt notandanum við með því að velja **Sækja notendur úr Office 365** aðgerðina á síðunni **Notendur**.

Í báðum tilvikum er fjöldi viðbótarstillinga valinn sjálfkrafa. Þessi atriði eru talin upp í öðrum og þriðja dálkinum í töflunni hér að neðan.

Ef þú breytir notandanum í Office 365 eftirá og þarft að samstilla breytingarnar við [!INCLUDE[d365fin](includes/d365fin_md.md)] geturðu notað mismunandi aðgerðir á síðunni **Notendur**, allt eftir því hvað nákvæmlega þú vilt samstilla. Þessi atriði eru talin upp í síðustu þremur dálkunum í töflunni hér að neðan.

|Hvað gerist ef:|Fyrsta innskráning|Fá notendur frá Office 365|Uppfæra notendur úr Office 365|Endurheimta sjálfgefna notendahópa notanda|Uppfæra notendahópa|
|-|-|-|-|-|-|
|Umfang:|Núverandi notandi|Nýir notendur í Office 365|Margir notendur valdir|Einn notandi valinn  (fyrir utan núverandi)|Margir notendur valdir|
|Bættu við nýjum notanda og úthlutaðu SUPER heimildasamstæðu.<br /><br />Kerfi|**X**|**X**| | | |
|Uppfærðu notandafærslu í samræmi við raunverulegar upplýsingar í Office 365: Staða, fullt nafn, netfang tengiliðs, sannvottunarpóstur.<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph|**X**|**X**|**X**|**X**| |
|Samstilltu notendaáskriftir (leyfi) með leyfum og hlutverkum sem eru úthlutuð í Office 365.<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans|**X**|**X**| |**X**|**X**|
|Bættu notandanum við notendaflokka í samræmi við notendaáskriftir. Afturkalla SUPER heimildasamstæðu. Velja þarf a.m.k. eitt SUPER Ekki afturkalla frá [kerfisstjóra](/dynamics365/business-central/dev-itpro/administration/tenant-administration).)<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups|**X**|**X**| |**X**<br /><br />Skrifa yfir: Fjarlægðu notandann úr öðrum hópum. Fjarlægja heimildasamstæður á notendur handvirkt.|**X**<br /><br />Bæta við: Haltu núverandi aðild í notendaflokkunum og úthlutaðu heimildasamstæðunum óbreyttum. Aðeins bæta notanda við hópa ef þörf krefur.|

## <a name="the-device-license"></a>Leyfi tækis
Með Dynamics 365 Business Central tækjaleyfinu geta margir notendur notað tæki sem hefur leyfi samkvæmt tækjaleyfinu til að reka tæki á sölustað, tæki í verslun eða tæki í vöruhúsi. Frekari upplýsingar er að finna í [Microsoft Dynamics 365 Business Central leyfishandbók](https://aka.ms/BusinessCentralLicensing).

Tækjaleyfið er innleitt samkvæmt líkani samhliða notenda. Þegar keyptur er X fjöldi af tækjaleyfum, geta allt að X fjöldi notenda frá tilgreindum hóp sem kallast Dynamics 365 Business Central tækjanotendur* skráð sig inn samtímis.

Stjórnandi Office 365 fyrirtækisins eða samstarfsaðili Microsoft ætti að stofna tilgreindan tækjahóp og bæta tækjanotendum við sem meðlimum þess hóps. Þetta geta hann gert í [Microsoft 365 stjórnendamiðstöðinni](https://admin.microsoft.com/) eða í [Azure-gáttinni](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Takmarkanir tækjanotanda
Notendur með tækjaleyfið geta ekki framkvæmt eftirfarandi verk í [!INCLUDE[d365fin](includes/d365fin_md.md)]:

-   Setja upp vinnslur sem á að keyra sem áætluð verk í verkröðinni. Notendur tækis eru samhliða notendur og því er ekki hægt að tryggja að viðkomandi notandi sé staddur í kerfinu þegar verk er keyrt, sem krafist er.

-   Tækjanotandi getur ekki verið fyrsti notandinn sem skráir sig inn. Notandi af gerðinni stjórnandi, fullur notandi eða ytri endurskoðandi verður að vera sá fyrsti sem skráir sig inn svo hann geti sett upp [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Stjórnendur](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Að stofna Dynamics 365 Business Central hóp tækjanotenda
1.  Í stjórnendamiðstöð Microsoft 365 skal fara á síðuna **Hópar**.
2.  Velja skal aðgerðina **Bæta við hópi**.
3.  Á síðunni **Velja gerð hóps** skal velja aðgerðina **Öryggi** og síðan velja aðgerðina **Bæta við**.
4.  Á síðunni **Grunnur** skal slá inn *Dynamics 365 Business Central tækjanotendur* sem heiti hópsins.

    > [!Note]
    > Heiti flokksins verður að vera stafað nákvæmlega eins og að ofan, einnig í uppsetningu sem ekki er á ensku.
5. Velja hnappinn **Loka**.

> [!NOTE]
> Einnig er hægt að stofna hóp af gerðinni Office 365. Frekari upplýsingar er að finna í [Bera saman hópa](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Bæta meðlimum við hópinn
1.  Í stjórnendamiðstöð Microsoft 365 skal uppfæra síðuna **Hópar** svo að nýju hóparnir birtist.
2.  Velja skal hópinn **Dynamics 365 Business Central tækjanotendur** og síðan aðgerðina **Skoða alla og hafa umsjón með meðlimum**.
3.  Veljið aðgerðina **Bæta við meðlimum**.
4.  Velja skal notendurna sem á að bæta við og síðan velja hnappinn **Vista**.
5.  Veljið hnappinn **Loka** þrisvar sinnum.

Hægt er að bæta við eins mörgum notendum við flokkinn Dynamics 365 Business Central og þörf er á. Fjöldi tækja sem notendur geta skráð sig inn á samtímis fer eftir fjölda keyptra tækjaleyfa.

> [!NOTE]
> Ekki þarf að úthluta [!INCLUDE[d365fin](includes/d365fin_md.md)] -leyfi til notenda sem eru meðlimir í hópi Dynamics 365 Business Central tækisnotenda.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Umsjón með notendum og leyfum í uppsetningu innanhúss
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
