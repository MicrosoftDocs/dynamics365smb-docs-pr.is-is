---
title: Setja upp ófrádráttarbæran virðisaukaskatt
description: Í greininni er útskýrt hvernig skilgreina á ófrádráttarbæran virðisaukaskatt í Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="set-up-non-deductible-vat" />Setja upp ófrádráttarbæran virðisaukaskatt

Ófrádráttarbær Virðisauki (VSK) er sá Innskattur sem kaupandi greiðir, en það er ekki frádráttarbært frá eigin skattalegu ábyrgð kaupanda. Fyrirtæki geta yfirleitt endurheimt virðisaukaskatt af innkaupum á vörum og þjónustu sem tengjast atvinnustarfsemi. En í sumum aðstæðum er Innskattur VSK sem ekki er frádráttarbær. Þessar aðstæður eru að jafnaði í tengslum við staðbundnar reglugerðir og geta verið frábrugðnar hér á landi. Líkanið um að nota hvorki frádráttarbæran eða hluta frádráttarbæran virðisaukaskatt er þó svipað. Hægt er að nota hlutfallslegan VSK til að reikna VSK þegar um frádráttarbæran frádrátt og frádreginn frádrátt er að ræða.

Almennt er ekki hægt að draga virðisaukaskatt vegna einhverra innkaupa vegna eftirfarandi þátta:

- **Tegund vöru eða þjónustu sem keypt**  er – virðisaukaskatt að fullu eða að hluta til án frádráttar samkvæmt ákvæðum laganna um vörur eins og bíla, farsíma og matvöru sem keyptar eru á veitingastöðum.
- **VSK**  -Virðisaukaskattur að hluta – VSK er metinn í samræmi við Hlutfallið milli þeirra söluaðgerða sem VSK er skuldajafnað fyrir og allar aðgerðir sem hafa verið framkvæmdar. VSK sem ekki er umfram Þetta hlutfall má ekki draga.

Þar sem það getur verið erfitt að vita hvar og hvernig vara er notuð þarf að hafa samband við skattyfirvöld í þínu landi til að ákvarða hvort tiltekin prósenta af VSK er frádráttarbær samkvæmt sögulegum gögnum. 

> [!IMPORTANT]
> Þessi hnattræna eiginleiki er tiltækur í öllum löndum með VSK  **sem er virkjaður nema fyrir Belgíu, Ítalíu, Noreg og Spán**. Þessi staðsetur hefur þegar staðbundna eiginleika og verður uppfærður í framtíðinni. Ekki keyra þennan eiginleika í þessum löndum þar sem uppfærsluferlið er ekki til.

## <a name="use-non-deductible-vat" />Nota ekki frádráttarbæran virðisaukaskatt

1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **VSK-uppsetningu** og velja síðan tengda tengilinn.
2.  **Veljið gátreitinn Virkja Ófrádrátt VSK** .

    > [!IMPORTANT]
    > Eftir að VSK er gerður Ófrádráttarbær er ekki hægt að slökkva á honum, þar sem aðgerðin gæti innihaldið breytingar á gögnum og gæti hafið uppfærslu á sumum gagnagrunnstöflum. Microsoft mælir eindregið með því að fyrst skuli virkja og prófa þennan eiginleika í sandkassa-umhverfinu áður en hann er gerður virkur í framleiðsluumhverfinu.

3. Skilgreina hvernig kerfið mun meðhöndla ófrádráttarbærar VSK-gildi.

    1.  **Tilgreinið í reitnum notkun fyrir vörukostnað**  hvort bæta þurfi ÓFRÁDRÁTTARBÆRUM VSK við vörukostnaðinn við innkaup á vörum. Að öðrum kosti mun Ófrádráttarbær INNSKATTUR ekki hafa áhrif á vörukostnað og skal þá heildarfjárhæðin aðeins skráð á fjárhagsstig.
    2.  **Velja gátreitinn nota fyrir gátreitinn kostnaðarverð**  til að bæta ÓFRÁDRÁTTARBÆR VSK við kostnað eignarinnar þegar nýjar eignir hafa verið innkomnar í eignina. Að öðrum kosti mun Ófrádráttarbær INNSKATTUR ekki hafa áhrif á eignakostnaðinn og skal þá heildarfjárhæðin aðeins skráð á fjárhagstigið.
    3.  **Gátreiturinn nota fyrir Starfskostnað**  er valinn til að tilgreina að bæta þurfi við ófrádráttarbæran VSK í vinnslukostnaðinn þegar vörur eru innkomnar vegna vinnslunnar. Að öðrum kosti mun Ófrádráttarbær ÚTSKATTUR ekki hafa áhrif á atvinnukostnaðinn og verður þá heildarupphæðin aðeins skráð á fjárhagstigi.
    4. Veljið Sýna sem ekki er búið að  **Dekkja. Gátreitur VSK í línum**  til að tilgreina að sýna verði ófrádráttarbæran virðisaukaskatt á síðum fylgiskjalslína til að auðvelda MEÐHÖNDLUN VSK-upphæða.

## <a name="use-the-non-deductible-vat-percentage" />Nota ófrádráttarbæran VSK-prósentu

1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **VSK-bókunaruppsetningu** og velja síðan tengda tengilinn.
2.  **Á síðunni VSK-bókunargrunnur**  eru svæðin stillt eftir eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Leyfa ófrádráttarbæran VSK | Tilgreinið hvort Ófrádráttarbær VSK sé fyrir gildandi samsetningu VSK-viðskiptabókunarflokks og VSK-vörubókunarflokks. |
    | % ófrádráttarbærs VSK | Tilgreinið prósentu færsluupphæðar sem VSK er ekki notuð á. |
    | Reikningur ófrádráttarbærs innskatts | Tilgreinið lykilinn sem tengist VSK-upphæðinni sem er ekki dregin frá vegna þeirrar tegundar vöru eða þjónustu sem keypt er. |

    > [!NOTE]
    > Til að hafa fjárhagsfærslur (fjárhags-) færslur sem nota tileinkaða lykilinn, í stað sölu-/innkaupareiknings, er annað hvort hægt að skilja reitinn Reikningur með  **ófrádráttarbæran innskatt auðan eða stilla**  reitinn Fjárhagsreikningur  **.** 

3. Veldu  **í lagi**.

> [!NOTE]
> Ekki er hægt að nota áætlaðan VSK ásamt óskattskyldum VSK.
>
> Ekki nota sama  **VSK-kenni**  fyrir bæði venjulegan VSK þar sem  **reiturinn án frádráttar**  er stilltur á  **0**  (núll) og venjulegur VSK þar sem  **reiturinn Ófrádráttarbær VSK%**  er stilltur á ekki núll-gildi. Annars er heildarupphæð ófrádráttarbærs VSK ranglega reiknuð.

## <a name="see-also" />Sjá einnig .

[Fjármálastjórnun](finance.md)  
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
