---
title: Settu upp ófrádráttarbæran virðisaukaskatt
description: Þessi grein útskýrir hvernig á að stilla ófrádráttarbæran VSK í Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="set-up-nondeductible-vat"></a>Settu upp ófrádráttarbæran virðisaukaskatt

Ófrádráttarbær virðisaukaskattur (VSK) er virðisaukaskattur sem kaupandi ber að greiða, en hann er ekki frádráttarbær frá eigin virðisaukaskattsskyldu kaupanda. Fyrirtæki geta yfirleitt endurheimt virðisaukaskatt af kaupum á vörum og þjónustu sem tengist atvinnustarfsemi þeirra. Hins vegar, í sumum tilfellum, ber fyrirtæki virðisaukaskatt sem er ekki frádráttarbær. Þessar aðstæður eru venjulega tengdar staðbundnum reglugerðum og geta verið mismunandi eftir löndum/svæðum. Hins vegar er líkanið að nota ófrádráttarbæran eða frádráttarbæran virðisaukaskatt að hluta til svipað. Þú getur notað hlutfallslegan virðisaukaskatt til að reikna út virðisaukaskatt þegar það er frádráttarbær og ófrádráttarbær virðisaukaskattur.

Almennt er ekki hægt að draga virðisaukaskatt fyrir sum innkaup vegna eftirfarandi þátta:

- **Tegund vöru eða þjónustu sem keypt er** – virðisaukaskattur er að öllu leyti eða að hluta ódreginn samkvæmt ákvæðum laga um vörur eins og bíla, farsíma og mat sem keyptur er á veitingastöðum.
- **Að hluta til frádráttarbær hlutfallslegur virðisaukaskattur** – Virðisaukaskattur er hlutfallslegur eftir hlutfalli milli þeirra söluaðgerða sem virðisaukaskattur ber af og allra aðgerða sem unnin hefur verið. Ekki er hægt að draga virðisaukaskatt sem fer yfir þetta hlutfall.

Vegna þess að það getur verið erfitt að vita hvar og hvernig hlutur er notaður, verður þú að hafa samband við skattyfirvöld í þínu landi/héraði til að ákvarða hvort tiltekið hlutfall af virðisaukaskatti sé frádráttarbært byggt á sögulegum gögnum. 

> [!IMPORTANT]
> Þessi alþjóðlegi eiginleiki er fáanlegur í öllum löndum með virkan VSK **nema í Belgíu, Ítalíu og Noregi**. Þessar staðsetningar hafa þegar núverandi staðbundna eiginleika og verða uppfærðar í framtíðinni. Ekki keyra þennan eiginleika í þessum löndum vegna þess að uppfærsluferlið er ekki til.

## <a name="use-nondeductible-vat"></a>Notaðu ófrádráttarbæran virðisaukaskatt

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **VAT Setup** og veldu síðan tengda hlekkinn.
2. Veldu gátreitinn **Virkja ófrádráttarbæran VSK** .

    > [!IMPORTANT]
    > Eftir að þú hefur virkjað ófrádráttarbæran virðisaukaskatt geturðu ekki slökkt á honum, vegna þess að eiginleikinn gæti falið í sér breytingar á gögnum og gæti komið af stað uppfærslu á sumum gagnagrunnstöflum. Microsoft mælir eindregið með því að þú kveikir og prófar þennan eiginleika fyrst í sandkassaumhverfinu áður en þú virkjar hann í framleiðsluumhverfinu.

3. Stilltu hvernig kerfið mun meðhöndla virðisaukaskattsgildi sem ekki eru frádráttarbær.

    1. Í reitnum **Notaðu fyrir vörukostnað**  skal tilgreina hvort óafdráttarbær virðisaukaskattur verði að bæta við vörukostnaðinn þegar þú kaupir vörur. Að öðrum kosti mun ófrádráttarbær virðisaukaskattur ekki hafa áhrif á vörukostnaðinn og heildarupphæðin verður aðeins skráð á aðalbókarstigi.
    2. Veljið gátreitinn **Nota fyrir fastafjárkostnað** til að bæta óafdráttarbærum virðisaukaskatti við eignakostnaðinn þegar þú kaupir nýja fastafjármuni. Að öðrum kosti mun ófrádráttarbær virðisaukaskattur ekki hafa áhrif á kostnað fastafjármuna og heildarupphæðin verður aðeins skráð á aðalbókarstigi.
    3. Veljið gátreitinn **Nota fyrir vinnukostnað** til að tilgreina að óafdráttarbær virðisaukaskattur verði að bæta við verkkostnaðinn þegar þú kaupir vörur fyrir verkið. Að öðrum kosti mun ófrádráttarbær virðisaukaskattur ekki hafa áhrif á vinnukostnaðinn og heildarupphæðin verður aðeins skráð á aðalbókarstigi.
    4. Veldu **Sýna ekki deed. VSK In Lines** gátreitur til að tilgreina að ófrádráttarbær virðisaukaskattur verði að sýna á skjalalínusíðum til að auðvelda meðhöndlun virðisaukaskattsupphæða.

## <a name="use-the-nondeductible-vat-percentage"></a>Notaðu ófrádráttarbæra virðisaukaskattsprósentu

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **VSK-bókunaruppsetning** og veldu síðan tengda hlekkinn.
2. Á síðunni **VSK-bókunaruppsetning**  skaltu stilla reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Leyfa ófrádráttarbæran VSK | Tilgreindu hvort ófrádráttarbær virðisaukaskattur komi til greina fyrir núverandi samsetningu virðisaukaskatts fyrirtækjabókunarflokks og vörubókunarflokks virðisaukaskatts. |
    | % ófrádráttarbærs VSK | Tilgreindu hlutfall færsluupphæðarinnar sem virðisaukaskattur er ekki lagður á. |
    | Reikningur ófrádráttarbærs innskatts | Tilgreindu reikninginn sem er tengdur virðisaukaskattsupphæðinni sem er ekki dregin frá vegna tegundar vöru eða þjónustu sem er keypt. |

    > [!NOTE]
    > Til að hafa aðalbókarfærslur sem nota sérstaka reikninginn í stað sölu-/innkaupareikningsins geturðu annaðhvort skilið eftir  **Ófrádráttarbær virðisaukaskattsreikningur innkaupa** reitinn auðan eða stilltu reitinn **G/L Account** .

3. Veldu **Í lagi**.

> [!NOTE]
> Ekki er hægt að nota óinnleyst virðisaukaskatt ásamt ófrádráttarbærum virðisaukaskatti.
>
> Ekki nota sama **VSK auðkenni** gildi fyrir bæði venjulegan VSK þar sem **Ófrádráttarbær VSK %** reiturinn er stillt á **0** (núll) og venjulegan VSK þar sem **Ófrádráttarbær VSK %** reiturinn er stilltur á ekki -núll gildi. Að öðrum kosti verður heildarupphæð ófrádráttarbærrar virðisaukaskatts ranglega reiknuð.

## <a name="see-also"></a>Sjá einnig .

[Fjármálastjórnun](finance.md)  
[Hönnunarupplýsingar: Ófrádráttarbær VSK](design-details-nondeductible-vat.md)  
[Nota ófrádráttarbæran VSK](finance-how-use-non-deductible-vat.md)  
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
