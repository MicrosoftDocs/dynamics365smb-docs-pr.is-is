---
title: Samstilla vörur og birgðir
description: Setja upp og keyra samstillingar á milli atriða milli Shopify -og Viðskiptamiðis
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: fac1a3df12070a2030d6d2d8dfd5e740d8cca4f9
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768098"
---
# <a name="synchronize-items-and-inventory"></a>Samstilla vörur og birgðir

**Vörurnar** í [!INCLUDE[prod_short](../includes/prod_short.md)] eru sambærilegar *vörum* í Shopify, sem innihalda efnislegar vörur, stafrænt niðurhal, þjónustu og gjafakort sem seljast. Tvær meginástæður eru til að samstilla atriðin:

1. Fyrst og fremst er gagnastjórnun framkvæmd í [!INCLUDE[prod_short](../includes/prod_short.md)], nauðsynlegt er að flytja öll eða einhver gögn til Shopify og gera það sýnilegt. Hægt er að flytja út Vöruheiti, lýsingu, mynd, verð, ráðstöfunarmagn, afbrigði, Lánardrottnaupplýsingar og strikamerki. Þegar flutt er inn geta vörurnar orðið strax sýnilegar eða þær skoðaðar og auknar af ábyrgum einstaklingi fyrst.
2. Þegar pöntun þaðan Shopify er flutt inn eru upplýsingar um vörur mikilvægar fyrir frekari vinnslu skjals í [!INCLUDE[prod_short](../includes/prod_short.md)].

Þessar tvær áætlanir eru alltaf virkjaðar.

