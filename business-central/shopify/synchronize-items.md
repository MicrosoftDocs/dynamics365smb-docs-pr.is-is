---
title: Samstilla vörur og birgðir
description: Setja upp og keyra samstillingar vara milli Shopify og Business Central
ms.date: 04/28/2024
ms.topic: article
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.collection:
  - bap-ai-copilot
---

# Samstilla vörur og birgðir

Vörurnar **í** [!INCLUDE[prod_short](../includes/prod_short.md)] eru jafngildar vörunum *í* Shopify og innihalda líkamlegar vörur, stafræn niðurhal, þjónustu og gjafakort sem selt er. Tvær meginástæður eru til að samstilla atriði:

1. Gagnastjórnun gerist fyrst og fremst í [!INCLUDE[prod_short](../includes/prod_short.md)]. Þú þarft að flytja öll eða sum gögn þaðan út í Shopify og gera þau sýnileg. Hægt er að flytja út vöruheiti, lýsingu, mynd, verð, framboð, afbrigði, upplýsingar um lánardrottinn og strikamerki. Þegar flutt hefur verið út er hægt að fara yfir atriðin eða gera þau sýnileg strax.
2. Þegar pöntun frá Shopify er flutt inn eru upplýsingarnar um hlutina mjög mikilvægar fyrir frekari skjalavinnslu í [!INCLUDE[prod_short](../includes/prod_short.md)].

Sviðsmyndirnar tvær á undan eru alltaf virkar.

