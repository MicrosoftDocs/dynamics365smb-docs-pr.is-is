---
title: Setja upp ófrádráttarbæran VSK
description: Þessi grein útskýrir hvernig á að grunnstilla ófrádráttarbæran VSK í Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 08/13/2024
ms.custom: bap-template
ms.reviewer: bholtorf
---

# Setja upp ófrádráttarbæran VSK

Ófrádráttarbær virðisaukaskattur (VSK) er VSK sem kaupandi greiðir en er ekki frádráttarbær frá eigin VSK-skuld kaupanda. Fyrirtæki geta venjulega endurheimt VSK af innkaupum á vörum og þjónustu sem tengist starfsemi fyrirtækisins. Í sumum tilvikum stofna fyrirtæki VSK sem er ekki frádráttarbært. Þessar aðstæður tengjast yfirleitt reglugerðum og geta verið mismunandi milli landa/svæða. Hins vegar er líkanið með því að nota ófrádráttarbæran eða frádráttarbæran VSK að hluta til svipað. Hægt er að nota hlutfallslegan VSK til að reikna VSK þegar um er að ræða frádráttarbæran og ófrádráttarbæran VSK.

Almennt er ekki hægt að draga FRÁ VSK fyrir sum innkaup vegna eftirfarandi þátta:

- **Tegund vara eða þjónusta sem keypt**  er – VSK er að fullu eða ekki hefur verið færður að hluta til samkvæmt lögum um vörur eins og bíla, farsíma og mat sem keyptur er á veitingastöðum.
- **AÐ hluta frádreginn VSK með prósentustigi – VSK**  er metinn samkvæmt hlutfalli söluaðgerða sem VSK er skuldaður fyrir og allra framkvæmdra aðgerða. EKKI er hægt að draga frá VSK sem er hærri en þetta hlutfall.

Þar sem erfitt getur verið að vita hvar og hvernig vara er notuð skal hafa samband við skattyfirvöld í viðkomandi landi/svæði. Þeir geta hjálpað til við að ákvarða hvort hægt sé að draga frá tiltekna prósentu af VSK á grundvelli eldri gagna.

> [!IMPORTANT]
> Þessi altæki eiginleiki er tiltækur í öllum löndum með VSK **sem er virkur nema Belgía, Ítalía og Noregur**. Þessar staðfæringar hafa þegar staðbundna eiginleika og verða uppfærðar í framtíðinni. Ekki keyra þessa aðgerð í þessum löndum vegna þess að uppfærsluferlið er ekki til.

## Nota ófrádráttarbæran VSK

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **VSK-grunn** og velja síðan tengda tengja.
2. Velja skal Gátreitinn **Gera ófrádráttarbær VSK**  kakassa virkan.

    > [!IMPORTANT]
    > Þegar búið er að gera ófrádráttarbær VSK virka er ekki hægt að slökkva á henni þar sem eiginleikinn getur innihaldið breytingar á gögnum og hafið uppfærslu á sumum gagnagrunnstöflum. Microsoft mælir eindregið með því að þessi eiginleiki sé gerður virkur og prófaður fyrst í sandkassaumhverfinu áður en hann er virkjaður í framleiðsluumhverfinu.

3. Grunnstilla hvernig farið er [!INCLUDE [prod_short](includes/prod_short.md)] með ófrádráttarbær VSK-gildi.

    1. Í reitnum **Nota fyrir vörukostnað** er tilgreint hvort bæta þurfi ófrádráttarbærum VSK við vörukostnað þegar vörur eru keyptar. Annars hefur ófrádráttarbæri VSK ekki áhrif á vörukostnað og heildarupphæðin er aðeins skráð á fjárhagur stigi.
    2. Velja skal gátreitinn **Nota fyrir fasta eign kostnaðarverð** til að bæta ófrádráttarbærum VSK við fastan eign kostnað þegar nýjar eignir eru keyptar. Annars hefur ófrádráttarbæri VSK ekki áhrif á fastan eign kostnað og heildarupphæðin er aðeins skráð á fjárhagur stigi.
    3. Velja skal gátreitinn **Nota fyrir verkkostnað** til að tilgreina að bæta þurfi ófrádráttarbærum VSK við verkkostnað þegar vörur eru keyptar fyrir verkið. Annars hefur ófrádráttarbæri VSK ekki áhrif á verkkostnað og heildarupphæðin er aðeins skráð á fjárhagur stigi.
    4. Velja skal Reitinn **Sýna óreikningsf. Í gátreitnum VSK í línum** til að tilgreina að sýna þurfi ófrádráttarbæran VSK á línusíðum fylgiskjals til að auðvelda hagræðingar vsk-upphæða.

## Nota ófrádráttarbæra VSK-prósentu

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **VSK-bókunargrunn og** velja síðan viðeigandi tengja.
2. Á síðunni **VSK-bókunargrunnur** eru reitirnir stilltir eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Leyfa ófrádráttarbær VSK** | Tilgreina skal hvort ófrávíkjanlegur VSK telst vera með gildandi samsetningu VSK-viðskiptabókunarflokks og VSK-vörubókunarflokks. |
    | **ófrádráttarbær VSK%** | Tilgreina prósentu færsluupphæðarinnar sem VSK er ekki jafnaður við. |
    | **Reikningur fyrir VSK-frádrátt innskatts** | Tilgreina reikning sem tengist VSK-upphæðinni sem ekki er dregin frá vegna tegundar vöru eða þjónustu sem er keypt. |

    > [!NOTE]
    > Eigi að fjárhagur (fjárhags) færslur sem nota sérstakan reikning í stað sölu-/innkaupareiknings er hægt að hafa **reitinn Reikningur ófrádráttarbærra innskattsreiknings** auðan eða stilla **reitinn Fjárhagsreikningur** .

3. Valið er **Í lagi**.

> [!NOTE]
> Ekki er hægt að nota áætlaðan VSK ásamt ófrádráttarbær VSK.
>
> Ekki skal nota sama **VSK-kennigildi** fyrir venjulegan VSK þar sem reiturinn **ófrádráttarbær VSK %** er stilltur **á 0** (núll) og venjulegan VSK þar sem reiturinn **ófrádráttarbær VSK %** er stilltur á gildi sem er ekki núll. Annars er heildarupphæðin ófrádráttarbær VSK ranglega reiknuð.

## Sjá einnig .

[Fjármálastjórnun](finance.md)  
[Upplýsingar um hönnun: Ófrádráttarbær VSK](design-details-nondeductible-vat.md)  
[Nota ófrádráttarbæran VSK](finance-how-use-non-deductible-vat.md)  
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
