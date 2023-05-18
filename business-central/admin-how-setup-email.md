---
title: Setja upp tölvupóst í Business Central (inniheldur myndskeið)
description: Lýsir því hvernig á að tengja tölvupóstsreikninga við Business Central til að hægt sé að senda skilaboð á útleið án þess að opna annað forrit.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 11/22/2022
ms.author: bholtorf
---

# Setja upp tölvupóst

Fólk í viðskiptum sendir upplýsingar og skjöl á borð við sölu- og innkaupapantanir og reikninga með tölvupósti á hverjum degi. Stjórnendur geta tengt einn eða fleiri tölvupóstsreikninga við [!INCLUDE[prod_short](includes/prod_short.md)] þannig að hægt sé að senda skjöl án þess að þurfa að opna annað tölvupóstforrit. Hægt er að semja hver skilaboð fyrir sig með einföldum sniðsverkfærum eins og leturgerð, útliti, litum og svo framvegis og bæta við viðhengjum allt að 100 MB að stærð. Auk þess gerir skýrsluútlit stjórnendum kleift að taka aðeins með lykilupplýsingar úr skjölunum. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Möguleikar tölvupósts í [!INCLUDE[prod_short](includes/prod_short.md)] eru aðeins fyrir skeyti á útleið. Ekki er hægt að fá svör, þ.e. þar er engin "fésbókarsíðu".

> [!NOTE]
> Aðeins er hægt að nota möguleika tölvupósts fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu með Exchange Online. Við styðjum ekki blandaðar aðstæður, eins og að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á netinu við innanhússútgáfu af Exchange.
>
> Ef notað er [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss þarf fyrst að stofna forritsskráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Azure-gáttinni áður en tölvupóstur er settur upp. Forritsskráningin gerir [!INCLUDE[prod_short](includes/prod_short.md)] kleift að heimila og sannvotta hjá tölvupóstþjónustu þinni. Frekari upplýsingar eru í [Uppsetning tölvupósts fyrir Business Central á staðnum](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). Á [!INCLUDE[prod_short](includes/prod_short.md)] netinu sjáum við um þetta fyrir þig.

## Kröfur

Gerðar eru tvær kröfur um uppsetningu og notkun á tölvupóstaðgerðum.

* Til að setja upp tölvupóst þarf að hafa heimildasamstæðuna **UPPSETNING TÖLVUPÓSTS**. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).
* Allir sem vilja nota tölvupóstaðgerðirnar verða að vera með fullgild leyfi [!INCLUDE [prod_short](includes/prod_short.md)]. Til dæmis geta úthlutuðum viðurkenningar-og gestanotendur ekki notað tölvupóstreikning leigjanda.

## Bæta við tölvupóstreikningum

Tölvupóstsreikningum er bætt við í gegnum viðbætur sem gera reikningum frá mismunandi þjónustuaðilum kleift að tengjast við [!INCLUDE[prod_short](includes/prod_short.md)]. Stöðluðu viðbæturnar gera kleift að nota reikninga frá Microsoft Exchange Online. Aðrar viðbætur sem gera kleift að tengja reikninga frá öðrum þjónustuaðilum á borð við Gmail kunna hins vegar að vera aðgengilegar.

