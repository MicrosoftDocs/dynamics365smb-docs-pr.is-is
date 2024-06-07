---
title: Setja upp tölvupóstskráningu
description: Kynntu þér hvernig tölvupóstsamskipti milli sölufólks og viðskiptavina geta skapað alvöru sölutækifærum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 09/18/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
ms.service: dynamics-365-business-central
---
# Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Fá meira út úr samskiptum milli sölufólks og viðskiptamanna með því að breyta tölvupóstsamskiptum í tækifæri sem hægt er að nýta. [!INCLUDE[prod_short](includes/prod_short.md)] getur unnið með Exchange Online til að halda skrá yfir skilaboð á inn- og útleið. Þú getur skoðað og greint innihald skilaboða á síðunni **Samskiptaskráningarfærslur**.

> [!IMPORTANT]
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] online,og [!INCLUDE[prod_short](includes/prod_short.md)]  Exchange Online  verður að vera á sama leigjanda.

## Til að setja upp tölvupóstskráningu

### Setja upp almennar möppur og reglur fyrir innskráningu tölvupósts Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Næst tengir þú [!INCLUDE[prod_short](includes/prod_short.md)] við Exchange Online.

### Setja upp samnýtt pósthólf og reglur um innskráningu tölvupósts Exchange Online

> [!NOTE]
> Þessi skref krefjast stjórnandaaðgangs fyrir Exchange Online.

