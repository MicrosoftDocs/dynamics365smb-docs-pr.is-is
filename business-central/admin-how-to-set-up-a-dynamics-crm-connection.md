---
title: Tengja við Dynamics 365 for Sales | Microsoft Docs
description: Hægt er að samþætta við Dynamics 365 for Sales.
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
ms.openlocfilehash: 28ce599b2067faa904f917f8fce7390202c98d7b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245758"
---
# <a name="set-up-a-connection-to-dynamics-365-for-sales"></a>Uppsetning á tengingu við Dynamics 365 for Sales
Til að samþætta við [!INCLUDE[crm_md](includes/crm_md.md)] þarf að setja upp tengingu á milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)]. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Áður en byrjað er
Áður en byrjað er að tengja forritin eru nokkrir þættir sem gagnlegt er að hafa tilbúna:  

* Vefslóð fyrir [!INCLUDE[crm_md](includes/crm_md.md)]-forritið þitt. Fljótleg leið til að ná í vefslóðina er að opna [!INCLUDE[crm_md](includes/crm_md.md)] og afrita vefslóðina og svo líma hana í reitinn **Dynamics 365 for Sales Vefslóð** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] mun leiðrétta sniðið fyrir þig.  
* Notandaheiti og aðgangsorð fyrir notandareikning sem er aðeins notaður fyrir samþættinguna.  
* Notandaheiti og aðgangsorð reikningsins sem er með heimildir stjórnanda.  
  
> [!Note]
> Þessi skref lýsa ferlinu fyrir netútgáfuna af [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrmmdincludescrmmdmd"></a>Uppsetning, prófun og virkjun tengingar við [!INCLUDE[crm_md](includes/crm_md.md)]  
Fyrir allar auðkennisgerðir aðrar en Office 365-auðkenningu, er sett upp tengingin við Dynamics 365 for Sales á síðunni **Microsoft Dynamics 365 for Sales Uppsetning tengingar**. Fyrir auðkenningu Office 365 er einnig hægt að nota **Setja upp Dynamics 365 for Sales-tenging** leiðbeiningar um uppsetningu með hjálp, sem hjálpar til við að veita nauðsynlegar upplýsingar.

### <a name="to-use-an-assisted-setup-guide"></a>Til að nota leiðbeiningar um uppsetningu með hjálp
**Setja upp Dynamics 365 for Sales-tengingu** leiðbeiningar um uppsetningu með hjálp getur auðveldað þér að setja upp tenginguna og gefa upp hvort eigi að virkja ítarlega eiginleika, t.d. tenging milli færslna. 

1. Veldu **Uppsetning og viðbætur** og veldu síðan **Uppsetning með hjálp**.
2. Veldu **Setja upp Dynamics 365 for Sales-tengingu** til að hefja leiðbeiningar um uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.
4. Einnig eru ítarlegar stillingar sem geta aukið öryggi og virkjað [!INCLUDE[crm_md](includes/crm_md.md)] viðbótarmöguleika, t.d. úrvinnsla sölupöntunar og skoðun á birgðastöðum. Eftirfarandi tafla lýsir ítarlegum stillingum.  

|Svæði|Description|
|-----|-----|
|**Flytja inn Dynamics 365 for Sales lausn**|Virkja þetta til að setja upp og grunnstilla samþættingarlausnina í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Um samþættingarlausn Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Birta vefþjónustuna „Vara til ráðstöfunar“**|Gera fólki sem er að nota [!INCLUDE[crm_md](includes/crm_md.md)] kleift að skoða framboð á vörum (afurðum) í birgðum í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta krefst [!INCLUDE[d365fin](includes/d365fin_md.md)]-notandareikningsins með aðgangslykli vefþjónustu. Úthlutun lykilsins er ferli í tveimur skrefum. Í notandareikningnum í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður þú að velja aðgerðina **Breyta vefþjónustulykli**. Í uppsetningarleiðbeiningum með hjálp fyrir uppsetningu Dynamics 365 for Sales-tengingar verður að tilgreina vefslóðina fyrir OData-vefþjónustu Dynamics 365 Business Central og veita [!INCLUDE[d365fin](includes/d365fin_md.md)] aðgangsupplýsingar notanda fyrir aðgang að þjónustunni. Nánari upplýsingar er að finna í [Vefþjónustur OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**Vefslóð fyrir vefþjónustu Dynamics 365 Business Central OData**|Ef vefþjónusta fyrir ráðstöfun á vöru er virkjuð verður vefslóð fyrir vefþjónustu OData útvegað fyrir þig.|
|**Dynamics 365 Business Central Notandanafn fyrir vefþjónustu OData**|Heit á [!INCLUDE[d365fin](includes/d365fin_md.md)]-notandareikningi sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar í [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData.|
|**Dynamics 365 Business Central Aðgangslykill vefþjónustu OData**|Aðgangslykill fyrir notandareikning sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar frá [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData. Lyklinum er úthlutað til notanda sem er valinn í reitnum **Dynamics 365 Business Central Notandanafn fyrir vefþjónustu OData**. Til að fá lykilinn skal velja hnappinn **Fletta upp gildi** við hliðina á notandanafninu, velja notandann, velja **Stjórna** og síðan **Breyta**. Á notandaspjaldinu skal velja **Aðgerðir**, **Sannvottun** og síðan velja **Breyta vefþjónustulykli**.|
|**Virkja samþættingu sölupöntunar**|Þegar fólk stofnar sölupantanir í [!INCLUDE[crm_md](includes/crm_md.md)], skal afrita pantanir í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta krefst þess að þú veitir aðgangsupplýsingar fyrir notandareikning stjórnanda í [!INCLUDE[crm_md](includes/crm_md.md)]. Nánari upplýsingar er að finna í [Meðhöndlun á gögnum sölupöntunar](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Virkja Dynamics 365 for Sales-tengingu**|Virkja tenginguna við [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Dynamics 365 SDK útgáfa**|Þetta á aðeins við ef verið er að samþætta við útgáfu á staðnum af [!INCLUDE[crm_md](includes/crm_md.md)]. Þetta er hugbúnaðarþróunarpakki Dynamics 365 (einnig vísað í sem Xrm) sem er notaður tili að tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)]. Útgáfan verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)] og sú sama eða nýrri og útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="to-create-or-maintain-the-connection-manually"></a>Að stofna eða vinna með tengingu handvirkt
Eftirfarandi ferli útskýrir hvernig á að fylla út reitina á síðunni **Microsoft Dynamics 365 for Sales Uppsetning tengingar** handvirkt. Þetta er einnig síðan þar sem stillingum fyrir samþættingu er stjórnað.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Microsoft Dynamics 365 Uppsetning tengingar** og veldu síðan tengda tengilinn.
2. Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)].

