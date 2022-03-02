---
title: Notar Microsoft Dataverse
description: Kynning á því hvernig á að samþætta og nota Microsoft Dataverse og hluta þess til að tengjast öðrum Dynamics 365-forritum.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 06/14/2021
ms.openlocfilehash: 95b1146f2f664ad73966162e24c3e0ad0c34e310
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141438"
---
# <a name="integrating-with-microsoft-dataverse"></a>Tengir við Microsoft Dataverse


Viðskiptaforrit nota oft gögn frá fleiri en einum uppruna. [!INCLUDE[prod_short](includes/cds_long_md.md)] sameinar gögn í einn grunn sem auðveldar að tengja önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða þitt eigið forrit smíðað ofan á [!INCLUDE[prod_short](includes/cds_long_md.md)], við [!INCLUDE[prod_short_md](includes/prod_short.md)]. Frekari upplýsingar um [!INCLUDE[prod_short](includes/cds_long_md.md)] er að finna í [Hvað er Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)

Eftirfarandi skref veita yfirlit yfir skrefin til að samþætta [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Þessi skref krefjast öryggishlutverksins **Kerfisstjóri** í [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Úthluta leyfum fyrir [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] notenda sem munu nota samþættu forritin.

2. Settu upp tengingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Tengjast við Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Samstilltu gögn milli forrita. Frekari upplýsingar er að finna í [Samstilling Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-prod_short"></a>Hafist handa með [!INCLUDE[prod_short](includes/cds_long_md.md)]
Til að hefjast handa með [!INCLUDE[prod_short](includes/cds_long_md.md)] þarf Microsoft Power Apps reikning. Ef þú ert ekki þegar með Power Apps-reikning er hægt að fá einn ókeypis með því að fara á [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og velja tengilinn **Hefjumst handa ókeypis**. Frekari upplýsingar um hvernig hafist er handa með [!INCLUDE[prod_short](includes/cds_long_md.md)] er að finna í einingunni [Hafist handa með Dataverse](/learn/modules/get-started-with-powerapps-common-data-service/) úr Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Gagnasamstilling í báðar áttir eða aðra áttina
Háð viðskiptaþörfum, er hægt að setja upp samþættinguna til að samstilla gögn annaðhvort til eða frá einu Dynamics 365 viðskiptaforriti til annars, eða í báðar áttir í næstum rauntíma í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ef þú til dæmis samþættar [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[crm_md](includes/crm_md.md)] í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)] getur sölumaður búið til sölupöntun í [!INCLUDE[crm_md](includes/crm_md.md)] og pöntunin verður samstillt við [!INCLUDE[prod_short](includes/prod_short.md)]. Á móti, úr [!INCLUDE[crm_md](includes/crm_md.md)], getur sölumaður skoðað upplýsingar úr [!INCLUDE[prod_short](includes/prod_short.md)] um framboð vörunnar í pöntuninni. 

## <a name="standard-and-custom-entities"></a>Staðlaðar og sérsniðnar einingar
[!INCLUDE[prod_short](includes/cds_long_md.md)] geymir gögn á öruggan hátt í einingatöflum, sem eru safn af færslum sem svipar til hvernig tafla geymir gögn í gagnagrunni. [!INCLUDE[prod_short](includes/cds_long_md.md)] inniheldur grunnsafn staðlaðra tafla sem ná yfir dæmigerðar aðstæður, en einnig er hægt að búa til sérsniðnar töflur sem miðast að fyrirtækinu þínu. Í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að skoða staðlaðar og sérsniðnar töflur sem eru samstilltar á síðunni „Vörpun samþættingartöflu“.

## <a name="about-the-business-central-base-integration-solution"></a>Um grunnsamþættingarlausn Business Central

Grunnsamþættingarlausnin er lykilþáttur samþættingarinnar. Lausnin bætir við nauðsynlegum hlutverkum og aðgangsstigum að notandareikningum fyrir samþættinguna og býr til töflur sem þarf til að varpa [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki í viðskiptaeiningu í [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Uppsetningarleiðbeining **Setja upp [!INCLUDE[prod_short](includes/cds_long_md.md)] tengingu** með hjálp flytur lausnina inn að sjálfgefnu. Til að gera það notar uppsetningarleiðbeiningin notandareikning stjórnanda sem þú tilgreinir. Þessi reikningur verður að vera gildur notandi í [!INCLUDE[prod_short](includes/cds_long_md.md)] með eftirfarandi öryggishlutverk:

* Kerfisstjóri  

Frekari upplýsingar er að finna í [Uppsetning notandareikninga fyrir samþættingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) og [Búa til notendur í Microsoft Dynamics 365 (online) og úthluta öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Stjórnandareikningurinn er aðeins notaður í eitt skipti við uppsetningu á grunnstillingarbreytingunum sem grunnsamþættingarlausnin gerir í [!INCLUDE[prod_short](includes/cds_long_md.md)]. Þegar lausnin hefur verið flutt inn er ekki lengur þörf á reikningnum. Samþætting heldur áfram að nota notandareikninginn sem var búinn sjálfkrafa til fyrir samþættinguna.

Til viðbótar við sérstillingu [!INCLUDE[prod_short](includes/cds_long_md.md)], býr lausnin líka til eftirfarandi hlutverk í [!INCLUDE[prod_short](includes/cds_long_md.md)] fyrir samþættinguna:

* **Samþættingarstjórnandi** - Gerir notendum kleift að stjórna tengingunni milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]. Venjulega eru þessu aðeins úthlutað á notandareikninginn sem er búinn til sjálfkrafa fyrir samstillingu.  
* **Samþættingarnotandi** - Gerir notendum kleift að fá aðgang að samstilltum gögnum. Venjulega er þessu úthlutað á notandareikninginn sem er sjálfkrafa búinn til fyrir samstillingu og á aðra notendur sem þurfa að skoða eða fá aðgang að samstilltum gögnum.

Frekari upplýsingar um hvert hlutverk, t.d. heimildar- og aðgangsstig, er að finna í [Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Við uppsetningu tengingar eru varpanir samþættingartöflu, sem þarf til að samstilla gögn, búnar til. Einingum í [!INCLUDE[prod_short](includes/cds_long_md.md)] er varpað í töflur og töflureiti í Business Central í gegnum samþættingartöflur. Frekari upplýsingar er að finna í [Stöðluð einingavörpun fyrir samstillingu](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-also"></a>Sjá einnig
[Gagnaeignarhaldslíkön](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->





[!INCLUDE[footer-include](includes/footer-banner.md)]