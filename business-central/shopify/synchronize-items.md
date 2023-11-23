---
title: Samstilla vörur og birgðir
description: Setja upp og keyra samstillingar vara milli Shopify og Business Central
ms.date: 11/17/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="synchronize-items-and-inventory"></a>Samstilla vörur og birgðir

 **Hlutirnir** í [!INCLUDE[prod_short](../includes/prod_short.md)] jafngilda *vörunum* í Shopify og innihalda líkamlegar vörur, stafrænt niðurhal, þjónustu og gjafakort sem þú selur. Það eru tvær meginástæður til að samstilla hluti:

1. Gagnastjórnun fer fyrst og fremst fram í [!INCLUDE[prod_short](../includes/prod_short.md)]. Þú þarft að flytja öll eða sum gögn þaðan út í Shopify og gera þau sýnileg. Hægt er að flytja út vöruheiti, lýsingu, mynd, verð, framboð, afbrigði, upplýsingar um lánardrottinn og strikamerki. Þegar flutt hefur verið út er hægt að fara yfir atriðin eða gera þau sýnileg strax.
2. Þegar pöntun frá Shopify er flutt inn eru upplýsingarnar um hlutina mjög mikilvægar fyrir frekari skjalavinnslu í [!INCLUDE[prod_short](../includes/prod_short.md)].

Sviðsmyndirnar tvær á undan eru alltaf virkar.

