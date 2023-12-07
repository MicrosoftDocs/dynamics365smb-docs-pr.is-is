---
title: Viðbót fyrir stjórnun VSK-hóps fyrir Bretland
description: Þú getur tengst öðrum fyrirtækjum og stofnað VSK-hóp þar sem allir meðlimir geta tilkynnt um VSK í einni skilagrein.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: soalex
ms.topic: conceptual
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 09/18/2023
---

# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Viðbót fyrir stjórnun VSK-hóps fyrir Bretland

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Þú getur tengt saman eitt eða fleiri fyrirtæki í Bretlandi til að sameina VSK-skil undir einu skráningarnúmeri. Þessi tilhögun er kölluð *VSK-hópur*. Hægt er að taka þátt í hópnum sem meðlimur eða fulltrúi hópsins.

## <a name="forming-a-vat-group"></a>Mynda VSK-flokk

Meðlimir VSK-hóps og fulltrúi hans geta notað uppsetningarleiðbeininguna **Uppsetning á stjórnun VSK-hóps** með hjálp bæði til að skilgreina aðkomu þeirra að hópnum og búa til tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda þeirra. Meðlimir hópsins nota tenginguna til að senda VSK-skýrslur sínar til fulltrúa hópsins. Fulltrúi hópsins notar þá eitt VSK-framtal til að standa skil á VSK hópsins til skattyfirvalda.

