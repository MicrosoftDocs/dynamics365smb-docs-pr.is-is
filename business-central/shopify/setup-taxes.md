---
title: Setja upp skatta fyrir Shopify tengingu
description: Hvernig á að setja upp skatta í Shopify og Business Central.
ms.date: 05/29/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# <a name="set-up-taxes-for-the-shopify-connection"></a>Setja upp skatta fyrir Shopify-tenginguna

Í þessari grein munum við rannsaka hvernig ýmsar stillingar hafa Shopify áhrif á geymsluverð og skatta sem sýna viðskiptamönnum. Við munum einnig sjá um hvernig á að stilla [!INCLUDE[prod_short](../includes/prod_short.md)] til að styðja við stillingarnar í Shopify. Þessari grein er ekki ætlað að vera ítarlegur leiðarvísir um skattlagningu. Hafðu samband við skattyfirvöld á staðnum eða skattalegan fagaðila til að fá frekari upplýsingar.  

Greinin gerir ráð fyrir að þú borgir skatta þegar þú selur vörur á staðnum eða á alþjóðavettvangi.

## <a name="if-you-sell-domestically"></a>Ef þú selur innanlands

Þegar notandi hefur skilgreint Shopify að innheimta skatta í heimalandi þínu eða svæði er hægt að ákveða hvernig verð er birt í verslunarfyrirtækjunum.

