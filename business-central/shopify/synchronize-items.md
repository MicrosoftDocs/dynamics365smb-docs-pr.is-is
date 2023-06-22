---
title: Samstilla vörur og birgðir
description: Setja upp og keyra samstillingar vara milli Shopify og Business Central
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30116, 30117, 30126, 30127,'
author: AndreiPanko
ms.author: andreipa
ms.reviewer: bholtorf
---

# <a name="synchronize-items-and-inventory" />Samstilla vörur og birgðir

 **Vörurnar**  í  [!INCLUDE[prod_short](../includes/prod_short.md)]  eru sambærilegar þeim sem  *Vara*  í  Shopify  og eru með efnislegar vörur, stafrænt niðurhal, þjónustu og gjafakort sem seljast. Tvær meginástæður eru til að samstilla atriði:

1. Gagnastjórnun gerist fyrst og fremst hjá [!INCLUDE[prod_short](../includes/prod_short.md)]. Þú þarft að flytja öll eða sum gögn þaðan út í Shopify og gera þau sýnileg. Hægt er að flytja út vöruheiti, lýsingu, mynd, verð, framboð, afbrigði, upplýsingar um lánardrottinn og strikamerki. Þegar flutt hefur verið út er hægt að fara yfir atriðin eða gera þau sýnileg strax.
2. Þegar pöntun frá Shopify er flutt inn eru upplýsingarnar um hlutina mjög mikilvægar fyrir frekari skjalavinnslu í [!INCLUDE[prod_short](../includes/prod_short.md)].

Sviðsmyndirnar tvær á undan eru alltaf virkar.