[!INCLUDE[prod_short](includes/prod_short.md)] styður VSK-skil innan samstæðu fyrir fyrirtæki sem nota [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss eða á netinu, í hvaða samsetningu sem er, sem hefur áhrif á uppsetningu samskipta á milli fyrirtækja. Í þessari grein er lýst ýmsum hópuppsetningum.

### <a name="license-requirements"></a>Leyfiskröfur

Þátttakendur í hópnum verða að hafa leyfi til að nota [!INCLUDE[prod_short](includes/prod_short.md)]. Þú getur ekki notað gestareikninga í VSK-hópum.

* Notandi verður að vera fullgildur notandi [!INCLUDE[prod_short](includes/prod_short.md)] til að reikna út og skila VSK-framtölum.
* Til að skrá þig inn og sinna grunnverkefnum, svo sem að stofna reikninga, þarftu [!INCLUDE[prod_long](includes/prod_long.md)] leyfi fyrir meðlimi hóps.

## <a name="set-up-a-vat-group"></a>Setja upp VSK hóp

Eftirfarandi er ráðlögð röð skrefa sem stjórnandi notar til að setja upp VSK-hóp:

1. Stofna uppsetningu í [Microsoft Entra uppsetningu kennis fyrir hópmeðlimi](#microsoft-entra-id-setup-for-group-members).
2. Deilið tæknilegum upplýsingum sem meðlimir og fulltrúi VSK-hópsins þurfa á að halda til að tengjast [!INCLUDE[prod_short](includes/prod_short.md)]-leigjandanum sínum. Venjulega hefur fulltrúi VSK-hópsins þessar upplýsingar, svo sem [API-vefslóðina](#group-api-setup) og heiti fulltrúa umhverfis VSK-hópsins sem meðlimir VSK-hópsins senda VSK-gögnin sín til.
3. Stofna notendur sem meðlimir VSK-hópsins nota til að staðfesta hvenær þeir tengjast fulltrúa VSK-hópsins [!INCLUDE[prod_short](includes/prod_short.md)]. Notendurnir verða að hafa fullgilt notendaleyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].
4. Keyrið uppsetningarleiðbeininguna **Setja upp umsjón VSK-hópa** með hjálp til að tengja meðlimi VSK-hópsins.

   Fulltrúi VSK-hópsins verður að veita hópmeðlimum tilteknar upplýsingar til að ljúka við uppsetningu þeirra. (Frekari upplýsingar er að finna í hlutanum [Setja upp meðlimi VSK-hóps](#set-up-vat-group-members) hér að neðan). Gera skal grein fyrir **Auðkenni hópmeðlims** fyrir hvern meðlim VSK-hópsins. Fulltrúi hópsins þarf þessi kenni til að bæta fyrirtækjunum við VSK-hópinn.
5. Setjið upp viðbótina fyrir umsjón VSK-hóps í VSK-hóp [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans með því að nota uppsetningarleiðbeininguna **Setja upp umsjón VSK-hópa** með hjálp.

> [!NOTE]
> Til að tengjast fulltrúa VSK-hópsins þurfa hópmeðlimir að vera með notandareikning hefur aðgang að fulltrúa VSK-hópsins [!INCLUDE[prod_short](includes/prod_short.md)]. Fulltrúi VSK-hópurinn verður að búa til að minnsta kosti einn notanda fyrir þetta. Af öryggisástæðum mælum við þó með því að notendur stofni VSK-hóp fyrir hvern meðlim, sem getur verið kerfisnotendareikningur sem tengist ekki raunverulegum aðila. Gangið úr skugga um að dreifa notandaskilríkjum til þessara meðlima VSK-hópsins á öruggan hátt.

### <a name="microsoft-entra-id-setup-for-group-members"></a>Microsoft Entra Uppsetning kennis fyrir hópmeðlimi

Þegar fulltrúi VSK-flokksins notar [!INCLUDE[prod_short](includes/prod_short.md)] netið eða innanhúss verða meðlimir VSK-flokksins að nota Microsoft Entra kenni til að sannvotta notendur þegar þeir senda VSK-skil til fulltrúa VSK-flokksins. Innanhúss [!INCLUDE[prod_short](includes/prod_short.md)] verða meðlimir að stilla einskráningu. Nánari upplýsingar eru í [Grunnstilla Microsoft Entra sannvottun með WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Ef meðlimir VSK-hópsins nota einnig [!INCLUDE[prod_short](includes/prod_short.md)] á netinu getur meðlimurinn staðfest með tilgreindum notendaskilríkjum og innskráningarupplýsingum frá fulltrúa hópsins. Fáðu frekari upplýsingar í hlutanum [Setja upp meðlimi VSK-hópa](#set-up-vat-group-members) hér að neðan.

Meðlimir VSK-flokks sem eru [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum þurfa að setja upp skráningu forrits í Microsoft Entra kenni fyrir leigjanda VSK-flokksins [!INCLUDE[prod_short](includes/prod_short.md)] . Skráning forritsins gerir fulltrúa VSK-hópsins [!INCLUDE[prod_short](includes/prod_short.md)] netinu kleift að sannvotta meðlim hópsins. Frekari upplýsingar er að finna hér [Stuttar leiðbeiningar: Skráið forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app).

Þegar stjórnandi VSK-flokksins stofnar skráningu forritsins með Microsoft Entra kenni verða þeir að tilgreina eftirfarandi upplýsingar.

* Í hlutanum **Sannvottun** skal bæta við **Vef** sem verkvang og nota eftirfarandi **Framsendingarvefslóð**: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* Í hlutanum **Sannvottun**, í valkostinum til að velja **Studdar reikningstegundir**, skal velja **Reikningar í hvaða stjórnunarskrá sem er (Any Microsoft Entra directory - Multitenant)**.
* Í hlutanum **Vottorð og leynilyklar** skal búa til nýjan leynilykil biðlara og skrá niður gildið. Meðlimir VSK-hópsins þurfa á leynilyklinum að halda þegar þeir setja upp tenginguna við fulltrúa hópsins.
* Í hlutanum **API-heimildir** skal bæta heimildum við [!INCLUDE[prod_short](includes/prod_short.md)]. Virkja úthlutun aðgangs fyrir **Financials.ReadWrite.All** og **user_impersonation**.
* Í hlutanum **Yfirlit** skal skrá hjá sér **Kenni forrits (biðlara)**. Meðlimir VSK-hópsins þurfa á auðkenninu að halda þegar þeir setja upp tenginguna við fulltrúa hópsins.

### <a name="group-api-setup"></a>Uppsetning API-hóps

Fulltrúi VSK-hópsins útbýr og afhendir API til meðlima hópsins. Meðlimirnir nota þetta API til að tengjast [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda fulltrúans og skila VSK-framtölum. Meðlimir VSK-flokks nota [!INCLUDE[prod_short](includes/prod_short.md)] oft í sérstökum Microsoft Entra leigjendum. Þess vegna þarf að setja upp uppsetningu til að tengja meðlim VSK-hópsins og [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans.

> [!NOTE]
> Þessi uppsetning krefst skilríkja stjórnandareiknings sem er með fullt notendaleyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

1. Í stjórnendamiðstöð Business Central fyrir fulltrúa leigjanda skal velja flipann **Umhverfi**.
1. Veldu umhverfi fulltrúans.
1. Afritaðu **vefslóðina** í hlutanum **Upplýsingar**.
1. Opnaðu glósubókina og límdu inn vefslóðina. Skipta `https://businesscentral.dynamics.com` út fyrir `https://api.businesscentral.dynamics.com/v2.0`.

## <a name="set-up-vat-group-members"></a>Setja upp meðlimi VSK-hópa

Meðlimir VSK-hóps tengjast fulltrúanum með því að hafa samband við vefþjónustu í VSK-hópnum í leigjanda fulltrúans. Sá sem hefur samband verður að vera sannvottaður með OAuth2. Þegar framlenging á umsjón með VSK-hópi hefur verið sett upp eru meðlimir beðnir um að staðfesta hjá fulltrúa VSK-hópsins en þá myndast aðgangstákn og það er vistað. Aðgangslykillinn er notaður VSK-skýrslum er skilað inn í VSK-hóp fulltrúans.

> [!IMPORTANT]
> Aðildarfyrirtækin í VSK-hópnum þurfa ekki að tengjast HMRC vegna þess að þau tilkynna í gegnum fulltrúa hópsins.

Áður en meðlimir VSK-hópsins hefja uppsetningu sína (sjá hér að neðan) þurfa þeir að hafa samband við fulltrúa VSK-hópsins til að fá eftirfarandi upplýsingar um [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda sinn:

* API-vefslóðin
* Heiti fyrirtækisins
* Skrá inn innskráningarupplýsingar fyrir úthlutaðan notanda

1. Í efra hægra horninu, velja **Stillingar** ![stillingar.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") táknið, veldu þá aðgerðina **Aðstoð við uppsetningu**.
2. Veldu aðgerðir til að **Setja upp umsjón VSK-hópa**.
3. Í reitnum **Hlutverk í VSK-hóp** er valið **Meðlimur** og síðan **Áfram**.
4. Afritið gildið í reitnum **Kenni hópmeðlims** og deilið því síðan með fulltrúa VSK-hópsins svo hann geti bætt fyrirtækinu við sem samþykktum meðlimi hópsins.
5. Í reitnum **Vöruútgáfa fulltrúa hóps** skal tilgreina hvaða útgáfu [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans er verið að nota.
6. Í **API-vefslóðinni** slærðu inn API-vefslóðina sem fulltrúi VSK-hópsins lætur í té. Yfirleitt er vefslóðin á eftirfarandi sniði: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Til dæmis, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. Í reitnum **Fyrirtæki í forsvari fyrir hóp** fyrirtækisheiti fyrir fulltrúa VSK-hópsins, t.d., **CRONUS UK Ltd**.
8. Í reitnum **Sannvottunargerð** skal velja **OAuth2**. Ef fulltrúi VSK hópsins er að nota [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er valinn valkosturinn **Fulltrúi hóps notar Business Central Online** og velur svo **Áfram**.

   Fylgdu svo skrefunum þar sem annaðhvort [fulltrúi VSK-hópsins notar Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eða hlutann [fulltrúi VSK-hópsins notar Business Central innanhúss](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises) að neðan.

### <a name="vat-group-representative-uses-business-central-online"></a>Fulltrúi VSK-hóps notar Business Central Online

1. Sláðu inn notendaskilríkin sem fulltrúi VSK-hópsins framvísar og bættu við áskildum heimildum til að búa til aðgangstáknið.
2. Veldu stillingar fyrir VSK-skýrslu sem þú notar til að senda inn VSK-framtöl til skattyfirvalda í Bretlandi. 

Eftir að uppsetningu er lokið býr [!INCLUDE[prod_short](includes/prod_short.md)] til nýja stillingu sem byggir á þessu vali sem gerir þér kleift að senda VSK-framtöl til fulltrúa VSK-hópsins.

### <a name="vat-group-representative-uses-business-central-on-premises"></a>Fulltrúi VSK-hóps notar Business Central innanhúss

1. Sláðu inn notendaskilríkin sem fulltrúi VSK-hópsins lét í té og veldu **Áfram**.
2. Í reitnum **Kenni** biðlara skal tilgreina kenni biðlara úr skráningu forritsins í [Microsoft Entra uppsetningu kennis fyrir hópmeðlimi](#microsoft-entra-id-setup-for-group-members).
3. Í reitnum **Leyndarmál** biðlara er tilgreint leyndarmál biðlarans úr skráningu forritsins í Microsoft Entra kenni.
4. Í reitinn **OAuth 2.0 endastöð eftirlits** skal færa inn `https://login.microsoftonline.com/common/oauth2`.
5. Í reitinn **OAuth 2.0 vefslóð tilfangs** skal færa inn `https://api.businesscentral.dynamics.com/`.
6. Í reitinn **OAuth 2.0 framsendingarvefslóð** skal færa inn `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. Þegar þú hefur tilgreint hina ýmsu reiti velur þú **Áfram** og staðfestir síðan tengingu sannvottunar til að búa til aðgangsmerkið.
8. Veldu stillingar fyrir VSK-skýrslu sem þú notar til að senda inn VSK-framtöl til skattyfirvalda í Bretlandi.

## <a name="set-up-the-vat-group-representative"></a>Setja upp fulltrúa VSK-hópsins

> [!NOTE]
> Notkun innanhúss [!INCLUDE[prod_short](includes/prod_short.md)] styður aðeins eitt tilvik leigjanda fyrir fulltrúa hópsins.

> [!IMPORTANT]
> Fyrirtæki fulltrúa verður að virkja þjónustutenginguna **Uppsetning HMRC á VSK** á síðunni **Þjónustutengingar**. Fulltrúar verða einnig að sækja skilatímabil virðisaukaskatts hjá HMRC.

1. Í efra hægra horninu skaltu velja **Stillingar** táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og velja síðan aðgerðina **Uppsetning með hjálp**.
2. Veldu aðgerðir til að **Setja upp umsjón VSK-hópa**.
3. Í reitnum **Hlutverk VSK-hópsins** velur þú **Fulltrúa** til að starfa sem fulltrúi VSK-hópsins og velur síðan **Áfram**.
4. Í reitnum **Reikningur fyrir hópuppgjör** skal tilgreina þann uppgjörsreikning sem notaður er fyrir VSK-fjárhæðir hópmeðlima. Þessi reikningur ætti að hafa **Eignir** sem **reikningsflokk**.
5. Í reitnum **VSK-uppgjörsreikningur** skaltu tilgreina reikninginn sem þú notar fyrir VSK-uppgjör. Þessi reikningur ætti að hafa **Skuldir** sem **reikningsflokk**.
6. Í **Reitarnúmer VSK til greiðslu.** reitinn, tilgreindu reitinn sem táknar samtölu VSK-upphæðar til greiðslu vegna innsendingar VSK-hóps.
7. Í reitnum **Sniðmát færslubókar hópuppgjörs** skaltu tilgreina sniðmátið fyrir almenna færslubók sem er notað til að búa til skjalið sem fulltrúi hópsins birtir VSK af á jöfnunarreikninginn.
8. Í reitnum **Samþykktir meðlimir** kemur fram fjöldi hópmeðlima sem stofnaðir eru til að skila VSK-framtölum til fulltrúa hópsins. Til að bæta við nýjum meðlimum velur þú númerið til að opna síðuna **Samþykktir meðlimir VSK-hóps** og bætir við eftirfarandi upplýsingum:
    1. Í reitnum **Kenni hópmeðlims** skal slá inn auðkenni hópmeðlima eins og það birtist við uppsetningu hópmeðlima (frekari upplýsingar er að finna í hlutanum [Uppsetning á meðlimi VSK-hóps](#set-up-vat-group-members) hér að ofan).
    2. Í reitnum **Nafn hópmeðlims** skal tilgreina nafn hópmeðlimsins.
    3. Í reitnum **Fyrirtæki** skal tilgreina fyrirtækið sem hópmeðlimurinn sendir VSK-framtöl frá [!INCLUDE[prod_short](includes/prod_short.md)], svo sem **CRONUS UK Ltd**.
    4. Tilgreina frekari upplýsingar fyrir fyrirtækið.

## <a name="use-the-vat-group-management-features"></a>Að nota stjórnunareiginleika VSK-hóps

Meðlimir VSK-hóps nota hefðbundin ferli til að ganga frá VSK-skýrslum. Eini munurinn liggur í að velja skýrsluútgáfuna **VATGROUP** á síðunni **VSK-skil**, sem sendir VSK-skýrsluna til fulltrúa VSK-hópsins frekar en yfirvalda. Frekari upplýsingar er að finna í [Um skýrsluna um VSK skil](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Meðlimir VSK-hóps geta leiðrétt innsendar VSK-skýrslur svo lengi sem fulltrúi hópsins hafi ekki sent frá sér VSK-skýrsluna fyrir hópinn. Til að gera leiðréttingu verður meðlimur VSK-hópsins að búa til VSK-skýrslu fyrir tímabil VSK-skýrslunnar og senda hana til fulltrúa VSK-hópsins. Á síðu VSK-hópsins kemur nýjasta VSK-framtal meðlimsins í stað þeirrar fyrri og kemur fram á síðunni **VSK-skil**.

Í eftirfarandi hlutum er lýst verkunum sem fulltrúar VSK-hóps verða að gera til að standa skil á VSK hópsins.

### <a name="review-vat-member-submissions"></a>Skoða innsendar VSK-umsóknir meðlima

Síðan **Innsendingar VSK-hóps** birtir VSK-skýrslurnar sem meðlimir hafa sent inn. Síðan virkar sem staðsetning þar sem drög að innsendingum þar til fulltrúi VSK-hópsins tekur þær með í VSK-skýrslu fyrir hópinn. Fulltrúinn getur opnað innsendingarnar til að fara yfir hvern reit sem inniheldur upphæðina sem hver meðlimur VSK-hópsins tilkynnir um.

> [!TIP]
> Á síðunni **VSK-tímabil** sýnir reiturinn fyrir **Innsendingar hópmeðlima** hve margir meðlimir hafa skilað inn skilagreinum. Veldu aðgerðina **Sækja VSK-framtöl** til að tryggja að þetta númer sé uppfært.

### <a name="create-a-group-vat-return"></a>Stofna VSK-skil fyrir hóp

Til að telja fram VSK fyrir hópsins skal á síðunni **VSK-framtöl** stofna VSK-framtal fyrir eingöngu þitt fyrirtæki. Eftir á skal bæta við nýjustu innsendingum á VSK frá meðlimum VSK-hópsins með því að velja aðgerðina **Hafa með VSK-hóp**.  

Þegar fulltrúi hópsins hefur skilað VSK-framtali til yfirvalda keyrir fulltrúinn venjulega aðgerðina **Reikna og bóka VSK-uppgjör**. Þessi aðgerð lokar opnum VSK-færslum og millifærir upphæðir á reikning VSK-uppgjörs. Sem stendur tekur þessi aðgerð ekki innsendingar hópsins með í reikninginn. Einungis VSK-færslur í fyrirtækinu í forsvari VSK-hópsins eru birtar. Upphæðir innsendinga frá meðlimum VSK-hópsins verða að vera bókaðar á VSK-uppgjörsupphæðina handvirkt þannig að VSK-uppgjörsreikningur hjá fulltrúa VSK-hópsins endurspegli skuldina sem tilkynnt var til yfirvalda. Þessi hegðun mun breytast í væntanlegri uppfærslu á [!INCLUDE[prod_short](includes/prod_short.md)], þannig að allur VSK-hópurinn (heildarupphæð í skýrslulínum í VSK-skýrslunni) verður gerður upp.

> [!IMPORTANT]
> VSK-flokksvirkni er aðeins studd á þeim mörkuðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] notar VSK-rammi sem inniheldur VSK-skil og VSK-skilatímabil. Ekki er hægt að nota VSK-hópa á öðrum mörkuðum sem eru með aðrar útfærslur af staðbundnum VSK-skýrslum, t.d. Austurríki, Þýskaland, Ítalía, Spánn og Sviss.

## <a name="issue-with-enabling-multifactor-authentication-mfa"></a>Útgáfa með gerð multifactor sannvottunar (MFA) virka

Ef villuboð tengjast heimild við endurnýjun OAuth2-táknsins **á** síðunni **VSK-skýrslugrunnur** eftir að MFA hefur verið gert virkt skal ljúka eftirfarandi skrefum.  

1. Skrá sig inn í **Azure Portal** sem sannvottunarstjóra.  
2. Farðu að kenninu **Microsoft Entra**.   
3. Flett er að **notendum** og síðan valinn notandinn sem á að framkvæma aðgerð.  
4.  **Velja skal sannvottunaraðferðirnar** og efst á síðunni skal velja **Krefjast endurskráningar margfölvu sannvottunar**. 
5. Farið er aftur í Dynamics 365 Business Central og valið til að endurnýja táknið úr VSK-skýrslugrunninum **·**.  

Þetta ætti að vera uppsetning í eitt skipti þegar margfengin sannvottun fyrir notandann sem valinn er í **VSK-skýrslugrunni** er gerð virk.  

## <a name="see-also"></a>Sjá einnig .

[Staðbundin virkni Bretlands í breskri útgáfu](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Stafrænir skattar í Bretlandi](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
