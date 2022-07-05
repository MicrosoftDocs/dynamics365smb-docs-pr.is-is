---
title: Samstilla og uppfylla sölupantanir
description: Setja upp og keyra innflutning og vinnslu sölupöntunar úr Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ce11aa8766550e72cab2f811ef6602dba4271211
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076306"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Samstilla og uppfylla sölupantanir

Þessi grein lýsir nauðsynlegum stillingum og skrefum sem þarf að framkvæma til að samstilla og uppfylla sölupantanir úr Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Stilla innflutning á pöntunum á Shopify verkstæðisspjaldinu

Regluleg Shopify pöntun getur haft aukaupphæðir ofan á, eins og sendingargjöld eða ef gert ráð fyrir ábendingum. Þessar upphæðir verða bókaðar beint á fjárhagsreikninga. Velja fjárhagsreikninginn sem á að nota fyrir tilteknar færslur:

- **Reikningur sendingarkostnaðar**
- **Selt gjafakorti**, nánari upplýsingar er að finna [á gjafakorti](synchronize-orders.md#gift-cards).
- **Ábending reikningur**  

Gera **sjálfvirkt stofna pantanir** til að stofna söluskjöl sjálfvirkt í [!INCLUDE[prod_short](../includes/prod_short.md)] pöntuninni sem Shopify er flutt inn.
Söluskjalið í [!INCLUDE[prod_short](../includes/prod_short.md)] inniheldur tengil við Shopify pöntunina. Ef hakað er í **Shopify Pöntunarnr. í reitnum Doc-lína** eru þessar upplýsingar endurteknar í sölulínur af gerðinni *Athugasemd*.

**Í reitnum upprunasvæði** skattsvæðis er hægt að tilgreina forgang að því hvernig velja á skattsvæðiskóta eða VSK-viðskiptabókunarflokk á grundvelli aðseturs. Þetta þrep á við um lönd með VSK en hægt er að nota það fyrir VSK-lönd. Nánar er fjallað [um Skattaleg ummæli](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Vörpun afhendingarmáta

Kóti **afhendingarmáta fyrir söluskjöl sem** fluttur er inn Shopify er hægt að fylla út sjálfvirkt. Stilla **þarf vörpun** afhendingaraðferðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verkstæðið sem skilgreina á vörpun á til að opna **Shopify vinnukortasíðuna**.
3. **Veljið aðgerðina vörpun** afhendingarmáta. Færslurnar fyrir sendingaraðferðirnar sem eru [**skilgreindar í sendingarstillingum**](https://www.shopify.com/admin/settings/payments) í admin **Shopify þínum** eru stofnaðar sjálfkrafa.
4. **Í reitnum Nafn** er hægt að sjá heiti sendingaraðferðarinnar Shopify.
5. **Færið inn Aðferðarkóta** fyrir afhendingarmáta samsvarandi Sendingaraðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Ef margar sendingargjöld eru tengd sölupöntun; aðeins ein verður valin sem Sendingaraðferð og úthlutuð söluskjalinu.

### <a name="payment-method-mapping"></a>Vörpun greiðsluaðferðar

Til að færa **inn greiðsluaðferðarkóta** fyrir söluskjöl sem eru sjálfkrafa flutt inn Shopify þarf að skilgreina **greiðsluaðferðarvörpunarkerfið**.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verkstæðið sem skilgreina á vörpun á til að opna **Shopify vinnukortasíðuna**.
3. **Veljið aðgerðina Greiðsluaðferðarvörpun**.
4. **Í reitina gátt** -og **kreditkortafyrirtæki** er fært inn heiti greiðsluaðferðar frá Shopify. Færslan verður stofnuð sjálfkrafa þegar pantanir á shopify eru fluttar inn.
5. **Færið inn Greiðsluaðferðarkóta** með samsvarandi greiðsluaðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].
6. **Stillið forgang** á tilvikum þegar viðskiptavinurinn notar marga greiðsluhætti. Greiðsluaðferðin með mestan forgang fær valið í söluskjalinu. Ef báðir Greiðsluaðferðirnar hafa sama forgang er Greiðsluaðferðin með hæstu upphæðina notuð.

### <a name="location-mapping"></a>Vörpun staðsetningar

Ef fylla á út í **birgðageymslukótann** fyrir söluskjöl sem eru flutt inn Shopify sjálfkrafa þarf að samskipa **Shopify verkstæðisstaðsetningunni**.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samskipa vörpun birgðageymslna til að opna **Shopify vinnukortasíðuna**.
3. **Veldu staðsetningaraðgerðina** til að opna **Shopify verkstæðisstaðastöðunum**.
4. **Velja aðgerðina Sækja Shopify staðsetningar** til að flytja inn alla staði sem skilgreindir eru í Shopify. Þær má finna í stillingum staðsetningar [**í stjórnborðinu þínu**](https://www.shopify.com/admin/settings/locations)**Shopify .** Athugið að Staðsetningin sem er merkt sem *sjálfgefin* verður notuð við innflutning óuppfylltra Shopify pantana.
5. **Færa skal inn sjálfgefinn birgðageymslukóta** með samsvarandi staðsetningu í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Samskipa verður staðsetningarvörpun ef **Birgðageymsla áskilin** er virkjuð í **birgðauppsetningarspjaldinu**, annars er ekki hægt að stofna söluskjöl.

## <a name="run-the-order-synchronization"></a>Keyra pöntunarsamstillingu

Eftirfarandi ferli lýsir því hvernig á að flytja inn og uppfæra sölupöntunum.

> [!NOTE]  
> Eldri pantanir í Shopify má ekki flytja inn. Afvirkja **sjálfkrafa pöntunarvalkostinn** í **hlutanum** **pöntunarvinnsla** í útskráningarstillingum í **Shopify** stjórnborðinu til að ganga úr skugga um að allar pantanir séu fluttar inn [!INCLUDE[prod_short](../includes/prod_short.md)] í. Ef flytja þarf inn geymdar pantanir skal nota **ónauðsynlegar** aðgerðir í [pantanunum](https://www.shopify.com/admin/orders) á Shopify síðunni stjórnborðið.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að flytja inn pantanir til að opna **Shopify Vinnukortasíðuna**.
3. **Velja pantanin** aðgerð.
4. **Veldu samkeyrslupantanirnar úr Shopify** aðgerðinni.
5. Skilgreina afmarkanir í pöntunum eftir þörfum. Til dæmis er hægt að flytja inn fullgreiddar pantanir eða þær sem eru með lágt hættustig.
6. Velja hnappinn **Í lagi**.

Einnig er hægt að leita að **Samkeyrsluskipanunum úr Shopify** keyrslunni.

Áætla má að verkefnið sé framkvæmt með sjálfvirkum hætti. Frekari upplýsingar er að finna [í Schedule endurtekin verk](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Yfirfara innfluttar pantanir

Þegar innflutningi er lokið er hægt að kanna Shopify pöntunina og finna allar tengdar upplýsingar. Til dæmis er að finna greiðslufærslur, sendingarkostnað, hættustig eða uppfylt ef pöntunin hefur verið uppfyllt Shopify. Einnig er hægt að sjá allar pöntunarstaðfestingar sem hafa verið sendar viðskiptavininum með því að **Shopify Velja aðgerðina staða**.

> [!NOTE]  
> Hægt er að **Shopify vafra um gluggann pantanir** beint og þú sérð pantanir með *opinni* stöðu úr öllum verslunum. Til að fara yfir fullfrágengnar pantanir þarf að opna **Shopify pantanassíðan** úr glugganum tiltekið **Shopify verkstæðisspjald**.

## <a name="create-sales-documents-in-business-central"></a>Stofna söluskjöl í Viðskiptamiðinu

**Ef Sjálfvirk pantanavíxla** eru virkjuð á **Shopify verkstæðisspjaldinu**[!INCLUDE[prod_short](../includes/prod_short.md)] er reynt að stofna söluskjal þegar pöntunin er flutt inn. Ef vinnslan er keyrð í úthreyfingar, eins og ef Viðskiptamaður eða afurð vantar, þarf að lagfæra vandann. Þá getur þú prófað að stofna sölupöntunina aftur.

### <a name="to-create-sales-documents"></a>Söluskjöl stofnuð

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samstilla pantanir til að opna **Shopify Vinnukortasíðuna**.
3. **Velja pantanin** aðgerð.
4. Veljið pöntunina sem stofna á söluskjal fyrir og veljið **aðgerðina stofna söluskjöl**.
5. Velja **Já**.

Shopify Ef pöntunin krefst uppfyllingar **verður sölupöntun** stofnuð. Til að uppfylla Shopify pantanir, t.d. þær pantanir sem innihalda aðeins gjafakort eða eru þegar Afgreiddar í Shopify, **verður sölureikningur** stofnaður.

Söluskjal er nú stofnað og hægt er að stjórna því með notkun staðalvirkleikaeiginleika [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="manage-missing-customers"></a>Stjórna týndan viðskiptavin

Ef stillingarnar koma í veg fyrir að viðskiptavinur geti stofnað sjálfkrafa og rétt fyrirliggjandi viðskiptavinar finnst ekki er viðskiptamanni Shopify úthlutað pöntun handvirkt. Nokkur kostur er á:

- Hægt er að úthluta reitnum **Selt-til viðskm.** Beint í **Shopify pöntunina** með því að velja viðskiptavin af lista yfir viðskiptamenn sem fyrir eru.
- Hægt er að velja sniðmátskóta viðskiptamanns, stofna og úthluta viðskiptamanninum **með aðgerðinni stofna nýjan viðskiptavin** á **Shopify síðunni pantanir**.
- Hægt er að varpa viðskiptamanni á tengda **Shopify viðskiptavininn** í **Shopify glugganum Viðskiptavinir** og velja **síðan aðgerðina leita að vörpun** á **Shopify pantanasíðunni**.

### <a name="tax-remarks"></a>Skattaleg ummæli

Á meðan innflutt Shopify pöntun inniheldur upplýsingar um skatta, fá skattaútreiknaðar þegar söluskjal er stofnað. Þessi endurútreikningur skiptir miklu máli að VSK/skattastillingar séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)].

- Margfeldi afurðskatts/VSK-vaxta. Sumar vörutegundir eru til dæmis gjaldskyldar fyrir minni skatthlutföll. Þær vörur þurfa að [!INCLUDE[prod_short](../includes/prod_short.md)] vera til í og vera kortlagðar í Shopify vörum. Að öðrum kosti er notaður VSK-vörubókunarflokkurinn til að nota sjálfvirka stofnun týnandi vara.

- Aðsetur-háð skatthlutföll. Svæðið Forgangur **skattsvæðis er** notað ásamt **töflunni Sniðmát** viðskiptamanns til að skrifa yfir staðlaðar röksemdir sem fylla **út kóta** skattsvæðisins í söluskjalinu. **Reiturinn Forgangur** skattsvæðis Tilgreinir forgang frá því að aðgerðin á að fara yfir upplýsingar um land/svæði og ríki/hérað. Síðan er samsvarandi færsla í Shopify sniðmátum viðskiptamanns fundin og **Skattsvæðiskóti**, **skattskyld** og **VSK-Bus. bókunarflokkur** er notaður þegar söluskjal er stofnað.

- Verð með skatti. **Verðin ásamt skattverði**/**með VSK** í stofnaða söluskjalinu fara ekki eftir viðskiptamanninum heldur á **sniðmátinu** viðskiptavinur úr Shopify verkstæðissniðmátinu eða sniðmáti viðskiptamanns á hvert land.

### <a name="impact-of-edits-of-orders"></a>Áhrif ritaðrar skipanir

|Breyta|Áhrif|
|------|-----------|
|Í Shopify er breytt staðsetning uppfyllingar | Upprunaleg staðsetning verður samsýnd [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Í Shopify, breyta pöntun og breyta magni| Pöntunarhaus og fylgitöflur verða uppfærðar í [!INCLUDE[prod_short](../includes/prod_short.md)], línur verða ekki. |
|Í Shopify, breyta pöntun og bæta við nýrri vöru | Pöntunarhaus verður uppfærður, línur renna ekki. |
|[!INCLUDE[prod_short](../includes/prod_short.md)] Breyta staðsetningu á öðrum stað, varpa Shopify á staðsetningartæki. Bóka sendingu. | Þegar búið er að samstilla uppfyllingu verður staðsetning uppfærð í Shopify. |
|[!INCLUDE[prod_short](../includes/prod_short.md)] Breyta staðsetningu á öðrum stað, ekki varpað Shopify á birgðageymslur. Bóka sendingu. | Ekki verður samstillt við uppfyllingu Shopify. |
|Í [!INCLUDE[prod_short](../includes/prod_short.md)], breyta minnkunar magni. Bóka sendingu. | Shopify Pöntunin verði merkt sem að hluta til uppfyllt. |
|Í [!INCLUDE[prod_short](../includes/prod_short.md)] er ný vara bætt við. Bóka sendingu. | Shopify Pöntunin verður merkt sem uppfylltur. Línur verða ekki uppfærðar. |

## <a name="synchronize-shipments-to-shopify"></a>Samstilla sendingar á Shopify

Þegar sölupöntun sem er stofnuð úr Shopify pöntun er samstillt er hægt að samstilla afhendingarnar við Shopify.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **samstillingu afhendingar við Shopify** og veljið síðan tengda tengilinn.
2. Skilgreinið afmarkanir á afhendingum eftir þörfum. Til dæmis er hægt að uppfæra sendingu sem er bókuð á tilteknum degi.
3. Velja hnappinn **Í lagi**.

Röðin sem í Shopify verður er merkt sem uppfyllt. Viðskiptavinurinn fær sjálfkrafa tilkynningu um sendingu sendingar eða textaskilaboð (SMS). Ef flutningsaðili og rakningarkóði eru tilgreind á sendingunni eru rakningarupplýsingar hafðar með í tölvupóstinum.

> [!NOTE]  
> Munið að keyra **Samstillingarpantanir frá Shopify** til að uppfæra stöðu pöntunar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Í tengimyningum eru Skjalasöfn einnig fullkomlega launuð og fullnaðarpantanir í bæði Shopify og í [!INCLUDE[prod_short](../includes/prod_short.md)] því kveðið að skilyrðin séu uppfyllt.

### <a name="shipping-agents-and-tracking-url"></a>Farmflutningar og rakningarvefslóð

**Ef bókaða Söluafhendingarskjalið** inniheldur **kóta** flutningsfyrirtækisins og/eða **pakkakengingu nr.** verða þessar upplýsingar sendar til Shopify og til lokafærslu í tölvupósti um staðfestingu á sendingu.

Rakningarfyrirtækið er útfyllt á grundvelli Flutningsfærslu með eftirfarandi forgangi (frá hæsta til lægsta):

- **Shopify Rakstrarfélagið**
- **Heiti**
- **Kóði**

**Ef SVÆÐIÐ slóð rakans slóðar** er fyllt út fyrir flutningsskrá staðfestingar þá inniheldur staðfestingakurl einnig RAKNINGARVEFSLÓÐ.

## <a name="gift-cards"></a>Gjafakortum

Shopify Í versluninni er hægt að selja gjafakort, sem síðar má nota til að greiða fyrir alvöru vörur.

Þegar verið er að fást við gjafakort er mikilvægt að slá inn gildi í **reitinn Selt gjafakort** í **Shopify verkstæðisglugganum**. Samstíga seldum gjafakortum ásamt pöntunum í takt. Notuð gjafakort verða einnig flutt inn með pöntuninni en nú sem færsluhirti. Takið eftir að gjafakortið minnkar ekki upphæðina í reikning.

Til að yfirfara Útgefin og notuð gjafakort skal velja þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **gjafakort** og veldu svo tengda tengilinn.

## <a name="transactions"></a>Færslur

Greiðslufærslurnar sem áttu sér stað á Shopify eru samstilltar ásamt pantanunum og hægt er að skoða *Shopify þær á síðunni pantanir*.

Til að yfirfara allar færslur skaltu velja þá ![ljósaperu sem opnast Segðu mér aðgerðina 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **færslur** og velja tengdan tengil.

## <a name="payouts"></a>Útgreiðslur

Ef verslunin þín er búin Shopify að gera greiðslur virkar færðu greiðslur í gegnum *Shopify útborganir* þegar viðskiptavinur greiðir með Shopify greiðslum og flýta fyrir afgreiðslugeymslu.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samstilla Greiðsluspjald til að opna **Shopify Vinnukortasíðuna**.
3. **Veljið aðgerðina samstilling Payouts**.

Til að fara yfir allar útborganir skaltu velja þá ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **payouts**, og velja tengdan tengil.

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