Þriðja sviðsmynd er að hafa umsjón með gögnum í Shopify en flytja þau atriði inn í heildsölu til [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi sviðsmynd getur verið gagnleg fyrir tilvik gagnaflutnings, svo sem þegar þú vilt tengja núverandi vefverslun við nýtt [!INCLUDE[prod_short](../includes/prod_short.md)] umhverfi.

## <a name="define-item-synchronizations" />Skilgreina vörusamstillingar

1. Í leitinni velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn og opna **Shopify Verslun**. Opna verslunina sem á að stilla samstillingu vöru fyrir.
2. Í reitnum **Samstilla vöru** skal velja nauðsynlegan valkost.

   Eftirfarandi tafla lýsir valkostunum.

|Valkostur|Lýsing|
|------|-----------|
|**Autt**| Vörur eru fluttar inn um leið og pantanir eru fluttar inn. Vörur eru fluttar út til Shopify ef notandi keyrir aðgerðina **Bæta við vöru** á síðunni **Shopify Vörur**. Þessi valkostur er sjálfgefið ferli.|
|**Til Shopify**| Þessi kostur er valinn ef upphafleg samstilling er virkjuð með aðgerðinni **Bæta við vöru**, þú ætlar að uppfæra vörur handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Munið að virkja reitinn **Getur uppfært Shopify vöru**. Ef það er ekki virkt jafngildir það valkostinum **Autt** (sjálfgefið ferli). Fáðu frekari upplýsingar í hlutanum [Flytja út vörur í Shopify](synchronize-items.md#export-items-to-shopify).|
|**Frá Shopify**| Þessi kostur er valinn ef ætlunin er að flytja vörur inn frá Shopify í lausasölu, annaðhvort handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Fáðu frekari upplýsingar í hlutanum [Flytja inn atriði frá Shopify](synchronize-items.md#import-items-from-shopify).|

## <a name="import-items-from-shopify" />Flytja inn atriði úr Shopify

Fyrst skaltu flytja inn vörur annað hvort í lausu frá Shopify eða ásamt pöntunum til að bæta þeim við töfluna **Shopify Vara** og **Shopify Afbrigði**. Síðan varpa innfluttar vörur og afbrigði á vörur og afbrigði í [!INCLUDE[prod_short](../includes/prod_short.md)]. Stjórna ferlinu með því að nota eftirfarandi stillingar:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Búa til óþekktar vörur sjálfvirkt**|Þegar Shopify vörur og afbrigði eru flutt inn í [!INCLUDE[prod_short](../includes/prod_short.md)], reynir [!INCLUDE[prod_short](../includes/prod_short.md)] aðgerðin fyrst að finna samsvarandi skrá í vörulistanum. **Vörpun birgðahaldseiningar** hefur áhrif á hvernig samsvörun er framkvæmd og býr til nýja vöru og/eða vöruafbrigði. Virkjaðu þennan valkost ef búa á til nýja vöru eða þegar samsvarandi skrá er ekki til. Nýja varan er búið til með því að nota innflutt gögn og **Vörusniðmátskóða**. Ef þessi valkostur er ekki virkur þarftu að búa til vöru handvirkt og nota aðgerðina **Varpa vöru** á síðunni **Shopify Vara**.|
|**Vörusniðmátskóði**|Notið þetta svæði með því að skipta óþekktu atriði  **út fyrir**  sjálfvirka stofna.<br>Veldu sniðmátið sem á að nota fyrir vörur sem eru sjálfkrafa búnar til.|
|**BHE-vörpun**|Veljið hvernig nota á gildi **Birgðarhaldseiningar** sem flutt er inn frá Shopify við vörpun og stofnun vörunnar/afbrigðisins. Frekari upplýsingar er að finna í hlutanum [Áhrif Shopify birgðarhaldseininga vöru og strikamerkja á vörpun og stofnun vöru og afbrigða í Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Reitaskiltákn birgðahaldseiningar**|Notið þetta svæði með  **be-vörpun**  sem sett er  **[á vöruna. Nei + Afbrigðiskóti](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**  valkostur.<br>Skilgreindu skilju sem nota á til að skipta birgðahaldseiningunni.<br>Þannig að ef Shopify þú býrð til afbrigðið með birgðahaldseiningu „1000/001“ þá skrifar þú „/“ reitinn **Reitaskiltákn birgðahaldseiningar** til að gera vörunúmerið í [!INCLUDE[prod_short](../includes/prod_short.md)] „1000“ og afbrigðiskóðann „001“.|
|**Forskeyti afbrigðis**|Notið ásamt **Vörpun birgðahaldseiningar** að stilla annað hvort valkostinn **Afbrigðiskóði** eða **Vörunr. + afbrigðiskóði** sem varavalkost þegar birgðahaldseiningin frá Shopify er auð.<br>Ef þú vilt búa til vöruafbrigði sjálfkrafa í [!INCLUDE[prod_short](../includes/prod_short.md)] þarftu að slá inn gildi í **Kóða**. Sjálfgefið er að nota gildið sem skilgreint er í reit birgðahaldseiningar flutt inn frá Shopify. Ef birgðahaldseiningin er auð mun hún hins vegar búa til kóða sem byrjar á skilgreinda forskeyti afbrigðisins og „001“.|
|**Shopify Get ég uppfært atriði**|Þessi kostur er valinn ef þú vilt uppfæra vörur og/eða afbrigði sjálfkrafa.|

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central" />Áhrif Shopify birgðahaldseininga vöru og strikamerkja á vörpun og stofnun vara og afbrigða í Business Central

Þegar vörur eru fluttar inn frá Shopify í töflurnar **Shopify Vörur** og **Shopify Afbrigði** reynir [!INCLUDE[prod_short](../includes/prod_short.md)] að finna fyrirliggjandi skrár.

Eftirfarandi tafla sýnir muninn á valkostum í reitnum **Vörpun birgðahaldseiningar**.

|Valkostur|Áhrif á vörpun|Áhrif á sköpun|
|------|-----------------|------------------|
|**Autt**|Be-svæðið er ekki notað í vörpunarkerfum.|Engin áhrif á stofnun vörunnar.<br>Þessi valkostur kemur í veg fyrir að hægt sé að búa til afbrigði. Aðeins aðalvaran er notuð í sölupöntun. Enn er hægt að kortleggja afbrigði handvirkt á síðunni **Shopify Vara**.|
|**Vörunr.**|Veldu hvort að reitur birgðahaldseiningar innihaldi vörunúmerið|Engin áhrif á sköpun atriðis án afbrigða. Fyrir vörur með afbrigðum er hvert afbrigði búið til sem aðskild vara.<br>Ef  Shopify  hefur afurð með tveimur vöruvíddasamsetningar og skimunum eru ' 1000 ' og ' 2000 ',  [!INCLUDE[prod_short](../includes/prod_short.md)]  munu tvö atriði tölusetja ' 1000 ' og ' 2000 '.|
|**Afbrigðiskóði**|Be-svæðið er ekki notað í vörpunarkerfum.|Engin áhrif á stofnun vörunnar. Þegar vöruafbrigði er búið til er gildi reits birgðahaldseiningar notað sem kóði. Ef birgðahaldseiningin er auð er kóði myndaður með því að nota reitinn **Forskeyti afbrigðis**.|
|**Vörunr. + afbrigðiskóði**|Þessi kostur er valinn ef birgðasvæðið inniheldur vörunúmer og afbrigðiskótinn vöru er aðskilinn gildinu sem er skilgreindur í  **Aðgreiningarsvæði**  skreita.|Þegar vara búin til er fyrsti hluti gildis reits birgðahaldseiningar tilgreindur með **Nr.** Ef reitur birgðahaldseiningar er auður er vörunúmer búið til með því að nota númeraröðina sem er skilgreind í reitnum **Vörusniðmátskóði** eða **Vörunr.** á síðunni **Uppsetning birgða**.<br>Þegar hlutur er sofnaður til notar afbrigðisaðgerðin seinni hluta gildis reits birgðahaldseiningarinnar sem **kóða**. Ef reitur birgðahaldseiningar er auður er kóði búinn til með því að nota reitinn **Forskeyti afbrigðis**.|
|**Vörunr. lánardr.**|Veldu hvort reitur birgðahaldseiningar inniheldur vörunúmer lánardrottins. Í þessu tilviki er **Lán.dr., vöru nr.** ekki notaður á síðunni fyrir **Vörukort** er **Vörunr.** af **Vörulisti lánadr.** notað. Ef skráin sem fannst í *Vörulisti lánardrottins* inniheldur afbrigðiskóða er sá kóði notaður til að varpa Shopify afbrigðið.|Ef samsvarandi lánardrottinn er til staðar  [!INCLUDE[prod_short](../includes/prod_short.md)] mun be-gildið verða notað sem  **Vörunr lánardrottins.**  **á síðunni Vöruspjald**  og sem  **vörutilvísun**  *í gerð lánardrottins* . <br>Kemur í veg fyrir myndun afbrigða. Það er gagnlegt þegar þú vilt aðeins nota aðalvöruna í sölupöntuninni. Þú getur enn varpað afbrigði handvirkt á síðunni **Shopify Vara**.|
|**Strikamerki**|Veldu reitur birgðahaldseiningar innihaldi strikamerki. Leit er framkvæmd meðal  **Vörutilvísana**  af  *gerðinni strikamerskóti* . Ef tilvísunarskráin sem fannst inniheldur afbrigðiskóða er sá afbrigðiskóði notaður til að varpa Shopify afbrigðið.|Engin áhrif á stofnun vörunnar. <br>Kemur í veg fyrir myndun afbrigða. Það er gagnlegt þegar þú vilt aðeins nota aðalvöruna í sölupöntuninni. Þú getur enn varpað afbrigði handvirkt á síðunni **Shopify Vara**.|

Eftirfarandi tafla lýsir áhrifum reitsins **Strikamerki**.

|Áhrif á vörpun|Áhrif á sköpun|
|-----------------|------------------|
|Leit er framkvæmd á **Vörutilvísunum** innihalda strikamerkistegund sem gildið í reitnum fyrir **strikamerki** í Shopify. Ef tilvísunarskráin sem fannst inniheldur afbrigðiskóða er sá afbrigðiskóði notaður til að varpa Shopify afbrigðið.|Strikamerkið er vistað **Vörutilvísun** fyrir vöruna og vöruafbrigðið.|

> [!NOTE]  
> Þú getur sett af stað vörpun á völdum vörum/afbrigðum með því að velja **Reyna að finna vörpun vöru** eða af öllum innfluttum, óvörpuðum vörum með því að velja **Reyna að finna varpanir**.

## <a name="export-items-to-shopify" />Flytja vörur í Shopify

Veldu atriði úr vörulistanum sem á að flytja út í Shopify. Nota aðgerðina **Bæta við vöru** á síðunni **Shopify Vörur** til að bæta vörum á Shopify vörulistann. 

>[!IMPORTANT]
>Vörunni verður aðeins  **bætt í sölusund netverslana** . Þú þarft að birta vörur á öðrum sölurásum eins og  Shopify  POS, úr Shopify.

Þú stjórnar ferlinu við að flytja út vörur með þessum stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Samstilla lengdan texta vöru**|Veljið þetta svæði til að samstilla lengdan texta vörunnar. Þar sem því verður bætt við í reitinn *Lýsing* getur það innihaldið HTML-kóða. |
|**Samstilla vörueigindir**|Veljið þetta svæði til að samstilla eigindir atriðis. Eiginleikar eru sniðnir sem tafla og fylgja í reitnum *Lýsing* í Shopify.|
|**Markaðssetning á Markaðstexta samkeyrslu vöru**|Veljið þetta svæði til að samstilla markaðstexta vöru. Þótt markaðstexti sé nokkurs konar Lýsing er hann mismunandi eftir lýsingarsviði  **vörutegundar** .  **Reiturinn Lýsing**  er vanalega notaður sem Birtingarheiti þess að nota fljótt til að auðkenna afurðin. Markaðstextinn er hins vegar frekar ríkur og lýsandi. Tilgangur þess er að bæta markaðsefni og kynningarefni. Þennan texta er síðan hægt að birta með vörunni í Shopify. Það eru tvær leiðir til að búa til markaðstexta. Notaðu Copilot sem stingur upp á AI-myndaðan texta fyrir þig, eða Byrjaðu frá grunni.|
|**Kóði tungumáls**|Veljið þetta svæði ef óskað er eftir að þýða útgáfur sem notaðar eru fyrir titil, eigindir og lengdan texta.|
|**BHE-vörpun**|Velja hvernig á að þýða reit birgðahaldseiningar í Shopify. Studdir valkostir eru:<br> - **Vörunr.** til að nota vörunr. bæði fyrir vörur og afbrigði.<br> - **Vörunr. + afbrigðiskóði** til að búa til birgðarhaldseiningu með því að samstilla gildi tveggja reita. Fyrir hluti án afbrigða er eingöngu notað vörunúmerið.<br>- **Lán.dr., vöru nr.** til að nota númer lánardrottins vöru sem skilgreint er í *Vörukortinu* bæði fyrir vörur og afbrigði.<br> - **Strikamerki** til að nota strikamerkistegundina **Vörutilvísun**. Þessi valkostur tekur mið af afbrigðum.|
|**Reitaskiltákn birgðahaldseiningar**|Skilgreindu skilju fyrir valkostinn **Vörunr. + afbrigðiskóði**.|
|**Birgðir raktar**| Veldu hvernig kerfið á að fylla út reitinn **Rekja birgðir** vörur sem eru fluttar út til Shopify. Hægt er að uppfæra framboðsupplýsingar [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir vörur í Shopify þar sem rakning birgða er virk. Fáðu frekari upplýsingar í hlutanum [Birgðir](synchronize-items.md#sync-inventory-to-shopify).|
|**Sjálfgefin birgðastefna**|Veldu *Neita* til að koma í veg fyrir neikvæðar birgðir á Shopify hliðinni.|
|**Getur uppfært Shopify Vörur**|Skilgreinið þetta svæði ef  [!INCLUDE[prod_short](../includes/prod_short.md)]  aðeins á að stofna vörur eða geta uppfært vörur einnig. Þessi kostur er valinn ef upphafleg samstilling er virkjuð með aðgerðinni **Bæta við vöru**, þú ætlar að uppfæra vörur handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Munið að velja **Til Shopify** í reitnum **Samstilling vöru**.|

### <a name="fields-mapping-overview" />Reitir-yfirlit yfir vörpun

|Shopify|Uppruni þegar flutt er frá [!INCLUDE[prod_short](../includes/prod_short.md)]|Mark flutt er inn á [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Staða|Samkvæmt reitnum **Staða fyrir stofnaðar vörur** í **Shopify Verslunarkortinu**. Frekari upplýsingar í  [tilfallandi uppfærslum  Shopify  á vörum](synchronize-items.md#ad-hoc-updates-of-shopify-products) .|Ekki notað.|
|Titill | **Lýsing**. Ef tungumálakóðinn er skilgreindur og samsvarandi þýðing vöru er til verður þýðing vöru notuð í stað lýsingarinnar.|**Lýsing**|
|Heimildasamstæða|Sameinar lengda texta, markaðstexta og eiginleika ef viðkomandi víxlar eru virkjaðra á  Shopify  verkstæðisspjaldinu. Hledur tungumálskóðanum.|Ekki notað.|
|Titill SEO-síðu|Fast gildi: autt. Frekari upplýsingar í  [tilfallandi uppfærslum  Shopify  á vörum](synchronize-items.md#ad-hoc-updates-of-shopify-products) .|Ekki notað.|
|Lýsing SEO-lýsigagna|Fast gildi: autt. Frekari upplýsingar í  [tilfallandi uppfærslum  Shopify  á vörum](synchronize-items.md#ad-hoc-updates-of-shopify-products) .|Ekki notað.|
|Geymslumiðill|**Mynd**. Fáðu frekari upplýsingar í hlutanum [Samstilla myndir af vörum](synchronize-items.md#sync-item-images)|**Mynd**|
|Verð|Útreikningur á verði lokans-viðskiptamanns inniheldur einingarverð vöru, verðflokk viðskiptamanna, afsláttarflokk viðskiptamanns og gjaldmiðilskóta. Frekari upplýsingar í  [kaflanum Samkeyrsla verð](synchronize-items.md#sync-prices-with-shopify) |**Einingaverði**. Verðið er aðeins innflutt í nýstofnuðum vörum en það verður ekki uppfært í síðar samstillingum.|
|Samanburður á verði|Útreikningur á verði án afsláttar.|Ekki notað.|
|Kostnaður á vöru|**Kostn.verð**|**Kostnaðarverð**. Einingarkostnaðurinn er aðeins fluttur inn í Nýstofnaðar vörur og uppfærist ekki í seinni samstillingum.|
|BHE|Upplýsingar um SKUs undir  **skr Kortvörpun**  í  [útflutningsgreinum  Shopify](synchronize-items.md#export-items-to-shopify)  í kafla.|Lærðu á SKUs í  [áhrif  Shopify  vörunar skus og barkóða á vörpun og myndun vara og afbrigða í miðlægum](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)  hluta fyrirtækja.|
|Strikamerki|**Vörutilvísanir** af gerð strikamerkis.|**Vörutilvísanir** af gerð strikamerkis.|
|Rekja magn|Samkvæmt reitnum **Birgðir raktar** á síðunni **Kort í Shopify Verslunarkort**. Fáðu frekari upplýsingar í hlutanum [Birgðir](synchronize-items.md#sync-inventory-to-shopify). Eingöngu notað þegar vara er flutt út í fyrsta sinn.|Ekki notað.|
|Halda áfram að selja þegar ekki er til á lager|Samkvæmt **Sjálfgefinni birgðastefnu** í **Shopify Verslunarkortinu**. Eingöngu notað þegar vara er flutt út í fyrsta sinn.|Ekki notað.|
|Gerð|**Lýsing** á **Vöruflokkskóða**. Ef tegundin er ekki tilgreind í Shopify er henni bætt við sem sérsniðinni tegund.|**Vöruflokkskóði**. Kortlagning eftir lýsingu.|
|Lánardrottinn|**Nafn** lánardrottins frá **Nr. lánardrottins.**|**Númer lánardrottins** Vörpun eftir nafni.|
|Þyngd|**Brúttóþyngd**.|Ekki notað.|
|Skattskylt|Fast gildi: virkt.|Ekki notað.|
|Skattkóðar|**Skattflokkskóði**. Á aðeins við fyrir virðisaukaskatt. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|Ekki notað.|

### <a name="tags" />Efnisorð notenda

Farið yfir innfluttu merkin í upplýsingareitnum **Merki** á síðunni **Shopify Vara**. Á sömu síðu, til að breyta merkjum, velur þú aðgerðina **Merki**.
Ef valkosturinn **Til Shopify** er valinn í reitnum **Samstilla vöru** er úthlutuðum merkjum flutt út í Shopify við næstu samstillingu.

## <a name="run-item-synchronization" />Keyra samstillingu vöru

Samstillingu vöru að öllu leyti eða að hluta er hægt að framkvæma á marga mismunandi vegu.

### <a name="initial-sync-of-items-from-business-central-to-shopify" />Upphafleg samstilling vara frá Business Central til Shopify

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Velja aðgerðina **Bæta við atriðum**.
3. Sláðu inn kóðann inn í reitinn **Verslunarkóði**. Ef þú opnar gluggann **Shopify Vara** á síðunni **Verslunarkort** verður verslunarkóðinn fylltur sjálfkrafa út.
4. Ef mynd og birgðasamsetingu er samskipað má setja þær í sama ferli. Þar með er þeim í sama ferli þægilegast að sýniatburðarás eða þegar um er að ræða minni gagnamagni. 
5. Skilgreina vörusíur eftir þörfum. Til dæmis er hægt að sía eftir vörunr. eða vöruflokkskóða.
6. Velja **Í lagi**.

Vörurnar sem til eru eru sjálfkrafa stofnaðar í  Shopify  með verði. Myndir og birgðastig gætu verið innifaldar eftir því hvaða ákvarðanir voru gerðar. Aðgerðin getur tekið nokkurn tíma ef mjög mörgum vörum er bætt við.

### <a name="sync-products-from-shopify-to-business-central" />Samstilla vörur frá Shopify í Business Central

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veljið verslunina þar sem á að samtilla vörur til að opna síðuna **Shopify verslunarspjald**.
3. Veldu aðgerðina **Samstilla vörur**.

Einnig er hægt að nota aðgerðina **Samstilla vörur** á síðunni **Shopify Vörur** eða leita að runuvinnslunni **Samstilla vörur**.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

### <a name="ad-hoc-updates-of-shopify-products" />Sértækar uppfærslur á Shopify vörum

Þegar skrárnar eru uppfærðar í töflunni **Shopify Vara** eru eftirfarandi breytingar samstilltar við Shopify.

Uppfæra:

* **Staða** - Hægt er að velja um virka, safnvistaða eða drög.
* **Titill leitarvélabestunar**
* **Lýsing leitarvélabestunar**

Eyðing:

Byggt á gildinu í **Aðgerð fyrir vörur sem voru fjarlægðar** á síðunni **Shopify Verslunarkort** er varan uppfærð í Shopify þegar skránni er eytt af síðunni **Shopify Vara**.

* **Auður** - Ekkert gerist. Ef nauðsyn krefur þarftu að framkvæma áskilda aðgerð frá **Shopify stjórnandamiðstöðinni**.
* **Staða í drög** - Staða vörunnar í Shopify er stillt á *Drög*.
* **Staða í safnvistað** - Varan er safnvistuð í Shopify.

## <a name="sync-item-images" />Samstilla myndir af vörum

Hægt er að stilla samstillingu mynda fyrir samstilltar vörur. Velja skal úr eftirfarandi:

* **Slökkt** - Samstilling myndar er óvirk.
* **Til Shopify** - Myndir af vörum fluttar yfir í Shopify.
* **Úr Shopify** - Myndir frá Shopify er flutt inn í [!INCLUDE[prod_short](../includes/prod_short.md)].

Hægt er að ræsa samstillingu mynda á þann hátt sem lýst er hér að neðan.

### <a name="sync-product-images-from-the-shopify-shop-page" />Samstilla vörumyndir af Shopify verslunarsíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2. Velja verslun sem á að samstilla myndir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Samstilla myndir af vörum**.

### <a name="sync-product-images-from-the-shopify-products-page" />Samstilla vörumyndir Shopify af vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu aðgerðina **Samstilla myndir af vörum**.

### <a name="image-synchronization-remarks" />Athugasemdir um samstillingu mynda

* Þegar myndir eru fluttar út frá [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify er nýjum myndum bætt inn á Shopify, þannig að gamlar myndir haldast óbreyttar. Ef mynd er uppfærð í [!INCLUDE[prod_short](../includes/prod_short.md)], þarftu að eyða gömlu myndunum í **Shopify Stjórnandamiðstöðinni**.
* Myndir fluttar út til Shopify og uppfylla ekki kröfur sem skilgreindar eru af Shopify verður ekki fluttar inn. Frekari upplýsingar um [efnisgerðir vöru er að finna á help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify" />Samstilla verð við Shopify

Útflutningur á verði er notaður með þessum stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Verðhópur viðskiptavinar**|Ákveða verð fyrir vöru í Shopify. Söluverð fyrir þennan verðflokk viðskiptamanns er notaður. Ef enginn flokkur er tilgreindur er notað verðið á birgðaspjaldinu.|
|**Afsláttarflokkur viðskm.**|Ákvarða afsláttinn sem á að nota við útreikning verðs á vöru í Shopify. Afsláttur er ekki geymdur á  **verðsvæðinu**  og fullt verð er geymt á  **svæðinu bera saman við verð** .|
|**Leyfa Línuafsl.**|Tilgreinir hvort leyfa eigi línuafslátt þegar reiknað er verð Shopify. Þessi stilling á aðeins við um verð á vörunni. Verð í verðflokki viðskiptamanns eru með eigin víxla í línum.|
|**Verð með VSK**|Tilgreinir hvort Verðútreikningur á að  Shopify  INNIHALDA VSK. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|
|**VSK-viðskiptabókunarflokkur**|Tilgreinir hvaða VSK-viðskiptabókunarflokkur er notaður til að reikna út verð í Shopify. Þetta ætti að vera sá hópur sem þú notar fyrir innlenda viðskiptavini. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|
|**Gjaldmiðilskóði**|Færið aðeins inn gjaldmiðilskóta ef vefverslunin notar annan gjaldmiðil en staðbundinn gjaldmiðil (ISK). Tilgreindur gjaldmiðill verður að hafa stillt gengi. Ef vefverslunin notar sama gjaldmiðil og [! INCLUDEprod_short], skal reiturinn hafður auður.|

Hægt er að flytja verð til samstilltra vara á þeim tveimur leiðum sem lýst er hér á eftir.

### <a name="sync-prices-from-the-shopify-products-page" />Samstilla verð Shopify af vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu **Samstilla verð til að framkvæma aðgerð Shopify**.

### <a name="price-calculation-remarks" />Athugasemdir verðútreiknings

* Við ákvörðun verðs notar [!INCLUDE[prod_short](../includes/prod_short.md)] rökin „lægsta verð“. Lægsta verðrökin hunsar einingarverðið sem er skilgreint á birgðaspjaldinu ef verð er skilgreint í verðflokknum. Þetta gildir jafnvel þó að einingaverð frá vörukortalverðinu sé lægra.
* Til að reikna út verð stofnar tengivirkið bráðabirgðasölutilboð fyrir vöruna með magninu 1 og notar staðlaða verðreiknigrunn. Aðeins eru notaðar verð og afslætti sem eiga við magnið 1. Ekki er hægt að flytja út mismunandi verð eða afslætti miðað við magn.

## <a name="sync-inventory-to-shopify" />Samstilla birgðir við Shopify

Hægt er að stilla samstillingu birgða fyrir vörur sem þegar hafa verið samstilltar. Það eru tvö skilyrði sem þarf að uppfylla:

1. Rakning birgða verður að vera virk fyrir vöru í Shopify. Ef vörur eru fluttar út tilShopify, skaltu íhuga að virkja valkostinn **Rakning birgða** á síðunni **Shopify Verslun**. Fáðu frekari upplýsingar í hlutanum [Flytja út vörur í Shopify](synchronize-items.md#export-items-to-shopify).
2. Samstilling birgða verður að vera virk fyrir **Shopify Staðsetningar**.

### <a name="to-enable-inventory-sync" />Til að virkja birgðasamstillingu

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Velja verslun sem á að samstilla birgðir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veljið aðgerðina **Staðsetningar** til að opna **Shopify Staðsetningar verslunar**.
4. Veldu aðgerðina **Sækja Shopify Staðsetningar** til að flytja inn allar staðsetningarnar sem skilgreindar eru í Shopify. Þú finnur þær í stillingum fyrir [**Staðsetningar**](https://www.shopify.com/admin/settings/locations) í **Shopify Stjórnandamiðstöðinni**.
5. Í reitnum **Staðsetningarsía** er hægt að bæta við staðsetningum ef aðeins á að taka með birgðir frá tilteknum stöðum. Svo, þú gætir slegið inn *AUSTUR|VESTUR* til að gera birgðir frá aðeins þessum tveimur staðsetningm í boði fyrir sölu í gegnum netverslunina.
6. Veljið aðferð verðbréfaútreiknings sem nota á fyrir valda  Shopify  staði.

Þú getur ræst birgðasamstillingu á tvo vegu sem lýst er hér að neðan.

### <a name="sync-inventory-from-the-shopify-shop-page" />Samstilla birgðir af Shopify síðu verslunarinnar

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2. Velja verslun sem á að samstilla birgðir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Samstilla birgðir**.

### <a name="sync-inventory-from-the-shopify-products-page" />Samstilla birgðir af Shopify vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu aðgerðina **Samstilla birgðir**.

### <a name="inventory-remarks" />Athugasemdir birgða

* Staðlaður Útreikningsaðferð verðbréfakaup er  **Áætluð staða til dags**. Með extensibility er hægt að bæta við fleiri valkostum. Til að fræðast meira um extensibility er farið í  [dæmi](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md). 
* Þú getur skoðað upplýsingar um birgðir sem þú fékkst frá upplýsingareitnum Shopify á síðunni **Shopify Upplýsingareitur birgða**. Í þessum upplýsingareit færðu yfirlit yfir Shopify birgða síðustu reiknuðu birgðirnar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það er ein færsla á hverjum stað.
* Ef upplýsingar um birgðir í Shopify eru aðrar en **Áætluð staða til ráðstöfunar** í [!INCLUDE[prod_short](../includes/prod_short.md)] þá verða birgðir uppfærðar í Shopify.
* Þegar bætt er við nýjum stað í  Shopify þarf einnig að bæta við birgðafærslum fyrir það. Shopify gerir það ekki sjálfkrafa fyrir afurðir og vöruvíddasamsetningar og Connector samstillir ekki birgðastig slíkra vara á nýjum stað. Til að fá frekari upplýsingar er farið í að  [úthluta birgðum til birgðageymslna](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).

#### <a name="example-of-calculation-of-projected-available-balance" />Dæmi um útreikning áætlaðrar stöðu í árslok

Um er að ræða 10 stykkja vöru A sem fáanleg er á lager og tvær útistandandi sölupantanir. Einn fyrir mánudag með magni  *einn*  og einn fyrir fimmtudag með magn  *tvö*. Kerfið uppfærir birgðastig í  Shopify  mismunandi magni eftir því hvenær birgðir eru samkeyrðar.

|Þegar samstilling birgða er keyrð|Gildi sem er notað til að uppfæra Hlutabréfaeign|Athugasemd|
|------|-----------------|-----------------|
|Þriðjudagur|9|Birgðir 10 mínus sölustokkar setja á skip á mánudegi|
|Föstudagur|7|Birgðir 10 að frádregnum báðum sölupöntunum|

## <a name="see-also" />Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