Hægt er að tilgreina fyrirframskilgreindar viðskiptaaðstæður þar sem notaður er tölvupóstsreikningur til að senda tölvupósta. Til dæmis er hægt að tilgreina að allir notendur sendi söluskjöl frá einum reikningi og innkaupaskjöl frá öðrum. Lærðu meira á  [að tengja Tölvupóstaðstæður við tölvupóstreikninga](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Eftirfarandi tafla lýsir þeim tölvupóstsviðbótum sem eru sjálfgefið í boði.

|Viðbót  |Lýsing  |Dæmi um notkun  |
|---------|---------|---------|
|**Microsoft 365 Tengill**|Allir senda tölvupóst úr samnýttu pósthólfi í Exchange Online.|Þegar öll skilaboð koma frá sömu deild, t.d. að sölufyrirtækið þitt sendir boð úr  sales@cronus.com  lykli. Þetta valkostur krefst þess að sett verði upp samnýtt pósthólf í Microsoft 365 stjórnendamiðstöðinni. Frekari upplýsingar eru í [Samnýtt pósthólf](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Tengill núverandi notanda**|Allir senda tölvupóst frá reikningnum sem var notaður til að skrá sig inn á [!INCLUDE[prod_short](includes/prod_short.md)].|Leyfa samskipti frá reikningum einstaklinga.|
|**SMTP-tengill**|Nota skal SMTP-samskiptareglu til að senda tölvupósta.|Leyfa skal samskipti í gegnum SMTP-póstþjóninn. |

> [!NOTE]
> Viðbætur **Microsoft 365 Tengils** og **Tengils núverandi notanda** nota reikningana til að setja upp fyrir notendur í Microsoft 365 stjórnendamiðstöðinni fyrir Microsoft 365-áskriftina. Til að senda tölvupóst með viðbótunum verða notendur að vera með gilt leyfi fyrir Exchange Online. Í sandkassaumhverfum þurfa þessar viðbætur líka að stillingin **Leyfa HttpClient-beiðnir** sé virk. Til að athuga hvort hún sé virk fyrir þessar viðbætur skal fara á síðuna **Viðbótastjórnun**, velja viðbótina og síðan velja valkostinn **Grunnstilla**.

> Ytri notendur, svo sem stjórnendur og utanaðkomandi endurskoðendur, geta ekki notað þessar viðbætur til að senda tölvupóstskeyti frá [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## Notkun SMTP

Ef nota á SMTP-samskiptaregluna til að senda tölvupósta úr [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að nota viðbót SMTP-tengils. Þegar settur er upp lykill sem notar SMTP  **er reiturinn Tegund**  sendanda mikilvægur. Ef valinn  **er sérstakur notandi** verður tölvupóstur sendur með nafni og öðrum upplýsingum af reikningnum sem verið er að setja upp. Ef valið  **er notandi** verður tölvupóstur hins vegar sendur úr tölvupóstreikningnum sem tilgreindur er fyrir reikning hvers notanda. „Núverandi notandi“ svipar til eiginleikans „Senda sem“. Frekari upplýsingar er að finna í [Nota staðgengilsnetfang sendanda fyrir tölvupóstskeyti á útleið](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Ef þið eruð að nota  [!INCLUDE[prod_short](includes/prod_short.md)]  innanhúss er hægt að nota OAuth 2,0 samskiptareglur til auðkenningar. Búa þarf til forritsskráningu í Azure-gáttinni og síðan keyra uppsetningarleiðbeininguna **Setja upp Azure Active Directory** í [!INCLUDE[prod_short](includes/prod_short.md)] til að tengjast við Azure AD. Frekari upplýsingar er að finna í [Búa til forritsskráningu fyrir Business Central í Azure-gátt](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online er sviptingu nota grunnsannvottun fyrir SMPT. Leigjendur sem eru nú með SMTP AUTH munu ekki hafa áhrif á þessa breytingu. Hins vegar mælum við eindregið með nýjustu útgáfunni af og Uppsetning á  [!INCLUDE [prod_short](includes/prod_short.md)]  OAuth 2,0 sannvottun fyrir SMTP. Við bætum vottunargrundvelli ekki við eldri útgáfur  [!INCLUDE [prod_short](includes/prod_short.md)], t.d. útgáfu 14. Ef þú getur ekki sett upp OAuth 2,0 auðkenningu, hvetjum við þig til að kanna val þriðja aðila ef þú vilt nota SMTP email í eldri útgáfum.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## Bæta tölvupóstreikningum við

Uppsetningarleiðbeiningarnar **Setja upp tölvupóst** með hjálp geta komið þér af stað með tölvupósta.

> [!NOTE]
> Þú verður að vera með sjálfgefinn tölvupóstsreikning, jafnvel þó svo þú notir aðeins einn reikning. Sjálfgefinn reikningur verður notaður fyrir allar aðstæður tölvupóstsins sem ekki er úthlutað á reikning. Lærðu meira á  [að tengja Tölvupóstaðstæður við tölvupóstreikninga](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Setja upp tölvupóstreikninga** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## Tengja tölvupóstaðstæður við tölvupóstreikninga

Aðstæður tölvupósts eru ferli sem fela í sér að senda skjal. Til dæmis sölu- eða innkaupapöntun eða tilkynning, t.d. boð til ytri endurskoðanda. Hægt er að nota tiltekna tölvupóstsreikninga fyrir tilteknar aðstæður. Til dæmis er hægt að tilgreina að allir notendur sendi alltaf söluskjöl frá einum reikningi, innkaupaskjöl frá öðrum og vöruhúsa- eða framleiðsluskjöl frá þriðja reikningi. Hægt er að úthluta, endurúthluta og fjarlægja aðstæður hvenær sem er. Aðeins er hægt að úthluta aðstæðum á einn tölvupóstsreikning í einu. Sjálfgefinn tölvupóstsreikningur verður notaður fyrir allar aðstæður sem ekki eru úthlutaðar á reikning.

 **Á úthlutunarsíðu aðstæðarsúthlutun**  er hægt að velja  **stilla sjálfgefna viðhengja**  aðgerð til að bæta viðhengjum við tölvupóstaðstæður. Viðhengi verða alltaf tiltæk þegar tölvupóstur er útbúinn fyrir skjal sem tengist aðstæðunum. Hver tölvupóstur getur haft eitt eða fleiri sjálfgefin viðhengi. Sjálfgefnum viðhengjum er sjálfkrafa bætt við tölvupósta fyrir aðstæður tölvupóstsins. Til dæmis þegar sölupöntun er send með tölvupósti verður sjálfgefnu viðhengi fyrir aðstæður sölupöntunarinnar bætt við. Sjálfgefin viðhengi birtast í hlutanum **Viðhengi** neðst á síðunni **Semja tölvupóst**. Þú getur bætt við viðhengjum sem eru ekki sjálfgefin við tölvupóstinn.

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

## Setja upp skoðunarreglur

Hægt er að stýra þeim tölvupósti sem notandi getur nálgast í Bréfapóstum og sent tölvupósta síður.

Í **Skoðunarreglur fyrir tölvupóst notanda** skal velja notanda og síðan velja einn af eftirfarandi valkostum í reitnum **Skoðunarregla tölvupósts**:

* **Skoða eigin tölvupóst** - Notandinn getur aðeins skoðað eigin tölvupóstskeyti.
* **Skoða alla tölvupósta** - Notandinn getur skoðað alla tölvupósta, þar á meðal tölvupósta sem aðrir notendur sendu.
* **Skoða ef aðgangur að öllum tengdum færslum** - Þessi skoðunarregla er notuð ef engin önnur regla er tilgreind. Notandi getur skoðað tölvupóstskeyti sem aðrir notendur hafa sent ef notandi hefur aðgang að færslunni sem var send og öllum tengdum færslum. Dæmi: Notandi A sendi bókaðan sölureikning á viðskiptamann. Notandi B getur séð tölvupóstskeytið ef hann hefur aðgang að bæði reikningnum og viðskiptamanninum.
* **Skoða ef aðgangur að einhverjum tengdum færslum** - Notandinn getur skoðað tölvupóstskeyti sem aðrir sendu ef notandinn hefur aðgang að a.m.k. einni færslu sem tengist færslunni sem var send. Dæmi: Notandi A sendi bókaðan sölureikning á viðskiptamann. Notandi B getur séð tölvupóstskeytið ef hann hefur aðgang að annaðhvort reikningnum eða viðskiptamanninum.

> [!NOTE]
>  **Ef reiturinn NOTANDAKENNI**  er auður og síðan er  **valið stefnuaðgerð**  tölvupóstsins, gildir regla um Sýn á alla notendur.

## Tilgreina hversu mörg boð geta sent reikning á mínútu

Sumar email veitur (ISP) takmarka fjölda netskeyta tölvupóstslykill getur sent í einni ferð, eða innan ákveðins tíma, eða hvort tveggja. Þekktur sem  *email eldvirkni*, starf hjálpa ISPs stjórn umferð á netþjónum sínum og hindra spam. Ef Tölvupóstreikningur er yfir mörkum gæti ÞJÓNUSTUVEITAN lokað fyrir skeytin. Til að tryggja að fjöldi skeyta sem þú sendir frá  [!INCLUDE [prod_short](includes/prod_short.md)]  sér samræmist hámarki Internetþjónustunnar skaltu tilgreina mörkin fyrir hvern tölvupóstreikninga þinna.

Sjálfgefin mörk fyrir  Microsoft 365  gerðir og gildandi notandareikninga eru 30 sem samsvara takmörunum sem eru sett af Exchange Online.

Tvær leiðir eru til að tilgreina mörkin:

* Þegar notuð er leiðarvísir um uppsetningu Tölvupóstaðstoðar til að stofna nýjan lykil þarf að tilgreina mörkin í  **reitnum gengismörk á hverri mínútu** .
* Fyrir fyrirliggjandi tölvupóstslykla eru mörkin í reitnum tölvupóstshlutfall takmörk  **tilgreind í**  reikningnum.

## Setja upp endurnýtanlegan senditexta og skipulag

Hægt er að nota skýrslur til að taka með helstu upplýsingar úr sölu-, innkaupa- og þjónustuskjölum í texta fyrir tölvupóst. Skýrsluútlit skilgreinir stíl og efni textans í tölvupóstinum. Til dæmis gætu efnið innihaldið texta á borð við kveðju eða leiðbeiningar sem koma á undan upplýsingum um skjalið. Þetta ferli lýsir því hvernig á að setja upp skýrsluna **Sala - Reikningur** fyrir bókaða sölureikninga, en ferlið er svipað fyrir aðrar skýrslur.

> [!NOTE]
> Til að nota útlitið til að búa til efni fyrir tölvupóstskeyti verður að nota Word-skráargerðina fyrir útlitið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skýrsluval - Sala** og velja síðan viðkomandi tengil.
2. Á síðunni **Skýrsluval - Sala** í reitnum **Notkun** skal velja **Reikningur**.
3. Í nýrri línu í reitnum **Skýrslukenni** skal velja t.d. staðlaða skýrslu 1306.
4.  **Veljið nota fyrir meginmál**  tölvupósts.
5. Veljið reitinn **Lýsing á útliti meginmáls tölvupósts** og veljið síðan útlit í listanum.
6. Til að skoða eða breyta útlitinu sem texti textans er byggður á, veljið útlitið á  **sérsniðnu útliti skýrslugerðar skýrslunnar**  og veljið  **síðan aðgerðina Flytja út** . Ef útlitið er sérsniðið er aðgerðin innflutningsútlit  **notuð**  til að hlaða upp nýju útlitinu.
    > [!NOTE]
    > Til að sérsníða staðlað skýrsluútlit, t.d. 1306, verður að gera afrit af skýrslunni. [!INCLUDE [prod_short](includes/prod_short.md)] mun hjálpa til við að búa til afrit þegar sérsniðið útlit er flutt inn fyrir staðlaða skýrslu. Heiti nýrrar sérsniðinnar skýrsluuppsetningar verður forlagfært með "Copy of."
7. Ef leyfa á viðskiptamanninum að nota greiðsluþjónustu á borð við PayPal þarf að setja upp þjónustuna. Eftir það eru PayPal upplýsingarnar og tengillinn sett inn í texta póstsins. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns gegnum PayPal](sales-how-enable-payment-service-extensions.md).
8. Velja hnappinn **Í lagi**.

Nú þegar t.d. er valið aðgerðin **Senda** á síðunni **Bókaður sölureikningur** munu meginmálslínur tölvupósts innihalda upplýsingar fylgiskjals skýrslu 1306 og á eftir fylgir sérsniðinn staðlaður texti í samræmi við skýrsluútlitið sem valið var í 5. þrepi.

## Nota vistfang staðgengils sendanda á útleið í tölvupósti

Ef notuð er viðbót SMTP-tengils er hægt að nota möguleikana **Senda sem** eða **Senda fyrir hönd** frá Microsoft Exchange til að breyta netfangi sendanda fyrir skeyti á útleið. [!INCLUDE[prod_short](includes/prod_short.md)] notar SMTP-reikning til að sannvotta fyrir Exchange, en mun annaðhvort skipta út netfangi sendanda fyrir það sem þú tilgreinir eða breytir því með „fyrir hönd.“

Þegar reikningur er settur upp og nota á möguleikann „Senda sem“ eða „Senda fyrir hönd“ úr Exchange, í reitnum **Gerð sendanda**, skal velja **Tiltekinn notandi**.

Einnig er hægt að velja **Núverandi notanda** til að leyfa fólki að senda skeyti í gegnum SMTP-tengilinn. Skeytið lítur út fyrir að hafa verið sent frá tölvupóstsreikningnum sem tilgreindur er í reitnum „Netfang tengiliðar“ á notandaspjaldinu fyrir notandann sem er innskráður. Hins vegar mun skeytið virka á svipaðan hátt og eiginleikinn „Senda sem“ og verður sent frá reikningnum sem tilgreindur er í uppsetningu SMTP-tengilsins.

Eftirfarandi eru dæmi um hvernig Senda sem og Senda fyrir hönd eru notuð í [!INCLUDE[prod_short](includes/prod_short.md)]:

* Innkaupa-eða sölupantanir sem sendar eru lánardrottnum og viðskiptamönnum virðast koma frá  _noreply@yourcompanyname.com_  aðsetri.
* Þegar verkflæðið þitt sendir samþykktarbeiðni með tölvupósti með tölvupósti á netfang umsækjanda.

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

## Setja upp forstillingar fyrir sendingu skjals

Hægt er að spara tíma með því að setja upp æskilega aðferð við að senda söluskjöl fyrir hvern viðskiptamann þinn. Ekki þarf að velja sendingarmöguleika, t.d. hvort senda skuli skjalið með tölvupósti eða sem rafrænt skjal, í hvert sinn sem skjal er sent. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

## Valfrjálst: setja upp tölvupóstskráningu í Exchange Online

Fáðu meira út úr samskiptum sölumanna við núverandi eða mögulega viðskiptamenn þína. Hægt er að rekja tölvupóstsamskipti og síðan breyta þeim í tækifæri sem hægt er að vinna með. Frekari upplýsingar í  [track tölvupóstskilaboð skipta á milli sölumanna og tengiliða](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## Uppsetning tölvupósts fyrir fyrirtæki Aðalskipulagstillagan innanhúss

[!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er hægt að samþætta við þjónustur sem byggja á Microsoft Azure. Til dæmis er hægt að nota Cortana Intelligence fyrir snjallari sjóðsstreymisspá, Power BI til að sjá fyrir sér reksturinn og Exchange Online til að senda tölvupóst. Samþætting við þessar þjónustur byggist á forritsskráningu í Azure Active Directory. Forritsskráningin býður upp á sannvottun og heimildaþjónusta fyrir samskipti. Til að nota möguleika tölvupóstsins í [!INCLUDE[prod_short](includes/prod_short.md)] þarf að skrá [!INCLUDE[prod_short](includes/prod_short.md)] sem forrit í Azure-gáttinni og síðan tengja [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna. Eftirfarandi hlutar útskýra hvernig.

### Búa til App skráning fyrir viðskipti Miðbær í Azure Portal

Skrefunum til að skrá [!INCLUDE[prod_short](includes/prod_short.md)] inn í Azure-gáttina er lýst í [Skrá forrit í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> Til að geta notað tölvupóstaðgerðirnar þarf App skráningunni að nota í samskipun margra leigjenda.

Stillingarnar sem miðast við möguleika tölvupóstsins eru úthlutuðu heimildirnar sem veittar eru forritsskráningunni. Í eftirfarandi töflu er listi yfir lágmarksheimildir.

|Heiti API / heimildar  |Tegund  |Description  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Úthlutað|Skráðu þig inn og lestu prófíl notanda.         |
|Microsoft Graph / Mail.ReadWrite |Úthlutað|Skrifa tölvupóstskeyti.         |
|Microsoft Graph / Mail.Send|Úthlutað|Senda tölvupóst.         |
|Microsoft Graph / offline_access|Úthlutað|Vinna með samþykki gagnaaðgangs.|

Heimildirnar eru örlítið frábrugðnar ef þú ert að nota eldri SMTP-tengil og vilt nota OAuth 2.0 fyrir auðkenningu. Eftirfarandi tafla sýnir heimildirnar.

|Heiti API / heimildar  |Tegund  |Description  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Úthlutað|Vinna með samþykki gagnaaðgangs.|
|Microsoft Graph / openid|Úthlutað|Skrá notendur inn.|
|Microsoft Graph / User.Read |Úthlutað|Skráðu þig inn og lestu prófíl notanda.         |
|Microsoft Graph / SMTP.Send|Úthlutað|Senda tölvupóst úr pósthólfum með SMTP AUTH.         |
|Office 365 Exchange Online / User.Read |Úthlutað|Skráðu þig inn og lestu prófíl notanda.         |

Þegar skráning forritsins er búin til skal hafa eftirfarandi upplýsingar í huga. Þær eru nauðsynlegar til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna.
 
* Kenni forrits (biðlari)
* Framsenda URI (valfrjálst)
* Leyniorð biðlara

Frekari upplýsingar um almennar leiðbeiningar fyrir skráningu í App hjá  [Quickstart: Skráðu þig inn umsókn með Platform](/azure/active-directory/develop/quickstart-register-app) Microsoft auðkenni.

> [!NOTE]
Ef þú átt í vandræðum með að nota SMTP-samskiptareglu til að senda tölvupóst eftir að þú tengir [!INCLUDE[prod_short](includes/prod_short.md)] við forritsskráninguna, gæti það verið vegna þess að SMTP AUTH er ekki virkt fyrir leigjanda þinn. Mælt er með því að Microsoft 365 og tölvupóststengla núverandi notanda í staðinn vegna þess að hann notar Microsoft Graph Mail API. Ef þú þarft hins vegar að nota SMTP-samskiptareglu er hægt að virkja SMTP AUTH. Frekari upplýsingar er að finna í [Kveikja eða slökkva á SMTP-innsendingu (SMTP AUTH) sannvottaðs biðlara í Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### Tengjast  [!INCLUDE[prod_short](includes/prod_short.md)]  við App skráningu þína

Eftir að þú hefur skráð þína umsókn í Azure Portal, inn  [!INCLUDE[prod_short](includes/prod_short.md)], Notaðu  **þá skráningarsíðu**  tölvupóst umsókn aad til að tengjast  [!INCLUDE[prod_short](includes/prod_short.md)]  henni.

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn **AAD-skráning póstforrits** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Annars, ef verið er að tengjast í fyrsta skipti, er hægt að keyra uppsetningarleiðbeininguna **Setja upp tölvupóst** með hjálp. Í því tilviki skal leiðbeiningastöð heimilanna einnig innihalda skráningarsíðu AAD-forritsins til að bæta við upplýsingunum fyrir tengingu við App-skráninguna. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

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

## Sjá tengda [Microsoft þjálfun](/training/modules/set-up-email/)

## Sjá einnig

[Samnýtt pósthólf í Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem viðskiptainnhólf þitt í Outlook](admin-outlook.md)  
[Sækja [!INCLUDE[prod_short](includes/prod_short.md)] í fartækinu mínu](install-mobile-app.md)
[Sækja [!INCLUDE[prod_short](includes/prod_short.md)] í fartækinu mínu](install-mobile-app.md)
[Greina fjarmælingu tölvupósts (efni stjórnanda)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
