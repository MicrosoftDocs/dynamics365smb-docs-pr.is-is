---
title: Samstilla færslur og greiðslur
description: Settu upp og keyrðu innflutning á færslum og greiðslum frá Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="transactions-and-payouts"></a>Færslur og greiðslur

Þegar viðskiptamaður lýkur greiðsluferlinu í netversluninni eru upplýsingar um greiðslur vistaðar sem **Færsla**. Margar færslur gætu verið tengdar pöntuninni, t.d. þegar viðskiptamaður notar gjafakort til að greiða hluta kostnaðarins og notar svo kreditkort eða PayPal fyrir eftirstandandi upphæð.

Ef þú notar Shopify greiðslu sem greiðsluþjónustuaðila getur þú einnig séð greiðslur af Shopify og inn á bankareikninginn þinn til viðbótar við upplýsingar um mótteknar greiðslur frá viðskiptamanninum.

## <a name="transactions"></a>Færslur

Greiðslufærslurnar sem eiga sér stað í Shopify eru samstilltar við pantanirnar og er hægt að skoða þær á síðunni **Shopify Pantanir**.

Til að fara yfir allar færslur skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Færslur** og velja viðkomandi tengil.

 **Bókaða Reikningnr.**  svæðið getur verið hjálplegt í afstemmingarferlinu.

