---
title: Samstilla viðskiptavini
description: Flytja inn viðskiptavini úr eða út í Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: d4ff86179fa5b82bcc398ee58cf92fc121c486d8
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361422"
---
# <a name="synchronize-customers"></a>Samstilla viðskiptavini

Þegar pöntun er flutt inn frá Shopify, er nauðsynlegt að fá upplýsingar um viðskiptamanninn og frekari vinnslu skjalsins í [!INCLUDE[prod_short](../includes/prod_short.md)]. Þetta eru tveir helstu Kostirnir fyrir að gera svo, og samsetningar þeirra:

* Notið sérstakan viðskiptavin fyrir allar pantanir.
* Flytja inn raunverulegar upplýsingar um viðskiptavin úr Shopify. Þessi valkostur er einnig tiltækur þegar Viðskiptavinir eru flutt í Shopify[!INCLUDE[prod_short](../includes/prod_short.md)] fyrsta sinn.

## <a name="how-the-connector-chooses-which-customer-to-use"></a>Hvernig Tenglarnir velja hvaða viðskiptavin á að nota

*Innflutningspöntunin úr Shopify* aðgerðinni reynir að velja viðskiptamenn í eftirfarandi röð:

1. **Ef sjálfgefinn viðskm. nr.** Er skilgreindur í **Shopify Viðskiptamannssniðmátinu** fyrir samsvarandi land er síðan **sjálfgefna Viðskiptavinasvæðið nr.** Er notað án tillits til stillinga í **reitum innflutnings Shopify** -og **Viðskiptavinavörpunargerðar**. Frekari upplýsingar um [sniðmát viðskiptavinar fyrir hvert land](synchronize-customers.md#customer-template-per-country).
2. **Ef innflutningur Shopify** viðskiptavinar er stilltur á *ekkert* og **sjálfgefna viðskiptavinarnr.** Er skilgreindur á **Shopify Vinnukortasíðunni**, þá **er sjálfgefinn viðskm. nr.** Er notað.

Næstu skref fara **eftir gerð** Viðskiptavinakortsvörunar.

* Ef það er **alltaf tekið sjálfgefinn viðskiptavin**, þá notar tengivirkið viðskiptavininn sem skilgreindur er í **sjálfgefnum viðskm.** Reitnum á **Shopify Vinnukortasíðunni**.
* Ef hún er **með tölvupósti/síma** þá reynir tengin að finna núverandi VIÐSKIPTAVIN með auðkenni fyrst, þá með tölvupósti, og svo eftir símanúmeri. Ef viðskiptavinurinn finnst ekki stofnar Connector nýjan viðskiptavin.
* Ef upplýsingar **eru** eftir uppskriftinni reynir Tengillinn að finna viðskiptavininn sem er fyrstur með kennið fyrst og síðan með upplýsingum um aðsetur í frumgögnum. Ef viðskiptavinurinn finnst ekki stofnar Connector nýjan viðskiptavin.

> [!NOTE]  
> Í tengivirkinu eru notaðar upplýsingar úr reitnum aðsetur og stofnar viðskiptamannsins [!INCLUDE[prod_short](../includes/prod_short.md)] sem er Reikn. Selt-til-viðskiptamaður er sá sami og Reikn.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Mikilvægar stillingar við innflutning viðskiptavina frá Shopify

Hvort sem þú fluttir inn viðskiptavini frá Shopify í magni eða á sama tíma og þú pantar inn eftirfarandi stillingar, þá gerum við það sem þú hefur umsjón með ferlinu:

|Svæði|Lýsing|
|------|-----------|
|**Innflutningur viðskiptavina frá Shopify**|Veljið **alla viðskiptamenn** ef þú ætlar að flytja inn viðskiptavini úr Shopify í magni; heldur handvirkt í **aðgerðinni samstilling viðskiptamanna** eða vinnslubiðröð með endurteknum uppfærslum. Án tillits til vals verða upplýsingar um viðskiptavin alltaf fluttar inn ásamt pöntuninni. Hins vegar fer notkun þessara upplýsinga eftir **Shopify sniðmátum** og stillingum viðskiptavinar í **reitnum Tegund** kortlagningar viðskiptamanns.|
|**Gerð Kortvörpun viðskiptavinar**|Skilgreinið hvernig tengja á Connector við vörpunaraðgerðina.<br>- **Með tölvupósti/Phone** ef óskað er eftir að Connector kortberi innflutta Shopify viðskiptavininn við viðskiptavin í [!INCLUDE[prod_short](../includes/prod_short.md)] notkun með tölvupósti og síma.</br>- **Með því að reikningsfæra upplýsingar** ef óskað er eftir að Connector noti aðsetur viðtakanda reiknings sem Shopify viðskiptavinurinn er viðskiptavinur í [!INCLUDE[prod_short](../includes/prod_short.md)].</br>-Veljið **alltaf sjálfgefinn viðskiptavin** ef kerfið á að nota viðskiptavin úr reitnum **Sjálfgefið viðskm.** . |
|**Shopify Hægt að uppfæra viðskiptavini**| Veljið þetta svæði ef óskað er eftir að Connector uppfæri viðskiptavinina sem finna þegar **valkosti með tölvupósti/síma** eða **eftir valkostum** frá frumvarpi til **upplýsingakvikju**.|
|**Sjálfvirk stofnun óþekktra viðskiptamanna**| Veljið þetta svæði ef óskað er eftir að Connector vanti viðskiptamenn þegar **Valkostir með tölvupósti/síma** eða **eftir uppskrift** eru valdir í **reitnum Tegund** kortlagningar í viðskiptavinarvörpun. Nýr viðskiptamaður verður stofnaður með innfluttu gögnunum og Sniðmátskóta viðskiptamanns sem **tilgreindur er á** síðum vinnukorta **Shopify eða** sniðmáts **Shopify** viðskiptamanns. Takið eftir að Shopify viðskiptavinurinn þarf að hafa minnst eitt aðsetur. Ef þessi valkostur er ekki virkjaður þarf að stofna viðskiptavin handvirkt og tengja hann við Shopify viðskiptamanninn. Þú getur alltaf haft frumkvæði að stofnun viðskiptavinar handvirkt á **Shopify pöntunarsíðunni**.|
|**Sniðmátskóti viðskiptamanns**|Þessi reitur er notaður með **sjálfvirkum stofna óþekktra viðskiptamanna**.<br>-Velja sjálfgefið sniðmát sem á að nota fyrir sjálfvirka stofna viðskiptavini. Ganga þarf úr skugga um að valið sniðmát innihaldi Skyldusvæðin eins og **Alm. viðsk.** Bókunarflokkur, **Bókunarflokkur** viðskm., og virðisauka-eða skatttengd svæði.<br>-Hægt er að skilgreina sniðmát fyrir hvert land/svæði á **Shopify síðunni sniðmát** viðskiptamanns sem er gagnlegt fyrir réttan skattaútreikning. <br>-Læra meira at [Setja upp skatta](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Sniðmát viðskiptavinar fyrir hvert land

Sumar stillingar er hægt að skilgreina á lands-/svæðisstigi eða á ríki/héraðþrepi. Hægt er að skilgreina stillingarnar í [sendingu og afhendingar](https://www.shopify.com/admin/settings/shipping) kl Shopify.

Hægt er að gera eftirfarandi fyrir hvern viðskiptavin með því að **Shopify nota sniðmát** viðskiptamanns:

1. **Tilgreinið sjálfgefið viðskm. nr.**, sem tekur forgang yfir valið í **reitum innflutnings Shopify** -og **Viðskiptavinavörpunargerðar**. Það er notað í innfluttu sölupöntuninni.
2. Skilgreinið **Sniðmátskóða viðskiptamanns sem er notaður til að stofna viðskiptavini sem vantar ef** Óþekkt viðskiptamódel **er** virkt. **Ef Sniðmátskóti** viðskiptamanns er auður notar **aðgerðin sniðmátskóta** viðskiptamanns sem tilgreindur er á **Shopify verkstæðisspjaldinu**.
3. Tilgreinið hvort verð feli í sér VSK/skatt fyrir innfluttar pantanir.
4. Í sumum tilfellum er **Sniðmátskóti** viðskiptamanns sem skilgreindur er fyrir land ekki nóg til að tryggja réttan útreikning skatta (til dæmis fyrir lönd með VSK). Í þessu tilviki gæti m.a. **skattsvæði** verið gagnleg viðbót.

> [!NOTE]  
> Landskótarnir ISO 3166-1 Alpha-2 landskótum. Frekari upplýsingar á [Landnúmeri](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Útflutningur viðskiptavina á Shopify

Núverandi viðskiptavini er hægt að Shopify Flytja út í í fjöldasöng. Í hverju tilviki stofnast viðskiptavinur og eitt sjálfgefið aðsetur. Hægt er að stjórna ferlinu með eftirfarandi stillingum:

|Svæði|Lýsing|
|------|-----------|
|**Útflutningur viðskiptavina á Shopify**|Veljið þetta ef ætlunin er að flytja út alla viðskiptamenn með gilt netfang úr [!INCLUDE[prod_short](../includes/prod_short.md)]Shopify í magnskrá. Hægt er að gera það handvirkt með **aðgerðinni samstilla viðskiptamenn** eða nota vinnsluröð til að fá endurteknar uppfærslur.<br> Við útflutning viðskiptavina með aðsetur sem innihalda héruð/ríki skal ganga úr skugga um að **ISO-Kóði** sé fylltur út fyrir lönd/svæði.|
|**Hægt að uppfæra Shopify viðskiptavini**|Þetta er notað ásamt **útflutningsviðskiptamanninum til að Shopify** Stilla. Gera það virkt ef mynda á uppfærslur síðar frá [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir viðskiptamenn sem eru þegar til í Shopify.|

> [!NOTE]  
> Þegar þú hefur stofnað viðskiptavinina í Shopify er hægt að senda þeim beint boð hvetja þá til að virkja reikninga þeirra.

### <a name="populate-customer-information-in-shopify"></a>Fylla út upplýsingar um viðskiptavin í Shopify

Viðskiptavinur í Shopify hefur fornafn, eftirnafn, netfang og/eða símanúmer. Hægt er að fylla út fyrstu og síðustu nöfnin af viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Svæði í viðskiptamannaspjaldi|Lýsing|
|------|------|-----------|
|1|**Nafn tengiliðar**|Hæsta Forgangur ef **reiturinn Heiti** tengiliðar er fylltur út og **upprunakort** tengiliðar á **Shopify verkstæðisspjaldinu** inniheldur annað hvort *fyrsta nafn og eftirnafn* eða *eftirnafn og valkosturinn fyrra heiti* til að skilgreina hvernig eigi að skipta gildum.|
|2|**Nefndu 2**|**Ef reiturinn Heiti 2** er fylltur út og **reiturinn Heiti 2** í **Shopify verkstæðisspjaldinu** inniheldur annað hvort *fyrsta nafn og eftirnafn* eða *eftirnafn og nafn sem fyrsta heiti* til að skilgreina hvernig eigi að skipta gildum.|
|3|**Heiti**|Lægsta forgang ef **reiturinn Heiti** er fylltur út og **reiturinn Heiti Uppruni** í **Shopify verkstæðisspjaldinu** inniheldur annað hvort *fyrsta nafn og eftirnafn* eða *eftirnafn og Valkostir skírnarnafns* til að skilgreina hvernig skipta á gildum.|

Viðskiptavinur í Shopify er einnig með sjálfgefið heimilisfang sem getur innihaldið fyrirtæki og heimilisfang auk fornafns þess, eftirnafns, tölvupósts og/eða síma. Hægt er að fylla út í **svæðið fyrirtæki** Byggt á gögnum af viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Svæði í viðskiptamannaspjaldi|Lýsing|
|------|------|-----------|
|1|**Heiti**|Hæsta Forgangur ef **reiturinn Heiti Uppruni** í **Shopify verkstæðisspjaldinu** inniheldur *Heiti* fyrirtækis.|
|2|**Nefndu 2**|Lægsta forgang ef **reiturinn 2 Upprunakort** á **Shopify verkstæðisspjaldinu** inniheldur *Heiti* fyrirtækis.|

Fyrir heimilisföng þar sem land/hérað er notað, veljið *þá kóða* eða *Heiti* í **upprunakrafta** **Shopify verkstæðiskortsins**. Þetta tilgreinir tegund gagna sem geymd eru í [!INCLUDE[prod_short](../includes/prod_short.md)] í landsvæðinu **.**

## <a name="sync-customers"></a>Viðskiptavinir samkaupa

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið síðan tengda tengilinn.
2. Valin er sú búð sem samstilla á viðskiptavini fyrir.
3. **Veljið aðgerðina samstilla viðskiptavin**.

Einnig er hægt að **nota samstillingaraðgerðina** **Shopify Ræsa viðskiptavin í glugganum Viðskiptavinir** eða leita að **keyrslunni samkeyrsluviðskiptamanna**.

Áætla má að verkefnið sé framkvæmt með sjálfvirkum hætti. Frekari upplýsingar um [tímasetningu endurtekinna verka](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