|Svæði|Description|
|-----|-----|
|**Dynamics 365 for Sales VEFSLÓÐ**|Vefslóðin fyrir tilvikið þitt af [!INCLUDE[crm_md](includes/crm_md.md)]. Til að fá vefslóðina skal opna [!INCLUDE[crm_md](includes/crm_md.md)], afrita vefslóðina úr aðseturslínunni í vafranum þínum og síðan líma vefslóðina í reitinn. [!INCLUDE[d365fin](includes/d365fin_md.md)] gengur úr skugga um að sniðið sé rétt.|
|**Notandaheiti** og **Aðgangsorð**|Aðgangsupplýsingar notandareikningsins sem er notaður fyrir samþættinguna. Nánari upplýsingar er að finna í [Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Virk**|Byrjaðu að nota samþættinguna. Ef tengingu er ekki komið á núna munu stillingar tengingar vera vistaðar en notendur geta ekki tengst [!INCLUDE[crm_md](includes/crm_md.md)] gögnum frá [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hægt er að koma aftur þessa síðu og virkja tenginguna seinna.  |
|**Dynamics 365 SDK útgáfa**|Ef verið er að samþætta við útgáfu á staðnum af [!INCLUDE[crm_md](includes/crm_md.md)], er þetta hugbúnaðarþróunarpakki Dynamics 365 (einnig vísað í sem Xrm) sem er notaður til að tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)]. Útgáfan sem var valin verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)]. Þessi útgáfa sem er til jafns á við eða nýrri en útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Ef verið er að tengja útgáfu á staðnum af [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)] og þú vilt skilgreina tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]-tilvik með tiltekinni gerð sannvottunar skaltu fylla út reitina á flýtiflipanum **Upplýsingar um sannvottunargerð**. Frekari upplýsingar er að finna í [Nota tengistrengi í XRM-verkfærum til að tengjast við Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Ekki er krafist þessa skrefs þegar tengd er netútgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Svæði|Description|
|-----|-----|
|**Dynamics 365 Business Central Vefslóð vefbiðlara**|Vefslóð fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilvikið þitt. Þetta gerir notendum í [!INCLUDE[crm_md](includes/crm_md.md)] kleift að opna samsvarandi færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] úr færslum í [!INCLUDE[crm_md](includes/crm_md.md)], svo sem reikning eða vöru afurð. [!INCLUDE[d365fin](includes/d365fin_md.md)]-færslur opnast í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Stillið þennan reit á vefslóð fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] tilvikið sem nota á.<br /><br /> Til að endurstilla reitinn á sjálfgefna vefslóð fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], skal velja aðgerðina **Endurstilla vefslóð vefbiðlara**.<br /><br /> Þessi reitur á aðeins við ef [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættingarlausn er sett upp í [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Kveikt er á vefþjónustunni Vara til ráðstöfunar**|Gera fólki sem er að nota [!INCLUDE[crm_md](includes/crm_md.md)] kleift að skoða framboð á vörum (afurðum) í birgðum í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef þetta er virkjað þarf einnig að útvega notandanafn og aðgangslykli fyrir [!INCLUDE[crm_md](includes/crm_md.md)] til að nota til að senda fyrirspurn á vefþjónustu OData um framboð á vörum (afurðum). Nánari upplýsingar er að finna í [Vefþjónustur OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**Vefslóð fyrir vefþjónustu Dynamics 365 Business Central OData**|Ef vefþjónusta fyrir ráðstöfun á vöru er virkjuð verður vefslóð fyrir vefþjónustu OData útvegað fyrir þig.|
|**Dynamics 365 Business Central Notandanafn fyrir vefþjónustu OData**|Heiti notandareiknings sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar frá [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData.|
|**Dynamics 365 Business Central Aðgangslykill vefþjónustu OData**|Aðgangslykill fyrir notandareikning sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar frá [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData. Lyklinum er úthlutað til notanda sem er valinn í reitnum **Dynamics 365 Business Central Notandanafn fyrir vefþjónustu OData**. Til að fá lykilinn skal velja hnappinn **Fletta upp gildi** við hliðina á notandanafninu, velja notandann, velja **Stjórna** og síðan **Breyta**. Á notandaspjaldinu skal velja **Aðgerðir**, **Sannvottun** og síðan velja **Breyta vefþjónustulykli**.|

4. Færið inn eftirfarandi stillingar fyrir [!INCLUDE[crm_md](includes/crm_md.md)].

|Svæði|Description|
|-----|-----|
|**Kveikt er á samþættingu sölupöntunar**|Gerðu notendum kleift að senda inn sölupantanir og virkjuð tilboð í [!INCLUDE[crm_md](includes/crm_md.md)] og síðan skoða og vinna úr þeim í [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Stofna sölupantanir sjálfvirkt**|Stofna sölupöntun í [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar notandi stofnar og sendir inn eina í [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Vinna sölutilboð sjálfkrafa**|Vinna úr sölutilboði í [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar notandi stofnar og virkjar eitt slíkt í [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Færðu inn eftirfarandi ítarlegar stillingar.

|Svæði|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Notendur verða að varpa í Dynamics 365 for Sales notendur**|Tilgreina hvort [!INCLUDE[d365fin](includes/d365fin_md.md)] notendareikningar verða að hafa samsvarandi notendareikninga í [!INCLUDE[crm_md](includes/crm_md.md)]. **Office 365 Sannvottunarnetfang** fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir notandann verður að vera sama og **Aðalnetfang** fyrir [!INCLUDE[crm_md](includes/crm_md.md)] notandann.<br /><br /> Ef þetta gildi er stillt á **Já**, [!INCLUDE[d365fin](includes/d365fin_md.md)] munu notendur sem ekki hafa samsvarandi [!INCLUDE[crm_md](includes/crm_md.md)] notandareikning ekki geta notað [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættingu í notandaviðmótinu. Aðgangur að [!INCLUDE[crm_md](includes/crm_md.md)] gögnum beint úr [!INCLUDE[d365fin](includes/d365fin_md.md)] er veittur fyrir hönd [!INCLUDE[crm_md](includes/crm_md.md)] notandareikningsins.<br /><br /> Ef þetta gildi er stillt á **Nei**, munu allir [!INCLUDE[d365fin](includes/d365fin_md.md)] notendur geta notað [!INCLUDE[crm_md](includes/crm_md.md)] samþættingu í notandaviðmótinu. Aðgangur að [!INCLUDE[crm_md](includes/crm_md.md)] gögnum er veittur fyrir hönd notanda [!INCLUDE[crm_md](includes/crm_md.md)]-tengingar (samþættingar).|
|**Núverandi notanda Business Central er varpað í Dynamics 365 for Sales notanda**|Gefur til kynna hvort notandareikningurinn þinn sé varpað í reikning í [!INCLUDE[crm_md](includes/crm_md.md)]|

6. Til að prófa stillingar tengingar skal velja **Prófa tengingu**.  

    > [!NOTE]  
    >  Ef dulritun gagna er ekki virkjuð í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður spurt hvort þú viljir virkja hana. Til að virkja dulritun gagna skal velja **Já** og gefa nauðsynlegar upplýsingar. Annars skal velja **Nei**. Hægt er að virkja dulritun gagna seinna. Nánari upplýsingar eru í [Gögn dulrituð í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) í Developer and IT Pro help.  

7. Ef [!INCLUDE[crm_md](includes/crm_md.md)] samstilling er ekki þegar sett upp verður spurt hvort nota eigi sjálfgefna samstillingaruppsetningu. Velja skal **Já** eða **Nei** á grunni þess hvort halda eigi færslum samræmdum í [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

### <a name="to-disconnect-from-includecrmmdincludescrmmdmd"></a>Að aftengjast [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Microsoft Dynamics 365 for Sales Uppsetning tengingar** og veldu síðan tengda tengilinn.
2. Á síðunni **Microsoft Dynamics 365 for Sales Uppsetning tengingar** skal hreinsa gátreitinn **Virkjað**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension? 


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.--> 

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 for Sales Connection]() --> 

<!-- 
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 for Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 for Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 for Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Sjá einnig  
[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  