Ef þú grunnstilltir vörpun greiðslumáta mun stofnað söluskjal fá kóða greiðslumáta úthlutaðan. Frekari upplýsingar er að finna í [Vörpun greiðslumáta](#payment-method-mapping).

## <a name="payouts"></a>Útgreiðslur

Ef verslunin þín notar Shopify Payment færðu greiðslur í gegnum **Shopify útborganir** þegar viðskiptamaður greiðir með Shopify Payments og hraðara greiðsluferli.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Veldu verslunina sem á að samstilla útborganir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Samstilla útborganir**.

Til að fara yfir allar útborganir skaltu velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Útborganir** og velja viðkomandi tengil.

**Útborganir** eru einungis í upplýsingaskyni og hafa ekki áhrif á fjárhagsbók eða bankabók þótt þær geti komið að gagni við úrvinnslu bankareikningsyfirlits þíns.

## <a name="payment-method-mapping"></a>Vörpun greiðslumáta

Til að fylla út **Kóða greiðslumáta** fyrir söluskjöl sem flutt eru inn úr Shopify sjálfkrafa þarftu að grunnstilla **Vörpun greiðslumáta**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Veljið þá verslun sem á að skilgreina vörpun fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Vörpun greiðslumáta**.
4. Í reitina **Gátt** og **Kreditkortafyrirtæki** skal færa inn heiti greiðslumátans frá Shopify. Færslan verður stofnuð sjálfkrafa þegar þú flytur inn Shopify pantanir.
5. Sláðu inn **Kóða greiðslumáta** með samsvarandi greiðslumáta í [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Veldu **Forgang** fyrir tilvik þar sem viðskiptamaður notar marga greiðslumáta. Greiðslumátinn með hæsta forgang er valinn í söluskjalinu. Ef báðir greiðslumátar eru með sama forgang er notaður sá greiðslumáti sem er með hæstu notuðu upphæðina.

> [!NOTE]  
> Ef samsvarandi greiðslumáti í [!INCLUDE[prod_short](../includes/prod_short.md)] er með reitina **Tegund mótreiknings** og **Númer mótreiknings** fyllta út mun reikningskerfið við bókun stofna mótfærslu af gerðinni *Greiðsla* og nota hana á tegund *Reiknings* í fjárhagsfærslu viðskiptamannsins.

## <a name="use-cases"></a>Dæmi um notkun
  
Aðilar:

* Kaupandi - aðili sem kaupir vörur af Shopify netverslun.
* Söluaðili - fyrirtækið þitt.
* Greiðsluþjónustuaðili - fyrirtæki sem auðveldar greiðslumiðlun fyrir þig. Getur verið Shopify Payments eða þriðji aðili.

### <a name="how-money-flows"></a>Hvernig peningar flæða

Kaupandi kaupir vörur í netverslun. Síðasta stigið er að greiðsluvinnslan.

>[!NOTE]
> Þetta dæmi nær ekki yfir mál þegar gengið er frá greiðslu fyrir utan Shopify greiðsluferlið sem gildir fyrir B2B-aðstæður.
  
Kaupandinn greiðir með kreditkorti, PayPal eða einhverjum staðbundnum greiðslumáta eins og MobilePay í Danmörku. Greiðsluþjónustuaðilinn tekur við allri upphæðinni frá kaupanda. Á þessari stundu eru peningar kaupenda fluttir yfir á greiðsluþjónustuaðilann.

Það fer eftir greiðsluþjónustuaðilanum, en söluaðilinn gæti séð þennan pening á reikningnum sínum hjá greiðsluþjónustuaðilanum - bæði mótteknar upphæðir ásamt frádregnum þóknunum. Greiðsluþjónustuaðilar taka oft þóknun af hverri færslu og í sumum tilvikum geta þeir einnig verið með fast gjald.
  
Það fer eftir greiðsluþjónustuaðilanum hvort söluaðilinn setur af stað handvirka millfærslu peninganna yfir á bankareikning þeirra (útborgun) eða hvort það gerist sjálfkrafa á ákveðnu tímabili - einu sinni á dag, einu sinni á mánuði og svo framvegis.
  
Það fer eftir bankanum, en söluaðilinn getur séð þessa færslur á innleið á bankareikningnum í gegnum netbanka eða á bankayfirliti.

Það eru nokkrir valkostir um hvernig á að meðhöndla greiðslufærslur í [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a>Valkostur 1: afstemma millifærslur á innleið á bankareikning á móti upprunalegum reikningum
  
Söluaðili flytur inn sölupöntun í [!INCLUDE[prod_short](../includes/prod_short.md)] og bókar sendingu og reikning.

Niðurstaða: kerfið stofnar **Fjárhagsfærslu viðskiptamanns** af tegundinni *Reikningur* með allri upphæðinni, **Opna** er stillt á „Já“. **Eftirstandandi upphæð** er jöfn reikningsfærðu upphæðinni.

Söluaðili flytur inn bankayfirlit með greiðsluafstemmingarbók.

Vandamál:

1. Það getur verið erfitt ef það eru margir reikningar (og kreditreikningar) en ein útborgun frá greiðsluþjónustuaðilanum með eingreiðslu.
2. Upphæð stemmir yfirleitt ekki vegna þóknunar. Hægt er að nota greiðsluvikmörk og/eða greiðsluafslætti til að meðhöndla gjöld.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a>Valkostur 2: afstemma millifærslur á innleið á bankareikning á móti bráðabirgðareikningi sem stendur fyrir peninga hjá greiðsluþjónustuaðila
  
Söluaðili flytur inn sölupöntun í [!INCLUDE[prod_short](../includes/prod_short.md)] og bókar sendingu og reikning.
  
Niðurstaða: kerfið stofnar fjárhagsfærslu viðskiptamanns af gerðinni **Reikningur** með allri upphæðinni og **Opna** er stillt á „Já“. **Eftirstandandi upphæð** er jöfn reikningsfærðu upphæðinni.

En þar sem sölupöntunin er með kóða greiðslumáta þar sem reitirnir **Tegund mótreiknings** og **Númer mótreiknings** eru fylltir út, stofnar kerfið sjálfkrafa aðra fjárhagsfærslu viðskiptamanns af gerðinni **Greiðsla** og notar hana á fjárhagsfærslu viðskiptamanns sem stofnuð var áður.

>[!NOTE]
> Kerfið fyllir út reitinn „Kóði greiðslumáta“ samkvæmt vörpun greiðslumáta. Frekari upplýsingar er að finna í [Vörpun greiðslumáta](#payment-method-mapping).
  
Hægt er að skilgreina mótreikninga fyrir greiðsluaðferðir á tvennan hátt:

* **Tegund mótreiknings** stilltur á *Banki* og reiturinn **Númer mótreiknings** fylla út sérstakan bankareikning sem stendur fyrir reikninginn þinn hjá greiðsluþjónustuaðilanum.
* **Tegund mótreiknings** stillt sem *Fjárhagsreikningur** og reiturinn **Númer mótreiknings** fylla út á fjárhagsreikninginn sem stendur fyrir reikninginn þinn hjá greiðsluþjónustuaðilanum.

Það er skynsamlegt að nota bankareikning ef greiðsluþjónustuaðilinn flytur út einhvers konar reikningsyfirlit, sem þú getur flutt inn í greiðsluafstemmingarbókina.

Söluaðili flytur inn bankayfirlit með greiðsluafstemmingarbók. Hægt er að vinna úr útborgun á innleið:

* sem millifærsla frá öðrum banka. Ef millifærslan tekur nokkra daga eða felur í sér gjaldmiðlaskipti getur verið gott að nota bráðabirgðafjárhagsreikning.
* sem mismunur á fjárhagsreikningnum sem táknar reikninginn þinn hjá greiðsluþjónustuaðilanum.
  
Eftirstöðvar á fjárhags- eða bankareikningnum sem stendur fyrir reikninginn þinn hjá greiðsluþjónustuaðilanum er hægt að afskrifa sem „gjald/þóknun“

Vandamál:

1. Hægt er að stofna marga fjárhags- eða bankareikninga ef átt er í viðskiptum við marga greiðsluþjónustuaðila. Sölupantanir í [!INCLUDE[prod_short](../includes/prod_short.md)] styðja hins vegar aðeins einn kóða greiðslumáta, sem gerir erfitt um vik að meðhöndla mál þegar kaupandi notar marga greiðslumáta fyrir pöntun.

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
