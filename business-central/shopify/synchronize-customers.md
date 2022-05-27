---
title: Samstilla viðskiptavini
description: Flytja inn viðskiptavini úr eða út í Shopify
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 92ac46e9f7e69204b4c7edee4aa430a8786b6c0b
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768101"
---
# <a name="synchronize-customers"></a>Samstilla viðskiptavini

Þegar pöntun er flutt inn frá Shopify eru upplýsingar um viðskiptavin nauðsynlegar fyrir frekari vinnslu skjalsins í [!INCLUDE[prod_short](../includes/prod_short.md)]. Um tvo meginkosti er að ræða og samsetningar þeirra:

* Nota sérstakan viðskiptavin fyrir allar pantanir.
* Flytja raunverulegar upplýsingar um viðskiptavin úr Shopify. Þessi valkostur er einnig tiltækur þegar viðskiptamaður er útflutt í Shopify frá [!INCLUDE[prod_short](../includes/prod_short.md)] fyrst.

## <a name="how-connector-chooses-which-customer-to-use"></a>Hvernig tengistykki kýs hvaða viðskiptavin á að nota

*Innflutningspöntunin úr Shopify* aðgerð reynir að velja viðskiptavin í eftirfarandi röð:

1. **Ef sjálfgefinn viðskm. nr.** Er skilgreindur í **Shopify Viðskiptamannssniðmátinu** fyrir samsvarandi land, þá **er sjálfgefinn Viðskiptamaður nr.** Er notaður, óháð stillingum í **innflutningi viðskiptavinar úr Shopify** og **viðskiptavinarvörpun**.
2. Ef **Viðskiptamaður flytja úr Shopify** og **Sjálfgefinn viðskiptamanns.** Er tilgreindur er síðan **sjálfgefna Viðskiptavinarnr.** Er notað.

Næstu skref fara eftir **gerð** viðskiptavinarkortanna.

* **Alltaf skal nota sjálfgefinn viðskiptavin**, síðan er viðskiptamaðurinn skilgreindur í reitnum **Sjálfgefinn Viðskiptamaður nr.** Svæði í **Shopify glugganum Spjald** verslunar.
* **Með tölvupósti/síma**, reynir tengin að finna núverandi viðskiptavin með auðkenni fyrst, þá með tölvupósti, og svo í síma. Ef viðskiptavinurinn finnst ekki-Connector stofnar nýr viðskiptamaður.
* **Eftir uppskrift**, reynir tengivirkið að finna viðskiptavin sem til er eftir kenni fyrst og síðan með upplýsingum um aðsetur eftir uppskrift. Ef ekki fundið-þá stofnar Connector nýjan viðskiptavin.

> [!NOTE]  
> Tengillinn notar upplýsingar úr Bill-til address og stofnar viðskiptamann í [!INCLUDE[prod_short](../includes/prod_short.md)]. Selt-til-viðskiptamaður er jafnt og Reikn.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Mikilvægar stillingar við innflutning viðskiptavina frá Shopify

Annað hvort er hægt að flytja inn viðskiptavini Shopify í fjöldaeða ásamt innflutningi á pöntunum, eftirfarandi stillingar láta þig hafa umsjón með ferlinu:

