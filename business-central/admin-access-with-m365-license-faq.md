---
title: Aðgangur með Microsoft 365 leyfisfjárfyrirmælum
description: Fá svör við algengum spurningum um aðgang að Business Central með Microsoft 365 leyfi.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: faq
ms.date: 09/28/2023
ms.custom: bap-template
---
# Aðgangur með Microsoft 365 leyfisfjárfyrirmælum

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Notendur geta nálgast Business Central gögn þegar Microsoft Teams þeir nota leyfi sitt Microsoft 365 . Þessi grein svarar algengum spurningum frá stjórnendum, ráðgjöfum og öðrum. Forritarar ættu að vísa í algengar spurningar forritara. Fyrir spurningar um samþættingu Business Central við Microsoft Teams er farið í [Teymi algengar spurningar](teams-faq.md).

## [Heimildir](#tab/permissions) 

### Get ég grunnstillt mismunandi upphafsheimildir fyrir mismunandi hópa notenda?

Ekki á þessum tíma. Business Central býður aðeins upp á að stilla einn hóp heimilda sem öllum notendum er úthlutað Microsoft 365 þegar þeir skrá sig inn í Business Central í fyrsta skipti.

### Get ég grunnstillt heimildir, forstillingar og stillingar einstakra notenda áður en þeir skrá sig inn?

Já. Hægt er að ná því í gegnum öryggishópa. Með því að tengja öryggishóp við umhverfi er skilgreint heildarsafn notenda sem hafa aðgang að því umhverfi. Þessi öryggishópur getur innihaldið notendur með Business Central leyfi og notendur með Microsoft 365 leyfi. Þegar notendur á listanum Microsoft 365  **Notendur** eru uppfærðir Microsoft 365 næst verða notandafærslurnar stofnaðar. Síðan er hægt að úthluta notendaflokkum, heimildum, forstillingum og öðrum stillingum áður en þeir hafa skráð sig inn.

### Eftir innskráningu notanda, get ég breytt hvaða hlutum þeir hafa aðgang að?

Já. Eftir að notandi hefur skráð sig inn í fyrsta skipti og notandafærslu þeirra er ráðstafað sjá stjórnendur um þá notendur rétt eins og allir aðrir Business Central-notendur. Þeir geta til dæmis bætt við eða fjarlægt heimildir fyrir mismunandi hluti. Ef heimildarmengunum sem úthlutað er á leyfið Microsoft 365 á síðunni Leyfisskilgreining hefur breytingin aðeins áhrif á næstu notendur sem skrá sig inn í fyrsta skipti.

### Hvernig hindra ég aðgang að viðkvæmum töflum?

Business Central býður upp á öflugt og sveigjanlegt heimildalíkan þar sem stjórnendur geta skilgreint heimildasafn sem veita aðgang að tilteknum hlutum, viðskiptaferlum eða öllum hlutverkum. Til að koma í veg fyrir aðgang að viðkvæmum töflum er hægt að búa til sérsniðin heimildarmeng sem útiloka heimild til viðkvæmra hluta. Nánari upplýsingar um heimildir án heimilda eru [í Create a permission set](ui-define-granular-permissions.md).  

### Í stað þess að sérstilla leyfisskilgreininguna, get ég sérstillt notendahóp?

Já. Ef heimildum Microsoft Teams er bætt við notendaflokk innri notenda í Business Central, hefur það sama nettóáhrif og að bæta heimildum stillt Microsoft 365 á leyfið, svo lengi sem leyfið Microsoft 365 heldur áfram að varpa á þennan notendaflokk. Þessi nálgun hefur þann viðbætta fríðindi sem heimildasafn eru alltaf samstillt við meðlimi hópsins í hvert skipti sem notendahópnum er breytt.

### Þegar Business Central notandi deilir færslu í Teymi veitir hann nýjar heimildir?

Nr. Þessi aðgerð er ekki sú sama og að deila tengli í SharePoint skjal þar sem aðilinn sem deilir skjalinu getur valið að veita öðrum heimild. Í Business Central geta aðeins kerfisstjórar stillt og úthlutað heimildum. Í samanburði við samnýtingu SharePoint skjala er það jafngildi þess að velja kost á að "Deila til fólks með fyrirliggjandi aðgang".

### Styður þessi aðgerð öryggi á línustigi?

Já. Jafnvel þó að einstaklingur sem hefur aðgang að færslu í Teymi með leyfi sitt Microsoft 365 geti haft réttu töfluna og síðuhlutaheimildir verður línustigsheimildum komið á framfæri ef hún hefur verið innleidd fyrir þá töflu.  

### Ef ég grunnstilli heimildir sem innihalda ritaðgang geta notendur skrifað í Teymi?

