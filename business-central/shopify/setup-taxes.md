---
title: Setja upp skatta fyrir Shopify tengingu
description: Hvernig á að setja upp skatta í Shopify og Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Setja upp skatta fyrir Shopify tenginguna

Í þessari grein munum við rannsaka hvernig ýmsar stillingar hafa Shopify áhrif á geymsluverð og skatta sem sýna viðskiptamönnum. Við munum einnig sjá um hvernig á að stilla [!INCLUDE[prod_short](../includes/prod_short.md)] til að styðja við stillingarnar í Shopify. Þessari grein er ekki ætlað að vera ítarlegur leiðarvísir um skattlagningu. Hafðu samband við skattyfirvöld á staðnum eða skattalegan fagaðila til að fá frekari upplýsingar.  

Greinin gerir ráð fyrir að þú borgir skatta þegar þú selur vörur á staðnum eða á alþjóðavettvangi.

## Ef þú selur innanlands

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
* Bretland. 

Á mörkuðum eins og þessum er verð á 100 EUR sem tilgreint er á framleiðsluspjaldinu þegar með virðisaukaskatt (VSK). Verðið, með VSK, sýnir viðskiptamanninum í versluninni og við útskráningu.  

Í Bandaríkjunum og Kanada eiga viðskiptavinir ekki von á verði með skatti. Tak er bætt við brottfararstað og **því er yfirleitt slökkt á skattvífæringu** í öllum verðum. Í þessu tilviki er verð $100 tilgreint á framleiðsluspjaldi verð án skatts. Við útritun er sköttum bætt við verðið.

Til að styðja aðstæður þar sem **Skattur er valinn í**  Öllum verðum er fyllt [!INCLUDE[prod_short](../includes/prod_short.md)] út í eftirfarandi reiti á síðu verkstæðisspjaldsins **Shopify** :  

1. Kveikja á verði **með VSK-vífæru** .  
2. Í reitnum **VSK-viðskiptabókunarflokkur** er tilgreindur sá bókunarflokkur sem notaður er fyrir innlenda viðskiptamenn.  

Nú er vöruverð skilgreint í reitunum **Birgðaspjald** eða **Söluverðlisti**, með eða án skatts. Við útflutning á verði Shopify [!INCLUDE [prod_short](../includes/prod_short.md)]  eru innlendir skattar á útreiknuðu verði og þar kemur fram það verð fyrir vöruna í Shopify.

[!Note]
> Þessar stillingar hafa áhrif á útflutning á verði. Þegar pantanir eru fluttar inn úr Shopify kemur stillingin fyrir reitinn **Verð með VSK** úr **sniðmáti** viðskiptamanns á Shopify verkstæðisspjaldinu eða viðskiptamannssniðmátinu fyrir hvert land/svæði. Jafnvel þótt sjálfgefinn viðskiptamaður sé notaður fyrir innfluttar pantanir þarf að fylla út kóta **sniðmáts viðskiptamanns**.

## Ef þú selur alþjóðlega

Í þessum hluta eru skoðaðar stillingar fyrir aðstæður þar sem innheimta þarf skatta þegar selt er til annars lands/svæðis, svo sem annarra landa/svæða í ESB.

 Shopify Eins og er býður tengið aðeins út eitt verð. Shopify er sjálfkrafa lagt á staðbundna skatta, gjaldmiðla og námundun. **Allt verð með skatti** birtir niðurstöður í aðgerðunum sem lýst er í eftirfarandi undirköflum.

### Skattur í öllum verðum er valinn

|-|Sala innanlands|Erlent land/svæði þar sem þú innheimtir skatta|Erlent land/svæði þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|1200|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1200|1200|

Verðið fyrir viðskiptamanninn helst óháð staðsetningu þeirra, en framlegð hefur áhrif á framlegð vegna mismunandi skatthlutfalla eftir löndum/svæðum.

### Skattur í öllum verðum er ekki valinn

|-|Sala innanlands|Erlent land þar sem þú innheimtir skatt|Erlent land þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1000|1000|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1250|1000|

Shopify bætir staðbundnum sköttum við verðið sem skilgreint er á framleiðsluspjaldinu eftir því hvar vörur eru sendar.

## Sveigjanleg verðlagning með skatti

Lönd/svæði krefjast þess að þ.m.t. skattur á verði sé tekinn með. Ef verð á sjálfkrafa að fela í sér skatt er hægt að kveikja á [kvikri verðlagningu](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing)  Shopify með skatti með innifalinni.

