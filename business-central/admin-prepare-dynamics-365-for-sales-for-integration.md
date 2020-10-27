---
title: Samþætting við Dynamics 365 Sales| Microsoft Docs
description: Kynntu þér hvernig þú sækir Dynamics 365 Business Central tilbúið til að samþætta við Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: e93d36c2767bc43444b5b23471b6d0aaa0c84adf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917827"
---
# <a name="integrating-with-dynamics-365-sales"></a>Samþætting við Dynamics 365 Sales

Hlutverk sölumannsins er oft talið sýnilegasti hlutinn í viðskiptum. Hins vegar getur það gagnast sölumönnum að geta fengið innsýn í viðskiptin og séð hvað er að gerast á bak við tjöldin. Með því að samþætta [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] er hægt að veita sölufólkinu þessa innsýn með því að gera því kleift að skoða upplýsingar í [!INCLUDE[d365fin](includes/d365fin_md.md)] á meðan það vinnur í [!INCLUDE[crm_md](includes/crm_md.md)]. Þegar sölutilboð er undirbúið getur það til dæmis verið gagnlegt að vita hvort nægar birgðir séu til staðar til að uppfylla pöntunina. Frekari upplýsingar er að finna í [Að nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Þetta efnisatriði útskýrir ferlið við samþættingu á vefútgáfum af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)]. Frekari upplýsingar um grunnstillingu á staðnum er að finna í [Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-common-data-service"></a>Samþætting í gegnum Common Data Service
[!INCLUDE[d365fin](includes/d365fin_md.md)] er einnig samþætt við [!INCLUDE[d365fin](includes/cds_long_md.md)], sem auðveldar tengingu og samstillingu gagna við önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forrit sem þú smíðar. Ef samþætting er gerð í fyrsta skipti er mælt með því að gera hana í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Common Data Service](admin-common-data-service.md).

Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni. Ef þú hins vegar uppfærir eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)] til að kveikja á henni aftur. Frekari upplýsingar er að finna í [Uppfærsla samþættingar við Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Endurtenging um [!INCLUDE[d365fin](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar. Til dæmis verða sjálfgefnar töfluvarpanir notaðar.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Stillingar samþættingar sem eiga sérstaklega við um [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingu
Samþætting við [!INCLUDE[d365fin](includes/d365fin_md.md)] gerist í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)] og samþættingin býður upp margar staðlaðar stillingar og einingar. Ásamt stöðluðum stillingum, eru nokkrar sem eiga sérstaklega við um [!INCLUDE[crm_md](includes/crm_md.md)]. Þær eru taldar upp í eftirfarandi hlutum.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Heimildir og öryggishlutverk fyrir notandareikninga í Sales
Þegar samþættingarlausnin er sett upp eru heimildir fyrir notandareikning samþættingar grunnstilltar. Ef þessum heimildum er breytt þarf mögulega að endurstilla þær. Hægt er að gera það með því að setja samþættingarlausnina upp aftur eða velja **Endurvirkja samþættingarlausn** á síðunni **Uppsetning Dynamics 365-tengingar** . Eftirfarandi öryggishlutverk eru virkjuð:

* Dynamics 365 Business Central Samþættingarstjórnandi
* Dynamics 365 Business Central Samþættingarnotandi
* Dynamics 365 Business Central Notandi afurðaframboðs

### <a name="connection-settings-in-the-setup-guide"></a>Tengingarstillingar í uppsetningarleiðbeiningum

Hægt er að nota uppsetningarleiðbeiningar með hjálp til að setja upp tenginguna á fljótvirkan hátt og tilgreina ítarlega eiginleika, t.d. tengingu milli færslna.

1. Veldu **Uppsetning og viðbætur** og veldu síðan **Uppsetning með hjálp** .
2. Veldu **Setja upp Dynamics 365 Sales tengingu** til að hefja leiðbeiningar um uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.
4. Einnig eru ítarlegar stillingar sem geta aukið öryggi og virkjað viðbótarmöguleika, t.d. úrvinnsla sölupöntunar og skoðun á birgðastöðum. Eftirfarandi tafla lýsir ítarlegum stillingum.  

| Svæði | Description |
|--|--|
| **Flytja inn Dynamics 365 Sales Solution** | Virkja þetta til að setja upp og grunnstilla samþættingarlausnina í [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Birta vefþjónustuna „Vara til ráðstöfunar“** | Gera fólki sem er að nota [!INCLUDE[crm_md](includes/crm_md.md)] kleift að skoða framboð á vörum (afurðum) í birgðum í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta krefst [!INCLUDE[d365fin](includes/d365fin_md.md)]-notandareiknings með aðgangslykli vefþjónustu. Úthlutun lykilsins er ferli í tveimur skrefum. Í notandareikningnum í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður þú að velja aðgerðina **Breyta vefþjónustulykli** . Í uppsetningarleiðbeiningum með hjálp fyrir uppsetningu Dynamics 365 Sales tengingar verður að tilgreina vefslóðina fyrir OData-vefþjónustu Dynamics 365 Business Central og veita [!INCLUDE[d365fin](includes/d365fin_md.md)] aðgangsupplýsingar notanda fyrir aðgang að þjónustunni. Nánari upplýsingar er að finna í [Vefþjónustur OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **Vefslóð vefþjónustu Business Central OData** | Ef vefþjónustan er virkjuð til að skoða vörur til ráðstöfunar færðu útvegaða vefslóð fyrir vefþjónustu OData. |
| **Notandanafn vefþjónustu Business Central OData** | Heiti [!INCLUDE[d365fin](includes/d365fin_md.md)]-notandareiknings sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar í [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData. |
| **Aðgangslykill vefþjónustu Business Central OData** | Aðgangslykill fyrir notandareikning sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar frá [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData. Lyklinum er úthlutað til notanda sem er valinn í reitnum **Notandanafn fyrir vefþjónustu Business Central OData** . Til að fá lykilinn skal velja hnappinn **Fletta upp gildi** við hliðina á notandanafninu, velja notandann, velja **Stjórna** og síðan **Breyta** . Á notandaspjaldinu skal velja **Aðgerðir** , **Sannvottun** og síðan velja **Breyta vefþjónustulykli** . |
| **Virkja samþættingu sölupöntunar** | Þegar fólk býr til sölupantanir í [!INCLUDE[crm_md](includes/crm_md.md)] og uppfyllir pantanir í [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættar þetta ferlið í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna á [Virkja sölupöntunarferli samþættingar](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Þetta krefst þess að þú veitir aðgangsupplýsingar fyrir notandareikning stjórnanda í [!INCLUDE[crm_md](includes/crm_md.md)]. Nánari upplýsingar er að finna í [Meðhöndlun á gögnum sölupöntunar](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **Virkja CDS-tengingu** | Virkja tenginguna við [!INCLUDE[d365fin](includes/cds_long_md.md)]. |
| **Dynamics 365 SDK útgáfa** | Þetta á aðeins við ef verið er að samþætta við útgáfu á staðnum af [!INCLUDE[crm_md](includes/crm_md.md)]. Þetta er hugbúnaðarþróunarpakki Dynamics 365 (einnig vísað í sem Xrm) sem er notaður tili að tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)]. Útgáfan verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)] og sú sama eða nýrri og útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Stillingar tengingar á Uppsetning tengingar  Microsoft Dynamics 365

Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Svæði | Description |
|--|--|
| **Dynamics 365 Sales vefslóð** | Vefslóð fyrir [!INCLUDE[crm_md](includes/crm_md.md)]-tilvikið þitt. Þetta gerir notendum kleift að opna samsvarandi færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] úr færslum í [!INCLUDE[crm_md](includes/crm_md.md)], svo sem reikningi eða vöru. [!INCLUDE[d365fin](includes/d365fin_md.md)]-færslur opnast í [!INCLUDE[d365fin](includes/d365fin_md.md)]. |
|**Dynamics 365 Sales vefslóð**|Vefslóð fyrir [!INCLUDE[crm_md](includes/crm_md.md)]-tilvikið þitt. Þetta gerir notendum kleift að opna samsvarandi færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] úr færslum í [!INCLUDE[crm_md](includes/crm_md.md)], svo sem reikningi eða vöru. [!INCLUDE[d365fin](includes/d365fin_md.md)]-færslur opnast í [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Kveikt er á vefþjónustunni Vara til ráðstöfunar**|Gera fólki sem er að nota [!INCLUDE[crm_md](includes/crm_md.md)] kleift að skoða framboð á vörum (afurðum) í birgðum í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef þetta er virkjað þarf einnig að útvega notandanafn og aðgangslykli fyrir [!INCLUDE[crm_md](includes/crm_md.md)] til að nota til að senda fyrirspurn á vefþjónustu OData um framboð á vörum (afurðum). Nánari upplýsingar er að finna í [Vefþjónustur OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Vefslóð fyrir vefþjónustu Dynamics 365 Business Central OData**|Ef vefþjónusta fyrir ráðstöfun á vöru er virkjuð verður vefslóð fyrir vefþjónustu OData útvegað fyrir þig. Stillið þennan reit á vefslóð fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] tilvikið sem nota á.<br /><br /> Til að endurstilla reitinn á sjálfgefna vefslóð fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], skal velja aðgerðina **Endurstilla vefslóð vefbiðlara** .<br /><br /> Þessi reitur á aðeins við ef [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættingarlausn er sett upp í [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Dynamics 365 Business Central Notandanafn fyrir vefþjónustu OData**|Heiti notandareiknings sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar frá [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData.|
|**Dynamics 365 Business Central Aðgangslykill vefþjónustu OData**|Aðgangslykill fyrir notandareikning sem [!INCLUDE[crm_md](includes/crm_md.md)] notar til að sækja upplýsingar um vöru til ráðstöfunar frá [!INCLUDE[d365fin](includes/d365fin_md.md)] í gegnum vefþjónustu OData. Lyklinum er úthlutað til notanda sem er valinn í reitnum **Dynamics 365 Business Central Notandanafn fyrir vefþjónustu OData** . Til að fá lykilinn skal velja hnappinn **Fletta upp gildi** við hliðina á notandanafninu, velja notandann, velja **Stjórna** og síðan **Breyta** . Á notandaspjaldinu skal velja **Aðgerðir** , **Sannvottun** og síðan velja **Breyta vefþjónustulykli** .|
|**Dynamics 365 SDK útgáfa**|Ef verið er að samþætta við útgáfu á staðnum af [!INCLUDE[crm_md](includes/crm_md.md)], er þetta hugbúnaðarþróunarpakki Dynamics 365 (einnig vísað í sem Xrm) sem er notaður til að tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)]. Útgáfan sem var valin verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)]. Þessi útgáfa sem er til jafns á við eða nýrri en útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)].|-->