Tilgreint er hvort skattur í verði skuli innifalinn í verði með því að kveikja eða slökkva **á Öllu verði, fela í sér skattvíkkun** í [**stillingunum Skattar og Skyldur**](https://www.shopify.com/admin/settings/taxes) í **Shopify stjórnandanum**.

Vísbendingin er yfirleitt virk fyrir eftirfarandi lönd/svæði:

* Ástralía
* Austurríki
* Belgía
* Tékkland
* Danmörku
* Finnlandi
* Frakkland
* Þýskaland
* Íslandi
* Ítalíu
* Holland
* Nýja-Sjáland
* Noregi
* Spánn
* Svíþjóð
* Sviss
* Bretland

Á mörkuðum eins og þessum er verð á 100 EUR sem tilgreint er á framleiðsluspjaldinu þegar með virðisaukaskatt (VSK). Verðið, með VSK, er birt á viðskiptamanninn í versluninni og við útskráningu.  

Í Bandaríkjunum og Kanada búast viðskiptavinir ekki við að sjá verð með sköttum vegna þess að endanlegur skattur fer eftir því hvar vörur eru sendar. Skatti er bætt við prófun svo **að skattvífæringin** í öllum verðum er yfirleitt gerð óvirk. Í þessu tilviki er verð á $100 tilgreint á framleiðsluspjaldi verð án skatts. Við útritun er sköttum bætt við verðið.

Til að styðja aðstæður þar sem **Skattur er valinn í**  Öllum verðum er fyllt [!INCLUDE[prod_short](../includes/prod_short.md)] út í eftirfarandi reiti á síðu verkstæðisspjaldsins **Shopify** :  

1. Kveikja á verði **með VSK-vífæru** .  
2. Í reitnum **VSK-viðskiptabókunarflokkur** er tilgreindur sá bókunarflokkur sem notaður er fyrir innlenda viðskiptamenn.  

Nú er vöruverð skilgreint í reitunum **Birgðaspjald** eða **Söluverðlisti**, með eða án skatts. Við útflutning á verði Shopify [!INCLUDE [prod_short](../includes/prod_short.md)]  eru innlendir skattar á útreiknuðu verði og þar kemur fram það verð fyrir vöruna í Shopify.

> [!NOTE]
> Þessar stillingar hafa áhrif á útflutning á verði. Þegar pantanir eru fluttar inn úr Shopify kemur stillingin fyrir reitinn **Verð með VSK** úr **sniðmáti** viðskiptamanns á Shopify verkstæðisspjaldinu eða viðskiptamannssniðmátinu fyrir hvert land/svæði. Jafnvel þótt sjálfgefinn viðskiptamaður sé notaður fyrir innfluttar pantanir þarf að fylla út kóta **sniðmáts viðskiptamanns**.

## <a name="if-you-sell-internationally"></a>Ef þú selur alþjóðlega

Í þessum hluta eru skoðaðar stillingar fyrir aðstæður þar sem innheimta þarf skatta þegar selt er til annars lands/svæðis, svo sem annarra landa/svæða í ESB.

 Shopify Eins og er býður tengið aðeins út eitt verð. Shopify er sjálfkrafa lagt á staðbundna skatta, gjaldmiðla og námundun. **Allt verð með skatti** birtir niðurstöður í aðgerðunum sem lýst er í eftirfarandi undirköflum.

### <a name="all-prices-include-tax-is-selected"></a>Skattur í öllum verðum er valinn

|-|Sala innanlands|Erlent land/svæði þar sem þú innheimtir skatta|Erlent land/svæði þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|1200|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1200|1200|

Verðið fyrir viðskiptamanninn helst óháð staðsetningu þeirra, en framlegð hefur áhrif á framlegð vegna mismunandi skatthlutfalla eftir löndum/svæðum.

### <a name="all-prices-include-tax-is-not-selected"></a>Skattur í öllum verðum er ekki valinn

|-|Sala innanlands|Erlent land þar sem þú innheimtir skatt|Erlent land þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1000|1000|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1250|1000|

Shopify bætir staðbundnum sköttum við verðið sem skilgreint er á framleiðsluspjaldinu eftir því hvar vörur eru sendar.

## <a name="dynamic-tax-inclusive-pricing"></a>Sveigjanleg verðlagning með skatti

Lönd/svæði krefjast þess að þ.m.t. skattur á verði sé tekinn með. Ef verð á sjálfkrafa að fela í sér skatt er hægt að kveikja á [kvikri verðlagningu](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing)  Shopify með skatti með innifalinni.

Í stjórnandanum **Shopify** skal velja **Taka með eða undanskilja skatt á grundvelli lands** viðskiptamanns í **öðrum mörkuðum - Kjörstillingar** í [**stillingum markaðarins**](https://www.shopify.com/admin/settings/markets) .  

> [!NOTE]
> Þessi stilling hefur ekki áhrif á verð á innlendum mörkuðum, sem stýrt er af **öllum verðum eru með skattvísbendingu** .

### <a name="all-prices-include-tax-is-selected-1"></a>Skattur í öllum verðum er valinn

|-|Sala innanlands|Erlent land/svæði þar sem skattur er innifalinn í verði|Erlent land/svæði þar sem skattur er undanskilinn|
|------------------------|---------------|---------------|--------|
|Verð sem birtist í netversluninni|1200|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

Verðið fyrir hvern viðskiptamann breytist eftir staðsetningu þeirra.

### <a name="all-prices-include-tax-is-not-selected-1"></a>Skattur í öllum verðum er ekki valinn

|-|Sala innanlands|Erlent land/svæði þar sem skattur er innifalinn í verði|Erlent land/svæði þar sem skattur er undanskilinn|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

> [!NOTE]
>  **Í öllum verðum er skattvísbendingin** ekki breytt hvernig verð birtast alþjóðlegum viðskiptamönnum.

## <a name="if-you-sell-to-eu-customers"></a>Ef þú selur innan ESB

Mismunandi ESB-lönd/svæði eru með mismunandi staðbundna skatthlutfalla. Ef hins vegar er staðsett í ESB og selt öðrum ESB-löndum/svæðum er hægt að nota staðbundið skatthlutfall í sumum tilvikum.  

Í stjórnandanum **Shopify** skal athuga gátreitinn **Innheimta VSK** í hlutanum **Evrópusambandið** í [**stillingum skatta og skyldna**](https://www.shopify.com/admin/settings/taxes) .

|Innheimta VSK|VSK-hlutfall|
|-|-|
|Undanþága fyrir smáfyrirtæki|Notaðu innlenda skatthlutfallið þitt fyrir alla sölu innan ESB|
|Verslun með einni stöðvun eða tiltekinni skráningu á landi/svæði|Nota VSK-hlutfall lands/svæðis viðskiptamanns|

### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Innheimta VSK sem er stilltur á skráningu í netverslun

Í eftirfarandi dæmi **er kveikt á skattvísbendingu** í öllum verðum. Verðið á vöruspjaldinu er stillt á *1200*.

|-|Sala innanlands|Erlent land/svæði|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1250|
|Prósenta skattur gefa einkunn|20|25|
|Verð þegar gengið er frá kaupum|1200|1250|

Shopify notar skatthlutfallið í erlendu landi/svæði þegar það reiknar lokaverð.

### <a name="collect-vat-set-to-micro-business-exemption"></a>Innheimta VSK sem er stilltur á undanþágu vegna smáfyrirtækja

Í eftirfarandi dæmi **er kveikt á skattvísbendingu** í öllum verðum. Verðið á vöruspjaldinu er stillt á *1200*.

|-|Sala innanlands|Erlent land/svæði með staðbundið skatthlutfall upp á 25 prósent.|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|
|Prósenta skattur gefa einkunn|20|20|
|Verð þegar gengið er frá kaupum|1200|1200|

Shopify notar skatthlutfall innanlands og hunsar skatthlutfallið í erlendu landi/svæði þegar það reiknar út lokaverð.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Innflutningur Shopify pantana seldur til alþjóðlegra viðskiptavina

Ef innheimta á skatta frá mörgum löndum/svæðum verður að skilgreina ákveðna lands-/svæðisstillingu í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það er ástæða fyrir því að þessarar stillingar er krafist. Þegar söluskjal er stofnað í [!INCLUDE[prod_short](../includes/prod_short.md)] [!INCLUDE [prod_short](../includes/prod_short.md)]  skal reikna skatta í stað þess að endurnýta skattana sem fluttir eru inn úr Shopify.

Lands-/svæðisbundnar stillingar eru tilgreindar á síðunni **Shopify Sniðmát** viðskiptamanns. Hægt er að skilgreina sjálfgefin viðskm.nr **.** eða **Sniðmátsnr. viðskiptamanns.**. Í hvoru tilvikinu er tryggt að viðskiptamaðurinn eða sniðmátið hafi eftirfarandi reiti verið fylltir út:

1. **Almennur viðskiptabókunarflokkur** (notaður fyrir erlenda viðskiptavini).
2. **VSK-viðskiptabókunarflokkur** (notaður fyrir erlenda viðskiptavini).
3. **Verð með VSK** (í samræmi við stillingu hér til Shopify hliðar):

* Velja Já **ef** **skattur** er tekinn með í öllum verðum og **Taka með eða án skatts á grundvelli lands** viðskiptamannsins er óvirkur.
* Velja Skal **Nei** ef **skattur** er tekinn með í öllum verðum er óvirkur og **Taka með eða án skatts sem byggir á landi** viðskiptamanns er óvirkur.
* Valið **er Já** ef **skattur sem byggist á landi** viðskiptamanns er virkjaður og landið eða svæðið er skráð í [skattalegu löndunum/svæðunum](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Velja **skal Nei** ef **skattur sem byggður er á er innifalin í landi** viðskiptamanns er virkur og landið/svæðið er ekki skráð í [löndum/svæðum](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions) þar sem skattur er tekinn með.

> [!NOTE]
> Stillingarnar í reitnum **Allt verð með VSK** eru úr sniðmátinu, ekki frá tilteknum viðskiptavini. Mikilvægt er að skilgreina sniðmát viðskiptamanns.

## <a name="other-tax-remarks"></a>Aðrar athugasemdir um skatta

Þó að innflutt Shopify pöntun innihaldi upplýsingar um skatta eru skattarnir endurreiknaðir þegar söluskjal er búið til. Það að endurreikningur merkir að VSK/skattstillingar séu réttar. [!INCLUDE[prod_short](../includes/prod_short.md)]

* Mörg vöruskatts- eða VSK-hlutföll. Til dæmis eru tilteknir vöruflokkar gjaldgengir fyrir lægri skatthlutfalli. Hægt er að nota eiginleikann [hnekking skatts](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) í Shopify. Þegar vörur eru [!INCLUDE[prod_short](../includes/prod_short.md)] fluttar inn og stofnaðar er skattuppsetningin sem tilgreind er á vörusniðmátskótanum á verkstæðinu Shopify notuð. Áður en pantanir eru fluttar inn með slíkum vörum skal uppfæra VSK-vörubókunarflokkinn.  
* Skatthlutföll háð heimilisfangi. Notaðu reitinn **Forgangur skattsvæðis** ásamt **Sniðmát viðskiptavinar** til að skrifa yfir stöðluðu rökin sem fylla út **Skattsvæðiskóða** í söluskjalinu. Reiturinn **Forgangur skattsvæðis** tilgreinir forgang varðandi það hvar aðgerðin á að taka við upplýsingum um landið eða svæðið og fylkið eða héraðið. Þá er samsvarandi skrá í Shopify sniðmátum viðskiptavina auðkennd og **Skattsvæðiskóði**, **Skattskylda** og **VSK-viðsk.bókunarflokkur** eru notaðar þegar söluskjal er búið til.  

## <a name="see-also"></a>Sjá einnig

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
