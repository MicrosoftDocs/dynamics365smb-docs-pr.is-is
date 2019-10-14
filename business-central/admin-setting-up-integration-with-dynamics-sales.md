---
title: Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales | Microsoft Docs
description: Kynntu þér hvernig á að setja upp notendareikninga sem forritin nota til að skiptast á gögnum og sem fólk notar til að fá aðgang að og samstilla gögn í forritunum.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: a876df301476cb6b4af335e8ee957de26865cbaa
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307829"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-sales"></a>Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales
Þetta efnisatriði veitir yfirlit um hvernig á að setja upp notendareikninga sem er krafist til að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Uppsetning á notandareikningi stjórnanda í Sales
Þú verður að bæta notandareikningi stjórnanda við fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] sem notandi í [!INCLUDE[crm_md](includes/crm_md.md)] og síðan uppfæra notandann sem stjórnanda í [!INCLUDE[crm_md](includes/crm_md.md)]. Notandareikningur stjórnanda verður einnig að verða með hlutverk sem sérstillandi kerfis og að minnsta kosti eitt annað notandahlutverk sem er ekki stjórnunarhlutverk, t.d. sölustjóri, í [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Uppsetning notandareiknings fyrir samþættinguna
Þú verður að búa til þar til gerðan notandareikning í Office 365-áskriftinni þinni sem bæði [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] geta notað til að samstilla gögn. Þessi notandareikningur verður að geta skráð sig inn á [!INCLUDE[crm_md](includes/crm_md.md)], sem þýðir að þessi notandi verður að hafa leyfi fyrir [!INCLUDE[crm_md](includes/crm_md.md)] og að minnsta kosti einu öryggishlutverki úthlutað í [!INCLUDE[crm_md](includes/crm_md.md)] eins og er útskýrt [hér](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Frekari upplýsingar um hvernig á að stofna notendur í [!INCLUDE[crm_md](includes/crm_md.md)] er að finna í [Stjórna öryggi, notendum og hópum](http://go.microsoft.com/fwlink/?LinkID=616518). Eftir að tengingin hefur verið sett upp mun [!INCLUDE[d365fin](includes/d365fin_md.md)] úthluta notandareikningi öryggishlutverki sem hann þarf í [!INCLUDE[d365fin](includes/d365fin_md.md)] og hægt er að stilla þennan reikning á [ógagnvirka aðgangsstillingu](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) í [!INCLUDE[crm_md](includes/crm_md.md)]

![Uppsetningarleiðbeiningar með hjálp sem sýnir stað til að færa inn samstilltar innskráningarupplýsingar](media/sync-user-setup.png "Síða leiðsagnarforrits fyrir myndræna uppsetningu með aðstoð sem sýnir stað til að færa inn samstilltar innskráningarupplýsingar")

> [!IMPORTANT]  
> Ekki nota stjórnandareikning fyrir [!INCLUDE[crm_md](includes/crm_md.md)] fyrir samstillingu. Það mun eyðileggja samstillinguna.
> Einnig, til að forðast stöðuga samstillingu, er breytingum á gögnum sem notandareikningur samþættingar gerir ekki samstilltar. <!--What changes would this account make?--> Eftir að tenging er gerð, er mælt með því að setja aðgangsstillinguna fyrir notandareikninginn fyrir samþættingu á ógagnvirka stillingu í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Stofna ógagnvirkan notandareikning](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-sales-people"></a>Uppsetning sölumanna reikninga
Stofna verður notendareikninga í [!INCLUDE[crm_md](includes/crm_md.md)] fyrir sölufólk úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til að auðvelda þetta býður stjórnendamiðstöð Microsoft 365 Excel sniðmát sem þú getur notað. Á síðunni **Virkir notendur** skal velja **Fleiri** og síðan **Flytja inn marga notendur**. Veldu **Niðurhala CSV-skrá með eingöngu hausum** og síðan færa inn upplýsingarnar fyrir sölufólkið. Til að sjá dæmi skal velja **Niðurhala CSV-skrá með eingöngu hausum og dæmi um notandaupplýsingar**. Eftir að upplýsingar um notendur hafa verð færðar inn er næsta skrefið í innflutningsferlinu að úthluta notendum leyfum að Dynamics 365 Customer Engagement-áskriftinni.  

Eftir að notendur hafa verið fluttir inn og þeim úthlutað leyfum fyrir Dynamics 365 Customer Engagement, verður að úthluta notendum hlutverkinu **Sölumaður** í [!INCLUDE[crm_md](includes/crm_md.md)].

![Að tengja sölumenn við notendur í Dynamics 365 Sales](media/couple-salespeople.png "Myndræn framsetning á tengingu sölumanna við notendur í Dynamics 365 Sales")

## <a name="minimum-permissions-for-user-accounts-in-includecrm_mdincludescrm_mdmd"></a>Lágmarksheimildir fyrir notendareikninga í [!INCLUDE[crm_md](includes/crm_md.md)]
Þegar heimildir samþættingarlausnar eru settar upp eru heimildir fyrir notandareikning samþættingar grunnstilltar í [!INCLUDE[crm_md](includes/crm_md.md)]. Ef þessum heimildum er breytt þarf mögulega að endurstilla þær. Hægt er að gera það með því að setja samþættingarlausnina upp aftur eða endurstilla þær handvirkt. Eftirfarandi töflur sýna lágmarksheimildir fyrir notendareikningana í [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Samþættingarstjórnandi
Eftirfarandi tafla sýnir lágmarksheimildir í hverjum flipa fyrir hvert öryggishlutverk sem stjórnandi þarf að hafa.

##### <a name="customization"></a>Sérsnið
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Líkanadrifið forrit|Altæk|||Lesa|
|Samsetning viðbótar|Altæk|Lesa|Lesa|Lesa|
|Gerð viðbótar|Altæk|Lesa|Lesa|Lesa|
|Tengsl|Altæk|||Lesa|
|SDK-skilaboð|Altæk|Lesa|Lesa|Lesa|
|Skref SDK-skilaboðavinnslu|Altæk|Lesa|Lesa|Lesa|
|Mynd af skrefi SDK-skilaboðavinnslu|Altæk|Lesa|Lesa|Lesa|
|Kerfi frá|Altæk|||Skrifa|

##### <a name="custom-entities"></a>Sérsniðnar einingar
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Talnagögn reiknings fyrir Business Central|Altæk|Lesa|Lesa|Lesa|
|Business Central-tenging|Altæk|Búa til, lesa, skrifa, eyða|Búa til, lesa, skrifa, eyða|Búa til, lesa, skrifa, eyða|
|Bókunarskilgreining|Altæk|||Skrifa|

#### <a name="integration-user"></a>Samþættingarnotandi
Eftirfarandi tafla sýnir lágmarksheimildir í hverjum flipa fyrir hvert öryggishlutverk sem notandi samþættingar þarf að vera með.

##### <a name="core-records"></a>Grunnfærslur
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Reikningur|Altæk|Búa til, lesa, skrifa, skeyta, skeyta við, úthluta|Búa til, lesa, skrifa, skeyta, skeyta við, úthluta|Búa til, lesa, skrifa, skeyta, skeyta við, úthluta|
|Aðgerðarspjald|Altæk||Lesa|Lesa|
|Tenging|Altæk|Lesa|Lesa|Lesa|
|Tengiliður|Altæk|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|
|Athugasemd|Altæk|||Búa til, lesa, skrifa, eyða viðbót, úthluta|
|Tækifæri|Altæk||Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|
|Færsla|Altæk|||Búa til, lesa, skeyta við|
|Viðmótseining notanda|Notandi|Búa til, lesa, skrifa|Búa til, lesa, skrifa|Búa til, lesa, skrifa|

##### <a name="sales"></a>Sölur
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Reikningsfæra|Altæk|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|
|Röð|Altæk|Lesa, skrifa, skeyta við|Lesa, skrifa, skeyta við|Lesa, skrifa, skeyta, skeyta við, úthluta|
|Vara|Altæk|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|
|Eiginleiki|Altæk|Lesa|Lesa|Lesa|
|Tengsl eiginleika|Altæk|Lesa|Lesa|Lesa|
|Stillingaratriði fyrir valkost eiginleika|Altæk|Lesa|Lesa|Lesa|
|Tilboð|Altæk|Lesa|Lesa|Lesa|

##### <a name="service"></a>Þjónusta
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Kassi|Altæk|Lesa|Lesa|Lesa|

##### <a name="business-management"></a>Viðskiptastjórnun
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Gjaldmiðill|Altæk|Búa til, lesa, skrifa|Búa til, lesa, skrifa|Búa til, lesa, skrifa|
|Fyrirtæki|Altæk|Lesa, skrifa|Lesa, skrifa|Lesa, skrifa|
|Öryggishlutverk|Altæk|||Lesa|
|Notandi|Altæk|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|Búa til, lesa, skrifa, skeyta, skeyta við|
|Notandastillingar|Altæk|Búa til, lesa, skrifa, eyða, skeyta við|Búa til, lesa, skrifa, eyða, skeyta við|Búa til, lesa, skrifa, eyða, skeyta við|
|Koma fram fyrir hönd annars notanda|Altæk|Já|Já|Já|

##### <a name="customization"></a>Sérsnið
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Svæði|Altæk||Lesa|Lesa|
|Samsetning viðbótar|Altæk|Lesa|Lesa|Lesa|
|Gerð viðbótar|Altæk|Lesa|Lesa|Lesa|
|SDK-skilaboð|Altæk|Lesa|Lesa|Lesa|
|Skref SDK-skilaboðavinnslu|Altæk|Lesa|Lesa|Lesa|
|Veftilföng|Altæk|Lesa|Lesa|Lesa|

##### <a name="custom-entities"></a>Sérsniðnar einingar
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Talnagögn reiknings fyrir Dynamics 365 Business Central|Altæk|Búa til, lesa, skrifa, skeyta við|Búa til, lesa, skrifa, skeyta við|Búa til, lesa, skrifa, skeyta við|
|Dynamics 365 Business Central-Tenging|Altæk|Lesa|Lesa|Lesa|

### <a name="product-availability-user"></a>Notandi afurðaframboðs
Hægt er að leyfa sölufólki að skoða birgðastöðu fyrir vörurnar sem það selur með því að veita þeim heimildir sem eru útskýrðar í eftirfarandi töflu.

##### <a name="custom-entities"></a>Sérsniðnar einingar
|Öryggishlutverk|Aðgangsstig|Dynamics NAV 2018 og eldri|Business Central <br> Október 2018|Business Central <br> Apríl 2019|
|----|----|-----|----|----|
|Talnagögn reiknings fyrir Dynamics 365 Business Central|Altæk|Búa til, lesa, skrifa, skeyta við|Búa til, lesa, skrifa, skeyta við|Búa til, lesa, skrifa, skeyta við|
|Dynamics 365 Business Central-Tenging|Altæk|Lesa|Lesa|Lesa|

## <a name="see-also"></a>Sjá einnig  
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