Ef Business Central er grunnstillt til að úthluta heimildarsafni sem inniheldur innsetningu, breytingu eða eytt aðgangi að einum eða fleiri hlutum geta notendur með viðkomandi heimildarsafn samt ekki skrifað í Teymi þegar þeir hafa Microsoft 365 aðeins leyfi. Business Central þjónustan framfylgir ritvarnum aðgangi sama hvaða innsetningu, breytingu eða heimild er úthlutað.  

Jafnvel þó Business Central veiti þessa vernd mælum við samt með því að þú komist hjá heimildarsamstæðum með ritaðgangi. Ef það er gert kemur það í veg fyrir að mál komi frekar niður á við þegar notendur skipta um hlutverk eða afla sér nýrra leyfia.  

## [Uppsetning og grunnstilling](#tab/setup)

### Hvers vegna er stillingin til að gera aðgang óvirkan fyrir umhverfið mitt?

Virkjun aðgangs með Microsoft 365 leyfi er aðeins í boði fyrir Business Central umhverfi verkvangsútgáfu 21.1 eða síðar. Þegar umhverfið er uppfært í þessa lágmarksútgáfu verður stillingin sjálfkrafa tiltæk. Til að athuga útgáfu umhverfisins er farið á upplýsingasíðu umhverfisins um umhverfið í stjórnunarmiðstöð Business Central. Einnig er hægt að skrá sig inn í umhverfið og fara á **hjálparsíðuna & stuðningur** á **hjálparvalmyndinni** .

### Get ég nálgast Business Central á húsnæði með Microsoft 365 leyfi?

Nei, hún er ekki studd. Business Central birtir villu þegar notendur reyna að fá aðgang að Business Central á húsnæðisfærslum í Teams.

### Hvað er forstilling starfsmanns?

Forstilling **starfsmanns** sem birtist á **listasíðunni Forstillingar (hlutverk)** var kynnt með Uppfæra 21.1. Það er sjálfgefna forstillingin sem er úthlutað á notendur sem fá aðgang að Business Central með leyfi sínu Microsoft 365 . Þessi forstilling er ætluð einstaklingum innan fyrirtækis sem ekki hefur sérstakt hlutverk í Business Central og þarf aðeins að skoða gögn sem var deilt með þeim.

### Hver er notendaflokkur teymisnotendanna?

Hópur **Microsoft Teams innri notenda** sem birtist á síðunni **Notendaflokkar** var kynntur með Uppfæra 21.1. Þessi hópur er sjálfgefinn notendaflokkur sem er tengdur notendum sem fá aðgang að Business Central með leyfi sínu Microsoft 365 . Notendahópurinn er ætlaður fólki innan sömu samtaka þar sem Business Central er hýst sem vinnur með Microsoft Teams.  

### Birtast notendur sem aðeins hafa Microsoft 365 leyfi á notendalistanum í Business Central?

Já. Ef öryggishópar eru notaðir í umhverfi birtast þeir notendur á listanum Notendur eftir að aðgerðin Uppfæra notendur Microsoft 365 hefur verið notuð úr listanum **Notendur** . Ef öryggishópar eru ekki notaðir birtast notendafærslur á listanum Notendur eftir fyrsta skipti sem þær fá aðgang að Business Central færslu.

### Virkar þessi eiginleiki fyrir ígræddar ISV lausnir?

Já. Notendur með aðeins Microsoft 365 leyfi geta einnig fengið aðgang að færslum í umhverfi sem keyra undir léninu *.bc.dynamics.com.

## [Leyfisveitandi](#tab/license)

### Getur viðskiptavinur notað þessa aðgerð ef hann er ekki með Business Central?

Aðgangur að Business Central með Microsoft 365 leyfi er ætlaður fyrir stofnanir sem þegar gerast áskrifandi að Business Central og starfrækja eitt eða fleiri Business Central umhverfi með leyfi frá Business Central notendum. Hann veitir enga nýja virkni eða notar réttindi fyrir Microsoft 365 viðskiptamenn sem eru ekki með Business Central áætlun.

### Hvernig hjálpar þetta mér að stýra áskriftarkostnaði innan fyrirtækisins?

Til að hámarka framleiðni og streyma aðgerðum sínum kaupir Dynamics 365 Business Central SMB oft saman við Microsoft 365. Í því tilviki fá Microsoft 365 flestir leyfi, en aðeins tiltekin hlutverk eða fólk fær Business Central leyfi. Business Central veitir sveigjanleika leyfis þannig að viðskiptavinir greiði aðeins fyrir það sem þeir þurfa:

- Notendum sem þarfnast fulls aðgangs að Business Central er yfirleitt úthlutað Business Central Essentials eða Business Central Premium leyfi. 
- Notendum sem krefjast takmarkaðs skrifaðgangs er yfirleitt úthlutað Meðlimur Business Central Team.
- Allir aðrir starfsmenn innan fyrirtækisins sem þurfa aðeins stundum að lesa viðskiptagögn sem er deilt með þeim, geta gert það ef þeir hafa Microsoft 365 leyfi. Það þarf ekki að úthluta þeim teymisfélagaleyfi. Aðrir leyfisvalkostir eru í boði. Nánari upplýsingar má finna í handbókinni [Dynamics](https://go.microsoft.com/fwlink/?LinkId=866544) 365 um leyfisveitingar og nánari upplýsingar.

### Er þetta 100% án endurgjalds?
 
Nr. Aðgangur að Business Central gögnum í Microsoft Teams krefst þess að hver notandi fái annaðhvort Business Central leyfi eða Microsoft 365 leyfi af listanum yfir studdar áætlanir.

### Virkar þetta með Microsoft 365 prufur og Business Central réttarhöld?

Já. Ef notandi fær Microsoft 365 leyfi frá prufuútgáfu af studdri áætlun getur hann einnig fengið aðgang að Business Central færslum í Teams. Þá er mögulegt fyrir viðskiptamenn að prófa framleiðni og viðskiptaforrit Microsoft sem vinna saman og gera sölumönnum og ráðgjöfum samstarfsaðila kleift að sýna þessa aðgerð auðveldlega. Til dæmis geta samstarfsaðilar ráðstafað eigin Microsoft Entra leigjendum sem [https://aka.ms/CDX](https://aka.ms/CDX) innihalda Microsoft 365 prufur og Business Central réttarhöld til að sýna Business Central.

### Listi yfir leyfi í Business Central sýnir Microsoft 365 leyfi. Hvað er þetta?

Síðan **Leyfisskilgreining** í Business Central birtir mismunandi gerðir af leyfi sem veitir aðgang að Business Central þjónustunni. Í útgáfu 21 bætti Microsoft 365 Microsoft við þennan lista sem nýja leið til að fá aðgang að Business Central. Þessi listi yfir leyfi gefur ekki í skyn að fyrirtækið hafi keypt áskrift að einhverju af þessum leyfum eða fyrirtækið hefur veitt aðgang að þessum leyfum.

### Þarf ég að fá nýja tegund af Microsoft 365 leyfi fyrir þessa aðgerð til að vinna?  

Microsoft hefur ekki búið til ný leyfi eða nýjar áætlanir til að knýja þessa aðgerð. Þessi aðgerð tengist eingöngu fyrirliggjandi Microsoft 365 áætlunum og leyfum. Ef þú ert þegar áskrifandi að einni af studdu Microsoft 365 áætlununum þá hefur þú þegar þessa nýju notkun rétta. Annars, ef þú gerast ekki áskrifandi að Microsoft 365 dagnum í dag getur þú skráð þig hér á Microsoft 365 slóð viðskiptaiðgjalds eða svipaðra áætlana. 

### Hvernig kemst ég að því hvaða notendur hafa aðeins Microsoft 365 leyfi?

Það eru margar leiðir.  Microsoft 365 Í stjórnunarstöðinni er farið á **listann Virkir notendur** og vísað í dálkinn **Leyfi** . Í Business Central er farið á **notendalistann**, einhver af notendunum valinn og skoðað **upplýsingakassann** Leyfi.  

### Hvernig afmarka ég notendalistann í Business Central til að sjá notendur sem hafa aðeins Microsoft 365 leyfi?

Ekki er hægt að nota afmörkunar- eða listayfirlit á þessu verki. Hins vegar er hægt að velja notanda á listanum og skoða leyfisreitinn sem nær aðeins Microsoft 365 til, ef notandinn hefur Microsoft 365 aðeins leyfi.

### Hvað með notendur sem hafa bæði Microsoft 365 leyfi og Business Central leyfi?

Þegar mörgum leyfum er úthlutað á notanda, vinna meiri leyfisnotkunarheimildir yfir minni notkunarheimildum þegar farið er í Business Central. Í þessu tilviki á Business Central leyfi notandanum að fá meiri notandaréttindi. Þannig geta notendur lesið og skrifað Business Central færslur í Teams og opnað Business Central vefbiðlarann í vafranum, rétt eins og allir aðrir Business Central leyfishafar. Ef tiltekin heimildarsamsetning hefur verið grunnstillt fyrir Microsoft 365 leyfið fær notandinn grunnstillt heimildasafn ásamt heimildarmengunum úr Business Central leyfinu eða sem þegar hefur verið úthlutað til notandans.

### Er þessi leyfisveiting tengd meðlimur Business Central Team?

Engin tengsl eru á milli leyfis business Central Team og aðgangs að Business Central með Microsoft Teams  Microsoft 365 leyfi. Þó svo Microsoft Teams að heimildir þess vísa til fólks í teymi sem *teymismeðlimi* er það sameiginlegt hugtak fyrir hóp Microsoft Teams notenda. Það vísar ekki til Business Central leyfis.

### Framfylgir Business Central einhverjum hömlunum?

Já, allar hömlur á verkvangnum og lágmarkskröfur, þ.m.t. leyfisskilyrði, er framfylgt af Business Central verkvangnum. Með þessu eru notendur með tiltekin villuboð til að aðstoða þá við að ræða uppsetningu þeirra og koma í veg fyrir misnotkun. Ef notandi sem hefur aðeins Microsoft 365 leyfistilraunir til að fá aðgang að Business Central vefbiðlara í vafranum er aðgangi hafnað og villuboð birtast leiðsagnarforrit. 

## [Notkun](#tab/usage)
 
### Get ég fengið aðgang að færslum í Teymi fyrir iOS og Teymi fyrir Android? 

Eins og er er ekki hægt að fá aðgang að Business Central gögnum í teymunum fyrir farsíma með því að nota aðeins Microsoft 365 leyfi. Microsoft vinnur að því að gera þennan möguleika virkan bráðlega. 

### Hvernig breyta notendur persónulegum stillingum sínum í Mínar stillingar? 

Þegar notandi fer inn á Business Central í fyrsta skipti notar aðeins leyfi sitt Microsoft 365 eru notendastillingar þeirra, svo sem tungumál, tímasvæði og svæðisstillingar stilltar sjálfkrafa á grundvelli stýrikerfis eða vafrastillinga. Kerfisstjórar geta breytt þessum stillingum í Business Central fyrir hvern notanda. 

### Hvað ræður vali á tungumáli þegar notandi skráir sig inn í fyrsta skipti? 

Tungumálið sem Business Central er notað á er byggt á ýmsum þáttum, þar á meðal teams biðlaranum sem þú náðir í í Business Central í fyrsta skipti. Fyrir teymisforrit, Teymi fyrir iOS og Teymi fyrir Android er tungumál stýrikerfisins notað. Fyrir teymi á vefnum er vaframálið notað. Í öllum tilvikum er tungumálið Teymi ekki talið. 

### Af hverju get ég ekki virkjað nokkra af lituðu tenglunum í flipum og kortaupplýsingum?

Aðgerðanlegir tenglar á Business Central síðum eru oft sýndir sem feitletraðar tenglar sem hægt er að virkja til að fara annars staðar eða keyra einhverja aðgerð. Á tæknilegu stigi eru þessir tenglar yfirleitt innleiddir sem reitagildi sem hafa enga fyrirsögn sem kallar fram einhvern kóta og þar sem val á stíl endurspeglar oft stöðu. Þegar notendur fá aðgang að Business Central síðum með leyfi sínu Microsoft 365 eru tenglarnir stílaðir eins og þeir séu aðgerðalausir. En ekki er hægt að virkja þá vegna þess að þetta leyfi býður ekki upp á notkunarheimildir til að keyra aðgerðir.  

### Hvers vegna get ég ekki virkjað tilkynningaaðgerðir á síðunni?

Samhengistilkynningar sem birtast á síðum fylgja oft aðgerðanlegum tenglum. Þegar notendur fá aðgang að Business Central síðum með leyfi sínu Microsoft 365 eru þessir tenglar birtir en ekki hægt að virkja þar sem þetta leyfi býður ekki upp á notkunarheimildir til að keyra aðgerðir. Á tæknilegu stigi eru þessir tenglar innleiddir sem aðgerðir.

### Geta Microsoft 365 notendur fjarlægt flipa?

Já. Allir í spjallinu eða rásinni geta fjarlægt flipa sem aðrir búa til. Fjarlæging flipa fjarlægir ekki eða hefur áhrif á gögn í Business Central en flipinn verður fjarlægður fyrir alla notendur á spjallinu eða rásinni.

### Ef ég get ekki afmarkað, sé ég samt afmarkaðan lista sem var búinn til af öðrum?

Notendur sem fá aðgang að Business Central með leyfi sínu Microsoft 365 hafa ekki notkunarheimildir til að afmarka með því að nota afmörkunarsvæðið eða nota listayfirlit. En ef annar notandi hefur stofnað flipa með afmarkaðri listasíðu Microsoft 365  mun notendur einnig skoða þær afmarkanir sem notaðar eru á flipann.

---

## Sjá einnig .

[Yfirlit yfir Business Central Access með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365-leyfum](admin-access-with-m365-license-setup.md)  