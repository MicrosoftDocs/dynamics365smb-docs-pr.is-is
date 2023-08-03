---
title: Upplýsingar um hönnun-ekki frádráttarbærni VSK
description: 'Í þessari grein er að finna upplýsingar um ófrádráttarbæran virðisauka (VAT) sem kaupanda ber að veita, en það er ekki frádráttarbært frá eigin skattalegu ábyrgð kaupanda.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
---

# <a name="design-details-non-deductible-vat"></a>Hönnunarupplýsingar: án frádráttar VSK

Ófrádráttarbær Virðisauki (VSK) er sá Innskattur sem kaupandi greiðir, en það er ekki frádráttarbært frá eigin skattalegu ábyrgð kaupanda. Þar sem það getur verið erfitt að vita hvar og hvernig vara er notuð þarf að hafa samband við skattyfirvöld í heimalandi þínu eða svæði til að ákvarða hvort tiltekið hlutfall af VSK sé frádráttarbært. Jafnvel þegar vitað er að tiltekið hlutfall VSK er ekki frádráttarbært eru mismunandi líkön til meðhöndlunar án frádráttar eins og þau eru tengd  **vörum**  og  **eignum**.

## <a name="prerequisites-for-using-non-deductible-vat"></a>Forsendur fyrir notkun ófrádráttarbærs VSK

Fylgdu þessum skrefum til að nota og bókið ófrádráttarbæran virðisaukaskatt.

1.  **Á síðunni VSK-Grunnur**  er valið  **VIRKJA án frádráttar VSK**  til að virkja aðgerðina.
2.  **Á síðunni VSK-bókunaruppsetning**  er hægt að velja hvaða VSK-Bókunarflokkar geta notað ófrádráttarbæran virðisaukaskatt.

## <a name="examples"></a>Dæmi

Fyrir eftirfarandi dæmi er Ófrádráttarbær VSK virkjaður og eftirfarandi uppsetningu er lokið:

-  **Reiturinn VSK-vörubókunarflokkur**  er stilltur á  **ndvat**.
-  **Á síðunni VSK-bókunaruppsetning** :

    - **NDVAT**  er stillt sem VSK-vörubókunarflokkur, og  **Innlendur**  er stilltur sem VSK-viðskiptabókunarflokkur.
    -  **VSK-kennigildið**  verður að vera einkvæmt.
    -  **Reiturinn VSK%**  er stilltur á  **25**.
    -  **Reiturinn leyfð ÓFRÁDRÁTTARBÆR VSK**  er stilltur á  **Leyfa**.
    -  **Reiturinn ÓFRÁDRÁTTARBÆR VSK%**  er stilltur á  **100**.
    -  **Reiturinn Tegund**  VSK-útreiknings er stilltur á  **venjulegan VSK**.
    - Aðeins VSK-lykill og VSK-lykill innkaupa eru samskipaðir.

Öll Dæmin nota vörur og eignir þar sem VSK-vörubókunarflokkurinn er  **ndvat**.

### <a name="items"></a>Vörur

Ný vara er með  **ndvat**  -STILLT sem VSK-vörubókunarflokk. Í kaupskjali, magn 1 og innkaupsverð Útlán án VSK  **1.000,00** = **.**  **·** = **·**

Án tillits til þess hvaða valkostur er notaður eru niðurstöðurnar í  **VSK-færslunni**  þær sömu.

| Gerð fylgiskjals | Gerð | Grunnur | Upphæð | Ófrádráttarbær VSK-stofn | Ófrádráttarbær VSK-upphæð |
|---|---|---|---|---|---|
| Reikningsfæra | Innkaup | 0.00 | 0.00 | 1,000.00 | 250.00 |

Upplýsingarnar eru sýndar í  **virðisfærslunum**.

> [!NOTE]
> Hægt er að  **virkja reitinn nota fyrir vörukostnað**  á  **uppsetningarsíðu**  VSK.

#### <a name="use-for-item-cost-isnt-enabled"></a>Notkun fyrir vörukostnað er ekki virk

| Tegund birgðafærslu | Færslutegund | Kostnaðarupphæð (raunveruleg) | Magn birgðafærslu |
|---|---|---|---|
| Innkaup | Beinn kostnaður | 1,000.00 | 1 |

#### <a name="use-for-item-cost-is-enabled"></a>Notkun fyrir vörukostnað er virkjuð

| Tegund birgðafærslu | Færslutegund | Kostnaðarupphæð (raunveruleg) | Magn birgðafærslu |
|---|---|---|---|
| Innkaup | Beinn kostnaður | 1,250.00 | 1 |

### <a name="fixed-assets"></a>Eignir

Ný eign hefur þann stofnkostnað stofnkostnaðar að nota  **ndvat**  sem VSK-vörubókunarflokk. Í kaupskjali, magn 1 og innkaupsverð Útlán án VSK  **1.000,00** = **.**  **·** = **·**

Án tillits til þess hvaða valkostur er notaður eru niðurstöðurnar í  **VSK-færslunni**  þær sömu.

| Gerð fylgiskjals | Gerð | Grunnur | Upphæð | Ófrádráttarbær VSK-stofn | Ófrádráttarbær VSK-upphæð |
|---|---|---|---|---|---|
| Reikningsfæra | Innkaup | 0.00 | 0.00 | 1,000.00 | 250.00 |

Upplýsingarnar eru sýndar í  **eignafærslum**.

> [!NOTE]
> Hægt er að  **virkja svæðið fyrir kostnað**  eignar á  **síðunni VSK-Grunnur** .

#### <a name="use-for-fixed-asset-cost-isnt-enabled"></a>Notkun fyrir Eignakostnað er ekki virk

| Gerð fylgiskjals | Eignabókunartegund | Upphæð | VSK-upphæð |
|---|---|---|---|
| Reikningsfæra | Kaupverð | 1,000.00 | 250.00 |

#### <a name="use-for-fixed-asset-cost-is-enabled"></a>Notkun fyrir Eignakostnað er virkjuð

| Gerð fylgiskjals | Eignabókunartegund | Upphæð | VSK-upphæð |
|---|---|---|---|
| Reikningsfæra | Kaupverð | 1,000.00 | 250.00 |
| Reikningsfæra | Kaupverð | 250.00 | 0.00 |

## <a name="see-also"></a>Sjá einnig .

[Setja upp ófrádráttarbæran VSK](finance-setup-nondeductible-vat.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
