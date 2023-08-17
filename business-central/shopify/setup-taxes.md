---
title: Setja upp skatta fyrir Shopify tengingu
description: Hvernig á að setja upp skatta í Shopify og Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# <a name="set-up-taxes-for-the-shopify-connection"></a>Setja upp skatta fyrir Shopify tenginguna

Í þessari grein munum við rannsaka hvernig ýmsar stillingar í  Shopify  því hafa áhrif á hæðarverð og skatta sem birta til viðskiptavina. Við munum einnig hylja hvernig á að samskipa  [!INCLUDE[prod_short](../includes/prod_short.md)]  til að styðja stillingar í Shopify. Þessari grein er ekki ætlað að vera ítarlegur leiðarvísir um skattlagningu. Hafðu samband við skattyfirvöld á staðnum eða skattalegan fagaðila til að fá frekari upplýsingar.  

Í greininni er gert ráð fyrir að gjaldskylt sé að greiða skatta þegar seldar eru vörur á staðnum eða á alþjóðavettvangi.

## <a name="if-you-sell-domestically"></a>Ef þú selur innanlands

Eftir að búið er að samskipa  Shopify  til að innheimta skatta í heimalandi eða svæði notanda er hægt að ákveða hvernig birta á verð á Storefront.

Tilgreint er hvort eigi að hafa skatt í verði með því að kveikja eða slökkva á öllum verðum er  **með skattvíxla**  í  [**stillingum skatta og skyldur**](https://www.shopify.com/admin/settings/taxes)  í  **Shopify  admin**.

Víxlun er vanalega virkjuð fyrir eftirtalin lönd/svæði:

* Ástralía
* Austurríki
* Belgía
* Tékkland
* Danmörk
* Finnland
* Frakkland
* Þýskaland
* Ísland
* Ítalíu
* Holland
* Nýja-Sjáland
* Noregur
* Spánn
* Svíþjóð
* Sviss
* Bretland. 

Á mörkuðum eins og þessum er verð á 100 EUR skilgreint á afurðakorti þegar Virðisauki (VSK) er virðisaukaskattur. Verðið, með VSK, birtist viðskiptavininum í Storefront stílsniðinu og við innritun.  

Í Bandaríkjunum og Kanada gera Viðskiptavinir ekki ráð fyrir að verð feli í sér skatt. Tak er bætt við útskrift, þannig að  **öll verð eru með skattskipta**  er yfirleitt slökkt. Í þessu tilfelli er verð $100 skilgreint á vörukortinu sé verðið án skatts. Við innritun bætast skattar á verð.

Til að styðja við atburðarásina þar sem  **öll verð eru með skatti**  er valið  [!INCLUDE[prod_short](../includes/prod_short.md)] í eftirfarandi reiti á  **Shopify  vinnukortasíðunni** :  

1. Kveikja á  **verði með VSK**  -víxl.  
2.  **Í reitnum VSK-viðskiptabókunarflokkur**  skal tilgreina bókunarflokkinn sem notaður er fyrir innlenda viðskiptamenn.  

Skilgreinið nú vöruverð í  **reitunum birgðaspjald**  eða  **Söluverð**, með eða án skatts. Þegar útflutningur á verði til  Shopify,  [!INCLUDE [prod_short](../includes/prod_short.md)]  inniheldur innlenda skatta í reiknuðu verði og sýnir að verð fyrir vöruna í Shopify.

[!Note]
> Þessar stillingar hafa áhrif á útflutning verðs. Þegar pantanir  Shopify eru fluttar inn kemur stillingin fyrir  **verð með VSK**  í  **sniðmáti**  viðskiptamanns á  Shopify  verkstæðisspjaldinu, eða sniðmát viðskiptavinar fyrir hvert land/svæði. Jafnvel þótt sjálfgefinn Viðskiptamaður sé notaður fyrir innfluttar pantanir þarf að fylla út  **kóta** sniðmáts viðskiptamanns.

## <a name="if-you-sell-internationally"></a>Ef þú selur alþjóðlega

Þessi hluti skoðar stillingar fyrir áætlanir þar sem þú hefur þörf fyrir að innheimta skatta þegar selt er í öðru landi/svæði, eins og öðrum löndum/svæðum í ESB.

 Shopify Sem stendur leyfir Connector aðeins að flytja út eitt verð. Shopify er sjálfkrafa lagt á staðbundna skatta, gjaldmiðla og námundun. **Allt verð með skatti** birtir niðurstöður í aðgerðunum sem lýst er í eftirfarandi undirköflum.

### <a name="all-prices-include-tax-is-selected"></a>Öll verð fela í sér að skattur er valinn

|-|Sala innanlands|Erlent land/svæði þar sem þú ert að innheimta skatta|Erlent land/svæði þar sem ekki er verið að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|1200|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1200|1200|

Verð fyrir viðskiptavinardvöl haldist óbreytt, óháð staðsetningu þeirra, en það hefur áhrif á framlegð þína vegna mismunandi skatthlutfalla fyrir hvert land/svæði.

### <a name="all-prices-include-tax-is-not-selected"></a>Öll verð eru með skatti er ekki valinn

|-|Sala innanlands|Erlent land þar sem þú innheimtir skatt|Erlent land þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1000|1000|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1250|1000|

Shopify bætir staðbundnum skatti við verðið sem tilgreint er á vöruspjaldinu eftir því hvaðan vörur eru sendar til.

## <a name="dynamic-tax-inclusive-pricing"></a>Sveigjanleg verðlagning með skatti

Lönd/svæði hafa mismunandi þarfir að meðtöldum skatti í verði. Ef óskað er eftir að verð taki sjálfkrafa með skatti er hægt að gera  [verðlagningu](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing)  með breytilegum skattlagningu í Shopify.

Í þinni  **Shopify  Stjórnun** skaltu velja  **taka með eða útiloka skatt samkvæmt landi**  viðskiptamanns á  **öðrum mörkuðum-kjörstillingum**  hluta  [**stillinga markaðarins**](https://www.shopify.com/admin/settings/markets) .  

> [!NOTE]
> Þessi stilling hefur ekki áhrif á verð á innlendum mörkuðum sem stjórnast af  **öllum verðum með skattvíxla** .

### <a name="all-prices-include-tax-is-selected-1"></a>Öll verð fela í sér að skattur er valinn

|-|Sala innanlands|Erlent land/svæði þar sem skattur er innifalinn í verði|Erlent land/svæði þar sem skattur er undanskilinn|
|------------------------|---------------|---------------|--------|
|Verð sem birtist í netversluninni|1200|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

Verðið fyrir hvern viðskiptavin breytist, allt eftir staðsetningu þeirra.

### <a name="all-prices-include-tax-is-not-selected-1"></a>Öll verð eru með skatti er ekki valinn

|-|Sala innanlands|Erlent land/svæði þar sem skattur er innifalinn í verði|Erlent land/svæði þar sem skattur er undanskilinn|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

> [!NOTE]
> Í öllum verðum með skattskipta  **breytir ekki því**  hvernig verð Sýna til alþjóðlegra viðskiptavina.

## <a name="if-you-sell-to-eu-customers"></a>Ef þú selur innan ESB

Mismunandi lönd/svæði í ESB eru með mismunandi skatthlutföll í sveitarfélögum. Ef þú ert hins vegar staðsettur í ESB og selur í öðrum löndum ESB/svæðum getur þú notað skatthlutfallið í einhverjum tilvikum.  

Í þinni  **Shopify  Stjórnun** er hakað  **í gátreitinn innheimta VSK**  í  **evrópusambandshlutanum**  [**í stillingum skatta og skyldur**](https://www.shopify.com/admin/settings/taxes) .

|Innheimta VSK|VSK-hlutfall|
|-|-|
|Undanþága fyrir smáfyrirtæki|Notaðu innlenda skatthlutfallið þitt fyrir alla sölu innan ESB|
|Skráning á One-Stop vinnuskyldu eða tilteknar skráningar á landi/svæði|Nota VSK-hlutfall af landi/svæði viðskiptavinar|

### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Innheimta VSK sem er stilltur á skráningu í netverslun

Í eftirfarandi dæmi  **er kveikt á öllum verðum með skattskipta** . Verðið á vöruspjaldinu er stillt á *1200*.

|-|Sala innanlands|Erlent land/svæði|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1250|
|Prósenta skattur gefa einkunn|20|25|
|Verð þegar gengið er frá kaupum|1200|1250|

### <a name="collect-vat-set-to-micro-business-exemption"></a>Innheimta VSK sem er stilltur á undanþágu vegna smáfyrirtækja

Í eftirfarandi dæmi  **er kveikt á öllum verðum með skattskipta** . Verðið á vöruspjaldinu er stillt á *1200*.

|-|Sala innanlands|Erlent land/svæði með skatthlutfalli sveitarfélaga 25 prósent.|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|
|Prósenta skattur gefa einkunn|20|20|
|Verð þegar gengið er frá kaupum|1200|1200|

Shopify notar innlendu skatthlutfallið og hunsar skatthlutfallið í erlendu landi/svæði þegar það reiknar endanlegt verð.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Innflutningur Shopify pantana seldur til alþjóðlegra viðskiptavina

Ef verið er að innheimta skatta frá mörgum löndum/svæðum verður að skilgreina tiltekna lands-/svæðisstillingu í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það er ástæða fyrir því að þessa stillingu þarf. Þegar söluskjal er stofnað í  [!INCLUDE[prod_short](../includes/prod_short.md)],  [!INCLUDE [prod_short](../includes/prod_short.md)]  reiknar skatta í stað þess að endurnota skatta sem fluttir eru inn Shopify.

Tilgreindar eru lands-/svæðisbundnar stillingar á  **Shopify  viðskiptavinarsíðu sniðmáts** . Hægt er að  **skilgreina sjálfgefinn viðskm.** eða **Sniðmátsnr. viðskiptamanns.**. Í öðru hvoru tilviki skal tryggja viðskiptavininum eða sniðmátinu eftirfarandi reiti útfyllta:

1. **Almennur viðskiptabókunarflokkur** (notaður fyrir erlenda viðskiptavini).
2. **VSK-viðskiptabókunarflokkur** (notaður fyrir erlenda viðskiptavini).
3. **Verð með VSK** (í samræmi við stillingu hér til Shopify hliðar):

* Velja  **skal Já**  ef  **öll verð eru með skatti**  er virkjaður og  **taka með eða útiloka skatt samkvæmt því að land**  viðskiptamanns er óvirkt.
* Velja Nei ef  **öll verð eru með skatti**  er  **ekki**  hægt  **að nota eða útiloka að skattur sem byggður er á landi**  viðskiptamanns sé gerður óvirkur.
* Velja  **skal Já**  ef  **taka á með eða útiloka skatt samkvæmt landi**  viðskiptamanns er virkt og land eða svæði er skráð í  [löndum/svæðum sem eru á skrá yfir lönd/svæði](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Velja  **Nei**  ef  **hafa á með eða útiloka skatt samkvæmt landi**  viðskiptamanns er virkjað og land/svæði er ekki skráð í löndum/svæðum sem eru á  [skrá yfir lönd/svæði](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> Stillingarnar í reitnum **Allt verð með VSK** eru úr sniðmátinu, ekki frá tilteknum viðskiptavini. Mikilvægt er að skilgreina sniðmát viðskiptamanns.

## <a name="other-tax-remarks"></a>Aðrar athugasemdir um skatta

Þó að innflutt Shopify pöntun innihaldi upplýsingar um skatta eru skattarnir endurreiknaðir þegar söluskjal er búið til. Sem endurútreikningur þýðir að mikilvægt er að VSK-/skattastillingar séu réttar [!INCLUDE[prod_short](../includes/prod_short.md)].

* Mörg vöruskatts- eða VSK-hlutföll. Til dæmis eru tilteknir vöruflokkar gjaldgengir fyrir lægri skatthlutfalli. Hægt er að nota eiginleikann [hnekking skatts](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) í Shopify. Þegar vörur  [!INCLUDE[prod_short](../includes/prod_short.md)] eru fluttar inn og stofnaðar eru þær notaðar með skattuppsetningunni sem tilgreind er í sniðmátskótanum í  Shopify  versluninni. Ef pantanir eru fluttar inn með slíkum vörum skal uppfæra VSK-vörubókunarflokkinn.  
* Skatthlutföll háð heimilisfangi. Notaðu reitinn **Forgangur skattsvæðis** ásamt **Sniðmát viðskiptavinar** til að skrifa yfir stöðluðu rökin sem fylla út **Skattsvæðiskóða** í söluskjalinu. Reiturinn **Forgangur skattsvæðis** tilgreinir forgang varðandi það hvar aðgerðin á að taka við upplýsingum um landið eða svæðið og fylkið eða héraðið. Þá er samsvarandi skrá í Shopify sniðmátum viðskiptavina auðkennd og **Skattsvæðiskóði**, **Skattskylda** og **VSK-viðsk.bókunarflokkur** eru notaðar þegar söluskjal er búið til.  

## <a name="see-also"></a>Sjá einnig

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
