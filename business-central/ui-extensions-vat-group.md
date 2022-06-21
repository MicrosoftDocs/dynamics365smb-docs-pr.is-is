---
title: Framlenging á stjórnun VSK-flokksins fyrir Bretland
description: Hægt er að taka þátt í öðrum fyrirtækjum til að mynda VSK-flokk þar sem allir aðilar tilkynna virðisaukaskatt í einu aftur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841921"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Framlenging á stjórnun VSK-flokksins fyrir Bretland

Hægt er að tengja eitt eða fleiri fyrirtæki við landið til að sameina VSK-skýrslur undir einu Skráningarnúmeri. Þessi tilhögun er kölluð *VSK-hópur*. Hægt er að taka þátt í hópnum sem meðlimur eða fulltrúi hópsins.

## <a name="forming-a-vat-group"></a>Mynda VSK-flokk
Meðlimir VSK-hóps og fulltrúi hans geta notað uppsetningarleiðbeininguna **Uppsetning á stjórnun VSK-hóps** með hjálp til að skilgreina aðkomu þeirra að hópnum og búa til tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda þeirra. Meðlimir hópsins nota tenginguna til að senda VSK-skýrslur sínar til fulltrúa hópsins. Fulltrúi beitir einu VSK-framtali til að senda VSK til skattyfirvalda fyrir flokkinn. 

## <a name="license-requirements"></a>Kröfur leyfis
Þátttakendur í hópnum hljóta leyfi til að nota [!INCLUDE[prod_short](includes/prod_short.md)]. Ekki er hægt að nota gestareikninga í VSK-flokkum. 

* Til að reikna og senda inn VSK-skil þarf notandi að vera með fullan Aðalnotanda.
* Til að skrá sig inn og gera grunnverkin, til dæmis Stofna reikninga, er hægt að hafa Dynamics 365 Business Central meðlim Team leyfi.

## <a name="vat-group-constellations"></a>Samskipti innan VSK-hóps
Meðlimir hópsins eiga samskipti við fulltrúa hans. Flokksfulltrúinn útfærir API-VEFSLÓÐ sem gerir meðlimum kleift að senda VSK-skilafulltrúa til VSK-flokksins. 
[!INCLUDE[prod_short](includes/prod_short.md)] styður sendingar á VSK innan hóps fyrir fyrirtæki með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum eða netinu, saman eða annað hvort. Uppsetning samskiptanna fer eftir samskiptanetinu. Í þessari grein er lýst ýmsum stjörnumerkjum hópsins.

Eftirfarandi listi sýnir ráðlagða röð skrefa til að setja upp VSK-hóp:

1. Búa til uppsetninguna í Azure Active Directory. Frekari upplýsingar er að finna í [Kröfur vegna sannvottunar](ui-extensions-vat-group.md#requirements-for-authentication).
2. Deilið tæknilegum upplýsingum sem meðlimir og fulltrúi VSK-hópsins þurfa á að halda til að tengjast [!INCLUDE[prod_short](includes/prod_short.md)]-leigjandanum sínum. Yfirleitt býr fulltrúi VSK-hópsins yfir þessum upplýsingum, t.d. heiti á umhverfinu sem fulltrúi VSK-hópsins notar til að taka á móti VSK frá meðlimum VSK-hópsins.
3. Stofna notendur sem VSK-flokksmenn geta notað til að staðfesta hvenær þeir tengjast VSK-flokki fulltrúa [!INCLUDE[prod_short](includes/prod_short.md)]. Notendur verða að hafa Full notendaleyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].
4. Keyra Uppsetningarleiðbeiningar fyrir **uppsetningu VSK-Flokkstjórnunar** til að tengja meðlimi VSK-flokka.

  Leiðarvísirinn krefst nokkurra upplýsinga frá fulltrúa VSK-hópsins. Frekari upplýsingar er að finna [í setja upp VSK-meðlimi](#set-up-vat-group-members). Skrifið hjá ykkur **Kenni hópmeðlims** fyrir hvern meðlim VSK-hópsins. Fulltrúinn þarf þessi auðkenni til að bæta fyrirtækjunum við VSK-hópinn.
5. Setja upp VSK-flokkstjórnendingendingu í VSK-flokksstjórnunarhandbók með því að nota leiðbeiningar um [!INCLUDE[prod_short](includes/prod_short.md)] uppsetningu VSK- **flokks stjórnunar**. 

> [!NOTE]
> Til að tengjast VSK-hópfulltrúunum verða Meðlimir flokksins að hafa notandareikning sem hefur aðgang að VSK- [!INCLUDE[prod_short](includes/prod_short.md)] flokkafulltrúa. Fulltrúi VSK-hópsins verður að búa til að minnsta kosti einn notanda fyrir þetta, en af öryggisástæðum mælum við með því að notandi verði búinn til fyrir hvern meðlim VSK-hópsins. Gangið úr skugga um að dreifa innskráningarupplýsingunum til þessara meðlima VSK-hópsins á öruggan hátt. Þetta er kerfisnotandareikning sem tengist ekki raunverulegum einstaklingi.

## <a name="about-the-vat-group-management-setup"></a>Um uppsetningu VSK-Hópstjórnunar

VSK-flokksfulltrúi útsetur API til flokksmanna. Landsmenn nota API til að tengjast leigjendavandanum og senda inn VSK- [!INCLUDE[prod_short](includes/prod_short.md)] skilagreinar. VSK-flokka aðilar nota [!INCLUDE[prod_short](includes/prod_short.md)] oft í aðskilnað Azure Active Directory leigjenda. Því er þörf á uppsetningu til að tengja VSK- [!INCLUDE[prod_short](includes/prod_short.md)] meðlimi og fulltrúa. 
  
VSK-flokkur aðilar tengjast fulltrúa með því að kalla eftir vefþjónustu á leigjendavandanum VSK-flokkafulltrúa. Sannvotta verður kallinum með OAuth2. Þegar uppsetningu VSK-Hópstjórnunar er stillt upp er beðið um að sannvotta að VSK-flokksfulltrúi sæki og bjargi aðgangstákn. Aðgangslykillinn er notaður VSK-skýrslum er skilað inn í VSK-hóp fulltrúans. 

## <a name="construct-the-api-url"></a>Reisa API URL
1. Í Viðskiptastöð aðalstöðvar fyrir leigjanda á Þingvöllum er flipinn umhverfi **valinn**.
2. **Í kaflanum upplýsingar** skal afrita **vefslóðina**.
3. Opna Notepad og líma VEFSLÓÐINA. Skipta **https://businesscentral.dynamics.com** um **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Kröfur vegna sannvottunar 
> [!NOTE]
> Þetta krefst skilríkja fyrir stjórnandareikning sem hefur fullt notendaleyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

Þegar VSK-flokksfulltrúi er notaður [!INCLUDE[prod_short](includes/prod_short.md)] á neti eða innanhúss, verða Azure Active Directory meðlimir VSK-flokka að votta notendur þegar þeir senda VSK-skil á VSK-flokksfulltrúa. Til [!INCLUDE[prod_short](includes/prod_short.md)] að innanhúss séu aðilar að samskipa stökum táknmálsmerki. Fyrir frekari upplýsingar sjá [Configure Azure Active Directory AUTHENTICATION með ws-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Ef meðlimir VSK-hópsins eru einnig að nota [!INCLUDE[prod_short](includes/prod_short.md)] á netinu, getur meðlimur hópsins sannvottað sig með því að nota úthlutaðar innskráningarupplýsingar og upplýsingar um endastöð. Frekari upplýsingar er að finna [í setja upp VSK-meðlimi](ui-extensions-vat-group.md#set-up-vat-group-members).

Meðlimir VSK-hóps sem eru með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum verða að setja upp skráningu forrits í Azure Active Directory fyrir VSK-hópinn í [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda fulltrúans. App-skráningin gerir kleift að tengjast VSK- [!INCLUDE[prod_short](includes/prod_short.md)] flokki fulltrúa á netinu til að sannvotta hópmeðliminn. Frekari upplýsingar er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app).

Þegar App-skráningin er búin til í Azure Active Directory þarf að tilgreina eftirfarandi upplýsingar.

* Í hlutanum **Sannvottun** skal bæta við **Vef** sem verkvang og nota eftirfarandi **Framsendingarvefslóð**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Í hlutanum **Sannvottun**, í valkostinum fyrir **Studdar reikningsgerðir**, skal velja **Reikningar í hvaða notendaskrá fyrirtækis sem er (Hvaða Azure AD notendaskrá sem er - Margir leigjendur)**.
* Í hlutanum **Vottorð og leynilyklar** skal búa til nýjan leynilykil biðlara og skrá niður gildið. Meðlimir VSK-hópsins þurfa á leynilyklinum að halda þegar þeir setja upp tenginguna við fulltrúa hópsins.
* Í hlutanum **API-heimildir** skal bæta heimildum við [!INCLUDE[prod_short](includes/prod_short.md)]. Virkja úthlutun aðgangs fyrir **Financials.ReadWrite.All** og **user_impersonation**.
* Í hlutanum **Yfirlit** skal skrá hjá sér **Kenni forrits (biðlara)**. Meðlimir VSK-hópsins þurfa á auðkenninu að halda þegar þeir setja upp tenginguna við fulltrúa hópsins. 

## <a name="set-up-vat-group-members"></a>Setja upp VSK-Flokksmenn
> [!IMPORTANT]
> Aðildarfyrirtækin í VSK-flokknum þurfa ekki að tengjast HMRC þar sem þau eru tilkynnt í gegnum fulltrúa hópsins.

Áður en hafist er handa skal hafa samband við fulltrúa VSK-hópsins vegna eftirfarandi upplýsinga um [!INCLUDE[prod_short](includes/prod_short.md)]-leigjandann hans:

* API-vefslóðin
* Heiti fyrirtækisins 
* Biðlarakenni
* Leyniorð biðlara
* Skrá inn innskráningarupplýsingar fyrir úthlutaðan notanda 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") **táknið skal setja upp VSK-Flokkustjórnun** og velja síðan tengdan tengil.
2. **Tilgreinið í hlutverkaleik** VSK-flokks hvort þú sért fulltrúi flokksins eða fulltrúa flokksins. Velja **skal aðila** til að vinna með flokksmeðlimi og senda VSK-skil til flokksfulltrúa frekar en skattyfirvalda og velja **svo Next**.
3. Afritið gildið í reitnum **Kenni hópmeðlims** og deilið því síðan með fulltrúa VSK-hópsins svo hann geti bætt fyrirtækinu við sem samþykktum meðlimi hópsins.
4. **Í reitnum Útgáfufulltrúi** afurðastöðva er tilgreind sú útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] sem fulltrúinn notar.
5. **Í reitinn Flokksfulltrúi fyrirtækis** er fært inn FYRIRTÆKJAHEITI VSK-flokksfulltrúa. Til dæmis **CRONUS Bretland ehf**.
6. **Í reitnum Tegund** auðkenningar er valið **OAuth2**. Ef VSK-flokksfulltrúi er notaður [!INCLUDE[prod_short](includes/prod_short.md)] á netinu skal tilgreina að **Flokksfulltrúi noti Aðalnúmer á netinu** og velji **síðan Next**. Eftir því hvort fulltrúi er með notkun [!INCLUDE[prod_short](includes/prod_short.md)] á netinu eða innanhúss skal fara eftir þeim skrefum sem annaðhvort [nota VSK-flokkurinn notar viðskipti miðlægt á netinu](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eða [VSK-Flokkafulltrúi notar Viðskiptamiðlar í forpressun](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis) hluta.

### <a name="vat-group-representative-uses-business-central-online"></a>VSK-Flokkafulltrúi notar Business miðlægt í netinu
1. Færa skal inn notendaskilríkið sem VSK-flokksfulltrúi veitir og bæta við tilskilin leyfi.
2. Veljið skilgreiningu VSK-skýrslunnar sem er notuð til að senda VSK-skil til skattyfirvalda. Eftir að uppsetningunni lýkur þarf [!INCLUDE[prod_short](includes/prod_short.md)] að stofna nýja skilgreiningu byggða á þessu vali og nota skilgreininguna til að senda VSK-fulltrúa aftur á VSK-flokk.  
3. Bætið við **API-vefslóð** frá fulltrúa VSK-hópsins. Yfirleitt er vefslóðin á eftirfarandi sniði: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Til dæmis, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>VSK-Flokkafulltrúi notar Business miðlæg í Premesis
1. **TILGREINIÐ kenni biðlara frá App-skráningunni í REITNUM kenni** biðlara Azure Active Directory.
2. **Í reitnum leyninúmer** biðlara skal tilgreina leynireitinn viðskiptavinur úr App skráningu í Azure Active Directory.
3. **Í reitinn oAuth 2,0 Authority endastöð** er fært inn `https://login.microsoftonline.com/common/oauth2`.
4. **Í reitinn eijörð 2,0. URL** er fært inn `https://api.businesscentral.dynamics.com/`.
5. **Í svæðinu eiauth 2,0** er fært inn `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. Þegar búið er að tilgreina hina ýmsu reiti er **smellt á áfram** og síðan fært inn notendaskilríkið sem VSK-flokksfulltrúi hefur gefið.
7. Veljið skilgreiningu VSK-skýrslu sem er notuð til að skila inn VSK til yfirvalda í þínu landi.

## <a name="set-up-the-vat-group-representative"></a>Setja upp VSK-Flokkafulltrúa
> [!NOTE]
> Fyrir um-premesis, styðjumst við aðeins eitt leigjendótað tilvik af flokksfulltrúunum.

> [!IMPORTANT]
> Fulltrúafélagið verður að gera uppsetningu á **HMRC VSK-tengingu virka á** síðunni þjónustutengingar **.** Fulltrúar verða einnig að sækja VSK-skilatímabil frá HMRC.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") **táknið skal setja upp VSK-Flokkustjórnun** og velja síðan tengdan tengil.
2. **Tilgreinið í hlutverkaleik** VSK-flokks hvort þú sért fulltrúi flokksins eða fulltrúa flokksins. Veldu **fulltrúa** til að vinna sem fulltrúi VSK og senda VSK til skattyfirvalda fyrir flokkinn og velja **svo Next**.
3. **Í reitnum VSK-Uppgjörsreikningur** skal tilgreina lykilinn sem notaður er fyrir VSK-uppgjör.
4. Í reitnum **VSK-skuld nr.** Er reiturinn tilgreindur sem táknar heildarupphæð VSK sem stafar frá sendingu VSK-flokks.
5. **Í reitnum sniðmát** flokksjöfnuðasafns er tilgreint færslubókarsniðmát sem notað er fyrir skjalið til að bóka flokkinn VSK á jöfnunarlykilinn.
6. **Reiturinn samþykkt meðlima** sýnir fjölda flokksmanna sem eru settir upp til að senda VSK-skilagreinar til fulltrúa. Til að bæta nýjum meðlimum við er númerið valið til að opna **síðuna samþykkt meðlima**.
7. Til að bæta nýjum meðlimum við, Bætið eftirfarandi upplýsingum við á **síðunni samþykktir VSK-flokks félaga**:
    1. **Í reitinn FLOKKSAUÐKENNI** flokksins er fært inn kenni fyrir meðlimi hópsins.
    2. **Í reitnum Heiti** flokksins er tilgreint heiti á meðlimi flokksins. 
    3. **Í svæðinu fyrirtæki** skal tilgreina fyrirtækið sem hópur MEÐLIM sendir VSK inn á [!INCLUDE[prod_short](includes/prod_short.md)]. Til dæmis **CRONUS Bretland ehf**.
    4. Tilgreinið tengiliðaupplýsingar fyrirtækisins.

## <a name="use-the-vat-group-management-features"></a>Nota Stjórnunaraðgerðirnar VSK-Hópstjórnun
Meðlimir VSK-hóps nota hefðbundin ferli til að ganga frá VSK-skýrslum. Eini munurinn liggur í að velja skýrsluútgáfuna **VATGROUP**, sem sendir VSK-skýrsluna til fulltrúa VSK-hópsins frekar en yfirvalda. Nánari upplýsingar er að finna [um VSK-skilaskýrslu](finance-how-report-vat.md#vatreturn).

Í eftirfarandi köflum er lýst verkefnum sem VSK-flokksfulltrúar verða að gera.

### <a name="vat-group-submissions"></a>Innsendingar VSK-hóps

Síðan **Innsendingar VSK-hóps** birtir VSK-skýrslurnar sem meðlimir hafa sent inn. Síðan virkar sem staðsetning þar sem drög að innsendingum þar til fulltrúi VSK-hópsins tekur þær með í VSK-skýrslu fyrir hópinn. Hægt er að opna innsendingarnar til að yfirfara VSK fyrir staka reiti sem meðlimur VSK-hópsins hefur tilkynnt um. 

> [!TIP]
> **Á síðunni VSK-Skilatímabil** sýnir reiturinn flokksmeðliðaflokkur **um** hversu mörg skil aðilar hafa sent. Til að tryggja að þessi tala sé up-til-dagsetning er valið **aðgerðin Sækja VSK-skil**.

### <a name="creating-a-group-vat-return"></a>Skýrsla VSK-hóps stofnuð

Til að tilkynna VSK fyrir flokkinn, á **síðunni skil** á VSK-skilum, STOFNAST aðeins VSK fyrir fyrirtækið. Eftir á skal bæta við nýjustu innsendingum á VSK frá meðlimum VSK-hópsins með því að velja aðgerðina **Hafa með VSK-hóp**.  

Þegar VSK-fulltrúi fyrir VSK-flokk hefur verið sendur til yfirvalda fyrir allan hópinn er venjulega keyrð **aðgerðin Reikna og bóka VSK-uppgjör**. Þessi aðgerð lokar opnum VSK-færslum og millifærir upphæðir á reikning VSK-uppgjörs. Sem stendur tekur þessi aðgerð ekki tillit til hópuppgjafar. <!--Has this changed?--> Aðeins VSK-færslur fulltrúa fyrirtækis í VSK-flokki verða bókaðar. Fyrirframsettar upphæðir VSK-flokks meðlima verður að bóka á upphæð VSK-uppgjörs þannig að VSK-jöfnunarreikningur fulltrúa VSK-flokksins endurspegli ábyrgð þess sem tilkynnti til yfirvalda. Þessi hegðun mun breytast í komandi uppfærslu [!INCLUDE[prod_short](includes/prod_short.md)] og þannig verður allur HÓPURINN VSK (heildarupphæð í skýrslulínum á VSK skilin) jöfnuð. <!--Has this behavior changed?-->

> [!NOTE]
> Meðlimir VSK-hóps geta leiðrétt innsendar VSK-skýrslur svo lengi sem fulltrúi hópsins hafi ekki sent frá sér VSK-skýrsluna fyrir hópinn. Til að gera leiðréttingu verður meðlimur VSK-hópsins að búa til VSK-skýrslu fyrir tímabil VSK-skýrslunnar og senda hana til fulltrúa VSK-hópsins. Hjá fulltrúa VSK-hópsins verður nýjasta VSK-skýrslan höfð með á síðunni **VSK-skýrslur**. 

> [!IMPORTANT]
> VSK-flokksvirkni er aðeins studd á þeim mörkuðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] notar VSK-rammi sem inniheldur VSK-skil og VSK-skilatímabil. Ekki er hægt að nota VSK-flokka á öðrum mörkuðum sem eru með aðrar útfærslur af staðbundnum VSK-skýrslum, t.d. Austurríki, Þýskaland, Ítalía, Spánn og Sviss. 

## <a name="see-also"></a>Sjá einnig
[Bretland staðbundin virkni í bresku útgáfunni](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Tax Digital í Bretlandi](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
