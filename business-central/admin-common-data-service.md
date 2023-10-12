---
title: Notar Microsoft Dataverse
description: Kynning á því hvernig á að samþætta og nota Microsoft Dataverse og hluta þess til að tengjast öðrum Dynamics 365-forritum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dataverse"></a>Samþætta við Microsoft Dataverse

Viðskiptaforrit nota oft gögn frá fleiri en einum uppruna. [!INCLUDE[prod_short](includes/cds_long_md.md)] sameinar gögn í eina stilla af rökfræði sem auðveldar tengingu  [!INCLUDE[prod_short](includes/prod_short.md)]  við önnur Dynamics 365 forrit. Til dæmis  [!INCLUDE[crm_md](includes/crm_md.md)]  eða eigin umsókn byggð á [!INCLUDE[prod_short](includes/cds_long_md.md)]. Til að fræðast meira um  [!INCLUDE[prod_short](includes/cds_long_md.md)], fara í  [Hvað er  Dataverse](/powerapps/maker/common-data-service/data-platform-intro)?.

Eftirfarandi skref veita yfirlit yfir skrefin til að samþætta [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Þessi skref krefjast öryggishlutverksins **Kerfisstjóri** í [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Úthluta leyfum fyrir [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] notenda sem munu nota samþættu forritin.

2. Settu upp tengingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Tengjast við Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Samstilltu gögn milli forrita. Frekari upplýsingar er að finna í [Samstilling Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="get-started-with-"></a>Byrjaðu með [!INCLUDE[prod_short](includes/cds_long_md.md)]

Til að byrja með  [!INCLUDE[prod_short](includes/cds_long_md.md)] Microsoft Power Apps  þarf að fá reikning. Ef þú ert  Power Apps  ekki nú þegar með reikning getur þú fengið einn fyrir frjáls með því að heimsækja  [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc)  og velja  **fá ræsir frjáls**  tengill. Til að fræðast nánar um hvernig hafist er handa  [!INCLUDE[prod_short](includes/cds_long_md.md)] er farið í the  [byrja með  Dataverse](/training/modules/get-started-with-powerapps-common-data-service/)  einingu úr Microsoft þjálfun.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Bi-stefnuor uni-stefnumiðuð gagnasamkeyrsla

Hægt er að samstilla gögn annaðhvort í eða úr einu Dynamics 365 Business App í annað eða í báðar áttir í rauntíma í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ef t.d. er samþætt  [!INCLUDE[prod_short](includes/prod_short.md)]  við  [!INCLUDE[crm_md](includes/crm_md.md)] getur Sölumaður stofnað sölupöntun í  [!INCLUDE[crm_md](includes/crm_md.md)]  og pantað samstillir [!INCLUDE[prod_short](includes/prod_short.md)]. Umráðandi, at frá  [!INCLUDE[crm_md](includes/crm_md.md)], at sölumaðurinn getur kannað ráðstöfunarmagn vörunnar á pöntuninni í [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="standard-and-custom-entities"></a>Staðall og séreiningar

[!INCLUDE[prod_short](includes/cds_long_md.md)] geymir gögn á öruggan hátt í einingatöflum, sem eru safn af færslum sem svipar til hvernig tafla geymir gögn í gagnagrunni. [!INCLUDE[prod_short](includes/cds_long_md.md)] inniheldur grunnsafn staðlaðra tafla sem ná yfir dæmigerðar aðstæður, en einnig er hægt að búa til sérsniðnar töflur sem miðast að fyrirtækinu þínu. Í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að skoða staðlaðar og sérsniðnar töflur sem eru samstilltar á síðunni „Vörpun samþættingartöflu“.

## <a name="about-the-business-central-base-integration-solution"></a>Um grunnsamþættingarlausn Business Central

Grunnsamþættingarlausnin er lykilþáttur samþættingarinnar. Lausnin bætir við nauðsynlegum hlutverkum og aðgangsstigum að notandareikningum fyrir samþættinguna og býr til töflur sem þarf til að varpa [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki í viðskiptaeiningu í [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Sjálfgefið er að  **uppsetningarhandbók fyrir aðstoðaði tengingu  [!INCLUDE[prod_short](includes/cds_long_md.md)]  er sett inn með því að setja upp**  lausnina. Til að gera það notar uppsetningarleiðbeiningin notandareikning stjórnanda sem þú tilgreinir. Þessi reikningur verður að vera gildur notandi í [!INCLUDE[prod_short](includes/cds_long_md.md)] með eftirfarandi öryggishlutverk:

* Kerfisstjóri  

Til að fræðast nánar um notendareikninga er farið í eftirfarandi greinar:

* [Uppsetning notendareikninga fyrir samþættingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Stofna notendur í  Microsoft Dynamics 365 (online)  og úthluta öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Stjórnandareikningurinn er aðeins notaður í eitt skipti við uppsetningu á grunnstillingarbreytingunum sem grunnsamþættingarlausnin gerir í [!INCLUDE[prod_short](includes/cds_long_md.md)]. Eftir að lausnin flytur inn er ekki lengur þörf á reikningnum. Samþætting heldur áfram að nota notandareikninginn sem var búinn sjálfkrafa til fyrir samþættinguna.

Til viðbótar við sérstillingu [!INCLUDE[prod_short](includes/cds_long_md.md)], býr lausnin líka til eftirfarandi hlutverk í [!INCLUDE[prod_short](includes/cds_long_md.md)] fyrir samþættinguna:

* **Samþættingarstjórnandi** - Gerir notendum kleift að stjórna tengingunni milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]. Yfirleitt er þessu hlutverki aðeins úthlutað á notandareikninginn sem er sjálfkrafa stofnaður fyrir samstillingu.  
* **Samþættingarnotandi** - Gerir notendum kleift að fá aðgang að samstilltum gögnum. Yfirleitt er þessu hlutverki úthlutað á eftirfarandi notendareikninga:

  * Notandareikningarnir sem eru stofnaðir sjálfkrafa fyrir samstillingu.
  * Aðrir notendur sem þurfa aðgang að samstilltu gögnunum.

Til að fræðast nánar um hvert hlutverk, svo sem heimildir og aðgangsstig, er farið í að  [Setja upp notendareikninga fyrir samþættingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Þegar tengingin er sett upp er búin til samþættingartöfluvörpun sem samstilla þarf gögn við. Einingar í  [!INCLUDE[prod_short](includes/cds_long_md.md)]  eru kortlagðar í töflum og töflusvæðum í  [!INCLUDE [prod_short](includes/prod_short.md)]  gegnum samþættingartöflur. Til að fá meiri upplýsingar um varpanir er farið í  [staðlaða Einingarvörpun fyrir samstillingu](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="handle-differences-in-local-and-base-transaction-currencies"></a>Meðhöndla mismun á staðbundnum gjaldmiðlum og grunnfærslum

Hægt er að  [!INCLUDE[prod_short](includes/cds_long_md.md)]  tengjast umhverfi sem hefur annan stofn að gjaldmiðli en staðbundinn Gjaldmiðill í [!INCLUDE[prod_short](includes/prod_short.md)]. Tengingin  [!INCLUDE[prod_short](includes/prod_short.md)]  er gerð á  **Dataverse  uppsetningarsíðu**  tengingar eða með því að nota leiðbeiningar um  **uppsetningu tengingar til  Dataverse**  aðstoðar.

Til að hægt sé að tengjast þarf að tryggja að gjaldmiðilsstilling grunnviðskipta í  [!INCLUDE[prod_short](includes/cds_long_md.md)]  hafi gjaldmiðilinn sem er tilgreindur á  **gjaldmiðilssíðunni**  í  [!INCLUDE [prod_short](includes/prod_short.md)] og að minnsta kosti eitt gengi sé tilgreint fyrir gjaldmiðilinn á  **síðunni gengi**  gjaldmiðla.

Hér er dæmi. Þú tengir  [!INCLUDE[prod_short](includes/cds_long_md.md)]  við Euro (EUR) sem er settur sem staðbundinn Gjaldmiðill á  **uppsetningarsíðu**  fjárhags í  [!INCLUDE[prod_short](includes/cds_long_md.md)]  umhverfi sem hefur grunnfærslugjald stillt á Bandaríkjadals (USD). Þú munt þurfa að hafa USD á  **síðunni Gjaldmiðlar**  í  [!INCLUDE [prod_short](includes/prod_short.md)]  og viðeigandi gengi. 

Þegar tengingin  [!INCLUDE[prod_short](includes/cds_long_md.md)] er gerð virk,  [!INCLUDE [prod_short](includes/prod_short.md)]  bætir staðbundinn Gjaldmiðill hans við  **gjaldmiðilinn**  með genginu  [!INCLUDE[prod_short](includes/cds_long_md.md)]  í  **reitnum gjaldmiðilstuðull**  á  **síðunni gengi**  gjaldmiðla.

Gjaldeyrisamsamstilling er einstefnuloka, frá  [!INCLUDE [prod_short](includes/prod_short.md)]  til [! HAFA með  [!INCLUDE[prod_short](includes/cds_long_md.md)] peningaupphæðir umbreyta og samstilla á eftirfarandi hátt:

* Upphæðir í  [!INCLUDE[prod_short](includes/cds_long_md.md)]  grunngjaldmiðlinum umbreyta í  [!INCLUDE [prod_short](includes/prod_short.md)]  staðbundinn gjaldmiðil samkvæmt Síðasta gengissamstillta  [!INCLUDE [prod_short](includes/prod_short.md)] kerfinu.
* Upphæðir í  [!INCLUDE [prod_short](includes/prod_short.md)]  staðbundinni samstillingu með  [!INCLUDE [prod_short](includes/prod_short.md)]  gjaldmiðil landsins í einum af hinum (ekki stofn-) gjaldmiðlunum í [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Sjá einnig .

[Gagnaeignarhaldslíkön](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