Þriðja sviðsmynd er að hafa umsjón með gögnum í Shopify en flytja þau atriði inn í heildsölu til [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi sviðsmynd getur verið gagnleg fyrir tilvik gagnaflutnings, svo sem þegar þú vilt tengja núverandi vefverslun við nýtt [!INCLUDE[prod_short](../includes/prod_short.md)] umhverfi.

## Skilgreina vörusamstillingar

1. Í leitinni velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn og opna **Shopify Verslun**. Opna verslunina sem á að stilla samstillingu vöru fyrir.
2. Í reitnum **Samstilla vöru** skal velja nauðsynlegan valkost.

   Eftirfarandi tafla lýsir valkostunum.

   |Valkostur|Lýsing|
   |------|-----------|
   |**Autt**| Vörur eru fluttar inn um leið og pantanir eru fluttar inn. Vörur eru fluttar út til Shopify ef notandi keyrir aðgerðina **Bæta við vöru** á síðunni **Shopify Vörur**. Þessi valkostur er sjálfgefna ferlið.|
   |**Til Shopify**| Þessi kostur er valinn ef upphafleg samstilling er virkjuð með aðgerðinni **Bæta við vöru**, þú ætlar að uppfæra vörur handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Munið að virkja reitinn **Getur uppfært Shopify vöru**. Ef það er ekki virkt jafngildir það valkostinum **Autt** (sjálfgefið ferli). Fáðu frekari upplýsingar í hlutanum [Flytja út vörur í Shopify](synchronize-items.md#export-items-to-shopify).|
   |**Frá Shopify**| Þessi kostur er valinn ef ætlunin er að flytja vörur inn frá Shopify í lausasölu, annaðhvort handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Fáðu frekari upplýsingar í hlutanum [Flytja inn atriði frá Shopify](synchronize-items.md#import-items-from-shopify).|

   > [!NOTE]
   > Breyting á samstilltri **vöru** úr Úr **Shopify** í í hefur ekki áhrif nema hægt **sé að Shopify**  **uppfæra Shopify vörur**.

## Flytja inn atriði úr Shopify

Fyrst skaltu flytja inn vörur annað hvort í lausu frá Shopify eða ásamt pöntunum til að bæta þeim við töfluna **Shopify Vara** og **Shopify Afbrigði**. Varpa síðan innfluttum vörum og afbrigðum á vörur og afbrigði í [!INCLUDE[prod_short](../includes/prod_short.md)]. Stjórna ferlinu með því að nota eftirfarandi stillingar:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Búa til óþekktar vörur sjálfvirkt**|Þegar Shopify vörur og afbrigði eru flutt inn í [!INCLUDE[prod_short](../includes/prod_short.md)], reynir [!INCLUDE[prod_short](../includes/prod_short.md)] aðgerðin fyrst að finna samsvarandi skrá í vörulistanum. **Vörpun birgðahaldseiningar** hefur áhrif á hvernig samsvörun er framkvæmd og býr til nýja vöru og/eða vöruafbrigði. Virkjaðu þennan valkost ef búa á til nýja vöru eða þegar samsvarandi skrá er ekki til. Nýja varan er búið til með því að nota innflutt gögn og **Vörusniðmátskóða**. Ef þessi valkostur er ekki virkur þarftu að búa til vöru handvirkt og nota aðgerðina **Varpa vöru** á síðunni **Shopify Vara**.|
|**Vörusniðmátskóði**|Þessi reitur er notaður með **því að stofna óþekkt atriði** sjálfvirkt.<br>Veldu sniðmátið sem á að nota fyrir vörur sem eru sjálfkrafa búnar til.|
|**BHE-vörpun**|Veljið hvernig nota á gildi **Birgðarhaldseiningar** sem flutt er inn frá Shopify við vörpun og stofnun vörunnar/afbrigðisins. Frekari upplýsingar er að finna í hlutanum [Áhrif Shopify birgðarhaldseininga vöru og strikamerkja á vörpun og stofnun vöru og afbrigða í Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Reitaskiltákn birgðahaldseiningar**|Þessi reitur er notaður með **birgðahaldseiningarvörpun** stillt á vöruna **[. Valkosturinn Afbrigðiskóti + Afbrigðiskóti](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)** .<br>Skilgreindu skilju sem nota á til að skipta birgðahaldseiningunni.<br>Þannig að ef Shopify þú býrð til afbrigðið með birgðahaldseiningu „1000/001“ þá skrifar þú „/“ reitinn **Reitaskiltákn birgðahaldseiningar** til að gera vörunúmerið í [!INCLUDE[prod_short](../includes/prod_short.md)] „1000“ og afbrigðiskóðann „001“. Athuga skal að ef afbrigðið er stofnað með birgðahaldseiningunni '1000/001/111' í Shopify verður vörunúmerið í'1000 [!INCLUDE[prod_short](../includes/prod_short.md)] ' og vöruafbrigðiskótinn '001'. Hlutinn '111' er hunsaður. |
|**Forskeyti afbrigðis**|Notið ásamt **Vörpun birgðahaldseiningar** að stilla annað hvort valkostinn **Afbrigðiskóði** eða **Vörunr. + afbrigðiskóði** sem varavalkost þegar birgðahaldseiningin frá Shopify er auð.<br>Ef þú vilt búa til vöruafbrigði sjálfkrafa í [!INCLUDE[prod_short](../includes/prod_short.md)] þarftu að slá inn gildi í **Kóða**. Sjálfgefið er að nota gildið sem skilgreint er í reit birgðahaldseiningar flutt inn frá Shopify. Ef birgðahaldseiningin er hins vegar tóm myndar hún kóta sem byrjar á tilgreindu afbrigðisforskeyti og '001'.|
|**Shopify Get ég uppfært atriði**|Þessi kostur er valinn ef þú vilt uppfæra vörur og/eða afbrigði sjálfkrafa.|
|**UoM sem afbrigði**| Þessi kostur er valinn ef flytja á allar mælieiningar vöru út sem sérstök afbrigði. Sérstilla síðuna til að bæta reitnum við. Nánari upplýsingar um mælieininguna [sem afbrigði](synchronize-items.md#unit-of-measure-as-variant) .|
|**Heiti afbrigðisvalkosts fyrir UoM**| Þessi reitur er notaður með **UoM sem afbrigði** til að tilgreina undir hvaða valkosti á að bæta við afbrigðum sem tákna mælieiningar. Sjálfgefna gildið er *Mælieining*. Sérstillingin er notuð til að bæta reitnum við síðuna.|

## Flytja vörur í Shopify

Hægt er að flytja vörur á margar leiðir til að Shopify:

* Nota skal **Bæta við vöru til að Shopify** aðgerð beint af **birgðaspjaldssíðunni** .
* Nota skal aðgerðina **Bæta við vöru** á síðunni **Shopify Vörur** .
* Keyra vörusamstillingu einu sinni eða ítrekað með sjálfvirkni.

Sama hvernig vörur eru fluttar út eru tilteknar vöruupplýsingar fluttar Shopify á vörulistann eftir því hvernig notandi velur stillingar fyrir samstillingu vöru.

> [!IMPORTANT]
> Vörunni er aðeins bætt við **sölurás Online Store** . Það þarf að birta vörur á öðrum sölurásum, eins og Shopify sölustöðvum, frá Shopify.

Þú stjórnar ferlinu við að flytja út vörur með þessum stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Samstilla lengdan texta vöru**|Veljið þennan reit til að samstilla lengdan texta vörunnar. Þar sem henni verður bætt í reitinn **Lýsing** getur hann innihaldið HTML-kóta. |
|**Samstilla vörueigindir**|Veljið þetta svæði til að samstilla vörueigindirnar. Eigindir eru sniðnar sem tafla og tekin með í reitnum **Lýsing** í Shopify.|
|**Samstilla markaðssetningartexta vöru**|Veljið þennan reit til að samstilla markaðssetningartexta vörunnar. Þótt markaðssetningatexti sé eins konar lýsing er hann frábrugðinn lýsingarreit **vörunnar** . Reiturinn **Lýsing** er gjarnan notaður sem nákvæmt birtingarheiti til að auðkenna vöruna á fljótlegan hátt. Markaðssetningatextinn er hins vegar ríkari og lýsandi. Tilgangur hennar er að bæta við markaðssetningu og kynningarefni. Þá er hægt að birta þennan texta með vörunni í Shopify. Það eru tvær leiðir til að búa til markaðssetningartextann. Nota Copilot, sem leggur til AI-mynda texta fyrir þig, eða byrja frá grunni.|
|**Kóði tungumáls**|Þessi reitur er valinn ef nota á þýddu útgáfurnar fyrir titil, eigindir og lengdan texta.|
|**BHE-vörpun**|Velja hvernig á að þýða reit birgðahaldseiningar í Shopify. Studdir valkostir eru:<br> - **Vörunr.** nota vörunúmerið fyrir bæði vörur og afbrigði.<br> - **Vörunr.+ afbrigðiskóti** til að stofna birgðahaldseiningu með því að steypa saman gildum tveggja reita. Fyrir hluti án afbrigða er eingöngu notað vörunúmerið.<br>- **Nr. birgðal. lánardr.** nota vörunúmer lánardrottins sem er tilgreint í **birgðaspjaldinu** fyrir bæði vörur og afbrigði.<br> - **Strikamerki** til að nota strikamerkistegundina **Vörutilvísun**. Þessi valkostur tekur mið af afbrigðum.<br>Ef **Geta Uppfært Shopify vörur** er virkt verða **breytingar í reitnum** Birgðahaldseining Shopify á eftir næstu samstillingu allra vara og afbrigða sem talin eru upp á **Shopify síðunni Vörur** fyrir valda búð.|
|**Reitaskiltákn birgðahaldseiningar**|Skilgreindu skilju fyrir valkostinn **Vörunr. + afbrigðiskóði**.|
|**Birgðir raktar**| Veldu hvernig kerfið á að fylla út reitinn **Rekja birgðir** vörur sem eru fluttar út til Shopify. Hægt er að uppfæra framboðsupplýsingar [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir vörur í Shopify þar sem rakning birgða er virk. Fáðu frekari upplýsingar í hlutanum [Birgðir](synchronize-items.md#sync-inventory-to-shopify).|
|**Sjálfgefin birgðastefna**|Veldu *Neita* til að koma í veg fyrir neikvæðar birgðir á Shopify hliðinni. <br>Ef **Geta uppfært Shopify vörur** er virkt verða breytingar í reitnum **Sjálfgefin birgðaregla** settar Shopify á eftir næstu samstillingu fyrir allar vörur og afbrigði sem skráð eru á síðunni **Shopify Vörur** fyrir valda verkstæði.|
|**Getur uppfært Shopify Vörur**|Skilgreina þennan reit ef [!INCLUDE[prod_short](../includes/prod_short.md)] aðeins er hægt að stofna vörur eða uppfæra vörur einnig. Þessi kostur er valinn ef upphafleg samstilling er virkjuð með aðgerðinni **Bæta við vöru**, þú ætlar að uppfæra vörur handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Munið að velja **Til Shopify** í reitnum **Samstilling vöru**.<br>**Getur uppfært Shopify vörur** hefur ekki áhrif á samstillingu verðs, mynda eða birgðastiga sem eru grunnstillt með sjálfstæðu eftirliti.<br>Ef **Geta Uppfært Shopify vörur** er virkt verða eftirfarandi reitir á hliðinni Shopify uppfærðir á vörunni og afbrigðisstigið: **BIRGÐAHALD**, **Strikamerki,Þyngd** **·**.  **Titil,Tegund** **framleiðslu**, **Lánardrottinn** og **Lýsing** á vörunni verður einnig uppfærð ef útflutt gildi eru ekki tóm. Til að fá lýsingu þarf að virkja einhvern af **samstilltum lengdum texta**, **samstilla markaðssetningartexta** **vöru og** Samstilla víxla og eigindir, lengdan eða markaðssetningartexta verður að hafa gildi. Ef afurðin notar afbrigði er afbrigðinu bætt við eða það fjarlægt ef með þarf. <br>Ef afurðin á Shopify er grunnstillt til að nota afbrigðisfylki sem sameinar tvo eða fleiri valkosti Shopify getur Connector ekki búið til afbrigði fyrir þá vöru. Ekki [!INCLUDE[prod_short](../includes/prod_short.md)] er hægt að skilgreina valkostafylki - þess vegna notar tengið afbrigðiskótann **sem** eini valkosturinn. Hins vegar Shopify  er búist við nokkrum valkostum og neitar að búa til afbrigði ef upplýsingar um annan og aðra valkosti vantar. |
|**UoM sem afbrigði**| Þessi kostur er valinn ef flytja á suma valkosti út sem flutta inn sem mælieiningar í stað afbrigða. Sérstilla síðuna til að bæta reitnum við. Nánari upplýsingar um mælieininguna [sem afbrigði](synchronize-items.md#unit-of-measure-as-variant) .|
|**Heiti afbrigðisvalkosts fyrir UoM**| Þessi reitur er notaður með **UoM sem afbrigði** til að tilgreina hvaða valkostur inniheldur afbrigði sem tákna mælieiningar. Sjálfgefni valie er *Mælieining*. Sérstilla síðuna til að bæta reitnum við.|

> [!NOTE]
> Þegar flytja á út margar vörur og afbrigði gæti verið lokað á margar vörur. Ekki er hægt að taka útilokaðar vörur og afbrigði í verðútreikningum svo að þær séu ekki fluttar út. Tengillinn sleppir þessum vörum og afbrigðum svo að ekki þarf að afmarka þær á síðunni **Bæta við vöru til að Shopify** biðja um.

## Ítarlegar upplýsingar

### Áhrif Shopify birgðahaldseininga vöru og strikamerkja á vörpun og stofnun vara og afbrigða í Business Central

Þegar vörur eru fluttar inn frá Shopify í töflurnar **Shopify Vörur** og **Shopify Afbrigði** reynir [!INCLUDE[prod_short](../includes/prod_short.md)] að finna fyrirliggjandi skrár.

Eftirfarandi tafla sýnir muninn á valkostum í reitnum **Vörpun birgðahaldseiningar**.

|Valkostur|Áhrif á vörpun|Áhrif á sköpun|
|------|-----------------|------------------|
|**Autt**|Reiturinn Birgðahaldseining er ekki notaður í birgðavörpunarleiðinni.|Engin áhrif á stofnun vörunnar.<br>Þessi valkostur kemur í veg fyrir að hægt sé að búa til afbrigði. Þegar hún er í sölupöntun er aðeins aðalvaran notuð. Enn er hægt að kortleggja afbrigði handvirkt á síðunni **Shopify Vara**.|
|**Vörunr.**|Velja skal hvort vörunúmerið sé í reitnum Birgðahaldseining.|Engin áhrif á sköpun atriðis án afbrigða. Fyrir vörur með afbrigðum er hvert afbrigði búið til sem aðskild vara.<br>Ef Shopify vara með tvö afbrigði og birgðageymslur þeirra eru '1000' og '2000', [!INCLUDE[prod_short](../includes/prod_short.md)]  stofnar tvær vörur tölusettar '1000' og '2000'.|
|**Afbrigðiskóði**|Reiturinn Birgðahaldseining er ekki notaður í birgðavörpunarleiðinni.|Engin áhrif á stofnun vörunnar. Þegar vöruafbrigði er búið til er gildi reits birgðahaldseiningar notað sem kóði. Ef birgðahaldseiningin er auð er kóði myndaður með því að nota reitinn **Forskeyti afbrigðis**.|
|**Vörunr. + afbrigðiskóði**|Þessi kostur er valinn ef birgðahaldseiningarreiturinn inniheldur vörunúmer og vöruafbrigðiskótinn er aðgreindur með gildinu sem tilgreint er í reitnum **Skiltákn** birgðahaldseiningareits.|Þegar vara búin til er fyrsti hluti gildis reits birgðahaldseiningar tilgreindur með **Nr.** Ef reitur birgðahaldseiningar er auður er vörunúmer búið til með því að nota númeraröðina sem er skilgreind í reitnum **Vörusniðmátskóði** eða **Vörunr.** á síðunni **Uppsetning birgða**.<br>Þegar hlutur er sofnaður til notar afbrigðisaðgerðin seinni hluta gildis reits birgðahaldseiningarinnar sem **kóða**. Ef reitur birgðahaldseiningar er auður er kóði búinn til með því að nota reitinn **Forskeyti afbrigðis**.|
|**Vörunr. lánardr.**|Veldu hvort reitur birgðahaldseiningar inniheldur vörunúmer lánardrottins. Í þessu tilviki er **Lán.dr., vöru nr.** ekki notaður á síðunni fyrir **Vörukort** er **Vörunr.** af **Vörulisti lánadr.** notað. Ef skráin sem fannst í *Vörulisti lánardrottins* inniheldur afbrigðiskóða er sá kóði notaður til að varpa Shopify afbrigðið.|Ef samsvarandi lánardrottinn er til í [!INCLUDE[prod_short](../includes/prod_short.md)] er birgðahaldseiningargildið notað sem **Vörunr. lánardr.** á síðunni Birgðaspjald og sem **Vörutilvísun** í tegund **lánardrottins** . *·*  <br>Kemur í veg fyrir myndun afbrigða. Það er gagnlegt þegar þú vilt aðeins nota aðalvöruna í sölupöntuninni. Þú getur enn varpað afbrigði handvirkt á síðunni **Shopify Vara**.|
|**Strikamerki**|Veldu reitur birgðahaldseiningar innihaldi strikamerki. Leit er framkvæmd milli **Vörutilvísana** af tegundinni *strikamerki* . Ef tilvísunarskráin sem fannst inniheldur afbrigðiskóða er sá afbrigðiskóði notaður til að varpa Shopify afbrigðið.|Engin áhrif á stofnun vörunnar. <br>Kemur í veg fyrir myndun afbrigða. Það er gagnlegt þegar þú vilt aðeins nota aðalvöruna í sölupöntuninni. Þú getur enn varpað afbrigði handvirkt á síðunni **Shopify Vara**.|

Eftirfarandi tafla lýsir áhrifum reitsins **Strikamerki**.

|Áhrif á vörpun|Áhrif á sköpun|
|-----------------|------------------|
|Leit er framkvæmd á **Vörutilvísunum** innihalda strikamerkistegund sem gildið í reitnum fyrir **strikamerki** í Shopify. Ef tilvísunarskráin sem fannst inniheldur afbrigðiskóða er sá afbrigðiskóði notaður til að varpa Shopify afbrigðið.|Strikamerkið er vistað **Vörutilvísun** fyrir vöruna og vöruafbrigðið.|

> [!NOTE]  
> Þú getur sett af stað vörpun á völdum vörum/afbrigðum með því að velja **Reyna að finna vörpun vöru** eða af öllum innfluttum, óvörpuðum vörum með því að velja **Reyna að finna varpanir**.

### Yfirlit yfir reitavörpun

|Shopify|Uppruni þegar flutt er frá [!INCLUDE[prod_short](../includes/prod_short.md)]|Mark flutt er inn á [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Staða|Samkvæmt reitnum **Staða fyrir stofnaðar vörur** í **Shopify Verslunarkortinu**. Nánari upplýsingar um [tilfallandi uppfærslur á Shopify vöruhlutanum](synchronize-items.md#ad-hoc-updates-of-shopify-products) .|Ekki notað.|
|Titill | **Lýsing**. Ef tungumálakóðinn er skilgreindur og samsvarandi þýðing vöru er til verður þýðing vöru notuð í stað lýsingarinnar.|**Lýsing**|
|Titill afbrigðis | **Afbrigðiskóti**.|**Lýsing** á afbrigði|
|Heimildasamstæða|Sameinar lengda texta, markaðssetningartexta og eigindir ef samsvarandi víxlar eru gerðir virkir á Shopify verkstæðisspjaldinu. Hledur tungumálskóðanum.|Ekki notað.|
|Titill SEO-síðu|Fast gildi: autt. Nánari upplýsingar um [tilfallandi uppfærslur á Shopify vöruhlutanum](synchronize-items.md#ad-hoc-updates-of-shopify-products) .|Ekki notað.|
|Lýsing SEO-lýsigagna|Fast gildi: autt. Nánari upplýsingar um [tilfallandi uppfærslur á Shopify vöruhlutanum](synchronize-items.md#ad-hoc-updates-of-shopify-products) .|Ekki notað.|
|Geymslumiðill|**Mynd**. Fáðu frekari upplýsingar í hlutanum [Samstilla myndir af vörum](synchronize-items.md#sync-item-images)|**Mynd**|
|Verð|Í útreikningi á verði lokaviðskiptamanna eru einingarverð vöru, verðflokkur viðskiptamanna, afsláttarflokkur viðskiptamanna og gjaldmiðilskóti. Nánari upplýsingar í hlutanum [Samstilla](synchronize-items.md#sync-prices-with-shopify) verð|**Einingarverð**. Verðið er aðeins flutt inn í nýstofnaðar vörur, en það verður ekki uppfært síðar í samstillingum.|
|Samanburður á verði|Útreikningur á verði án afsláttar. Ef gildið er lægra eða jafnt **Verð** sendir tengillinn 0 (núll) í stað raunverulegs gildis.|Ekki notað.|
|Kostnaður á vöru|**Kostn.verð**|**Kostnaðarverð**. Kostnaðarverðið er aðeins flutt inn í nýstofnaðar vörur og verður ekki uppfært síðar.|
|BHE|Fræðast um birgðahaldseiningar undir **birgðahaldseiningarvörpun** í hlutanum [Flytja út vörur í Shopify](synchronize-items.md#export-items-to-shopify) hlutann.|Fræðast um birgðahaldseiningar [í áhrifum Shopify birgðahaldseininga og strikamerkis við vörpun og stofnun vara og afbrigða í Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) hlutanum.|
|Strikamerki|**Vörutilvísanir** af gerð strikamerkis.|**Vörutilvísanir** af gerð strikamerkis.|
|Birgðir verða í birgðum á| Ræðst Shopify af staðsetningum verkstæðis. Ef **Business Central Fulfillment Services** er **með svæðið Sjálfgefið vörustaðsetning** virkt eru birgðir settar í birgðir og sendar frá **Business Central Fulfillment Services**. Annars Shopify er aðalstaðsetningin eða margar birgðageymslur notaðar. Nánari upplýsingar um nálgunina [tvær til að sjá um uppfyllingarhlutann](synchronize-items.md#two-approaches-to-manage-fulfillments) .| Ekki notað.|
|Rekja magn|Samkvæmt reitnum **Birgðir raktar** á síðunni **Kort í Shopify Verslunarkort**. Fáðu frekari upplýsingar í hlutanum [Birgðir](synchronize-items.md#sync-inventory-to-shopify). Aðeins notað þegar vara er flutt út í fyrsta skipti.|Ekki notað.|
|Halda áfram að selja þegar ekki er til á lager|Samkvæmt **Sjálfgefinni birgðastefnu** í **Shopify Verslunarkortinu**.|Ekki notað.|
|Gerð|**Lýsing** á **Vöruflokkskóða**. Ef tegundin er ekki tilgreind í Shopify er henni bætt við sem sérsniðinni tegund.|**Vöruflokkskóði**. Kortlagning eftir lýsingu.|
|Lánardrottinn|**Nafn** lánardrottins frá **Nr. lánardrottins.**|**Númer lánardrottins** Vörpun eftir nafni.|
|Þyngd|**Brúttóþyngd**.|Ekki notað.|
|Skattskylt|Fast gildi: virkt.|Ekki notað.|
|Skattkóðar|**Skattflokkskóði**. Á aðeins við fyrir virðisaukaskatt. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|Ekki notað.|

### Efnisorð notenda

Farið yfir innfluttu merkin í upplýsingareitnum **Merki** á síðunni **Shopify Vara**. Á sömu síðu, til að breyta merkjum, velur þú aðgerðina **Merki**.

Ef valkosturinn **Til Shopify** er valinn í reitnum **Samstilla vöru** er úthlutuðum merkjum flutt út í Shopify við næstu samstillingu.

### Mælieining sem afbrigði

Shopify styður ekki margar mælieiningar. Ef selja á sömu vöru og til dæmis stykki og setja og nota mismunandi verð eða afslátt þarf að stofna mælieiningu sem afurðarafbrigði.
Shopify hægt er að grunnstilla tengi til að flytja út mælieiningar sem afbrigði eða flytja inn afbrigði sem mælieiningar.

Til að gera þennan möguleika virka eru reitirnir **UoM notaðir sem Afbrigði** og **Valkostaheiti** afbrigðis á **Shopify verkstæðisspjaldinu**. Reitirnir eru sjálfgefið faldir; nota sérstillingu til að bæta þeim á síðuna.

**Mælieining sem afbrigðismerki**

* Þegar vara er flutt inn í [!INCLUDE[prod_short](../includes/prod_short.md)] stofnar tengill mælieiningar. Uppfæra **þarf Magn á mælieiningu**.
* Þegar fylki afbrigðis er fylki, t.d. Color og UoM og flytja á inn vörur, ætti að stilla *Vörunr. + Afbrigðiskóti* í **reitnum Birgðahaldseining** og ganga úr skugga um að **reiturinn Birgðahaldseining** hafi Shopify sama gildi fyrir allar mælieiningar og innihalda bæði vörunúmer og afbrigðiskóta.
* Til [!INCLUDE[prod_short](../includes/prod_short.md)] ráðstöfunar er reiknað á vöru/vöruafbrigði en ekki með mælieiningu. Það þýðir að sama ráðstöfunarmagn verður úthlutað á hvert afbrigði sem táknar mælieiningu (með tilliti til **Magn á mælieiningu**) sem getur leitt til tilvika þegar tiltækt magn í Shopify er ekki nákvæmt. Dæmi: Vara sem er seld í PCS og Kassa af 6. Birgðir eru [!INCLUDE[prod_short](../includes/prod_short.md)] 6 stk. Vara flutt út í Shopify sem PRoduct með tveimur afbrigðum. Þegar birgðasamstilling hefur verið keyrð í Shopify verður birgðastigið 6 fyrir varaint PCS og 1 fyrir afbrigðisBOX. Kaupandi getur aðeins skoðað geymingu og séð að varan er fáanleg í báðum valkostum og sett pöntun fyrir 1 BOX. Næsti kaupandi mun sjá að BOX er ekki í boði, en það eru enn 6 PCS. Þetta verður fast á eftir með næstu samstillingu birgða.

### URL og forskoðunarslóð

Vara sem bætt er við Shopify eða flutt inn úr Shopify gæti verið með **URL** eða **Preview URL** fyllt út. Reiturinn **URL** verður auður ef varan er ekki birt í netversluninni– til dæmis vegna þess að staða hennar er uppkast. Veffangið **verður** tómt ef verslunin er varin með aðgangsorði – til dæmis vegna þess að þetta er þróunarverslun. Í flestum tilfellum er hægt að nota **Forskoðunarslóðina til að athuga hvernig varan lítur** út þegar hún er birt.

## Keyra samstillingu vöru

Samstillingu vöru að öllu leyti eða að hluta er hægt að framkvæma á marga mismunandi vegu.

### Upphafleg samstilling vara frá Business Central til Shopify

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Velja aðgerðina **Bæta við atriðum**.
3. Sláðu inn kóðann inn í reitinn **Verslunarkóði**. Ef þú opnar gluggann **Shopify Vara** á síðunni **Verslunarkort** verður verslunarkóðinn fylltur sjálfkrafa út.
4. Ef samskipað var mynd og samstilling birgða er hægt að hafa þær með í sama ferli. Þar með talið í sama ferli er hentugt fyrir kynningu eða þegar unnið er með smærri gögn.
5. Skilgreina vörusíur eftir þörfum. Hægt er t.d. að afmarka eftir vörunúmeri eða vöruflokkskóta.
6. Velja **Í lagi**.

Vörurnar sem verða til eru sjálfkrafa búnar til með Shopify verði. Hægt er að taka myndir og birgðastig með eftir vali sem notandi velur. Aðgerðin getur tekið nokkurn tíma ef mjög mörgum vörum er bætt við.

Einnig er hægt að samstilla eina vöru með því að velja aðgerðina **Bæta við á síðunni Shopify** Birgðaspjald **.**   

> [!NOTE]  
> Upphafleg samstilling á vörum frá [!INCLUDE[prod_short](../includes/prod_short.md)] til tekur ekki tillit Shopify til **stillinganna Samstilla vöru** og **Getur uppfært Shopify vörur** . 

### Samstilla vörur frá Shopify í Business Central

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veljið verslunina þar sem á að samtilla vörur til að opna síðuna **Shopify verslunarspjald**.
3. Veldu aðgerðina **Samstilla vörur**.

Einnig er hægt að nota aðgerðina **Samstilla vörur** á síðunni **Shopify Vörur** eða leita að runuvinnslunni **Samstilla vörur**.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

### Sértækar uppfærslur á Shopify vörum

Þegar skrárnar eru uppfærðar í töflunni **Shopify Vara** eru eftirfarandi breytingar samstilltar við Shopify.

Uppfæra:

* **Staða** - Hægt er að velja um virka, safnvistaða eða drög.
* **Titill leitarvélabestunar**
* **Lýsing leitarvélabestunar**

Eyðing:

Byggt á gildinu í **Aðgerð fyrir vörur sem voru fjarlægðar** á síðunni **Shopify Verslunarkort** er varan uppfærð í Shopify þegar skránni er eytt af síðunni **Shopify Vara**.

* **Auður**: Ekkert mun gerast. Ef nauðsyn krefur þarftu að framkvæma áskilda aðgerð frá **Shopify stjórnandamiðstöðinni**.
* **Staða drög**: Staða vörunnar í Shopify er stillt á *Drög*.
* **Staða í skjalasafn**: Varan er sett í Shopify geymslu.

## Samstilla myndir af vörum

Hægt er að stilla samstillingu mynda fyrir samstilltar vörur. Velja skal úr eftirfarandi:

* **Óvirk**: Myndsamstilling er gerð óvirk.
* **Til Shopify**: Myndir af vörum eru fluttar út í Shopify.
* **Frá Shopify**: Myndir úr Shopify eru fluttar inn í [!INCLUDE[prod_short](../includes/prod_short.md)].

Hægt er að ræsa samstillingu mynda á þann hátt sem lýst er hér að neðan.

### Samstilla vörumyndir af Shopify verslunarsíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2. Velja verslun sem á að samstilla myndir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Samstilla myndir af vörum**.

### Samstilla vörumyndir Shopify af vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu aðgerðina **Samstilla myndir af vörum**.

### Athugasemdir um samstillingu mynda

* Þegar myndir eru fluttar út frá [!INCLUDE[prod_short](../includes/prod_short.md)]  Shopify þeim sem áður voru fluttar út koma þær í staðinn fyrir þær sem áður voru fluttar út. Eldri myndirnar eru ekki lengur tiltækar.
* Ef mynd [!INCLUDE[prod_short](../includes/prod_short.md)] er eytt í Shopify eyðir myndin ekki einnig. Það þarf að eyða gömlu myndunum handvirkt í stjórnandanum **Shopify**.
* Myndir sem fluttar eru út Shopify í samræmi við Shopify kröfur fyrirtækisins. Annars er ekki hægt að flytja þær inn. Nánari upplýsingar um kröfur miðla fást með því að fara [á tegundir vörumiðla á help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## Samstilla verð við Shopify

Unnið er með útflutningsverð með þessum stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Verðhópur viðskiptavinar**|Ákveða verð fyrir vöru í Shopify. Söluverð fyrir þennan verðflokk viðskiptamanns er notaður. Ef enginn flokkur er tilgreindur er verðið á birgðaspjaldinu notað.|
|**Afsláttarflokkur viðskm.**|Ákveða afsláttinn sem nota skal þegar verð vöru er reiknað í Shopify. Afsláttarverð er geymt í reitnum **Verð** og fullt verð er geymt í reitnum **Samanburður á verði** .|
|**Leyfa línuafsl.**|Tilgreinir hvort línuafsláttur er leyfður þegar verð er reiknað fyrir Shopify. Þessi stilling á aðeins við um verð vörunnar. Verð fyrir verðflokk viðskiptamanns eru með sína eigin ví6 í línum.|
|**Verð með VSK**|Tilgreinir hvort verðútreikningar fyrir Shopify VSK eru innifalir. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|
|**VSK-viðskiptabókunarflokkur**|Tilgreinir hvaða VSK-viðskiptabókunarflokkur er notaður til að reikna verð í Shopify. Þetta ætti að vera flokkurinn sem notaður er fyrir innlenda viðskiptamenn. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|
|**Gjaldmiðilskóði**|Aðeins skal færa inn gjaldmiðilskóta ef netverslunin notar annan gjaldmiðil en staðbundinn gjaldmiðil (SGM). Tilgreindur gjaldmiðill verður að hafa stillt gengi. Ef vefverslunin þín notar sama gjaldmiðil og [!INCLUDE[prod_short](../includes/prod_short.md)] skaltu skilja þennan reit eftir auðan.|

Hægt er að flytja út verð á samstilltum vörum á tvo vegu sem lýst er hér á eftir.

### Samstilla verð Shopify af vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu **Samstilla verð til að framkvæma aðgerð Shopify**.

### Athugasemdir verðútreiknings

* Við ákvörðun verðs notar [!INCLUDE[prod_short](../includes/prod_short.md)] rökin „lægsta verð“. Hins vegar hunsar lægsta verðgrunnurinn einingarverðið sem tilgreint er á birgðaspjaldinu ef verð er skilgreint í verðflokknum. Þetta á við jafnvel þótt einingaverðið á birgðaspjaldsverðinu sé lægra.
* Til að reikna út verð stofnar tengillinn bráðabirgðasölutilboð fyrir vöruna með magnið 1 og notar staðlaðan verðútreikningsgrunn. Aðeins er notað verð og afslættir fyrir magn 1. Ekki er hægt að flytja út mismunandi verð eða afslátt eftir magni.
* Tengið sendir beiðni um að uppfæra verð í Shopify ef verð í [!INCLUDE[prod_short](../includes/prod_short.md)] hefur breyst. Ef t.d. vara og verð var samstillt og verði breytt í Shopify **Shopify**, hefur það engin áhrif á verðið þar Shopify sem nýja verðið sem tengið reiknar er það sama og verðið sem geymt er í Shopify afbrigðinu úr fyrri samstillingu. Samanburður **á verði** er aðeins uppfærður ef aðalverðið hefur breyst.

## Samstilla birgðir við Shopify

Hægt er að stilla samstillingu birgða fyrir vörur sem þegar hafa verið samstilltar. Það eru tvö skilyrði sem þarf að uppfylla:

1. Rakning birgða verður að vera virk fyrir vöru í Shopify. Ef vörur eru fluttar út tilShopify, skaltu íhuga að virkja valkostinn **Rakning birgða** á síðunni **Shopify Verslun**. Fáðu frekari upplýsingar í hlutanum [Flytja út vörur í Shopify](synchronize-items.md#export-items-to-shopify).
2. Samstilling birgða verður að vera virk fyrir **Shopify Staðsetningar**.

### Til að virkja birgðasamstillingu

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Velja verslun sem á að samstilla birgðir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veljið aðgerðina **Staðsetningar** til að opna **Shopify Staðsetningar verslunar**.
4. Veldu aðgerðina **Sækja Shopify Staðsetningar** til að flytja inn allar staðsetningarnar sem skilgreindar eru í Shopify. Þú finnur þær í stillingum fyrir [**Staðsetningar**](https://www.shopify.com/admin/settings/locations) í **Shopify Stjórnandamiðstöðinni**.
5. Í reitnum **Staðsetningarsía** er hægt að bæta við staðsetningum ef aðeins á að taka með birgðir frá tilteknum stöðum. Svo, þú gætir slegið inn *AUSTUR|VESTUR* til að gera birgðir frá aðeins þessum tveimur staðsetningm í boði fyrir sölu í gegnum netverslunina.
6. Velja skal birgðaútreikningsaðferðina sem nota á fyrir valdar Shopify birgðageymslur.
7. Gera sjálfgefna birgðageymslu **afurðar virka** ef nota á birgðageymslu til að stofna birgðafærslur og taka þátt í birgðasamstillingunni.

Þú getur ræst birgðasamstillingu á tvo vegu sem lýst er hér að neðan.

### Samstilla birgðir af Shopify síðu verslunarinnar

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2. Velja verslun sem á að samstilla birgðir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Samstilla birgðir**.

### Samstilla birgðir af Shopify vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu aðgerðina **Samstilla birgðir**.

### Athugasemdir birgða

* Tvær staðlaðar birgðaútreikningsaðferðir eru tvær: **Áætluð staða til ráðstöfunar til dags** og **Frjálsar birgðir (Ekki fráteknar)**. Með miklum möguleika er hægt að bæta við fleiri valkostum. Til að fræðast meira um möguleika er farið í [dæmi](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* Þú getur skoðað upplýsingar um birgðir sem þú fékkst frá upplýsingareitnum Shopify á síðunni **Shopify Upplýsingareitur birgða**. Í þessum upplýsingareit færðu yfirlit yfir Shopify birgða síðustu reiknuðu birgðirnar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það er ein færsla á hverjum stað.
* Ef upplýsingar um birgðir í Shopify eru aðrar en **Áætluð staða til ráðstöfunar** í [!INCLUDE[prod_short](../includes/prod_short.md)] þá verða birgðir uppfærðar í Shopify.
* Þegar nýrri birgðageymslu Shopify er bætt við þarf einnig að bæta við birgðafærslum fyrir hana. Shopify gerir það ekki sjálfkrafa fyrir fyrirliggjandi vörur og afbrigði og tengið samstillir ekki birgðastig fyrir slíkar vörur á nýja staðnum. Nánari upplýsingar eru í [Úthlutun birgðageymslna](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* Bæði **Business Central Fulfillment Services** og hefðbundnar staðsetningar eru studdar og hægt er að nota þær til afhendingar og birgða.

#### Dæmi um útreikning á áætluðum stöðu til ráðstöfunar

Til eru 10 stykki af vöru A tiltækt til ráðstöfunar og tvær útistandandi sölupantanir. Einn fyrir mánudag með magn *einn* og einn fyrir fimmtudag með magnið *Tvö*. Eftir því hvenær birgðir eru samstilltar uppfærir kerfið birgðastigið í Shopify með mismunandi magni:

|Þegar birgðastaða er keyrð|Virði sem notað er til að uppfæra birgðastig|Athugasemd|
|------|-----------------|-----------------|
|Þriðjudagur|9|Birgðir 10 mínus sölupöntun stilltar á afhendingu á mánudegi|
|Föstudagur|7|Birgðir 10 mínus báðar sölupantanir|

### Tvær aðferðir til að stjórna uppfyllingum

Tvær leiðir eru til að afgreiða uppfyllingu í Shopify:

* Shopify "innbyggður" uppfylling og birgðarakning
* Uppfylling þriðja aðila og birgðarakning

Birgðir hverrar vöru í Shopify geta verið annaðhvort í birgðum um Shopify eða með 3PL.

Ef uppfyllingin er notuð Shopify er einnig hægt að skilgreina margar birgðageymslur í Shopify. Þegar pöntun er búin til Shopify  er birgðageymsla valin eftir framboði og forgangi. Einnig er hægt að tilgreina á hvaða birgðageymslum ætlunin er að rekja tiltekna vöru, til dæmis selja aldrei frá birgðageymslunni *ShowRoom*.

Ef þú notar 3PL líkamlega meðhöndlun er sinnt af 3PL veitanda, þannig að staðsetningar er ekki þörf. 3PL verður birgðahaldseiningarreiturinn áskilinn.

Þegar ákveðið er hvaða birgðageymslu skuli rekja vöru Shopify  stofnar notandi færslur í **töflunni Birgðastig**, sem hægt er að uppfæra handvirkt með birgðastöðu.

Tengið styður báðar stillingar. Hann getur sent birgðir til margra Shopify birgðageymslna eða unnið sem uppfyllingarþjónusta.

Frá sjónarhóli [!INCLUDE[prod_short](../includes/prod_short.md)] er þegar vara er stofnuð og senda á hana á Shopify einnig að:

* Nota **skal sjálfgefna víkkun um birgðageymslu** vöru Shopify til að tilgreina hvort uppfylla eigi þessa vöru eða með 3PL. Það er alltaf **Business Central Fulfillment Service**, en það getur verið uppfyllingarþjónusta ef fleiri forrit eru uppsett. Aðeins er hægt að gera sjálfgefna birgðageymslu **vöru virka** í einni færslu ef ætlunin er að uppfylla þjónustuna. 
* nota **sjálfgefna vímu** til að tilgreina hvaða birgðageymslur á að nota til að rekja birgðir. Hægt er að kveikja á **sjálfgefinni birgðageymslu** vöru fyrir margar birgðageymslur þar sem **Þjónustuuppfylling** er gerð óvirk. Takið eftir að birgðir verða alltaf raktar fyrir aðalstaðsetningu.

#### Hver er mismunurinn?

Shopify Uppfylling er gagnleg þegar posi er notaður Shopify og margar raunverslanir eru til staðar. Starfsmenn í raunversluninni eiga að þekkja núverandi birgðir þeirra. Í þessu tilviki eru búnar til margar birgðageymslur í Shopify, margar birgðageymslur í [!INCLUDE[prod_short](../includes/prod_short.md)] og sjálfgefin birgðageymsla **gerð virk** fyrir allar þessar birgðageymslur.  

Ef vörustjórnun er unnin í [!INCLUDE[prod_short](../includes/prod_short.md)], þar sem hann getur haft eins margar birgðageymslur og þarf til að tákna dreifingarmiðstöðvar, stofnar notandinn ekki staðsetningar í Shopify, stofnar tengillinn Business Central Fulfillment Services sjálfkrafa og hægt er að tengja birgðir með birgðageymsluafmörkunum frá nokkrum birgðageymslum í eina uppfyllingarþjónustufærslu. Þar af leiðandi Shopify hafa engar upplýsingar um hvaðan vörur eru sendar – þar eru aðeins rakningarupplýsingar, en [!INCLUDE[prod_short](../includes/prod_short.md)] inn er hægt að velja út frá framboði og nágrenni við áfangastaðarstaðinn.

#### Dæmi um notkun sjálfgefinnar vísbreiðslu vörustaðsetningar

Þegar aðgerðin **Sækja Shopify birgðageymslur** hefur verið valin á síðunni **Shopify Birgðageymslur** sjást eftirfarandi birgðageymslur:

|Nafn|Er uppfyllingarþjónusta|Er aðal|
|------|-----------------|-----------------|
|Helstu| |**Já**|
|Second| | |
|Uppfyllingarþjónusta Business Central|**Já**| |

Við skulum skoða áhrif þess að gera vífæringu sjálfgefinnar birgðageymslu afurðar virka:

|Heiti birgðageymslna þar sem vísbending um sjálfgefna birgðageymslu er virkjuð|Áhrif á hvernig vara er búin til í Shopify|
|------|-----------------|
|Helstu| Birgðir verða geymdar í: Margar birgðageymslur; Valdar birgðageymslur: Aðalstaðsetning (aðal) |
|Aðal og Í öðru lagi| Birgðir verða geymdar í: Margar birgðageymslur; Valdar staðsetningar: Aðalstaðsetning og Í öðru lagi |
|Uppfyllingarþjónusta Business Central|Birgðir verða birgðir á: Business Central Fulfillment Service; Valdar staðsetningar: (App) Business Central Fulfillment Service|
|Uppfyllingarþjónusta Business Central og Aðal| Villa: Ekki er hægt að nota staðlaðar Shopify birgðageymslur með þjónustustaðsetningum uppfylla|

## Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
