---
title: Tengjast við Dynamics 365 Sales | Microsoft docs
description: Notkun annarra forrita með Business Central um Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196640"
---
# <a name="connect-to-common-data-service"></a>Tengjast við Common Data Service
Í þessu efnisatriði er lýst hvernig skal setja upp tengingu milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit á borð við [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Áður en byrjað er
Áður en tengingin er búin til þarf að koma nokkrum upplýsingum á framfæri:  

* Vefslóðin fyrir [!INCLUDE[d365fin](includes/cds_long_md.md)] umhverfið sem á að tengjast við. Ef uppsetningarleiðbeiningin **Uppsetning CDS-tengingar** með hjálp er notuð til að stofna tengingu finnum við umhverfin þín, en þú getur einnig slegið inn vefslóð fyrir annað umhverfi í leigjandanum þínum.  
* Notandaheiti og aðgangsorð fyrir notandareikning sem er aðeins notaður fyrir samþættinguna. Þessi reikningur er kallaður reikningur „samþættingarnotanda“. 
* Notandanafn og aðgangsorð reiknings sem er með heimildir stjórnanda í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Þessi skref lýsa ferlinu fyrir netútgáfuna af [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Uppsetning á tengingu við [!INCLUDE[d365fin](includes/cds_long_md.md)]  
Fyrir allar auðkennisgerðir aðrar en Office 365-auðkenningu, er sett upp tengingin við [!INCLUDE[d365fin](includes/cds_long_md.md)] á síðunni **Uppsetning CDS-tengingar**. Fyrir Office 365 auðkenningu er mælt með að þú notir uppsetningarleiðbeiningar **Uppsetning CDS-tengingar** með hjálp. Leiðbeiningarnar auðvelda uppsetningu á tengingu og tilgreina ítarlega eiginleika, t.d. tengingu milli færslna.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>Nota hjálparleiðbeiningar fyrir uppsetningu CDS-tengingar 
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning með hjálp** og veldu síðan tengda tengilinn.
2. Veldu **Setja upp CDS-grunnsamþættingartengingu** til að hefja uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.

> [!Note]
> Leiðbeiningarnar **Uppsetning CDS-tengingar** með hjálp úthlutar sjálfkrafa öryggishlutverkunum **Samþættingarstjórnandi** og **Samþættingarnotandi** til notandareiknings sem er notaður í samþættingu og stillir aðganginn að reikningnum á **Ógagnvirkur**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Að stofna eða vinna með tengingu handvirkt
Eftirfarandi ferli útskýrir hvernig á að setja upp tenginguna handvirkt á síðunni **Uppsetning CDS-tengingar**. Þetta er einnig síðan þar sem stillingum fyrir samþættingu er stjórnað.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning CDS-tengingar** og veldu síðan tengda tengilinn.
2. Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Svæði|Description|
|-----|-----|
|**Vefslóð umhverfis**|Ef þú átt umhverfi í [!INCLUDE[d365fin](includes/cds_long_md.md)] finnum við þau fyrir þig þegar þú keyrir uppsetningarleiðbeiningarnar. Ef þú vilt tengjast öðru umhverfi í öðrum leigjanda geturðu slegið inn innskráningarupplýsingar stjórnanda fyrir umhverfið og við finnum það fyrir þig. |
|**Notandaheiti** og **Aðgangsorð**|Aðgangsupplýsingar notandareikningsins sem er notaður fyrir samþættinguna. Nánari upplýsingar er að finna í [Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Virk**|Byrjaðu að nota samþættinguna. Ef tengingu er ekki komið á núna munu stillingar tengingar vera vistaðar en notendur geta ekki tengst [!INCLUDE[d365fin](includes/cds_long_md.md)] gögnum frá [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hægt er að koma aftur þessa síðu og virkja tenginguna seinna.  |

3. Í reitnum **Eignarhaldslíkan** skaltu velja hvort þú viljir að teymiseining í [!INCLUDE[d365fin](includes/cds_long_md.md)] eigi nýjar færslur eða einn eða fleiri tilteknir notendur. Ef valið er **Einstaklingur** þarf að tilgreina hvern notanda fyrir sig. Ef valið er **Teymi** birtist sjálfgefna fyrirtækiseiningin BCI_Company í reitnum **Tengd fyrirtækiseining**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Til að prófa stillingar tengingar skal velja **Tenging** og síðan **Prófa tengingu**.  

    > [!NOTE]  
    >  Ef dulritun gagna er ekki virkjuð í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður spurt hvort þú viljir virkja hana. Til að virkja dulritun gagna skal velja **Já** og gefa nauðsynlegar upplýsingar. Annars skal velja **Nei**. Hægt er að virkja dulritun gagna seinna. Nánari upplýsingar eru í [Gögn dulrituð í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) í Developer and IT Pro help.  

5. Ef [!INCLUDE[d365fin](includes/cds_long_md.md)] samstilling er ekki þegar sett upp verður spurt hvort nota eigi sjálfgefna samstillingaruppsetningu. Velja skal **Já** eða **Nei** á grunni þess hvort halda eigi færslum samræmdum í [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]
> Ef tengst er við [!INCLUDE[d365fin](includes/cds_long_md.md)] með síðunni **Uppsetning CDS-tengingar** kann að reynast nauðsynlegt að úthluta öryggishlutverkum Samþættingarstjórnanda og Samþættingarnotanda til reikningsins sem er notaður í samþættingu í Dynamics 365 Sales. Frekari upplýsingar er að finna í [Úthluta öryggishlutverki á notanda](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>Að aftengjast [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning CDS-tengingar** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning CDS-tengingar** skal slökkva á víxlhnappnum **Virkjað**.  

## <a name="see-also"></a>Sjá einnig  
[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  
