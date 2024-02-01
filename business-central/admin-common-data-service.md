---
title: Samþætta við Microsoft Dataverse með samstillingu gagna
description: Kynning á því hvernig á að samþætta og nota Microsoft Dataverse og hluta þess til að tengjast öðrum Dynamics 365-forritum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="integrate-with-microsoft-dataverse-via-data-sync"></a>Samþætta við Microsoft Dataverse með samstillingu gagna

Viðskiptaforrit nota oft gögn frá fleiri en einum uppruna. [!INCLUDE[prod_short](includes/cds_long_md.md)] sameinar gögn í eitt sett af rökfræði sem gerir það auðveldara að tengjast [!INCLUDE[prod_short](includes/prod_short.md)] við önnur Dynamics 365 forrit. Til dæmis, [!INCLUDE[crm_md](includes/crm_md.md)] eða þitt eigið forrit byggt á [!INCLUDE[prod_short](includes/cds_long_md.md)]. Til að læra meira um [!INCLUDE[prod_short](includes/cds_long_md.md)] skaltu fara á [Hvað er Dataverse](/powerapps/maker/common-data-service/data-platform-intro)?.

Eftirfarandi skref veita yfirlit yfir skrefin til að samþætta [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Þessi skref krefjast öryggishlutverksins **Kerfisstjóri** í [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Úthluta leyfum fyrir [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] notenda sem munu nota samþættu forritin.

2. Settu upp tengingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Tengjast við Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Samstilltu gögn milli forrita. Frekari upplýsingar er að finna í [Samstilling Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="get-started-with-"></a>Byrjaðu með [!INCLUDE[prod_short](includes/cds_long_md.md)]

Til að byrja með [!INCLUDE[prod_short](includes/cds_long_md.md)] þarftu Microsoft Power Apps reikning. Ef þú ert ekki nú þegar með Power Apps reikning geturðu fengið einn ókeypis með því að fara á [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og velja **Byrjaðu ókeypis** hlekkur. Til að læra meira um hvernig á að byrja með [!INCLUDE[prod_short](includes/cds_long_md.md)] skaltu fara í [Byrjaðu með Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) einingunni frá Microsoft þjálfun.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Tvíátta eða einátta gagnasamstilling

Þú getur samstillt gögn annað hvort við eða frá einu Dynamics 365 viðskiptaforriti í annað, eða í báðar áttir í næstum rauntíma, í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Til dæmis, ef þú samþættir [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[crm_md](includes/crm_md.md)], getur sölumaður búið til sölupöntun í [!INCLUDE[crm_md](includes/crm_md.md)] og pöntunin samstillist við [!INCLUDE[prod_short](includes/prod_short.md)]. Aftur á móti, frá [!INCLUDE[crm_md](includes/crm_md.md)], getur söluaðili athugað framboð á hlutnum í pöntuninni í [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="standard-and-custom-entities"></a>Staðlaðar og sérsniðnar einingar

[!INCLUDE[prod_short](includes/cds_long_md.md)] geymir gögn á öruggan hátt í einingatöflum, sem eru safn af færslum sem svipar til hvernig tafla geymir gögn í gagnagrunni. [!INCLUDE[prod_short](includes/cds_long_md.md)] inniheldur grunnsafn staðlaðra tafla sem ná yfir dæmigerðar aðstæður, en einnig er hægt að búa til sérsniðnar töflur sem miðast að fyrirtækinu þínu. Í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að skoða staðlaðar og sérsniðnar töflur sem eru samstilltar á síðunni „Vörpun samþættingartöflu“.

## <a name="about-the-business-central-base-integration-solution"></a>Um grunnsamþættingarlausn Business Central

Grunnsamþættingarlausnin er lykilþáttur samþættingarinnar. Lausnin bætir við nauðsynlegum hlutverkum og aðgangsstigum að notandareikningum fyrir samþættinguna og býr til töflur sem þarf til að varpa [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki í viðskiptaeiningu í [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Sjálfgefið er að  **Uppsetning [!INCLUDE[prod_short](includes/cds_long_md.md)] tenging** uppsetningarhandbókin flytur lausnina inn. Til að gera það notar uppsetningarleiðbeiningin notandareikning stjórnanda sem þú tilgreinir. Þessi reikningur verður að vera gildur notandi í [!INCLUDE[prod_short](includes/cds_long_md.md)] með **kerfisstjóra** öryggishlutverkinu.  

Til að læra meira um notendareikninga skaltu fara í eftirfarandi greinar:

* [Setja upp notendareikninga til að samþætta við [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Búðu til notendur í Microsoft Dynamics 365 (online) og úthlutaðu öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Stjórnandareikningurinn er aðeins notaður í eitt skipti við uppsetningu á grunnstillingarbreytingunum sem grunnsamþættingarlausnin gerir í [!INCLUDE[prod_short](includes/cds_long_md.md)]. Eftir að lausnin hefur verið flutt inn er ekki lengur þörf á reikningnum. Samþætting heldur áfram að nota notandareikninginn sem var búinn sjálfkrafa til fyrir samþættinguna.

Auk þess að sérsníða [!INCLUDE [cds_long_md](includes/cds_long_md.md)], skapar lausnin einnig öryggishlutverk í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] fyrir samþættinguna:

* **Business Central Dataverse Samþætting** - Gerir þér kleift að stjórna tengingunni milli [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Venjulega er þessu hlutverki aðeins úthlutað á notandareikninginn sem er sjálfkrafa búinn til fyrir samstillingu. Til að læra meira um þetta hlutverk skaltu fara í [Setja upp notendareikninga til að samþætta við [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Þegar þú setur upp tenginguna býrðu til samþættingartöflukortin sem þú þarft til að samstilla gögn. Einingum í [!INCLUDE[prod_short](includes/cds_long_md.md)] eru varpað á töflur og töflureitir í [!INCLUDE [prod_short](includes/prod_short.md)] í gegnum samþættingartöflur. Til að læra meira um kortlagningu skaltu fara í [Staðlað einingakortlagning fyrir samstillingu](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="handle-differences-in-local-and-base-transaction-currencies"></a>Meðhöndla mun á staðbundnum gjaldmiðlum og grunnviðskiptum

Þú getur tengst [!INCLUDE[prod_short](includes/cds_long_md.md)] umhverfi sem hefur annan grunngjaldmiðil en staðbundinn gjaldmiðill í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú gerir tenginguna í [!INCLUDE[prod_short](includes/prod_short.md)] á  **Dataverse Tengiuppsetning** síðunni eða með því að nota **Setja upp tengingu við Dataverse** uppsetningarleiðbeiningar með aðstoð.

Til að geta tengst skaltu ganga úr skugga um að grunnstilling gjaldmiðils í [!INCLUDE[prod_short](includes/cds_long_md.md)]  hafi þann gjaldmiðil sem stilltur er á  **Gjaldmiðlum** síðunni í [!INCLUDE [prod_short](includes/prod_short.md)], og að minnsta kosti eitt gengi er tilgreint fyrir gjaldmiðilinn á síðunni **Gengi gjaldmiðla** .

Hér er dæmi. Þú ert að tengjast [!INCLUDE[prod_short](includes/cds_long_md.md)] með evru (EUR) sem er stillt sem staðbundinn gjaldmiðill á **uppsetningarsíðunni** á [!INCLUDE[prod_short](includes/cds_long_md.md)]  umhverfi sem hefur grunnviðskiptagjaldmiðil stillt á Bandaríkjadal (USD). Þú þarft að hafa USD á  **Gjaldmiðlum** síðunni í [!INCLUDE [prod_short](includes/prod_short.md)] og viðeigandi gengi. 

Þegar þú virkjar tenginguna við [!INCLUDE[prod_short](includes/cds_long_md.md)] bætir [!INCLUDE [prod_short](includes/prod_short.md)]  staðbundnum gjaldmiðli sínum við **Gjaldmiðill** eininguna í [!INCLUDE[prod_short](includes/cds_long_md.md)] með genginu frá **Gjaldmiðilsstuðull** reitnum á  **Gengigjaldmiðla** síðunni.

Samstilling gjaldmiðils er einstefnu, frá [!INCLUDE [prod_short](includes/prod_short.md)] í [!INCLUDE [!INCLUDE[prod_short](includes/cds_long_md.md)], peningaupphæðir umbreyta og samstilla sem hér segir:

* Upphæðir í [!INCLUDE[prod_short](includes/cds_long_md.md)] grunngjaldmiðlinum breytast í [!INCLUDE [prod_short](includes/prod_short.md)] innlendan gjaldmiðil miðað við nýjasta gengi samstillt frá [!INCLUDE [prod_short](includes/prod_short.md)].
* Upphæðir í [!INCLUDE [prod_short](includes/prod_short.md)] innlendum gjaldmiðli samstillast við [!INCLUDE [prod_short](includes/prod_short.md)] innlenda gjaldmiðilinn í einum af hinum (ekki grunn) gjaldmiðlum í [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Sjá einnig .

[Gagnaeignarhaldslíkön](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