Önnur atburðarás er þegar gögnum er stjórnað í Shopify og óskað er eftir að flytja þær vörur í magn til [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi atburðarás getur verið gagnleg fyrir tilvik um gagnaflutingu, þegar tenging við netverslun sem þegar er til þarf að tengjast nýju [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="to-define-item-synchronizations"></a>Vörusamstillingar skilgreindar

1. Veldu leitarljósasermið ![sem opnar aðgerðina segja mér upp.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Shopify búð**. Opna búð þar sem skilgreina á samstillingu vöru.
2. **Velja þarf valkostinn úr reitnum sync-vara**. <br>Eftirfarandi tafla lýsir muninum á milli valkostina.

|Valkostur|Lýsing|
|------|-----------|
|**Autt**| Vörur eru fluttar inn ásamt innflutningi á pöntunum. Afurðir eru fluttar út í Shopify ef notandi keyrir **Bæta við vöruaðgerð** í **Shopify glugganum vörur**. Þetta er sjálfgefin hegðun. |
|**Að Shopify**| Velja skal þennan valkost ef, eftir að Upphafleg Samkeyrsla ræsast með því **að bæta við vöruaðgerð**, er ætlunin að uppfæra afurðir handvirkt **með samstillingaraðgerð afurðar** eða í gegnum vinnslubiðröð fyrir endurteknar uppfærslur. Munið að gera kleift **að uppfæra Shopify afurðakvöldin**. Ef ekki er virkjað er það jafngilt **auðu** valmöguleikanum. |
|**Frá Shopify**| Veldu þennan valkost ef þú ætlar að flytja afurðir úr Shopify í magnskrá, annaðhvort með því að nota samstillingaraðgerð afurðar **eða vinnslubiðröð með** endurteknum uppfærslum. Ef enginn valkostur er valinn jafngildir **hún auðum** valkosti.|

## <a name="import-items-from-shopify"></a>Flytja inn vörur úr Shopify

Annað hvort er innflutningur vara frá Shopify í magni eða ásamt innflutningi á pöntunum, en þeim vörum er bætt **Shopify við afurðavöruafbrigðatöflurnar** **Shopify** fyrst. Eftirfarandi stillingar láta þig hafa umsjón með ferlinu:

|Svæði|Lýsing|
|------|-----------|
|**Sjálfvirk stofnun óþekktra atriða**|Þegar shopify vörur og vöruvíddasamsetningar eru fluttar inn [!INCLUDE[prod_short](../includes/prod_short.md)][!INCLUDE[prod_short](../includes/prod_short.md)] reynir aðgerðin alltaf að finna samsvarandi færslu á vörulistanum. **BIRGÐAHALDSVÖRPUN** hefur áhrif á hvernig jöfnun er gerð og stofnar nýja vöru og/eða vöruafbrigði. Sjá [Product mapping](synchronize-items.md#) fyrir frekari upplýsingar. Gera þennan valkost virkan ef stofna á nýja vöru eða þegar samsvarandi færsla er ekki til. Nýja varan verður stofnuð með innfluttu gögnum og **Sniðmátskóta**. Ef þessi valkostur er ekki virkjaður þarf að stofna vöru handvirkt og nota **vörpun afurðaraðgerða** úr afurðum frá **Shopify síðunni vörur**.|
|**Kóði vörusniðmáts**|Notað ásamt sjálfvirkum atriðum til að **Stofna Óþekkt atriði**. <br> Velja sniðmát sem á að nota fyrir sjálfvirkt stofnaðar vörur.|
|**SKR Kortvörpun**|Veldu hvernig þú vilt nota **birgðavirði** innflutt frá Shopify meðan á vörpun vöru/afbrigðis og stofnunar stendur. Sjá [hvernig be-og barcode sem er skilgreint í afurð hefur áhrif á Shopify vörpun og stofnun vara og afbrigða](synchronize-items.md#how-sku-and-barcode-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**Aðkoma að svæði SKÚLAGÖTU**|Notað ásamt **be-vörpun** sem stillt er á **vöru. Nei + Afbrigðiskóti** valkostur.<br> Skilgreinið Skilrúm sem á að nota til að kljúfa BIRGÐAHALDSEININGU. <br>Ef Shopify til dæmis er búið til afbrigði með be ' 1000/001 ' er ritað '/' í **skilríkjakóðakinu** skreita til að fá vörunúmerið í [!INCLUDE[prod_short](../includes/prod_short.md)] sem ' 1000 ' og vöruafbrigðakótinn sem ' 001 '.
|**Forskeyti afbrigðis**|Notað ásamt **be-vörpun** sem stillt er á **afbrigðiskóta** eða **vöru. Engir + Afbrigðiskóti** Valkostir sem varaáætlun þegar birgðahaldseining Shopify er auð.<br>Ef stofna á Vöruafbrigðið [!INCLUDE[prod_short](../includes/prod_short.md)] sjálfvirkt þarf að færa inn gildi í **kóða**. Sjálfgefið er að gildið sem er skilgreint í be-svæðinu sem flutt er inn úr Shopify er notað. Ef be er hins vegar autt býr hún til kóða sem er ræstur með skilgreindu afbrigðisforskeyti og "001".|
|**Shopify Hægt að uppfæra vöru**| Þessi kostur er valinn ef uppfæra á vörur og/eða vöruvíddasamsetningar sjálfvirkt.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Hvernig SKUs og barkóðar eru skilgreindir í Shopify afurð hefur áhrif á vörpun og stofnun vara og afbrigða í aðalkerfum fyrirtækja

Þegar afurðir eru fluttar inn úr Shopify töflunum yfir í **Shopify vöruvíddasamsetningar** **Shopify** er [!INCLUDE[prod_short](../includes/prod_short.md)] reynt að finna tiltækar færslur. Eftirfarandi tafla lýsir muninum á milli valkostina í **reitnum skr. vörpun**.

|Valkostur|Áhrif á kortlagningu|Áhrif á sköpun|
|------|-----------------|------------------|
|**Autt**|Skreitin er ekki notuð í vöruvörpunarvenjum.|Engin áhrif á stofnun vörunnar. <br>Hindrar stofnun vöruvíddasamsetningar. Það er gagnlegt þegar í sölupöntuninni er aðeins notað aðalatriði. Enn er hægt að varpa afbrigði handvirkt úr **Shopify glugganum vara**.|
|**Vörunr.**|Veljið, ef reiturinn BIRGÐAHALDSEINING inniheldur reitinn Vörunr.|Engin áhrif á stofnun vöru án vöruvíddasamsetningar. Fyrir vöru með vöruvíddasamsetningar er hvert afbrigði stofnað sem aðskilin vara.<br> Til dæmis, ef Shopify er með afurð með tveimur vöruvíddasamsetningar og skimun þeirra er ' 1000 ' og ' 2000 ', í [!INCLUDE[prod_short](../includes/prod_short.md)] kerfi verða til tvær vörur með númerum ' 1000 ' og ' 2000 '.|
|**Afbrigðiskóði**|BIRGÐAHALDSEINING er ekki notuð í venja við vörpun vöru.|Engin áhrif á stofnun vörunnar. Þegar vöruafbrigði er stofnað er gildi be notað sem kóti. Ef be er autt er Kóði myndaður með því að **nota Forskeytisvæðið** afbrigði.|
|**Vörunr. + Afbrigðiskóti**| Veljið ef be-reiturinn inniheldur vörunúmer. vöruafbrigðakótinn sem er aðgreindur eftir gildinu sem er skilgreindur í **Aðgreiningarsvæði** skr svæðisins.|Þegar vara er stofnuð er fyrsti hluti gildis á be-svæðinu notaður sem **enginn.**. Ef BIRGÐAHALDSEINING er tóm er atriði nr. er mynduð með því að nota númeraröð sem er skilgreind í Sniðmátskóta eða vöruvöru **í** **glugganum Birgðagrunnur** . **·**<br>Þegar vara er stofnuð notar afbrigðið seinni hluta af gildi be-reitsins sem **kóða**. Ef be er autt er Kóði myndaður með því að **nota Forskeytisvæðið** afbrigði.|
|**Vörunr.**| Velja hvort be-reiturinn innihaldi Vörunr. Í þessu tilfelli **er Vörunr. lánardr.** ekki notað í **glugganum birgðaspjald**, en **Vörunr** **. lánardrottins í vörulista lánardrottins**. Ef kóti fyrir fundaskrá *lánardrottins* inniheldur afbrigðiskóta er þessi Afbrigðiskóti notaður til að varpa Shopify afbrigðinu.|Ef samsvarandi lánardrottinn er til staðar [!INCLUDE[prod_short](../includes/prod_short.md)] mun be-gildið verða notað sem **Vörunr lánardrottins** í **birgðaspjaldinu** og **vörutilvísuninni** af gerðinni lánardrottinn. <br>Hindrar stofnun vöruvíddasamsetningar. Það er gagnlegt þegar nota á aðalatriði í sölupöntuninni. Enn er hægt að varpa afbrigði handvirkt úr **Shopify glugganum vara**.|
|**Strikamerki**| Velja hvort be-svæðið innihaldi strikamerki. Leit er framkvæmd meðal **Vörutilvísana** af gerðinni lánardrottinn. Ef fann Vörutilvísanaskrá sem inniheldur afbrigðiskóta verður þessi Afbrigðiskóti notuð til að varpa Shopify afbrigðinu.|Engin áhrif á stofnun vörunnar. <br>Hindrar stofnun vöruvíddasamsetningar. Það getur verið gagnlegt ef aðeins aðalatriði er notað í sölupöntuninni. Enn er hægt að varpa afbrigði handvirkt úr **Shopify glugganum vara**.|

Eftirfarandi tafla lýsir áhrifum **reitsins strikamerskóti**.

|Áhrif á kortlagningu|Áhrif á sköpun|
|-----------------|------------------|
|Leit er gerð á milli **vörutilvísana** af gerðinni strikamerki fyrir gildið sem tilgreint er í reitnum strikamerki í Shopify. Ef fann vörutilvísanaskrá sem inniheldur afbrigðiskóta verður þessi Afbrigðiskóti notuð til að varpa Shopify afbrigðinu.|Strikamerki er vistað sem **vörutilvísun** fyrir vöru og vöruafbrigði.|

> [!NOTE]  
> Hægt er að kveikja á vörpun fyrir valdar afurðir/afbrigði eða allar innfluttar ókortlagðar vörur með því að velja **reyna finna vörpun** afurða (fyrir valið) eða **reyna að finna varpanir** (fyrir alla).

## <a name="export-items-to-shopify"></a>Flytja út vörur á Shopify

Velja einingarnar úr vörulistanum sem verður fluttur út í Shopify. **Nota skal aðgerðina bæta við vöru** úr **Shopify glugganum vörur** til að bæta vörum við Shopify lista yfir vörur.

Eftirfarandi stillingar láta þig hafa umsjón með ferlinu við útflutning á vörum:

|Svæði|Lýsing|
|------|-----------|
|**Verðflokkur viðskiptamanns**|Ákvarða verð fyrir vöru í Shopify. Söluverð þessa verðflokks viðskiptamanns er tekið. Ef enginn flokkur er færður inn er verðið á birgðaspjaldinu notað.|
|**Afsláttarflokkur viðskiptamanns**|Ákvarða afsláttinn sem á að nota við útreikning verðs á vöru í Shopify. Afsláttur er ekki geymdur í **verðsvæðinu** og fullt verð er geymt á **svæðinu bera saman við verð**.|
|**Samstilling lengdrar texta samkeyrslu**|Veljið til að samstilla lengdan texta vörunnar. Þar sem það verður bætt við *lýsingu* getur það innihaldið HTML-kóða. |
|**Eigindir samkeyrslu atriðis**|Veljið til að samstilla eigindir atriðis. Eigindi eru sniðin sem tafla og innifalin í *lýsingarsvæði* á Shopify.|
|**Tungumálskóða**|Ef þetta er valið eru þýddar útgáfur notaðar fyrir titil, eigindir og lengdan texta.|
|**SKR Kortvörpun**|Veldu hvernig þú vilt fylla út skreitan í Shopify. Stuðningsvalkostir eru:<br> - **Vörunr.** til að nota Vörunr. fyrir bæði afurðir og vöruvíddasamsetningar.<br> - **Vörunr. + Afbrigðiskóti** til að búa til birgðaskrá með samtengingar-gildi tveggja svæða. Fyrir vörur án vöruvíddasamsetningar er Vörunr. er eingöngu notað.<br>- **Vörunr.** til að nota vörunúmer lánardrottins sem er *skilgreint á birgðaspjaldinu* fyrir bæði afurðir og vöruvíddasamsetningar.<br> - **Strikamerki** -notar **vörutilvísun** af gerðinni strikamerskóti. Þessi valkostur virðir afbrigði. |
|**Aðkoma að svæði SKÚLAGÖTU**|Skilgreinið skiltákn fyrir **vöru. Nei + Afbrigðiskóti** valkostur.|
|**Birgðastöðvar raktar**|Velja hvernig kerfið á að fylla út reitinn rekja birgðir **fyrir afurðir sem fluttar eru** út í Shopify. Hægt er að uppfæra ráðstöfunarupplýsingar úr [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir afurðir þar Shopify sem birgðahald er virkjað. Sjá [Inventory](synchronize-items.md#sync-inventory-to-shopify) fyrir frekari upplýsingar.|
|**Sjálfgefin Birgðastefna**|Velja *afnot* til að koma í veg fyrir neikvæða kaupliði Shopify megin. |
|**Hægt að uppfæra Shopify afurðir**|Tilgreinið hvort [!INCLUDE[prod_short](../includes/prod_short.md)] aðeins megi stofna vörur eða geta uppfært vörur einnig. Veljið þennan valkost ef að eftir að Upphafleg Samkeyrsla sem sett var af stað með **aðgerðinni bæta við vöru** er notuð til að uppfæra afurðir handvirkt með **samstillingu afurðaaðgerða** eða gegnum vinnslubiðröð í endurteknum uppfærslum. Munið að velja **Shopify** **í svæðið vara samkv**.|

### <a name="fields-mapping-overview"></a>Yfirlit yfir vörpun svæða

|Shopify|Uppspretta þegar flutt er út úr[!INCLUDE[prod_short](../includes/prod_short.md)]|Mark þegar flutt var inn til[!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Staða|**Samkvæmt stöðunni fyrir stofnaðar afurðir** í **Shopify verkstæðisspjaldinu**. Nánari upplýsingar eru [í ad hock uppfærslum á Shopify vörum](synchronize-items.md#ad-hock-updates-of-shopify-products).|Ekki notaður.|
|Titill|**Lýsingu**. Ef tungumálakóðinn er skilgreindur og samsvarandi þýðing vöru er til staðar verður að nota vöruþýðingar í stað lýsingar.|**Lýsing**|
|Lýsing|Sameinar lengda texta og eigindir ef samsvarandi víxlar Shopify verkstæðisspjaldanna eru virkir. Virðir tungumálskóða.|Ekki notaður.|
|Titilsíða titils|Festa gildi: tóm, sjá [auglýsingat-hock uppfærslur á Shopify vörum](synchronize-items.md#ad-hock-updates-of-shopify-products). |Ekki notaður.|
|SEO meta Lýsing|Festa gildi: tóm, sjá [auglýsingat-hock uppfærslur á Shopify vörum](synchronize-items.md#ad-hock-updates-of-shopify-products). |Ekki notaður.|
|Geymslumiðill|**Mynd**, nánari upplýsingar má finna [í myndum samstillingarvöru](synchronize-items.md#sync-item-images)|**Mynd**|
|Verð|Verð í lok viðskiptamanns er reiknað með tilliti til vöruverðflokks, vöruafsláttarflokks, gjaldmiðilskóða og sniðmátskóta viðskiptamanns. |Ekki notaður.|
|Bera saman á verðlagi|Verð án afsláttar er reiknað með tilliti til vöruverðflokks, vöruafsláttarflokks, gjaldmiðilskóða og sniðmátskóta viðskiptamanns. |Ekki notaður.|
|Kostnaður á vöru|**Kostnaðarverð**|**Kostnaðarverð**|
|BHE|Sjá **Skunarvörpun** í [útflutningsvörur á Shopify](synchronize-items.md#export-items-to-shopify)| Sjá [hvernig birgðahaldseining og strikamerki hafa áhrif á Shopify vörpun og stofnun vara og vöruvíddasamsetningar](synchronize-items.md#how-sku-and-barcode-defined-in-shopify-product-impact-mapping-and-creation-of-items-and-variants-in-business-central)|
|Strikamerki|**Vörutilvísun** af gerðinni strikamerskóti|**Vörutilvísun** af gerðinni strikamerskóti|
|Rekja magn|**Samkvæmt birgðatrakinu** á **Shopify verkstæðisspjaldinu**. Sjá [Inventory](synchronize-items.md#sync-inventory-to-shopify) fyrir frekari upplýsingar.|Ekki notaður.|
|Halda áfram að selja þegar út af hlutabréfum|**Samkvæmt sjálfgefinni Birgðastefnu** í **Shopify verkstæðisspjaldinu**. Ekki flutt inn.|Ekki notaður.|
|Gerð|**Lýsing** á **tegundakóða vörunnar**. Ef tegundin er ekki tilgreind í Shopify er henni bætt við sem sérsniðna gerð.|**Kóði vöruflokks**. Kortlagning eftir lýsingu.|
|Lánardrottinn|**Nafn** lánardrottins úr **Lánardr.** |**Nr.** lánardrottins Vörpun eftir nafni.|
|Þyngd|**Brúttóþyngd**.|Ekki notaður.|
|Skattskylt|Fast gildi: virkjað.|Ekki notaður.|
|Skattkóðar|**Kóta** skattflokks. Á aðeins við um virðisaukaskatt. Sjá [skatta](synchronize-orders.md#tax-remarks) fyrir frekari upplýsingar. |Ekki notaður.|

### <a name="tags"></a>Efnisorð notenda

Innflutt merki má rýna í **upplýsingakassa merkan** í **Shopify vörunni**. Ef breyta á merkjum er merki **aðgerðinnar valið** á **Shopify síðunni afurð**.
**Ef valkosturinn til að Shopify** Velja í **reitnum sync vara** er úthlutað merkjum sem eru flutt út Shopify í við næstu samstillingu.

## <a name="run-item-synchronization"></a>Keyra samstillingu vöru

Hægt er að framkvæma fulla eða að hluta samstillingu atriða á marga mismunandi vegu.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Upphaflega Samkeyrsla á vörum frá Viðskiptamiðinu til Shopify

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. **Veljið aðgerðina bæta við vörum**.
3. **Kótinn er færður í reitinn verkstæðiskóti**. Ef glugginn afurð **Shopify er opnaður** úr **Verkstæðisglugganum** verður vinnukóði sjálfkrafa fylltur út.
4. Skilgreinið afmarkanir á vörur eftir þörfum. Til dæmis er hægt að afmarka eftir vörunnr. eða vörutegundakóða.
5. Velja **Í lagi**.

Vörurnar sem koma fram eru sjálfkrafa stofnaðar í Shopify með verði en myndir og birgðastig eru ekki teknar með. Aðgerðin gæti tekið nokkurn tíma ef mikill fjöldi atriða bætist við.

### <a name="sync-products-from-shopify-to-business-central"></a>Samkeyrsla afurða frá Shopify til Aðalstarfsemi

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem á að samstilla vörur til að opna **Shopify spjald** -síðu verkstæðis.
3. Velja skal **aðgerðina samstilla vörur**.

Einnig er hægt að **nota aðgerðina Samkeyrsluvörur** í **Shopify glugganum vörur** eða leita að **keyrslu samstillingarvara**.

### <a name="ad-hock-updates-of-shopify-products"></a>Auglýsingastofa-hock uppfærslur á Shopify vörum

Þegar færslurnar eru uppfærðar í **Shopify vörutöflunni** eru eftirfarandi breytingar samstilltar með Shopify.

Uppfæra

* **Staða** -hægt er að velja á milli virkra, safnvista eða uppkvaðna.
* **SEO titill**
* **SEO Lýsing**

Eyðingu

Byggt er á gildinu í **aðgerð fyrir fjarlægar afurðir** í **Shopify verkstæðiskorti**, Shopify ef skráningu er eytt af **Shopify síðunni vörur**.

* **Auður** -Ekkert mun gerast. Ef þörf krefur þarf notandinn að framkvæma aðgerðina sem er nauðsynleg frá Shopify admin.
* **Staða í drögum** -Staða afurðar í Shopify er stillt á *drög*.
* **Staða í skjalasafni** -afurð er skjöluð í Shopify.

## <a name="sync-item-images"></a>Samstilla vörumyndir

Samstillingu mynda er hægt að skilgreina fyrir samstilltar vörur. Hægt er að velja um eftirfarandi valkosti:

* **Auður** -samstilling mynda er óvirk.
* **Til Shopify** -myndir af vörum eru fluttar út til Shopify
* **Úr Shopify** -myndir frá Shopify eru fluttar inn á[!INCLUDE[prod_short](../includes/prod_short.md)]

Hægt er að frumstilla samstillingu mynda á tvennan hátt.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Samstilla myndir afurðar úr Shopify verkstæðisglugganum

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu tengdan tengil.
2. Veldu verkstæðið sem á að samstilla myndir við til að opna **Shopify spjald-síðu vinnukorts**.
3. Velja skal **aðgerðina samstilla Afurðarmyndir**.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Samstilla myndir afurðar úr Shopify glugganum vörur

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. Velja skal **aðgerðina samstilla Afurðarmyndir**.

### <a name="image-synchronization-remarks"></a>Athugasemd samstillingu mynda

* Við útflutning mynda frá [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, að nýjum myndum sé bætt við Shopify, halda Gamlar myndir ósnortinn. Ef mynd er uppfærð í [!INCLUDE[prod_short](../includes/prod_short.md)] þarf að eyða gömlum myndum í Shopify admin.
* Myndir sem eru fluttar út til Shopify og ekki í samræmi við kröfur sem skilgreindar eru af Shopify, verða ekki fluttar inn. Frekari upplýsingar er að finna [í Vörumiðilsgerðum á help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Samkeyrsla verði með Shopify

Verð má flytja út fyrir samstilltar vörur með þeim hætti sem lýst er hér á eftir.

### <a name="sync-prices-from-the-shopify-products-window"></a>Sync verð úr Shopify glugganum vörur

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. Samstilla verð er **valið í Shopify** aðgerð.

### <a name="price-calculation-remarks"></a>Athugasemdir við verðútreikning

* Fyrir verðútreikninga er mikilvægt að hafa gildið í **reitnum sjálfgefið Viðskiptamannssniðmát**.
* Munið að færa inn **gjaldmiðilskóta** ef vefverslunin notar annan GJALDMIÐIL en ISK.
* Þegar ákvarðað er verð, [!INCLUDE[prod_short](../includes/prod_short.md)] notar "Lægsta verð" rökin. Það þýðir að ef einingarverð sem er skilgreint á birgðaspjaldinu er lægra en það sem er skilgreint í verðflokknum er einingarverðið frá birgðaspjaldinu notað.

## <a name="sync-inventory-to-shopify"></a>Samstilla birgðir til Shopify

Samstillingu birgða er hægt að skilgreina fyrir þegar samstilltar vörur. Um tvö skilyrði er að ræða sem þarf að uppfylla:

1. Birgðakælingar verða að vera virkjaðar fyrir afurð í Shopify. Ef vörur eru fluttar út til Shopify er það gert með því **að virkja** víxla rakinna **Shopify birgða í verkstæðisspjaldinu**. Sjá [útflutningsvörur Shopify](synchronize-items.md#export-items-to-shopify) fyrir frekari upplýsingar.
2. Birgðasamsynch verður að vera virkt fyrir **Shopify staðsetningar**.

### <a name="to-enable-inventory-sync"></a>Til að virkja samstillingu birgða

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verkstæðið þar sem samstilla á birgðir til að opna **Shopify spjald** -síðu verkstæðis.
3. **Veldu staðsetningar** aðgerða til að opna **Shopify verkstæðisstaði**.
4. **Velja aðgerðina Sækja Shopify staðsetningar** til að flytja inn alla staði sem skilgreindir eru í Shopify. Þær má finna í [**stillingum staðsetningar**](https://www.shopify.com/admin/settings/locations) í **Shopify admin**.
5. **Í reitnum Birgðageymsluafmörkun** er hægt að bæta við birgðageymslum ef aðeins á að taka birgðir frá tilteknum birgðageymslum. Þar má t.d. nefna *Austur | VESTURS* þannig að birgðir aðeins af þessum tveimur birgðageymslum eru til sölu í gegnum vefverslun.
6. Hafna því að skipta um **óvirka** til að virkja samstillingu birgða á völdum Shopify stöðum.

Hægt er að frumstilla samstillingu birgða á tvennan hátt.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Samstilla birgðir úr Shopify verkstæðisglugganum

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu tengdan tengil.
2. Veljið verkstæðið þar sem samstilla á birgðir til að opna **Shopify spjald** -síðu verkstæðis.
3. **Veljið samstillingarbirgðaaðgerðina**.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Samstilla birgðir úr Shopify glugganum vörur

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify afurðir** og veljið tengdan tengil.
2. **Veljið samstillingarbirgðaaðgerðina**.

### <a name="inventory-remarks"></a>Athugasemdir birgða

* Tengið reiknar út áætlaða stöðu **sem er** í boði og flytja hana Shopify út.
* Hægt er að skoða birgðaupplýsingar sem mótteknar Shopify eru í **Shopify birgðaupplýsingarsíðu** birgða. Í þessum upplýsingakassa fæst yfirlit yfir Shopify Birgðir og síðast reiknaðar birgðir í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það er Skráning á staðnum.
* Ef upplýsingar um birgðir í Shopify eru mismunandi eftir **áætlaðri stöðu** til staðar í [!INCLUDE[prod_short](../includes/prod_short.md)], verður birgðir uppfærðar í Shopify.

## <a name="see-also"></a>Sjá einnig

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
