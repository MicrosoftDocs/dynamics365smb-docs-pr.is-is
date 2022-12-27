---
title: Samstilla viðskiptavini
description: Flytja inn viðskiptamenn úr eða flytja þá út í Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 1a796d1094401cd2ebc0efd54f752211d22bfb12
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728654"
---
# <a name="synchronize-customers"></a>Samstilla viðskiptavini

Þegar pöntun er flutt inn úr Shopify er mikilvægt að fá upplýsingar um viðskiptamanninn fyrir frekari vinnslu á skjalinu í [!INCLUDE[prod_short](../includes/prod_short.md)]. Þetta eru tveir helstu valkostirnir til að gera það og samsetningar þeirra:

* Notaðu sérstakan viðskiptamann fyrir allar pantanir.
* Flyttu inn raunverulegar upplýsingar um viðskiptamann úr Shopify. Þessi valkostur er einnig í boði þegar þú flytur út viðskiptamenn í Shopify úr [!INCLUDE[prod_short](../includes/prod_short.md)] fyrst.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Mikilvægar stillingar við innflutning viðskiptamanna úr Shopify

Hvort sem þú flytur inn viðskiptamenn úr Shopify í magni eða á sama tíma og þú flytur inn pantanir munu eftirfarandi stillingar gera þér kleift að stjórna ferlinu:

|Svæði|Lýsing|
|------|-----------|
|**Innflutningur viðskiptamanns úr Shopify**|Veldu **Allir viðskiptamenn** ef þú ætlar að flytja inn viðskiptamenn úr Shopify í magni; annaðhvort handvirkt með aðgerðinni **Samstilla viðskiptamenn** eða í gegnum verkröðina fyrir endurteknar uppfærslur. Óháð því hvað er valið munu upplýsingar um viðskiptamanninn alltaf vera fluttar inn með pöntuninni. Notkun þessara upplýsingar eru hins vegar háðar **Shopify Viðskiptamannasniðmátum** og stillingum í reitnum **Vörpunargerð viðskiptamanns**.|
|**Vörpunargerð viðskiptamanns**|Skilgreindu hvernig tengillinn á að framkvæma vörpunina.<br>- **Með tölvupósti/síma** ef þú vilt að tengillinn varpi innfluttum Shopify viðskiptamanni í fyrirliggjandi viðskiptamann í [!INCLUDE[prod_short](../includes/prod_short.md)] með tölvupósti og síma.</br>- **Eftir upplýsingum um „reikningsfæra á“** ef þú vilt að tengillinn noti aðsetur viðtakanda reikningsins til að varpa innfluttum Shopify viðskiptamanni í fyrirliggjandi viðskiptamann í [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Veldu **Alltaf taka sjálfgefinn viðskiptamann** ef þú vilt að kerfið noti viðskiptamann úr **Sjálfgefnu viðskiptamannanr.** . |
|**Shopify Getur uppfært viðskiptamenn**| Veldu þennan reit ef þú vilt að tengillinn uppfæri viðskiptamennina sem hann finnur þegar annaðhvort valkosturinn **Eftir tölvupósti/síma** eða **Eftir upplýsingum um „reikningsfæra á“** er valinn í reitnum **Vörpunargerð viðskiptamanns**.|
|**Búa til óþekktan viðskiptamann sjálfvirkt**| Veldu þennan reit ef þú vilt að tengillinn stofni viðskiptamennina sem vantar þegar valkosturinn **Eftir tölvupósti/síma** eða **Eftir upplýsingum um „reikningsfæra á“** er valinn í reitnum **Vörpunargerð viðskiptamanns**. Nýr viðskiptamaður verður stofnaður með innfluttum gögnum og **Sniðmátskóði viðskiptamanns** sem skilgreindur er á síðunum **Shopify Verslunarkort** eða **Shopify Viðskiptamannasniðmát**. Taktu eftir að Shopify viðskiptamaðurinn verður að vera með minnst eitt aðsetur. Ef þessi valkostur er ekki virkur þarftu að stofna viðskiptamann handvirkt og tengja hann við Shopify viðskiptamanninn. Það er alltaf hægt að hefja stofnun viðskiptamanns handvirkt af síðunni **Shopify Pöntun**.|
|**Viðskiptamannasniðmátskóði**|Þessi reitur er notaður með **Stofna óþekktan viðskiptamann sjálfkrafa**.<br>- Veldu sjálfgefna sniðmátið sem á að nota fyrir sjálfkrafa stofnaða viðskiptamenn. Gakktu úr skugga um að valið sniðmát innihaldi áskilda reiti á borð við **Alm. viðskiptabókunarflokkur**, **Bókunarflokkur viðskiptamanns** og VSK-reiti eða aðra skatttengda reiti.<br>- Þú getur skilgreint sniðmát fyrir hvert land/svæði á síðunni **Shopify Viðskiptamannasniðmát**, sem er gagnleg fyrir réttan skattaútreikning. <br>- Frekari upplýsingar á [Setja upp skatta](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Sniðmát viðskiptamanns eftir landi

Hægt er að skilgreina sumar stillingar á stigi lands/svæðis eða ríkis/héraðs. Hægt er að velja stillingarnar í [Sending og afhending](https://www.shopify.com/admin/settings/shipping) í Shopify.

Þú getur gert eftirfarandi fyrir hvern viðskiptamann með því að nota **Shopify Sniðmát viðskiptamanns**:

1. Tilgreindu **Sjálfgefið viðskiptamannanr.**, sem hefur forgang fram  yfir valið í reitunum **Innflutningur viðskiptamanns úr Shopify** og **Vörpunargerð viðskiptamanns**. Þetta er notað í innfluttri sölupöntun.
2. Skilgreindu **Sniðmátskóða viðskiptamanns**, sem er notaður til að stofna viðskiptamenn sem vantar ef **Stofna óþekkta viðskiptamenn sjálfkrafa** er virkjað. Ef **Sniðmátskóði viðskiptamanns** er auður, þá notar aðgerðin **Sniðmátskóði viðskiptamanns** sem skilgreind er í **Shopify Verslunarkort**.
3. Skilgreina hvort verð innihaldi VSK/skatt fyrir innfluttar pantanir.
4. Í sumum tilfellum er **Sniðmátskóði viðskiptamanns** sem skilgreindur er fyrir land ekki nóg til að tryggja réttan útreikning á sköttum (til dæmis fyrir lönd með söluskatti). Í þessu tilfelli gæti verið gagnlegt að bæta við **Skattsvæðum**.

> [!NOTE]  
> Landskóðar eru ISO 3166-1 og alfa-2 landskóðar. Frekari upplýsingar er að finna í [Landskóði](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Flytja út viðskiptamenn í Shopify

Hægt er að flytja núverandi viðskiptavina í Shopify í miklu magni. Í hverju tilviki er búinn til viðskiptavinur og eitt sjálfgefið heimilisfang. Þú getur stjórnað ferlinu með eftirfarandi stillingum:

|Svæði|Lýsing|
|------|-----------|
|**Flytja út viðskiptamenn í Shopify**|Veldu þetta ef þú ætlar að flytja út alla viðskiptamenn úr [!INCLUDE[prod_short](../includes/prod_short.md)] í Shopify í magni. Þetta er hægt að gera annaðhvort handvirkt með aðgerðinni **Samstilla viðskiptamenn** eða sjálfkrafa með verkröð fyrir endurteknar uppfærslur.<br> Þegar fluttir eru út viðskiptamenn með aðsetur sem inniheldur héröð/ríki skaltu ganga úr skugga um **ISO-kóði** sé útfylltur fyrir löndin/svæðin.|
|**Getur uppfært Shopify viðskiptamenn**|Þetta er notað með stillingunni **Flytja út viðskiptamann í Shopify**. Virkja hana ef þú vilt búa til uppfærslur síðar úr [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir viðskiptamenn sem þegar eru til í Shopify.|

Eftirfarandi kröfur eru gerðar til útflutnings viðskiptavinar:

* Viðskiptavinurinn verður að vera með gilt netfang.
* Land/svæði er valið á viðskiptamannaspjaldinu, fyrir trygga viðskiptamenn, með autt land/svæði verður land/svæði sem tilgreint er á síðunni **Upplýsingar um fyrirtæki** að vera með ISO-kóða skilgreindan.
* Ef viðskiptamaðurinn er með símanúmer þá verður númerið að vera einkvæmt því að Shopify samþykkir ekki annan viðskiptamann með sama símanúmerið.
* Ef viðskiptavinur er með símanúmer verður það að vera á E.164-sniði. Mismunandi snið eru studd ef þau gefa upp númer sem hægt er að hringja í hvaðan sem er í heiminum. Eftirfarandi snið eru gild:
  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Þegar þú hefur stofnað viðskiptamennina í Shopify geturðu sent þeim bein boð til að hvetja þá til að virkja reikningana sína.

### <a name="populate-customer-information-in-shopify"></a>Fylltu út upplýsingar um viðskiptamann í Shopify

Viðskiptavinur í Shopify er með fornafn, eftirnafn, netfang og/eða símanúmer. Hægt er að slá inn fornafn og eftirnafn af viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Reitur í viðskiptamannaspjaldinu|Lýsing|
|------|------|-----------|
|1|**Heiti tengiliðar**|Hæsti forgangur, ef reiturinn **Nafn tengiliðar** er fyllt út og reiturinn **Uppruni tengiliðar** í **Shopify verslunarkortinu** inniheldur annaðhvort valkostinn *Fornafn og eftirnafn* eða *Eftirnafn og fornafn* til að skilgreina hvernig á að skipta gildunum|
|2|**Heiti 2**|Ef reiturinn **Nafn 2** er fylltur út og reiturinn **Nafn 2 uppruni** í **Shopify verslunarkortinu** inniheldur annaðhvort valkostinn *Fornafn og eftirnafn* eða *Eftirnafn og fornafn* til að skilgreina hvernig á að skipta gildunum.|
|3|**Heiti**|Lægsti forgangur, ef reiturinn **Nafn** er fylltur út og reiturinn **Uppruni nafns** í **Shopify verslunarkortinu** inniheldur annaðhvort valkostinn *Fornafn og eftirnafn* eða *Eftirnafn og fornafn* til að skilgreina hvernig á að skipta gildunum.|

Viðskiptamaður í Shopify er einnig með sjálfgefið aðsetur sem gæti innihaldið fyrirtæki og aðsetur ásamt fornafni, eftirnafni, netfangi og/eða síma. Þú getur fyllt út reitinn **Fyrirtæki** á grundvelli gagna frá viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Reitur í viðskiptamannaspjaldinu|Lýsing|
|------|------|-----------|
|1|**Heiti**|Hæsti forgangur, ef reiturinn **Uppruni nafns** í **Shopify verslunarkortinu** inniheldur *Nafn fyrirtækis*.|
|2|**Heiti 2**|Lægsti forgangur, ef reiturinn **Uppruni nafns 2** í **Shopify verslunarkortinu** inniheldur *Nafn fyrirtækis*.|

Fyrir aðsetur þar sem landið/svæðið er notað skal velja *Kóði* eða *Nafn* í reitnum **Uppruni lands** í **Shopify verslunarkortinu**. Þetta tilgreinir hvers konar gögn eru geymd í [!INCLUDE[prod_short](../includes/prod_short.md)] í reitnum **Land**.

## <a name="sync-customers"></a>Samstilla viðskiptamenn

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Shopify verslun** og velja síðan viðkomandi tengil.
2. Veldu tiltekna verslun þar sem þú vilt samstilla viðskiptamenn.
3. Veldu aðgerðina **Samstilla viðskiptamenn**.

Einnig er hægt að nota aðgerðina **Hefja samstillingu viðskiptamanns** í glugganum **Shopify viðskiptamenn** eða leita að runuvinnslunni **Samstilla viðskiptamenn**.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
