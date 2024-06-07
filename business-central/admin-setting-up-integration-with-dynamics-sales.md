---
title: Uppsetning á notendareikningum fyrir samþættingu við Microsoft Dataverse | Microsoft Docs
description: Kynntu þér hvernig á að setja upp notendareikninga sem forritin nota til að skiptast á gögnum og sem fólk notar til að fá aðgang að og samstilla gögn í forritunum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 01/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Uppsetning notendareikninga til samþættingar við Microsoft Dataverse með samstillingu gagna

Þetta efnisatriði veitir yfirlit um hvernig á að setja upp notendareikninga sem er krafist til að samþætta [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)].

## Setja upp notandareikning stjórnanda

Til að setja upp tenginguna á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] verður þú að skrá þig inn á [!INCLUDE[prod_short](includes/prod_short.md)] með notandareikningi sem er úthlutað á [!INCLUDE[prod_short](includes/prod_short.md)]  Nauðsynlegt eða [!INCLUDE[prod_short](includes/prod_short.md)] Premium leyfi. Við munum nota þennan reikning einu sinni til að setja upp og stilla nauðsynlega íhluti.

> [!IMPORTANT]
> Við uppsetningu verður þú beðinn um að gefa upp skilríki fyrir [!INCLUDE[prod_short](includes/cds_long_md.md)] umhverfið. Gefðu upp skilríki reiknings sem er með leyfisnotanda og úthlutað er **kerfisstjóra** öryggishlutverki í [!INCLUDE[prod_short](includes/cds_long_md.md)] umhverfinu og alþjóðlegum stjórnanda á leigjanda til að sem umhverfið tilheyrir. Þessi reikningur þarf ekki leyfi til að [!INCLUDE[prod_short](includes/prod_short.md)] vegna þess að hann verður aðeins notaður til að gera uppsetningarverkefni í [!INCLUDE[prod_short](includes/cds_long_md.md)] umhverfinu.
>
> Eftir að uppsetningu tengingarinnar er lokið geturðu fjarlægt þennan [!INCLUDE[prod_short](includes/cds_long_md.md)] notanda. Samþættingin heldur áfram að nota notandareikninginn sem er búinn sjálfkrafa til fyrir samþættinguna.

## Heimildir og öryggishlutverk fyrir notandareikninga í [!INCLUDE[prod_short](includes/cds_long_md.md)]

Grunnsamþættingarlausnin skapar eftirfarandi hlutverk í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] fyrir samþættinguna:

* **Business Central Dataverse Samþætting** - Gerir þér kleift að stjórna tengingunni milli [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Venjulega eru þessu aðeins úthlutað á notandareikninginn sem er búinn til sjálfkrafa fyrir samstillingu.

> [!NOTE]
> Aðeins notandi forritsins sem rekur samþættinguna ætti að hafa **Business Central Dataverse Integration** hlutverkið. Notandi forritsins þarf ekki [!INCLUDE [prod_short](includes/prod_short.md)] eða [!INCLUDE [cds_long_md](includes/cds_long_md.md)] leyfin.

Þegar grunnsamþættingarlausn er sett upp eru heimildir fyrir notandareikning samþættingar grunnstilltar. Ef þeim heimildum er breytt handvirkt er hægt að endurstilla þær. Veldu **Endurvirkja samþættingarlausn** á síðunni **Uppsetning Dataverse tengingar** til að setja aftur upp grunnsamþættingarlausnina. Þetta skref mun innleiða öryggishlutverk Business Central-samþættingar.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## Sjá einnig .

[Samþætting við Microsoft Dataverse](admin-common-data-service.md)  
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
