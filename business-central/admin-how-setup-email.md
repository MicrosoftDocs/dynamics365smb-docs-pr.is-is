---
title: Setja upp tölvupóst í Business Central | Microsoft Docs
description: Lýsir því hvernig á að tengja tölvupóstsreikninga við Business Central til að hægt sé að senda skilaboð á útleið án þess að opna annað forrit.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 06/15/2020
ms.author: bholtorf
ms.openlocfilehash: 44fb1f467b0b44c41456a64c8de3f5ae9dc85786
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752751"
---
# <a name="set-up-email"></a>Setja upp tölvupóst
Fólk í viðskiptum sendir upplýsingar og skjöl á borð við sölu- og innkaupapantanir og reikninga með tölvupósti á hverjum degi. Stjórnendur geta auðveldað verkið með því að tengja einn eða fleiri tölvupóstsreikninga við [!INCLUDE[prod_short](includes/prod_short.md)] þannig að hægt sé að senda skjöl án þess að þurfa að opna annað tölvupóstforrit. Hægt er að semja hver skilaboð fyrir sig með einföldum sniðsverkfærum eins og leturgerð, útliti, litum og svo framvegis og bæta við viðhengjum allt að 100 MB að stærð. Stjórnendur geta einnig sett upp skýrsluútlit sem inniheldur aðeins helstu upplýsingar úr fylgiskjölum. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Möguleikar tölvupóstsins í [!INCLUDE[prod_short](includes/prod_short.md)] eru aðeins fyrir skilaboð á útleið. Ekki er hægt að fá nein skilaboð til baka, þ.e. ekkert innhólf er í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Ef notað er [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss þarf fyrst að stofna forritsskráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Azure-gáttinni áður en tölvupóstur er settur upp. Forritsskráningin gerir [!INCLUDE[prod_short](includes/prod_short.md)] kleift að heimila og sannvotta hjá tölvupóstþjónustu þinni. Frekari upplýsingar eru í [Uppsetning tölvupósts fyrir Business Central á staðnum](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). Á [!INCLUDE[prod_short](includes/prod_short.md)] netinu sjáum við um þetta fyrir þig.

## <a name="required-permissions"></a>Nauðsynlegar heimildir
Til að setja upp tölvupóst þarf að hafa heimildasamstæðuna **UPPSETNING TÖLVUPÓSTS**. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Bæta við tölvupóstreikningum
Tölvupóstsreikningum er bætt við í gegnum viðbætur sem gera reikningum frá mismunandi þjónustuaðilum kleift að tengjast við [!INCLUDE[prod_short](includes/prod_short.md)]. Stöðluðu viðbæturnar gera kleift að nota reikninga frá Microsoft Exchange Online, en aðrar viðbætur kunna að vera aðgengilegar sem gera kleift að tengja reikninga frá öðrum þjónustuaðilum á borð við Gmail.

Þegar búið er að bæta við tölvupóstsreikningi er hægt að tilgreina fyrirframskilgreindar viðskiptaaðstæður þar sem á að nota reikninginn til að senda tölvupóst. Til dæmis er hægt að tilgreina að allir notendur sendi söluskjöl frá einum reikningi og innkaupaskjöl frá öðrum. Frekari upplýsingar er að finna í [Úthluta aðstæðum tölvupósts á tölvupóstsreikninga](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Eftirfarandi tafla lýsir þeim tölvupóstsviðbótum sem eru sjálfgefið í boði.

|Innanhússsími  |Description  |Dæmi um notkun  |
|---------|---------|---------|
|**Microsoft 365**|Allir senda tölvupóst úr samnýttu pósthólfi í Exchange Online.|Þegar öll skilaboð koma frá sömu deildinni sem dæmi, þá sendir sölufyrirtækið skilaboð frá reikningnum sales@cronus.com. Þetta krefst þess að sett verði upp samnýtt pósthólf í Office 365 stjórnendamiðstöðinni. Frekari upplýsingar eru í [Samnýtt pósthólf](/Exchange/collaboration/shared-mailboxes/shared-mailboxes.md).|
|**Núverandi notandi**|Allir senda tölvupóst frá reikningnum sem var notaður til að skrá sig inn á [!INCLUDE[prod_short](includes/prod_short.md)].|Leyfa samskipti frá reikningum einstaklinga.|
|**Annað (SMTP)**|Nota skal SMTP-samskiptareglu til að senda tölvupósta.|Leyfa skal samskipti í gegnum SMTP-póstþjóninn. |

> [!NOTE]
> Viðbætur **Microsoft 365** og **Núverandi notanda** nota reikningana til að setja upp fyrir notendur í stjórnendamiðstöð Microsoft 365 fyrir Office 365-áskriftina þína. Til að senda tölvupóst með viðbótunum verða notendur að vera með gilt leyfi fyrir Exchange Online. 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Eldri SMTP-stillingar og tölvupóstur - Viðbót SMTP-tengils
Ef verið er að nota [!INCLUDE[prod_short](includes/prod_short.md)] og búið er að grunnstilla tölvupóst í gegnum eldri uppsetningu SMTP, er hægt að halda áfram að nota uppsetninguna samhliða tölvupóstinum - viðbót SMTP-tengils. Þegar við uppfærum [!INCLUDE[prod_short](includes/prod_short.md)] í næstu útgáfu munum við afrita eldri SMTP-stillingar í tölvupóstinn - viðbót SMTP-tengils. Við tækifæri getur stjórnandinn kveikt á viðbótareiginleika tölvupóstsins og hægt verður að nota tölvupóstinn - viðbót SMTP-tengils. Frekari upplýsingar eru í [Um eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management.md#about-feature-management). Hinsvegar er engin samstilling milli viðbótar SMTP-tengils og eldri stillinga. Ef SMTP-stillingum er breytt í viðbótinni ætti að gera sömu breytingar á eldri SMTP-uppsetningu eða öfugt.

> [!NOTE]
> Ef til staðar eru sérstillingar sem tengjast eldri uppsetningu SMTP-tölvupósts, eru líkur á að eitthvað fari úrskeiðis í sérstillingunum ef viðbætur tölvupóstsins eru notaðar. Mælt er með því að setja upp og prófa viðbæturnar áður en kveikt er á eiginleikanum fyrir viðbótareiginleika tölvupósts.

## <a name="add-email-accounts"></a>Bæta tölvupóstreikningum við
Uppsetningarleiðbeiningarnar **Setja upp tölvupóst** með hjálp geta komið þér af stað með tölvupósta.

> [!NOTE]
> Þú verður að vera með sjálfgefinn tölvupóstsreikning, jafnvel þó svo þú notir aðeins einn reikning. Sjálfgefinn reikningur verður notaður fyrir allar aðstæður tölvupóstsins sem ekki er úthlutað á reikning. Frekari upplýsingar er að finna í [Úthluta aðstæðum tölvupósts á tölvupóstsreikninga](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Setja upp tölvupóstreikninga** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Office 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Úthluta aðstæðum tölvupósts á tölvupóstsreikninga
Aðstæður tölvupósts eru ferlar sem fela í sér að senda skjal, t.d. sölu- eða innkaupapöntun eða tilkynningu, t.d. boð til ytri endurskoðanda. Hægt er að nota tiltekna tölvupóstreikninga fyrir tilteknar aðstæður. Til dæmis er hægt að tilgreina að allir notendur sendi alltaf söluskjöl frá einum reikningi, innkaupaskjöl frá öðrum og vöruhúsa- eða framleiðsluskjöl frá þriðja reikningi. Hægt er að úthluta, endurúthluta og fjarlægja aðstæður hvenær sem er, en aðeins er hægt að úthluta aðstæðum á einn tölvupóstsreikning í einu. Sjálfgefinn tölvupóstsreikningur verður notaður fyrir allar aðstæður sem ekki er úthlutað á reikning.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Setja upp endurnýtanlega texta og útlit tölvupósts fyrir sölu- og innkaupaskjöl
Hægt er að nota skýrslur til að taka með helstu upplýsingar úr sölu-og innkaupaskjölum í texta fyrir tölvupóst. Þetta ferli lýsir því hvernig á að setja upp skýrsluna **Sala - Reikningur** fyrir bókaða sölureikninga, en ferlið er svipað fyrir aðrar skýrslur.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skýrsluval - Sala** og veldu síðan tengda tengilinn.
2. Á síðunni **Skýrsluval - Sala** í reitnum **Notkun** skal velja **Reikningur**.
3. Í nýrri línu í reitnum **Skýrslukenni** skal velja t.d. staðlaða skýrslu 1306.
4. Veljið gátreitinn **Nota fyrir meginmál tölvupósts**.
5. Veljið reitinn **Útlitsauðkenni meginmáls tölvupósts** og veljið síðan útlit úr fellilistanum.

    Skýrsluútlit skilgreina bæði útlit og efni textans í tölvupóstinum, þ.m.t. texta á borð við kveðju eða leiðbeiningar sem koma neðst á eftir upplýsingum skjalsins. Þú sérð öll tiltæk skýrsluútlit ef þú velur **Velja af öllum listanum**.
6. Til að skoða eða breyta útlitinu sem texti tölvupósts byggist á, veldu útlit á síðunni **Sérsniðið skýrsluútlit** og veldu síðan **Breyta útliti** aðgerðina.
7. Til að hægt sé að bjóða viðskiptamönnum að greiða rafrænt fyrir sölur er hægt að setja upp tengda rafræna greiðsluþjónustu, til dæmis PayPal, og láta PayPal upplýsingar og tengla í meginmál tölvupóstsins. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns gegnum PayPal](sales-how-enable-payment-service-extensions.md).
8. Velja hnappinn **Í lagi**.

Nú þegar t.d. er valið aðgerðin **Senda** á síðunni **Bókaður sölureikningur** munu meginmálslínur tölvupósts innihalda upplýsingar fylgiskjals skýrslu 1306 og á eftir fylgir sérsniðinn staðlaður texti í samræmi við skýrsluútlitið sem valið var í 5. þrepi.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Notkun staðgengilsnetfang sendanda fyrir send tölvupóstskeyti
Ef notaðar eru eldri SMTP-stillingar er hægt að nota **Senda sem** eða **Senda fyrir hönd** á Microsoft Exchange til að breyta netfangi sendanda fyrir skeyti á útleið. [!INCLUDE[prod_short](includes/prod_short.md)] notar SMTP-reikning til að sannvotta fyrir Exchange, en mun annaðhvort skipta út netfangi sendanda með því sem þú tilgreinir eða breytir því með „fyrir hönd.“

Eftirfarandi eru dæmi um hvernig Senda sem og Senda fyrir hönd eru notuð í [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Þegar þú sendir skjöl eins og innkaupa- eða sölupantanir til lánardrottna og viðskiptamanna viltu mögulega að það líti út fyrir að þeir hafi komið frá netfanginu _noreply@yourcompanyname.com_.
 * Þegar verkflæðið þitt sendir samþykktarbeiðni í tölvupósti með netfangi beiðanda.

> [!Note]
> Aðeins er hægt að nota einn reikning sem staðgengil fyrir netföng sendanda. Þú getur sem sagt ekki haft eitt staðgengilsnetfang fyrir innkaupferli og annað fyrir söluferli.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Til að setja upp staðgengilsnetfang sendanda fyrir öll tölvupóstskeyti á útleið
1. Í **Stjórnandamiðstöð Exchange** fyrir Microsoft 365-reikninginn þinn skaltu finna pósthólfið sem nota á sem staðgengilsnetfang og síðan skaltu afrita eða skrifa hjá þér netfangið. Ef þú þarft nýtt netfang skaltu fara í Stjórnendamiðstöð Microsoft 365 til að búa til nýjan notanda og setja upp pósthólfið hans.
2. Í [!INCLUDE[prod_short](includes/prod_short.md)] veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **SMTP uppsetning tölvupósts**, og veldu síðan tengda tengilinn.
3. Í reitnum **Senda sem** skal færa inn staðgengilsnetfangið.
4. Afritaðu eða skráðu netfangið niður í reitinn **Notandakennið**.
5. Í **Stjórnandamiðstöð Exchange** skaltu finna pósthólfið sem á að nota sem staðgengilsnetfang og færðu síðan inn netfangið úr reitnum **Notandakenni** í reitnum **Senda sem**. Nánari upplýsingar eru í [Nota EAC til að úthluta heimildum til einstakra pósthólfa](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Til að nota staðgengilsnetfangið í samþykktarverkflæðum
1. Í [!INCLUDE[prod_short](includes/prod_short.md)] veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **SMTP uppsetning tölvupósts**, og veldu síðan tengda tengilinn.
2. Afritaðu eða skráðu netfangið niður í reitinn **Notandakennið**.
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning samþykktar** og veldu síðan tengda tengilinn.
4. Í **Stjórnandamiðstöð Exchange** skaltu finna pósthólfin fyrir hvern notanda sem kemur fyrir á síðunni **Notandauppsetning samþykktar** og í reitinn **Senda sem** skal færa inn netfangið úr reitnum **Notandakenni** á síðunni **SMTP uppsetning tölvupósts** í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Stjórna heimildum fyrir viðtakendur](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. Í [!INCLUDE[prod_short](includes/prod_short.md)] veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið **SMTP uppsetning tölvupósts**, og veldu síðan tengda tengilinn.
6. Til að virkja skiptingu skal kveikja á víxlun **Leyfa að skipta um sendanda**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] ákvarðar hvaða netfang eigi að birta í eftirfarandi röð: <br><br> 1. Netfang tilgreint í reitnum **Tölvupóstur** á síðunni **Notandauppsetning samþykktar** fyrir skeyti í verkflæði. <br> 2. Netfang tilgreint í reitnum **Senda sem** á síðunni **SMTP uppsetning tölvupósts**. <br> 3. Netfang tilgreint í reitnum **Notandakenni** á síðunni **SMTP uppsetning tölvupósts**.

## <a name="set-up-document-sending-profiles"></a>Setja upp sendisnið skjala
Hægt er að setja upp æskilega aðferð til að senda söluskjöl fyrir hvern viðskiptamann þannig að ekki þurfi að velja sendingarmöguleika, t.d. hvort senda skuli skjalið með tölvupósti eða sem rafrænt skjal, í hvert sinn sem skjal er sent. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Setja upp almenningsmöppur og reglur fyrir tölvupóstsskráningu á Exchange Online
Fáðu meira út úr samskiptum sölumanna við núverandi eða mögulega viðskiptavini þína með því að rekja tölvupóstsamskipti og breyta þeim síðan í möguleg tækifæri. Frekari upplýsingar eru í [Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Næst tengir þú [!INCLUDE[prod_short](includes/prod_short.md)] við Exchange Online. Frekari upplýsingar eru í [Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Uppsetning tölvupósts fyrir Business Central á staðnum 
[!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er hægt að samþætta við þjónustur sem byggja á Microsoft Azure. Til dæmis er hægt að nota Cortana Intelligence fyrir snjallari sjóðsstreymisspá, Power BI til að sjá fyrir sér reksturinn og Exchange Online til að senda tölvupóst. Samþætting við þessar þjónustur byggist á forritsskráningu í Azure Active Directory. Forritsskráningin býður upp á sannvottun og heimildaþjónusta fyrir samskipti. Til að nota möguleika tölvupóstsins í [!INCLUDE[prod_short](includes/prod_short.md)] þarf að skrá [!INCLUDE[prod_short](includes/prod_short.md)] sem forrit í Azure-gáttinni og síðan tengja [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna. Eftirfarandi hlutar útskýra hvernig.

### <a name="create-an-app-registration-for-prod_short-in-azure-portal"></a>Stofna forritsskráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Azure-gáttinni
Skrefunum til að skrá [!INCLUDE[prod_short](includes/prod_short.md)] inn í Azure-gáttina er lýst í [Skrá forrit í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Stillingarnar sem miðast við möguleika tölvupóstsins eru úthlutuðu heimildirnar sem veittar eru forritsskráningunni. Í eftirfarandi töflu er listi yfir lágmarksheimildir.

|Heiti API / heimildar  |Tegund  |Description  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Úthlutað|Skráðu þig inn og lestu prófíl notanda.         |
|Microsoft Graph / Mail.ReadWrite |Úthlutað|Skrifa tölvupóstskeyti.         |
|Microsoft Graph / Mail.Send|Úthlutað|Senda tölvupóst.         |
|Microsoft Graph / offline_access|Úthlutað|Vinna með samþykki gagnaaðgangs. <!--need to verify this-->|

> [!TIP]
> Þegar skráning forritsins er búin til skal hafa eftirfarandi upplýsingar í huga. Þær eru nauðsynlegar til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna.
> 
> * Kenni forrits (biðlari) 
> * Framsenda URI (valfrjálst)
> * Leyniorð biðlara

Almennar leiðbeiningar um skráningu forrits má finna í [Stuttar leiðbeiningar: Skráið forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app.md). 

### <a name="connect-prod_short-to-your-app-registration"></a>Tengja [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna
Þegar forritið hefur verið skráð í Azure-gáttina, í [!INCLUDE[prod_short](includes/prod_short.md)], skal nota uppsetningarleiðbeininguna **AAD-skráning tölvupóstforrits** með hjálp til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við það.

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn **AAD-skráning póstforrits** og veldu síðan tengda tengilinn.
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

## <a name="see-also"></a>Sjá einnig
[Samnýtt pósthólf í Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem viðskiptainnhólf þitt í Outlook](admin-outlook.md)  
[Fáðu [!INCLUDE[prod_short](includes/prod_short.md)] í fartækið þinn](install-mobile-app.md)
