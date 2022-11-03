---
title: Samstilla og uppfylla sölupantanir
description: Setja upp og keyra innflutning og vinnslu sölupöntunar úr Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 2e79d19fd2fd03ec245c020cb9004809bccb5ec4
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728330"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Samstilla og uppfylla sölupantanir

Þessi grein lýsir nauðsynlegum stillingum og skrefum sem Ljúka þarf við til að samstilla og uppfylla sölupantanir með Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Stilla innflutning á pöntunum á Shopify verkstæðisspjaldinu

Regluleg Shopify pöntun getur innihaldið kostnað auk millisamtölu, s.s. sendingargjalda eða ef þær eru virkjaðar, ábendingar. Þessar upphæðir eru bókaðar beint á fjárhagsreikninginn sem á að nota fyrir tilteknar færslugerðir:

* **Reikningur sendingarkostnaðar**
* **Seldan gjafakortið reikning** ; frekari upplýsingar hjá [gjafakorti](synchronize-orders.md#gift-cards)
* **Ábending reikningur**  

Gera **sjálfvirkt stofna pantanir** til að stofna söluskjöl sjálfvirkt í [!INCLUDE[prod_short](../includes/prod_short.md)] pöntuninni sem Shopify er flutt inn.

Söluskjalið í [!INCLUDE[prod_short](../includes/prod_short.md)] inniheldur tengil við Shopify pöntunina. Ef hakað er í **Shopify Pöntunarnr. í reitnum Doc. lína** eru þessar upplýsingar endurteknar í sölulínur af gerðinni *Athugasemd*.

**Í reitnum upprunasvæði** skattsvæðis er hægt að stilla forgang að því hvernig velja á skattsvæðiskóta eða VSK-viðskiptabókunarflokk samkvæmt aðsetri. Í innfluttu Shopify pöntuninni eru upplýsingar um skatta en skattalækkunum fá að endurreikna þegar söluskjalið er stofnað þannig að mikilvægt er að VSK-/skattstillingarnar séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Frekari upplýsingar um skatta er að finna [í setja upp skatta fyrir Shopify tenginguna](setup-taxes.md).

### <a name="shipment-method-mapping"></a>Vörpun afhendingarmáta

Kóti **afhendingarmáta fyrir söluskjöl sem** fluttur er inn Shopify er hægt að fylla út sjálfvirkt. Stilla **þarf vörpun** afhendingaraðferðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu síðan tengda tengilinn.
2. Veljið verkstæðið sem skilgreina á vörpun á til að opna **Shopify vinnukortasíðuna**.
3. **Veljið aðgerðina vörpun** afhendingarmáta. Þetta stofnar sjálfkrafa færslur fyrir sendingaraðferðir sem eru [**skilgreindar í stillingum sendinga**](https://www.shopify.com/admin/settings/payments) í **Shopify admin**.
4. **Í reitnum Nafn** er hægt að sjá heiti sendingaraðferðarinnar Shopify.
5. **Færið inn Aðferðarkóta** fyrir afhendingarmáta samsvarandi Sendingaraðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Ef mörg sendingargjöld eru tengd sölupöntun verður aðeins valin ein Sendingaraðferð og henni úthlutað á söluskjalið.

### <a name="location-mapping"></a>Vörpun staðsetningar

Vörpun staðsetningarinnar er nauðsynleg í þrennu skyni:

* Til að samstilla birgðir, frekari upplýsingar er að finna [í samstillingarbirgðum til Shopify](synchronize-items.md#sync-inventory-to-shopify)
* Til að fylla út í **birgðageymslukótann** fyrir söluskjöl flutt inn Shopify. Þetta er mikilvægt þegar **Birgðageymsla áskilin** er virkjuð á **birgðauppsetningarspjaldinu**, annars er ekki hægt að stofna söluskjöl.
* Til að uppfæra Shopify pöntunina með upplýsingum um uppfyllingu sem er byggð á síðunni fyrir **bókaða söluafhendingar**.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samskipa vörpun birgðageymslna til að opna **Shopify vinnukortasíðuna**.
3. **Veldu staðsetningaraðgerðina** til að opna **Shopify verkstæðisstaðastöðunum**.
4. **Velja aðgerðina Sækja Shopify staðsetningar** til að flytja inn alla staði sem skilgreindir eru í Shopify. Þær má finna í stillingum staðsetningar [**í stjórnborðinu þínu**](https://www.shopify.com/admin/settings/locations)**Shopify .** Athugið að Staðsetningin sem er merkt sem *sjálfgefin* verður notuð við innflutning óuppfylltra Shopify pantana.
5. **Færa skal inn sjálfgefinn birgðageymslukóta** með samsvarandi staðsetningu í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="run-the-order-synchronization"></a>Keyra pöntunarsamstillingu

Eftirfarandi ferli lýsir því hvernig á að flytja inn og uppfæra sölupöntunum.

> [!NOTE]  
> Eldri pantanir í Shopify má ekki flytja inn. Afvirkja **sjálfkrafa pöntunarvalkostinn** í **hlutanum** **pöntunarvinnsla** í útskráningarstillingum í **Shopify** stjórnborðinu til að ganga úr skugga um að allar pantanir séu fluttar inn [!INCLUDE[prod_short](../includes/prod_short.md)] í. Ef flytja þarf inn geymdar pantanir skal nota **ónauðsynlegar** aðgerðir á [pöntunum](https://www.shopify.com/admin/orders) á síðunni á **Shopify** stjórnborðinu.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu síðan tengda tengilinn.
2. Veljið verslunina þar sem á að flytja inn pantanir til að opna **Shopify Vinnukortasíðuna**.
3. **Velja pantanin** aðgerð.
4. **Veldu samkeyrslupantanirnar úr Shopify** aðgerðinni.
5. Skilgreina afmarkanir í pöntunum eftir þörfum. Til dæmis er hægt að flytja inn fullgreiddar pantanir eða þær sem eru með lághættustig.
6. Velja hnappinn **Í lagi**.

Einnig er hægt að leita að **Samkeyrsluskipanunum úr Shopify** keyrslunni.

Áætla má að verkefnið sé framkvæmt með sjálfvirkum hætti. Frekari upplýsingar um [tímasetningu endurtekinna verka](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Yfirfara innfluttar pantanir

Þegar innflutningi er lokið er hægt að kanna Shopify pöntunina og finna allar tengdar upplýsingar, svo sem greiðslufærslur, sendingarkostnað, hættustig eða uppfyllum, ef pöntunin hefur verið uppfyllt Shopify. Einnig er hægt að sjá allar pöntunarstaðfestingar sem hafa verið sendar viðskiptavininum með því að **Shopify Velja aðgerðina staða**.

> [!NOTE]  
> Hægt er að **Shopify vafra um gluggann pantanir** beint og þú sérð pantanir með *opinni* stöðu úr öllum verslunum. Til að fara yfir fullfrágengnar pantanir þarf að opna **Shopify pantanassíðan** úr glugganum tiltekið **Shopify verkstæðisspjald**.

## <a name="create-sales-documents-in-business-central"></a>Stofna söluskjöl í Viðskiptamiðinu

**Ef Sjálfvirk pantanavíxla** eru virkjuð á **Shopify verkstæðisspjaldinu**[!INCLUDE[prod_short](../includes/prod_short.md)] er reynt að stofna söluskjal þegar pöntunin er flutt inn. Ef málefni eins og viðskiptamaður sem vantar eða er stofnuð þarf að lagfæra vandamálin og stofna síðan sölupöntunina aftur.

### <a name="to-create-sales-documents"></a>Söluskjöl stofnuð

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samstilla pantanir til að opna **Shopify Vinnukortasíðuna**.
3. **Velja pantanin** aðgerð.
4. Veljið pöntunina sem stofna á söluskjal fyrir og veljið **aðgerðina stofna söluskjöl**.
5. Velja **Já**.

Shopify Sölupöntun **er stofnuð ef pöntunin krefst uppfyllingar**. Til að uppfylla Shopify pantanir, t.d. þær pantanir sem innihalda aðeins gjafakort eða eru þegar Afgreiddar í Shopify, **verður sölureikningur** stofnaður.

Söluskjal er nú stofnað og hægt er að stjórna því með venjulegri [!INCLUDE[prod_short](../includes/prod_short.md)] virkni.

### <a name="manage-missing-customers"></a>Stjórna týndan viðskiptavin

Ef stillingarnar koma í veg fyrir að viðskiptavinur geti stofnað sjálfkrafa og rétt núverandi viðskiptavinur finnst ekki þarf að úthluta viðskiptamanni Shopify pöntuninni handvirkt. Það eru nokkrar leiðir til að gera þetta:

* Hægt er að úthluta reitnum **Selt-til viðskm.** Og **Reikn. að viðskm. nr.** Beint á **Shopify síðuna pantanir** með því að velja viðskiptavin af listanum yfir fyrirliggjandi viðskiptamenn.
* Hægt er að velja sniðmátskóta viðskiptamanns og stofna síðan og úthluta viðskiptamanninum **með aðgerðinni stofna nýjan viðskiptavin** á **Shopify síðunni pantanir**.
* Hægt er að varpa viðskiptamanni á tengda viðskiptavininn í glugganum Viðskiptavinir **Shopify og velja** síðan aðgerðina leita að vörpun **Shopify á** pantanasíðunni **·** . **Shopify**

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Hvernig Tenglarnir velja hvaða viðskiptavin á að nota

*Innflutningspöntunin úr Shopify* aðgerðinni reynir að velja viðskiptamenn í eftirfarandi röð:

1. **Ef sjálfgefinn viðskm. nr.** Er skilgreindur í **Shopify Viðskiptamannssniðmátinu** fyrir samsvarandi land er síðan **sjálfgefna Viðskiptavinasvæðið nr.** Er notað án tillits til stillinga í **reitum innflutnings Shopify** -og **Viðskiptavinavörpunargerðar**. Frekari upplýsingar um [sniðmát viðskiptavinar fyrir hvert land](synchronize-customers.md#customer-template-per-country).
2. **Ef innflutningur Shopify** viðskiptavinar er stilltur á *ekkert* og **sjálfgefna viðskiptavinarnr.** Er skilgreindur á **Shopify Vinnukortasíðunni**, þá **er sjálfgefinn viðskm. nr.** Er notað.

Næstu skref fara **eftir gerð** Viðskiptavinakortsvörunar.

* Ef það er **alltaf tekið sjálfgefinn viðskiptavin**, þá notar tengivirkið viðskiptavininn sem skilgreindur er í **sjálfgefnum viðskm.** Reitnum á **Shopify Vinnukortasíðunni**.
* Ef hún er **með tölvupósti/síma** þá reynir tengin að finna núverandi VIÐSKIPTAVIN með auðkenni fyrst, þá með tölvupósti, og svo eftir símanúmeri. Ef viðskiptavinurinn finnst ekki stofnar Connector nýjan viðskiptavin.
* Ef upplýsingar **eru** eftir uppskriftinni reynir Tengillinn að finna viðskiptavininn sem er fyrstur með kennið fyrst og síðan með upplýsingum um aðsetur í frumgögnum. Ef viðskiptavinurinn finnst ekki stofnar Connector nýjan viðskiptavin.

> [!NOTE]  
> Í tengivirkinu eru notaðar upplýsingar úr reitnum aðsetur og stofnar viðskiptamannsins sem er Reikn [!INCLUDE[prod_short](../includes/prod_short.md)]. Selt-til-viðskiptamaður er sá sami og Reikn.

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
|Breyttu staðsetningunni í annan stað, kortlögðu Shopify staðsetningarinnar. Bóka sendingu. | Þegar búið er að samstilla uppfyllingu verður Staðsetningin uppfærð í Shopify. |
|Breyttu staðsetningunni í annan stað, ekki varpað á Shopify birgðageymslur. Bóka sendingu. | Ekki er Samstaða um uppfyllingu Shopify. |
|Breyta minnkun magns. Bóka sendingu. | Shopify Pöntunin verði merkt sem að hluta til uppfyllt. |
|Bæta við nýju atriði. Bóka sendingu. | Shopify Pöntunin verður merkt sem uppfylltur. Línur verða ekki uppfærðar. |

## <a name="synchronize-shipments-to-shopify"></a>Samstilla sendingar á Shopify

Þegar sölupöntun sem búin er til úr Shopify pöntun er afhent er hægt að samstilla afhendingarnar með Shopify.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **samstillingu afhendingar við Shopify** og velja síðan tengda tengilinn.
2. Skilgreinið afmarkanir á afhendingum eftir þörfum. Til dæmis er hægt að uppfæra sendingu sem er bókuð á tiltekinni dagsetningu.
3. Velja hnappinn **Í lagi**.

Röðin sem í Shopify verður er merkt sem uppfyllt. Viðskiptavinurinn fær sjálfkrafa tilkynningu um sendingu sendingar eða textaskilaboð (SMS). Ef flutningsaðili og rakningarkóði eru tilgreind á sendingunni eru rakningarupplýsingar hafðar með í tölvupóstinum.

Einnig er hægt að **nota aðgerðina samstilla sendingar** í Shopify sölupöntunum eða Shopify síðum verkstæðisáætlana.

Áætla má að verkefnið sé framkvæmt með sjálfvirkum hætti. Frekari upplýsingar um [tímasetningu endurtekinna verka](background.md#to-schedule-recurring-tasks).

>Mikilvægt Staðsetningin, þar á meðal auður Birgðageymsla, sem er skilgreind í bókuðu afhendingarlínunni verður að hafa samsvarandi færslu í Shopify birgðageymslunni. Annars verður þessi lína ekki send aftur til Shopify. Frekari upplýsingar á [staðsetningarvörpun](synchronize-orders.md#location-mapping).

Munið að keyra **Samstillingarpantanir frá Shopify** til að uppfæra stöðu pöntunar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Í tengimyningum er einnig Skjalasafn að fullu greidd og fullnaðarpantanir í báða Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] að því gefnu að skilyrðin séu uppfyllt.

### <a name="shipping-agents-and-tracking-url"></a>Farmflutningar og rakningarvefslóð

**Ef bókaða söluafhendingarskjalið** inniheldur **kóta** flutningsfyrirtækisins og/eða **pakkakengingu nr.** verða þessar upplýsingar sendar til Shopify og viðskiptavinarins í tölvupósti afhendingarstaðfestingarinnar.

Rakningarfyrirtækið er fyllt út í eftirfarandi pöntun (frá hæsta til lægsta) samkvæmt færslunni flutningsaðili:

* **Shopify Rakstrarfélagið**
* **Heiti**
* **Kóði**

**Ef SVÆÐIÐ slóð rakans slóðar** er fyllt út fyrir flutningsskrá staðfestingar þá inniheldur staðfestingakurl einnig RAKNINGARVEFSLÓÐ.

## <a name="gift-cards"></a>Gjafakortum

Shopify Í versluninni er hægt að selja gjafakort, sem hægt er að nota til að greiða fyrir alvöru vörur.

Þegar verið er að fást við gjafakort er mikilvægt að slá inn gildi í **reitinn Selt gjafakort** í **Shopify verkstæðisglugganum**. Samstíga seldum gjafakortum ásamt pöntunum í takt. Notuð gjafakort verða einnig flutt inn með pöntuninni en nú sem færsluhirti. Takið eftir að gjafakortið minnkar ekki upphæðina í reikning.

Til að yfirfara Útgefin og notuð gjafakort skal velja þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **gjafakort** og veldu síðan tengda tengilinn.

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
