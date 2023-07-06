---
title: Nota ekki frádráttarbæran virðisaukaskatt
description: Í greininni er útskýrt hvernig nýta og tilkynna ófrádráttarbæran virðisaukaskatt.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="use-non-deductible-vat"></a><a name="use-non-deductible-vat"></a><a name="use-non-deductible-vat"></a>Nota ekki frádráttarbæran virðisaukaskatt

Í greininni er útskýrt hvernig nýta og tilkynna ófrádráttarbæran virðisaukaskatt.

## <a name="create-a-purchase-invoice-with-non-deductible-vat"></a><a name="create-a-purchase-invoice-with-non-deductible-vat"></a><a name="create-a-purchase-invoice-with-non-deductible-vat"></a>Stofna innkaupareikning með ófrádráttarbæran virðisaukaskatt

1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 3](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið, fara í **Innkaupareikningur** og velja síðan viðkomandi tengil.
2. Veljið  **nýtt**  til að stofna innkaupareikning og Færið inn viðeigandi upplýsingar í reikningshausinn.
3.  **Stofnið nýja línu af hvaða gerð sem er, í hlutanum línur**, á grundvelli VSK-viðskiptabókunarflokks og VSK-vörubókunarflokksins þar sem notandi samskipar ófrádráttarbæran VSK.
4.  **Í reitina magn**  og  **innkaupsverð**  skal slá inn viðeigandi gildi.

    Ef Sýningin hefur  **ekki verið valin. Í gátreitnum**  **VSK á uppsetningarsíðu**  VSK eru upphæðirnar í  **reitunum Ófrádráttarbær VSK**  og  **Ófrádráttarbær VSK**  -upphæðir reiknaðar út samkvæmt  **reitnum Ófrádráttarbær**  VSK á  **uppsetningarsíðu**  VSK-bókunar.

5. Bóka skal reikninginn.

## <a name="create-a-purchase-order-with-non-deductible-vat"></a><a name="create-a-purchase-order-with-non-deductible-vat"></a><a name="create-a-purchase-order-with-non-deductible-vat"></a>Stofna innkaupapöntun með ófrádráttarbæran virðisaukaskatt

1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 3](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Teiknið, Færið inn  **innkaupapantanir**  og veljið síðan tengda tengilinn.
2. Veljið  **nýtt**  til að stofna innkaupapöntun og Færið inn viðeigandi upplýsingar í fylgiskjalshausinn.
3.  **Stofnið nýja línu af hvaða gerð sem er, í hlutanum línur**, á grundvelli VSK-viðskiptabókunarflokks og VSK-vörubókunarflokksins þar sem notandi samskipar ófrádráttarbæran VSK.
4.  **Í reitina magn**  og  **innkaupsverð**  skal slá inn viðeigandi gildi.

    Ef Sýningin hefur  **ekki verið valin. Í gátreitnum**  **VSK á uppsetningarsíðu**  VSK eru upphæðirnar í  **reitunum Ófrádráttarbær VSK**  og  **Ófrádráttarbær VSK**  -upphæðir reiknaðar út samkvæmt  **reitnum Ófrádráttarbær**  VSK á  **uppsetningarsíðu**  VSK-bókunar.

5. Innkaupapöntunin er bókuð.

## <a name="adjust-rounded-vat-amounts-before-document-posting"></a><a name="adjust-rounded-vat-amounts-before-document-posting"></a><a name="adjust-rounded-vat-amounts-before-document-posting"></a>Leiðrétta slétta VSK-upphæðir fyrir bókun skjals

Ef VSK-upphæðir eru ekki sléttaðar með sama hætti í umhverfi þínu og í ytra bókhaldskerfinu (upprunalegu reikningsskjalinu) er hægt að leiðrétta VSK-upphæðina áður en skjalið er bókað. Ef gera á leiðréttingu er þessum skrefum fylgt áður en skjalið er bókað.

1. Í aðgerðarúðunni skal velja  **talnagögn**.
2. Ef þú ert að vinna með innkaupareikning, Fylgdu þessum skrefum:

    1.  **Á fastlínuflipanum**, Veljið VSK-upphæð, án frádráttar VSK-upphæðar.
    2. Stillið gildin sem þú þarft úr upprunalega skjalinu og lokaðu síðan síðunni upplýsingar  **um**  innkaupareikning.

3.  Ef unnið er við innkaupapöntunina er eftirfarandi þrepum fylgt:

    1.  **Á flipanum Reikningsfæra**  er valið  **Nei. af skattlínum**  til að opna  **síðuna VSK-upphæðir** .
    2. Veljið VSK-upphæð eða ófrádráttarbæra VSK sem óskað er að leiðrétta.
    3. Færið inn gildin sem þarf að koma úr upprunalega skjalinu,  **síðan er VSK-upphæðarlínur**  gerðar og síðan er síðan lokað á upplýsingar  **um**  innkaupapöntun.

Ef nota á leiðréttingar VSK-upphæða verður að virkja leiðréttingarnar.  **Í reitnum leyfður mismunur á Fjárhagsgrunni er færð inn leyfileg**  Upphæð VSK til leiðréttingar í  **reitnum Hámarksvsk-Uppsetning** . Á  **uppsetningarsíðu**  innkaupa & lánardrottna er VALIÐ  **Leyfa VSK-mismun**.

Hægt er að leiðrétta gildi  **VSK-upphæðar**  og  **ófrádráttarbærra VSK-upphæðarreita** .  **Reiturinn frádráttarbært VSK-upphæð**  er afleiðing þessara tveggja gilda. Upphæðin sem færð er í  **reitinn Ófrádráttarbær**  Upphæð getur ekki verið meira en sú upphæð sem færð er inn í  **reitinn VSK-upphæð** .  **Reiturinn**  hámarkvat-VSK-mismunur  **í fjárhagsgrunni**  virkar ekki á sjálfstæðan hátt fyrir frádráttarbæran og ófrádráttarbæra VSK-upphæðir á síðum á talnagögnum þegar VSK-upphæðir eru leiðrétt.

> [!IMPORTANT]
> Ekki má nota ófrádráttarbæran virðisaukaskatt á reikninga fyrirframgreiðslunnar.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Fjármálastjórnun](finance.md)  
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Setja upp ófrádráttarbæran virðisaukaskatt](finance-setup-nondeductible-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
