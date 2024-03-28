---
title: Setja upp aðgang með Microsoft 365 leyfum
description: Leiðarvísir um hvernig stjórnendur geta grunnstillt aðgang að Business Central með Microsoft 365 leyfum.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: '9061,'
---
# Setja upp miðlægu aðgengi fyrir fyrirtæki í teymum með  Microsoft 365  leyfi

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Stjórnendur verða að ljúka mörgum verkþáttum áður en notendur geta nálgast  [!INCLUDE [prod_short](includes/prod_short.md)]  með leyfi sínu Microsoft 365 . Skrefin hér að neðan sýna lágmarksuppsetningu sem þarf til að hefjast handa. Frekari upplýsingar um aðgang með  Microsoft 365  leyfum er að fá með því að fara í  [miðborg Business með  Microsoft 365  leyfum](admin-access-with-m365-license.md).

## Leiðbeiningar

Uppsetning aðgangs með  Microsoft 365  leyfi felur í sér eftirfarandi verkefni:

|Skref|Verkefni|Áskilið|
|-|-|-|
|1|[Skilgreina hvaða viðskipti aðalgögn  Microsoft 365  sem notendur hafa leyfi til að skoða](#configure-permissions)|![gátmerki](media/check.png "ávísun")|
|2|[Virkja aðgang með  Microsoft 365  leyfum á miðbæjarumhverfi fyrirtækja](#enable-access-with-microsoft-365-licenses)|![gátmerki](media/check.png "ávísun")|
|3|[Úthluta öryggisflokki á umhverfið](#choose-who-gets-access-by-using-security-group)|
|4|[Virkjaðu Viðskiptablaðið miðlægt í App fyrir hópana fyrir notendur](#deploy-the-business-central-app-for-teams)|![gátmerki](media/check.png "ávísun")|
|5|[Prófa uppsetninguna](#test-your-setup)||

> [!TIP]
> Að frátöldum Síðasta verkhluta er hægt að ljúka verkefnunum í hvaða röð sem er. Hægt er að gera verk sérstaklega eins og lýst er í köflunum sem fylgja eða nota  **aðganginn með aðstoð Uppsetningarleiðbeiningar með  Microsoft 365  leyfi**  til að útskýra fyrir þér þær.
>
> Ef keyra á uppsetningu aðstoðar er eftirfarandi skrefum fylgt:
>
> 1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
> 2.  **Á síðunni aðstoðar-Uppsetning**  er farið í  **gera meira með miðlægu viðskiptamiðinu**  og valið  **aðgangur með  Microsoft 365  leyfum**.
> 3. Fylgið leiðbeiningunum.  

## Grunnstilla heimildir

[!INCLUDE [prod_short](includes/prod_short.md)] er örugg með því að hanna og lágmarka áhættu með því að  Microsoft 365  veita ekki heimildir notendum út úr kassanum. Stjórnendur verða að grunnstilla heimildir hlutar sem ákvarða hvaða töflur, síður og skýrslur hægt er að nálgast í Teams með aðeins Microsoft 365 leyfi. Þessar heimildir eru fyrstu heimildirnar sem eru úthlutaðar þegar notandi skráir sig inn í fyrsta skipti með Microsoft 365 leyfinu. 

Grunnstilling fyrstu heimilda:

1. Inn  [!INCLUDE [prod_short](includes/prod_short.md)], leita að  **skilgreiningu** leyfis.
2. Veldu Microsoft 365 leyfið.
3. Efst á leyfissíðunni **Microsoft 365** skaltu velja breytingartáknið ![Breyta tákni](media/edit-pencil.png) og kveiktu síðan á **Sérsníða heimildir**. 
4. Í hlutanum **Sérsniðnar heimildasamstæður** skaltu bæta við viðeigandi heimildasamstæðum og velja hvort þær eigi við eitt fyrirtæki eða öll fyrirtæki innan umhverfisins.

Með þessari skilgreiningu er notendum eingöngu fengið  Microsoft 365  leyfi bætt  **við lista yfir notendur**  þegar þeir komast  [!INCLUDE [prod_short](includes/prod_short.md)]  í fyrsta sinn. Nánari upplýsingar um notendur fara í að búa til  [notendur samkvæmt leyfum](ui-how-users-permissions.md).

> [!NOTE]
> Aðeins notendum sem hafa  [!INCLUDE [prod_short](includes/prod_short.md)]  leyfi er bætt  Microsoft 365 við notendalista á listanum  [!INCLUDE [prod_short](includes/prod_short.md)]  [!INCLUDE [prod_short](includes/prod_short.md)] þegar notendur eru samstilltir. Nánari reglur um stjórn heimilda og snið er hægt að tengja öryggisflokk við umhverfið. Þegar umhverfi er tryggt með því að nota öryggiaflokk og virkja aðgang með  Microsoft 365  leyfum,  **taka uppfærslunotendur úr  Microsoft 365**  aðgerð  **·**  einnig notendur  Microsoft 365  með leyfi. Til að fræðast um umhverfi gæsalaka er  [stjórnað aðgangi með því að nota  Microsoft Entra  flokka](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups)  í HÖNNUÐINUM og það hjálpar.

> [!TIP]
> Ertu að leita að fljótari leið til að byrja þegar þú reynir að koma þessari aðgerð á sandkassa eða mat fyrirtækis? Úthlutaðu heimildasamstæðunni **D365 Lesa** sem veitir heimildir að flestum hlutum.  

Þegar unnið er með margs konar umhverfi þarf að nota grunnstillingu leyfis á hvert umhverfi og það getur verið mismunandi í hverju umhverfi.

Frekari upplýsingar er að finna í [Úthluta heimildum á notendur og hópa](ui-define-granular-permissions.md) og [Búa til heimildasamstæður](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## Virkja aðgang með  Microsoft 365  leyfum

Sjálfgefið er slökkt á aðgangi með Microsoft 365 leyfum. Aðgangur verður að vera virkur fyrir hvert umhverfi fyrir sig, sem gefur stjórnendum stjórn og leyfir stigskipta útgáfu í öllu fyrirtækinu. Þú kveikir á aðgangi með því að  [!INCLUDE [prod_short](includes/prod_short.md)]  nota admin Center: 

1. Í efra hægra horninu skal velja  **stillingar** ![.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") > **Stjórnendamiðstöð**  
2. Í stjórnendamiðstöðinni skal velja  **Umhverfi**, síðan velja umhverfið þar sem þú vilt breyta leyfisaðgangi. 
3. Á síðunni **Umhverfisupplýsingar** skaltu velja **Breyta** fyrir stillinguna **Aðgangur með Microsoft 365 leyfum**.
4. Á svæðinu **Microsoft 365 leyfi** skal kveikja á rofanum. 
5. Veldu **Vista** þegar því er lokið og samþykktu staðfestinguna. Breytingin tekur strax gildi.

## Veldu hver fær aðgang með því að nota öryggisflokk

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Í stjórnstöðinni stjórnun er hægt að úthluta umhverfi í einn eða fleiri öryggishópa til að stýra aðgangi. Hægt er að tengja  Microsoft Entra  hóp við umhverfið. Með því að úthluta  Microsoft Entra  hópi á umhverfi fá aðeins beinir og Óbeinir Meðlimir flokksins aðgang að umhverfinu. Óbeinir meðlimir eru notendur í öðrum flokki, sem sjálfir tilheyra þeim hópi sem er tengdur umhverfinu. Þó öllum leyfi notendum  Microsoft Entra  Kenni verði bætt við umhverfið þegar samstillt er við  Microsoft 365 það geta aðeins Meðlimir í hópi skráð sig inn. Til að fá frekari upplýsingar er farið að  [stjórna aðgangi með því að nota  Microsoft Entra  hópa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups)  í Hönnuðinum og það hjálpar.

## Setja upp Business Central-forritið fyrir Teams

 [!INCLUDE [prod_short](includes/prod_short.md)] Leyfi leyfishafa til að samnýta gögn í teymum og fyrir  Microsoft 365  leyfishafa til að fá aðgang að gögnum þarf að hafa  [!INCLUDE [prod_short](includes/prod_short.md)]  App fyrir teymi uppsett. Þótt notendur geti sett upp forritið á eigin spýtur er mælt með að stjórnendur noti miðlæga innleiðingu. Miðlæg innleiðing gerir þér kleift að færa víðtækari notendahópi forritið í öllu fyrirtækinu og lágmarka einstaklingsframtak notanda. 

Til að læra hvernig á að  [!INCLUDE [prod_short](includes/prod_short.md)]  nota forritið í miðlægu forriti fyrir teygur, sjá  [Uppsetning Business Central App með miðstýringu virkjunar](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Ef keyrð hefur verið miðlæg innleiðing áður og forritið virkjað það í öryggisflokknum fyrir leyfða  [!INCLUDE [prod_short](includes/prod_short.md)]  notendur þarf að keyra það aftur til að virkja fleiri flokka eða allt skipulagið eftir því hvernig aðgangur er skilgreindur.

> [!TIP]
> Ertu að leita að fljótlegri leið til að hefjast handa þegar þú prófar þennan eiginleika? Prófunarnotendur geta sett upp App kl [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## Prófaðu uppsetninguna

Til að staðfesta að uppsetningin sé tilbúin fyrir framleiðslu munu eftirfarandi skref hjálpa þér að treysta því að allt virki sem skyldi.

1. Stofna eða auðkenna tvo prufunotendur (A og B).

   - Prófunarnotandi A þarf að hafa  [!INCLUDE [prod_short](includes/prod_short.md)]  leyfi og  Microsoft 365  leyfi fyrir aðgangi að teymum.
   - Prufunotandi B verður að vera aðeins með Microsoft 365 leyfi með aðgang að Teams.

2. Skráðu þig inn í  [!INCLUDE [prod_short](includes/prod_short.md)]  vefbiðlarann sem Prófunarnotanda A.

   1. Opnaðu færslu sem prufunotandi B á að hafa aðgang að, t.d. **Birgðaspjald** í viðeigandi fyrirtæki eða umhverfi.
   2. Veldu **Deila** ![!Deildu með öðrum forritum á síðum.](media/share-icon.png) > **Deila með Teams** til að fá upp gluggann „Deila með Teams“.
   3. Í reitnum **Deila með** skaltu bæta við prufunotanda B sem viðtakanda.
   4. Bíddu eftir að tengillinn stækki í spjald og veldu „Deila“.

3. Skráðu þig inn í Microsoft Teams sem prufunotandi B.

   1. Veldu „Spjalla“ og opnaðu samtalið með prufunotanda A.
   2. Veldu upplýsingahnappinn á spjaldinu í skilaboðunum sem prufunotandi A sendi. Ef biðlarinn  [!INCLUDE [prod_short](includes/prod_short.md)]  birtist og er skrifvarin var uppsetningin árangursrík.

> [!TIP]
> Fór eitthvað úrskeiðis? Athugaðu [Úrræðaleita aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-troubleshooting.md).

## Sjá einnig .

[Yfirlit yfir miðlægu aðgengi fyrirtækja með  Microsoft 365  leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Úrræðaleita aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-troubleshooting.md)  
[Business Central og Microsoft Teams samþætting](across-teams-overview.md)  
