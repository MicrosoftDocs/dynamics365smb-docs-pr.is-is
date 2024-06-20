---
title: Setja upp ófrádráttarbæran VSK
description: Þessi grein útskýrir hvernig á að grunnstilla ófrádráttarbæran VSK í Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
ms.reviewer: bholtorf
---

# <a name="set-up-nondeductible-vat"></a>Setja upp ófrádráttarbæran VSK

Ófrádráttarbær virðisaukaskattur (VSK) er VSK sem kaupandi greiðir en er ekki frádráttarbær frá eigin VSK-skuld kaupanda. Fyrirtæki geta venjulega endurheimt VSK af innkaupum á vörum og þjónustu sem tengist starfsemi fyrirtækisins. Í sumum tilvikum stofna fyrirtæki VSK sem er ekki frádráttarbært. Þessar aðstæður tengjast yfirleitt reglugerðum og geta verið mismunandi milli landa/svæða. Hins vegar er líkanið með því að nota ófrádráttarbæran eða frádráttarbæran VSK að hluta til svipað. Hægt er að nota hlutfallslegan VSK til að reikna VSK þegar um er að ræða frádráttarbæran og ófrádráttarbæran VSK.

Almennt er ekki hægt að draga FRÁ VSK fyrir sum innkaup vegna eftirfarandi þátta:

- **Tegund vara eða þjónusta sem keypt**  er – VSK er að fullu eða ekki hefur verið færður að hluta til samkvæmt lögum um vörur eins og bíla, farsíma og mat sem keyptur er á veitingastöðum.
- **AÐ hluta frádreginn VSK með prósentustigi – VSK**  er metinn samkvæmt hlutfalli söluaðgerða sem VSK er skuldaður fyrir og allra framkvæmdra aðgerða. EKKI er hægt að draga frá VSK sem er hærri en þetta hlutfall.

Þar sem erfitt getur verið að vita hvar og hvernig vara er notuð skal hafa samband við skattyfirvöld í viðkomandi landi/svæði. Þeir geta hjálpað til við að ákvarða hvort hægt sé að draga frá tiltekna prósentu af VSK á grundvelli eldri gagna.

> [!IMPORTANT]
> Þessi altæki eiginleiki er tiltækur í öllum löndum með VSK **sem er virkur nema Belgía, Ítalía og Noregur**. Þessar staðfæringar hafa þegar staðbundna eiginleika og verða uppfærðar í framtíðinni. Ekki keyra þessa aðgerð í þessum löndum vegna þess að uppfærsluferlið er ekki til.

## <a name="use-nondeductible-vat"></a>Nota ófrádráttarbæran VSK

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **VSK-grunn** og velja síðan viðeigandi tengil.
2. Velja skal gátreitinn **Gera ófrádráttarbæran VSK-gátreit** virkan.

    > [!IMPORTANT]
    > Þegar VSK sem er ekki frádreginn hefur verið gerður virkur er ekki hægt að slökkva á honum þar sem aðgerðin gæti falið í sér breytingar á gögnum og átt frumkvæði að uppfærslu á sumum gagnagrunnstöflum. Microsoft mælir eindregið með því að þessi eiginleiki sé gerður virkur og prófaður fyrst í sandkassaumhverfinu áður en hann er virkjaður í framleiðsluumhverfinu.

3. Grunnstilla hvernig farið er [!INCLUDE [prod_short](includes/prod_short.md)] með ófrádráttarbær VSK-gildi.

    1. Í reitnum **Nota fyrir vörukostnað** er tilgreint hvort bæta þurfi ófrádráttarbærum VSK við vörukostnað þegar vörur eru keyptar. Annars hefur ófrádráttarbæri VSK ekki áhrif á vörukostnað og heildarupphæðin er aðeins skráð á fjárhagsstigi.
    2. Velja skal gátreitinn **Nota fyrir eignakostnað** til að bæta ófrádregnum VSK við eignakostnaðinn þegar nýjar eignir eru keyptar. Annars hefur ófrádráttarbæri VSK ekki áhrif á kostnað eignar og heildarupphæðin er aðeins skráð á fjárhagsstigi.
    3. Velja skal gátreitinn **Nota fyrir verkkostnað** til að tilgreina að bæta þurfi ófrádráttarbærum VSK við verkkostnað þegar vörur eru keyptar fyrir verkið. Annars hefur ófrádráttarbæri VSK ekki áhrif á verkkostnað og heildarupphæðin er aðeins skráð á fjárhagsstigi.
    4. Velja skal Reitinn **Sýna óreikningsf. Í gátreitnum VSK í línum** til að tilgreina að sýna þurfi ófrádráttarbæran VSK á línusíðum fylgiskjals til að auðvelda hagræðingar vsk-upphæða.

## <a name="use-the-nondeductible-vat-percentage"></a>Nota ófrádráttarbæra VSK-prósentu

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **VSK-bókunargrunn og** velja síðan viðeigandi tengil.
2. Á síðunni **VSK-bókunargrunnur** eru reitirnir stilltir eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Leyfa ófrádráttarbæran VSK | Tilgreina skal hvort ófrávíkjanlegur VSK telst vera með gildandi samsetningu VSK-viðskiptabókunarflokks og VSK-vörubókunarflokks. |
    | % ófrádráttarbærs VSK | Tilgreina prósentu færsluupphæðarinnar sem VSK er ekki jafnaður við. |
    | Reikningur ófrádráttarbærs innskatts | Tilgreina reikning sem tengist VSK-upphæðinni sem ekki er dregin frá vegna tegundar vöru eða þjónustu sem er keypt. |

    > [!NOTE]
    > Ef fjárhagsfærslur (fjárhags) sem nota sérstakan reikning í stað sölu-/innkaupareiknings er hægt að hafa **reitinn Reikningur ófrádráttarbærra innskattsreiknings** auðan eða stilla **reitinn Fjárhagsreikningur** .

3. Valið er **Í lagi**.

> [!NOTE]
> Ekki er hægt að nota áætlaðan VSK ásamt VSK sem er ekki frádreginn.
>
> Ekki skal nota sama **VSK-kennigildi fyrir venjulegan VSK þar sem** reiturinn Vsk% **frádráttur** er stilltur **á 0** (núll) og venjulegan VSK þar sem **reiturinn VSK%** sem er ekki frádráttarbært er stilltur á gildið sem er ekki núll. Annars er heildarupphæð VSK sem er ekki frádráttarbær reiknuð ranglega.

## <a name="see-also"></a>Sjá einnig .

[Fjármálastjórnun](finance.md)  
[Upplýsingar um hönnun: Ófrádráttarbær VSK](design-details-nondeductible-vat.md)  
[Nota ófrádráttarbæran VSK](finance-how-use-non-deductible-vat.md)  
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
