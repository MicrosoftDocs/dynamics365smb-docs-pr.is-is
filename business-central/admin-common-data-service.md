---
title: Samþætta við Microsoft Dataverse með samstillingu gagna
description: Kynning á því hvernig á að samþætta og nota Microsoft Dataverse og hluta þess til að tengjast öðrum Dynamics 365-forritum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.search.form: 7214_Primary
ms.service: dynamics-365-business-central
---

# Samþætta við Microsoft Dataverse með samstillingu gagna

Viðskiptaforrit nota oft gögn frá fleiri en einum uppruna. [!INCLUDE[prod_short](includes/cds_long_md.md)] sameinar gögn í eitt safn af rökfræði sem auðveldar tengingu við [!INCLUDE[prod_short](includes/prod_short.md)] önnur Dynamics 365 forrit. Til dæmis, [!INCLUDE[crm_md](includes/crm_md.md)]  eða eigin forrit byggt á [!INCLUDE[prod_short](includes/cds_long_md.md)]. Til að fræðast meira um [!INCLUDE[prod_short](includes/cds_long_md.md)] er farið í [Hvað er Dataverse](/powerapps/maker/common-data-service/data-platform-intro)?.

Eftirfarandi skref veita yfirlit yfir skrefin til að samþætta [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Þessi skref krefjast öryggishlutverksins **Kerfisstjóri** í [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Úthluta leyfum fyrir [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] notenda sem munu nota samþættu forritin.

2. Settu upp tengingu við [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Tengjast við Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Samstilltu gögn milli forrita. Frekari upplýsingar er að finna í [Samstilling Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## Hafist handa við [!INCLUDE[prod_short](includes/cds_long_md.md)]

Til að byrja með [!INCLUDE[prod_short](includes/cds_long_md.md)] þarftu reikning Microsoft Power Apps . Ef þú ert ekki þegar með Power Apps reikning getur þú fengið einn ókeypis með því að [heimsækjapowerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og velja **Að byrja ókeypis**  tengja. Til að fræðast meira um hvernig hafist er handa er [!INCLUDE[prod_short](includes/cds_long_md.md)] hafist handa með [því að fara í eininguna Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) í Microsoft-þjálfuninni.

## Samstilling tvístefnulegra eða uni-stefnumiðaðra gagna

Hægt er að samstilla gögn annaðhvort til eða frá einu Dynamics 365 viðskiptaforriti til annars eða í báðar áttir í nánast rauntíma, í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ef t.d. er samþætt [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[crm_md](includes/crm_md.md)] getur sölumaður stofnað sölupöntun í [!INCLUDE[crm_md](includes/crm_md.md)] og pöntunin samstillt við [!INCLUDE[prod_short](includes/prod_short.md)]. Samt sem á móti [!INCLUDE[crm_md](includes/crm_md.md)] getur sölumaðurinn kannað ráðstöfunarmagn vörunnar í pöntuninni í [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Staðlaðar og sérsniðnar einingar

[!INCLUDE[prod_short](includes/cds_long_md.md)] geymir gögn á öruggan hátt í einingatöflum, sem eru safn af færslum sem svipar til hvernig tafla geymir gögn í gagnagrunni. [!INCLUDE[prod_short](includes/cds_long_md.md)] inniheldur grunnsafn staðlaðra tafla sem ná yfir dæmigerðar aðstæður, en einnig er hægt að búa til sérsniðnar töflur sem miðast að fyrirtækinu þínu. Í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að skoða staðlaðar og sérsniðnar töflur sem eru samstilltar á síðunni „Vörpun samþættingartöflu“.

## Um grunnsamþættingarlausn Business Central

Grunnsamþættingarlausnin er lykilþáttur samþættingarinnar. Lausnin bætir við nauðsynlegum hlutverkum og aðgangsstigum að notandareikningum fyrir samþættinguna og býr til töflur sem þarf til að varpa [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki í viðskiptaeiningu í [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Sjálfgefið **er að uppsetningarleiðbeiningar með aðstoð setja upp [!INCLUDE[prod_short](includes/cds_long_md.md)] tengingu** flytji inn lausnina. Til að gera það notar uppsetningarleiðbeiningin notandareikning stjórnanda sem þú tilgreinir. Þessi reikningur verður að vera gildur notandi í [!INCLUDE[prod_short](includes/cds_long_md.md)] með **öryggishlutverk kerfisstjóra** .  

Til að fræðast meira um notendareikninga er farið í eftirfarandi greinar:

* [Uppsetning notendareikninga til samþættingar [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Stofna notendur í Microsoft Dynamics 365 (online) og úthluta öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Stjórnandareikningurinn er aðeins notaður í eitt skipti við uppsetningu á grunnstillingarbreytingunum sem grunnsamþættingarlausnin gerir í [!INCLUDE[prod_short](includes/cds_long_md.md)]. Eftir innflutning lausnarinnar er ekki lengur þörf á reikningnum. Samþætting heldur áfram að nota notandareikninginn sem var búinn sjálfkrafa til fyrir samþættinguna.

Auk sérstillinga [!INCLUDE [cds_long_md](includes/cds_long_md.md)] stofnar lausnin einnig öryggishlutverk í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] fyrir samþættinguna:

* **Business Central Dataverse Samþætting** - Gerir þér kleift að stjórna tengingunni milli [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Yfirleitt er þessu hlutverki aðeins úthlutað á notandareikninginn sem er sjálfkrafa stofnaður í samstillingu. Nánari upplýsingar um þetta hlutverk fást með því að [fara í Uppsetning notendareikninga til samþættingar. [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)

Þegar tengingin er sett upp eru búnar til samþættingartafla vörpun sem þarf til að samstilla gögn. Einingum í er varpað á [!INCLUDE[prod_short](includes/cds_long_md.md)] töflur og töflureiti í [!INCLUDE [prod_short](includes/prod_short.md)] með samþættingartöflum. Nánari upplýsingar um vörpun fást með því að [fara í Staðlaða einingu vörpun fyrir samstillingu](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Meðhöndla mismun í staðbundnum gjaldmiðlum og grunnfærslum

Hægt er að [!INCLUDE[prod_short](includes/cds_long_md.md)] tengja við umhverfi sem er með annan grunngjaldmiðil en staðbundinn gjaldmiðill í [!INCLUDE[prod_short](includes/prod_short.md)]. Tenging er gerð á [!INCLUDE[prod_short](includes/prod_short.md)] síðunni **Dataverse Uppsetning** tengingar eða með því að nota **Setja upp tengingu til uppsetningarleiðsagnar Dataverse** með aðstoð.

Til að geta tengst þarf að tryggja að gjaldmiðilsstilling grunnviðskipta í [!INCLUDE[prod_short](includes/cds_long_md.md)] sé með gjaldmiðilinn sem stilltur er á **síðunni Gjaldmiðlar** í [!INCLUDE [prod_short](includes/prod_short.md)] og að minnsta kosti eitt gengi er tilgreint fyrir gjaldmiðilinn á síðunni **Gengi gjaldmiðils** .

Hér er dæmi. Þú ert að tengjast [!INCLUDE[prod_short](includes/cds_long_md.md)] evru (EUR) sem staðbundinn gjaldmiðill á fjárhagur uppsetningarsíðunni **við** umhverfi sem er með grunnfærslugjaldmiðil stilltur á [!INCLUDE[prod_short](includes/cds_long_md.md)]  Bandaríkjadali (USD). Þú þarft að hafa USD á síðunni **Gjaldmiðlar** í [!INCLUDE [prod_short](includes/prod_short.md)] og viðeigandi gengi. 

Þegar tenging [!INCLUDE[prod_short](includes/cds_long_md.md)] er gerð virk við bætir [!INCLUDE [prod_short](includes/prod_short.md)]  staðbundinn gjaldmiðill **hennar við gjaldmiðilseininguna**  [!INCLUDE[prod_short](includes/cds_long_md.md)] með genginu úr reitnum **Gengisstuðull** á síðunni **Gengi gjaldmiðils** .

Gjaldmiðilssamstilling er einstefnuleg, allt frá [!INCLUDE [prod_short](includes/prod_short.md)] til [! TAKA MEÐ [!INCLUDE[prod_short](includes/cds_long_md.md)], umbreyta upphæðum og samstilla á eftirfarandi hátt:

* Upphæðir í grunngjaldmiðlinum [!INCLUDE[prod_short](includes/cds_long_md.md)] breytast [!INCLUDE [prod_short](includes/prod_short.md)]  í staðbundinn gjaldmiðill byggðar á því gengi sem síðast var samstillt úr [!INCLUDE [prod_short](includes/prod_short.md)].
* Upphæðir í [!INCLUDE [prod_short](includes/prod_short.md)]  staðbundinn gjaldmiðill samstilla við [!INCLUDE [prod_short](includes/prod_short.md)]  staðbundinn gjaldmiðill í öðrum (óstofnuðum) gjaldmiðlum í [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Hvað gerist þegar fyrirtæki er afritað

Hægt er að afrita fyrirtæki sem eru samþætt [!INCLUDE[prod_short](includes/cds_long_md.md)] eða [!INCLUDE[crm_md](includes/crm_md.md)] á öruggan hátt. Afritun fyrirtækja dregur úr hættu á ósamræmi í gögnum og getur sparað verðmætasköpun. Til að [fræðast meira um afritun fyrirtækja er farið í Afrita fyrirtæki](about-new-company.md#copy-a-company).

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## Sjá einnig .

[Gagnaeignarhaldslíkön](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
