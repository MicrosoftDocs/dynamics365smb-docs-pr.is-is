---
title: Setja upp tölvupóstsskráningu
description: Kynntu þér hvernig tölvupóstsamskipti milli sölufólks og viðskiptavina geta skapað alvöru sölutækifærum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 03/22/2022
ms.search.form: 1680, 1811, 5076
ms.author: bholtorf
ms.openlocfilehash: fc755362a5b29cca9eb8e8e403374e173cff3630
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516136"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða
Fáðu meira út úr samskipunum milli sölumanna þinna og viðskiptavina með því að kveikja á tölvupóstskiptum í Gantt tækifæri. [!INCLUDE[prod_short](includes/prod_short.md)] getur unnið með Exchange Online til að halda skrá yfir skilaboð á inn- og útleið. Þú getur skoðað og greint innihald skilaboða á síðunni **Samskiptaskráningarfærslur**.

> [!NOTE]
> Í 2022 út bylgjan 1 við höfum straumlínulagað ferla til að setja upp tölvupóstskráningu til að auka sveigjanleika og öryggi. Ef þú ert nýr viðskiptamaður í þeirri útgáfu notar þú nýja reynslu. Ef viðskiptavinur er til staðar, hvort sem nýi reynslan er notuð, veltur á því hvort kerfisstjórinn hefur virkjað **tölvupóstskráninguna með API** -aðgerðum í Microsoft graph í **aðgangsstjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er ný reynsla krefst [!INCLUDE[prod_short](includes/prod_short.md)] þess og Exchange Online eru á sama leigjanda.

## <a name="to-set-up-email-logging"></a>Uppsetning tölvupóstskráningar
Þessar leiðbeiningar eru mismunandi eftir því hvort kerfisstjóri hefur kveikt á **tölvupóstskrá sem notar AÐGERÐINA API** eiginleiki í Microsoft-grafi. Ef ekki er kveikt á eiginleikann, er skrefunum á **flipanum upplifun** fylgt.

## <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience)

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Setja upp almenningsmöppur og reglur fyrir tölvupóstsskráningu á Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Næst tengir þú [!INCLUDE[prod_short](includes/prod_short.md)] við Exchange Online.

## <a name="new-experience"></a>[Ný reynsla](#tab/new-experience)
### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a>Setja upp samnýtta póstkassa og reglur fyrir email Innskráning í Exchange Online

> [!NOTE]
> Þessar leiðbeiningar þurfa aðgang að Exchange Online stjórnanda.

