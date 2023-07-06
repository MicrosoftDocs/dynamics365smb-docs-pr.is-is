---
title: Samstilla viðskiptavini
description: Flytja inn viðskiptamenn úr eða flytja þá út í Shopify
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# Samstilla viðskiptavini

Þegar pöntun er flutt inn frá  Shopify, fá upplýsingarnar um viðskiptamanninn nauðsynlegt fyrir frekari vinnslu skjalsins í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það eru tveir meginmöguleikar til að gera það, og nokkrar samsetningar:

* Notaðu sérstakan viðskiptamann fyrir allar pantanir.
* Flyttu inn raunverulegar upplýsingar um viðskiptamann úr Shopify. Þessi valkostur er einnig í boði þegar þú flytur út viðskiptamenn í Shopify úr [!INCLUDE[prod_short](../includes/prod_short.md)] fyrst.

## Mikilvægar stillingar við innflutning viðskiptamanna úr Shopify

Hvort sem þú fluttir inn viðskiptavini frá  Shopify  í fjöldaeða þegar þú pantar, Notaðu þá eftirfarandi stillingar til að stjórna ferlinu:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Innflutningur viðskiptamanns úr Shopify**|Veldu **Allir viðskiptamenn** ef þú ætlar að flytja inn viðskiptamenn úr Shopify í magni; annaðhvort handvirkt með aðgerðinni **Samstilla viðskiptamenn** eða í gegnum verkröðina fyrir endurteknar uppfærslur. Óháð því hvað er valið munu upplýsingar um viðskiptamanninn alltaf vera fluttar inn með pöntuninni. Notkun þessara upplýsingar eru hins vegar háðar **Shopify Viðskiptamannasniðmátum** og stillingum í reitnum **Vörpunargerð viðskiptamanns**.|
|**Vörpunargerð viðskiptamanns**|Skilgreindu hvernig tengillinn á að framkvæma vörpunina.<br>- **Með tölvupósti/síma** ef þú vilt að tengillinn varpi innfluttum Shopify viðskiptamanni í fyrirliggjandi viðskiptamann í [!INCLUDE[prod_short](../includes/prod_short.md)] með tölvupósti og síma.</br>- **Eftir upplýsingum um „reikningsfæra á“** ef þú vilt að tengillinn noti aðsetur viðtakanda reikningsins til að varpa innfluttum Shopify viðskiptamanni í fyrirliggjandi viðskiptamann í [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Veldu **Alltaf taka sjálfgefinn viðskiptamann** ef þú vilt að kerfið noti viðskiptamann úr **Sjálfgefnu viðskiptamannanr.** . |
|**Shopify Getur uppfært viðskiptamenn**| Veldu þennan reit ef þú vilt að tengillinn uppfæri viðskiptamennina sem hann finnur þegar annaðhvort valkosturinn **Eftir tölvupósti/síma** eða **Eftir upplýsingum um „reikningsfæra á“** er valinn í reitnum **Vörpunargerð viðskiptamanns**.|
|**Búa til óþekktan viðskiptamann sjálfvirkt**| Veldu þennan reit ef þú vilt að tengillinn stofni viðskiptamennina sem vantar þegar valkosturinn **Eftir tölvupósti/síma** eða **Eftir upplýsingum um „reikningsfæra á“** er valinn í reitnum **Vörpunargerð viðskiptamanns**. Nýr viðskiptamaður verður stofnaður með innfluttum gögnum og **Sniðmátskóði viðskiptamanns** sem skilgreindur er á síðunum **Shopify Verslunarkort** eða **Shopify Viðskiptamannasniðmát**. Taktu eftir að Shopify viðskiptamaðurinn verður að vera með minnst eitt aðsetur. Oft eru upplýsingar um aðsetursskipanir stofnaðar með  Shopify  sölurásum sölustaða. Ef þessi valkostur er ekki virkur þarftu að stofna viðskiptamann handvirkt og tengja hann við Shopify viðskiptamanninn.|
|**Viðskiptamannasniðmátskóði**|Þessi reitur er notaður með **Stofna óþekktan viðskiptamann sjálfkrafa**.<br>- Veldu sjálfgefna sniðmátið sem á að nota fyrir sjálfkrafa stofnaða viðskiptamenn. Gakktu úr skugga um að valið sniðmát innihaldi áskilda reiti á borð við **Alm. viðskiptabókunarflokkur**, **Bókunarflokkur viðskiptamanns** og VSK-reiti eða aðra skatttengda reiti.<br>- Þú getur skilgreint sniðmát fyrir hvert land/svæði á síðunni **Shopify Viðskiptamannasniðmát**, sem er gagnleg fyrir réttan skattaútreikning. <br>- Frekari upplýsingar á [Setja upp skatta](setup-taxes.md).|

### Sniðmát viðskiptavinar fyrir hvert land/svæði

Hægt er að skilgreina sumar stillingar á stigi lands/svæðis eða ríkis/héraðs. Hægt er að velja stillingarnar í [Sending og afhending](https://www.shopify.com/admin/settings/shipping) í Shopify.

Þú getur gert eftirfarandi fyrir hvern viðskiptamann með því að nota **Shopify Sniðmát viðskiptamanns**:

1. Tilgreindu **Sjálfgefið viðskiptamannanr.**, sem hefur forgang fram  yfir valið í reitunum **Innflutningur viðskiptamanns úr Shopify** og **Vörpunargerð viðskiptamanns**. Þetta er notað í innfluttri sölupöntun.
2. Skilgreindu **Sniðmátskóða viðskiptamanns**, sem er notaður til að stofna viðskiptamenn sem vantar ef **Stofna óþekkta viðskiptamenn sjálfkrafa** er virkjað. Ef **Sniðmátskóði viðskiptamanns** er auður, þá notar aðgerðin **Sniðmátskóði viðskiptamanns** sem skilgreind er í **Shopify Verslunarkort**. Kerfið reynir fyrst að finna sniðmát fyrir  **contry/svæðiskótann**  fyrir sjálfgefna aðsetrið. Ef hann finnur ekki sniðmát notar það fyrsta aðsetrið.
3. Í sumum tilfellum er Sniðmátskóti  **viðskiptamanns sem**  skilgreindur er fyrir land/svæði ekki nægur til að tryggja rétta skattaútreikninga (til dæmis fyrir lönd/svæði með virðisaukaskatti). Í þessu tilviki gæti þar með  **skattsvæði**  verið gagnleg viðbót.
4. Svæðið skattsvæði inniheldur einnig landskóta  **og**  par sem  **Sýsla heiti**  .  **·**  Þetta par er gagnlegt þegar Connector þarf að umbreyta kóta í heiti, eða öfugt.

> [!NOTE]  
> Landskóðar eru ISO 3166-1 og alfa-2 landskóðar. Frekari upplýsingar er að finna í [Landskóði](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Flytja út viðskiptamenn í Shopify

Hægt er að flytja núverandi viðskiptavina í Shopify í miklu magni. Í hverju tilviki er búinn til viðskiptavinur og eitt sjálfgefið heimilisfang. Þú getur stjórnað ferlinu með eftirfarandi stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Flytja út viðskiptamenn í Shopify**|Þessi kostur er valinn ef flytja á út alla viðskiptavini úr  [!INCLUDE[prod_short](../includes/prod_short.md)]  Shopify  í magn. Þetta er hægt að gera annaðhvort handvirkt með aðgerðinni **Samstilla viðskiptamenn** eða sjálfkrafa með verkröð fyrir endurteknar uppfærslur.<br> Þegar fluttir eru út viðskiptamenn með aðsetur sem inniheldur héröð/ríki skaltu ganga úr skugga um **ISO-kóði** sé útfylltur fyrir löndin/svæðin.|
|**Getur uppfært Shopify viðskiptamenn**|Þessi valkostur vinnur saman með  **útflutningsviðskiptamanninum sem á að  Shopify**  setja. Gera þennan valkost virkan ef mynda á uppfærslur síðar frá  [!INCLUDE[prod_short](../includes/prod_short.md)]  fyrir viðskiptamenn sem eru þegar til í Shopify.|

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

### Fylltu út upplýsingar um viðskiptamann í Shopify

Viðskiptavinur í  Shopify  hefur fornafn, nafn fjölskyldu, netfang og/eða símanúmer. Fyrst má færa inn nöfn og fjölskylduheiti af viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Reitur í viðskiptamannaspjaldinu|Lýsing|
|------|------|-----------|
|1|**Heiti tengiliðar**|Hæsti forgangur, ef reiturinn **Nafn tengiliðar** er fyllt út og reiturinn **Uppruni tengiliðar** í **Shopify verslunarkortinu** inniheldur annaðhvort valkostinn *Fornafn og eftirnafn* eða *Eftirnafn og fornafn* til að skilgreina hvernig á að skipta gildunum|
|2|**Heiti 2**| **Ef reiturinn Heiti 2**  er fylltur út og  **reiturinn Heiti 2**  í  **Shopify  verkstæðisspjaldinu**  inniheldur annað hvort  *fyrsta nafn og eftirnafn*  eða  *eftirnafn og valkostinn fornafn*  til að skilgreina hvernig eigi að skipta gildum.|
|3|**Heiti**|Lægsti forgangur, ef reiturinn **Nafn** er fylltur út og reiturinn **Uppruni nafns** í **Shopify verslunarkortinu** inniheldur annaðhvort valkostinn *Fornafn og eftirnafn* eða *Eftirnafn og fornafn* til að skilgreina hvernig á að skipta gildunum.|

Viðskiptavinur í  Shopify  er einnig með sjálfgefið aðsetur. Heimilisfangið gæti innihaldið fyrirtæki og heimilisfang auk skírnarnafns þeirra, fjölskyldunafns, tölvupósts og/eða símanúmera. Þú getur fyllt út reitinn **Fyrirtæki** á grundvelli gagna frá viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Reitur í viðskiptamannaspjaldinu|Lýsing|
|------|------|-----------|
|1|**Heiti**|Hæsti forgangur, ef reiturinn **Uppruni nafns** í **Shopify verslunarkortinu** inniheldur *Nafn fyrirtækis*.|
|2|**Heiti 2**|Lægsti forgangur, ef reiturinn **Uppruni nafns 2** í **Shopify verslunarkortinu** inniheldur *Nafn fyrirtækis*.|

Fyrir aðsetur þar sem Sýsla/hérað er notað er valinn  **kóti**  eða  **Heiti**  í  **reitnum sýsluuppruni**  á  **Shopify  vinnukortasíðunni** . Kótinn eða nafnið Tilgreinir tegund gagna sem geymd eru  [!INCLUDE[prod_short](../includes/prod_short.md)]  í  **í svæðinu Sýsla** . Munið að frumstilla sniðmát viðskiptamanns eftir landi/svæði svo að vörpun sýslukóta/heitilnafna sé tilbúin. 


## Samstilla viðskiptamenn

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Shopify verslun** og velja síðan viðkomandi tengil.
2. Veldu tiltekna verslun þar sem þú vilt samstilla viðskiptamenn.
3. Veldu aðgerðina **Samstilla viðskiptamenn**.

Einnig er hægt að nota aðgerðina **Hefja samstillingu viðskiptamanns** í glugganum **Shopify viðskiptamenn** eða leita að runuvinnslunni **Samstilla viðskiptamenn**.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

## Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
