---
title: Samstilla og uppfylla sölupantanir
description: Setja upp og keyra innflutning og vinnslu sölupöntunar úr Shopify.
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: e7c54cc620011d238942c093a05918e2f4e57c7d
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768097"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Samstilla og uppfylla sölupantanir

Í þessari grein er lýst nauðsynlegum stillingum og skrefum sem þarf að framkvæma til að samstilla og uppfylla sölupantanir.

## <a name="set-import-of-orders-on-the-shopify-shop-card"></a>Stilla innflutning á pöntunum á Shopify verkstæðisspjaldinu

Regluleg Shopify pöntun getur haft aukaupphæðir ofan á, eins og sendingargjöld eða ef gert ráð fyrir ábendingum. Þessar upphæðir verða bókaðar beint í fjárhagsreikninga. Velja fjárhagsreikninginn sem á að nota fyrir tilteknar færslur:

- **Reikningur sendingarkostnaðar**
- **Selt gjafakorti**, nánari upplýsingar er að finna [á gjafakorti](synchronize-orders.md#gift-cards).
- **Ábending reikningur**  

Gera **sjálfvirkt stofna pantanir** til að stofna söluskjöl sjálfvirkt í [!INCLUDE[prod_short](../includes/prod_short.md)] pöntuninni sem Shopify er flutt inn.
Söluskjalið í [!INCLUDE[prod_short](../includes/prod_short.md)] inniheldur tengil við Shopify pöntunina. Ef, er virkjað **Shopify Pöntunarnr. á Doc. línu** þá verða þessar upplýsingar endurteknar í sölulínu af gerðinni *comment*.

**Í reitnum upprunasvæði** skattsvæðis er hægt að tilgreina forgang að því hvernig velja á skattsvæðiskóta eða VSK-viðskiptabókunarflokk á grundvelli aðseturs. Þetta þrep á við um lönd með VSK en hægt er að nota það fyrir VSK-lönd. Nánar er fjallað [um Skattaleg ummæli](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Vörpun afhendingarmáta

**Sjálfkrafa er hægt að fylla út kóta** afhendingarmáta fyrir söluskjöl Shopify. Stilla **þarf vörpun** afhendingaraðferðar.

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem skilgreina á vörpun á síðu opinna **Shopify vinnukorta**.
3. **Veljið aðgerðina vörpun** afhendingarmáta. Færslurnar fyrir sendingaraðferðirnar sem eru [**skilgreindar í sendingarstillingum**](https://www.shopify.com/admin/settings/payments) í admin **Shopify þínum** eru stofnaðar sjálfkrafa.
4. **Í reitnum Nafn** er hægt að sjá nafn sendingaraðferðar Shopify.
5. **Færið inn Aðferðarkóta** fyrir afhendingarmáta samsvarandi Sendingaraðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Ef margar sendingargjöld eru tengd sölupöntun; aðeins ein verður valin sem Sendingaraðferð og úthlutuð í söluskjali.

### <a name="payment-method-mapping"></a>Vörpun greiðsluaðferðar

Til að færa **inn greiðsluaðferðarkóta** fyrir söluskjöl sem eru flutt inn Shopify sjálfkrafa þarf að skilgreina **greiðsluaðferðarvörpun**.

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem skilgreina á vörpun á síðu opinna **Shopify vinnukorta**.
3. **Veljið aðgerðina Greiðsluaðferðarvörpun**.
4. **Í reitina gátt** -og **kreditkortafyrirtæki** er fært inn heitið Greiðsluháttur Shopify. Færslan verður stofnuð sjálfkrafa þegar pantanir á shopify eru fluttar inn.
5. **Færið inn Greiðsluaðferðarkóta** með samsvarandi greiðsluaðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].
6. **Stillið forgang** fyrir tilvik þegar viðskiptamaður notar marga greiðsluhætti. Greiðsluaðferðin með mestan forgang fær valið í söluskjalinu. Ef báðir Greiðsluaðferðirnar hafa sama forgang er Greiðsluaðferðin með hæstu upphæðina notuð.

## <a name="run-order-synchronization"></a>Keyra samstillingu pöntunar

Eftirfarandi ferli lýsir því hvernig á að flytja inn og uppfæra sölupöntunum.

> [!NOTE]  
> Eldri pantanir í Shopify má ekki flytja inn. Afvirkja **sjálfvirkt** í **hlutanum** **pöntunarvinnsla** í útskráningarstillingum í **Shopify admin** til að ganga úr skugga um að allar pantanir séu fluttar inn [!INCLUDE[prod_short](../includes/prod_short.md)]. Ef flytja þarf inn geymdar pantanir skal nota **ónauðsynlegar** aðgerðir í [pantansíðunni](https://www.shopify.com/admin/orders)Shopify admin.

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem á að flytja inn pantanir til að opna **Shopify spjald** -síðu verslunar.
3. **Velja pantanin** aðgerð.
4. **Veldu samkeyrslupantanirnar úr Shopify** aðgerðinni.
5. Skilgreina afmarkanir í pöntunum eftir þörfum. Til dæmis er hægt að flytja inn fullgreiddar pantanir eða þær sem eru með lágt áhættustig.
6. Velja hnappinn **Í lagi**.

Einnig er hægt að leita að **Samstillingarpöntunum úr Shopify** runuvinnslu.

Þegar innflutningi er lokið er hægt að kanna Shopify pöntunina og finna allar tengdar upplýsingar, svo sem greiðslufærslur, sendingarkostnað, uppfylla, hættustig. Einnig er hægt að sjá pöntunarstaðfestingu sem send er viðskiptavininum með því að velja **Shopify aðgerðina staða**.

> [!NOTE]  
> Hægt er að vafra um **Shopify gluggann pantanir** beint og þú sérð pantanir með *opinni* stöðu úr öllum verslunum. Til að fara yfir fullgerðar pantanir þarf að opna **Shopify pantanassíðu** úr glugganum tiltekið **Shopify verkstæðisspjald**.

## <a name="create-sales-document-in-business-central"></a>Stofna söluskjal í Viðskiptamiðinu

**Ef Sjálfvirk pantanavíxla** eru virkjuð á **Shopify verkstæðisspjaldi**, reynir það [!INCLUDE[prod_short](../includes/prod_short.md)] að búa til söluskjal þegar pöntun er flutt inn. Ef um er að ræða vinnslu sem tekur til atriða, til dæmis ef Viðskiptamaður eða afurð vantar, þarf að laga vandann og reyna að stofna sölupöntun aftur.

### <a name="to-create-sales-document"></a>Til að stofna söluskjal

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina þar sem á að samstilla pantanir til að opna **Shopify spjald-síðu vinnukorts**.
3. **Velja pantanin** aðgerð.
4. Veljið pöntunina sem stofna á söluskjal fyrir og veljið **aðgerðina stofna söluskjöl**.
5. Velja **Já**.

Shopify Ef pöntunin krefst uppfyllingar **verður sölupöntunin** stofnuð til að uppfylla Shopify pantanirnar. Til dæmis, þau sem innihalda aðeins gjafakort **verður sölureikningurinn** stofnaður.

Söluskjal er nú stofnað og hægt er að stjórna því með notkun staðalvirkleikaeiginleika [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="manage-missing-customers"></a>Stjórna týndan viðskiptavin

Ef stillingarnar koma í veg fyrir að viðskiptavinur geti stofnað sjálfkrafa og rétt fyrirliggjandi viðskiptavinar finnst ekki er viðskiptamanni Shopify úthlutað pöntun handvirkt. Nokkur kostur er á:

- Hægt er að úthluta reitnum **Selt-til viðskm.** Beint í **Shopify pöntunina** með því að velja viðskiptavin af lista yfir viðskiptamenn sem fyrir eru.
- Hægt er að velja sniðmátskóta viðskiptamanns, stofna og úthluta viðskiptamanninum **með aðgerðinni stofna nýjan viðskiptavin** í **Shopify pöntuninni**.
- Hægt er að varpa fyrirliggjandi viðskiptamanni á tengdan **Shopify viðskiptavin** í **Shopify glugganum Viðskiptavinir** og velja **síðan aðgerðina leita að vörpun** í **Shopify pöntuninni**.

### <a name="tax-remarks"></a>Skattaleg ummæli

Þegar innflutt Shopify pöntun inniheldur upplýsingar um skatta, fá skattstofnar endurreiknað þegar söluskjal er stofnað. Þess vegna er mikilvægt að VSK-reikning/Skattastillingar séu réttar skv [!INCLUDE[prod_short](../includes/prod_short.md)].

- Margfeldi afurðskatts/VSK-vaxta. Sumar vörutegundir eru til dæmis gjaldskyldar fyrir minni skatthlutföll. Þær vörur þurfa að [!INCLUDE[prod_short](../includes/prod_short.md)] vera til í og vera kortlagðar í Shopify vörum. Að öðrum kosti er notaður VSK-vörubókunarflokkurinn til að nota sjálfvirka stofnun týnandi vara.

- Aðsetur-háð skatthlutföll. Svæðið Forgangur skattsvæðis er **notað ásamt** töflunni Sniðmát **viðskiptamanns til að skrifa yfir staðlaðar röksemdir sem fylla út** kóta **skattsvæðis í söluskjalinu.** **Reiturinn Forgangur** skattsvæðis Tilgreinir forgang þar sem aðgerðin á að taka með upplýsingar um land/svæði og ríki/hérað. Síðan er fundin samsvarandi færsla í Shopify sniðmátum viðskiptamanns og **Skattsvæðiskóti**, **skattskyld** og **VSK-Bus. bókunarflokkur** er notaður þegar söluskjal er stofnað.

## <a name="synchronize-shipments-to-shopify"></a>Samstilla sendingar á Shopify

Þegar sölupöntun sem er stofnuð úr Shopify pöntun er afhent er hægt að samstilla afhendingarnar við Shopify.

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **samstillingu afhendingar við Shopify** og veljið tengdan tengil.
2. Skilgreinið afmarkanir á sendingar eftir þörfum. Til dæmis er hægt að uppfæra vörusendingu sem er bókuð á tilteknum degi.
3. Velja hnappinn **Í lagi**.

Röðin sem í Shopify verður er merkt sem uppfyllt. Viðskiptavinurinn fær sjálfkrafa tilkynningu um sendingu sendingar eða textaskilaboð (SMS). Ef flutningsaðili og rakningarkóði eru tilgreind á sendingunni eru rakningarupplýsingar hafðar með í tölvupóstinum.

> [!NOTE]  
> Munið að keyra **samstillingu pantana frá Shopify** til að uppfæra stöðu pöntunar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Í tengimyningum eru Skjalasöfn einnig fullkomlega launuð og fullnaðarpantanir í bæði Shopify og í [!INCLUDE[prod_short](../includes/prod_short.md)] því kveðið að skilyrðin séu uppfyllt.

### <a name="shipping-agents-and-tracking-url"></a>Farmflutningar og rakningarvefslóð

**Ef bókaða söluafhendingarskjalið** inniheldur **flutningskóta** og/eða **pakkakengingu nr.** verða þessar upplýsingar sendar til Shopify og til enda viðskiptamanns í tölvupósti staðfestingar sendingar.

Mælingar fyrirtækja eru útfylltar út frá færslu Flutningsinnar með eftirfarandi forgangi (frá hæsta til lægsta):

- **Shopify Rakstrarfélagið**
- **Heiti**
- **Kóði**

Ef svæðið slóð **á** rakningu á pakka er fyllt út fyrir flutningsskrá staðfestingar mun sendingarslóð innihalda einnig rakningarvefslóð.

## <a name="gift-cards"></a>Gjafakortum

Shopify Í versluninni er hægt að selja gjafakort, sem síðar má nota til að greiða fyrir alvöru vörur.

Þegar verið er að fást við gjafakort er mikilvægt að slá inn gildi í **reitinn Selt gjafakort** í **Shopify verkstæðisglugganum**. Samstíga seldum gjafakortum ásamt pöntunum í takt. Notuð gjafakort verða einnig flutt inn með pöntuninni en nú sem færsluhirti. Takið eftir að gjafakortið minnkar ekki upphæðina í reikning.

Til að yfirfara Útgefin og notuð gjafakort skal velja þá ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **gjafakort** og veldu svo tengda tengilinn.

## <a name="transactions"></a>Færslur

Greiðslufærslurnar sem áttu sér stað á Shopify eru samstilltar ásamt pantanunum og er hægt að skoða þær *Shopify úr pöntuninni*.

Til að yfirfara allar færslur skaltu velja ![lightljósaperuna sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **færslur** og velja tengdan tengil.

## <a name="payouts"></a>Útgreiðslur

Ef verslunin þín er búin Shopify að gera greiðslur virkar færðu greiðslur í gegnum *Shopify útborganir* þegar viðskiptavinur greiðir með Shopify greiðslum og flýta fyrir afgreiðslugeymslu.

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verkstæðið sem á að samstilla greiðslukort við til að opna **Shopify vinnuspjald**.
3. **Veljið aðgerðina samstilling Payouts**.

Til að fara yfir allar útborganir skaltu velja þá ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **payouts**, og velja tengdan tengil.

## <a name="see-also"></a>Sjá einnig

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
