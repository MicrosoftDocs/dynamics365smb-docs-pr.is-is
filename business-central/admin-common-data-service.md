---
title: Notar Common Data Service
description: Kynning á Common Data Service og íhlutum þess.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 85823e93b1d239bf4e59ec6a8872cdc4a2cef9c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911581"
---
# <a name="integrating-with-common-data-service"></a>Tengir við Common Data Service

Viðskiptaforrit nota oft gögn frá fleiri en einum uppruna. [!INCLUDE[d365fin](includes/cds_long_md.md)] sameinar gögn í einn grunn sem auðveldar að tengja önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða þitt eigið forrit smíðað ofan á [!INCLUDE[d365fin](includes/cds_long_md.md)], við [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Frekari upplýsingar um [!INCLUDE[d365fin](includes/cds_long_md.md)] er að finna í [Hvað er Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Eftirfarandi skref veita yfirlit yfir skrefin til að samþætta [!INCLUDE[d365fin](includes/cds_long_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Þessi skref krefjast öryggishlutverksins **Kerfisstjóri** í [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Úthluta leyfum fyrir [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)] notenda sem munu nota samþættu forritin.

2. Settu upp tengingu við [!INCLUDE[d365fin](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Tengjast við Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Samstilltu gögn milli forrita. Frekari upplýsingar er að finna í [Samstilling Business Central og Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Hafist handa með [!INCLUDE[d365fin](includes/cds_long_md.md)]
Til að hefjast handa með [!INCLUDE[d365fin](includes/cds_long_md.md)] þarf Microsoft Power Apps reikning. Ef þú ert ekki þegar með Power Apps-reikning er hægt að fá einn ókeypis með því að fara á [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og velja tengilinn **Hefjumst handa ókeypis** . Frekari upplýsingar um hvernig hafist er handa með [!INCLUDE[d365fin](includes/cds_long_md.md)] er að finna í einingunni [Hafist handa með Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) úr Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Gagnasamstilling í báðar áttir eða aðra áttina
Háð viðskiptaþörfum, er hægt að setja upp samþættinguna til að samstilla gögn annaðhvort til eða frá einu Dynamics 365 viðskiptaforriti til annars, eða í báðar áttir í næstum rauntíma í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)]. Ef þú til dæmis samþættar [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)] í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)] getur sölumaður búið til sölupöntun í [!INCLUDE[crm_md](includes/crm_md.md)] og pöntunin verður samstillt við [!INCLUDE[d365fin](includes/d365fin_md.md)]. Á móti, úr [!INCLUDE[crm_md](includes/crm_md.md)], getur sölumaður skoðað upplýsingar úr [!INCLUDE[d365fin](includes/d365fin_md.md)] um framboð vörunnar í pöntuninni. 

## <a name="standard-and-custom-entities"></a>Staðlaðar og sérsniðnar einingar
[!INCLUDE[d365fin](includes/cds_long_md.md)] geymir gögn á öruggan hátt í einingasafni, sem eru safn af færslum sem svipar til hvernig tafla geymir gögn í gagnagrunni. [!INCLUDE[d365fin](includes/cds_long_md.md)] inniheldur grunnsafn staðlaðra eininga sem ná yfir dæmigerðar aðstæður, en einnig er hægt að búa til sérsniðnar einingar sem miðast að fyrirtækinu þínu. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að skoða staðlaðar og sérsniðnar einingar sem eru samstilltar á síðunni „Vörpun samþættingartöflu“.

## <a name="about-the-base-cds-integration-solution"></a>Um CDS-grunnsamþættingarlausnina

CDS-grunnsamþættingarlausnin er lykilþáttur samþættingarinnar. Lausnin bætir við nauðsynlegum hlutverkum og aðgangsstigum að notandareikningum fyrir samþættinguna og býr til einingar sem þarf til að varpa [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtæki í viðskiptaeiningu í [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

Uppsetningarleiðbeining **Setja upp [!INCLUDE[d365fin](includes/cds_long_md.md)] tengingu** með hjálp flytur lausnina inn að sjálfgefnu. Til að gera það notar uppsetningarleiðbeiningin notandareikning stjórnanda sem þú tilgreinir. Þessi reikningur verður að vera gildur notandi í [!INCLUDE[d365fin](includes/cds_long_md.md)] með eftirfarandi öryggishlutverk:

* Kerfisstjóri  

Frekari upplýsingar er að finna í [Uppsetning notandareikninga fyrir samþættingu við [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) og [Búa til notendur í Microsoft Dynamics 365 (online) og úthluta öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Reikningur stjórnanda er notaður aðeins einu sinni við uppsetningu vegna breytinga á grunnstillingu sem CDS-grunnlausn er að gera í [!INCLUDE[d365fin](includes/cds_long_md.md)]. Þegar lausnin hefur verið flutt inn er ekki lengur þörf á reikningnum. Samþætting heldur áfram að nota notandareikninginn sem var búinn sjálfkrafa til fyrir samþættinguna.

Til viðbótar við sérstillingu [!INCLUDE[d365fin](includes/cds_long_md.md)], býr lausnin líka til eftirfarandi hlutverk í [!INCLUDE[d365fin](includes/cds_long_md.md)] fyrir samþættinguna:

* **Samþættingarstjórnandi** - Gerir notendum kleift að stjórna tengingunni milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]. Venjulega eru þessu aðeins úthlutað á notandareikninginn sem er búinn til sjálfkrafa fyrir samstillingu.  
* **Samþættingarnotandi** - Gerir notendum kleift að fá aðgang að samstilltum gögnum. Venjulega er þessu úthlutað á notandareikninginn sem er sjálfkrafa búinn til fyrir samstillingu og á aðra notendur sem þurfa að skoða eða fá aðgang að samstilltum gögnum.

Frekari upplýsingar um hvert hlutverk, t.d. heimildar- og aðgangsstig, er að finna í [Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Við uppsetningu tengingar eru varpanir samþættingartöflu, sem þarf til að samstilla gögn, búnar til. Einingum í Common Data Service er varpað í töflur og töflureiti í Business Central í gegnum samþættingartöflur. Frekari upplýsingar er að finna í [Stöðluð einingavörpun fyrir samstillingu](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Sjá einnig
[Gagnaeignarhaldslíkön](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



