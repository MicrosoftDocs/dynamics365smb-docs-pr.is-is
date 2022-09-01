---
title: Framlenging á stjórnun VSK-flokksins fyrir Bretland
description: Hægt er að taka þátt í öðrum fyrirtækjum til að mynda VSK-flokk þar sem allir aðilar tilkynna virðisaukaskatt í einu aftur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.form: 4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,
ms.date: 07/08/2022
ms.author: bholtorf
ms.openlocfilehash: b428973ab64d22b2e336a8067979bc7257af173b
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361529"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Framlenging á stjórnun VSK-flokksins fyrir Bretland

Hægt er að tengja eitt eða fleiri fyrirtæki við Bretland til að sameina virðisaukandi skatt (VSK) sem er skráð undir einu Skráningarnúmeri. Þessi tilhögun er kölluð *VSK-hópur*. Hægt er að taka þátt í hópnum sem meðlimur eða sem hópfulltrúi.

## <a name="forming-a-vat-group"></a>VSK-flokkur myndast

VSK-flokksmeðlimir og hópfulltrúarnir geta notað leiðbeiningar um **uppsetningu VSK-flokka** sem bæði skilgreina þátttöku þeirra í hópnum og stofna tengingu á milli leigjenda þeirra [!INCLUDE[prod_short](includes/prod_short.md)]. Meðlimir hópsins nota þessa tengingu til að senda VSK-skilagreinar sínar til flokkafulltrúa. Hópfulltrúinn notar þá einu VSK-framtali til að senda VSK-flokkinn til skattyfirvalda.

