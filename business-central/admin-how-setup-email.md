---
title: Setja upp email í Business Central (inniheldur Video)
description: Lýsir því hvernig á að tengja tölvupóstsreikninga við Business Central til að hægt sé að senda skilaboð á útleið án þess að opna annað forrit.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.search.form: 1805, 9813, 9814, 1262, 1263
ms.date: 02/06/2022
ms.author: bholtorf
ms.openlocfilehash: 22bd7fcf0eff9b3f7c41975a32127d9d482c42cc
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534292"
---
# <a name="set-up-email"></a>Setja upp tölvupóst
Fólk í viðskiptum sendir upplýsingar og skjöl á borð við sölu- og innkaupapantanir og reikninga með tölvupósti á hverjum degi. Kerfisstjórar geta tengt einn eða fleiri tölvupóstreikninga við til [!INCLUDE[prod_short](includes/prod_short.md)] að senda skjöl án þess að þurfa að opna App fyrir tölvupóst. Hægt er að setja hvert boð fyrir sig með grunnsniðs verkfærum, svo sem leturgerðum, stílum, litum o. s. frv., og bæta viðhengjum um allt að 100 MB. Auk þess gera skýrsluskipanir kerfisstjóra kleift að taka aðeins með helstu upplýsingar úr skjölum. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Tölvupóstsgetu í eru aðeins fyrir skilaboð á [!INCLUDE[prod_short](includes/prod_short.md)] útleið. Ekki er hægt að fá svör, þ.e. það er engin "innsend" síða í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Aðeins er hægt að nota möguleika tölvupósts fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu með Exchange Online. Við styðjum ekki Hybrid-aðstæður, eins og tengingu [!INCLUDE[prod_short](includes/prod_short.md)] á netinu við útgáfu innanhúss.
> 
> Ef þú ert að nota [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss, áður en þú getur sett upp tölvupóst þarftu að búa til App skráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Azure gáttinni. Forritsskráningin gerir [!INCLUDE[prod_short](includes/prod_short.md)] kleift að heimila og sannvotta hjá tölvupóstþjónustu þinni. Frekari upplýsingar eru í [Uppsetning tölvupósts fyrir Business Central á staðnum](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). Á [!INCLUDE[prod_short](includes/prod_short.md)] netinu sjáum við um þetta fyrir þig.

## <a name="required-permissions"></a>Nauðsynlegar heimildir
Til að setja upp tölvupóst þarf að hafa heimildasamstæðuna **UPPSETNING TÖLVUPÓSTS**. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Bæta við tölvupóstreikningum
Tölvupóstsreikningum er bætt við í gegnum viðbætur sem gera reikningum frá mismunandi þjónustuaðilum kleift að tengjast við [!INCLUDE[prod_short](includes/prod_short.md)]. Stöðluðu viðaukunum sleppir þú notar lykla af Microsoft Exchange netinu. Hins vegar eru aðrir Viðaukar sem láta þig tengja reikninga frá öðrum veitum, eins og Gmail, gætu verið tiltækir.

Hægt er að tilgreina fyrirfram skilgreindar viðskiptaáætlanir þar sem nota á tölvupóstreikning til að senda tölvupóst. Til dæmis er hægt að tilgreina að allir notendur sendi söluskjöl frá einum reikningi og innkaupaskjöl frá öðrum. Frekari upplýsingar er að finna í [Úthluta aðstæðum tölvupósts á tölvupóstsreikninga](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Eftirfarandi tafla lýsir þeim tölvupóstsviðbótum sem eru sjálfgefið í boði.

|Viðbót  |Lýsing  |Dæmi um notkun  |
|---------|---------|---------|
|**Microsoft 365 Connector**|Allir senda tölvupóst úr samnýttu pósthólfi í Exchange Online.|Þegar öll skilaboð koma frá sömu deildinni sem dæmi, þá sendir sölufyrirtækið skilaboð frá reikningnum sales@cronus.com. Þessi valkostur krefst þess að sett sé upp samnýtt pósthólf í Microsoft 365 admin Center. Frekari upplýsingar eru í [Samnýtt pósthólf](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Núverandi notandaviðmót**|Allir senda tölvupóst frá reikningnum sem var notaður til að skrá sig inn á [!INCLUDE[prod_short](includes/prod_short.md)].|Leyfa samskipti frá reikningum einstaklinga.|
|**SMTP tengi**|Nota skal SMTP-samskiptareglu til að senda tölvupósta.|Leyfa skal samskipti í gegnum SMTP-póstþjóninn. |

> [!NOTE]
> Í **Microsoft 365 tengivirkinu** og **núgildandi notendaviðmóti** nota þeir reikningarnir sem settir voru upp fyrir notendur í Microsoft 365 stjórnstöðinni fyrir Microsoft 365 áskriftina. Til að senda tölvupóst með viðbótunum verða notendur að vera með gilt leyfi fyrir Exchange Online. Að auki, í sandkassa umhverfi, þurfa þessir Viðaukar að **Leyfa stillingu httpclient beiðni** er virkjuð. Til að athuga hvort hún sé virk fyrir þessa viðauka er farið á **síðuna Viðaukar**, nafn valið og síðan **er valkosturinn samskipa** valinn.

> Utanaðkomandi notendur, eins og fulltrúar viðurkenningar og utanbókarnotenda, geta ekki notað þessa viðauka til að senda tölvupóstskeyti frá [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="using-smtp"></a>Notkun SMTP
Ef nota á SMTP-samskiptareglur til að senda tölvupóst frá [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að nota VIÐAUKANN SMTP Connector. Þegar settur er upp lykill sem notar SMTP er gerð sendanda mikilvægur reitur. Ef valinn er sérstakur notandi verður tölvupóstur sendur með nafni og öðrum upplýsingum af reikningnum sem verið er að setja upp. Ef valið er notandi verður tölvupóstur hins vegar sendur úr tölvupóstreikningnum sem tilgreindur er fyrir reikning hvers notanda. Núgildandi notandi er svipaður og aðgerðin senda. Frekari upplýsingar er að finna [í use staðgengill sendanda í tölvupósti](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages) á útleið. 

> [!IMPORTANT]
> Ef þú notar [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss er hægt að nota OAuth 2,0 til auðkenningar. Það verður að stofna jöfnunarskráningu í Azure gáttina og keyra síðan uppsetningarleiðbeiningu sem **sett er upp Azure Active Directory** í [!INCLUDE[prod_short](includes/prod_short.md)] til að tengjast við Azure AD. Frekari upplýsingar er að finna í [Búa til forritsskráningu fyrir Business Central í Azure-gátt](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).

## <a name="add-email-accounts"></a>Bæta tölvupóstreikningum við
Uppsetningarleiðbeiningarnar **Setja upp tölvupóst** með hjálp geta komið þér af stað með tölvupósta.

> [!NOTE]
> Þú verður að vera með sjálfgefinn tölvupóstsreikning, jafnvel þó svo þú notir aðeins einn reikning. Sjálfgefinn lykill verður notaður fyrir allar tölvupóstaðstæður sem eru ekki tengdar við lykil. Frekari upplýsingar er að finna í [Úthluta aðstæðum tölvupósts á tölvupóstsreikninga](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Setja upp tölvupóstreikninga** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Úthluta aðstæðum tölvupósts á tölvupóstsreikninga
Tölvupóstaðstæður eru ferlar sem fela í sér að senda skjal. T.d. sölu-eða innkaupapöntun eða tilkynningu um slíkt, t.d. boð til ytri endurskoðanda. Sérstaka tölvupóstreikninga má nota við tilteknar aðstæður. Til dæmis er hægt að tilgreina að allir notendur sendi alltaf söluskjöl frá einum reikningi, innkaupaskjöl frá öðrum og vöruhúsa- eða framleiðsluskjöl frá þriðja reikningi. Hægt er að úthluta, rökstyðja og fjarlægja áætlanir þegar óskað er. Aðeins er hægt að úthluta atburðarás á einn tölvupóstlykil í einu. Sjálfgefinn Tölvupóstreikningur verður notaður fyrir allar aðstæður sem eru ekki tengdar við lykil.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-view-policies"></a>Setja upp Skoðunarreglur
Hægt er að stýra þeim tölvupósti sem notandi getur séð í Bréfapóstum og sent tölvupósta síður.

**Á Notendaskoðunarreglum** tölvupóstsins skal velja notanda og velja síðan einn af eftirtöldum valkostum í **tölvupóstskoða stefnu** svæðisins:

* **Skoða eigin tölvupóst** -notandinn getur aðeins skoðað eigin tölvupóstskeyti.
* **Skoða allan tölvupóst** -notandinn getur skoðað öll tölvupóstskilaboð, þar á meðal tölvupóst sem aðrir notendur Sendu.
* **Skoða hvort aðgangur að öllum tengdum færslum** -þessi Skoðunarregla er notuð ef engin önnur regla er tilgreind. Notandi getur skoðað tölvupóst sem aðrir notendur senda ef notandinn hefur aðgang að skráningunni sem send var og öllum tengdum skráningum. Til dæmis er notanda sendur Bókaður sölureikningur til viðskiptamanns. Notandi B. getur séð í tölvupóstinum hvort þeir hafi aðgang að bæði reikningnum og viðskiptavininum.
* **Skoða ef aðgangur að tengdum færslum** -notandinn getur skoðað tölvupóstskilaboð sem voru send af öðrum ef notandinn hefur aðgang að að minnsta kosti einni færslu sem tengist færslunni sem var send. Til dæmis er notanda sendur Bókaður sölureikningur til viðskiptamanns. Notandi B. getur séð í tölvupóstinum hvort þeir hafi aðgang að annaðhvort reikningnum eða viðskiptavininum.

> [!NOTE]
>  **Ef reiturinn NOTANDAKENNI** er auður og síðan er valið stefnuaðgerð tölvupóstsins, er sú regla sem skilgreind er á við um alla notendur tilgreind.

## <a name="set-up-reusable-email-texts-and-layouts"></a>Setja upp Endurnýtanlegan Senditexta og skipulag
Hægt er að nota skýrslur til að taka með helstu upplýsingar úr sölu-og innkaupaskjölum í texta fyrir tölvupóst. Þetta ferli lýsir því hvernig á að setja upp skýrsluna **Sala - Reikningur** fyrir bókaða sölureikninga, en ferlið er svipað fyrir aðrar skýrslur.

> [!NOTE]
> Ef nota á útlitið til að búa til efni fyrir tölvupóstskeyti verður að nota Word-skrárgerðina fyrir útlitið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skýrsluval - Sala** og velja síðan viðkomandi tengil.
2. Á síðunni **Skýrsluval - Sala** í reitnum **Notkun** skal velja **Reikningur**.
3. Í nýrri línu í reitnum **Skýrslukenni** skal velja t.d. staðlaða skýrslu 1306.
4. Veljið gátreitinn **Nota fyrir meginmál tölvupósts**.
5. Veljið reitinn **Lýsing á útliti meginmáls tölvupósts** og veljið síðan útlit í listanum.

    Skipulag skýrslu skilgreina stíl og innihald textans í tölvupósti. Efnið gæti til dæmis innihaldið texta eins og kveðju eða leiðbeiningar sem eru á undan skjalupplýsingunum. Ef fyrirtækið hefur margar uppsetningar er hægt að velja **Velja úr fullum lista** til að fá aðgang að öllum tiltækum skýrslusetningum.
6. Til að skoða eða breyta útlitinu sem texti tölvupósts byggist á, veldu útlit á síðunni **Sérsniðið skýrsluútlit** og veldu síðan **Uppfæra útlit** aðgerðina.
7. Ef þú vilt láta viðskiptavini nota greiðsluþjónustu, eins og PayPal, þá þarftu að setja upp þjónustuna. Eftir sem áður er búið að setja inn PayPal upplýsingar og tengil inn í email textann. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns gegnum PayPal](sales-how-enable-payment-service-extensions.md).
8. Velja hnappinn **Í lagi**.

Nú þegar t.d. er valið aðgerðin **Senda** á síðunni **Bókaður sölureikningur** munu meginmálslínur tölvupósts innihalda upplýsingar fylgiskjals skýrslu 1306 og á eftir fylgir sérsniðinn staðlaður texti í samræmi við skýrsluútlitið sem valið var í 5. þrepi.

## <a name="use-a-substitute-sender-address-on-outbound-email-messages"></a>Nota vistfang staðgengils sendanda á útleið í tölvupósti
Ef nota á SMTP Connector Extension er hægt að nota þá **möguleika að senda sem** eða **senda á fyrir hönd** frá Microsoft Exchange til að breyta heimilisfangi sendanda á skilaboðum á útleið. [!INCLUDE[prod_short](includes/prod_short.md)] mun nota SMTP-lykil til að staðfesta skipti, en mun annaðhvort skipta um heimilisfang sendanda með því sem tilgreint er, eða breyta honum með "fyrir hönd."

Þegar reikningur er settur upp og ætlunin er að nota aðgerðina Senda sem eða senda á fyrir hönd úr húsum í **reitnum Tegund** sendanda skal velja **tiltekinn notanda**.

Einnig er hægt að velja **gildandi notanda** til að leyfa fólki að senda skilaboð í gegnum SMTP-tengið. Skilaboðin birtast frá tölvupóstreikningnum sem tilgreindur er í reitnum Netfang tengiliðar á Notendakorts notandans sem þeir eru skráðir inn á. Hins vegar mun hún virka svipað og senda sem aðgerð og verður send úr reikningnum sem er tilgreindur í uppsetningu SMTP-Tengitengis.

Eftirfarandi eru dæmi um hvernig Senda sem og Senda fyrir hönd eru notuð í [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Hægt er að kaupa eða sölupantana sem sendar eru lánardrottnum og viðskiptamönnum til að koma í stað gamans _noreply@yourcompanyname.com_ aðsetri.
 * Þegar verkflæðið þitt sendir samþykktarbeiðni í tölvupósti með netfangi beiðanda.

> [!Note]
> Aðeins er hægt að nota einn reikning sem staðgengil fyrir netföng sendanda. Þú getur sem sagt ekki haft eitt staðgengilsnetfang fyrir innkaupferli og annað fyrir söluferli.

<!--
### To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## <a name="set-up-document-sending-profiles"></a>Setja upp sendisnið skjala
Hægt er að spara tíma með því að setja upp æskilega aðferð við að senda söluskjöl fyrir sérhvern viðskiptavin. Þú munt ekki þurfa að velja sendingarvalkost, eins og hvort á að senda skjalið með tölvupósti eða sem rafrænt skjal, í hvert sinn sem skjal er sent. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

## <a name="optional-set-up-email-logging-in-exchange-online"></a>Valfrjálst: setja upp tölvupóstskráningu í Exchange Online
Fáðu meira út úr samskiptum milli sölumanna og þinna sem til eru eða hugsanlegra viðskiptavina. Hægt er að rekja tölvupóstskiptingar og snúa þeim síðan í Gantt tækifæri. Frekari upplýsingar eru í [Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## <a name="setting-up-email-for-business-central-on-premises"></a>Uppsetning tölvupósts fyrir Business Central á staðnum 
[!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er hægt að samþætta við þjónustur sem byggja á Microsoft Azure. Til dæmis er hægt að nota Cortana Intelligence fyrir snjallari sjóðsstreymisspá, Power BI til að sjá fyrir sér reksturinn og Exchange Online til að senda tölvupóst. Samþætting við þessar þjónustur byggist á forritsskráningu í Azure Active Directory. Forritsskráningin býður upp á sannvottun og heimildaþjónusta fyrir samskipti. Til að nota möguleika tölvupóstsins í [!INCLUDE[prod_short](includes/prod_short.md)] þarf að skrá [!INCLUDE[prod_short](includes/prod_short.md)] sem forrit í Azure-gáttinni og síðan tengja [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna. Eftirfarandi hlutar útskýra hvernig.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Búa til App skráning fyrir viðskipti Miðbær í Azure Portal
Skrefunum til að skrá [!INCLUDE[prod_short](includes/prod_short.md)] inn í Azure-gáttina er lýst í [Skrá forrit í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Stillingarnar sem miðast við möguleika tölvupóstsins eru úthlutuðu heimildirnar sem veittar eru forritsskráningunni. Í eftirfarandi töflu er listi yfir lágmarksheimildir.

|Heiti API / heimildar  |Tegund  |Description  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Úthlutað|Skráðu þig inn og lestu prófíl notanda.         |
|Microsoft Graph / Mail.ReadWrite |Úthlutað|Skrifa tölvupóstskeyti.         |
|Microsoft Graph / Mail.Send|Úthlutað|Senda tölvupóst.         |
|Microsoft Graph / offline_access|Úthlutað|Vinna með samþykki gagnaaðgangs.|

Ef þú ert að nota SMTP tengi og vilt nota OAuth 2,0 til sannprófunar eru heimildirnar aðeins frábrugðnar. Eftirfarandi tafla sýnir heimildirnar.

|Heiti API / heimildar  |Tegund  |Description  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Úthlutað|Vinna með samþykki gagnaaðgangs.|
|Microsoft Graph / openid|Úthlutað|Skrá notendur inn.|
|Microsoft Graph / User.Read |Úthlutað|Skráðu þig inn og lestu prófíl notanda.         |
|Microsoft Graph / SMTP.Send|Úthlutað|Senda tölvupóst úr pósthólfum með SMTP AUTH.         |
|Office 365 Exchange Online / User.Read |Úthlutað|Skráðu þig inn og lestu prófíl notanda.         |

Þegar skráning forritsins er búin til skal hafa eftirfarandi upplýsingar í huga. Þú þarft því að tengjast [!INCLUDE[prod_short](includes/prod_short.md)] við App skráningu þína.
 
* Kenni forrits (biðlari) 
* Framsenda URI (valfrjálst)
* Leyniorð biðlara

Almennar leiðbeiningar um skráningu forrits má finna í [Stuttar leiðbeiningar: Skráið forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app). 

> [!NOTE]
Ef þú átt í vandræðum með að nota SMTP-samskiptareglurnar til að senda tölvupóst eftir að þú tengist [!INCLUDE[prod_short](includes/prod_short.md)] App-skráningunni þinni gæti verið að SMTP AUTH sé ekki virkt fyrir leigjanda þinn. Mælt er með því að nota Microsoft 365 og gildandi tölvupóstsamtengingarforrit notanda í staðinn, þar sem þau nota Microsoft graph-API. Ef hins vegar þarf að nota SMTP-samskiptareglur er hægt að virkja SMTP AUTH. Frekari upplýsingar er að finna í [Kveikja eða slökkva á SMTP-innsendingu (SMTP AUTH) sannvottaðs biðlara í Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect-prod_short-to-your-app-registration"></a>Tengja [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna
Þegar forritið hefur verið skráð í Azure-gáttina, í [!INCLUDE[prod_short](includes/prod_short.md)], skal nota uppsetningarleiðbeininguna **AAD-skráning tölvupóstforrits** með hjálp til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við það.

1. [!INCLUDE[prod_short](includes/prod_short.md)] Veljið þá ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn **AAD-skráning póstforrits** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Annars, ef verið er að tengjast í fyrsta skipti, er hægt að keyra uppsetningarleiðbeininguna **Setja upp tölvupóst** með hjálp. Leiðarvísirinn þarf upplýsingarnar til að tengjast við forritsskráninguna. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/set-up-email/)

## <a name="see-also"></a>Sjá einnig

[Samnýtt pósthólf í Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Viðskiptainnhólf í Outlook](admin-outlook.md)  
[Sækja [!INCLUDE[prod_short](includes/prod_short.md)] í fartækinu mínu](install-mobile-app.md)
[Sækja [!INCLUDE[prod_short](includes/prod_short.md)] í fartækinu mínu](install-mobile-app.md)
[Greina fjarmælingu tölvupósts (efni stjórnanda)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