Útbúa sameiginlegt pósthólf í stjórnunarmiðstöð Exchange. Einnig er hægt að nota Exchange Online PowerShell. Frekari upplýsingar er að finna í [Búa til samnýtt pósthólf](/microsoft-365/admin/email/create-a-shared-mailbox) eða [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Ef þú notar Exchange Management PowerShell eru breytingar þínar tiltækar í stjórnunarmiðstöð Exchange eftir töf. Seinkunin gæti verið margar klukkustundir.

### Bæta við notandareikningi fyrir meðlimi samnýtta pósthólfsins

Reikningurinn sem þú notar fyrir tölvupóstsskráningu er Exchange Online reikningur. Áætlað verk mun nota reikninginn til að tengjast samnýtta pósthólfinu og vinna úr tölvupóstum. Þessi reikningur ætti ekki að vera tengdur tilteknum aðila. Bæta netfanginu við fyrir samnýtta pósthólfið. Frekari upplýsingar er að finna í [Nota EAC til að breyta úthlutun samnýtts pósthólfs](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### Leyfa öðrum notendum að sjá skráða tölvupósta

Þú getur leyft öðrum notanda að opna tölvupóstskeyti í Exchange sem tengist samskiptaskráningarfærslu úr [!INCLUDE[prod_short](includes/prod_short.md)]. Til að gera það skaltu veita notandanum ``Read`` aðgangsheimild að möppu **Safnvistunar** í samnýtta pósthólfinu. Frekari upplýsingar er að finna í [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### Stofna póstflæðisreglur

Póstflæðisreglur leita að ákveðnum skilyrðum á skeytum og gera aðgerðir á þeim. Búa til tvær reglur um póstflæði út frá upplýsingunum í eftirfarandi töflu Frekari upplýsingar er að finna á [Reglum um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Aðgerðum reglu um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Tilgangur  |Nafn  |Nota þessa reglu ef ...  |Gera eftirfarandi ...  |
|---------|---------|---------|---------|
|Regla fyrir móttekinn tölvupóst     |Skrá tölvupóst sem sendur er til þessa fyrirtækis|Sendandi er staðsettur utan fyrirtækis og viðtakandinn er staðsettur innan fyrirtækis|Sendu falið afrit af tölvupóstsreikningnum sem er tilgreindur fyrir samnýtta pósthólfið.|
|Regla fyrir sendan tölvupóst     |Skrá tölvupóst sem sendur er frá þessu fyrirtæki|Sendandi er staðsettur innan fyrirtækisins og viðtakandinn er staðsettur utan fyrirtækis|Sendu falið afrit af tölvupóstsreikningnum sem er tilgreindur fyrir samnýtta pósthólfið.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] vinnur aðeins úr skeytum í innhólfinu í samnýtta pósthólfinu. Ef regla færir skeyti úr innhólfinu í aðra möppu verður ekki unnið úr þessum skeytum. Þar að auki eru skeyti í ruslpóstinum líka hunsuð.

## Setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að skrá tölvupóstskeyti

Hafist handa með tölvupóstskráningu í tveimur einföldum skrefum:

1. Tengdu [!INCLUDE[prod_short](includes/prod_short.md)] við Exchange Online fyrir Microsoft 365 áskriftina þína. Exchange Online sér um tölvupóstskilaboðin þín. Við höfum einfaldað þetta skref með því að bjóða upp á uppsetningarleiðbeiningar. Þú þarft bara innskráningarupplýsingar stjórnanda fyrir stjórnandareikning þinn í Microsoft 365. Til að hefja leiðsögnina skaltu opna síðuna **Uppsetning með hjálp** og velja síðan **Setja upp tölvupóstskráningu**.  

2. Gakktu úr skugga um að netföng sölufólks þíns og tengiliða í [!INCLUDE[prod_short](includes/prod_short.md)] séu gild. Til að gera það fyrir hvern viðskiptavin eða sölumann skal opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** og kíkja í reitinn **Netfang**.

    > [!Tip]
    > Eftir að þú hefur lokið skrefum leiðsagnarinnar geturðu athugað hvort tengingin hafi borið árangur. Leita að skráningu **tölvupósts, velja** Aðgerðir **og velja** svo Staðfesta uppsetningu **.**

## Skoða póstskipti í samskiptakladda

[!INCLUDE[prod_short](includes/prod_short.md)] býr til færslu á síðunni **Samskiptaskrá** í hvert skipti sem sölumaður og tengiliður skiptast á tölvupóstskilaboðum. Til að skoða samskiptaskrána skaltu opna spjaldið **Tengiliður** fyrir einstaklinginn og velja síðan **Tengt**, **Ferill** og að lokum velja **Samskiptaskráningarfærslur**. Við getum gert nokkra hluti við hverja færslu í skránni, til dæmis:

* Skoðaðu innihald tölvupóstsins sem var sendur á milli með því að velja **Vinna** og svo **Sýna viðhengi**.
* Breyttu tölvupóstsamskiptum í sölutækifæri. Þú getur skapað tækifæri úr færslu sem lofar góðu og náð sölu út úr henni. Til að breyta tölvupóstskiptum í tækifæri skaltu velja færsluna, síðan **Ferli** og síðan **Búa til tækifæri**. Nánari upplýsingar er að finna í [Umsjón sölutækifæra](marketing-manage-sales-opportunities.md).

## Takmarkanir á pósthólfi og möppu í Exchange Online

Það eru takmörk á pósthólfi og möppu í Exchange Online, eins og takmarkanir á möppustærð og fjölda skeyta. Nánari upplýsingar eru [Exchange Online í takmörkun](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) og [takmörkun á almennum möppum í Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] geymir skráð tölvupóstskeyti í möppu í Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] geymir einnig tengil á sérhvert skráð skeyti. Tenglarnir opna skráð skeyti í Exchange Online á síðunum Samskiptaskráningarfærsla, Tengiliðaspjald og Sölumannaspjald í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef skráð skeyti er fært yfir í aðra möppu verður tengillinn rofinn. Til dæmis er hægt að færa skeyti handvirkt eða Exchange Online gæti ræst AutoSplit sjálfkrafa þegar geymslumörkum er náð.

Eftirfarandi skref geta hjálpað þér að koma í veg fyrir að rjúfa tengla á skeyti í Exchange Online.

1. Ekki færa skeyti sem þegar eru til yfir í aðra möppu eftir að þú hefur breytt stillingum fyrir uppsetningu tölvupóstsskráningarinnar. Að halda fyrirliggjandi skeytum þar sem þau eru mun viðhalda tenglunum. Tenglar á skilaboð í nýju möppunni verða gildir.
2. Forðastu að ná mörkum pósthólfs og möppu. Ef þú ert að fara að ná að mörkunum skaltu gera eftirfarandi:
    1. Setja upp nýtt samnýtt pósthólf í Exchange Online.
    2. Uppfærðu póstflæðisreglurnar í Exchange Online.
    3. Uppfærðu uppsetningu tölvupóstsskráningar í Business Central í samræmi við það

## Tengjast útgáfum innanhúss við Microsoft Exchange

Hægt er að tengja [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss við Exchange innanhúss eða Exchange Online fyrir tölvupóstsskráningu. Fyrir báðar útgáfur af Exchange eru stillingar fyrir tenginguna í boði á síðunni **Uppsetning markaðssetningar**. Fyrir Exchange Online er einnig hægt að nota uppsetningarleiðbeiningar með hjálp.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## Tengjast við Exchange Online

Til að Exchange Online tengjast þarf að skrá forrit í Microsoft Entra kenni. Gefðu upp forritskennið, leynilykil lyklageymslu og framsendingarslóðina til að nota fyrir skráninguna. Framsendingarslóðin er forstillt og ætti að virka fyrir flestar uppsetningar. Nánari upplýsingar eru [í Til að skrá forrit í Microsoft Entra kenni til að tengjast frá Business Central til Exchange Online](#to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-exchange-online). 

Nota þarf **OAuth2** sem **Sannvottunargerð**. Einnig þarf að skrá jöfnun í Microsoft Entra kenni. Gefðu upp forritskennið, leynilykil lyklageymslu og framsendingarslóðina til að nota fyrir skráninguna. Framsend vefslóð er fyllt út fyrirfram og ætti að virka fyrir flestar uppsetningar. Nánari upplýsingar eru í Til að skrá forrit í Microsoft Entra kenni til að tengjast frá Business Central til hér að Exchange Online neðan.

Nauðsynlegt er að setja upp uppsetninguna til að nota HTTPS. Frekari upplýsingar er að finna í [Skilgreining SSL til að tryggja örugga tengingu vefbiðlara Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Ef verið er að setja upp þjóninn til að hafa aðra heimasíðu er hægt að breyta vefslóðinni. Leynilykill biðlara verða vistaður sem dulkóðaður strengur í gagnagrunninum.

### Til að skrá forrit í Microsoft Entra kenni til tengingar frá Business Central til Exchange Online

Eftirfarandi skref gera ráð fyrir því að kenni séu notuð Microsoft Entra til að vinna með auðkenni og aðgang. Frekari upplýsingar er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app). 

1. Í Azure-gáttinni, undir **Stjórna**, skal velja **Sannvottun**.
2. Undir **Framsendingarslóð** skal bæta við framsendingarslóðinni sem mælt er með á síðunni **Tölvupóstsskráning** í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef reitur framsendingarslóðar á síðu tölvupóstsskráningar er auður skal finna ráðlagða framsendingarslóð á síðunni **Uppsetning með hjálp**. Til að opna síðuna skaltu fara á síðunni **Tölvupóstsskráning**, velja **Aðgerðir** og svo **Uppsetning með hjálp**.

    > [!NOTE]
    > Ef framsendingarslóðin er ekki tilgreind er hægt að gera það seinna með því að velja **Bæta við verkvangi** og síðan velja **Vef** til að bæta við vefforritinu og framsendingarvefslóðinni.

3. Undir **Stjórna** skal velja **API-heimildir** og velja **Microsoft Graph** og síðan velja **Úthlutaðar heimildir**.
4. Notaðu leitarreitinn til að finna og velja **Póst** og bættu síðan við heimildinni **Mail.ReadWrite.Shared**. 
5. Undir **Stjórna** skal velja **Vottorð og leynilyklar** og síðan stofna nýjan leynilykil fyrir forritið. Þú munt nota leynilykilinn annaðhvort í reitnum **Leynilykill biðlara** á síðunni **Tölvupóstsskráning** í [!INCLUDE[prod_short](includes/prod_short.md)].
6. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. Þetta er biðlarakenni forritsins. Þú verður að slá það inn annaðhvort í reitinn **Biðlarakenni** á síðunni **Tölvupóstsskráning**.
7. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal setja upp tölvupóstsskráningu á síðunni **Tölvupóstsskráning** eða nota leiðbeininguna **Hjálparuppsetning** til að fá aðstoð.

### Nota annað auðkenni og fá aðgang að stýringarþjónustu

Ef kenni er ekki notað Microsoft Entra til að stjórna auðkenni og aðgangi þarf hjálp frá forritara. Ef þú kýst frekar að geyma forritskennið og leynilykilinn á annarri staðsetningu, geturðu skilið reiti biðlarakennis og leynilykils biðlara eftir auða og skrifað viðbót til að sækja auðkennið og leynilykilinn frá staðsetningunni. Hægt er að gefa upp leynilykilinn við keyrslu með því að gerast áskrifandi að tilvikum OnGetEmailLoggingClientId og OnGetEmailLoggingClientSecret tilvikum í codeunit 1641 „Uppsetning tölvupóstskráningar“.

## Að hefja skráningu tölvupósts

1. Til að hefja skráningu tölvupósts skal á síðunni **Tölvupóstsskráning** velja **Virkja**.
2. Skráðu þig inn með Exchange Online reikningnum sem áætlað verk notar til að tengjast samnýtta pósthólfinu og vinna úr tölvupóstum.

    > [!NOTE]
    > Ef þú ert ekki beðin(n) um að skrá þig inn á Exchange Online reikninginn gæti það verið vegna þess að vafrinn þinn lokar á sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr https://login.microsoftonline.com.

## Að hætta að skrá tölvupóst

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tölvupóstsskráning** og velja síðan viðkomandi tengil.
2. Slökkva skal á víxlhnappnum **Virkjað**.

## Til að breyta notandareikningi sem er notaður við tölvupóstsskráningu

### [!INCLUDE[prod_short](includes/prod_short.md)] Á netinu

1. Skráðu þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] með reikningnum sem áætlað verk mun nota til að tengjast samnýtta pósthólfinu og vinna úr tölvupóstum. Þessi reikningur verður að hafa aðgang að bæði [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tölvupóstsskráning** og velja síðan viðkomandi tengil. 
3. Veldu **Tengt** og síðan **Verkraðarfærsla**.
4. Endurræstu verkinu **Tölvupóstsskráning**.

### [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tölvupóstsskráning** og velja síðan viðkomandi tengil.
2. Veldu **Aðgerðir** og síðan **Endurnýja lykil**.
3. Skráðu þig inn með Exchange Online reikningnum sem áætlað verk notar til að tengjast samnýtta pósthólfinu og vinna úr tölvupóstum.

## Sjá einnig
[Stjórnun tengsla](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]