Þriðja sviðsmynd er að hafa umsjón með gögnum í Shopify en flytja þau atriði inn í heildsölu til [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi sviðsmynd getur verið gagnleg fyrir tilvik gagnaflutnings, svo sem þegar þú vilt tengja núverandi vefverslun við nýtt [!INCLUDE[prod_short](../includes/prod_short.md)] umhverfi.

## <a name="define-item-synchronizations"></a>Skilgreina vörusamstillingar

1. Í leitinni velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn og opna **Shopify Verslun**. Opna verslunina sem á að stilla samstillingu vöru fyrir.
2. Í reitnum **Samstilla vöru** skal velja nauðsynlegan valkost.

   Eftirfarandi tafla lýsir valkostunum.

|Valkostur|Lýsing|
|------|-----------|
|**Autt**| Vörur eru fluttar inn um leið og pantanir eru fluttar inn. Vörur eru fluttar út til Shopify ef notandi keyrir aðgerðina **Bæta við vöru** á síðunni **Shopify Vörur**. Þessi valkostur er sjálfgefið ferli.|
|**Til Shopify**| Þessi kostur er valinn ef upphafleg samstilling er virkjuð með aðgerðinni **Bæta við vöru**, þú ætlar að uppfæra vörur handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Munið að virkja reitinn **Getur uppfært Shopify vöru**. Ef það er ekki virkt jafngildir það valkostinum **Autt** (sjálfgefið ferli). Fáðu frekari upplýsingar í hlutanum [Flytja út vörur í Shopify](synchronize-items.md#export-items-to-shopify).|
|**Frá Shopify**| Þessi kostur er valinn ef ætlunin er að flytja vörur inn frá Shopify í lausasölu, annaðhvort handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Fáðu frekari upplýsingar í hlutanum [Flytja inn atriði frá Shopify](synchronize-items.md#import-items-from-shopify).|

> [!NOTE]
> Breytir **Samstillingaratriði** úr **Frá Shopify** í **Í Shopify** vann það hefur ekki áhrif nema þú virkjar **Getur uppfært Shopify vörur**. 

## <a name="import-items-from-shopify"></a>Flytja inn atriði úr Shopify

Fyrst skaltu flytja inn vörur annað hvort í lausu frá Shopify eða ásamt pöntunum til að bæta þeim við töfluna **Shopify Vara** og **Shopify Afbrigði**. Kortleggðu síðan innfluttar vörur og afbrigði við hluti og afbrigði í [!INCLUDE[prod_short](../includes/prod_short.md)]. Stjórna ferlinu með því að nota eftirfarandi stillingar:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Búa til óþekktar vörur sjálfvirkt**|Þegar Shopify vörur og afbrigði eru flutt inn í [!INCLUDE[prod_short](../includes/prod_short.md)], reynir [!INCLUDE[prod_short](../includes/prod_short.md)] aðgerðin fyrst að finna samsvarandi skrá í vörulistanum. **Vörpun birgðahaldseiningar** hefur áhrif á hvernig samsvörun er framkvæmd og býr til nýja vöru og/eða vöruafbrigði. Virkjaðu þennan valkost ef búa á til nýja vöru eða þegar samsvarandi skrá er ekki til. Nýja varan er búið til með því að nota innflutt gögn og **Vörusniðmátskóða**. Ef þessi valkostur er ekki virkur þarftu að búa til vöru handvirkt og nota aðgerðina **Varpa vöru** á síðunni **Shopify Vara**.|
|**Vörusniðmátskóði**|Notaðu þennan reit með  **Búa til óþekkta hluti sjálfkrafa** rofa.<br>Veldu sniðmátið sem á að nota fyrir vörur sem eru sjálfkrafa búnar til.|
|**BHE-vörpun**|Veljið hvernig nota á gildi **Birgðarhaldseiningar** sem flutt er inn frá Shopify við vörpun og stofnun vörunnar/afbrigðisins. Frekari upplýsingar er að finna í hlutanum [Áhrif Shopify birgðarhaldseininga vöru og strikamerkja á vörpun og stofnun vöru og afbrigða í Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Reitaskiltákn birgðahaldseiningar**|Notaðu þennan reit með **SKU Mapping** stillt á **[Item. Nei + afbrigðiskóði](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)** valkostur.<br>Skilgreindu skilju sem nota á til að skipta birgðahaldseiningunni.<br>Þannig að ef Shopify þú býrð til afbrigðið með birgðahaldseiningu „1000/001“ þá skrifar þú „/“ reitinn **Reitaskiltákn birgðahaldseiningar** til að gera vörunúmerið í [!INCLUDE[prod_short](../includes/prod_short.md)] „1000“ og afbrigðiskóðann „001“.|
|**Forskeyti afbrigðis**|Notið ásamt **Vörpun birgðahaldseiningar** að stilla annað hvort valkostinn **Afbrigðiskóði** eða **Vörunr. + afbrigðiskóði** sem varavalkost þegar birgðahaldseiningin frá Shopify er auð.<br>Ef þú vilt búa til vöruafbrigði sjálfkrafa í [!INCLUDE[prod_short](../includes/prod_short.md)] þarftu að slá inn gildi í **Kóða**. Sjálfgefið er að nota gildið sem skilgreint er í reit birgðahaldseiningar flutt inn frá Shopify. Ef birgðahaldseiningin er auð mun hún hins vegar búa til kóða sem byrjar á skilgreinda forskeyti afbrigðisins og „001“.|
|**Shopify Get ég uppfært atriði**|Þessi kostur er valinn ef þú vilt uppfæra vörur og/eða afbrigði sjálfkrafa.|

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Áhrif Shopify birgðahaldseininga vöru og strikamerkja á vörpun og stofnun vara og afbrigða í Business Central

Þegar vörur eru fluttar inn frá Shopify í töflurnar **Shopify Vörur** og **Shopify Afbrigði** reynir [!INCLUDE[prod_short](../includes/prod_short.md)] að finna fyrirliggjandi skrár.

Eftirfarandi tafla sýnir muninn á valkostum í reitnum **Vörpun birgðahaldseiningar**.

|Valkostur|Áhrif á vörpun|Áhrif á sköpun|
|------|-----------------|------------------|
|**Autt**|SKU reiturinn er ekki notaður í vöruvörpunarrútínu.|Engin áhrif á stofnun vörunnar.<br>Þessi valkostur kemur í veg fyrir að hægt sé að búa til afbrigði. Aðeins aðalvaran er notuð í sölupöntun. Enn er hægt að kortleggja afbrigði handvirkt á síðunni **Shopify Vara**.|
|**Vörunr.**|Veldu hvort að reitur birgðahaldseiningar innihaldi vörunúmerið|Engin áhrif á sköpun atriðis án afbrigða. Fyrir vörur með afbrigðum er hvert afbrigði búið til sem aðskild vara.<br>Ef Shopify er með vöru með tveimur afbrigðum og vörunúmer þeirra eru '1000' og '2000', mun [!INCLUDE[prod_short](../includes/prod_short.md)] búa til tvo hluti sem eru númeraðir '1000' og '2000'.|
|**Afbrigðiskóði**|SKU reiturinn er ekki notaður í vöruvörpunarrútínu.|Engin áhrif á stofnun vörunnar. Þegar vöruafbrigði er búið til er gildi reits birgðahaldseiningar notað sem kóði. Ef birgðahaldseiningin er auð er kóði myndaður með því að nota reitinn **Forskeyti afbrigðis**.|
|**Vörunr. + afbrigðiskóði**|Veldu þennan valkost ef SKU reiturinn inniheldur vörunúmer og vöruafbrigðiskóði er aðskilinn með gildinu sem er skilgreint í  **SKU Field Separator** reitnum.|Þegar vara búin til er fyrsti hluti gildis reits birgðahaldseiningar tilgreindur með **Nr.** Ef reitur birgðahaldseiningar er auður er vörunúmer búið til með því að nota númeraröðina sem er skilgreind í reitnum **Vörusniðmátskóði** eða **Vörunr.** á síðunni **Uppsetning birgða**.<br>Þegar hlutur er sofnaður til notar afbrigðisaðgerðin seinni hluta gildis reits birgðahaldseiningarinnar sem **kóða**. Ef reitur birgðahaldseiningar er auður er kóði búinn til með því að nota reitinn **Forskeyti afbrigðis**.|
|**Vörunr. lánardr.**|Veldu hvort reitur birgðahaldseiningar inniheldur vörunúmer lánardrottins. Í þessu tilviki er **Lán.dr., vöru nr.** ekki notaður á síðunni fyrir **Vörukort** er **Vörunr.** af **Vörulisti lánadr.** notað. Ef skráin sem fannst í *Vörulisti lánardrottins* inniheldur afbrigðiskóða er sá kóði notaður til að varpa Shopify afbrigðið.|Ef samsvarandi söluaðili er til í [!INCLUDE[prod_short](../includes/prod_short.md)], verður SKU gildið notað sem **vörunúmer söluaðila** á **vörunni Card** síðu og sem **Item Reference** af *seljandi* gerð. <br>Kemur í veg fyrir myndun afbrigða. Það er gagnlegt þegar þú vilt aðeins nota aðalvöruna í sölupöntuninni. Þú getur enn varpað afbrigði handvirkt á síðunni **Shopify Vara**.|
|**Strikamerki**|Veldu reitur birgðahaldseiningar innihaldi strikamerki. Leitað er meðal **Item References** af *strikamerkja* gerðinni. Ef tilvísunarskráin sem fannst inniheldur afbrigðiskóða er sá afbrigðiskóði notaður til að varpa Shopify afbrigðið.|Engin áhrif á stofnun vörunnar. <br>Kemur í veg fyrir myndun afbrigða. Það er gagnlegt þegar þú vilt aðeins nota aðalvöruna í sölupöntuninni. Þú getur enn varpað afbrigði handvirkt á síðunni **Shopify Vara**.|

Eftirfarandi tafla lýsir áhrifum reitsins **Strikamerki**.

|Áhrif á vörpun|Áhrif á sköpun|
|-----------------|------------------|
|Leit er framkvæmd á **Vörutilvísunum** innihalda strikamerkistegund sem gildið í reitnum fyrir **strikamerki** í Shopify. Ef tilvísunarskráin sem fannst inniheldur afbrigðiskóða er sá afbrigðiskóði notaður til að varpa Shopify afbrigðið.|Strikamerkið er vistað **Vörutilvísun** fyrir vöruna og vöruafbrigðið.|

> [!NOTE]  
> Þú getur sett af stað vörpun á völdum vörum/afbrigðum með því að velja **Reyna að finna vörpun vöru** eða af öllum innfluttum, óvörpuðum vörum með því að velja **Reyna að finna varpanir**.

## <a name="export-items-to-shopify"></a>Flytja vörur í Shopify

Það eru margar leiðir til að flytja hluti til Shopify: 

- Notaðu **Bæta hlut við Shopify** aðgerðina beint af **Atriðispjaldinu** síðunni. 
- Notaðu aðgerðina **Bæta við hlut** á síðunni **Shopify Vörur** . 
- Keyrðu hlutsamstillingu einu sinni eða ítrekað með sjálfvirkni. 

Sama hvernig þú flytur út vörur, eru tilteknar vöruupplýsingar fluttar á Shopify vörulistann eftir vali þínu á stillingum fyrir samstillingu vöru.

>[!IMPORTANT]
>Varan verður aðeins bætt við **Netverslun** sölurásina. Þú þarft að birta vörur á aðrar sölurásir, eins og Shopify POS, frá Shopify.

Þú stjórnar ferlinu við að flytja út vörur með þessum stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Samstilla lengdan texta vöru**|Veldu þennan reit til að samstilla útbreiddan texta hlutarins. Þar sem því verður bætt við **Description** reitinn getur hann innihaldið HTML kóða. |
|**Samstilla vörueigindir**|Veldu þennan reit til að samstilla eiginleika vörunnar. Eigindir eru sniðnir sem töflu og innifalin í reitnum **Lýsing**  í Shopify.|
|**Samstilla vörumarkaðstexta**|Veldu þennan reit til að samstilla markaðstexta fyrir vöruna. Þrátt fyrir að markaðstexti sé eins konar lýsing er hann öðruvísi en  **Lýsing** reit hlutarins. Reiturinn **Lýsing**  er venjulega notaður sem hnitmiðað nafn til að auðkenna vöruna fljótt. Markaðstextinn er aftur á móti ríkari og lýsandi. Tilgangur þess er að bæta við markaðs- og kynningarefni. Þennan texta má síðan birta með hlutnum í Shopify. Það eru tvær leiðir til að búa til markaðstextann. Notaðu Copilot, sem stingur upp á gervigreindum texta fyrir þig, eða byrjaðu frá grunni.|
|**Kóði tungumáls**|Veldu þennan reit ef þú vilt að þýddar útgáfur séu notaðar fyrir titil, eiginleika og útbreiddan texta.|
|**BHE-vörpun**|Velja hvernig á að þýða reit birgðahaldseiningar í Shopify. Studdir valkostir eru:<br> - **Vörunr.** til að nota vörunr. bæði fyrir vörur og afbrigði.<br> - **Vörunr. + afbrigðiskóði** til að búa til birgðarhaldseiningu með því að samstilla gildi tveggja reita. Fyrir hluti án afbrigða er eingöngu notað vörunúmerið.<br>- **Vöru seljanda nr.** til að nota vörusölunúmerið sem skilgreint er á **vöruspjaldinu** fyrir bæði vörur og afbrigði.<br> - **Strikamerki** til að nota strikamerkistegundina **Vörutilvísun**. Þessi valkostur tekur mið af afbrigðum.<br>Ef  **Can Update Shopify Products** er virkjuð verða breytingar á reitnum **SKU Mapping**  dreift til Shopify eftir næstu samstillingu fyrir allar vörur og afbrigði sem skráðar eru á **Shopify Vörur** síðunni fyrir valda verslun.|
|**Reitaskiltákn birgðahaldseiningar**|Skilgreindu skilju fyrir valkostinn **Vörunr. + afbrigðiskóði**.|
|**Birgðir raktar**| Veldu hvernig kerfið á að fylla út reitinn **Rekja birgðir** vörur sem eru fluttar út til Shopify. Hægt er að uppfæra framboðsupplýsingar [!INCLUDE[prod_short](../includes/prod_short.md)] fyrir vörur í Shopify þar sem rakning birgða er virk. Fáðu frekari upplýsingar í hlutanum [Birgðir](synchronize-items.md#sync-inventory-to-shopify).|
|**Sjálfgefin birgðastefna**|Veldu *Neita* til að koma í veg fyrir neikvæðar birgðir á Shopify hliðinni. <br>Ef  **Can Update Shopify Products** er virkt munu breytingar á **Sjálfgefin birgðareglur** reitnum vera dreift til Shopify eftir næstu samstillingu fyrir allar vörur og afbrigði sem skráðar eru á **Shopify Vörur** síðunni fyrir valda verslun.|
|**Getur uppfært Shopify Vörur**|Skilgreindu þennan reit ef [!INCLUDE[prod_short](../includes/prod_short.md)] getur aðeins búið til hluti eða getur líka uppfært hluti. Þessi kostur er valinn ef upphafleg samstilling er virkjuð með aðgerðinni **Bæta við vöru**, þú ætlar að uppfæra vörur handvirkt með því að nota aðgerðina **Samstilla vöru** eða með því að nota verkröðina fyrir endurteknar uppfærslur. Munið að velja **Til Shopify** í reitnum **Samstilling vöru**.<br>**Getur uppfært Shopify Vörur** hefur ekki áhrif á samstillingu verðs, mynda eða birgðastiga, sem eru stillt af óháðum stýribúnaði.<br>Ef **Can Update Shopify Products** er virkt verða eftirfarandi reitir  Shopify megin uppfærðir á vöru og ef þörf krefur:  **SKU**, **Strikamerki**, **Þyngd**.  **Titill**, **Vörutegund**, **Sala**,  **Lýsing** á vöru verður einnig uppfærð ef útflutt gildi eru ekki tóm. Fyrir lýsingu þýðir þetta að þú þarft að virkja eitthvað af  **Sync Item Extended Text**, **Sync Item Marketing Text**,  **Samstillingareiginleikar** skipta og eiginleikar, útbreiddur eða markaðstexti verða að hafa gildi. Ef varan notar afbrigði er afbrigði bætt við eða fjarlægt ef þörf krefur. <br>Ef varan á Shopify  er stillt til að nota afbrigðisfylki sem sameinar tvo eða fleiri valkosti getur Shopify tengilið ekki búið til afbrigði fyrir þá vöru. Í [!INCLUDE[prod_short](../includes/prod_short.md)] er engin leið að skilgreina valmöguleikafylki, þess vegna notar tengibúnaður **afbrigðiskóðann** sem eina valmöguleikann. Hins vegar Shopify býst við nokkrum valmöguleikum og neitar að búa til afbrigði ef upplýsingar um annan og aðra valkosti vantar. |

### <a name="fields-mapping-overview"></a>Yfirlit yfir kortlagningu reita

|Shopify|Uppruni þegar flutt er frá [!INCLUDE[prod_short](../includes/prod_short.md)]|Mark flutt er inn á [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Staða|Samkvæmt reitnum **Staða fyrir stofnaðar vörur** í **Shopify Verslunarkortinu**. Frekari upplýsingar er að finna í [Ad hoc uppfærslur á Shopify vörum](synchronize-items.md#ad-hoc-updates-of-shopify-products) hlutanum.|Ekki notað.|
|Titill | **Lýsing**. Ef tungumálakóðinn er skilgreindur og samsvarandi þýðing vöru er til verður þýðing vöru notuð í stað lýsingarinnar.|**Lýsing**|
|Titill afbrigðis | **Afbrigðiskóði**.|**Lýsing** af afbrigði|
|Heimildasamstæða|Sameinar útbreiddan texta, markaðstexta og eiginleika ef þú virkjar samsvarandi rofa á  Shopify verslunarspjaldinu. Hledur tungumálskóðanum.|Ekki notað.|
|Titill SEO-síðu|Fast gildi: autt. Frekari upplýsingar er að finna í [Ad hoc uppfærslur á Shopify vörum](synchronize-items.md#ad-hoc-updates-of-shopify-products) hlutanum.|Ekki notað.|
|Lýsing SEO-lýsigagna|Fast gildi: autt. Frekari upplýsingar er að finna í [Ad hoc uppfærslur á Shopify vörum](synchronize-items.md#ad-hoc-updates-of-shopify-products) hlutanum.|Ekki notað.|
|Geymslumiðill|**Mynd**. Fáðu frekari upplýsingar í hlutanum [Samstilla myndir af vörum](synchronize-items.md#sync-item-images)|**Mynd**|
|Verð|Útreikningur lokaverðs tekur til einingaverðs vöru, verðflokks viðskiptavina, afsláttarflokks viðskiptavina og gjaldmiðilskóða. Frekari upplýsingar eru í kaflanum [Samstillingarverð](synchronize-items.md#sync-prices-with-shopify) |**Einingarverð**. Verðið er aðeins flutt inn í nýbúið atriði, en það verður ekki uppfært í síðari samstillingum.|
|Samanburður á verði|Útreikningur á verði án afsláttar.|Ekki notað.|
|Kostnaður á vöru|**Kostn.verð**|**Einingakostnaður**. Einingakostnaðurinn er aðeins fluttur inn í nýstofnaðar vörur og hann verður ekki uppfærður í síðari samstillingum.|
|BHE|Kynntu þér SKU undir **SKU kortlagning** í hlutanum [Flytja út hluti í Shopify](synchronize-items.md#export-items-to-shopify) .|Lærðu um SKUs í [Áhrif Shopify vöru SKUs og strikamerkjum á kortlagningu og sköpun af hlutum og afbrigðum í Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) hlutanum.|
|Strikamerki|**Vörutilvísanir** af gerð strikamerkis.|**Vörutilvísanir** af gerð strikamerkis.|
|Birgðir verða tilbúnar kl| Fer eftir Shopify verslunarstöðum. Ef **Business Central Fulfillment Services** hefur **Sjálfgefinn** reitinn virkan, þá verða birgðir geymdar og sendar frá **Business Central Fulfillment Services** annars Shopify aðal staðsetning eða margar staðsetningar verða notaðar.| Ekki notað.|
|Rekja magn|Samkvæmt reitnum **Birgðir raktar** á síðunni **Kort í Shopify Verslunarkort**. Fáðu frekari upplýsingar í hlutanum [Birgðir](synchronize-items.md#sync-inventory-to-shopify). Aðeins notað þegar þú flytur út vöru í fyrsta skipti.|Ekki notað.|
|Halda áfram að selja þegar ekki er til á lager|Samkvæmt **Sjálfgefinni birgðastefnu** í **Shopify Verslunarkortinu**.|Ekki notað.|
|Gerð|**Lýsing** á **Vöruflokkskóða**. Ef tegundin er ekki tilgreind í Shopify er henni bætt við sem sérsniðinni gerð.|**Vöruflokkskóði**. Kortlagning eftir lýsingu.|
|Lánardrottinn|**Nafn** lánardrottins frá **Nr. lánardrottins.**|**Númer lánardrottins** Vörpun eftir nafni.|
|Þyngd|**Brúttóþyngd**.|Ekki notað.|
|Skattskylt|Fast gildi: virkt.|Ekki notað.|
|Skattkóðar|**Skattflokkskóði**. Á aðeins við fyrir virðisaukaskatt. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|Ekki notað.|


### <a name="tags"></a>Efnisorð notenda

Farið yfir innfluttu merkin í upplýsingareitnum **Merki** á síðunni **Shopify Vara**. Á sömu síðu, til að breyta merkjum, velur þú aðgerðina **Merki**.
Ef valkosturinn **Til Shopify** er valinn í reitnum **Samstilla vöru** er úthlutuðum merkjum flutt út í Shopify við næstu samstillingu.

## <a name="run-item-synchronization"></a>Keyra samstillingu vöru

Samstillingu vöru að öllu leyti eða að hluta er hægt að framkvæma á marga mismunandi vegu.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Upphafleg samstilling vara frá Business Central til Shopify

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Velja aðgerðina **Bæta við atriðum**.
3. Sláðu inn kóðann inn í reitinn **Verslunarkóði**. Ef þú opnar gluggann **Shopify Vara** á síðunni **Verslunarkort** verður verslunarkóðinn fylltur sjálfkrafa út.
4. Ef þú stilltir mynd- og birgðasamstillingu geturðu sett þær inn í sama ferli. Að taka þau með í sama ferli er þægilegt fyrir kynningaratburðarás eða þegar um er að ræða minna magn af gögnum. 
5. Skilgreina vörusíur eftir þörfum. Til dæmis er hægt að sía eftir vörunr. eða vöruflokkskóða.
6. Velja **Í lagi**.

Hlutirnir sem myndast eru sjálfkrafa búnir til í Shopify með verðum. Það fer eftir vali sem þú tókst, myndir og birgðastig gætu verið innifalin. Aðgerðin getur tekið nokkurn tíma ef mjög mörgum vörum er bætt við.

### <a name="sync-products-from-shopify-to-business-central"></a>Samstilla vörur frá Shopify í Business Central

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veljið verslunina þar sem á að samtilla vörur til að opna síðuna **Shopify verslunarspjald**.
3. Veldu aðgerðina **Samstilla vörur**.

Einnig er hægt að nota aðgerðina **Samstilla vörur** á síðunni **Shopify Vörur** eða leita að runuvinnslunni **Samstilla vörur**.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

### <a name="url-and-preview-url"></a>URL og Preview URL

Atriði bætt við Shopify eða flutt inn af Shopify  gæti verið með **vefslóðinni** eða **Forskoðunarslóðinni** fjölmennt. Reiturinn **URL**  verður auður ef vara er ekki birt í netverslun, til dæmis vegna þess að staða hennar er drög.  **URL** verður tóm ef verslun er varin með lykilorði, til dæmis vegna þess að þetta er þróunarverslun. Í flestum tilfellum geturðu notað **Forskoðunarslóð** til að athuga hvernig varan mun líta út þegar hún er birt.

### <a name="ad-hoc-updates-of-shopify-products"></a>Sértækar uppfærslur á Shopify vörum

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

## <a name="sync-item-images"></a>Samstilla myndir af vörum

Hægt er að stilla samstillingu mynda fyrir samstilltar vörur. Velja skal úr eftirfarandi:

* **Slökkt** - Samstilling myndar er óvirk.
* **Til Shopify** - Myndir af vörum fluttar yfir í Shopify.
* **Úr Shopify** - Myndir frá Shopify er flutt inn í [!INCLUDE[prod_short](../includes/prod_short.md)].

Hægt er að ræsa samstillingu mynda á þann hátt sem lýst er hér að neðan.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Samstilla vörumyndir af Shopify verslunarsíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2. Velja verslun sem á að samstilla myndir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Samstilla myndir af vörum**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Samstilla vörumyndir Shopify af vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu aðgerðina **Samstilla myndir af vörum**.

### <a name="image-synchronization-remarks"></a>Athugasemdir um samstillingu mynda

* Þegar þú flytur út myndir úr [!INCLUDE[prod_short](../includes/prod_short.md)] í Shopify, koma myndirnar í stað þeirra sem þú fluttir út áður. Fyrri myndirnar eru ekki lengur tiltækar.
* Ef þú eyðir mynd í [!INCLUDE[prod_short](../includes/prod_short.md)] er myndinni í Shopify ekki líka eytt. Þú þarft að eyða gömlum myndum handvirkt í **Shopify Admin**.
* Myndir sem þú flytur út á Shopify verða að vera í samræmi við kröfur Shopify. Annars geturðu ekki flutt þau inn. Til að læra meira um fjölmiðlakröfur skaltu fara í [vörumiðlategundir á help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify"></a>Samstilla verð við Shopify

Þú stjórnar ferlinu við að flytja út verð með þessum stillingum:

|Svæði|Heimildasamstæða|
|------|-----------|
|**Verðhópur viðskiptavinar**|Ákveða verð fyrir vöru í Shopify. Söluverð fyrir þennan verðflokk viðskiptamanns er notaður. Ef enginn hópur er tilgreindur er notað verð á vöruspjaldi.|
|**Afsláttarflokkur viðskm.**|Ákveðið afsláttinn sem á að nota þegar verð á vöru í Shopify er reiknað út. Afsláttarverð eru geymd í reitnum **Verð**  og fullt verð er geymt í reitnum **Samburður á verði** .|
|**Leyfa línudisk.**|Tilgreinir hvort þú leyfir línuafslátt þegar þú reiknar út verð fyrir Shopify. Þessi stilling á aðeins við um verð á vörunni. Verð fyrir verðflokk viðskiptavina hafa sinn eigin skipta á línum.|
|**Verð með vsk**|Tilgreinir hvort verðútreikningar fyrir Shopify innifali vsk. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|
|**VSK Business Posting Group**|Tilgreinir hvaða VSK fyrirtækjabókunarflokkur er notaður til að reikna út verð í Shopify. Þetta ætti að vera hópurinn sem þú notar fyrir innlenda viðskiptavini. Frekari upplýsingar er að finna á [Setja upp skatta](setup-taxes.md).|
|**Gjaldmiðilskóði**|Sláðu aðeins inn gjaldmiðilskóða ef netverslun þín notar annan gjaldmiðil en staðbundinn gjaldmiðil (LCY). Tilgreindur gjaldmiðill verður að hafa stillt gengi. Ef vefverslunin þín notar sama gjaldmiðil og [!INCLUDE[prod_short](../includes/prod_short.md)] skaltu skilja þennan reit eftir auðan.|

Þú getur flutt út verð fyrir samstilltar vörur á tvo vegu sem lýst er hér að neðan.

### <a name="sync-prices-from-the-shopify-products-page"></a>Samstilla verð Shopify af vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu **Samstilla verð til að framkvæma aðgerð Shopify**.

### <a name="price-calculation-remarks"></a>Athugasemdir verðútreiknings

* Við ákvörðun verðs notar [!INCLUDE[prod_short](../includes/prod_short.md)] rökin „lægsta verð“. Hins vegar hunsar rökfræði lægsta verðs einingaverðið sem er skilgreint á vöruspjaldinu ef verð er skilgreint í verðflokknum. Þetta á við jafnvel þótt einingarverð frá vörukortaverði sé lægra.
* Til að reikna út verð, býr tengilinn til tímabundið sölutilboð fyrir vöruna með magninu 1 og notar staðlaða verðútreikningsrökfræði. Aðeins eru notuð verð og afslættir sem eiga við um magn 1. Þú getur ekki flutt út mismunandi verð eða afslætti miðað við magn.

## <a name="sync-inventory-to-shopify"></a>Samstilla birgðir við Shopify

Hægt er að stilla samstillingu birgða fyrir vörur sem þegar hafa verið samstilltar. Það eru tvö skilyrði sem þarf að uppfylla:

1. Rakning birgða verður að vera virk fyrir vöru í Shopify. Ef vörur eru fluttar út tilShopify, skaltu íhuga að virkja valkostinn **Rakning birgða** á síðunni **Shopify Verslun**. Fáðu frekari upplýsingar í hlutanum [Flytja út vörur í Shopify](synchronize-items.md#export-items-to-shopify).
2. Samstilling birgða verður að vera virk fyrir **Shopify Staðsetningar**.

### <a name="to-enable-inventory-sync"></a>Til að virkja birgðasamstillingu

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Velja verslun sem á að samstilla birgðir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veljið aðgerðina **Staðsetningar** til að opna **Shopify Staðsetningar verslunar**.
4. Veldu aðgerðina **Sækja Shopify Staðsetningar** til að flytja inn allar staðsetningarnar sem skilgreindar eru í Shopify. Þú finnur þær í stillingum fyrir [**Staðsetningar**](https://www.shopify.com/admin/settings/locations) í **Shopify Stjórnandamiðstöðinni**.
5. Í reitnum **Staðsetningarsía** er hægt að bæta við staðsetningum ef aðeins á að taka með birgðir frá tilteknum stöðum. Svo, þú gætir slegið inn *AUSTUR|VESTUR* til að gera birgðir frá aðeins þessum tveimur staðsetningm í boði fyrir sölu í gegnum netverslunina.
6. Veldu stofnútreikningsaðferðina sem á að nota fyrir valda Shopify staðsetningar.
7. Virkja **Sjálfgefið** ef þú vilt að staðsetning sé notuð til að búa til birgðaskrár og taka þátt í birgðasamstillingu. Virkjaðu **Sjálfgefið** fyrir **Business Central Fulfillment Services** til að búa til birgðaskrá sem táknar uppfyllingarþjónustu, annars verður birgðaskrá fyrir aðal shopify staðsetning og allar venjulegar staðsetningar þar sem kveikt er á **Sjálfgefið** .


Þú getur ræst birgðasamstillingu á tvo vegu sem lýst er hér að neðan.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Samstilla birgðir af Shopify síðu verslunarinnar

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2. Velja verslun sem á að samstilla birgðir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Samstilla birgðir**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Samstilla birgðir af Shopify vörusíðunni

1. Farðu í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Veldu aðgerðina **Samstilla birgðir**.

### <a name="inventory-remarks"></a>Athugasemdir birgða

* Hefðbundin birgðareikningsaðferð er **Áætluð laus staða á dagsetningu**. Með stækkanleika geturðu bætt við fleiri valkostum. Til að læra meira um stækkanleika skaltu fara í [dæmi](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* Þú getur skoðað upplýsingar um birgðir sem þú fékkst frá upplýsingareitnum Shopify á síðunni **Shopify Upplýsingareitur birgða**. Í þessum upplýsingareit færðu yfirlit yfir Shopify birgða síðustu reiknuðu birgðirnar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það er ein færsla á hverjum stað.
* Ef upplýsingar um birgðir í Shopify eru aðrar en **Áætluð staða til ráðstöfunar** í [!INCLUDE[prod_short](../includes/prod_short.md)] þá verða birgðir uppfærðar í Shopify.
* Þegar þú bætir við nýrri staðsetningu í Shopify þarftu líka að bæta við birgðaskrám fyrir hana. Shopify gerir það ekki sjálfkrafa fyrir núverandi vörur og afbrigði og tengið mun ekki samstilla birgðastig fyrir slíka hluti á nýjum stað. Til að fá frekari upplýsingar skaltu fara í [Að úthluta birgðum á staðsetningar](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* Bæði **Business Central Fulfillment Services** og venjulegar staðsetningar eru studdar og hægt er að nota þær fyrir sendingu og birgðahald.

#### <a name="example-of-calculation-of-projected-available-balance"></a>Dæmi um útreikning á áætlaðri tiltækri stöðu

Það eru 10 stykki af vöru A í boði og tvær útistandandi sölupantanir. Einn fyrir mánudag með magni *Einn* og einn fyrir fimmtudag með magni *Tvö*. Það fer eftir því hvenær þú samstillir birgðir, kerfið uppfærir birgðir í Shopify með mismunandi magni:

|Þegar samstillingarbirgðir eru keyrðar|Gildi notað til að uppfæra lagerstöðu|Athugasemd|
|------|-----------------|-----------------|
|Þriðjudagur|9|Birgðir 10 mínus sölupöntun sett á að senda á mánudag|
|Föstudagur|7|Birgðir 10 mínus báðar sölupantanir|

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
