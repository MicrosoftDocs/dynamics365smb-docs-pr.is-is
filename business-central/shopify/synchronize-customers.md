---
title: Samstilla viðskiptavini
description: Flytja inn viðskiptamenn úr eða flytja þá út í Shopify
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# <a name="synchronize-customers-and-companies"></a>Samstilla viðskiptavini og fyrirtæki

Þegar pöntun er flutt inn úr Shopify er nauðsynlegt að fá upplýsingar um viðskiptamanninn til frekari vinnslu skjalsins í [!INCLUDE[prod_short](../includes/prod_short.md)]. Tveir aðalvalkostir eru í boði til að gera það og nokkrar samsetningar:

* Notaðu sérstakan viðskiptamann fyrir allar pantanir.
* Flytja inn upplýsingar um viðskiptavin úr Shopify. Þessi valkostur er einnig tiltækur þegar viðskiptamenn eru fluttir út til Shopify  [!INCLUDE[prod_short](../includes/prod_short.md)].

Shopify gerir þér kleift að keyra B2B og DTC fyrirtæki frá einum stað með krafti og vellíðan Shopify í öllum-einn vettvang. Shopify Connector vinnur einnig með mismunandi bragðtegundir e-Commerce.

Á meðan Shopify eru tvær einingar, viðskiptamenn og fyrirtæki, en [!INCLUDE[prod_short](../includes/prod_short.md)] hefur aðeins viðskiptamannaeininguna, sem hefur áhrif á það hvernig samstilling virkar.

Þegar DTC er keyrt er kaupandinn stofnaður sem Shopify viðskiptamaður. THe viðskiptavinur er síðan fluttur inn í [!INCLUDE[prod_short](../includes/prod_short.md)] sem viðskiptamaður Shopify og tengdur eða breytt í viðskiptamann.

Ef B2B er keyrt er kaupandinn stofnaður sem Shopify viðskiptamaður sem tengist fyrirtæki. Viðskiptavinurinn er fluttur inn í [!INCLUDE[prod_short](../includes/prod_short.md)] sem viðskiptamaður Shopify og fyrirtækið er flutt inn í [!INCLUDE[prod_short](../includes/prod_short.md)]  Shopify fyrirtæki og tengt við viðskiptamann.

