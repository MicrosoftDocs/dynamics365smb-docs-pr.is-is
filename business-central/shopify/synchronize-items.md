---
title: Samstilla vörur og birgðir
description: Setja upp og keyra samstillingar á milli atriða milli Shopify -og Viðskiptamiðis
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30116, 30117, 30126, 30127,
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 2c54b24a38be055fb8f6e641761130e6eab8b829
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361610"
---
# <a name="synchronize-items-and-inventory"></a>Samstilla vörur og birgðir

**Vörurnar** í [!INCLUDE[prod_short](../includes/prod_short.md)] eru sambærilegar þeim sem *Vara* í Shopify og innihalda efnislegar vörur, stafrænt niðurhal, þjónustu og gjafakort sem selja má. Tvær meginástæður eru til að samstilla atriðin:

1. Gagnastjórnun er fyrst og fremst framkvæmd í [!INCLUDE[prod_short](../includes/prod_short.md)]. Þú þarft að flytja öll eða einhver gögn þaðan inn Shopify og gera það sýnilegt. Hægt er að flytja út Vöruheiti, lýsingu, mynd, verð, ráðstöfunarmagn, afbrigði, Lánardrottnaupplýsingar og strikamerki. Þegar flutt er út, er hægt að fara yfir vörurnar eða hafa þær gerðar sýnilegar strax.
2. Þegar pöntun Shopify sem flutt er inn er upplýsingar um atriði er mikilvægt að frekari Skjalavinnsla sé í [!INCLUDE[prod_short](../includes/prod_short.md)].

Undanfarandi tvær aðstæður eru ávallt virkjaðar.

