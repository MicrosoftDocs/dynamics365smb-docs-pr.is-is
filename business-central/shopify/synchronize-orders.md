---
title: Samstilla og uppfylla sölupantanir
description: Setja upp og keyra innflutning og vinnslu sölupöntunar úr Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: bef02c5fcbc2b6174e8a3f746a97f0e11564dcf6
ms.sourcegitcommit: 902da19b0ab7a3fbc051cd69ab2802f30d0f378f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2022
ms.locfileid: "9213690"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Samstilla og uppfylla sölupantanir

Þessi grein lýsir nauðsynlegum stillingum og skrefum sem Ljúka þarf við til að samstilla og uppfylla sölupantanir með Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Stilla innflutning á pöntunum á Shopify verkstæðisspjaldinu

Regluleg Shopify pöntun getur innihaldið kostnað auk millisamtölu, s.s. sendingargjalda eða ef þær eru virkjaðar, ábendingar. Þessar upphæðir eru bókaðar beint á fjárhagsreikninginn sem á að nota fyrir tilteknar færslugerðir:

- **Reikningur sendingarkostnaðar**
- **Seldan gjafakortið reikning** ; frekari upplýsingar hjá [gjafakorti](synchronize-orders.md#gift-cards)
- **Ábending reikningur**  

Gera **sjálfvirkt stofna pantanir** til að stofna söluskjöl sjálfvirkt í [!INCLUDE[prod_short](../includes/prod_short.md)] pöntuninni sem Shopify er flutt inn.
Söluskjalið í [!INCLUDE[prod_short](../includes/prod_short.md)] inniheldur tengil við Shopify pöntunina. Ef hakað er í **Shopify Pöntunarnr. í reitnum Doc. lína** eru þessar upplýsingar endurteknar í sölulínur af gerðinni *Athugasemd*.

**Í reitnum upprunasvæði** skattsvæðis er hægt að stilla forgang að því hvernig velja á skattsvæðiskóta eða VSK-viðskiptabókunarflokk samkvæmt aðsetri. Þetta skref er viðeigandi fyrir lönd með virðisaukaskatti sem og þá sem eru með VSK. Læra meira at [skattaummælis](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Vörpun afhendingarmáta

Kóti **afhendingarmáta fyrir söluskjöl sem** fluttur er inn Shopify er hægt að fylla út sjálfvirkt. Stilla **þarf vörpun** afhendingaraðferðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verkstæðið sem skilgreina á vörpun á til að opna **Shopify vinnukortasíðuna**.
3. **Veljið aðgerðina vörpun** afhendingarmáta. Þetta stofnar sjálfkrafa færslur fyrir sendingaraðferðir sem eru [**skilgreindar í stillingum sendinga**](https://www.shopify.com/admin/settings/payments) í **Shopify admin**.
4. **Í reitnum Nafn** er hægt að sjá heiti sendingaraðferðarinnar Shopify.
5. **Færið inn Aðferðarkóta** fyrir afhendingarmáta samsvarandi Sendingaraðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Ef mörg sendingargjöld eru tengd sölupöntun verður aðeins valin ein Sendingaraðferð og henni úthlutað á söluskjalið.

### <a name="payment-method-mapping"></a>Vörpun greiðsluaðferðar

Til að færa **inn greiðsluaðferðarkóta** fyrir söluskjöl sem eru flutt inn Shopify sjálfkrafa þarf að skilgreina **greiðsluaðferðarvörpun**.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verkstæðið sem skilgreina á vörpun á til að opna **Shopify vinnukortasíðuna**.
3. **Veljið aðgerðina Greiðsluaðferðarvörpun**.
4. **Í reitina gátt** -og **kreditkortafyrirtæki** er fært inn heiti greiðsluaðferðar frá Shopify. Færslan verður stofnuð sjálfkrafa þegar pantanir eru fluttar inn Shopify.
5. **Færið inn Greiðsluaðferðarkóta** með samsvarandi greiðsluaðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].
6. **Stillið forgang** á tilvikum þegar viðskiptavinurinn notar marga greiðsluhætti. Greiðsluaðferðin með mestan forgang fær valið í söluskjalinu. Ef báðir Greiðsluaðferðirnar hafa sama forgang er Greiðsluaðferðin með hæstu upphæðina notuð.

> [!NOTE]  
> Ef samsvarandi Greiðsluháttur í [!INCLUDE[prod_short](../includes/prod_short.md)]**reitnum gerð** mótreiknings og **Mótreikningur nr.** útfyllist, við bókun reikningakerfisins er stofnuð mótfærsla af *greiðslugerðinni* og jöfnuð *við reikningsgerð* viðskiptamannafærsla.

### <a name="location-mapping"></a>Vörpun staðsetningar

Ef fylla á út í **birgðageymslukótann** fyrir söluskjöl sem eru flutt inn Shopify sjálfkrafa þarf að samskipa **Shopify verkstæðisstaðsetningunni**.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samskipa vörpun birgðageymslna til að opna **Shopify vinnukortasíðuna**.
3. **Veldu staðsetningaraðgerðina** til að opna **Shopify verkstæðisstaðastöðunum**.
4. **Velja aðgerðina Sækja Shopify staðsetningar** til að flytja inn alla staði sem skilgreindir eru í Shopify. Þær má finna í stillingum staðsetningar [**í stjórnborðinu þínu**](https://www.shopify.com/admin/settings/locations)**Shopify .** Athugið að Staðsetningin sem er merkt sem *sjálfgefin* verður notuð við innflutning óuppfylltra Shopify pantana.
5. **Færa skal inn sjálfgefinn birgðageymslukóta** með samsvarandi staðsetningu í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Samskipa verður staðsetningarvörpun ef **Birgðageymsla áskilin** er virkjuð á **birgðauppsetningarspjaldinu** eða ekki er hægt að stofna söluskjöl.

## <a name="run-the-order-synchronization"></a>Keyra pöntunarsamstillingu

Eftirfarandi ferli lýsir því hvernig á að flytja inn og uppfæra sölupöntunum.

> [!NOTE]  
> Eldri pantanir í Shopify má ekki flytja inn. Afvirkja **sjálfkrafa pöntunarvalkostinn** í **hlutanum** **pöntunarvinnsla** í útskráningarstillingum í **Shopify** stjórnborðinu til að ganga úr skugga um að allar pantanir séu fluttar inn [!INCLUDE[prod_short](../includes/prod_short.md)] í. Ef flytja þarf inn geymdar pantanir skal nota **ónauðsynlegar** aðgerðir í [pantanunum](https://www.shopify.com/admin/orders) á **Shopify** síðunni stjórnborðið.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að flytja inn pantanir til að opna **Shopify Vinnukortasíðuna**.
3. **Velja pantanin** aðgerð.
4. **Veldu samkeyrslupantanirnar úr Shopify** aðgerðinni.
5. Skilgreina afmarkanir í pöntunum eftir þörfum. Til dæmis er hægt að flytja inn fullgreiddar pantanir eða þær sem eru með lágt hættustig.
6. Velja hnappinn **Í lagi**.

Einnig er hægt að leita að **Samkeyrsluskipanunum úr Shopify** keyrslunni.

Áætla má að verkefnið sé framkvæmt með sjálfvirkum hætti. Frekari upplýsingar um [tímasetningu endurtekinna verka](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Yfirfara innfluttar pantanir

Þegar innflutningi er lokið er hægt að kanna Shopify pöntunina og finna allar tengdar upplýsingar, svo sem greiðslufærslur, sendingarkostnað, hættustig eða uppfyllum, ef pöntunin hefur verið uppfyllt Shopify. Einnig er hægt að sjá allar pöntunarstaðfestingar sem hafa verið sendar viðskiptavininum með því að **Shopify Velja aðgerðina staða**.

> [!NOTE]  
> Hægt er að **Shopify vafra um gluggann pantanir** beint og þú sérð pantanir með *opinni* stöðu úr öllum verslunum. Til að fara yfir fullfrágengnar pantanir þarf að opna **Shopify pantanassíðan** úr glugganum tiltekið **Shopify verkstæðisspjald**.

## <a name="create-sales-documents-in-business-central"></a>Stofna söluskjöl í Viðskiptamiðinu

**Ef Sjálfvirk pantanavíxla** eru virkjuð á **Shopify verkstæðisspjaldinu**[!INCLUDE[prod_short](../includes/prod_short.md)] er reynt að stofna söluskjal þegar pöntunin er flutt inn. Ef málefni eins og viðskiptavinur sem vantar eða hefur komið fram þarf að lagfæra vandamálin svo sölupöntunin er stofnuð aftur.

### <a name="to-create-sales-documents"></a>Söluskjöl stofnuð

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samstilla pantanir til að opna **Shopify Vinnukortasíðuna**.
3. **Velja pantanin** aðgerð.
4. Veljið pöntunina sem stofna á söluskjal fyrir og veljið **aðgerðina stofna söluskjöl**.
5. Velja **Já**.

Shopify Sölupöntun **er stofnuð ef pöntunin krefst uppfyllingar**. Til að uppfylla Shopify pantanir, t.d. þær pantanir sem innihalda aðeins gjafakort eða eru þegar Afgreiddar í Shopify, **verður sölureikningur** stofnaður.

Söluskjal er nú stofnað og hægt er að stjórna því með venjulegri [!INCLUDE[prod_short](../includes/prod_short.md)] virkni.

### <a name="manage-missing-customers"></a>Stjórna týndan viðskiptavin

Ef stillingarnar koma í veg fyrir að viðskiptavinur geti stofnað sjálfkrafa og rétt núverandi viðskiptavinur finnst ekki þarf að úthluta viðskiptamanni Shopify pöntuninni handvirkt. Það eru nokkrar leiðir til að gera þetta:

- Hægt er að úthluta reitnum **Selt-til viðskm.** Beint á **Shopify síðuna pantanir** með því að velja viðskiptavin af listanum yfir fyrirliggjandi viðskiptamenn.
- Hægt er að velja sniðmátskóta viðskiptamanns og stofna síðan og úthluta viðskiptamanninum **með aðgerðinni stofna nýjan viðskiptavin** á **Shopify síðunni pantanir**.
- Hægt er að varpa viðskiptamanni á tengda **Shopify viðskiptavininn** í **Shopify glugganum Viðskiptavinir** og velja **síðan aðgerðina leita að vörpun** á **Shopify pantanasíðunni**.

### <a name="tax-remarks"></a>Skattaleg ummæli

Í innfluttu Shopify pöntuninni eru upplýsingar um skatta en skattalækkunum fá að endurreikna þegar söluskjalið er stofnað þannig að mikilvægt er að VSK-/skattstillingarnar séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)].

- Margfeldi VSK/skatthlutföll í vöru. Sumar vörutegundir eru til dæmis gjaldskyldar fyrir minni skatthlutföll. Þær vörur þurfa að [!INCLUDE[prod_short](../includes/prod_short.md)] vera til í og vera kortlagðar í Shopify vörum. Að öðrum kosti er notaður VSK-vörubókunarflokkurinn til að nota sjálfvirka stofnun týnandi vara.

- Aðsetur-háð skatthlutföll. **Svæðið Forgangur** skattsvæðis er notað ásamt **töflunni Sniðmát** viðskiptamanns til að skrifa yfir staðlaðar röksemdir sem fylla út í **skattsvæðiskótanum** í söluskjalinu. **Reiturinn Forgangur** skattsvæðis Tilgreinir forgang sem notaður er til að ákvarða upplýsingar um land/svæði og ríki/hérað. Síðan er samsvarandi færsla í Shopify sniðmátum viðskiptamanns fundin og **Skattsvæðiskóti**, **skattskyld** og **VSK-Bus. bókunarflokkur** er notaður þegar söluskjal er stofnað.

- Verð með skatti. **Verðin með skattverði**/**með VSK** í stofnaða söluskjalinu fara ekki eftir viðskiptamanninum heldur á **sniðmáti** viðskiptamanns af **Shopify vinnukorti** eða sniðmáti viðskiptamanns á hvert land.

### <a name="impact-of-order-editing"></a>Áhrif breytinga á pöntun

Í Shopify:

|Breyta|Áhrif|
|------|-----------|
|Breyta uppfyllingu | Upprunaleg staðsetning verður samsýnd [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Breyta pöntun og breyta magni| Pöntunarhaus og fylgitöflur verða uppfærðar í [!INCLUDE[prod_short](../includes/prod_short.md)], línur verða ekki. |
|Breyta pöntun og bæta við nýrri vöru | Pöntunarhaus verður uppfærður, línur renna ekki. |

Í [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Breyta|Áhrif|
|------|-----------|
|Breyttu staðsetningunni í annan stað, kortlögðu Shopify staðsetningarinnar. Bóka sendingu. | Þegar búið er að samstilla uppfyllingu verður staðsetning uppfærð í Shopify. |
|Breyttu staðsetningunni í annan stað, ekki varpað á Shopify birgðageymslur. Bóka sendingu. | Ekki er Samstaða Shopify um uppfyllingu. |
|Breyta minnkun magns. Bóka sendingu. | Shopify Pöntunin verði merkt sem að hluta til uppfyllt. |
|Bæta við nýju atriði. Bóka sendingu. | Shopify Pöntunin verður merkt sem uppfylltur. Línur verða ekki uppfærðar. |

## <a name="synchronize-shipments-to-shopify"></a>Samstilla sendingar á Shopify

Þegar sölupöntun sem búin er til úr Shopify pöntun er afhent er hægt að samstilla afhendingarnar með Shopify.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **samstillingu afhendingar við Shopify** og veljið síðan tengda tengilinn.
2. Skilgreinið afmarkanir á afhendingum eftir þörfum. Til dæmis er hægt að uppfæra sendingu sem er bókuð á tiltekinni dagsetningu.
3. Velja hnappinn **Í lagi**.

Röðin sem í Shopify verður er merkt sem uppfyllt. Viðskiptavinurinn fær sjálfkrafa tilkynningu um sendingu sendingar eða textaskilaboð (SMS). Ef flutningsaðili og rakningarkóði eru tilgreind á sendingunni eru rakningarupplýsingar hafðar með í tölvupóstinum.

> [!NOTE]  
> Munið að keyra **Samstillingarpantanir frá Shopify** til að uppfæra stöðu pöntunar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Í tengimyningum eru Skjalasöfn einnig fullkomlega launuð og fullnaðarpantanir í bæði Shopify og í [!INCLUDE[prod_short](../includes/prod_short.md)] því kveðið að skilyrðin séu uppfyllt.

### <a name="shipping-agents-and-tracking-url"></a>Farmflutningar og rakningarvefslóð

**Ef bókaða söluafhendingarskjalið** inniheldur **kóta** flutningsfyrirtækisins og/eða **pakkakengingu nr.** verða þessar upplýsingar sendar til Shopify og viðskiptavinarins í tölvupósti afhendingarstaðfestingarinnar.

Rakningarfyrirtækið er fyllt út í eftirfarandi pöntun (frá hæsta til lægsta) samkvæmt færslunni flutningsaðili:

- **Shopify Rakstrarfélagið**
- **Heiti**
- **Kóði**

**Ef SVÆÐIÐ slóð rakans slóðar** er fyllt út fyrir flutningsskrá staðfestingar þá inniheldur staðfestingakurl einnig RAKNINGARVEFSLÓÐ.

## <a name="gift-cards"></a>Gjafakortum

Shopify Í versluninni er hægt að selja gjafakort, sem hægt er að nota til að greiða fyrir alvöru vörur.

Þegar verið er að fást við gjafakort er mikilvægt að slá inn gildi í **reitinn Selt gjafakort** í **Shopify verkstæðisglugganum**. Samstíga seldum gjafakortum ásamt pöntunum í takt. Notuð gjafakort verða einnig flutt inn með pöntuninni en nú sem færsluhirti. Takið eftir að gjafakortið minnkar ekki upphæðina í reikning.

Til að yfirfara Útgefin og notuð gjafakort skal velja þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **gjafakort** og veldu svo tengda tengilinn.

## <a name="transactions-and-payouts"></a>Færslur og útborganir

Þegar viðskiptavinur lýkur útskrift sína í netverslun eru upplýsingar um greiðslur vistaðar sem **færsla**. Það gætu verið margar færslur tengdar pöntuninni, eins og til dæmis þegar viðskiptavinur notar gjafakort til að greiða einhvern kostnað og notar síðan kreditkort eða PayPal fyrir eftirstandandi upphæð. 

Ef þú notar Shopify greiðslu sem greiðsluþjónustuveitandi þá þarf auk þess upplýsingar um peninga sem berast frá viðskiptavininum af greiðsluveitunni, einnig er hægt að sjá greiðslur frá Shopify þér á bankareikninginn þinn. 

### <a name="transactions"></a>Færslur

Greiðslufærslurnar sem eiga sér stað í Shopify eru samstilltar við pantanirnar og er hægt að skoða þær á *Shopify pantansíðunni*.

Til að yfirfara allar færslur skaltu velja þá ![ljósaperu sem opnast Segðu mér aðgerðina 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **færslur** og velja tengdan tengil.

Ef greiðsluaðferðarvörpun er skilgreind þá hefur innkaupaaðferð sem er stofnuð verið úthlutað. Frekari upplýsingar um [Greiðsluaðferðarvörpun](#payment-method-mapping).

### <a name="payouts"></a>Útgreiðslur

Ef verslunin notar Shopify greiðslu munt þú fá greiðslur í gegnum *Shopify útborganir* þegar viðskiptavinur greiðir með Shopify greiðslum og flýta fyrir afgreiðsluúttöku.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samstilla Greiðsluspjald til að opna **Shopify Vinnukortasíðuna**.
3. **Veljið aðgerðina samstilling Payouts**.

Til að fara yfir allar útborganir skaltu velja þá ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **payouts**, og velja tengdan tengil.

**Útborganir** eru eingöngu til upplýsinga og hafa ekki áhrif á fjárhag eða fjárhag notanda þó að þær geti verið hjálplegar þegar unnið er úr uppgjöri bankareiknings.

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