Í stjórnandanum **Shopify** skal velja **Taka með eða undanskilja skatt á grundvelli lands** viðskiptamanns í **öðrum mörkuðum - Kjörstillingar** í [**stillingum markaðarins**](https://www.shopify.com/admin/settings/markets) .  

> [!NOTE]
> Þessi stilling hefur ekki áhrif á verð á innlendum mörkuðum, sem stýrt er af **öllum verðum eru með skattvísbendingu** .

### Skattur í öllum verðum er valinn

|-|Sala innanlands|Erlent land/svæði þar sem skattur er innifalinn í verði|Erlent land/svæði þar sem skattur er undanskilinn|
|------------------------|---------------|---------------|--------|
|Verð sem birtist í netversluninni|1200|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

Verðið fyrir hvern viðskiptamann breytist eftir staðsetningu þeirra.

### Skattur í öllum verðum er ekki valinn

|-|Sala innanlands|Erlent land/svæði þar sem skattur er innifalinn í verði|Erlent land/svæði þar sem skattur er undanskilinn|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

> [!NOTE]
>  **Í öllum verðum er skattvísbendingin** ekki breytt hvernig verð birtast alþjóðlegum viðskiptamönnum.

## Ef þú selur innan ESB

Mismunandi ESB-lönd/svæði eru með mismunandi staðbundna skatthlutfalla. Ef hins vegar er staðsett í ESB og selt öðrum ESB-löndum/svæðum er hægt að nota staðbundið skatthlutfall í sumum tilvikum.  

Í stjórnandanum **Shopify** skal athuga gátreitinn **Innheimta VSK** í hlutanum **Evrópusambandið** í [**stillingum skatta og skyldna**](https://www.shopify.com/admin/settings/taxes) .

|Innheimta VSK|VSK-hlutfall|
|-|-|
|Undanþága fyrir smáfyrirtæki|Notaðu innlenda skatthlutfallið þitt fyrir alla sölu innan ESB|
|Verslun með einni stöðvun eða tiltekinni skráningu á landi/svæði|Nota VSK-hlutfall lands/svæðis viðskiptamanns|

### Innheimta VSK sem er stilltur á skráningu í netverslun

Í eftirfarandi dæmi **er kveikt á skattvísbendingu** í öllum verðum. Verðið á vöruspjaldinu er stillt á *1200*.

|-|Sala innanlands|Erlent land/svæði|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1250|
|Prósenta skattur gefa einkunn|20|25|
|Verð þegar gengið er frá kaupum|1200|1250|

### Innheimta VSK sem er stilltur á undanþágu vegna smáfyrirtækja

Í eftirfarandi dæmi **er kveikt á skattvísbendingu** í öllum verðum. Verðið á vöruspjaldinu er stillt á *1200*.

|-|Sala innanlands|Erlent land/svæði með staðbundið skatthlutfall upp á 25 prósent.|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|
|Prósenta skattur gefa einkunn|20|20|
|Verð þegar gengið er frá kaupum|1200|1200|

Shopify notar skatthlutfall innanlands og hunsar skatthlutfallið í erlendu landi/svæði þegar það reiknar út lokaverð.

## Innflutningur Shopify pantana seldur til alþjóðlegra viðskiptavina

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

## Aðrar athugasemdir um skatta

Þó að innflutt Shopify pöntun innihaldi upplýsingar um skatta eru skattarnir endurreiknaðir þegar söluskjal er búið til. Það að endurreikningur merkir að VSK/skattstillingar séu réttar. [!INCLUDE[prod_short](../includes/prod_short.md)]

* Mörg vöruskatts- eða VSK-hlutföll. Til dæmis eru tilteknir vöruflokkar gjaldgengir fyrir lægri skatthlutfalli. Hægt er að nota eiginleikann [hnekking skatts](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) í Shopify. Þegar vörur eru [!INCLUDE[prod_short](../includes/prod_short.md)] fluttar inn og stofnaðar er skattuppsetningin sem tilgreind er á vörusniðmátskótanum á verkstæðinu Shopify notuð. Áður en pantanir eru fluttar inn með slíkum vörum skal uppfæra VSK-vörubókunarflokkinn.  
* Skatthlutföll háð heimilisfangi. Notaðu reitinn **Forgangur skattsvæðis** ásamt **Sniðmát viðskiptavinar** til að skrifa yfir stöðluðu rökin sem fylla út **Skattsvæðiskóða** í söluskjalinu. Reiturinn **Forgangur skattsvæðis** tilgreinir forgang varðandi það hvar aðgerðin á að taka við upplýsingum um landið eða svæðið og fylkið eða héraðið. Þá er samsvarandi skrá í Shopify sniðmátum viðskiptavina auðkennd og **Skattsvæðiskóði**, **Skattskylda** og **VSK-viðsk.bókunarflokkur** eru notaðar þegar söluskjal er búið til.  

## Sjá einnig

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