Auk ofangreindra stillinga skal færa inn eftirfarandi stillingar fyrir [!INCLUDE[crm_md](includes/crm_md.md)].

| Svæði | Description |
|--|--|
| **Kveikt er á samþættingu sölupöntunar** | Gerðu notendum kleift að senda inn sölupantanir og virkjuð tilboð í [!INCLUDE[crm_md](includes/crm_md.md)] og síðan skoða og vinna úr þeim í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta samþættar ferlið í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna á [Virkja sölupöntunarferli samþættingar](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Stofna sölupantanir sjálfvirkt** | Stofna sölupöntun í [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar notandi stofnar og sendir inn eina í [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Vinna sölutilboð sjálfkrafa** | Vinna úr sölutilboði í [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar notandi stofnar og virkjar eitt slíkt í [!INCLUDE[crm_md](includes/crm_md.md)]. |

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Stöðluð einingavörpun Sales fyrir samstillingu

Einingar í [!INCLUDE[crm_md](includes/crm_md.md)], t.d. pantanir, eru samþættar við jafngildar gerðir af einingum í [!INCLUDE[d365fin](includes/d365fin_md.md)], t.d. sölupantanir. Til að vinna með [!INCLUDE[crm_md](includes/crm_md.md)]-gögn eru tenglar settir upp, kallast tengingar, milli eininga í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Eftirfarandi töflur birta staðlaða vörpun milli eininga í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] sem [!INCLUDE[d365fin](includes/d365fin_md.md)] veitir.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Stefna samstillingar | Sjálfgefin sía |
|--|--|--|--|
| Mælieining | Einingarflokkur | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Vara | Vara | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Tengiliðasía Sales: **Gerð afurðar** er **Birgðir Sales** |
| Forði | Vara | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Tengiliðasía Sales: **Gerð afurðar** er **Þjónusta** |
| Verðflokkur viðskiptamanna | Verðlisti | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Söluverð | Verðlisti vöru | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] tengiliðasía: **Sölukóði** er ekki auður, **Sölugerð** er **Verðflokkur viðskiptamanns** |
| Tækifæri | Tækifæri | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |
| Sölureikningshaus | Reikningsfæra | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Sölureikningslína | Reikningsfæra vöru | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Sölupöntunarhaus | Sölupöntun | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] Sía söluhauss: **Gerð skjals** er Pöntun, **Staða** er útgefin |
| Athugasemdir sölupöntunar | Athugasemdir sölupöntunar | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |

### <a name="synchronization-rules"></a>Samstillingarreglur

Í eftirfarandi töflu eru taldar upp reglurnar sem stjórna samstillingu milli [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta er viðbót við reglur sem skilgreindar eru fyrir Common Data Service, sem eiga einnig við. Frekari upplýsingar er að finna í [Stöðluð einingavörpun](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization).

> [!NOTE]  
> Breytingar á gögnum í  sem voru gerðar af notandareikningi samþættingar eru ekki samstilltar. Mælt er með því að gögnum sé ekki breytt á meðan reikningurinn er notaður. Nánari upplýsingar er að finna í [Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tafla|Regla|
|-----|----|
|Mælieiningar|Mælieiningar eru samstillar við einingahópa í [!INCLUDE[crm_md](includes/crm_md.md)]. Aðeins er hægt að skilgreina eina mælieiningu í einingahópnum.|
|Birgðir|Þegar vörur eru samstilltar við [!INCLUDE[crm_md](includes/crm_md.md)]-vörur mun [!INCLUDE[d365fin](includes/d365fin_md.md)] sjálfkrafa stofna verðlista í [!INCLUDE[crm_md](includes/crm_md.md)]. Til að forðast samstillingarvillur ætti ekki að breyta þessum verðlisti handvirkt.|
|Forði|Tilföng eru samstillt við vörur [!INCLUDE[crm_md](includes/crm_md.md)] sem hafa þjónustu sem vörugerðina.|
|Verðflokkar viðskm.|Verðflokkar viðskiptavinar eru samstilltir við verðlista Sales.|
|Söluverð|Söluverð sem eru með verðflokk viðskiptavinar sem sölugerð og eru með skilgreindan sölukóða eru samstillt við verðlistalínur [!INCLUDE[crm_md](includes/crm_md.md)]|
|Tækifæri|Tækifæri eru samstillt við tækifæri [!INCLUDE[crm_md](includes/crm_md.md)]. Gildið á kóða sölumanns skilgreinir eiganda tengdu einingarinnar í [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bókaðir sölureikningar|Bókaðir sölureikningar eru samstilltir við sölureikninga. Áður en hægt er að samstilla reikning er betra að samstilla allar aðrar einingar sem geta verið hluti af reikningnum, frá sölumanni til verðlista. Gildið á kóða sölumanns í fyrirsögn reiknings skilgreinir eiganda tengdu einingarinnar í Sales.|
|Sölupantanir|Þegar samþætting sölupöntunar er virkjuð eru sölupantanir í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem eru búnar til úr innsendum sölupöntunum í [!INCLUDE[crm_md](includes/crm_md.md)] samstilltar við sölupantanir í TAKA MEÐ SÖLU þegar þær eru gefnar út. Áður en þú samstillir pantanir mælum við með að þú samstillir fyrst allar einingar sem koma við sögu í pöntuninni, t.d. sölufólk og verðlistar. Kóðareitur sölumanns í pöntunarhaus skilgreinir eiganda tengdu einingarinnar í [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Samstillingarverk fyrir samþættingu Sales

Verkin eru keyrð í eftirfarandi röð til að koma í veg fyrir tengsl tenginga milli eininga. Þetta eru aukaleg verk sem eru í boði úr Common Data Service. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](/dynamics365/business-central/admin-job-queues-schedule-tasks).

1. UNITOFMEASURE-samstillingarvinnsla Dynamics 365 Sales  
2. TILFÖNG-AFURÐ fyrir samstillingarvinnslu Dynamics 365 Sales  
3. ITEM-PRODUCT - Dynamics 365 Sales samstillingarverk  
4. CUSTPRCGRP-VERÐ í samstillingarvinnslu Dynamics 365 Sales.
5. SALESPRC-PRODPRICE - Dynamics 365 Sales samstillingarvinnsla.
6. POSTEDSALESINV-INV - Dynamics 365 Sales samstillingarvinnsla.

### <a name="default-synchronization-job-queue-entries"></a>Sjálfgefnar Verkraðarfærslur samstillingar

Eftirfarandi tafla lýsir sjálfgefnu samstillingarverkunum fyrir Sales.  

|Verkraðarfærsla|Description|Stefna|Vörpun samþættingartöflu|Sjálfgefin tíðni samstillinga (mín)|Sjálfgefinn hvíldarstaða vegna aðgerðarleysis (mín.)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|UNITOFMEASURE-samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] einingahópa við [!INCLUDE[d365fin](includes/d365fin_md.md)] mælieiningar.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÆLIEINING|30|720<br> (12 klst.)|
|TILFÖNG-AFURÐ fyrir samstillingarvinnslu Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[d365fin](includes/d365fin_md.md)] tilföng.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|TILFÖNG-VARA|30|720<br> (12 klst.)|
|VARA-AFURÐ- samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[d365fin](includes/d365fin_md.md)] atriði.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|ATRIÐI-VARA|30|1440<br> (24 klst.)|
|CUSTPRCGRP-VERÐ í samstillingarvinnslu Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] söluverðlista við [!INCLUDE[d365fin](includes/d365fin_md.md)] verðflokka viðskiptamanns.| |VERÐFLOKKAR VIÐSKIPTAMANNS-LISTAR SÖLUVERÐS|30|1440<br> (24 klst.)|
|SALESPRC-PRODUCTPRICE-samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] afurðarverð við [!INCLUDE[d365fin](includes/d365fin_md.md)] söluverð.||AFURÐARVERÐ-SÖLUVERÐ|30|1440<br> (24 klst.)|
|POSTEDSALESINV-INV-Dynamics 365 Sales samstillingarvinnsla|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga við [!INCLUDE[d365fin](includes/d365fin_md.md)] bókaða sölureikninga.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|REIKNINGAR-BÓKAÐIR SÖLUREIKNINGAR|30|1440<br> (24 klst.)|
|Talnagögn viðskiptavinar - samstillingarvinnsla Dynamics 365 Sales|Uppfærir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga með nýjustu [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamannagögnunum. Í [!INCLUDE[crm_md](includes/crm_md.md)] birtast upplýsingarnar í **Tölfræði fyrir Business Central-reikning** skjámynd flýtiyfirlits yfir reikninga sem eru tengdir við [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn.<br /><br /> Einnig er hægt að uppfæra þessi gögn handvirkt úr hverri viðskiptamannafærslu. Frekari upplýsingar er að finna í [Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Athugið:** Þessi verkraðarfærsla á aðeins við ef [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættingarlausnin er sett upp í [!INCLUDE[crm_md](includes/crm_md.md)]. |Á ekki við|Á ekki við|30|Á ekki við| 

### <a name="note-for-on-premises-versions"></a>Athugasemd fyrir útgáfur á staðnum

> [!Note]
> Ef verið er að tengja útgáfu á staðnum af [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)] og þú vilt skilgreina tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]-tilvik með tiltekinni gerð sannvottunar skaltu fylla út reitina á flýtiflipanum **Upplýsingar um sannvottunargerð** . Frekari upplýsingar er að finna í [Nota tengistrengi í XRM-verkfærum til að tengjast við Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Ekki er krafist þessa skrefs þegar tengd er netútgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Sjá einnig

[Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sérstilling Business Central og [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