Útbúið samnýtt pósthólf í húsum stjórnsýslumiðstöðvarinnar. Einnig er hægt að nota Exchange Online PowerShell. Frekari upplýsingar er að finna [í búið til samnýtt pósthólf](/microsoft-365/admin/email/create-a-shared-mailbox) eða [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Ef notuð er Exchange Management PowerShell eru breytingarnar aðgengilegar í Exchange admin miðstöðinni eftir seinkun. Seinkunin gæti verið margar klukkustundir.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox"></a>Bæta við notandareikning fyrir meðlimi í samnýttu pósthólfi
Lykillinn sem þú notar við innskráningu í tölvupósti er Exchange Online Reikningur. Tímasetta vinnslan mun nota lykilinn til að tengjast samnýttu pósthólfinu og vinna úr tölvupósti. Þessi reikningur ætti ekki að tengjast tilteknum einstaklingi. Bættu við tölvupóstreikningnum til félaginn fyrir samnýtta pósthólfið. Frekari upplýsingar [fást með því að nota EAC til að breyta samnýttu pósthólfi sendifulltrúa](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails"></a>Leyfa öðrum notendum að sjá skráða tölvupósta
Hægt er að leyfa öðrum notanda að opna tölvupóstskeyti í skiptum sem tengjast samskiptaskráningarfærslu [!INCLUDE[prod_short](includes/prod_short.md)]. Til að gera það skaltu gefa notendunum ``Read`` heimild **í safnmöppunni** í samnýttu pósthólfinu. Nánari upplýsingar má finna [Exchange Online á PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### <a name="create-mail-flow-rules"></a>Stofna póstflæðisreglur
Reglur um póstflæði leita að tilteknum skilyrðum í boðum og grípa til aðgerða á þeim. Stofnið tvær reglur um póstflæði út frá upplýsingunum í eftirfarandi töflu. Frekari upplýsingar er að finna á [Reglum um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Aðgerðum reglu um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Tilgangur  |Name  |Nota þessa reglu ef ...  |Gera eftirfarandi ...  |
|---------|---------|---------|---------|
|Regla fyrir móttekinn tölvupóst     |Skrá tölvupóst sem sendur er til þessa fyrirtækis|Sendandi er staðsettur utan stofnunar og er viðtakandi staðsettur inni í fyrirtækinu|BCC tölvupóstreikningurinn sem er tilgreindur fyrir samnýtta pósthólfið.|
|Regla fyrir sendan tölvupóst     |Skrá tölvupóst sem sendur er frá þessu fyrirtæki|Sendandi er staðsettur inni í fyrirtækinu og er viðtakandi staðsettur utan fyrirtækisins.|BCC tölvupóstreikningurinn sem er tilgreindur fyrir samnýtta pósthólfið.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] vinnur einungis með boð í möppunni innhólf í samnýttu pósthólfinu. Ef regla flytur boð úr innhólfinu í aðra möppu verða þau boð ekki unnin. Auk þess eru skilaboð í möppunni Ruslpóstur einnig hunsuð. 

---

## <a name="setting-up-prod_short-to-log-email-messages"></a>Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)] til að skrá tölvupóstskilaboð
Þessar leiðbeiningar eru þær sömu fyrir bæði núverandi og nýjar upplifanir.

Hafist handa með tölvupóstskráningu í tveimur einföldum skrefum:

1. Tengjast [!INCLUDE[prod_short](includes/prod_short.md)] við Exchange Online áskriftina þína Microsoft 365. Exchange Online sér um tölvupóstskilaboðin þín. Við höfum einfaldað þetta skref með því að bjóða upp á uppsetningarleiðbeiningar. Þú þarft bara að hafa kerfisstjóra-skilríkin fyrir kerfisstjóra lykilinn í Microsoft 365. Til að hefja leiðsögnina skaltu opna síðuna **Uppsetning með hjálp** og velja síðan **Setja upp tölvupóstskráningu**.  

2. Gakktu úr skugga um að netföngin fyrir Sölufólk þitt og tengiliði í [!INCLUDE[prod_short](includes/prod_short.md)] séu gild. Til að gera það fyrir hvern viðskiptavin eða sölumann skal opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** og kíkja í reitinn **Netfang**.

> [!Tip]
> Eftir að þú hefur lokið skrefum leiðsagnarinnar geturðu athugað hvort tengingin hafi borið árangur. Eftir því hvort þú ert að nota núverandi eða ný Útlán skaltu gera eitt af eftirfarandi skrefum: 
>
> * **Núverandi reynsla** : leita að uppsetningu **markaðssetningar, velja** aðgang **, svo** Aðgerðir **og** Staðfesta uppsetningu **á** tölvupóstskráningu.
> * **Ný reynsla** : leita að **skráningu** tölvupósts, velja **Aðgerðir** og velja **síðan Villuleita uppsetningu**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Að skoða tölvupóstsamskipti í samskiptaskránni

[!INCLUDE[prod_short](includes/prod_short.md)] býr til færslu á síðunni **Samskiptaskrá** í hvert skipti sem sölumaður og tengiliður skiptast á tölvupóstskilaboðum. Til að skoða samskiptaskrána skaltu opna spjaldið **Tengiliður** fyrir einstaklinginn og velja síðan **Tengt**, **Ferill** og að lokum velja **Samskiptaskráningarfærslur**. Við getum gert nokkra hluti við hverja færslu í skránni, til dæmis:

- Skoðaðu innihald tölvupóstsins sem var sendur á milli með því að velja **Vinna** og svo **Sýna viðhengi**.
- Snúðu tölvupóstsamskiptum við sölutækifæri. Ef skráning er vænleg er hægt að kveikja á henni í tækifæri og stýra svo framvindu hennar að sölu. Til að kveikja á tölvupóstsamskiptum við tækifæri þarf að velja færsluna, vinna **síðan** og **Stofna tækifæri**. Nánari upplýsingar er að finna í [Umsjón sölutækifæra](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Að tengja útgáfur á staðnum við Microsoft Exchange

Hægt er að tengja [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss við Exchange innanhúss eða Exchange Online fyrir tölvupóstsskráningu. Fyrir báðar útgáfur af Exchange eru stillingar fyrir tenginguna í boði á síðunni **Uppsetning markaðssetningar**. Fyrir Exchange Online er einnig hægt að nota uppsetningarleiðbeiningar með hjálp.

> [!IMPORTANT]
> Nýja reynslan styður ekki tengingu við skipti innanhúss. Ef nota þarf Exchange innanhúss, skal ekki virkja uppfærsluuppfærslu fyrir nýja reynslu.

## <a name="connecting-to-exchange-on-premises"></a>Tenging við húsum innanhúss
## <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience)
Til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss við Exchange innanhúss er hægt á síðunni **Uppsetning markaðssetningar** að nota **Grunnútfærsla** sem **Sannvottunargerð** og síðan slá inn innskráningarupplýsingar fyrir notandareikninginn fyrir Exchange innanhúss. Því næst skal kveikja á **Virkja** til að hefja skráningu á tölvupósti.

## <a name="new-experience"></a>[Ný reynsla](#tab/new-experience)
Nýja reynslan styður ekki tengingar við skipti innanhúss.

---

## <a name="connecting-to-exchange-online"></a>Tengist við Exchange Online
Til að tengjast Exchange Online þarf að skrá umsókn í Azure Active Directory. Gefið umsóknarkenninu, leyniorð lyklageymslu og beina vefslóð sem nota á fyrir skráninguna. Beina veffangið er forstillt og ætti að virka fyrir flestar uppsetningar. Frekari upplýsingar eru í [Til að skrá forrit í Azure AD fyrir tengingu úr Business Central í Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Einnig þarf að nota **OAuth2** sem **Tegund auðkenningar**. Einnig þarf að skrá umsókn í Azure Active Directory. Gefið umsóknarkenninu, leyniorð lyklageymslu og beina vefslóð sem nota á fyrir skráninguna. Framsend vefslóð er fyllt út fyrirfram og ætti að virka fyrir flestar uppsetningar. Frekari upplýsingar eru í Til að skrá forrit í Azure AD fyrir tengingu úr Business Central í Exchange Online.

Nauðsynlegt er að setja upp uppsetninguna til að nota HTTPS. Frekari upplýsingar er að finna í [Skilgreining SSL til að tryggja örugga tengingu vefbiðlara Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Ef þjónn er settur upp til að geta haft aðra heimasíðu er hægt að breyta SLÓÐINNI. Leynilykill biðlara verða vistaður sem dulkóðaður strengur í gagnagrunninum.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Til að skrá forrit í Azure AD fyrir tengingu úr Business Central í Exchange Online
Eftirfarandi skref gera ráð fyrir að nota Azure Active Directory til að stjórna auðkennum og aðgangsheimild. Frekari upplýsingar er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app). 

## <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience) 
Eftirfarandi skref gera ráð fyrir að nota Azure Active Directory til að stjórna auðkennum og aðgangsheimild. Frekari upplýsingar er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app). Ef það er ekki notað Azure Active Directory skaltu sjá [nota aðra auðkenni og Aðgangsstjórnunarþjónustu](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

1. Í Azure-gáttinni, undir **Stjórna**, skal velja **Sannvottun**.
2. Undir **Framsendingarvefslóð** skal bæta við framsendingarvefslóðinni sem mælt er með á síðunni **Uppsetning markaðssetningar** í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef framsendingarslóðin á uppsetningarsíðu markaðssetningar er tóm skal finna ráðlagða framsendingarslóð á síðunni **Uppsetning tölvupóstsskráningar með hjálp**.

    > [!NOTE]
    > Ef framsendingarslóðin er ekki tilgreind er hægt að gera það seinna með því að velja **Bæta við verkvangi** og síðan velja **Vef** til að bæta við vefforritinu og framsendingarvefslóðinni. 

3. Undir **Stjórna** skal velja **Skrá**.
4. Finnið eiginleikann **requiredResourceAccess** í skránni og bætið við eftirfarandi kóða innan hornklofanna ([]) til að bæta við áskildum heimildum. Frekari upplýsingar er að finna í [Skrá forritið](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Velja **Vista**.
6. Undir **Stjórna** skal velja **API-heimildir** og síðan ganga úr skugga um að eftirfarandi heimildir komi fram:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Undir **Stjórna** skal velja **Vottorð og leynilyklar** og síðan stofna nýjan leynilykil fyrir forritið. Þú notar leyndarmálið annað hvort í [!INCLUDE[prod_short](includes/prod_short.md)], í **leynireitnum** í biðlara á **uppsetningarsíðu** markaðssetningar eða geymir hann í öruggri geymslu og útvegar hann í tilviki áskrifanda.
8. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. **Kennigildið (biðlara) ID** er Biðlarakenni forritsins. Færa verður inn biðlarakennið annað hvort á **síðu Markaðsuppsetningarsíðunnar**, í **reitnum Kenni** biðlara, eða geyma það í öruggri geymslu og útvega það í tilvik áskrifanda.
9. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal setja upp tölvupóstsskráningu á síðunni **Uppsetning markaðssetningar** eða nota leiðbeininguna **Uppsetning tölvupóstsskráningar með hjálp** til að fá aðstoð við ferlið.
    * Gefið upp tölvupóstsreikning notandans fyrir hönd þess sem áætlað verk mun tengjast við Exchange Online og vinna úr tölvupósti. Notandinn verður að hafa gilt leyfi fyrir Exchange Online.
    * Gefðu upp vefslóðina fyrir Exchange Online. Algengast er að þessi VEFSLÓÐ sé lénið sem tilgreint var á netfangi notandans.
    * Gefið upp **Slóð biðraðarmöppu** og **Slóð geymslumöppu**.
10. Kveikið á **Virkja** til að hefja skráningu á tölvupósti.
11. Skráðu þig inn með stjórnandareikningnum fyrir Azure Active Directory (þessi reikningur verður að hafa gilt leyfi fyrir Exchange og má vera stjórnandi í Exchange Online þínu). Eftir að þú hefur skráð þig inn þarftu að leyfa skráðri umsókn þinni að skrá þig inn fyrir Exchange Online hönd samtakanna. Veita þarf samþykki til að ljúka uppsetningunni.

   > [!NOTE]
   > Ef ekki er beðið um innskráningu með stjórnandareikningnum er það líklega vegna þess að lokað er fyrir sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr https://login.microsoftonline.com.

## <a name="new-experience"></a>[Ný reynsla](#tab/new-experience)
1. Í Azure-gáttinni, undir **Stjórna**, skal velja **Sannvottun**.
2. **Í beina-veffangi** skal bæta við beina-vefslóð sem er lögð til á **skráningarsíðu** tölvupóstinnar í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef reiturinn áframtenging á póstskrá er auður er fundið leiðbeinandi beinslóð á **uppsetningarsíðu** aðstoðar. Til að opna síðuna, á skráningarsíðu **tölvupóstanna, skal velja** Aðgerðir **og** aðstoða uppsetninguna **.**

    > [!NOTE]
    > Ef framsendingarslóðin er ekki tilgreind er hægt að gera það seinna með því að velja **Bæta við verkvangi** og síðan velja **Vef** til að bæta við vefforritinu og framsendingarvefslóðinni.

3. **Í Umsjón** skal velja **API-heimildir** og velja **Microsoft graph** og velja síðan **úthlutuðum heimildum**.
4. Notaðu leitargluggann til að finna og velja **Mail** og bættu svo við **póstinum. Leskrifa. sameiginleg** heimild. 
5. Undir **Stjórna** skal velja **Vottorð og leynilyklar** og síðan stofna nýjan leynilykil fyrir forritið. Þú notar leyndarmálið annað hvort í **reitnum** leyninúmer **í biðlara í email skráningarsíðunni í.**[!INCLUDE[prod_short](includes/prod_short.md)]
6. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. Þetta er biðlarakenni forritsins. Það verður að rita annað hvort í **REITINN kenni** biðlara á **síðunni skráning** tölvupósts.
7. [!INCLUDE[prod_short](includes/prod_short.md)] Setja upp tölvupóstinnskráningu á **skráningarsíðu** tölvupósts eða nota **leiðbeiningar um uppsetningu** aðstoðar.

### <a name="use-another-identity-and-access-management-service"></a>Nota aðra auðkenni og Aðgangsstjórnunarþjónustu
Ef þú ert ekki að nota Azure Active Directory til að stjórna auðkennum og aðgangsheimild Þarftu aðstoð frá þróunaraðila. Ef þú kýst frekar að geyma forritskennið og leynilykilinn á annarri staðsetningu, geturðu skilið reiti biðlarakennis og leynilykils biðlara eftir auða og skrifað viðbót til að sækja auðkennið og leynilykilinn frá staðsetningunni. Hægt er að gefa upp leynilykilinn við keyrslu með því að gerast áskrifandi að tilvikum OnGetEmailLoggingClientId og OnGetEmailLoggingClientSecret tilvikum í codeunit 1641 „Uppsetning tölvupóstskráningar“.

---

## <a name="to-start-logging-email"></a>Að hefja skráningu tölvupósts
1. Ef hefja á skráningu tölvupósts, á **skráningarsíðu** tölvupósts, er kveikt á **virkjunni** skipta.
2. Skráðu þig inn með Exchange Online reikningnum sem áætlaða vinnslan mun nota til að tengjast samnýttu pósthólfinu og vinna úr tölvupósti.

    > [!NOTE]
    > Ef notandi er ekki beðinn um að skrá sig inn Exchange Online í lykilinn getur hann verið vegna þess að vafrinn útilokar sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr https://login.microsoftonline.com.

## <a name="to-stop-logging-email"></a>Að hætta að skrá tölvupóst
## <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience)
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning markaðssetningar** og velja síðan viðkomandi tengil.
1. Slökkva skal á víxlhnappnum **Virkjað**.

## <a name="new-experience"></a>[Ný reynsla](#tab/new-experience)
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **email Innskráning** og veldu svo tengda tengilinn.
2. Slökkva skal á víxlhnappnum **Virkjað**.

---

## <a name="to-change-the-user-account-used-for-email-logging"></a>Breyta notandareikning sem notaður er við innskráningu í tölvupósti
Ef notuð er ný reynsla er hægt að breyta notandareikning sem notaður er við innskráningu í tölvupósti. Núverandi reynsla styður þetta ekki.

## <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience) 
Slökkva á núverandi uppsetningu, breyta notandanum á **síðunni skráning** tölvupósts og virkja svo aftur tölvupóstskráningu. Einnig er hægt að keyra Uppsetningarleiðbeiningar aðstoðar.

## <a name="new-experience"></a>[Ný reynsla](#tab/new-experience)
### <a name="prod_short-online"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Á netinu
1. Skráðu þig inn til [!INCLUDE[prod_short](includes/prod_short.md)] að nota lykilinn sem áætlaða vinnslan notar til að tengjast samnýttu pósthólfinu og vinna úr tölvupósti. Þessi reikningur verður að hafa aðgang að báðum [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **email Innskráning** og veldu svo tengda tengilinn. 
3. Velja **tengda** og síðan **verkraðarafærslu**.
4. **Endurræsa vinnslu Tölvupóstskráningar**.

### <a name="prod_short-on-premises"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Innanhúss
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **email Innskráning** og veldu svo tengda tengilinn. 
2. Velja **skal aðgerðir** og **Endurnýja tákn**.
3. Skráðu þig inn með Exchange Online reikningnum sem áætlaða vinnslan mun nota til að tengjast samnýttu pósthólfinu og vinna úr tölvupósti.

## <a name="see-also"></a>Sjá einnig
[Stjórnun tengsla](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]