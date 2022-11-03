---
title: Samstarf og færslur og útborganir
description: Setja upp og keyra innflutning færslna og útborganir frá Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30124, 30125, 30130, 30131, 30132, 30133, 30134,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: f4833a3fa77cdff587947a9686e61e3255b66a7c
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728708"
---
# <a name="transactions-and-payouts"></a>Færslur og útborganir

Þegar viðskiptavinur lýkur útskrift sína í netverslun eru upplýsingar um greiðslur vistaðar sem **færsla**. Það gætu verið margar færslur tengdar pöntuninni, eins og til dæmis þegar viðskiptavinur notar gjafakort til að greiða einhvern kostnað og notar síðan kreditkort eða PayPal fyrir eftirstandandi upphæð.

Ef þú notar Shopify greiðslu sem greiðsluþjónustuveitandi þá þarf auk þess upplýsingar um peninga sem berast frá viðskiptavininum af greiðsluveitunni, einnig er hægt að sjá greiðslur frá Shopify þér á bankareikninginn þinn.

## <a name="transactions"></a>Færslur

Greiðslufærslurnar sem eiga sér stað í Shopify eru samstilltar við pantanirnar og er hægt að skoða þær á **Shopify pantansíðunni**.

Til að yfirfara allar færslur skaltu velja þá ![ljósaperu sem opnast Segðu mér aðgerðina 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **færslur** og velja tengdan tengil.

Ef vörpun greiðslumáta er samskipað þá er búið að úthluta innkaupaskjali Greiðsluháttur. Frekari upplýsingar um [Greiðsluaðferðarvörpun](#payment-method-mapping).

## <a name="payouts"></a>Útgreiðslur

Ef verslunin notar Shopify greiðslu munt þú fá greiðslur í gegnum **Shopify útborganir** þegar viðskiptavinur greiðir með Shopify greiðslum og flýta fyrir afgreiðsluúttöku.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu síðan tengda tengilinn.
2. Veljið verslunina þar sem á að samstilla Greiðsluspjald til að opna **Shopify Vinnukortasíðuna**.
3. **Veljið aðgerðina samstilling Payouts**.

Til að fara yfir allar útborganir skaltu velja þá ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **payouts**, og velja tengdan tengil.

**Útborganir** eru eingöngu til upplýsinga og hafa ekki áhrif á fjárhag eða fjárhag notanda þó að þær geti verið hjálplegar þegar unnið er úr uppgjöri bankareiknings.

## <a name="payment-method-mapping"></a>Vörpun greiðsluaðferðar

Til að færa **inn greiðsluaðferðarkóta** fyrir söluskjöl sem eru flutt inn Shopify sjálfkrafa þarf að skilgreina **greiðsluaðferðarvörpun**.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu síðan tengda tengilinn.
2. Veljið verkstæðið sem skilgreina á vörpun á til að opna **Shopify vinnukortasíðuna**.
3. **Veljið aðgerðina Greiðsluaðferðarvörpun**.
4. **Í reitina gátt** -og **kreditkortafyrirtæki** er fært inn heiti greiðsluaðferðar frá Shopify. Færslan verður stofnuð sjálfkrafa þegar pantanir eru fluttar inn Shopify.
5. **Færið inn Greiðsluaðferðarkóta** með samsvarandi greiðsluaðferð í [!INCLUDE[prod_short](../includes/prod_short.md)].
6. **Stillið forgang** á tilvikum þegar viðskiptavinurinn notar marga greiðsluhætti. Greiðsluaðferðin með mestan forgang fær valið í söluskjalinu. Ef báðir Greiðsluaðferðirnar hafa sama forgang er Greiðsluaðferðin með hæstu upphæðina notuð.

> [!NOTE]  
> Ef samsvarandi Greiðslumáti í [!INCLUDE[prod_short](../includes/prod_short.md)] hafi-gerð **mótreiknings og** mótreiknings nr. **útfyllist, við bókun í reikningakerfi stofnast jöfnunarfærsla fyrir** greiðslugerðina *og gildir um hana* í reikningsgerðinni *viðskiptamannafærsla*.

## <a name="use-cases"></a>Nota mál
  
Aðila

* Kaupandi-einstaklingur sem kaupir vörur af Shopify netverslun.
* Merchant-fyrirtækið þitt.
* Greiðsluþjónustuveitandi-fyrirtæki sem auðveldar greiðsluvinnslu fyrir þig. Getur verið Shopify Greiðslugeta eða þriðji aðili.

### <a name="how-money-flows"></a>Hvernig peningar streyma

Kaupandi kaupir vörur í netverslun. Síðasti áfangi er að vinna úr greiðslu.

>[!NOTE]
> Þetta dæmi nær þó ekki til tilvika þegar greiðslu er lokið utan Shopify útskriftar, sem gildir fyrir B2B áætlanir.
  
Kaupandinn greiðir með kreditkorti, PayPal eða einhverri staðbundinni greiðsluaðferð líkt og MobilePay í Danmörku. Greiðsluþjónustuveitandi tekur alla upphæðina frá kaupanda. Á þessari stundu eru peningar kaupanda færðir til Greiðsluveitunnar.

Allt frá því að Greiðsluveitan gæti orðið til gæti seljandi séð þennan pening á reikningi sínum hjá greiðsluveitunni – bæði mótteknar Eftirstöðvar, sem og Frádregin þóknun. Greiðsluþjónustuveitendur taka oft þóknun af hverri færslu og í sumum tilfellum geta þær haft fast gjald einnig.
  
Það fer eftir greiðsluveitunni hvort viðskiptamaður kallar annaðhvort millifærslu af fjármunum inn á bankareikning sinn (útborgun) handvirkt eða að það gerist sjálfkrafa innan skilgreinds tímabils-einu sinni á dag, einu sinni í mánuði o. frv.
  
Það fer eftir bankanum hvort viðskiptamaður sér þessa innsendu færslu á bankareikninginn sinn í gegnum netbankayfirlit eða í bankayfirlitinu.

Ýmsir möguleikar eru á því hvernig fara skuli með greiðslufærslur í [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a>Valkostur 1: stemmir viðtökumillifærslur við bankareikning á móti upphaflegum reikningum
  
Viðskiptamaður flytur sölupöntun til [!INCLUDE[prod_short](../includes/prod_short.md)] og bókar sendingu og reikning.

Niðurstaða: kerfið stofnar **viðskiptamannafærslu** af gerðinni *Reikningur* með heildarupphæðinni, sem **opin** er stillt á Já. **Eftirstandandi upphæð** er jöfn reikningsfærðu upphæðinni.

Viðskiptamaður flytur bankayfirlit sem notuð eru í greiðsluafstemmingarbók.

Málefni

1. Getur verið erfitt ef um marga reikninga (og kreditreikninga) er að ræða en eina útborgun frá greiðsluveitunni með moldu summu.
2. Upphæð fer venjulega ekki saman vegna þóknunar. Hægt er að nota greiðsluvikmörk eða/og greiðsluafslátt til að halda utan um þóknanir.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a>Valkostur 2: stemma af incoming millifærslur á bankareikning gegn bráðabirgðareikningi sem táknar peninga hjá greiðsluveitunni
  
Viðskiptamaður flytur sölupöntun til [!INCLUDE[prod_short](../includes/prod_short.md)] og bókar sendingu og reikning.
  
Niðurstaða: kerfið stofnar viðskiptamannafærslu af gerðinni **Reikningur** með fulla upphæð og **opin** er stillt á Já. **Eftirstandandi upphæð** er jöfn reikningsfærðu upphæðinni.

Hins vegar, vegna þess að sölupöntunin er með greiðsluaðferðarkóta þar **sem** **fyllt** er út í reitina sjálfvirkt önnur viðskiptamannafærsla af gerðinni **greiðsla** og gildir það í viðskiptamannafærslum sem stofnaðar eru áður.

>[!NOTE]
> Kerfið fyllir út reitinn Greiðsluháttur kóti út frá greiðsluaðferðarvörpun. Frekari upplýsingar um [Greiðsluaðferðarvörpun](#payment-method-mapping).
  
Hægt er að skilgreina mótreikninga vegna greiðsluaðferða með tvennum hætti:

* **Mótreikningagerð** sem er stillt sem *Banki* og **reikningur fyrir reikning nr.** fylla út sérstakan bankareikning sem stendur fyrir reikning þinn hjá greiðsluveitunni.
* **Mótlykill sem gerð** er sem *fjárhagsreikningur* * og **Mótreikningur nr.** Fyllið inn fjárhagsreikning sem stendur á reikningnum hjá greiðsluveitunni.

Það er skynsamlegt að nota bankareikning ef greiðsluþjónustuveitandi flytur út einhvers konar reikningsyfirlit, sem hægt er að flytja inn í greiðsluafstemmingarbókina.

Viðskiptamaður flytur bankayfirlit með greiðsluafstemmingarbók. Í utanaðkomandi Útborgun er hægt að vinna:

* Sem millifærslu frá öðrum banka. Ef flutningurinn tekur nokkra daga eða felur í sér gjaldeyrisviðskipti kann að vera hægt að nota bráðabirgðafjárhagsreikning.
* Sem mismunur á fjárhagsreikningnum sem stendur á reikningnum hjá greiðsluveitunni.
  
Eftirstandandi staða á fjárhags-eða bankareikningi sem stendur fyrir reikninginn hjá greiðsluveitunni má skrifa út sem "þóknanir/þóknanir"

Málefni

1. Hægt er að búa til marga fjárhags-eða bankareikninga ef verið er að eiga við margar greiðsluveitur. En sölupantanir [!INCLUDE[prod_short](../includes/prod_short.md)] styðja aðeins einn greiðsluaðferðarkóta, sem gerir erfitt að afgreiða tilvik þegar kaupandi notar margar greiðsluaðferðir við pöntun.

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
