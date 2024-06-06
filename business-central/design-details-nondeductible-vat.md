---
title: Hönnunarupplýsingar - Ófrádráttarbær VSK
description: Í þessari grein eru upplýsingar um virðisaukaskatt sem ekki er frádráttarbær (VSK) sem kaupandi greiðir en er ekki frádráttarbært frá eigin VSK-skuld kaupanda.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Upplýsingar um hönnun: Ófrádráttarbær VSK

Virðisaukaskattur sem ekki er frádráttarbær (VSK) er VSK sem kaupandi greiðir en er ekki frádráttarbær frá eigin VSK-skuld kaupanda. Þar sem erfitt getur verið að vita hvar og hvernig vara er notuð þarf að hafa samband við skattyfirvöld í viðkomandi landi eða svæði til að ákvarða hvort tiltekin prósenta af VSK sé frádráttarbær. Jafnvel þó vitað sé að tiltekin prósenta af VSK sé ekki frádráttarbær eru mismunandi gerðir til að **meðhöndla upphæðir sem ekki eru frádregnar þar sem þær tengjast vörum** og **eignum**.

## Skilyrði fyrir notkun VSK sem ekki er frádráttarbær

Til að nota og bóka frádráttarbæran VSK skal fylgja þessum skrefum.

1. Á síðunni **VSK-uppsetning** skal velja Gera ófrádráttarbæran VSK **virkan** til að gera aðgerðina virka.
2. Á síðunni **VSK-bókunargrunnur** skal velja hvaða VSK-bókunarflokkar geta notað ófrádráttarbæran VSK.

## Dæmi

Fyrir eftirfarandi dæmi er VSK sem ekki er frádráttarbær og eftirfarandi uppsetningu er lokið:

- Reiturinn **VSK-vörubókunarflokkur** er stilltur á **NDVAT**.
- Á síðunni **VSK-bókunargrunnur** :

    - **NDVAT er stillt** sem VSK-vörubókunarflokkur og **INNLENT** er stilltur sem VSK-viðskiptabókunarflokkur.
    -  **Gildi VSK-kennisins** verður að vera einstakt.
    - Reiturinn **VSK%** er stilltur á **25**.
    - Reiturinn **Leyfa ófrádráttarbæran VSK** er stilltur á **Leyfa**.
    - Reiturinn **Ófrádráttarbær VSK %** er stilltur á **100**.
    - Reiturinn **Teg. VSK-útreiknings** er stilltur á **Venjulegur VSK**.
    - Aðeins VSK-reikningur sölu og VSK-reikningur innkaupa eru grunnstilltir.

Öll dæmin nota vörur og eignir þar sem VSK-vörubókunarflokkurinn er **NDVAT**.

### Vörur

Ný vara hefur **NDVAT stillt** sem VSK-vörubókunarflokk. Í innkaupaskjalinu, **Magn** = **1** og **Innk.verð án VSK** = **1,000,00**.

Óháð þeim valkosti sem notaður er er útkoman í **VSK-færslunni** sú sama.

| Gerð fylgiskjals | Gerð | Grunnur | Upphæð | Ófrádráttarbær VSK-stofn | Ófrádráttarbær VSK-upphæð |
|---|---|---|---|---|---|
| Reikningsfæra | Innkaup | 0.00 | 0.00 | 1,000.00 | 250.00 |

Upplýsingarnar eru birtar í **virðisfærslunum**.

> [!NOTE]
> Hægt er að virkja reitinn **Nota fyrir vörukostnað** á síðunni **VSK-uppsetning** .

#### Notkun fyrir vörukostnað er ekki virk

| Tegund birgðafærslu | Færslugerð | Kostnaðarupphæð (raunveruleg) | Magn birgðafærslu |
|---|---|---|---|
| Innkaup | Beinn kostnaður | 1,000.00 | 1 |

#### Notkun fyrir vörukostnað er virk

| Tegund birgðafærslu | Færslugerð | Kostnaðarupphæð (raunveruleg) | Magn birgðafærslu |
|---|---|---|---|
| Innkaup | Beinn kostnaður | 1,250.00 | 1 |

### Eignir

Ný eign hefur kostnaðarreikning stofnkostnaðar stillt á að nota **NDVAT** sem VSK-vörubókunarflokk. Í innkaupaskjalinu, **Magn** = **1** og **Innk.verð án VSK** = **1,000,00**.

Óháð þeim valkosti sem notaður er er útkoman í **VSK-færslunni** sú sama.

| Gerð fylgiskjals | Gerð | Grunnur | Upphæð | Ófrádráttarbær VSK-stofn | Ófrádráttarbær VSK-upphæð |
|---|---|---|---|---|---|
| Reikningsfæra | Innkaup | 0.00 | 0.00 | 1,000.00 | 250.00 |

Upplýsingarnar eru birtar í **Eignafærslunum**.

> [!NOTE]
> Hægt er að virkja reitinn **Nota fyrir eignakostnað** á síðunni **VSK-uppsetning** .

#### Notkun fyrir eignakostnað er ekki virkjuð

| Gerð fylgiskjals | Eignabókunartegund | Upphæð | VSK-upphæð |
|---|---|---|---|
| Reikningsfæra | Kaupverð | 1,000.00 | 250.00 |

#### Notkun fyrir eignakostnað er virkjuð

| Gerð fylgiskjals | Eignabókunartegund | Upphæð | VSK-upphæð |
|---|---|---|---|
| Reikningsfæra | Kaupverð | 1,000.00 | 250.00 |
| Reikningsfæra | Kaupverð | 250.00 | 0.00 |

## Sjá einnig .

[Setja upp ófrádráttarbæran VSK](finance-setup-nondeductible-vat.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
