---
title: Samþætting við Dynamics 365 Sales| Microsoft Docs
description: Kynntu þér hvernig þú sækir Dynamics 365 Business Central tilbúið til að samþætta við Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 09edf4a84720085d0accb008b0ae29f47fa38f60
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808770"
---
# <a name="integrating-with-dynamics-365-sales"></a>Samþætting við Dynamics 365 Sales
Hlutverk sölumannsins er oft talið sýnilegasti hlutinn í viðskiptum. Hins vegar getur það gagnast sölumönnum að geta fengið innsýn í viðskiptin og séð hvað er að gerast á bak við tjöldin. Með því að samþætta [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] er hægt að veita sölufólkinu þessa innsýn með því að gera því kleift að skoða upplýsingar í [!INCLUDE[d365fin](includes/d365fin_md.md)] á meðan það vinnur í [!INCLUDE[crm_md](includes/crm_md.md)]. Þegar sölutilboð er undirbúið getur það til dæmis verið gagnlegt að vita hvort nægar birgðir séu til staðar til að uppfylla pöntunina. Frekari upplýsingar er að finna í [Að nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Þessi skref lýsa ferlinu við samþættingu á vefútgáfunum af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar um grunnstillingu á staðnum er að finna í [Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Yfirlit yfir samþættingarferlið
Eftirfarandi skref veita yfirlit yfir skrefin til að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Þessi skref krefjast öryggishlutverksins **Kerfisstjóri** í [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Í Microsoft 365 stjórnendamiðstöðinni skal setja upp notandareikning til að tengja við og samstilla gögn við [!INCLUDE[crm_md](includes/crm_md.md)]. Nánari upplýsingar er að finna í [Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Úthluta leyfum fyrir [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)] notenda sem munu nota samþættu forritin.

3. Settu upp tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Setja upp tengingu við Dynamics 365 Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Valfrjálst: Tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] færslur. Frekari upplýsingar er að finna í [Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md).

5. Samstilltu gögn milli forrita. Frekari upplýsingar er að finna í [Samstilling Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Um samþættingarlausn Business Central
Lausnin gerir fólki kleift að skoða upplýsingar í [!INCLUDE[d365fin](includes/d365fin_md.md)] á meðan unnið er í [!INCLUDE[crm_md](includes/crm_md.md)]. Til að mynda getur hún veitt innsýn inn í tölfræði viðskiptamanna, gert notendum kleift að tengja og skoða færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] úr [!INCLUDE[crm_md](includes/crm_md.md)], og leyft fólki að sjá hvort afurðir séu í boði í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Sjálfgefið er að uppsetningarleiðbeiningar með hjálp fyrir **Setja upp Dynamics 365 Sales tengingu** muni flytja inn samþættingarlausn [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til að gera það nota uppsetningarleiðbeiningarnar notandareikning stjórnanda. Þessi reikningur verður einnig að vera gildur notandi í [!INCLUDE[crm_md](includes/crm_md.md)] með eftirfarandi öryggishlutverkum:

* Kerfisstjóri  
* Lausnastilling  

Frekari upplýsingar er að finna í [Uppsetning notendareikninga fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md), [Búa til notendur í Microsoft Dynamics 365 (online) og úthluta öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) og [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

Þessi reikningur er aðeins notaður einu sinni við uppsetninguna. Þegar lausnin er flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] er ekki lengur þörf á reikningnum. Samþætting heldur áfram að nota notandareikninginn sem var sérstaklega búinn til fyrir samþættinguna.

Til viðbótar við sérstillingu [!INCLUDE[crm_md](includes/crm_md.md)], býr [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættingarlausnin líka til eftirfarandi hlutverk í [!INCLUDE[crm_md](includes/crm_md.md)] fyrir samþættinguna:

* **Samþættingarstjórnandi** - Gerir notendum kleift að stjórna tengingunni milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)]. Venjulega aðeins úthlutað á notandareikninginn fyrir samstillingu.  
* **Samþættingarnotandi** - Gerir notendum kleift að fá aðgang að samstilltum gögnum. Venjulega úthlutað á notandareikninginn fyrir samstillingu og á alla aðra notendur sem þurfa að skoða eða fá aðgang að samstilltum gögnum.
* **Notandi afurðaframboðs** - Gerir notendum kleift að spyrjast fyrir um framboð í [!INCLUDE[d365fin](includes/d365fin_md.md)] úr [!INCLUDE[crm_md](includes/crm_md.md)].

Frekari upplýsingar um hvert hlutverk, t.d. heimildar- og aðgangsstig, er að finna í [Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

Undir lok uppsetningarleiðbeiningar, biður [!INCLUDE[d365fin](includes/d365fin_md.md)] þig um að tengja sölufólk við notendur í [!INCLUDE[crm_md](includes/crm_md.md)]. Færslur í [!INCLUDE[crm_md](includes/crm_md.md)] eru venjulega með eiganda (notanda) úthlutaðan, og ef tenging milli notandans í [!INCLUDE[crm_md](includes/crm_md.md)] og sölumanns í [!INCLUDE[d365fin](includes/d365fin_md.md)] er ekki til mun samstilling ekki takast. Einnig er hægt að gera þetta seinna með því að nota aðgerðina **Tengja sölumenn** á síðunni **Microsoft Dynamics 365 Uppsetning tengingar**.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við Dynamics 365 Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Samstilling á Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
