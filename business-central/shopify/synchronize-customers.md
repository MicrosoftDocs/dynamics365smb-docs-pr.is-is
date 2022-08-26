---
title: Samstilla viðskiptavini
description: Flytja inn viðskiptavini úr eða út í Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 0c1402c4f41f108b504ad31829ede5a1095b6ce4
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317327"
---
# <a name="synchronize-customers"></a>Samstilla viðskiptavini

Þegar pöntun er innflutt frá Shopify er nauðsynlegt að upplýsingar um viðskiptavininn séu frekari vinnslu skjalsins [!INCLUDE[prod_short](../includes/prod_short.md)]. Um tvo meginkosti er að ræða og samsetningar þeirra:

* Notið sérstakan viðskiptavin fyrir allar pantanir.
* Flytja inn raunverulegar upplýsingar um viðskiptavin úr Shopify. Þessi valkostur er einnig tiltækur þegar Viðskiptavinir eru flutt í Shopify[!INCLUDE[prod_short](../includes/prod_short.md)] fyrsta sinn.

## <a name="how-the-connector-chooses-which-customer-to-use"></a>Hvernig Tenglarnir velja hvaða viðskiptavin á að nota

*Innflutningspöntunin úr Shopify* aðgerðinni reynir að velja viðskiptavin í eftirfarandi röð:

1. **Ef sjálfgefinn viðskm. nr.** Er skilgreindur í **Shopify Viðskiptamannssniðmátinu** fyrir samsvarandi land er síðan **sjálfgefna Viðskiptavinasvæðið nr.** Er notað án tillits til stillinga í **reitum innflutnings Shopify** -og **Viðskiptavinavörpunargerðar**. Sjá [viðskiptamannasniðmát á landi](synchronize-customers.md#customer-template-per-country) fyrir frekari upplýsingar.
2. **Ef innflutningur Shopify** viðskiptavinar er stilltur á *ekkert* og **sjálfgefna viðskiptavinarnr.** Er skilgreindur í **Shopify verkstæðisspjaldinu** þá **er sjálfgefinn viðskm. nr.** Er notað.

Næstu skref fara **eftir gerð** Viðskiptavinakortsvörunar.

* **Alltaf skal taka sjálfgefinn viðskiptavin**, þá notar tengivirkið viðskiptavininn sem skilgreindur er í **sjálfgefnum viðskm.** Svæðinu á **Shopify vinnukortasíðunni**.
* **Með tölvupósti/síma**, reynir tengivirkið að finna núverandi viðskiptavin með auðkenni fyrst, þá með tölvupósti, og síðan í síma. Ef viðskiptavinurinn finnst ekki-Connector stofnar nýr viðskiptamaður.
* **Með því að** frumskrá upplýsingar reynir Tengillinn að finna viðskiptavininn sem er fyrstur með kennið fyrst og síðan með upplýsingum um aðsetur í reitnum Reikningur. Ef ekki fundið-þá stofnar Connector nýjan viðskiptavin.

> [!NOTE]  
> Í tengivirkinu eru notaðar upplýsingar úr reitnum aðsetur og stofnar viðskiptamannsins [!INCLUDE[prod_short](../includes/prod_short.md)] sem er Reikn. Selt-til-viðskiptamaður er jafnt og Reikn.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Mikilvægar stillingar við innflutning viðskiptavina frá Shopify

Annað hvort er hægt að flytja inn viðskiptavini Shopify í fjöldaeða ásamt innflutningi á pöntunum, eftirfarandi stillingar láta þig hafa umsjón með ferlinu:

|Svæði|Lýsing|
|------|-----------|
|**Innflutningur viðskiptavina frá Shopify**|Veljið **alla viðskiptamenn** ef þú ætlar að flytja inn viðskiptavini úr Shopify í magni; heldur handvirkt í **aðgerðinni samstilling viðskiptamanna** eða vinnslubiðröð með endurteknum uppfærslum. Án tillits til vals verða upplýsingar um viðskiptavin alltaf fluttar inn ásamt pöntuninni. Hins vegar fer notkun þessara upplýsinga eftir **Shopify sniðmátum** og stillingum viðskiptavinar í **reitnum Tegund** kortlagningar viðskiptamanns.|
|**Gerð Kortvörpun viðskiptavinar**|Skilgreinið hvernig tengja á Connector við vörpunaraðgerðina.<br>- **Með tölvupósti/Phone** ef óskað er eftir að Connector kortberi innflutta Shopify viðskiptavininn við viðskiptavin í [!INCLUDE[prod_short](../includes/prod_short.md)] notkun með tölvupósti og síma.</br>- **Með því að reikningsfæra upplýsingar** ef óskað er eftir að Connector kortberi innflutta Shopify viðskiptavininn við viðskiptavin sem hann er í [!INCLUDE[prod_short](../includes/prod_short.md)] með upplýsingum um aðsetursupplýsingar aðilans sem tekur við reikningnum.</br>Veljið **alltaf taka sjálfgefinn viðskiptavin** ef kerfið á að nota viðskiptavin úr reitnum **Sjálfgefið viðskm.** . |
|**Shopify Hægt að uppfæra viðskiptavini**| Veljið ef óskað er eftir að Connector uppfæri viðskiptavini sem finnast þegar **eftir valkosti með tölvupósti/síma** eða **samkvæmt Frumupplýsingum** af frumvarpi í **reitinn Tegund** viðskiptavinarkortlagningar.|
|**Sjálfvirk stofnun óþekktra viðskiptamanna**| Veljið ef óskað er að Connector vanti til að stofna viðskiptamenn, þegar **Valkostir með tölvupósti/síma** eða **eftir uppskrift** eru valdir í **reitnum Tegund** kortvörpun viðskiptavinar. Nýr viðskiptamaður verður stofnaður með innfluttu gögnunum og Sniðmátskóta viðskiptamanns sem **tilgreindur er á** síðum vinnukorta **Shopify eða** sniðmáts **Shopify** viðskiptamanns. Takið eftir að Shopify viðskiptavinurinn þarf að hafa minnst eitt aðsetur. Ef þessi valkostur er ekki virkjaður þarf að stofna viðskiptavin handvirkt og tengja hann við Shopify viðskiptamanninn. Þú getur alltaf haft frumkvæði að stofnun viðskiptavinar handvirkt á **Shopify pöntunarsíðunni**.|
|**Sniðmátskóti viðskiptamanns**|Notað ásamt **sjálfvirkum stofna óþekktum viðskiptavina**.<br> Velja sjálfgefið sniðmát sem á að nota fyrir sjálfvirka stofna viðskiptavini. Ganga þarf úr skugga um að valið sniðmát innihaldi Skyldusvæðin eins og **Alm. viðsk.** **Bókunarflokkur, bókunarflokkur** viðskm., VSK eða VSK-tengd svæði.<br> Hægt er að skilgreina sniðmát fyrir hvert land/svæði á **Shopify síðunni sniðmát** viðskiptamanns sem er gagnlegt fyrir réttan skattaútreikning. <br>Nánari upplýsingar er að finna [í Skattuppsetningu](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Sniðmát viðskiptavinar fyrir hvert land

Sumar stillingar er hægt að skilgreina á lands-/svæðisstigi eða á ríki/héraðsstigi. Hægt er að skilgreina stillingarnar í [sendingu og afhendingar](https://www.shopify.com/admin/settings/shipping) kl Shopify.

**Shopify Viðskiptamannssniðmátið** gerir notanda kleift að gera eftirfarandi við hvert land:

1. **Tilgreinið sjálfgefið viðskm. nr.**, sem tekur forgang yfir valið í **reitum innflutnings Shopify** -og **Viðskiptavinavörpunargerðar**. Það er notað í innfluttu sölupöntuninni.
2. Skilgreinið **Sniðmátskóða viðskiptamanns sem er notaður til að stofna viðskiptavini sem vantar ef** Óþekkt viðskiptamódel **er** virkt. **Ef Sniðmátskóti** viðskiptamanns er auður notar **aðgerðin sniðmátskóta** viðskiptamanns sem tilgreindur er á **Shopify verkstæðisspjaldinu**.
3. Tilgreinið hvort verð feli í sér skatt/VSK fyrir innfluttar pantanir.
4. Í sumum tilvikum er **Sniðmátskóti** viðskiptamanns sem skilgreindur er fyrir land ekki nægur til að tryggja réttan útreikning skatta. T.d. vegna löndaðrar með virðisaukaskatti. Í þessu tilviki **gætu skattasvæðin** verið gagnleg viðbót.

> [!NOTE]  
> Landskótarnir ISO 3166-1 Alpha-2 landskótum. Sjá [Country Code](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode) fyrir nánari upplýsingar.

## <a name="export-customers-to-shopify"></a>Útflutningur viðskiptavina á Shopify

Núverandi viðskiptavini er hægt að Shopify Flytja út í í fjöldasöng. Þar af leiðandi stofnast viðskiptavinur og eitt sjálfgefið aðsetur. Hægt er að stjórna ferlinu með hjálp eftirfarandi stillinga:

|Svæði|Lýsing|
|------|-----------|
|**Útflutningur viðskiptavina á Shopify**|Veljið ef ætlunin er að flytja út alla viðskiptamenn með gilt tölvupóstfang úr [!INCLUDE[prod_short](../includes/prod_short.md)]Shopify í í magnskrá, annað hvort með handvirkt, með **aðgerðinni samstilling viðskiptavina** eða vinnslubiðröð fyrir endurteknar uppfærslur.<br> Við útflutning viðskiptavina með héruðum/ríkjum er gengið úr skugga um að **ISO-Kóði** sé fylltur út fyrir lönd/svæði.|
|**Hægt að uppfæra Shopify viðskiptavini**|Notað ásamt **útflutningsviðskiptamanninum til að Shopify** setja. Gera það virkt ef mynda á uppfærslur síðar frá [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir viðskiptamenn sem eru þegar til í Shopify.|

> [!NOTE]  
> Þegar viðskiptamennirnir Shopify hafa verið stofnaðir gæti verið gott að senda bein fundarboð til viðskiptavina. Það hvetur þá til að virkja reikninginn sinn.

### <a name="populate-customer-information-in-shopify"></a>Fylla út upplýsingar um viðskiptavin í Shopify

Viðskiptavinur í Shopify hefur fornafn, eftirnafn, netfang og/eða símanúmer. Hægt er að fylla út fyrsta nafn og eftirnafn af viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

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

Fyrir heimilisföng þar sem land/hérað er notað er valið *kóti* eða *Heiti* í **reitnum** Upprunagátt á **Shopify verkstæðisspjaldinu** til að tilgreina hvaða tegund af gögnum er geymd í [!INCLUDE[prod_short](../includes/prod_short.md)] í **reitnum land**.

## <a name="sync-customers"></a>Viðskiptavinir samkaupa

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samstilla viðskiptavini til að opna **Shopify síðuna Verkstæðisspjald**.
3. **Veljið aðgerðina samstilla viðskiptavin**.

Einnig er hægt að **nota samstillingaraðgerðina** **Shopify Ræsa viðskiptavin í glugganum Viðskiptavinir** eða leita að **keyrslunni samstilla viðskiptamenn**.

Áætla má að verkefnið sé framkvæmt með sjálfvirkum hætti. Frekari upplýsingar er að finna [í Schedule endurtekin verk](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