[!INCLUDE[prod_short](includes/prod_short.md)] styður vöruuppsendingar innan-flokka VSK fyrir fyrirtæki sem nota [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss eða á neti, í hvaða samsetningu sem er, sem hafa áhrif á uppsetningu samskiptanna á milli fyrirtækja. Í þessari grein er lýst ýmsum hópuppsetum.

### <a name="license-requirements"></a>Kröfur leyfis

Þátttakendur í hópnum hljóta leyfi til að nota [!INCLUDE[prod_short](includes/prod_short.md)]. Ekki er hægt að nota gestareikninga í VSK-flokkum.

* Til að reikna og senda inn VSK-skil þarf notandi að vera fullur [!INCLUDE[prod_short](includes/prod_short.md)] notandi.
* Til að skrá sig inn og gera grunnverkin, til dæmis Stofna reikninga, þarf leyfi fyrir [!INCLUDE[prod_long](includes/prod_long.md)] teymismeðlim.

## <a name="set-up-a-vat-group"></a>Setja upp VSK-flokk

Hér á eftir er mælt með röð þeirra skrefa sem kerfisstjóri notar til að setja upp VSK-flokk:

1. Stofna uppsetninguna í [Azure Active Directory fyrir flokksmeðlimi](#azure-active-directory-setup-for-group-members).
2. Samnýta tæknilegar upplýsingar VSK-meðlimir og hópfulltrúarnir þurfa að tengjast leigjendum sínum [!INCLUDE[prod_short](includes/prod_short.md)]. Oftast hefur fulltrúi hópsins þessar upplýsingar, svo sem [API-vefslóð](#group-api-setup) og nafn umhverfis-og þjónustufulltrúa VSK-flokka VSK-aðilar senda VSK-gögn til sín.
3. Stofna notendur sem VSK-flokksmenn nota til að sannvotta þegar þeir tengjast VSK- [!INCLUDE[prod_short](includes/prod_short.md)] flokki fulltrúa. Notendur verða að hafa Full notendaleyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].
4. Keyra Uppsetningarleiðbeiningar fyrir **uppsetningu VSK-Flokkstjórnunar** til að tengja meðlimi VSK-flokka.

   VSK-flokkurinn verður að veita ákveðnum upplýsingum til flokks meðlima til að ljúka uppsetningu þeirra. (Lærðu meira á [Setja upp kafla VSK-flokka](#set-up-vat-group-members) hér á eftir.) Gera skal athugasemd við **flokksmeðliðakerfi** fyrir hvern VSK-flokk. Hópfulltrúinn þarf þessi kenni til að bæta fyrirtækjunum við VSK-flokkinn.
5. Setja upp VSK-flokkstjórnkerfisstjórnun í VSK-flokksfulltrúanum með því að nota leiðbeiningar um [!INCLUDE[prod_short](includes/prod_short.md)] uppsetningu VSK- **flokks**

> [!NOTE]
> Til að tengjast VSK-hópfulltrúunum verða Meðlimir flokksins að hafa notandareikning sem hefur aðgang að VSK- [!INCLUDE[prod_short](includes/prod_short.md)] flokkafulltrúa. VSK-flokksfulltrúi verður að stofna a.m.k. einn notanda vegna þessa. Hins vegar, af öryggisástæðum, er mælt með því að þeir búi til notanda fyrir hvern VSK-flokk, sem getur verið kerfisnotandareiknings sem ekki er tengdur raunverulegum einstaklingi. Gættu þess að dreifa notandaskilríkjum á VSK-flokk meðlima á öruggan hátt.

### <a name="azure-active-directory-setup-for-group-members"></a>Azure Active Directory Uppsetning fyrir meðlimi hópsins

Þegar VSK-flokksfulltrúi er notaður [!INCLUDE[prod_short](includes/prod_short.md)] á neti eða innanhúss, verða Azure Active Directory meðlimir VSK-flokka að votta notendur þegar þeir senda VSK-skil á VSK-flokksfulltrúa. Til [!INCLUDE[prod_short](includes/prod_short.md)] að innanhúss séu aðilar að samskipa stökum táknmálsmerki. Frekari upplýsingar er að [samskipa Azure Active Directory SANNVOTTUN með ws-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Ef meðlimir VSK-flokksins eru einnig með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu getur aðilinn Vottað með tilgreindum notendaskilríkjum og innskráningarupplýsingum sem fulltrúi hópsins veitir. Frekari upplýsingar eru í kaflanum Uppsetning meðlima [VSK-flokka hér að](#set-up-vat-group-members) neðan.

Meðlimir VSK-hóps sem eru með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum verða að setja upp skráningu forrits í Azure Active Directory fyrir VSK-hópinn í [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda fulltrúans. App-skráningin gerir kleift að tengjast VSK- [!INCLUDE[prod_short](includes/prod_short.md)] flokki fulltrúa á netinu til að sannvotta hópmeðliminn. Frekari upplýsingar hjá [Quickstart: skráðu inn umsókn með Platform](/azure/active-directory/develop/quickstart-register-app) Microsoft auðkennislykill.

Þegar umsjónarmaður VSK-flokksins stofnar App skráningu í Azure Active Directory flokkinn verða þeir að tilgreina eftirfarandi upplýsingar.

* **Í hlutanum sannvottun** skal bæta við **vef** sem vettvang og nota eftirfarandi **redirect vefslóð** :`https://businesscentral.dynamics.com/OAuthLanding.htm`.
* Í hlutanum **Sannvottun**, í valkostinum fyrir **Studdar reikningsgerðir**, skal velja **Reikningar í hvaða notendaskrá fyrirtækis sem er (Hvaða Azure AD notendaskrá sem er - Margir leigjendur)**.
* Í hlutanum **Vottorð og leynilyklar** skal búa til nýjan leynilykil biðlara og skrá niður gildið. Meðlimir VSK-hópsins þurfa á leynilyklinum að halda þegar þeir setja upp tenginguna við fulltrúa hópsins.
* Í hlutanum **API-heimildir** skal bæta heimildum við [!INCLUDE[prod_short](includes/prod_short.md)]. Virkja úthlutun aðgangs fyrir **Financials.ReadWrite.All** og **user_impersonation**.
* Í hlutanum **Yfirlit** skal skrá hjá sér **Kenni forrits (biðlara)**. Meðlimir VSK-hópsins þurfa á auðkenninu að halda þegar þeir setja upp tenginguna við fulltrúa hópsins.

### <a name="group-api-setup"></a>Uppsetning API-flokks

VSK-flokksfulltrúinn stofnar og veitir API til flokksmanna. Landsmenn nota þetta API til að tengjast leigjandanum og senda inn VSK- [!INCLUDE[prod_short](includes/prod_short.md)] skilagreinar. VSK-flokka aðilar nota [!INCLUDE[prod_short](includes/prod_short.md)] oft í aðskilnað Azure Active Directory leigjenda. Af þeirri ástæðu þarf að tengja uppsetningu við meðlimi VSK-flokksins og fulltrúa hans [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Þessi uppsetning krefst skilríkja fyrir stjórnandareikning sem hefur fullt notendaleyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

1. Í Viðskiptastöð aðalstöðvar fyrir leigjanda á Þingvöllum er flipinn umhverfi **valinn**.
1. Veldu umhverfi fulltrúaráðs.
1. **Í kaflanum upplýsingar** skal afrita **vefslóðina**.
1. Opna Notepad og líma VEFSLÓÐINA. Skipta `https://businesscentral.dynamics.com` um `https://api.businesscentral.dynamics.com/v2.0`.

## <a name="set-up-vat-group-members"></a>Setja upp VSK-flokksmenn

VSK-flokkur aðilar tengjast fulltrúa með því að kalla eftir vefþjónustu á leigjendavandanum VSK-flokkafulltrúa. Sannvotta verður kallinum með OAuth2. Þegar Uppsetning VSK-hópstjórnunar er uppsett eru aðilar beðnir um að sannvotta að VSK-flokksfulltrúi hafi aðgangstákn sem er búið til og vistað. Aðgangslykillinn er notaður VSK-skýrslum er skilað inn í VSK-hóp fulltrúans.

> [!IMPORTANT]
> Aðildarfyrirtækin í VSK-flokknum þurfa ekki að tengjast HMRC þar sem þau eru tilkynnt í gegnum fulltrúa hópsins.

Áður en VSK-aðilar hefja uppsetningu sína (hér að neðan) þurfa þeir að hafa samband við VSK-flokkafulltrúa fyrir eftirfarandi upplýsingar um leigjendur sína [!INCLUDE[prod_short](includes/prod_short.md)]:

* API-vefslóðin
* Heiti fyrirtækisins
* Skrá inn innskráningarupplýsingar fyrir úthlutaðan notanda

1. Í efst í hægra horninu skaltu velja **stillingar stillinga**![.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") Táknið velur **síðan Uppsetningaraðgerð** aðstoðar.
2. **Veljið aðgerðina Setja upp VSK-Flokksstjórnun**.
3. **Í reitnum hlutverk** VSK-flokks skal velja **meðlim** **næst**.
4. Afritið gildið í reitnum **Kenni hópmeðlims** og deilið því síðan með fulltrúa VSK-hópsins svo hann geti bætt fyrirtækinu við sem samþykktum meðlimi hópsins.
5. **Í reitnum Útgáfufulltrúi** afurðastöðva er tilgreind útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] sem fulltrúi notar.
6. **Í reit API-URL** er API-vefslóð færð inn sem VSK-flokksfulltrúi sem veitir. Yfirleitt er vefslóðin á eftirfarandi sniði: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Til dæmis, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. **Í reitinn Hópfulltrúi fyrirtækis** er fært inn FYRIRTÆKJAHEITI VSK-flokkafulltrúa, svo sem, **CRONUS UK ehf**.
8. **Í reitnum Tegund** auðkenningar er valið **OAuth2**. Ef VSK-flokksfulltrúi er notaður [!INCLUDE[prod_short](includes/prod_short.md)] á netinu skal gera hópnum kleift að **nota miðnetsvíxl** og velja **síðan Next**.

   Síðan skal fylgja skrefunum annaðhvort [notar VSK-flokkurinn viðskipti miðsvæðis á netinu](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eða [VSK-Flokkafulltrúi notar Business Central innanhússkaflann](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises) hér á eftir.

### <a name="vat-group-representative-uses-business-central-online"></a>VSK-flokkafulltrúi notar Business miðlægt í netinu

1. Færa inn notendaskilríkið sem VSK-flokksfulltrúi veitir og bæta nauðsynlegum heimildum við til að mynda aðgangstakið.
2. Veldu skilgreininguna á VSK-skýrslu sem þú notar til að senda VSK-skilagreinar til bresku skattyfirvalda. 

Þegar búið er að ljúka uppsetningunni verður stofnuð ný skilgreining, [!INCLUDE[prod_short](includes/prod_short.md)] byggð á þessu vali sem gerir kleift að senda VSK-fulltrúa til VSK-flokksins.

### <a name="vat-group-representative-uses-business-central-on-premises"></a>VSK-flokkur fulltrúi notar Business miðlægt innanhúss

1. Færa inn notendaskilríkið sem VSK-flokksfulltrúi veitir og velur **Next**.
2. **TILGREINIÐ kenni biðlara frá App-skráningunni** í reitnum Kenni [Azure Active Directory](#azure-active-directory-setup-for-group-members) biðlara.
3. **Í reitnum leyninúmer** biðlara skal tilgreina leynireitinn viðskiptavinur úr App skráningu í Azure Active Directory.
4. **Í reitinn oAuth 2,0 Authority endastöð** er fært inn `https://login.microsoftonline.com/common/oauth2`.
5. **Í reitinn eijörð 2,0. URL** er fært inn `https://api.businesscentral.dynamics.com/`.
6. **Í svæðinu eiauth 2,0** er fært inn `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. Þegar búið er að tilgreina hin ýmsu svæði er **smellt á áfram** og síðan staðfest tenging til að mynda aðgangstákn.
8. Veldu skilgreininguna á VSK-skýrslu sem þú notar til að senda VSK-skilagreinar til bresku skattyfirvalda.

## <a name="set-up-the-vat-group-representative"></a>Setja upp VSK-flokkafulltrúa

> [!NOTE]
> Til innanhúss, [!INCLUDE[prod_short](includes/prod_short.md)] styður aðeins við eitt leigjanda tilvik af hópfulltrúunum.

> [!IMPORTANT]
> Fulltrúafélagið verður að gera uppsetningu á **HMRC VSK-tengingu virka á** síðunni þjónustutengingar **.** Fulltrúar verða einnig að sækja VSK-skilatímabil frá HMRC.

1. Efst í hægra horninu er valið stillingar fyrir **stillingar** teikn ![.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og síðan er Uppsetningaraðgerðin **aðstoða valin**.
2. **Veljið aðgerðina Setja upp VSK-Flokksstjórnun**.
3. **Í reitnum hlutverk** VSK-flokks er hægt að velja **fulltrúa** til að vinna sem fulltrúi VSK og velja **síðan Next**.
4. **Í svæðinu Flokkur Jöfnunarlykils** skal tilgreina jöfnunarlykilinn sem notaður er fyrir upphæð VSK-skatts flokksins.
5. **Í reitnum VSK-Uppgjörsreikningur** skal tilgreina lykilinn sem notaður er fyrir VSK-uppgjör.
6. Í reitnum **VSK-skuld nr.** Er reiturinn tilgreindur sem táknar heildarupphæð VSK vegna innsendingar VSK-flokks.
7. **Í reitnum sniðmát** flokksjöfnuðasafns er tilgreint færslubókarsniðmát sem notað er til að stofna skjalið sem hópfulltrúinn BÓKAR flokkinn VAT á uppgjörsreikninginn.
8. **Reiturinn samþykktir félags** sýnir fjölda flokksmanna sem eru settir upp til að senda VSK-skilagreinar til flokkafulltrúa. Ef bæta á við nýjum meðlimum er númerið valið til að opna **síðu VSK-flokks samþykktra meðlima** og eftirfarandi upplýsingum bætt við:
    1. **Í reitinn FLOKKSAUÐKENNI** flokksins er fært inn kenni fyrir meðlimi flokksins eins og það birtist meðan á flokksuppsetningu stendur (frekari upplýsingar eru í kaflanum um [meðlim](#set-up-vat-group-members) VSK-flokks hér að ofan).
    2. **Í reitnum Heiti** flokksins er tilgreint heiti á meðlimi flokksins.
    3. **Í svæðinu fyrirtæki** skal tilgreina fyrirtækið sem HÓPAÐILDIN sendir VSK inn á [!INCLUDE[prod_short](includes/prod_short.md)], ss., **CRONUS UK ehf**.
    4. Tilgreinið tengiliðaupplýsingar fyrirtækisins.

## <a name="use-the-vat-group-management-features"></a>Nota stjórnunaraðgerðirnar VSK-hópstjórnun

Meðlimir VSK-hóps nota hefðbundin ferli til að ganga frá VSK-skýrslum. Eini munurinn er að félagsmenn verða að velja **skýrslu vataflokksins** á **skilasíðu** virðisaukaskatts til að senda inn skilamat á VSK-flokkafulltrúa frekar en hjá yfirvöldum. Frekari upplýsingar á [um VSK-skilaskýrslu](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Meðlimir VSK-hóps geta leiðrétt innsendar VSK-skýrslur svo lengi sem fulltrúi hópsins hafi ekki sent frá sér VSK-skýrsluna fyrir hópinn. Til að gera leiðréttingu verður meðlimur VSK-hópsins að búa til VSK-skýrslu fyrir tímabil VSK-skýrslunnar og senda hana til fulltrúa VSK-hópsins. Á hlið VSK-flokkafulltrúa kemur nýjasta VSK-skilagrein meðlimurinn á undan og er innifalin á **síðunni VSK-skil**.

Í eftirfarandi köflum er lýst verkefnum sem VSK-flokksfulltrúar verða að gera til að skrá VSK-flokk.

### <a name="review-vat-member-submissions"></a>Endurskoða VSK-meðlim-sendingar

Síðan **Innsendingar VSK-hóps** birtir VSK-skýrslurnar sem meðlimir hafa sent inn. Síðan virkar sem staðsetning þar sem drög að innsendingum þar til fulltrúi VSK-hópsins tekur þær með í VSK-skýrslu fyrir hópinn. Fulltrúi getur opnað innsendingar til að fara yfir einstaka reiti þar sem hver meðlimur VSK-flokksins er tilkynntur.

> [!TIP]
> **Á síðunni VSK-Skilatímabil** sýnir reiturinn flokksmeðliðaflokkur **um** hversu mörg skil aðilar hafa sent. Til að tryggja að þessi tala sé up-til-dagsetning er valið **aðgerðin Sækja VSK-skil**.

### <a name="create-a-group-vat-return"></a>Stofna VSK-vöruflokk

Til að tilkynna VSK fyrir flokkinn, á **síðunni skil** á VSK-skilum, STOFNAST aðeins VSK fyrir fyrirtækið. Eftir á skal bæta við nýjustu innsendingum á VSK frá meðlimum VSK-hópsins með því að velja aðgerðina **Hafa með VSK-hóp**.  

Þegar að hópfulltrúi hefur sent inn VSK-reikning **hópsins til yfirvalda, þá keyrir fulltrúi þeirra vanalega í** að reikna og bóka VSK-aðgerðina. Þessi aðgerð lokar opnum VSK-færslum og upphæðir færslna á VSK-uppgjörsreikning. Sem stendur tekur þessi aðgerð ekki tillit til hópuppgjafar. Aðeins VSK-færslur fulltrúa fyrirtækisins í VSK-flokki eru bókaðar. Fyrirframsettar upphæðir VSK-flokks meðlima verður að bóka í VSK-jöfnunarupphæðina handvirkt þannig að VSK-jöfnunarreikningur fulltrúa VSK-flokksins endurspeglar ábyrgð þess sem var tilkynntur yfirvöldum. Þessi hegðun mun breytast í komandi uppfærslu [!INCLUDE[prod_short](includes/prod_short.md)], svo allur HÓPURINN VSK (heildarupphæð í skýrslulínum VSK-skila) er jöfnuð.

> [!IMPORTANT]
> VSK-flokksvirkni er aðeins studd á þeim mörkuðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] notar VSK-rammi sem inniheldur VSK-skil og VSK-skilatímabil. Ekki er hægt að nota VSK-flokka á mörkuðum með aðrar útfærslur af staðbundnum VSK-tilkyningum, eins og Austurríki, Þýskaland, Ítalía, Spánn og Sviss.

## <a name="see-also"></a>Sjá einnig .

[Bretland staðbundin virkni í bresku útgáfunni](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Tax Digital í Bretlandi](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
