---
title: Viðbót fyrir stjórnun VSK-hóps
description: Hægt er að tengjast við önnur fyrirtæki til að mynda VSK-hóp og vera annaðhvort meðlimur eða fulltrúa þess hóps þegar VSK er gefið upp.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 7148fa8e59a509af3206e7da898a371ffb5332a5
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029141"
---
# <a name="the-vat-group-management-extension"></a>Viðbót fyrir stjórnun VSK-hóps

Hægt er að tengja saman eitt eða fleiri fyrirtæki í landinu til að sameina VSK-skýrslugerð undir einu skráningarnúmeri. Þessi tilhögun er kölluð *VSK-hópur*. Hægt er að taka þátt í hópnum sem meðlimur eða fulltrúi hópsins.

## <a name="forming-a-vat-group"></a>Mynda VSK-flokk
Meðlimir VSK-hóps og fulltrúi hans geta notað uppsetningarleiðbeininguna **Uppsetning á stjórnun VSK-hóps** með hjálp til að skilgreina aðkomu þeirra að hópnum og búa til tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda þeirra. Meðlimir hópsins nota tenginguna til að senda VSK-skýrslur sínar til fulltrúa hópsins. Fulltrúinn mun senda VSK til skattayfirvalda fyrir hönd hópsins með einni VSK-skýrslu. 

## <a name="vat-group-constellations"></a>Samskipti innan VSK-hóps
Meðlimir hópsins eiga samskipti við fulltrúa hans. Fulltrúi hópsins gefur upp API sem gerir meðlimum kleift að senda VSK-skýrslur þeirra til fulltrúa VSK-hópsins. 
[!INCLUDE[prod_short](includes/prod_short.md)] styður sendingar á VSK innan hóps fyrir fyrirtæki með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum eða netinu, saman eða annað hvort. Uppsetning samskiptanna fer eftir samskiptanetinu. Eftirfarandi hlutar útskýra hvernig á að setja upp hin og þessi samskiptanet innan hópsins.

Eftirfarandi listi sýnir ráðlagða röð skrefa til að setja upp VSK-hóp:

1. Búa til uppsetninguna í Azure Active Directory. Frekari upplýsingar er að finna í [Kröfur vegna sannvottunar](ui-extensions-vat-group.md#requirements-for-authentication).
2. Deilið tæknilegum upplýsingum sem meðlimir og fulltrúi VSK-hópsins þurfa á að halda til að tengjast [!INCLUDE[prod_short](includes/prod_short.md)]-leigjandanum sínum. Yfirleitt býr fulltrúi VSK-hópsins yfir þessum upplýsingum, t.d. heiti á umhverfinu sem fulltrúi VSK-hópsins notar til að taka á móti VSK frá meðlimum VSK-hópsins.
3. Búið til notendur í VSK-hóp [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans sem meðlimir hópsins geta notað til að auðkennt og tengt sig.
4. Keyrið uppsetningarleiðbeininguna **Setja upp umsjón VSK-hópa** með hjálp til að tengja meðlimi VSK-hópsins.

  Leiðarvísirinn krefst nokkurra upplýsinga frá fulltrúa VSK-hópsins. Frekari upplýsingar er að finna í hlutanum [Uppsetning á meðlimi VSK-hóps](#vat-group-member-setup). Skrifið hjá ykkur **Kenni hópmeðlims** fyrir hvern meðlim VSK-hópsins. Fulltrúinn þarf þessi auðkenni til að bæta fyrirtækjunum við VSK-hópinn.
5. Setjið upp viðbótina fyrir umsjón VSK-hóps í VSK-hóp [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans með því að nota uppsetningarleiðbeininguna **Setja upp umsjón VSK-hópa** með hjálp. 

> [!NOTE]
> Til að tengjast fulltrúa VSK-hóps þurfa meðlimir notanda sem er með aðgang að VSK-hópnum í [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans. Fulltrúi VSK-hópsins verður að búa til að minnsta kosti einn notanda fyrir þetta, en af öryggisástæðum mælum við með því að notandi verði búinn til fyrir hvern meðlim VSK-hópsins. Gangið úr skugga um að dreifa innskráningarupplýsingunum til þessara meðlima VSK-hópsins á öruggan hátt.

## <a name="understanding-the-vat-group-management-setup"></a>Að skilja uppsetningu á umsjón VSK-hóps

Fulltrúi VSK-hópsins gefur upp API sem meðlimir hópsins geta notað til að tengjast við [!INCLUDE[prod_short](includes/prod_short.md)]-leigjandann sinn og senda VSK-skýrslur. Meðlimir VSK-hóps nota oft [!INCLUDE[prod_short](includes/prod_short.md)] í aðskildum Azure Active Directory-leigjendum. Þess vegna þarf fleiri uppsetningar til að koma á tengingu milli meðlima VSK-hópsins og [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans. 
  
Meðlimir VSK-hóps tengjast fulltrúanum með því að hafa samband við vefþjónustu í VSK-hópnum í leigjanda fulltrúans. Sá sem hefur samband verður að vera sannvottaður með OAuth. Þegar viðbótin fyrir umsjón VSK-hóps hefur verið sett upp, verður beðið um að auðkenna fulltrúa VSK-hópsins til að fá og vista aðgangslykil. Aðgangslykillinn er notaður VSK-skýrslum er skilað inn í VSK-hóp fulltrúans. 

Sannvottun er gerð af Azure Active Directory, þannig að uppsetningin verður að eiga sér stað í VSK-hópnum í Azure Active Directory fulltrúans til að leyfa tengingar. Skilgreina þarf skráningu Azure Active Directory-forrits með aðgang VSK-hópnum í [!INCLUDE[prod_short](includes/prod_short.md)] fulltrúans. Þetta gildir einnig ef fulltrúi VSK-hópsins notar [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum. Þar að auki verður að skilgreina staka innskráningu ef fulltrúi VSK-hópsins er að nota [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum.

> [!NOTE]
> Í takmarkaðan tíma verður sannvottun með aðgangslykli vefþjónustu einnig studd. Frekari upplýsingar er að finna í [Úreltir eiginleikar í 2021 útgáfutímabili 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Kröfur vegna sannvottunar 
Þegar fulltrúi VSK-hópsins notar [!INCLUDE[prod_short](includes/prod_short.md)] á netinu eða á staðnum, nota meðlimir VSK-hópsins Azure Active Directory til að sannvotta sig þegar þeir senda VSK-skýrslur til fulltrúa hópsins. Ef meðlimir VSK-hópsins eru einnig að nota [!INCLUDE[prod_short](includes/prod_short.md)] á netinu, getur meðlimur hópsins sannvottað sig með því að nota úthlutaðar innskráningarupplýsingar og upplýsingar um endastöð. Frekari upplýsingar er að finna í [Uppsetning á meðlimi VSK-hóps](ui-extensions-vat-group.md#vat-group-member-setup).

Meðlimir VSK-hóps sem eru með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum verða að setja upp skráningu forrits í Azure Active Directory fyrir VSK-hópinn í [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda fulltrúans. Skráning forritsins gerir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu fyrir fulltrúa VSK-hópsins kleift að sannvotta meðlim hópsins. Frekari upplýsingar er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app).

Þegar skráning forrtisins er búin til í Azure Active Directory, þarf að tilgreina eftirfarandi.

* Í hlutanum **Sannvottun** skal bæta við **Vef** sem verkvang og nota eftirfarandi **Framsendingarvefslóð**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Í hlutanum **Sannvottun**, í valkostinum fyrir **Studdar reikningsgerðir**, skal velja **Reikningar í hvaða notendaskrá fyrirtækis sem er (Hvaða Azure AD notendaskrá sem er - Margir leigjendur)**.
* Í hlutanum **Vottorð og leynilyklar** skal búa til nýjan leynilykil biðlara og skrá niður gildið. Meðlimir VSK-hópsins þurfa á leynilyklinum að halda þegar þeir setja upp tenginguna við fulltrúa hópsins.
* Í hlutanum **API-heimildir** skal bæta heimildum við [!INCLUDE[prod_short](includes/prod_short.md)]. Virkja úthlutun aðgangs fyrir **Financials.ReadWrite.All** og **user_impersonation**.
* Í hlutanum **Yfirlit** skal skrá hjá sér **Kenni forrits (biðlara)**. Meðlimir VSK-hópsins þurfa á auðkenninu að halda þegar þeir setja upp tenginguna við fulltrúa hópsins. 

## <a name="vat-group-member-setup"></a>Uppsetning á meðlimi VSK-hóps
Setjið upp meðlim VSK-hópsins með því að hefja uppsetningarleiðbeininguna **Setja upp umsjón VSK-hópa** með hjálp. 

> [!NOTE]
> Áður en hafist er handa skal hafa samband við fulltrúa VSK-hópsins vegna eftirfarandi upplýsinga um [!INCLUDE[prod_short](includes/prod_short.md)]-leigjandann hans:
>
> * API-vefslóðin
> * Heiti fyrirtækisins 
> * Biðlarakenni
> * Leyniorð biðlara
> * Skrá inn innskráningarupplýsingar fyrir úthlutaðan notanda 

1. Til að skilgreina hlutverk VSK-hóps fyrirtækisins skal velja **Meðlim** og síðan **Áfram**.
2. Afritið gildið í reitnum **Kenni hópmeðlims** og deilið því síðan með fulltrúa VSK-hópsins svo hann geti bætt fyrirtækinu við sem samþykktum meðlimi hópsins.
3. Bætið við **API-vefslóð** frá fulltrúa VSK-hópsins. Yfirleitt er vefslóðin á eftirfarandi sniði: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Til dæmis, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
4. Bætið við [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtækisheiti fyrir fulltrúa VSK-hópsins, t.d. *CRONUS UK Ltd.*.
5. Veljið **Gerð sannvottunar**, veljið **OAuth2** og síðan **Áfram**.
6. Í reitinn **Biðlarakenni** skal færa inn auðkennið sem fulltrúi VSK-hópsins bjó til.
7. Í reitinn **Leynilykill biðlara sem fulltrúi VSK-hópsins bjó til** skal færa inn leynilykilinn sem fulltrúi VSK-hópsins bjó til.
8. Í reitinn **OAuth 2.0 endastöð eftirlits** skal færa inn *https://login.microsoftonline.com/common/oauth2*.
9. Í reitinn **OAuth 2.0 vefslóð tilfangs** skal færa inn *https://api.businesscentral.dynamics.com/*.
10. Í reitinn **OAuth 2.0 framsendingarvefslóð** skal færa inn *https://businesscentral.dynamics.com/OAuthLanding.htm*. 
11. Þegar búið er að tilgreina ýmsa reiti skal velja **Áfram** og síðan færa inn innskráningarupplýsingar notanda sem fulltrúi VSK-hópsins bjó til.
12. Veljið skilgreiningu VSK-skýrslu sem er notuð til að skila inn VSK til yfirvalda í þínu landi.

  Í Bretlandi yrði skilgreining VSK-skýrslu stillt á að skila VSK til HMRC. Viðbótin fyrir umsjón VSK-hóps afritar þessa uppsetningu, en skiptir út kóðaeiningu innsendingar fyrir aðra sem styður innsendingu til fulltrúa VSK-hópsins frekar en skattayfirvalda. Kóðaeiningin kemur frá Microsoft. Þegar þessu eru lokið skal velja **Áfram**.

## <a name="using-the-vat-group-management-features"></a>Að nota eiginleikann fyrir umsjón VSK-hóps

Meðlimir VSK-hóps nota hefðbundin ferli til að ganga frá VSK-skýrslum. Eini munurinn liggur í að velja skýrsluútgáfuna **VATGROUP**, sem sendir VSK-skýrsluna til fulltrúa VSK-hópsins frekar en yfirvalda. Nánari upplýsingar er að finna í [Um skil á VSK-skýrslu](finance-how-report-vat.md#about-the-vat-return-report).

Í eftirfarandi hlutum er lýst verkunum sem fulltrúar VSK-hóps verða að gera.

### <a name="vat-group-submissions"></a>Innsendingar VSK-hóps

Síðan **Innsendingar VSK-hóps** birtir VSK-skýrslurnar sem meðlimir hafa sent inn. Síðan virkar sem staðsetning þar sem drög að innsendingum þar til fulltrúi VSK-hópsins tekur þær með í VSK-skýrslu fyrir hópinn. Hægt er að opna innsendingarnar til að yfirfara VSK fyrir staka reiti sem meðlimur VSK-hópsins hefur tilkynnt um.

### <a name="creating-a-group-vat-return"></a>Skýrsla VSK-hóps stofnuð

Til að gefa upp VSK fyrir hönd hópsins skal á síðunni **VSK-skýrslur** stofna VSK-skýrslu fyrir eingöngu þitt fyrirtæki. Eftir á skal bæta við nýjustu innsendingum á VSK frá meðlimum VSK-hópsins með því að velja aðgerðina **Hafa með VSK-hóp**.  

Þegar VSK-skýrsla fulltrúa VSK-hópsins hefur verið send til yfirvalda fyrir hönd alls hópsins er aðgerðin **Reikna og bóka VSK-uppgjör** yfirleitt keyrð. Þessi aðgerð lokar opnum VSK-færslum og millifærir upphæðir á reikning VSK-uppgjörs. Sem stendur tekur þessi aðgerð ekki innsendingar hópsins með í reikninginn. Þetta þýðir að aðeins VSK-færslur frá fulltrúa fyrirtækis VSK-hópsins verða bókaðar. Upphæðir innsendinga frá meðlimum VSK-hópsins verða að vera bókaðar á VSK-uppgjörið handvirkt þannig að VSK-uppgjörsreikningur hjá fulltrúa VSK-hópsins endurspegli skuldina sem tilkynnt var til yfirvalda. Þessi hegðun mun breytast í væntanlegri uppfærslu á [!INCLUDE[prod_short](includes/prod_short.md)], þannig að allur VSK-hópurinn (heildarupphæð í skýrslulínum í VSK-skýrslunni) verður gerður upp. 

> [!NOTE]
> Meðlimir VSK-hóps geta leiðrétt innsendar VSK-skýrslur svo lengi sem fulltrúi hópsins hafi ekki sent frá sér VSK-skýrsluna fyrir hópinn. Til að gera leiðréttingu verður meðlimur VSK-hópsins að búa til VSK-skýrslu fyrir tímabil VSK-skýrslunnar og senda hana til fulltrúa VSK-hópsins. Hjá fulltrúa VSK-hópsins verður nýjasta VSK-skýrslan höfð með á síðunni **VSK-skýrslur**. 

> [!IMPORTANT]
> VSK-flokksvirkni er aðeins studd á þeim mörkuðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] notar VSK-rammi sem inniheldur VSK-skil og VSK-skilatímabil. Ekki er hægt að nota VSK-flokka á öðrum mörkuðum sem eru með aðrar útfærslur af staðbundnum VSK-skýrslum, t.d. Austurríki, Þýskaland, Ítalía, Spánn og Sviss. 

## <a name="see-also"></a>Sjá einnig

[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Tax Digital í Bretlandi](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Norsk VSK-skýrsla í norsku útgáfunni](LocalFunctionality/Norway/norwegian-vat-reporting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