Þriðja dæmi er að hafa umsjón með gögnum Shopify en flytja þau inn í fjöldagerð [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi atburðarás getur verið gagnleg fyrir atvik í flutningi, eins og þegar óskað er eftir að tengja fyrirliggjandi vefverslun við nýtt [!INCLUDE[prod_short](../includes/prod_short.md)] umhverfi.

## <a name="define-item-synchronizations"></a>Skilgreina vörusamstillingar

1. Veldu leitarljósasermið ![sem opnar aðgerðina segja mér upp.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teig og slá **Shopify búð**. Opna verkstæðið sem skilgreina á samstillingu vöru fyrir.
2. **Velja þarf valkostinn úr reitnum sync-vara**.<br>Eftirfarandi tafla lýsir valkostunum.

|Valkostur|Lýsing|
|------|-----------|
|**Autt**| Afurðir eru fluttar inn ásamt innflutningi skipanna. Afurðir eru fluttar út til Shopify ef notandi keyrir **aðgerðina bæta við vöru** af **Shopify síðunni vörur**. Þetta er sjálfgefið ferli.|
|**Að Shopify**| Þessi kostur er valinn ef eftir að **aðgerðinni bæta við vöru** er ætlunin að uppfæra afurðir handvirkt **með samstillingu afurðaaðgerða** eða með því að nota vinnslubiðröð fyrir endurteknar uppfærslur. Munið að gera **hægt að uppfæra Shopify afurðakvöldin**. Ef hún er ekki virkjuð jafngildir **valkosturinn auður** (sjálfgefinn ferli). Frekari upplýsingar í [kaflanum útflutningsvörur Shopify](synchronize-items.md#export-items-to-shopify).|
|**Frá Shopify**| Þessi kostur er valinn ef ætlunin er að flytja afurðir úr Shopify í magni, annað hvort handvirkt með **aðgerðinni samkeyrsluvörur** eða með því að nota vinnslubiðröð fyrir endurteknar uppfærslur. Frekari upplýsingar í [innflutningsatriðum úr Shopify](synchronize-items.md#import-items-from-shopify) kafla.|

## <a name="import-items-from-shopify"></a>Flytja inn vörur úr Shopify

Fyrst þarf að flytja inn vörur annaðhvort í fjöldaúr Shopify eða ásamt pöntunum til að bæta þeim við **Shopify töflurnar afurð** og **Shopify afbrigði**. Þá varpa innfluttar vörur og afbrigði á vörur og afbrigði í [! INCLUDEprod_short]. Stjórna ferlinu með eftirfarandi stillingum:

|Svæði|Lýsing|
|------|-----------|
|**Sjálfvirk stofnun óþekktra atriða**|Þegar Shopify afurðir og vöruvíddasamsetningar eru fluttar inn [!INCLUDE[prod_short](../includes/prod_short.md)][!INCLUDE[prod_short](../includes/prod_short.md)] reynir fyrst að finna jöfnunarfærsluna á listanum. **Birgðafrávörpun** hefur áhrif á hvernig jöfnun er framkvæmd og stofnar nýja vöru og/eða vöruafbrigði. Gera þennan valkost virkan ef stofna á nýja vöru eða þegar samsvarandi færsla er ekki til. Nýja varan er stofnuð með innfluttu gögnunum og **Sniðmátskótanum**. Ef þessi valkostur er ekki virkjaður þarf að stofna vöru handvirkt og nota **aðgerðina vörpun vöru** á **Shopify vörum á síðunni vörur**.|
|**Kóði vörusniðmáts**|Notið þetta með því að skipta um óþekkt atriði **á** sjálfvirka stofna.<br>Sniðmátið sem á að nota fyrir sjálfvirkt stofnaða vöru er valið.|
|**SKR Kortvörpun**|Veldu hvernig þú vilt nota Be **-gildið sem flutt er** inn frá Shopify meðan á vörpun vöru/afbrigðis og stofnunar stendur. [Frekari upplýsingar um áhrif Shopify vörunar og strikamerkjum á vörpun og myndun vara og afbrigða í miðlægum](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) kafla viðskipta.|
|**Aðkoma að svæði SKÚLAGÖTU**|Notið þetta með **be-vörpun** sem stillt er **á vöruna. Nei + afbrigði (synchronize-items.md#effect-shopify-vara-skus-og-barkóðar-on-vörpun-og-stofna-vara-og-vöruafbrigði-í-** <br> Skilgreinið skiltákn sem á að nota til að skipta skr.<br>Ef Shopify afbrigðið er stofnað með be ' 1000/001 ' ' er ritað '/' í **aðskilakreitasvæði** til að gera vörunúmerið í [!INCLUDE[prod_short](../includes/prod_short.md)] ' 1000 ' og vöruafbrigðakótanum ' 001 '.|
|**Forskeyti afbrigðis**|Notið saman með **be-vörpun** sem er stillt á annaðhvort **afbrigðiskótann** eða **Vörunr. valkosturinn vöruvíddakóði** sem varaaðgerð þegar birgðahaldseining Shopify er auð.<br>Ef stofna á Vöruafbrigðið [!INCLUDE[prod_short](../includes/prod_short.md)] sjálfvirkt þarf að færa inn gildi í **kóða**. Sjálfgefið er að gildið sem er skilgreint í be-svæðinu sem flutt er inn úr Shopify er notað. Ef be er hins vegar autt býr hún til kóða sem er ræstur með skilgreindu forskeytinu afbrigði og "001".|
|**Shopify Hægt að uppfæra vöru**|Þessi kostur er valinn ef uppfæra á vörur og/eða vöruvíddasamsetningar sjálfvirkt.|

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Shopify Áhrif Vöruskimana og strikamerkjum á vörpun og myndun vara og afbrigða í Viðskiptamiðinu

Þegar afurðir eru fluttar inn úr Shopify töflunum yfir í **Shopify vöruvíddasamsetningar** **Shopify** er [!INCLUDE[prod_short](../includes/prod_short.md)] reynt að finna tiltækar færslur.

Eftirfarandi tafla gerir grein fyrir muninum á valkostum í **reitnum skr. vörpun**.

|Valkostur|Áhrif á kortlagningu|Áhrif á sköpun|
|------|-----------------|------------------|
|**Autt**|BIRGÐAHALDSEINING er ekki notuð í venja við vörpun vöru.|Engin áhrif á stofnun vörunnar.<br>Þessi valkostur hindrar stofnun vöruvíddasamsetningar. Þegar í sölupöntun er aðeins aðalvaran notuð. Enn er hægt að varpa afbrigði handvirkt á **Shopify síðuna afurð**.|
|**Vörunr.**|Veljið hvort be-svæðið innihaldi vörunúmerið|Engin áhrif á stofnun vöru án afbrigða. Fyrir vöru með vöruvíddasamsetningar er hvert afbrigði stofnað sem aðskilin vara.<br>Þannig að ef Shopify er með vöru með tveimur vöruvíddasamsetningar og SKUs eru ' 1000 ' og ' 2000 ', [!INCLUDE[prod_short](../includes/prod_short.md)] munu tvö atriði tölusetja ' 1000 ' og ' 2000 '.|
|**Afbrigðiskóði**|BIRGÐAHALDSEINING er ekki notuð í venja við vörpun vöru.|Engin áhrif á stofnun vörunnar. Þegar vöruafbrigði er stofnað, er gildið í be-svæðinu notað sem kóti. Ef be er autt er Kóði myndaður með því að **nota Forskeytisvæðið** afbrigði.|
|**Vörunr. + Afbrigðiskóti**|Veljið þetta ef reiturinn be inniheldur vörunúmer og afbrigðiskótinn er aðskilinn frá gildinu sem tilgreint er í **Aðgreiningarsvæði** skreita.|Þegar vara er stofnuð er fyrsti hluti gildis í be-reit merktur **Nr.** Ef be-svæðið er autt er vörunúmer myndað með því að skilgreint er í númeraröðinni sem er **skilgreind í Sniðmátskóði** eða **Vörunr.** á **birgðauppsetningarsíðunni**.<br>Þegar vara er stofnuð notar afbrigðið seinni hluta af gildi be-reitsins sem **kóða**. Ef be-svæðið er autt er Kóði myndaður með því að **nota Forskeytisvæðið** afbrigði.|
|**Vörunr.**|Velja hvort be-svæðið innihaldi vörunúmer lánardrottins. Í þessu tilfelli **er Vörunr. lánardr.** ekki notað á **síðunni birgðaspjald** ; frekar lánardrottininn **Vörunr.** **í vörulista** lánardrottins er notað. Ef kóti fyrir fundaskrá *lánardrottins* inniheldur afbrigðiskóta er kótinn notaður til að varpa Shopify afbrigðinu.|Ef samsvarandi lánardrottinn er til staðar [!INCLUDE[prod_short](../includes/prod_short.md)] mun be-gildið verða notað sem **Vörunr lánardrottins** á **birgðaspjaldinu** og sem **vörutilvísun** í gerð lánardrottins. <br>Hindrar stofnun vöruvíddasamsetningar. Það er gagnlegt þegar á að nota aðalatriðið í sölupöntuninni. Enn er hægt að kortleggja afbrigði handvirkt frá **Shopify afurðasíðunni**.|
|**Strikamerki**|Velja hvort be-svæðið innihaldi strikamerki. Leit er framkvæmd meðal **Vörutilvísana** af gerðinni lánardrottinn. Ef færsla í fann vörutilvísanaskrá inniheldur afbrigðiskóta er afbrigðiskótinn notaður til að varpa Shopify afbrigðinu.|Engin áhrif á stofnun vörunnar. <br>Hindrar stofnun vöruvíddasamsetningar. Það er gagnlegt þegar á að nota aðalatriðið í sölupöntuninni. Enn er hægt að kortleggja afbrigði handvirkt frá **Shopify afurðasíðunni**.|

Eftirfarandi tafla lýsir áhrifum **reitsins strikamerskóti**.

|Áhrif á kortlagningu|Áhrif á sköpun|
|-----------------|------------------|
|Leit fer fram á **vörutilvísunum** sem innihalda gerð strikamerskóta sem gildið í **reitnum strikamerki** í Shopify. Ef færsla í fann vörutilvísanaskrá inniheldur afbrigðiskóta er afbrigðiskótinn notaður til að varpa Shopify afbrigðinu.|Strikamerkóðið er vistað sem **vörutilvísun** fyrir vöruna og Vöruafbrigðið.|

> [!NOTE]  
> Hægt er að kveikja á vörpun valinna afurða/vöruvíddasamsetningar **með því að velja** reyna finna vörpun afurða eða allar innfluttar ókortlagðar afurðir með því að velja **reyna svörvarpanir**.

## <a name="export-items-to-shopify"></a>Flytja út vörur á Shopify

Velja einingarnar úr vörulistanum sem á að flytja út í Shopify. Nota skal **aðgerðina bæta við vöru** á **Shopify síðunni vörur** til að bæta vörum við Shopify lista yfir vörur.

Þú stjórnar ferlinu við útflutning á vörum með þessum stillingum:

|Svæði|Lýsing|
|------|-----------|
|**Verðflokkur viðskiptamanns**|Ákvarða verð fyrir vöru í Shopify. Söluverð þessa verðflokks viðskiptamanns er tekið. Ef enginn flokkur er færður inn er notað verð á birgðaspjaldinu.|
|**Afsláttarflokkur viðskiptamanns**|Ákvarða afsláttinn sem á að nota við útreikning verðs á vöru í Shopify. Afsláttur er ekki geymdur í **verðsvæðinu** og fullt verð er geymt á **svæðinu bera saman við verð**.|
|**Samstilling lengdrar texta samkeyrslu**|Veljið þetta til að samstilla lengdan texta vörunnar. Þar sem því verður *við komið í lýsingarreitinn* getur það innihaldið HTML-kóða. |
|**Eigindir samkeyrslu atriðis**|Veljið þetta til að samstilla eigindir atriðis. Eigindi eru sniðin sem tafla og innifalin í *lýsingarreitnum* í Shopify.|
|**Tungumálskóða**|Veljið þetta ef óskað er eftir þýddum útgáfum sem notaðar eru fyrir titil, eigindir og lengdan texta.|
|**SKR Kortvörpun**|Veljið hvernig á að fylla út skreitan reit í Shopify. Stuðningsvalkostir eru:<br> - **Vörunr.** til að nota Vörunr. fyrir bæði afurðir og vöruvíddasamsetningar.<br> - **Vörunr. + Afbrigðiskóti** til að búa til birgðaskrá með samtengingar-gildi tveggja svæða. Vörunúmerin eru aðeins notuð fyrir vörur án vöruvíddasamsetningar.<br>- **Vörunr.** til að nota lánardrottinsnúmer sem tilgreint er *á birgðaspjaldi* fyrir bæði afurðir og vöruvíddasamsetningar.<br> - **Strikamerki** til að nota strikamerkógerðargerð **Vörutilvísunarinnar**. Þessi valkostur virðir afbrigði.|
|**Aðkoma að svæði SKÚLAGÖTU**|Skilgreinið skiltákn fyrir **vöruna. Nei + Afbrigðiskóti** valkostur.|
|**Birgðastöðvar raktar**| Velja hvernig kerfið á að fylla út reitinn rekja birgðir **fyrir afurðir sem fluttar eru** út í Shopify. Hægt er að uppfæra ráðstöfunarupplýsingar úr [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir afurðir þar Shopify sem birgðahald er virkjað. Frekari upplýsingar í [hlutanum Birgðir](synchronize-items.md#sync-inventory-to-shopify).|
|**Sjálfgefin Birgðastefna**|Velja *afnot* til að koma í veg fyrir neikvæða birgðir á Shopify hliðinni.|
|**Hægt að uppfæra Shopify afurðir**|Skilgreinið þetta ef [!INCLUDE[prod_short](../includes/prod_short.md)] Aðeins má stofna vörur eða geta uppfært vörur einnig. Þessi kostur er valinn ef eftir að aðgerðinni bæta við vöru **er** ætlunin að uppfæra handvirkt afurðir með því **að nota samstillingarvöruaðgerðina** eða nota vinnslubiðröð fyrir endurteknar uppfærslur. Munið að velja **Shopify** **í svæðið vara samkv**.|
|**Sniðmátskóti viðskiptamanns**|Velja sjálfgefið sniðmát sem á að nota við verðútreikninga. Læra meira at [Setja upp skatta](setup-taxes.md).|

### <a name="fields-mapping-overview"></a>Yfirlit yfir vörpun svæða

|Shopify|Uppspretta þegar flutt er út úr[!INCLUDE[prod_short](../includes/prod_short.md)]|Mark þegar flutt var inn til[!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Staða|**Samkvæmt reitnum Staða fyrir stofnaðar afurðir** í **Shopify verkstæðisspjaldinu**. Frekari upplýsingar í tilfallandi uppfærslum [á vörum Shopify í](synchronize-items.md#ad-hoc-updates-of-shopify-products) kaflanum.|Ekki notaður.|
|Titill | **Lýsingu**. Ef Tungumálskótinn er skilgreindur og samsvarandi þýðing á vöru er til verður vöruþýðing notuð í stað lýsingar.|**Lýsing**|
|Lýsing|Sameinar lengda texta og eiginleika ef samsvarandi víxlar á Shopify verkstæðisspjaldinu eru virkjaðir. Virðir tungumálskóða.|Ekki notaður.|
|Titilsíða titils|Fast gildi: auð. Frekari upplýsingar í tilfallandi uppfærslum [á vörum Shopify í](synchronize-items.md#ad-hoc-updates-of-shopify-products) kaflanum.|Ekki notaður.|
|SEO meta Lýsing|Fast gildi: auð. Frekari upplýsingar í tilfallandi uppfærslum [á vörum Shopify í](synchronize-items.md#ad-hoc-updates-of-shopify-products) kaflanum.|Ekki notaður.|
|Geymslumiðill|**Ímynd**. Frekari upplýsingar er [að fá í kaflanum Samkeyrsla atriðis mynda](synchronize-items.md#sync-item-images)|**Mynd**|
|Verð|Útreikningur á verði í lok-Viðskiptamaður inniheldur vöruverðsflokk, vöruafsláttarflokk, gjaldmiðilskóða og sniðmátskóta viðskiptamanns.|**Einingaverð**|
|Bera saman á verðlagi|Útreikningur á verðinu án afsláttar inniheldur vöruverðsflokk, vöruafsláttarflokk, gjaldmiðilskóða og sniðmátskóta viðskiptamanns.|Ekki notaður.|
|Kostnaður á vöru|**Kostnaðarverð**|**Kostnaðarverð**|
|BHE|Nánar um þetta undir **Skýrr Kortvörpun** í [útflutningsgreinum Shopify](synchronize-items.md#export-items-to-shopify) í kafla.|Fræðast um þetta í hvaða [áhrif Shopify Vöruskus og barkóðar eiga að varpa og búa til vörur og afbrigði í miðlægum](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) kafla viðskipta.|
|Strikamerki|**Vörutilvísanir** af gerðinni strikamerskóti.|**Vörutilvísanir** af gerðinni strikamerskóti.|
|Rekja magn|**Samkvæmt reitnum birgðatraki** á **Shopify síðunni verkstæðiskort**. Frekari upplýsingar í [hlutanum Birgðir](synchronize-items.md#sync-inventory-to-shopify).|Ekki notaður.|
|Halda áfram að selja þegar út af hlutabréfum|**Samkvæmt sjálfgefinni Birgðastefnu** í **Shopify verkstæðisspjaldinu**. Ekki flutt inn.|Ekki notaður.|
|Gerð|**Lýsing** á **tegundakóða vörunnar**. Ef tegundin er ekki tilgreind í Shopify er henni bætt við sem sérsniðna gerð.|**Kóði** vöruflokks. Kortlagning eftir lýsingu.|
|Lánardrottinn|**Nafn** lánardrottins úr **Lánardr.**|**Nr.** lánardrottins Vörpun eftir nafni.|
|Þyngd|**Brúttóþyngd**.|Ekki notaður.|
|Skattskylt|Fast gildi: virkjað.|Ekki notaður.|
|Skattkóðar|**Kóta** skattflokks. Á aðeins við um virðisaukaskatt. Læra meira at [Setja upp skatta](setup-taxes.md).|Ekki notaður.|

### <a name="tags"></a>Efnisorð notenda

Skoðið innfluttu merkin í **upplýsingakassa á merkjum** á **Shopify vörusíðunni**. Á sömu síðu, til að breyta seðlum, skaltu velja **Tags** aðgerð.
**Ef valkosturinn til að Shopify** Velja í **reitnum sync vara** er úthlutað merkjum sem eru flutt út Shopify í við næstu samstillingu.

## <a name="run-item-synchronization"></a>Keyra samstillingu vöru

Samstilling vöru í fullri eða hluta getur farið fram á marga mismunandi vegu.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Upphaflega Samkeyrsla á vörum frá Viðskiptamiðinu til Shopify

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. **Veljið aðgerðina bæta við vörum**.
3. **Kótinn er færður í reitinn verkstæðiskóti**. Ef glugginn vara **Shopify er opnaður** á **verkstæðissíðunni** verður verkstæðiskóðinn sjálfkrafa fylltur út.
4. Skilgreinið afmarkanir á vörur eftir þörfum. Til dæmis er hægt að afmarka eftir reitnum Vörunr. eða vörutegundakóða.
5. Velja **Í lagi**.

Vörurnar sem koma fram eru sjálfkrafa stofnaðar í Shopify með verði en myndir og birgðastig eru ekki teknar með. Aðgerðin gæti tekið nokkurn tíma ef mikill fjöldi atriða bætist við.

### <a name="sync-products-from-shopify-to-business-central"></a>Samkeyrsla afurða frá Shopify til Aðalstarfsemi

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem á að samstilla vörur til að opna **Shopify spjald** -síðu verkstæðis.
3. Velja skal **aðgerðina samstilla vörur**.

Einnig er hægt að **nota aðgerðina sync afurðir** á **Shopify vörum** á síðunni eða leita að **keyrslunni samkeyrsluvörur**.

Áætla má að verkefnið sé framkvæmt með sjálfvirkum hætti. Frekari upplýsingar um [tímasetningu endurtekinna verka](background.md#to-schedule-recurring-tasks).

### <a name="ad-hoc-updates-of-shopify-products"></a>Tilfallandi uppfærslur á Shopify afurðum

Þegar færslurnar eru uppfærðar í **Shopify vörutöflunni** eru eftirfarandi breytingar samstilltar með Shopify.

Uppfæra

* **Staða** -hægt er að velja á milli virkra, safnvista eða uppkvaðna.
* **SEO titill**
* **SEO Lýsing**

Eyðingu

Þegar gildinu í **aðgerðinni er eytt á spjaldinu** verkstæðisaðgerð **Shopify** er afurðin uppfærð í Shopify þegar færslunni er eytt af **Shopify síðunni vörur**.

* **Auður** -Ekkert mun gerast. Ef þörf krefur þarf að framkvæma aðgerðina **Shopify sem er nauðsynleg í admin**.
* **Staða til uppkvaðingar** -Staða afurðar í Shopify er stillt á *drög*.
* **Staða í skjalasafni** -varan er skjöluð í Shopify.

## <a name="sync-item-images"></a>Samstilla vörumyndir

Samstillingu mynda er hægt að skilgreina fyrir samstilltar vörur. Velja skal úr eftirfarandi:

* **Auður** -samstilling mynda er óvirk.
* **Til Shopify** -myndir af vörum eru fluttar út í Shopify.
* **Úr Shopify** -myndir frá Shopify eru fluttar inn [!INCLUDE[prod_short](../includes/prod_short.md)] kl.

Hægt er að frumstilla samstillingu mynda á þeim tveimur leiðum sem lýst er hér að neðan.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Samstilla myndir af vöru frá Shopify búð-síðunni

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu tengdan tengil.
2. Veldu verkstæðið sem á að samstilla myndir við til að opna **Shopify spjald-síðu vinnukorts**.
3. Velja skal **aðgerðina samstilla Afurðarmyndir**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Samkeyra myndir af vörum frá Shopify síðunni vörur

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. Velja skal **aðgerðina samstilla Afurðarmyndir**.

### <a name="image-synchronization-remarks"></a>Athugasemd samstillingu mynda

* Við útflutning mynda frá [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, að nýjum myndum sé bætt við Shopify, halda Gamlar myndir ósnortinn. Ef mynd er uppfærð í [!INCLUDE[prod_short](../includes/prod_short.md)] er nauðsynlegt að eyða gömlum myndum í **Shopify admin**.
* Myndir fluttar út til Shopify að ekki sé samræmi í kröfum sem skilgreindar eru samkvæmt Shopify verða ekki fluttar inn. Frekari upplýsingar í [vörumiðilsgerðum á help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Samkeyrsla verði með Shopify

Hægt er að flytja verð til samstilltra vara á þeim tveimur leiðum sem lýst er hér á eftir.

### <a name="sync-prices-from-the-shopify-products-page"></a>Sync verð frá Shopify vörum síðunni

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. Samstilla verð er **valið í Shopify** aðgerð.

### <a name="price-calculation-remarks"></a>Athugasemdir við verðútreikning

* Fyrir verðútreikninga er mikilvægt að hafa gildið í **reitnum sjálfgefið Viðskiptamannssniðmát**. Læra meira at [Setja upp skatta](setup-taxes.md).
* **Færið inn gjaldmiðilskóða** ef vefverslunin notar annan gjaldmiðil en staðbundinn GJALDMIÐIL (ISK). Tilgreindur Gjaldmiðill verður að hafa gengi skilgreint. Ef vefverslunin notar sama gjaldmiðil og [!INCLUDE[prod_short](../includes/prod_short.md)] er reiturinn hafður auður.
* Þegar ákvarðað er verð, [!INCLUDE[prod_short](../includes/prod_short.md)] notar "Lægsta verð" rökin. Það þýðir að ef skilgreint einingarverð á birgðaspjaldinu er lægra en það sem er skilgreint í verðflokknum, er einingarverð frá birgðaspjaldi notað.

## <a name="sync-inventory-to-shopify"></a>Samstilla birgðir til Shopify

Samstillingu birgða er hægt að skilgreina fyrir þegar samstilltar vörur. Um tvö skilyrði er að ræða sem þarf að uppfylla:

1. Birgðakælingar verða að vera virkjaðar fyrir afurð í Shopify. Ef vörur eru fluttar út til Shopify skal hafa í **huga virkjun birgðatrakanna** á **Shopify verkstæðissíðunni**. Frekari upplýsingar í [kaflanum útflutningsvörur Shopify](synchronize-items.md#export-items-to-shopify).
2. Samstilling birgða verður að vera virk fyrir **Shopify staðsetningar**.

### <a name="to-enable-inventory-sync"></a>Til að virkja samstillingu birgða

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem samstilla á birgðabirgðir til að opna **Shopify síðuna Verkstæðisspjald**.
3. **Veldu staðsetningar** aðgerða til að opna **Shopify verkstæðisstaði**.
4. **Velja aðgerðina Sækja Shopify staðsetningar** til að flytja inn alla staði sem skilgreindir eru í Shopify. Þær má finna í [**stillingum staðsetningar**](https://www.shopify.com/admin/settings/locations) í **Shopify admin**.
5. **Í reitnum Birgðageymsluafmörkun** er hægt að bæta við birgðageymslum ef taka á með birgðir frá tilteknum birgðageymslum. Svo mætti slá *Austur | Vestur* til að gera birgðir frá einungis þessum tveimur stöðum sem eru til sölu í gegnum vefverslunina.
6. Hafna því að skipta um **óvirka** til að virkja samstillingu birgða á völdum Shopify stöðum.

Hægt er að frumstilla samstillingu birgða á þeim tveimur leiðum sem lýst er hér að neðan.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Samstilla birgðir úr Shopify verkstæðissíðunni

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu tengdan tengil.
2. Veljið verslunina þar sem samstilla á birgðabirgðir til að opna **Shopify síðuna Verkstæðisspjald**.
3. **Veljið samstillingarbirgðaaðgerðina**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Samstilla birgðir af Shopify vörum síðunni

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. **Veljið samstillingarbirgðaaðgerðina**.

### <a name="inventory-remarks"></a>Athugasemdir birgða

* Tengið reiknar **út áætlaða stöðu** í boði og flytur hana út Shopify.
* Hægt er að skoða birgðaupplýsingar sem mótteknar Shopify eru í á **Shopify síðunni Birgðaupplýsingakassi**. Í þessum upplýsingakassa fæst yfirlit yfir Shopify Birgðir og síðast reiknaðar birgðir í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það er ein færsla á stað.
* Ef upplýsingar um hlutabréf í Shopify er annað en **Áætluð staða** í boði í [!INCLUDE[prod_short](../includes/prod_short.md)], þá uppfærist Hlutabréfakaup í Shopify.

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
