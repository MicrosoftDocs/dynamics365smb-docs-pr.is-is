---
title: Setja upp aðgang með Microsoft 365 leyfum
description: Leiðarvísir um hvernig stjórnendur geta grunnstillt aðgang að Business Central með Microsoft 365 leyfum.
author: mikebc
ms.author: mikebc
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: '9061,'
---
# <a name="set-up-business-central-access-in-teams-with-microsoft-365-licenses"></a>Setja upp Business Central aðgang í teymum með Microsoft 365 leyfi

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Stjórnendur verða að ljúka mörgum aðgerðum áður en notendur hafa aðgang að [!INCLUDE [prod_short](includes/prod_short.md)] með leyfi sínu Microsoft 365 . Skrefin hér að neðan sýna lágmarksuppsetningu sem þarf til að hefjast handa. Til að fræðast meira um aðgang með Microsoft 365 leyfi er farið í [Business Central Access með Microsoft 365 leyfi](admin-access-with-m365-license.md).

## <a name="guidelines"></a>Leiðbeiningar

Uppsetning aðgangs með Microsoft 365 leyfi felur í sér eftirfarandi verk:

|Skref|Verkefni|Áskilið|
|-|-|-|
|1|[Grunnstilla hvaða Business Central gögn leyfi Microsoft 365 notendur hafa heimild til að skoða](#configure-permissions)|![gátmerki](media/check.png "ávísun")|
|2|[Virkja aðgang með Microsoft 365 leyfi í Business Central umhverfinu](#enable-access-with-microsoft-365-licenses)|![gátmerki](media/check.png "ávísun")|
|3|[Úthluta öryggishópi á umhverfið](#choose-who-gets-access-by-using-security-group)|
|4|[Virkja Business Central forritið fyrir teymi til notenda](#deploy-the-business-central-app-for-teams)|![gátmerki](media/check.png "ávísun")|
|5|[Prófa uppsetninguna](#test-your-setup)||

> [!TIP]
> Fyrir utan síðasta verk er hægt að ljúka verkunum í hvaða röð sem er. Hægt er að vinna verk sérstaklega, eins og lýst er í hlutunum sem fylgja eða nota **Aðgangur með leiðbeiningum Microsoft 365 með** aðstoð við uppsetningu leyfis til að útskýra fyrir þér þau.
>
> Eftirfarandi skref eru framkvæmd til að keyra aðstoðaruppsetninguna:
>
> 1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
> 2. Á síðunni **Aðstoðaruppsetning** er farið í hlutann **Gera meira með Business Central** og Aðgangur valinn **með Microsoft 365 leyfi.**
> 3. Leiðbeiningunum er fylgt.  

## <a name="configure-permissions"></a>Grunnstilla heimildir

[!INCLUDE [prod_short](includes/prod_short.md)] er örugg með hönnun og dregur úr áhættu með því að veita notendum engar heimildir út Microsoft 365 úr kassanum. Stjórnendur verða að grunnstilla heimildir hlutar sem ákvarða hvaða töflur, síður og skýrslur hægt er að nálgast í Teams með aðeins Microsoft 365 leyfi. Þessar heimildir eru fyrstu heimildirnar sem eru úthlutaðar þegar notandi skráir sig inn í fyrsta skipti með Microsoft 365 leyfinu. 

Grunnstilling fyrstu heimilda:

1. Í [!INCLUDE [prod_short](includes/prod_short.md)] skal leita að **leyfisskilgreiningu**.
2. Veldu Microsoft 365 leyfið.
3. Efst á leyfissíðunni **Microsoft 365** skaltu velja breytingartáknið ![Breyta tákni](media/edit-pencil.png) og kveiktu síðan á **Sérsníða heimildir**. 
4. Í hlutanum **Sérsniðnar heimildasamstæður** skaltu bæta við viðeigandi heimildasamstæðum og velja hvort þær eigi við eitt fyrirtæki eða öll fyrirtæki innan umhverfisins.

Með þessari grunnstillingu er notendum með aðeins Microsoft 365 leyfi bætt **við listann Notendur** þegar þeir fá aðgang að [!INCLUDE [prod_short](includes/prod_short.md)] í fyrsta skipti. Nánari upplýsingar um notendur eru í [Stofnun notenda samkvæmt leyfi.](ui-how-users-permissions.md)

> [!NOTE]
> Þegar notendur eru samstilltir við [!INCLUDE [prod_short](includes/prod_short.md)] notendur í Microsoft 365 er aðeins notendum með [!INCLUDE [prod_short](includes/prod_short.md)] leyfi bætt [!INCLUDE [prod_short](includes/prod_short.md)] við notendalistann. Hægt er að fá meiri stjórnunareftirlit með heimildum og forstillingum með því að úthluta öryggishópi til umhverfisins. Þegar umhverfi eru tryggð með því að nota öryggishóp og leyfa aðgang með Microsoft 365 leyfi eru einnig í aðgerðinni **Microsoft 365** Uppfæra notendur **á síðunni Notendur** sem hafa aðeins Microsoft 365 leyfi. Nánari upplýsingar um tryggingaumhverfi má finna [í Manage access með því að nota Microsoft Entra hópa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) í forritaranum og upplýsingatæknihjálpinni.

> [!TIP]
> Ertu að leita að fljótlegri leið til að byrja þegar þú reynir þetta á sandkassa eða matsfyrirtæki? Úthlutaðu heimildasamstæðunni **D365 Lesa** sem veitir heimildir að flestum hlutum.  

Þegar unnið er með margs konar umhverfi þarf að nota grunnstillingu leyfis á hvert umhverfi og það getur verið mismunandi í hverju umhverfi.

Frekari upplýsingar er að finna í [Úthluta heimildum á notendur og hópa](ui-define-granular-permissions.md) og [Búa til heimildasamstæður](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="enable-access-with-microsoft-365-licenses"></a>Virkja aðgang með Microsoft 365 leyfi

Sjálfgefið er slökkt á aðgangi með Microsoft 365 leyfum. Aðgangur verður að vera virkur fyrir hvert umhverfi fyrir sig, sem gefur stjórnendum stjórn og leyfir stigskipta útgáfu í öllu fyrirtækinu. Aðgangur er virkur með því að nota [!INCLUDE [prod_short](includes/prod_short.md)] stjórnunarmiðstöðina: 

1. Í horninu uppi í hægra horninu skal velja **Stillingar** ![.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") > **Stjórnendamiðstöð**  
2. Í stjórnendamiðstöðinni skal velja  **Umhverfi**, síðan velja umhverfið þar sem þú vilt breyta leyfisaðgangi. 
3. Á síðunni **Umhverfisupplýsingar** skaltu velja **Breyta** fyrir stillinguna **Aðgangur með Microsoft 365 leyfum**.
4. Á svæðinu **Microsoft 365 leyfi** skal kveikja á rofanum. 
5. Veldu **Vista** þegar því er lokið og samþykktu staðfestinguna. Breytingin tekur strax gildi.

## <a name="choose-who-gets-access-by-using-security-group"></a>Velja hver fær aðgang með því að nota öryggisflokk

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Í stjórnunarmiðstöð viðskiptamiðstöðarinnar er hægt að tengja umhverfi við einn eða fleiri öryggishópa til að stýra aðgangi. Hægt er að úthluta Microsoft Entra hóp á umhverfið. Með því að Microsoft Entra tengja hóp við umhverfi fá aðeins beinir og óbeinir meðlimir hópsins aðgang að umhverfinu. Óbeinir meðlimir eru notendur í öðrum hópi, sem sjálfur er meðlimur hópsins sem umhverfinu er úthlutað. Þó svo að öllum notendum í Microsoft Entra auðkenni séu bætt við umhverfið þegar þeir eru samstilltir við Microsoft 365 geta aðeins hópmeðlimir skráð sig inn. Nánari upplýsingar fást með því að fara í Stjórna aðgangi með því að [nota Microsoft Entra hópa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) í hjálp forritara og tækni.

## <a name="deploy-the-business-central-app-for-teams"></a>Setja upp Business Central-forritið fyrir Teams

Til [!INCLUDE [prod_short](includes/prod_short.md)] að fá leyfishafa til að deila gögnum í Teymi og fyrir Microsoft 365 leyfishafa til að fá aðgang að þeim gögnum verður hver að hafa forritið [!INCLUDE [prod_short](includes/prod_short.md)] fyrir Teymi uppsett. Þótt notendur geti sett upp forritið á eigin spýtur er mælt með að stjórnendur noti miðlæga innleiðingu. Miðlæg innleiðing gerir þér kleift að færa víðtækari notendahópi forritið í öllu fyrirtækinu og lágmarka einstaklingsframtak notanda. 

Til að læra hvernig á að dreifa forritinu [!INCLUDE [prod_short](includes/prod_short.md)] miðlægt fyrir teymi má sjá [Uppsetning Business Central forritsins með því að nota Centralized Deployment](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Ef þú hefur keyrt miðlæga virkjun áður og aðeins virkjað forritið til öryggishóps leyfis [!INCLUDE [prod_short](includes/prod_short.md)] notenda þarftu að keyra það aftur til að virkja til fleiri hópa eða allt fyrirtækið, eftir því hvernig þú ert að stilla aðgang.

> [!TIP]
> Ertu að leita að fljótlegri leið til að hefjast handa þegar þú prófar þennan eiginleika? Prófa notendur geta sett forritið upp á [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="test-your-setup"></a>Prófaðu uppsetninguna

Til að staðfesta að uppsetningin sé tilbúin fyrir framleiðslu munu eftirfarandi skref hjálpa þér að treysta því að allt virki sem skyldi.

1. Stofna eða auðkenna tvo prufunotendur (A og B).

   - Prófa notanda A verður að hafa [!INCLUDE [prod_short](includes/prod_short.md)] leyfi og Microsoft 365 leyfi með aðgangi að teymi.
   - Prufunotandi B verður að vera aðeins með Microsoft 365 leyfi með aðgang að Teams.

2. Skrá sig inn í [!INCLUDE [prod_short](includes/prod_short.md)] vefbiðlarann sem prófunarnotanda A.

   1. Opnaðu færslu sem prufunotandi B á að hafa aðgang að, t.d. **Birgðaspjald** í viðeigandi fyrirtæki eða umhverfi.
   2. Veldu **Deila** ![!Deildu með öðrum forritum á síðum.](media/share-icon.png) > **Deila með Teams** til að fá upp gluggann „Deila með Teams“.
   3. Í reitnum **Deila með** skaltu bæta við prufunotanda B sem viðtakanda.
   4. Bíddu eftir að tengillinn stækki í spjald og veldu „Deila“.

3. Skráðu þig inn í Microsoft Teams sem prufunotandi B.

   1. Veldu „Spjalla“ og opnaðu samtalið með prufunotanda A.
   2. Veldu upplýsingahnappinn á spjaldinu í skilaboðunum sem prufunotandi A sendi. Ef biðlarinn [!INCLUDE [prod_short](includes/prod_short.md)] birtist og er ritvarinn heppnaðist uppsetningin.

> [!TIP]
> Fór eitthvað úrskeiðis?  [Skoða Business Central úrræðaleit](/troubleshoot/dynamics-365/business-central/welcome-business-central).

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir Business Central Access með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Úrræðaleita aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-troubleshooting.md)  
[Business Central og Microsoft Teams samþætting](across-teams-overview.md)  