|Svæði|Lýsing|
|------|-----------|
|**Innflutningur viðskiptavina frá Shopify**|Velja **alla viðskiptamenn** ef þú ætlar að flytja inn viðskiptavini úr Shopify í magni; annað hvort nota **handvirkt aðgerðina samstillingarviðskiptavinur** eða vinnslubiðröð með því að færa endurteknar uppfærslur. Án tillits til vals verða upplýsingar um viðskiptavin alltaf fluttar inn ásamt pöntun. Hins vegar fer notkun þessara upplýsinga eftir **Shopify sniðmátum** og stillingum viðskiptavinar í **reitnum Tegund** kortlagningar.|
|**Gerð Kortvörpun viðskiptavinar**|Skilgreinið hvernig tengja á Connector við vörpun.<br>- **Með tölvupósti/Phone** ef Connector er óskað að varpa innfluttu Shopify viðskiptavinunum á viðskiptavin sem til eru í [!INCLUDE[prod_short](../includes/prod_short.md)] tölvupósti og síma.</br>- **Hjá BillTo info** eigi Connector að varpa innfluttu Shopify viðskiptamanni á viðskiptavininn í [!INCLUDE[prod_short](../includes/prod_short.md)] því að nota aðsetursupplýsingar þess aðila sem tekur við reikningnum.</br>Veljið **alltaf taka sjálfgefinn viðskiptavin** ef kerfið á að nota viðskiptavin úr reitnum **Sjálfgefið viðskm.** . |
|**Shopify Hægt að uppfæra viðskiptavini**| Veljið ef óskað er eftir að Connector uppfæri viðskiptavini sem finnast þegar **eftir valkosti með tölvupósti/síma** eða **samkvæmt Frumupplýsingum** af frumvarpi í **reitinn Tegund** viðskiptavinarkortlagningar.|
|**Sjálfvirk stofnun óþekktra viðskiptamanna**| Veljið ef óskað er að Connector vanti til að stofna viðskiptavini, þegar **Valkostir með tölvupósti/síma** eða **með Billto-upplýsingum** eru valdir í **reitnum Tegund** kortvörpun viðskiptavinar. Nýr viðskiptamaður verður stofnaður með innfluttu gögnum og **Sniðmátskóta viðskiptamanns sem tilgreindur er á síðum vinnukorta** eða **Shopify sniðmáta** **Shopify fyrir** viðskiptavin. Takið eftir að Shopify viðskiptavinurinn þarf að hafa minnst eitt aðsetur. Ef þessi valkostur er ekki virkjaður þarf að stofna viðskiptavin handvirkt og tengja hann við Shopify viðskiptamanninn. Þú getur alltaf haft frumkvæði að stofnun viðskiptavinar handvirkt á **Shopify pöntunarsíðunni**.|
|**Sniðmátskóti viðskiptamanns**|Notað ásamt **sjálfvirkum stofna óþekktum viðskiptavina**.<br> Velja sjálfgefið sniðmát sem á að nota fyrir sjálfvirka stofna viðskiptavini. Hægt er að skilgreina sniðmát fyrir hvert land/svæði í **Shopify glugganum Sniðmát** viðskiptamanns sem er gagnlegt fyrir réttan skattaútreikning. Nánar er fjallað [um Skattaleg ummæli](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Sniðmát viðskiptavinar fyrir hvert land

Sumar stillingar er hægt að skilgreina á lands-/svæðisstigi eða á stöðu-/héraðsstigi. Hægt er að skilgreina stillingarnar í [sendingu og afhendingar](https://www.shopify.com/admin/settings/shipping) kl Shopify.

**Shopify Viðskiptamannssniðmátið** gerir notanda kleift að gera eftirfarandi við hvert land:

1. **Tilgreinið sjálfgefið viðskm. nr.**, sem tekur forgang yfir valið í **reitum innflutnings Shopify** -og **Viðskiptavinavörpunargerðar**. Það er notað í innfluttu sölupöntuninni.
2. Skilgreinið **Sniðmátskóða viðskiptamanns sem er notaður til að stofna viðskiptamenn sem vantar, ef** Óþekkt viðskiptamódel **er** virkt. Ef **Sniðmátskóti** viðskiptamanns er auður notar **aðgerðin sniðmátskóta** viðskiptamanns sem tilgreindur er á **Shopify verkstæðisspjaldinu**.
3. Í sumum tilfellum er **Sniðmátskóti** viðskiptamanns á landi ekki nægur til að tryggja réttan útreikning skatta. T.d. vegna löndaðrar með virðisaukaskatti.

> [!NOTE]  
> Landskótarnir ISO 3166-1 Alpha-2 landskótum. Sjá [Country Code](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode) fyrir nánari upplýsingar.

## <a name="export-customers-to-shopify"></a>Útflutningur viðskiptavina á Shopify

Núverandi viðskiptavini er hægt að Shopify Flytja út í í fjöldasöng. Þar af leiðandi stofnast viðskiptavinur og eitt sjálfgefið aðsetur. Hægt er að stjórna ferlinu með hjálp eftirfarandi stillinga:

|Svæði|Lýsing|
|------|-----------|
|**Útflutningur viðskiptavina á Shopify**|Veljið ef ætlunin er að flytja út alla viðskiptamenn með gilt tölvupóstfang úr [!INCLUDE[prod_short](../includes/prod_short.md)]Shopify í í magnskrá, annað hvort með handvirkt, **aðgerðin samstillingarviðskiptavinir** eða vinnslubiðröð í vinnsluröð fyrir endurteknar uppfærslur.|
|**Hægt að uppfæra Shopify viðskiptavini**|Notað ásamt **útflutningi viðskiptavinar til Shopify**. Gera hana virka ef mynda á uppfærslur síðar frá [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir viðskiptamenn sem eru þegar til í Shopify.|

> [!NOTE]  
> Þegar Viðskiptavinir Shopify hafa verið stofnaðir gæti verið gott að senda bein fundarboð til viðskiptavina. Það hvetur þá til að virkja reikninginn sinn.

### <a name="populate-customer-information-in-shopify"></a>Fylla út upplýsingar um viðskiptavin í Shopify

Viðskiptavinur í Shopify hefur fornafn, eftirnafn, netfang og/eða símanúmer. Hægt er að fylla út fyrsta nafn og eftirnafn, Byggt á gögnum af viðskiptamannaspjaldi í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Svæði í viðskiptamannaspjaldi|Lýsing|
|------|------|-----------|
|1|**Nafn tengiliðar**|Hæsta Forgangur ef **reiturinn Heiti** tengiliðar er fylltur út og **Reiturinn Tengiliður tengiliðar** í **Shopify verkstæðisspjaldinu** inniheldur *fyrsta heiti og eftirnafn* eða *eftirnafn og Valkostir fornafns* eru að skilgreina hvernig á að skipta gildum.|
|2|**Nefndu 2**|**Ef reiturinn Heiti 2** er fylltur út og **reiturinn Heiti 2** í **Shopify verkstæðisspjaldinu** eru *fyrstu heiti og eftirnafn* eða *eftirnafn og Valkostir skírnarnafns* eru skilgreindar hvernig á að skipta gildum.|
|3|**Heiti**|Lægsta forgang ef **reiturinn Heiti** er fylltur út og **reiturinn Heiti Uppruni** í **Shopify verkstæðisspjaldinu** inniheldur *fyrsta heiti og eftirnafn* eða *eftirnafn og Valkostir fornafns*, sem skilgreina hvernig á að skipta gildum.|

Viðskiptavinur í Shopify er einnig með sjálfgefið aðsetur þar sem fornafn, eftirnafn, Tölvupóstur og/eða Sími gætu innihaldið fyrirtæki og aðsetur. Hægt er að fylla út í **svæðið fyrirtæki** Byggt á gögnum af viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Svæði í viðskiptamannaspjaldi|Lýsing|
|------|------|-----------|
|1|**Heiti**|Hæsta Forgangur ef **reiturinn Heiti Uppruni** í **Shopify verkstæðisspjaldinu** inniheldur *Heiti* fyrirtækis.|
|2|**Nefndu 2**|Lægsta forgang ef **reiturinn 2 Upprunakort** á **Shopify verkstæðisspjaldinu** inniheldur *Heiti* fyrirtækis.|

Fyrir aðsetur þar sem notað er land/hérað er valið *kóti* eða *Heiti* í **reitnum** Upprunagátt á **Shopify verkstæðisspjaldinu** til að tilgreina hvaða tegund af gögnum er geymd í [!INCLUDE[prod_short](../includes/prod_short.md)] í **reitnum land**.

## <a name="sync-customers"></a>Viðskiptavinir samkaupa

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem á að samstilla viðskiptavini til að opna **Shopify spjald** -síðu verkstæðis.
3. **Veljið aðgerðina samstilla viðskiptavin**.

Einnig er hægt að **nota aðgerðina** Ræsa viðskiptavin samkeyrslu **Shopify í glugganum Viðskiptavinir** eða leita að **keyrslu samstillingarviðskiptamanna**.

## <a name="see-also"></a>Sjá einnig

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