Til að flytja viðskiptamann út frá [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify eru skrefin aðeins mismunandi eftir því hvað á að gera:

* Flytja út viðskiptavin sem Shopify viðskiptavin fyrir DTC.
* Flytja út viðskiptavin sem fyrirtæki og viðskiptavinapar fyrir B2B-flæðið.

## <a name="important-settings-when-importing-dtc-customers-from-shopify"></a>Mikilvægar stillingar þegar DTC viðskiptavinir eru fluttir inn frá Shopify

Hvort sem viðskiptavinir eru fluttir inn úr Shopify lausu eða þegar pantanir eru fluttar inn eru eftirfarandi stillingar notaðar til að stjórna ferlinu:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Innflutningur viðskiptamanns úr Shopify**|Veldu **Allir viðskiptamenn** ef þú ætlar að flytja inn viðskiptamenn úr Shopify í magni; annaðhvort handvirkt með aðgerðinni **Samstilla viðskiptamenn** eða í gegnum verkröðina fyrir endurteknar uppfærslur. Óháð því hvað er valið munu upplýsingar um viðskiptamanninn alltaf vera fluttar inn með pöntuninni. Notkun þessara upplýsingar eru hins vegar háðar **Shopify Viðskiptamannasniðmátum** og stillingum í reitnum **Vörpunargerð viðskiptamanns**.|
|**Vörpunargerð viðskiptamanns**|Skilgreindu hvernig tengillinn á að framkvæma vörpunina.</br></br>- **Með tölvupósti/síma** ef þú vilt að tengillinn noti tölvupóstreikning og símaupplýsingar til að varpa innfluttum Shopify viðskiptavini á viðskiptavin í Business Central.</br></br>- **Með Reikningsfærsluuppl.** ef tengillinn á að nota aðsetur viðtakanda reiknings til að varpa innfluttum Shopify viðskiptamanni á viðskiptamann sem er til í Business Central.</br></br>Valið er **Alltaf taka sjálfgefinn viðskiptamann** ef kerfið á að nota viðskiptamann úr reitnum **Sjálfgefinn viðskm.nr.** . |
|**Shopify Getur uppfært viðskiptamenn**| Veldu þennan reit ef þú vilt að tengillinn uppfæri viðskiptamennina sem hann finnur þegar annaðhvort valkosturinn **Eftir tölvupósti/síma** eða **Eftir upplýsingum um „reikningsfæra á“** er valinn í reitnum **Vörpunargerð viðskiptamanns**.|
|**Búa til óþekktan viðskiptamann sjálfvirkt**| Veldu þennan reit ef þú vilt að tengillinn stofni viðskiptamennina sem vantar þegar valkosturinn **Eftir tölvupósti/síma** eða **Eftir upplýsingum um „reikningsfæra á“** er valinn í reitnum **Vörpunargerð viðskiptamanns**. Nýr viðskiptamaður er stofnaður með innfluttum gögnum og **Kóti** viðskiptamannssniðmáts sem skilgreindur er á síðunum **Shopify Vinnusalarspjald** eða **Shopify Sniðmát** viðskiptamanns. Taktu eftir að Shopify viðskiptamaðurinn verður að vera með minnst eitt aðsetur. Pantanir sem búnar eru til í gegnum sölurás sölustaðar Shopify vantar oft aðsetursupplýsingar. Ef þessi valkostur er ekki virkjaður verður að stofna viðskiptamann handvirkt og tengja hann við viðskiptamanninn Shopify .|
|**Kóti viðskiptamanns-fyrirtækissniðmáts**|Þessi reitur er notaður með **Sjálfvirk stofnun óþekktra viðskiptamanna**.</br></br> Velja sjálfgefna sniðmátið sem nota á fyrir viðskiptamenn sem eru stofnaðir sjálfvirkt. Ganga þarf úr skugga um að í völdu sniðmáti séu áskildir reitir, svo sem **Alm. viðskiptabókunarflokkur**, **Bókunarflokkur** viðskm. og virðisaukaskattur (VSK) eða skatttengdir reitir.</br></br>Hægt er að skilgreina sniðmát fyrir hvert land/svæði á síðunni **Shopify Sniðmát viðskiptamanns** sem hjálpar til við að reikna skatta rétt.</br></br>Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|

### <a name="customer-template-per-countryregion"></a>Sniðmát viðskiptamanns eftir landi/svæði

Hægt er að skilgreina sumar stillingar á stigi lands/svæðis eða ríkis/héraðs. Hægt er að velja stillingarnar í [Sending og afhending](https://www.shopify.com/admin/settings/shipping) í Shopify.

Þú getur gert eftirfarandi fyrir hvern viðskiptamann með því að nota **Shopify Sniðmát viðskiptamanns**:

1. Tilgreindu **Sjálfgefið viðskiptamannanr.**, sem hefur forgang fram  yfir valið í reitunum **Innflutningur viðskiptamanns úr Shopify** og **Vörpunargerð viðskiptamanns**. Þetta er notað í innfluttri sölupöntun.
2. Skilgreindu **Sniðmátskóða viðskiptamanns**, sem er notaður til að stofna viðskiptamenn sem vantar ef **Stofna óþekkta viðskiptamenn sjálfkrafa** er virkjað. Ef **Sniðmátskóði viðskiptamanns** er auður, þá notar aðgerðin **Sniðmátskóði viðskiptamanns** sem skilgreind er í **Shopify Verslunarkort**. Kerfið leitar fyrst að sniðmáti fyrir **samn./svæðiskóta** fyrir sjálfgefna aðsetrið. Ef það finnur ekki sniðmát notar það fyrsta aðseturið.
3. Í sumum tilvikum nægir kóti **sniðmáts viðskiptamanns** sem skilgreindur er fyrir land/svæði til að tryggja rétta skattútreikninga (til dæmis fyrir lönd/svæði með söluskatt). Í þessu tilviki **gæti skattsvæði** verið gagnleg viðbót.
4. Í **reitnum Skattsvæði** eru **einnig landskóti** og **Sýsluheiti** . Þetta par er gagnlegt þegar tengið þarf að umbreyta kóta í nafn eða öfugt.

> [!NOTE]  
> Landskóðar eru ISO 3166-1 og alfa-2 landskóðar. Frekari upplýsingar er að finna í [Landskóði](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="important-settings-when-exporting-dtc-customers-to-shopify"></a>Mikilvægar stillingar þegar DTC viðskiptavinir eru fluttir út til Shopify

Hægt er að flytja núverandi viðskiptavina í Shopify í miklu magni. Í hverju tilviki er búinn til viðskiptavinur og eitt sjálfgefið heimilisfang. Þú getur stjórnað ferlinu með eftirfarandi stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Getur uppfært Shopify viðskiptamenn**| Þessi valkostur er gerður virkur ef búa á til uppfærslur síðar úr Business Central fyrir viðskiptamenn sem þegar eru til í Shopify.|

Eftirfarandi kröfur eru gerðar til útflutnings viðskiptavinar:

* Viðskiptavinurinn verður að vera með gilt netfang.
* Þegar viðskiptamenn eru fluttir út með aðsetrum sem eru héruð/ríki skal ganga úr skugga um að **ISO-kótinn** sé fylltur út fyrir lönd/svæði.|
* Fyrir landið/svæðið er valið á viðskiptamannaspjaldinu þarf að tryggja að ISO-kótinn **sé**. Fyrir staðbundna viðskiptamenn Shopify  notar tengill landið/svæðið sem tilgreint er í **Stofngögnunum**.
* Ef viðskiptamaðurinn er með símanúmer þá verður númerið að vera einkvæmt því að Shopify samþykkir ekki annan viðskiptamann með sama símanúmerið.
* Ef viðskiptavinur er með símanúmer verður það að vera á E.164-sniði. Mismunandi snið eru studd ef þau gefa upp númer sem hægt er að hringja í hvaðan sem er í heiminum. Eftirfarandi snið eru gild:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Þegar búið er að stofna viðskiptamennina í Shopify er hægt að senda þeim bein fundarboð til að hvetja þá til að virkja reikninga sína.

### <a name="populate-customer-information-in-shopify"></a>Fylltu út upplýsingar um viðskiptamann í Shopify

Viðskiptavinur með Shopify fornafn, samsafnsheiti, tölvupóst og/eða símanúmer. Hægt er að færa inn for- og samsafnsheiti á viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Reitur í viðskiptamannaspjaldinu|Lýsing|
|------|------|-----------|
|1|**Heiti tengiliðar**|Hæsti forgangur, ef reiturinn **Nafn tengiliðar** er fyllt út og reiturinn **Uppruni tengiliðar** í **Shopify verslunarkortinu** inniheldur annaðhvort valkostinn *Fornafn og eftirnafn* eða *Eftirnafn og fornafn* til að skilgreina hvernig á að skipta gildunum|
|2|**Heiti 2**|Ef reiturinn **Heiti 2** er fylltur út og í reitnum **Heiti 2, Uppruni** í **Shopify verkstæðisspjaldinu**, er annaðhvort *valkosturinn Fornafn og Eftirnafn* og *Fornafn* til að skilgreina hvernig gildunum er skipt.|
|3|**Heiti**|Lægsti forgangur, ef reiturinn **Nafn** er fylltur út og reiturinn **Uppruni nafns** í **Shopify verslunarkortinu** inniheldur annaðhvort valkostinn *Fornafn og eftirnafn* eða *Eftirnafn og fornafn* til að skilgreina hvernig á að skipta gildunum.|

Viðskiptamaður í Shopify hefur einnig sjálfgefið aðsetur. Heimilisfangið gæti innihaldið fyrirtæki og heimilisfang auk fornafns, samsafnsheitis, tölvupósts og/eða símanúmers. Þú getur fyllt út reitinn **Fyrirtæki** á grundvelli gagna frá viðskiptamannaspjaldinu í [!INCLUDE[prod_short](../includes/prod_short.md)].

|Forgangur|Reitur í viðskiptamannaspjaldinu|Lýsing|
|------|------|-----------|
|1|**Heiti**|Hæsti forgangur, ef reiturinn **Uppruni nafns** í **Shopify verslunarkortinu** inniheldur *Nafn fyrirtækis*.|
|2|**Heiti 2**|Lægsti forgangur, ef reiturinn **Uppruni nafns 2** í **Shopify verslunarkortinu** inniheldur *Nafn fyrirtækis*.|

Fyrir aðsetur þar sem sýsla/hérað er notuð skal velja **Kóti** eða **Heiti** í reitnum **Uppruni** sýslu á síðunni **Shopify Vinnusalarspjald** . Kótinn eða heitið tilgreinir tegund gagna sem geymd eru í [!INCLUDE[prod_short](../includes/prod_short.md)] reitnum **Sýsla** . Muna þarf að frumstilla viðskiptamannasniðmát eftir landi/svæði svo að vörpun sýslukóta/heitis sé tilbúin. 

## <a name="export-dtc-customers-to-shopify"></a>Flytja viðskiptavini DTC út til Shopify

### <a name="initial-sync-of-customers-from-business-central-to-shopify"></a>Upphafleg samstilling viðskiptavina frá Business Central til Shopify

1. Farðu í leitarljósið ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Shopify Viðskiptamenn** og velja viðeigandi tengil.
2. Veljið aðgerðina **Bæta við viðskiptamanni** .
3. Sláðu inn kóðann inn í reitinn **Verslunarkóði**. Ef glugginn Viðskiptamenn **Shopify er opnaður** af síðunni **Vinnusalarspjald** er vinnusalarkótinn fylltur út sjálfkrafa.
4. Skilgreina afmarkanir á viðskiptavin eins og þörf krefur. Hægt er t.d. að afmarka eftir lands-/svæðiskóta.
5. Velja **Í lagi**.

Viðskiptamennirnir sem verða til verða sjálfkrafa stofnaðir með aðsetri Shopify .

> [!NOTE]  
> Upphafleg samstilling viðskiptamanna frá [!INCLUDE[prod_short](../includes/prod_short.md)] til tekur ekki tillit Shopify til **stillinganna Uppfæra Shopify viðskiptamenn** .

### <a name="sync-customers"></a>Samstilla viðskiptamenn

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Shopify verslun** og velja síðan viðkomandi tengil.
2. Veldu tiltekna verslun þar sem þú vilt samstilla viðskiptamenn.
3. Veldu aðgerðina **Samstilla viðskiptamenn**.

Einnig er hægt að nota aðgerðina **Hefja samstillingu viðskiptamanns** í glugganum **Shopify viðskiptamenn** eða leita að runuvinnslunni **Samstilla viðskiptamenn**.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

## <a name="b2b-companies"></a>B2B fyrirtæki

Ef B2B er notað í Shopify er einnig hægt að stofna fyrirtæki til viðbótar við viðskiptamenn. Hægt er að tengja einn eða fleiri viðskiptamenn við fyrirtæki. Einnig er hægt að skilgreina greiðsluskilmála, birgðageymslur og vörulista.

## <a name="important-settings-when-importing-b2b-companies-from-shopify"></a>Mikilvægar stillingar þegar B2B-fyrirtæki eru flutt inn frá Shopify

Hvort sem fyrirtæki eru flutt inn úr Shopify lausu eða þegar pantanir eru fluttar inn skal nota stillingarnar í eftirfarandi töflu til að stjórna ferlinu.

|Svæði|Heimildasamstæða|
|------|-----------|
|**Fyrirtækisinnflutningur úr Shopify**|Veljið **Öll fyrirtæki** ef ætlunin er að flytja viðskiptamenn inn úr Shopify í lausu, annaðhvort handvirkt með aðgerðinni **Samstilla fyrirtæki** eða með verkröðinni fyrir endurteknar uppfærslur. Burtséð frá því sem valið er eru upplýsingar um viðskiptavininn alltaf fluttar inn með pöntuninni. Notkun þessara upplýsinga ræðst hins **Shopify vegar af stillingum** og stillingum fyrirtækisvörpunar í reitnum **Tegund** fyrirtækisvörpunar.|
|**Tegund fyrirtækisvörpunar**|Skilgreina hvernig tengillinn á að gera vörpunina.</br></br>- **Með tölvupósti/síma** ef þú vilt að tengillinn varpar innfluttum Shopify fyrirtækjum á núverandi viðskiptavin í Business Central með tölvupósti og síma frá aðaltengiliði.</br></br>- Taka **alltaf sjálfgefið fyrirtæki** ef kerfið á að nota fyrirtækið í reitnum **Sjálfgefið fyrirtæki nr.** . |
|**Shopify Hægt að uppfæra fyrirtæki**| Þessi reitur er valinn ef tengillinn á að uppfæra viðskiptamennina sem hann finnur þegar valkosturinn **Með tölvupósti/síma** er valinn í reitnum **Tegund** fyrirtækisvörpunar.|
|**Stofna óþekkt fyrirtæki sjálfvirkt**| Þessi reitur er valinn ef tengillinn á að stofna nýja viðskiptamenn þegar valkosturinn **Með tölvupósti/síma** er valinn í reitnum **Tegund** fyrirtækisvörpunar. Nýr viðskiptamaður er stofnaður með innfluttum gögnum og **Kóti** viðskiptamanns/fyrirtækissniðmáts sem skilgreindur er á síðunum **Shopify Vinnusalarspjald** eða **Shopify Sniðmát** viðskiptamanns.|
|**Kóti viðskiptamanns/fyrirtækissniðmáts**|Þessi reitur er notaður með **Sjálfvirk stofnun óþekkts fyrirtækis**.</br></br>- Velja sjálfgefna sniðmátið sem nota á fyrir viðskiptamenn sem hafa verið stofnaðir sjálfvirkt. Ganga þarf úr skugga um að áskildir reitir séu fylltir út í sniðmátinu, svo sem **Alm. viðskiptabókunarflokkur**, **Bókunarflokkur** viðskm., **Virðisaukaskattur (VSK)**- eða aðrir skatttengdir reitir.</br></br>- Þú getur skilgreint sniðmát fyrir hvert land/svæði á síðunni **Shopify Viðskiptamannasniðmát**, sem er gagnleg fyrir réttan skattaútreikning.</br></br>Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|

> [!NOTE]  
> Fyrirtækið verður að hafa aðaltengilið. Annars sleppir tengið við fyrirtæki.
> Aðeins ein elsta birgðageymsla er flutt inn.
> Aðeins aðaltengiliður er fluttur inn.

## <a name="important-settings-when-exporting-b2b-companies-to-shopify"></a>Mikilvægar stillingar þegar B2B-fyrirtæki eru flutt út til Shopify

Hægt er að flytja viðskiptamenn sem fyrir Shopify eru út í magni sem fyrirtæki. Í hverju tilviki eru fyrirtæki og ein sjálfgefin birgðageymsla stofnuð og einn aðaltengiliður. Einnig er hægt að búa til vörulista.

|Svæði|Heimildasamstæða|
|------|-----------|
|**Geta uppfært Shopify fyrirtæki**| Þessi kostur er valinn ef búa á til uppfærslur síðar frá Business Central fyrir fyrirtæki sem þegar eru til í Shopify.|
|**Sjálfgefnar tengiliðaheimildir**| Tilgreina hvaða heimildum verður að úthluta á aðaltengilið, aðeins er hægt að velja milli Ekkert, Panta eingöngu **og** Birgðageymslu stjórnanda **.** **·**|
|**Stofna vörulista sjálfvirkt**| Þessi kostur er gerður virkur ef búa á til vörulista sem inniheldur allar vörur. Vörulisti er stofnaður fyrir hvert útflutt fyrirtæki.|

## <a name="export-b2b-company-to-shopify"></a>Flytja fyrirtækið B2B út í Shopify

### <a name="initial-sync-of-b2b-companies-from-business-central-to-shopify"></a>Upphafleg samstilling B2B fyrirtækja frá Business Central til Shopify

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Shopify Fyrirtæki** og velja viðeigandi tengil.
2. Veljið aðgerðina **Bæta við fyrirtæki** .
3. Sláðu inn kóðann inn í reitinn **Verslunarkóði**. Ef glugginn Fyrirtæki **Shopify er opnaður** af síðunni **Vinnusalarspjald** er vinnusalarkótinn fylltur út sjálfkrafa.
4. Skilgreina afmarkanir á viðskiptavin eins og þörf krefur. Hægt er t.d. að afmarka eftir lands-/svæðiskóta.
5. Velja **Í lagi**.

Fyrirtækið og viðskiptamenn sem verða til eru sjálfkrafa stofnuð í Shopify.

> [!NOTE]  
> Upphafleg samstilling fyrirtækja frá [!INCLUDE[prod_short](../includes/prod_short.md)] til tekur ekki tillit Shopify til **stillinga fyrirtækis Shopify .** 

### <a name="sync-b2b-company"></a>Samstilla B2B-fyrirtæki

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Shopify verslun** og velja síðan viðkomandi tengil.
2. Veldu tiltekna verslun þar sem þú vilt samstilla viðskiptamenn.
3. Veljið aðgerðina **Samstilla fyrirtæki** .

Einnig er hægt að nota aðgerðina **Samstilla fyrirtæki á síðunni** Fyrirtæki **Shopify** eða leita að keyrslunni **Samstilla fyrirtæki** .

Hægt er að tímasetja verkið á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
