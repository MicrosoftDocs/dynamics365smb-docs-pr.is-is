---
title: Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 for Sales | Microsoft Docs
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
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c318346c62b7776a550a77a2947173e33d5f17c0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246575"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 for Sales
Þetta efnisatriði veitir yfirlit um hvernig á að setja upp notendareikninga sem er krafist til að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Uppsetning á notandareikningi stjórnanda í Sales
Þú verður að bæta notandareikningi stjórnanda við fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] sem notandi í [!INCLUDE[crm_md](includes/crm_md.md)] og síðan uppfæra notandann sem stjórnanda í [!INCLUDE[crm_md](includes/crm_md.md)]. Notandareikningur stjórnanda verður einnig að verða með hlutverk sem sérstillandi kerfis og að minnsta kosti eitt annað notandahlutverk sem er ekki stjórnunarhlutverk, t.d. sölustjóri, í [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Uppsetning notandareiknings fyrir samþættinguna
Þú verður að búa til þar til gerðan notandareikning í Office 365-áskriftinni þinni sem bæði [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] geta notað til að samstilla gögn. Þessi notandareikningur verður að geta skráð sig inn á [!INCLUDE[crm_md](includes/crm_md.md)], sem þýðir að þessi notandi verður að hafa leyfi fyrir [!INCLUDE[crm_md](includes/crm_md.md)]. Þessi reikningur má ekki vera gagnvirkur reikningur í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar um hvernig á að stofna notendur í [!INCLUDE[crm_md](includes/crm_md.md)] er að finna í [Stjórna öryggi, notendum og hópum](http://go.microsoft.com/fwlink/?LinkID=616518). Eftir að tengingin hefur verið sett upp mun [!INCLUDE[d365fin](includes/d365fin_md.md)] úthluta notandareikningi öryggishlutverki sem hann þarf í [!INCLUDE[d365fin](includes/d365fin_md.md)].

![Uppsetningarleiðbeiningar með hjálp sem sýnir stað til að færa inn samstilltar innskráningarupplýsingar](media/sync-user-setup.png "Síða leiðsagnarforrits fyrir myndræna uppsetningu með aðstoð sem sýnir stað til að færa inn samstilltar innskráningarupplýsingar")

> [!IMPORTANT]  
> Ekki nota stjórnandareikning fyrir [!INCLUDE[crm_md](includes/crm_md.md)] fyrir samstillingu. Það mun eyðileggja samstillinguna.
> Einnig, til að forðast stöðuga samstillingu, er breytingum á gögnum sem notandareikningur samþættingar gerir ekki samstilltar. <!--What changes would this account make?--> Eftir að tenging er gerð, er mælt með því að setja aðgangsstillinguna fyrir notandareikninginn fyrir samþættingu á ógagnvirka stillingu í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Stofna ógagnvirkan notandareikning](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Uppsetning reikninga fyrir sölumenn
Stofna verður notendareikninga í [!INCLUDE[crm_md](includes/crm_md.md)] fyrir sölufólk úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til að auðvelda þetta býður stjórnendamiðstöð Microsoft 365 Excel sniðmát sem þú getur notað. Á síðunni **Virkir notendur** skal velja **Fleiri** og síðan **Flytja inn marga notendur**. Veldu **Niðurhala CSV-skrá með eingöngu hausum** og síðan færa inn upplýsingarnar fyrir sölufólkið. Til að sjá dæmi skal velja **Niðurhala CSV-skrá með eingöngu hausum og dæmi um notandaupplýsingar**. Eftir að upplýsingar um notendur hafa verð færðar inn er næsta skrefið í innflutningsferlinu að úthluta notendum leyfum að Dynamics 365 Customer Engagement-áskriftinni.  

Eftir að notendur hafa verið fluttir inn og þeim úthlutað leyfum fyrir Dynamics 365 Customer Engagement, verður að úthluta notendum hlutverkinu **Sölumaður** í [!INCLUDE[crm_md](includes/crm_md.md)].

![Að tengja sölumenn við notendur í Dynamics 365 for Sales](media/couple-salespeople.png "Myndræn framsetning á tengingu sölumanna við notendur í Dynamics 365 for Sales")

## <a name="see-also"></a>Sjá einnig  
[Samþætting við Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
