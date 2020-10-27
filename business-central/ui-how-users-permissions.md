---
title: Búa til notendur samkvæmt leyfum | Microsoft Docs
description: Lýsir því hvernig skal bæta notendum við Business Central á netinu eða á staðnum samkvæmt leyfum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df34469bc28b081800ddf583e7aa9cf08a15dc27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925648"
---
# <a name="create-users-according-to-licenses"></a>Búa til notendur samkvæmt leyfum

Í þessari grein er því lýst hvernig stjórnendur búa til notendur og skilgreina hverjir geta skráð sig inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] og hvaða heimildir eru gefnar mismunandi gerðum notenda samkvæmt leyfunum.

Þegar notendur eru búnir til í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að úthluta þeim ákveðnum heimildum í gegnum heimildasamstæður og raða notendum í notendaflokka. Notendaflokkar auðvelda stjórnun heimilda fyrir marga notendur á sama tíma. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

> [!NOTE]
> Ferlið við að stjórna notendum og leyfum er mismunandi eftir því hvort [!INCLUDE[d365fin](includes/d365fin_md.md)] er sett upp á netinu eða innanhúss. Fyrir [!INCLUDE [prodshort](includes/prodshort.md)] á netinu þarf að bæta við notendum úr Microsoft 365 . Í uppsetningum á staðnum er hægt að búa til, breyta og eyða notendum beint.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Umsjón með notendum og leyfum uppsetningum á netinu

Í [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu er fjöldi notenda skilgreindur eftir áskriftinni og bætt við leigjandann þinn í Microsoft Partner Center, yfirleitt af Microsoft-samstarfsaðila þínum. Frekari upplýsingar er að finna í [Bæta nýjum viðskiptavin við](/partner-center/add-a-new-customer) og [Stofna, setja í bið eða segja upp áskriftum viðskiptamanna](/partner-center/create-a-new-subscription) í hjálp Microsoft Partner Center.

Til að skilgreina hverjir geta skráð sig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)] þarf að úthluta vöruleyfum til notenda í samræmi við þau hlutverk sem þeir munu framkvæma í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta er hægt að gera á eftirfarandi hátt:

- Microsoft 365 stjórnandi fyrirtækisins þíns getur gert það í [Microsoft 365 Admin Center](https://admin.microsoft.com). Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Microsoft 365](https://aka.ms/CreateOffice365Users).  
- Samstarfsaðili Microsoft getur úthlutað leyfum í stjórnendamiðstöð Microsoft 365 eða í Microsoft Partner Center. Frekari upplýsingar er að finna í [Stjórnunarverk notanda fyrir viðskiptamannalykla](/partner-center/assign-licenses-to-users) í hjálp Microsoft Partner Center.

Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp stjórnenda.

Þegar notendum er úthlutað [!INCLUDE[d365fin](includes/d365fin_md.md)] leyfi í Microsoft 365 er hægt að flytja þá inn í **Notendur** síðuna í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Sækja nýja notendur úr Office 365** .

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Að bæta við notanda eða uppfæra notandaupplýsingar í Business Central

Nota skal sérstaka innflutningsaðgerð til að bæta við nýjum notendum eða uppfæra notandaupplýsingar í [!INCLUDE[d365fin](includes/d365fin_md.md)] úr stjórnendamiðstöð Microsoft 365.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.  
2. Veldu aðgerðina **Uppfæra notendur úr Office 365** .

    Ef þetta er í fyrsta skipti sem þú bætir við notendum úr Microsoft 365, skaltu velja aðgerðina **Ná í nýja notendur úr Office 365** .  
3. Fylgdu skrefunum í leiðarvísinum sem birtist.

Nýjum notendum og notandaupplýsingum í Microsoft 365 áskriftinni þinni verður bætt við á síðunni **Notendur** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nú geturðu úthlutað notendaflokkum og heimildum. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

Frekari upplýsingar um samstillingu notandaupplýsinga við Microsoft 365  er að finna í hlutanum [Samstilling við Microsoft 365](#m365).

> [!NOTE]
> Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt Business Central svo þeir geti unnið með þín fjárhagsgögn. Frekari upplýsingar eru í [Bjóða ytri endurskoðanda í þitt Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-change-the-assigned-license-for-a-user"></a>Til að breyta úthlutuðu leyfi notanda

Stundum gætirðu þurft að breyta leyfi sem er úthlutað til notanda. Ef þú ákveður til dæmis að nota þjónustukerfiseininguna og þarft því að uppfæra allar grunnáskriftir í úrvalsáskriftir. Eða ef ábyrgð notanda hefur breyst og nauðsynlegt er að skipta út Team Members-leyfi fyrir grunnáskrift.

1. Breyttu leyfinu í Microsoft 365 stjórnendamiðstöð. Frekari upplýsingar er að finna í [Bæta stökum notendum eða mörgum í einu við Microsoft 365](https://aka.ms/CreateOffice365Users).
2. Skráðu þig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)] sem stjórnandi.
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
4. Á síðunni **Notendur** skal velja aðgerðina **Endurheimta sjálfgefna notendahópa notanda** .

Notendurnir verða færðir yfir í viðeigandi notendahóp og heimildasamstæðurnar verða uppfærðar. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md).

> [!NOTE]
> Úthluta verður öllum notendum sama leyfið, annaðhvort Essential eða Premium. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

### <a name="to-remove-a-users-access-to-the-system"></a>Til að fjarlægja aðgang notanda að kerfinu

Í uppsetningu á netinu er hægt að fjarlægja aðgang notanda að [!INCLUDE[d365fin](includes/d365fin_md.md)]. Allar tilvísanir til notandans verða varðveittar, en notandinn getur ekki lengur skráð sig inn í virkar lotur fyrir notandann verða stöðvaðar.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Opnaðu síðuna **Notandaspjald** fyrir viðkomandi notanda og síðan, í reitnum **Staða** , skal velja **Óvirkt** .
3. Til að veita notandanum aðgang aftur skal stilla **Ástand** reitinn á **Virkt** .

Auk þess er hægt að taka leyfið af notanda í Microsoft 365 stjórnendamiðstöðinni. Þá getur notandinn ekki skráð sig inn. Nánari upplýsingar er að finna í [Leyfi tekin af notendum](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Samstilla við Microsoft 365

Þegar notanda er úthlutað leyfi fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] í Microsoft 365 eru tvær leiðir til að búa notandann til í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- Stjórnandi getur bætt notandanum við með því að velja **Uppfæra notendur úr Office 365** aðgerðina á síðunni **Notendur** eins og lýst er í hlutanum [Að bæta við notanda eða uppfæra notandaupplýsingar í Business Central](#adduser).
- Leyfisupplýsingar uppfærast sjálfkrafa þegar notandinn skráir sig inn í fyrsta skipti.

Í báðum tilvikum er fjöldi stillinga valinn sjálfkrafa. Þessi atriði eru talin upp í öðrum og þriðja dálkinum í töflunni hér að neðan.

Ef notandaupplýsingum er breytt í Microsoft 365  er hægt að uppfæra [!INCLUDE[d365fin](includes/d365fin_md.md)] til að endurspegla breytinguna. Eftir því hvað á að uppfæra er hægt að velja eina af aðgerðunum á síðunni **Notendur** . Aðgerðunum er lýst í síðustu þremur dálkunum í töflunni hér að neðan.

|Hvað gerist ef:|Fyrsti notandi, fyrsta innskráning|Sækja notendur úr Microsoft 365 |Uppfæra notendur úr Microsoft 365|Endurheimta sjálfgefna notendahópa notanda|Uppfæra notendahópa|
|-|-|-|-|-|-|
|Umfang:|Núverandi notandi|Nýir notendur í Microsoft 365|Margir notendur valdir|Einn notandi valinn  (fyrir utan núverandi)|Margir notendur valdir|
|Bættu við nýjum notanda og úthlutaðu SUPER heimildasamstæðu.<br /><br /><!--Platform-->|**X**|| | | |
|Uppfærðu notandafærslu í samræmi við raunverulegar upplýsingar í Microsoft 365: Staða, fullt nafn, netfang tengiliðs, sannvottunarpóstur.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**| |
|Samstilltu notendaáskriftir (leyfi) með leyfum og hlutverkum sem eru úthlutuð í Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**| |**X**|**X**|
|Bættu notandanum við notendaflokka í samræmi við notendaáskriftir. Fjarlægja skal SUPER-heimildasamstæðuna fyrir alla notendur nema þann fyrsta sem skráir sig inn og [stjórnendur](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Velja þarf a.m.k. eitt SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**| |**X**<br /><br />Fjarlægir handvirkt úthlutuðum notendaflokkum og heimildum.|**X**<br /><br />Uppfæra úthlutunum notendaflokks.|

## <a name="the-device-license"></a>Leyfi tækis

Tækjaleyfið Dynamics 365 Business Central gerir mörgum notendum kleift að nota tæki samtímis sem leyfið nær yfir. Til dæmis gæti þetta verið tæki sölustaðar, verslunarrýmis eða vöruhúss. Þegar ákveðinn fjöldi tækjaleyfa hefur verið keyptur, getur sá fjöldi notenda sem hefur verið úthlutað flokki Dynamics 365 Business Central tækjanotenda skráð sig inn á sama tíma. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Stjórnandi Microsoft 365 fyrirtækisins eða samstarfsaðili Microsoft getur stofnað flokk Dynamics 365 Business Central tækjanotenda og bætt tækjanotendum við sem meðlimum í [Stjórnendamiðstöð Microsoft 365](https://admin.microsoft.com/) eða í [Azure-gáttinni](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Takmarkanir tækjanotanda

Notendur með tækjaleyfið geta ekki framkvæmt eftirfarandi verk í [!INCLUDE[d365fin](includes/d365fin_md.md)]:

- Setja upp vinnslur sem á að keyra sem áætluð verk í verkröðinni. Notendur tækis eru samhliða notendur og því er ekki hægt að tryggja að viðkomandi notandi sé staddur í kerfinu þegar verk er keyrt, sem krafist er.

- Tækjanotandi getur ekki verið fyrsti notandinn sem skráir sig inn. Notandi af gerðinni stjórnandi, fullur notandi eða ytri endurskoðandi verður að vera sá fyrsti sem skráir sig inn svo hann geti sett upp [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar er að finna í [Stjórnun Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) í hjálp stjórnenda.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Að stofna Dynamics 365 Business Central hóp tækjanotenda

1. Í stjórnendamiðstöð Microsoft 365 skal fara á síðuna **Hópar** .
2. Velja skal aðgerðina **Bæta við hópi** .
3. Á síðunni **Velja gerð hóps** skal velja aðgerðina **Öryggi** og síðan velja aðgerðina **Bæta við** .
4. Á síðunni **Grunnur** skal slá inn **Dynamics 365 Business Central tækjanotendur** sem heiti hópsins.
  
   >[!NOTE]
   >Heiti flokksins verður að vera stafað á ensku, nákvæmlega eins og er sýnt í skrefi 4, jafnvel þótt annað tungumál sé notað.
5. Velja hnappinn **Loka** .

> [!NOTE]
> Einnig er hægt að stofna hóp af gerðinni Microsoft 365. Frekari upplýsingar er að finna í [Bera saman hópa](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Bæta meðlimum við hópinn

1. Í stjórnendamiðstöð Microsoft 365 skal uppfæra síðuna **Hópar** svo að nýju hóparnir birtist.
2. Velja skal hópinn **Dynamics 365 Business Central tækjanotendur** og síðan aðgerðina **Skoða alla og hafa umsjón með meðlimum** .
3. Veljið aðgerðina **Bæta við meðlimum** .
4. Velja skal notendurna sem á að bæta við og síðan velja hnappinn **Vista** .
5. Veljið hnappinn **Loka** þrisvar sinnum.

Hægt er að bæta við eins mörgum notendum við flokkinn Dynamics 365 Business Central og þörf er á. Fjöldi tækja sem notendur geta skráð sig inn á samtímis fer eftir fjölda keyptra tækjaleyfa.

> [!NOTE]
> Ekki þarf að úthluta [!INCLUDE[d365fin](includes/d365fin_md.md)] -leyfi til notenda sem eru meðlimir í hópi Dynamics 365 Business Central tækisnotenda.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Umsjón með notendum og leyfum í uppsetningu innanhúss

Fyrir uppsetningu á staðnum er fjöldi notandaleyfa tilgreindur í leyfisskránni (.flf). Þegar stjórnandi eða Microsoft-samstarfsaðili hleður upp leyfisskránni getur stjórnandinn tilgreint hvaða notendur geta skráð sig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)].

Fyrir uppsetningar innanhúss býr stjórnandinn til, breytir og eyðir notendum beint af síðunni **Notendur** .

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Til að breyta eða eyða notanda í uppsetningu á staðnum

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Velja skal notandann sem á að breyta og velja síðan aðgerðina **Breyta** .
3. Á síðunni **Notandaspjald** skal breyta upplýsingunum eftir þörfum.  
4. Til að eyða notanda, skal velja notandann sem á að eyða og velja síðna aðgerðina **Eyða** .

> [!NOTE]
> Fyrir uppsetningar á staðnum getur stjórnandi tilgreint hvernig á að sannvotta innskráningarupplýsingar notanda í [!INCLUDE[server](includes/server.md)] tilvikinu. Þegar notandi er búinn til er gefin upp gerð innskráningarupplýsinga sem er notuð.
>
> Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í hjálparefni stjórnenda fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Sjá einnig

[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Sérstillir [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Bæta notendum við Microsoft 365 for Business](https://aka.ms/CreateOffice365Users)  
[Öryggi og vernd í Business Central (efni stjórnenda)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
